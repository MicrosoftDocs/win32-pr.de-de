---
title: Auflisten von Dateien und Verzeichnissen
description: Beschreibt, wie ein projfs-Anbieter an der verzeichnisenumeration teilnimmt.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/25/2018
ms.topic: article
ms.openlocfilehash: e0712ceb927388b090a84a89f80f0e2d3a1befbb
ms.sourcegitcommit: 80d74c0bf4fc402865a1ad223480abe1ce4d1115
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2020
ms.locfileid: "103723992"
---
# <a name="enumerating-files-and-directories"></a>Auflisten von Dateien und Verzeichnissen

Wenn ein Anbieter erstmalig einen virtualisierungsstamm erstellt, ist er auf dem lokalen System leer.  Das heißt, keines der Elemente im Sicherungsdaten Speicher wurde noch auf dem Datenträger zwischengespeichert.  Beim Öffnen eines Elements wird es zwischengespeichert, aber bis ein Element geöffnet ist, ist es nur im Sicherungsdaten Speicher vorhanden.

Da nicht geöffnete Elemente nicht lokal vorhanden sind, gibt die normale Verzeichnis Enumeration dem Benutzer nicht offen.  Daher muss der Anbieter an der verzeichnisenumeration teilnehmen, indem er Informationen über Elemente in seinem Sicherungsdaten Speicher an projfs zurückgibt.  Projfs führt die Informationen vom Anbieter mit dem Inhalt des lokalen Dateisystems zusammen, mit dem der Benutzer eine einheitliche Liste der Inhalte eines Verzeichnisses enthält.

## <a name="directory-enumeration-callbacks"></a>Verzeichnisenumerationsrückrufe

Um an der verzeichnisenumeration teilnehmen zu können, muss der Anbieter die **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** und **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** Rückrufe implementieren.  Wenn ein Verzeichnis unter dem virtualisierungsstamm des Anbieters aufgezählt wird, führt projfs die folgenden Aktionen aus:

1. Projfs Ruft den **PRJ_START_DIRECTORY_ENUMERATION_CB** Rückruf des Anbieters auf, um eine enumerationssitzung zu starten.

    Im Rahmen der Verarbeitung dieses Rückrufs sollte der Anbieter die Ausführung der-Enumeration vorbereiten.  Beispielsweise muss der Arbeitsspeicher belegt werden, der möglicherweise erforderlich ist, um den Fortschritt der Enumeration im Sicherungsdaten Speicher zu verfolgen.

    Projfs identifiziert das Verzeichnis, das im **FilePathName** -Member des _callBackData_ -Parameters des Rückrufs aufgeführt wird.  Dies wird als Pfad relativ zum virtualisierungsstamm angegeben.  Wenn sich beispielsweise der virtualisierungsstamm unter befindet `C:\virtRoot` und das aufgelistete Verzeichnis ist `C:\virtRoot\dir1\dir2` , enthält das Member **FilePathName** `dir1\dir2` .  Der Anbieter bereitet sich darauf vor, diesen Pfad im Sicherungsdaten Speicher aufzuzählen.  Abhängig von den Funktionen des Sicherungs Speicher eines Anbieters ist es möglicherweise sinnvoll, die Sicherungs Speicher-Enumeration im **PRJ_START_DIRECTORY_ENUMERATION_CB** Rückruf auszuführen.

    Da mehrere Enumerationen parallel im gleichen Verzeichnis auftreten können, weist jeder enumerationsrückruf ein _enumerationid_ -Argument auf, damit der Anbieter die Rückruf Aufrufe einer einzelnen enumerationssitzung zuordnen kann.

    Wenn der Anbieter S_OK vom **PRJ_START_DIRECTORY_ENUMERATION_CB** Rückruf zurückgibt, muss er alle aufgelisteten enumerationssitzungsinformationen aufbewahren, bis der **PRJ_END_DIRECTORY_ENUMERATION_CB** -Rückruf mit dem gleichen Wert für _enumerationid_ von projfs aufgerufen wird.  Wenn der Anbieter einen Fehler von **PRJ_START_DIRECTORY_ENUMERATION_CB** zurückgibt, ruft projfs den **PRJ_END_DIRECTORY_ENUMERATION_CB** -Rückruf für diese _enumerationid_ nicht auf.

1. Der **PRJ_GET_DIRECTORY_ENUMERATION_CB** Rückruf des Anbieters wird von projfs einmal oder mehrmals aufgerufen, um den Verzeichnis Inhalt des Anbieters zu erhalten.

    Als Reaktion auf diesen Rückruf gibt der Anbieter eine sortierte Liste von Elementen aus dem Sicherungsdaten Speicher zurück.

    Der Rückruf kann einen Such Ausdruck in seinem _SearchExpression_ -Parameter bereitstellen, den der Anbieter für den Bereich der Ergebnisse der-Enumeration verwendet.  Wenn _SearchExpression_ NULL ist, gibt der Anbieter alle Einträge in dem aufgelisteten Verzeichnis zurück.  Wenn er nicht NULL ist, kann der Anbieter **[prjdoesnamecontainwildcards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** verwenden, um zu bestimmen, ob der Ausdruck Platzhalter enthält.  Wenn dies der Fall ist, verwendet der Anbieter **[prjdatamematch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** , um zu bestimmen, ob ein Eintrag im Verzeichnis mit dem Such Ausdruck übereinstimmt.

    Der Anbieter sollte beim ersten Aufruf dieses Rückrufs den Wert von _SearchExpression_ erfassen.  Der erfasste Wert wird bei jedem nachfolgenden Aufruf des Rückrufs in derselben enumerationssitzung verwendet, es sei denn, PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN im **Flags** -Feld des _callBackData_ -Parameters des Rückrufs festgelegt.  In diesem Fall sollte der Wert von _SearchExpression_ erneut erfasst werden.

    Wenn der Sicherungs Speicher keine übereinstimmenden Einträge enthält, gibt der Anbieter einfach S_OK aus dem Rückruf zurück.  Andernfalls formatiert der Anbieter jeden übereinstimmenden Eintrag aus dem Sicherungs Speicher in eine **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** Struktur und verwendet dann **[prjfilldirentrybuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** , um den Puffer auszufüllen, der vom _direntrybufferhandle_ -Parameter des Rückrufs bereitgestellt wird.  Der Anbieter fügt weiterhin Einträge hinzu, bis Sie alle hinzugefügt haben oder bis **prjfilldirentrybuffer** HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) zurückgibt.  Anschließend gibt der Anbieter S_OK aus dem Rückruf zurück.  Beachten Sie, dass der Anbieter die Einträge dem _direntrybufferhandle_ -Puffer in der richtigen Sortierreihenfolge hinzufügen muss.  Der Anbieter sollte **[prjdatamecompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** verwenden, um die richtige Sortierreihenfolge zu bestimmen.

    > Der Anbieter muss einen Wert für das **IsDirectory** -Mitglied von **PRJ_FILE_BASIC_INFO** bereitstellen.  Wenn **IsDirectory** den Wert false hat, muss der Anbieter auch einen Wert für das **FileSize** -Element angeben.
    >
    > Wenn der Anbieter keine Werte für die Member " **comationtime**", " **LastAccessTime**", " **lastschreitetime**" und " **changetime** " bereitstellt, verwendet projfs die aktuelle Systemzeit.
    >
    > Projfs verwendet alle FILE_ATTRIBUTE Flags, die der Anbieter im **FileAttribute** -Member festlegt, außer FILE_ATTRIBUTE_DIRECTORY; Er legt den korrekten Wert für FILE_ATTRIBUTE_DIRECTORY im **fileattributmember** gemäß dem angegebenen Wert des **IsDirectory** -Members fest.

    Wenn **prjfilldirentrybuffer** HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) zurückgibt, bevor der Anbieter keine Einträge mehr hinzufügt, um ihn hinzuzufügen, muss der Anbieter den Eintrag nachverfolgen, den er beim Empfangen des Fehlers hinzufügen wollte.  Beim nächsten Aufrufen des **PRJ_GET_DIRECTORY_ENUMERATION_CB** Rückrufs für die gleiche enumerationssitzung durch projfs muss der Anbieter das Hinzufügen von Einträgen zum _direntrybufferhandle_ -Puffer mit dem hinzu zufügenden Eintrag fortsetzen.

    > Wenn der Sicherungs Speicher symbolische Verknüpfungen unterstützt, muss der Anbieter **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** verwenden, um den Puffer auszufüllen, der vom _direntrybufferhandle_ -Parameter des Rückrufs bereitgestellt wird.  **PrjFillDirEntryBuffer2** unterstützt eine zusätzliche Puffer Eingabe, die es dem Anbieter ermöglicht, anzugeben, dass es sich bei dem Enumerationseintrag um einen symbolischen Link handelt und was sein Ziel ist.  Andernfalls verhält sie sich wie oben für **prjfilldirentrybuffer** beschrieben.  Im folgenden Beispiel wird **PrjFillDirEntryBuffer2** verwendet, um die Unterstützung für symbolische Verknüpfungen zu veranschaulichen.
    >
    > Beachten Sie, dass **PrjFillDirEntryBuffer2** ab Windows 10, Version 2004, unterstützt wird.  Ein Anbieter sollte überprüfen, ob PrjFillDirEntryBuffer2 vorhanden ist, z. . mithilfe von **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.

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

1. Projfs Ruft den **PRJ_END_DIRECTORY_ENUMERATION_CB** Rückruf des Anbieters auf, um die enumerationssitzung zu beenden.

    Der Anbieter sollte sämtliche Bereinigungs Schritte ausführen, um die enumerationssitzung zu beenden, wie z. b. das Aufheben der Zuordnung von Arbeitsspeicher, der im Rahmen der Verarbeitung **PRJ_START_DIRECTORY_ENUMERATION_CB** zugeordnet ist
