---
title: Asynchroner Rückrufabschluss
description: Beschreibt, wie der Anbieter Rückrufe asynchron bedienen kann.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/12/2018
ms.topic: article
ms.openlocfilehash: f2262e803d1ee3d071538dc6e520517c6fd7b800c4d7fdc4a7404748b9f9f0dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127950"
---
# <a name="asynchronous-callback-handling"></a>Asynchrone Rückrufbehandlung

Wenn ein Client mit den Dateien und Verzeichnissen unterhalb des Virtualisierungsstamms des Anbieters interagiert, führen diese Interaktionen in der Regel dazu, dass die Rückrufe des Anbieters aufgerufen werden.  ProjFS ruft Anbieterrückrufe auf, indem eine Nachricht aus dem Kernelmodus an die ProjFS-Benutzermodusbibliothek gesendet wird, wo ein Arbeitsthread die Nachricht empfängt und den entsprechenden Rückruf aufruft.  Sobald der Rückruf zurückgegeben wurde, wartet der Arbeitsthread darauf, dass eine andere Nachricht aus dem Kernelmodus eintrifft.  Wenn alle Arbeitsthreads mit der Ausführung des Anbieterrückrufcodes ausgelastet sind, wird jede weitere Client-E/A, die einen Rückruf auslöst, blockiert, bis ein Arbeitsthread verfügbar ist, um die Nachricht zu empfangen und den entsprechenden Rückruf aufzurufen.  Wenn ein Anbieter gestartet wird, kann er die Anzahl der Arbeitsthreads angeben, die ProjFS für Dienstrückrufe erstellen soll, über den _Optionsparameter_ von **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)**.  Ein Anbieter kann die Effizienz der Nachrichten empfangenden Arbeitsthreads verbessern, indem er seine Rückrufe asynchron bedient.

> Wenn der Anbieter den _Optionsparameter_ für **PrjStartVirtualizing** nicht angibt oder 0 für den ConcurrentThreadCount-Member des _Optionsparameters_ angibt, verwendet ProjFS die Anzahl logischer Prozessoren im System für den Wert concurrentThreadCount.
>
> Wenn der Anbieter nicht den _Optionsparameter_ für **PrjStartVirtualizing** angibt oder 0 für den PoolThreadCount-Member des _Optionsparameters_ angibt, verwendet ProjFS den doppelten Wert von ConcurrentThreadCount für den Wert von PoolThreadCount.

Ein Anbieterdienst ruft asynchron zurück, indem er HRESULT_FROM_WIN32(ERROR_IO_PENDING) aus seinen Rückrufen zurückgibt und diese später mit **[PrjCompleteCommand abschließt.](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjcompletecommand)**  Ein Anbieter, der Rückrufe asynchron verarbeitet, sollte auch den Rückrufabbruch unterstützen, indem er den **[PRJ_CANCEL_COMMAND_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb)** Rückruf implementiert.

Wenn ProjFS den Rückruf eines Anbieters aufruft, identifiziert es den spezifischen Aufruf des Rückrufs mithilfe des CommandId-Members des _callbackData-Parameters_ des Rückrufs.  Wenn der Anbieter entscheidet, diesen Rückruf asynchron zu verarbeiten, muss er den Wert des CommandId-Members speichern und HRESULT_FROM_WIN32(ERROR_IO_PENDING) aus dem Rückruf zurückgeben.  Nachdem der Anbieter die Verarbeitung des Rückrufs abgeschlossen hat, ruft er **PrjCompleteCommand** auf und übergibt den gespeicherten Bezeichner im _commandId-Parameter._  Dadurch wird ProjFS mitgeteilt, welcher Rückrufaufruf abgeschlossen wurde.

Ein Anbieter, der die **PRJ_CANCEL_COMMAND_CB** Rückruf implementiert, muss nachverfolgen, welche Rückrufe noch nicht abgeschlossen wurden.  Wenn der Anbieter diesen Rückruf empfängt, gibt er an, dass die E/A, die den Aufruf eines dieser Rückrufe verursacht hat, entweder explizit abgebrochen wurde oder weil der Thread, für den er ausgegeben wurde, beendet wurde. Der Anbieter sollte die Verarbeitung des durch CommandId identifizierten Rückrufaufrufs so bald wie möglich abbrechen.

> Obwohl ProjFS **PRJ_CANCEL_COMMAND_CB** für eine bestimmte CommandId erst aufruft, nachdem der abzubrechende Rückruf aufgerufen wurde, können der Abbruch und der ursprüngliche Aufruf gleichzeitig in einem Multithreadanbieter ausgeführt werden.  Der Anbieter muss in der Lage sein, diese Situation ordnungsgemäß zu behandeln.

Das folgende Beispiel ist eine Version des Beispiels für das Thema [Enumerating Files and Directories ( Dateien und Verzeichnisse aufzählen),](enumerating-files-and-directories.md) geändert, um die asynchrone Rückrufbehandlung zu veranschaulichen.

```C++
typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

typedef struct MY_ENUM_ENTRY {
    MY_ENUM_ENTRY* Next;
    PWSTR Name;
    BOOLEAN IsDirectory;
    INT64 FileSize;
} MY_ENUM_ENTRY;

typedef struct MY_ENUM_SESSION {
    GUID EnumerationId;
    PWSTR SearchExpression;
    USHORT SearchExpressionMaxLen;
    BOOLEAN SearchExpressionCaptured;
    MY_ENUM_ENTRY* EnumHead;
    MY_ENUM_ENTRY* LastEnumEntry;
    BOOLEAN EnumCompleted;
} MY_ENUM_SESSION;

typedef struct MY_ENUM_PARAMS {
    GUID EnumerationId;
    PRJ_DIR_ENTRY_BUFFER_HANDLE DirEntryBufferHandle;
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT NamespaceVirtualizationContext;
    INT32 CommandId;
    PRJ_CALLBACK_DATA_FLAGS Flags;
    WCHAR SearchExpression[1];
} MY_ENUM_PARAMS;

// Prototype for the enumeration worker routine.  In this example this is a
// ThreadProc.  See https://msdn.microsoft.com/library/windows/desktop/ms686736.aspx
DWORD WINAPI MyGetEnumCallbackWorker(_In_ LPVOID parameter);

#define ROLLBACK_NONE           0
#define ROLLBACK_PARAM_ALLOC    1
#define ROLLBACK_TRACK_ENUM     2

HRESULT
MyGetEnumCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ const GUID* enumerationId,
    _In_opt_z_ PCWSTR searchExpression,
    _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
    )
{
    UINT rollback = ROLLBACK_NONE;

    // This example creates a thread to run the enumeration in.  The provider
    // can access callbackData only while the callback is running, so we copy
    // out the fields that the worker thread will need.
    MY_ENUM_PARAMS* enumParams = NULL;
    size_t bufSize = sizeof(MY_ENUM_PARAMS);

    // Allocate enough space for the parameter buffer and the search expression
    // string plus a terminating NULL character.
    if (searchExpression != NULL)
    {
        bufSize += (wcslen(searchExpression) + 1) * sizeof(WCHAR);
    }
    else
    {
        // We'll store "*" as the search expression in this case.
        bufSize += 2 * sizeof(WCHAR);
    }

    enumParams = (MY_ENUM_PARAMS*) calloc(1, bufSize);

    if (enumParams == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto RollbackOnError;
    }

    // enumParams allocated.
    rollback = ROLLBACK_PARAM_ALLOC;

    // Copy the search expression into our parameter buffer.
    if (searchExpression != NULL)
    {
        wcsncpy_s(enumParams->SearchExpression,
                  wcslen(searchExpression),
                  searchExpression,
                  wcslen(searchExpression));
    }
    else
    {
        wcsncpy_s(enumParams->SearchExpression, 1, "*", 1);
    }

    // Copy the other parameters into our parameter buffer.
    enumParams->EnumerationId = enumerationId;
    enumParams->DirEntryBufferHandle = dirEntryBufferHandle;
    enumParams->NamespaceVirtualizationContext = callbackData->NamespaceVirtualizationContext
    enumParams->CommandId = callbackData->CommandId;
    enumParams->Flags = callbackData->Flags;

    // MyTrackEnumForCancellation is a routine the provider might implement to
    // track active enumeration callbacks in case they are cancelled.  It stores
    // the CommandId for the callback in some structure.
    hr = MyTrackEnumForCancellation(callbackData->CommandId);

    if (FAILED(hr))
    {
        goto RollbackOnError;
    }

    // Enum callback tracked.
    rollback = ROLLBACK_TRACK_ENUM;

    // Create the worker thread.
    HANDLE workerThread = NULL;
    workerThread = CreateThread(NULL,
                                0,
                                MyGetEnumCallbackWorker,
                                enumParams,
                                0
                                NULL);

    // We'll treat failure to create the thread as a low-resources error.
    if (workerThread == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto RollbackOnError;
    }

    // Return pending to signal that we'll complete the enumeration later.
    return HRESULT_FROM_WIN32(ERROR_IO_PENDING);

RollbackOnError:

    // Clean up manually.  Note the fall-through structure of the switch, and that
    // we clean up in reverse order.
    switch(rollback)
    {
    case ROLLBACK_TRACK_ENUM:
        // MyUntrackEnumForCancellation removes the CommandId for the callback
        // from the structure that MyTrackEnumForCancellation put it in.
        MyUntrackEnumForCancellation(callbackData->CommandId);

    case ROLLBACK_PARAM_ALLOC:
        free(enumParams);

    default:
        break;
    }

    return hr;
}

DWORD
WINAPI
MyGetEnumCallbackWorker(
    _In_ LPVOID parameter
)
{
    HRESULT hr = S_OK;
    MY_ENUM_PARAMS* enumParams = (MY_ENUM_PARAMS*) parameter;

    // MyCheckEnumForCancellation is a routine the provider might implement to
    // check whether a pended enumeration callback has been cancelled.  Even
    // though the enumeration has been cancelled, ProjFS will still call the
    // provider's end-enumeration callback.  This allows general cleanup, such
    // as tearing down the enumeration session, to always happen in that callback.
    if (MyCheckEnumForCancellation(enumParams->CommandId))
    {
        // The operation has been cancelled.  Clean up and get out.
        free(enumParams);
        return 0;
    }

    // MyGetEnumSession is a routine the provider might implement to find
    // information about the enumeration session that it first stored
    // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
    //
    // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
    // already retrieved a list of the items in the backing store located at
    // callbackData->FilePathName, sorted them using PrjFileNameCompare()
    // to determine collation order, and stored the list in session->EnumHead.
    MY_ENUM_SESSION* session = NULL;
    session = MyGetEnumSession(enumParams->EnumerationId);

    if (session == NULL)
    {
        hr = HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        goto CompleteCallback;
    }

    if (!session->SearchExpressionCaptured ||
        (enumParams->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
    {
        if (wcsncpy_s(session->SearchExpression,
                      session->SearchExpressionMaxLen,
                      enumParams->SearchExpression,
                      wcslen(enumParams->SearchExpression)))
        {
            // Failed to copy the search expression; perhaps the provider
            // could try reallocating session->SearchExpression.
        }

        session->SearchExpressionCaptured = TRUE;
    }

    MY_ENUM_ENTRY* enumHead = NULL;

    // We have to start the enumeration from the beginning if we aren't
    // continuing an existing session or if the caller is requesting a restart.
    if (((session->LastEnumEntry == NULL) &&
         !session->EnumCompleted) ||
        (enumParams->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
    {
        // Ensure that if the caller is requesting a restart we reset our
        // bookmark of how far we got in the enumeration.
        session->LastEnumEntry = NULL;

        // In case we're restarting ensure we don't think we're done.
        session->EnumCompleted = FALSE;

        // We need to start considering items from the beginning of the list
        // retrieved from the backing store.
        enumHead = session->EnumHead;
    }
    else
    {
        // We are resuming an existing enumeration session.  Note that
        // session->LastEnumEntry may be NULL.  That is okay; it means
        // we got all the entries the last time this callback was invoked.
        // Returning S_OK without adding any new entries to the
        // enumParams->DirEntryBufferHandle buffer signals ProjFS that the
        // enumeration has returned everything it can.
        enumHead = session->LastEnumEntry;
    }

    if (enumHead == NULL)
    {
        // There are no items to return.  Remember that we've returned everything
        // we can.
        session->EnumCompleted = TRUE;
    }
    else
    {
        MY_ENUM_ENTRY* thisEntry = enumHead;
        while (thisEntry != NULL)
        {
            // We'll insert the entry into the return buffer if it matches
            // the search expression captured for this enumeration session.
            if (PrjFileNameMatch(thisEntry->Name, session->SearchExpression))
            {
                PRJ_FILE_BASIC_INFO fileBasicInfo = {};
                fileBasicInfo.IsDirectory = thisEntry->IsDirectory;
                fileBasicInfo.FileSize = thisEntry->FileSize;

                // Format the entry for return to ProjFS.
                if (S_OK != PrjFillDirEntryBuffer(thisEntry->Name,
                                                  &fileBasicInfo,
                                                  enumParams->DirEntryBufferHandle))
                {
                    // We couldn't add this entry to the buffer; remember where we left
                    // off for the next time we're called for this enumeration session.
                    session->LastEnumEntry = thisEntry;
                    hr = S_OK;

                    goto CompleteCallback;
                }
            }

            thisEntry = thisEntry->Next;
        }

        // We reached the end of the list of entries; remember that we've returned
        // everything we can.
        session->EnumCompleted = TRUE;
    }

CompleteCallback:

    // Signal ProjFS that we've completed this callback.  Since this is an enumeration
    // we use the extendedParameters parameter to PrjCompleteCommand.
    PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS extendedParams = {};
    extendedParams.CommandType = PRJ_COMPLETE_COMMAND_TYPE_ENUMERATION;
    extendedParams.enumeration.DirEntryBufferHandle = enumParams->DirEntryBufferHandle;

    PrjCompleteCommand(enumParams->NamespaceVirtualizationContext,
                       enumParams->CommandId,
                       hr,
                       &extendedParams);

    MyUntrackEnumForCancellation(enumParams->CommandId);

    free(enumParams);

    // ThreadProc returns 0 on successful completion.
    return 0;
}
```

Hier ist ein kurzes Beispiel PRJ_CANCEL_COMMAND_CB, das mit dem vorherigen Beispielcode funktioniert.

```C++
void
MyCancelCommandCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData
)
{
    // MyMarkEnumForCancellation is a routine the provider might implement to
    // mark a pended enumeration callback as cancelled.  If the given CommandId
    // is not found, it is not an error.  It may not yet have been tracked or
    // it may already have completed and been untracked.
    MyMarkEnumForCancellation(callbackData->CommandId);
}
```