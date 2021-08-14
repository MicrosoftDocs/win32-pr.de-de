---
title: Auflisten von Dateien und Verzeichnissen
description: Beschreibt, wie ein ProjFS-Anbieter an der Verzeichnisenumeration teilnimmt.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/25/2018
ms.topic: article
ms.openlocfilehash: 606b379e206cdbc64726e0ea97aed34e00f5253ecbffb7f8b7d42469b0cbb5fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792813"
---
# <a name="enumerating-files-and-directories"></a>Auflisten von Dateien und Verzeichnissen

Wenn ein Anbieter zum ersten Mal einen Virtualisierungsstamm erstellt, ist er auf dem lokalen System leer.  Das heißt, dass noch keines der Elemente im Sicherungsdatenspeicher auf dem Datenträger zwischengespeichert wurde.  Während jedes Element geöffnet wird, wird es zwischengespeichert, aber bis es geöffnet wird, ist es nur im sicherungsenden Datenspeicher vorhanden.

Da nicht geöffnete Elemente nicht lokal vorhanden sind, würde die normale Verzeichnisenumeration ihre Existenz für den Benutzer nicht preisgeben.  Daher muss der Anbieter an der Verzeichnisenumeration teilnehmen, indem er Informationen zu Elementen in seinem Sicherungsdatenspeicher an ProjFS zurückgibt.  ProjFS führt die Informationen des Anbieters mit dem Inhalt des lokalen Dateisystems zusammen, um dem Benutzer eine einheitliche Liste der Inhalte eines Verzeichnisses zu präsentieren.

## <a name="directory-enumeration-callbacks"></a>Rückrufe von Verzeichnisenumerationen

Um an der Verzeichnisenumeration teilzunehmen, muss der Anbieter die **[Rückrufe PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** und **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** implementieren.  Wenn ein Verzeichnis im Virtualisierungsstamm des Anbieters aufzählt wird, führt ProjFS die folgenden Aktionen aus:

1. ProjFS ruft den **PRJ_START_DIRECTORY_ENUMERATION_CB-Rückruf** des Anbieters auf, um eine Enumerationssitzung zu starten.

    Im Rahmen der Verarbeitung dieses Rückrufs sollte der Anbieter die Ausführung der Enumeration vorbereiten.  Beispielsweise sollte der Speicher belegt werden, den er möglicherweise benötigt, um den Fortschritt der Enumeration im sicherungsenden Datenspeicher nachzuverfolgen.

    ProjFS identifiziert das Verzeichnis, das im **FilePathName-Member** des _callbackData-Parameters_ des Rückrufs aufzählt wird.  Dies wird als Pfad relativ zum Virtualisierungsstamm angegeben.  Wenn sich beispielsweise der Virtualisierungsstamm unter befindet `C:\virtRoot` und das Verzeichnis, das aufzählt `C:\virtRoot\dir1\dir2` wird, ist, enthält der **FilePathName-Member** `dir1\dir2` .  Der Anbieter bereitet die Aufzählung dieses Pfads im Sicherungsdatenspeicher vor.  Abhängig von den Funktionen des Sicherungsspeichers eines Anbieters kann es sinnvoll sein, die Sicherungsspeicherenumeration im **PRJ_START_DIRECTORY_ENUMERATION_CB** Rückruf auszuführen.

    Da mehrere Enumerationen parallel im gleichen Verzeichnis auftreten können, verfügt jeder Enumerationsrückruf über ein _enumerationId-Argument,_ damit der Anbieter die Rückrufaufrufe einer einzelnen Enumerationssitzung zuordnen kann.

    Wenn der Anbieter S_OK aus dem **PRJ_START_DIRECTORY_ENUMERATION_CB** Rückruf zurückgibt, muss er alle Enumerationssitzungsinformationen beibehalten, die er besitzt, bis ProjFS den **PRJ_END_DIRECTORY_ENUMERATION_CB** Rückruf mit dem gleichen Wert für _enumerationId_ aufruft.  Wenn der Anbieter einen Fehler von **PRJ_START_DIRECTORY_ENUMERATION_CB** zurückgibt, ruft ProjFS den **PRJ_END_DIRECTORY_ENUMERATION_CB** Rückruf für diese _enumerationId_ nicht auf.

1. ProjFS ruft den **PRJ_GET_DIRECTORY_ENUMERATION_CB-Rückruf** des Anbieters ein oder mehrere Male auf, um den Verzeichnisinhalt vom Anbieter abzurufen.

    Als Reaktion auf diesen Rückruf gibt der Anbieter eine sortierte Liste von Elementen aus seinem Sicherungsdatenspeicher zurück.

    Der Rückruf stellt möglicherweise einen Suchausdruck in seinem _searchExpression-Parameter_ bereit, den der Anbieter verwendet, um die Ergebnisse der Enumeration zu beschneiden.  Wenn _searchExpression_ NULL ist, gibt der Anbieter alle Einträge im Verzeichnis zurück, das aufgeführt wird.  Wenn es sich nicht um NULL handelt, kann der Anbieter **[prjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** verwenden, um zu bestimmen, ob im Ausdruck Platzhalter vorhanden sind.  Falls vorhanden, verwendet der Anbieter **[PrjFileNameMatch,](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** um zu bestimmen, ob ein Eintrag im Verzeichnis mit dem Suchausdruck übereinstimmt.

    Der Anbieter sollte den Wert von _searchExpression_ beim ersten Aufruf dieses Rückrufs erfassen.  Er verwendet den erfassten Wert bei jedem nachfolgenden Aufruf des Rückrufs in derselben Enumerationssitzung, es sei denn, PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN wird im Feld **Flags** des _callbackData-Parameters_ des Rückrufs festgelegt.  In diesem Fall sollte der Wert von _searchExpression_ erneut gekapselt werden.

    Wenn im Sicherungsspeicher keine übereinstimmenden Einträge vorhanden sind, gibt der Anbieter einfach S_OK aus dem Rückruf zurück.  Andernfalls formatiert der Anbieter jeden übereinstimmenden Eintrag aus seinem Sicherungsspeicher in eine **[PRJ_FILE_BASIC_INFO-Struktur](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** und verwendet dann **[PrjFillDirEntryBuffer,](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** um den Puffer auszufüllen, der vom _dirEntryBufferHandle-Parameter_ des Rückrufs bereitgestellt wird.  Der Anbieter fügt einträge so lange hinzu, bis alle hinzugefügt wurden, oder bis **PrjFillDirEntryBuffer** HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) zurückgibt.  Anschließend gibt der Anbieter S_OK aus dem Rückruf zurück.  Beachten Sie, dass der Anbieter die Einträge dem _dirEntryBufferHandle-Puffer_ in der richtigen Sortierreihenfolge hinzufügen muss.  Der Anbieter sollte **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** verwenden, um die richtige Sortierreihenfolge zu bestimmen.

    > Der Anbieter muss einen Wert für den **IsDirectory-Member** von **PRJ_FILE_BASIC_INFO** bereitstellen.  Wenn **IsDirectory** FALSE ist, muss der Anbieter auch einen Wert für den **FileSize-Member** bereitstellen.
    >
    > Wenn der Anbieter keine Werte für die Member **CreationTime,** **LastAccessTime,** **LastWriteTime** und **ChangeTime** anpasst, verwendet ProjFS die aktuelle Systemzeit.
    >
    > ProjFS verwendet alle FILE_ATTRIBUTE, die der Anbieter im **FileAttributes-Member** festlegt, mit Ausnahme von FILE_ATTRIBUTE_DIRECTORY; der richtige Wert für FILE_ATTRIBUTE_DIRECTORY im **FileAttributes-Member** entsprechend dem angegebenen Wert des **IsDirectory-Members** festgelegt wird.

    Wenn **PrjFillDirEntryBuffer** HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) zurückgibt, bevor dem Anbieter die Einträge zum Hinzufügen ausgehen, muss der Anbieter den Eintrag nachverfolgen, den er beim Empfang des Fehlers hinzugefügt hat.  Wenn ProjFS das nächste Mal den **PRJ_GET_DIRECTORY_ENUMERATION_CB** Rückruf für dieselbe Enumerationssitzung aufruft, muss der Anbieter das Hinzufügen von Einträgen zum _dirEntryBufferHandle-Puffer_ mit dem Eintrag fortsetzen, den er hinzufügen wollte.

    > Wenn der Sicherungsspeicher symbolische Verknüpfungen unterstützt, muss der Anbieter **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** verwenden, um den Puffer auszufüllen, der vom _dirEntryBufferHandle-Parameter_ des Rückrufs bereitgestellt wird.  **PrjFillDirEntryBuffer2** unterstützt eine zusätzliche Puffereingabe, mit der der Anbieter angeben kann, dass der Enumerationseintrag ein symbolischer Link und sein Ziel ist.  Andernfalls verhält er sich wie oben für **PrjFillDirEntryBuffer** beschrieben.  Im folgenden Beispiel wird **PrjFillDirEntryBuffer2** verwendet, um die Unterstützung symbolischer Verknüpfungen zu veranschaulichen.
    >
    > Beachten Sie, dass **PrjFillDirEntryBuffer2** ab Windows 10 Version 2004 unterstützt wird.  Ein Anbieter sollte das Vorhandensein von **PrjFillDirEntryBuffer2** prüfen, z. B. mit **[getProcAddress.](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**

    ```C++
    typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

    typedef struct MY_ENUM_ENTRY {
        MY_ENUM_ENTRY* Next;
        PWSTR Name;
        BOOLEAN IsDirectory;
        INT64 FileSize;
        BOOLEAN IsSymlink;
        PWSTR SymlinkTarget;
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

    HRESULT
    MyGetEnumCallback(
        _In_ const PRJ_CALLBACK_DATA* callbackData,
        _In_ const GUID* enumerationId,
        _In_opt_z_ PCWSTR searchExpression,
        _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
        )
    {
        // MyGetEnumSession is a routine the provider might implement to find
        // information about the enumeration session that it first stored
        // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
        //
        // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
        // already retrieved a list of the items in the backing store located at
        // callbackData->FilePathName, sorted them using PrjFileNameCompare()
        // to determine collation order, and stored the list in session->EnumHead.
        MY_ENUM_SESSION* session = NULL;
        session = MyGetEnumSession(enumerationId);

        if (session == NULL)
        {
            return HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        }

        if (!session->SearchExpressionCaptured ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            if (searchExpression != NULL)
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              searchExpression,
                              wcslen(searchExpression)))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            else
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              "*",
                              1))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            session->SearchExpressionCaptured = TRUE;
        }

        MY_ENUM_ENTRY* enumHead = NULL;

        // We have to start the enumeration from the beginning if we aren't
        // continuing an existing session or if the caller is requesting a restart.
        if (((session->LastEnumEntry == NULL) &&
             !session->EnumCompleted) ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
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
            // dirEntryBufferHandle buffer signals ProjFS that the enumeration
            // has returned everything it can.
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

                    // If our backing store says this is really a symbolic link,
                    // set up to tell ProjFS that it is a symlink and what its
                    // target is.
                    PRJ_EXTENDED_INFO extraInfo = {};
                    if (thisEntry->IsSymlink)
                    {
                        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
                        extraInfo.Symlink.TargetName = thisEntry->SymlinkTarget;
                    }

                    // Format the entry for return to ProjFS.
                    HRESULT fillResult = PrjFillDirEntryBuffer2(dirEntryBufferHandle,
                                                                thisEntry->Name,
                                                                &fileBasicInfo,
                                                                thisEntry->IsSymlink ? &extraInfo : NULL);

                    if (fillResult == HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER))
                    {
                        // We couldn't add this entry to the buffer; remember where we left
                        // off for the next time we're called for this enumeration session.
                        session->LastEnumEntry = thisEntry;
                        return S_OK;
                    }
                }

                thisEntry = thisEntry->Next;
            }

            // We reached the end of the list of entries; remember that we've returned
            // everything we can.
            session->EnumCompleted = TRUE;
        }

        return S_OK;
    }
    ```

1. ProjFS ruft den **PRJ_END_DIRECTORY_ENUMERATION_CB-Rückruf** des Anbieters auf, um die Enumerationssitzung zu beenden.

    Der Anbieter sollte alle Bereinigungen durchführen, die er ausführen muss, um die Enumerationssitzung zu beenden, z. B. die Zuordnung des Speichers, der im Rahmen der Verarbeitung **PRJ_START_DIRECTORY_ENUMERATION_CB** zugeordnet ist.
