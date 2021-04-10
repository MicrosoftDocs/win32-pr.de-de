---
title: Behandeln von Änderungen der Ansicht
description: Beschreibt, wie die Client Ansicht des Sicherungs Speicher eines Anbieters aktualisiert wird.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/09/2018
ms.topic: article
ms.openlocfilehash: 1d5a709752f92b7449d2ccc38f67c4417edf8d62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039109"
---
# <a name="handling-view-changes"></a>Behandeln von Änderungen der Ansicht

Wenn Dateien und Verzeichnisse unterhalb des virtualisierungsstamms geöffnet werden, erstellt der Anbieter Platzhalter auf dem Datenträger  Diese Platzhalter stellen den Zustand des Sicherungs Speicher zu dem Zeitpunkt dar, zu dem Sie erstellt wurden.  Diese zwischengespeicherten Elemente in Kombination mit den Elementen, die vom Anbieter in Enumerationen projiziert werden, bilden die "Ansicht" des Sicherungs Speicher des Clients.  Von Zeit zu Zeit kann der Anbieter die Client Ansicht aktualisieren, ob aufgrund von Änderungen im Sicherungs Speicher oder aufgrund expliziter Maßnahmen durch den Benutzer zum Ändern der Ansicht.

> Wenn der Anbieter die Ansicht proaktiv aktualisiert, wenn sich der Sicherungs Speicher ändert, empfiehlt es sich, die Anzeige von Änderungen relativ selten zu überprüfen.  Dies liegt daran, dass eine Ansicht für ein Element, das geöffnet wurde und daher einen Platzhalter hat, auf dem Datenträger erstellt wurde, erfordert, dass das Element auf dem Datenträger entweder aktualisiert oder gelöscht wird, um die Sicht Änderung widerzuspiegeln.  Häufige Updates können zu zusätzlichen Datenträger Aktivitäten führen, die sich negativ auf die Systemleistung auswirken können.

## <a name="item-versioning"></a>Element Versionsverwaltung

Um die Verwaltung mehrerer Ansichten zu unterstützen, stellt projfs die **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** Struktur bereit.  Ein Anbieter verwendet diese Struktur eigenständig in Aufrufen von **[prjmarkdirectoryasplachalter](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** und ist in den **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** und **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** Strukturen eingebettet.  Der **PRJ_PLACEHOLDER_VERSION_INFO**. Im Feld "contentid" speichert der Anbieter bis zu 128 Bytes Versionsinformationen für eine Datei oder ein Verzeichnis.  Der Anbieter kann diesen Wert dann intern einem Wert zuordnen, der eine bestimmte Ansicht identifiziert.

Ein Anbieter, der ein Quellcodeverwaltungs-Repository virtualisiert, könnte z. b. einen Hash des Datei Inhalts verwenden, der als contentid dient, und kann Zeitstempel verwenden, um die Ansichten des Repository zu verschiedenen Zeitpunkten zu identifizieren.  Die Zeitstempel sind möglicherweise die Zeiten, in denen Commits in das Repository durchgeführt wurden.

Wenn Sie das Beispiel für ein Zeitstempel indiziertes Repository verwenden, könnte ein typischer Ablauf für die Verwendung der contentid eines Elements wie folgt lauten:

1. Der Client legt eine Ansicht fest, indem er den Zeitstempel angibt, bei dem der Inhalt des Repository angezeigt werden soll.  Dies erfolgt über eine Schnittstelle, die vom Anbieter implementiert wird, nicht über eine projfs-API.  Der Anbieter kann z. b. über ein Befehlszeilen Tool verfügen, das verwendet werden kann, um dem Anbieter mitzuteilen, welche die Benutzer Wünsche anzeigen.
1. Wenn der Client ein Handle für eine virtualisierte Datei oder ein virtualisiertes Verzeichnis erstellt, erstellt der Anbieter mithilfe von Dateisystem Metadaten aus dem Sicherungs Speicher einen Platzhalter dafür.  Der jeweilige verwendete Satz von Metadaten wird durch den contentid-Wert identifiziert, der mit dem Zeitstempel der gewünschten Ansicht verknüpft ist.  Wenn der Anbieter **[prjschreiteplaceholderinfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** aufruft, um die Platzhalter Informationen zu schreiben, liefert er die contentid im VERSIONINFO-Member des _placeholderinfo_ -Arguments.  Der Anbieter sollte dann aufzeichnen, dass in dieser Ansicht ein Platzhalter für die Datei oder das Verzeichnis erstellt wurde.
1. Wenn der Client aus einem Platzhalter liest, wird der **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** Rückruf des Anbieters aufgerufen.  Der VERSIONINFO-Member des _callBackData_ -Parameters enthält die contentid des Anbieters, der in **prjschreiteplaceholderinfo** angegeben wurde, als der Datei Platzhalter erstellt wurde.  Der Anbieter verwendet diese contentid, um den korrekten Inhalt der Datei aus dem Sicherungs Speicher abzurufen.
1. Der Client fordert eine Ansichts Änderung an, indem er einen neuen Zeitstempel angibt.  Für jeden Platzhalter, den der in der vorherigen Ansicht erstellte Anbieter enthält, kann der Anbieter den Platzhalter auf dem Datenträger durch einen aktualisierten ersetzen, dessen contentid dem neuen Zeitstempel durch Aufrufen von **[prjupdatefijecbenötigter](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)** zugeordnet ist, wenn in der neuen Ansicht eine andere Version der Datei vorhanden ist.  Alternativ kann der Anbieter den Platzhalter durch Aufrufen von **[prjdeletefile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** löschen, damit die neue Ansicht der Datei in Enumerationen projiziert wird.  Wenn die Datei in der neuen Ansicht nicht vorhanden ist, muss Sie vom Anbieter durch Aufrufen von **prjdeletefile** gelöscht werden.

Beachten Sie, dass der Anbieter sicherstellen muss, dass der Anbieter, wenn der Client ein Verzeichnis auflistet, den Inhalt bereitstellt, der der Sicht des Clients entspricht.  Der Anbieter könnte z. b. den VERSIONINFO-Member des _callBackData_ -Parameters des **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** und **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** Rückrufe verwenden, um Verzeichnisinhalte im Handumdrehen abzurufen.  Alternativ kann es eine Verzeichnisstruktur für diese Sicht im Sicherungs Speicher als Teil der Einrichtung der Ansicht erstellen und diese Struktur dann einfach auflisten.

> Wenn ein Anbieter Rückruf für einen Platzhalter oder eine partielle Datei aufgerufen wird, wird der vom Anbieter beim Erstellen des Elements angegebene Versionsinformationen im VERSIONINFO-Member des _callBackData_ -Parameters des Rückrufs bereitgestellt.

## <a name="updating-the-view"></a>Aktualisieren der Ansicht

Im folgenden finden Sie eine Beispiel Funktion, die veranschaulicht, wie ein Anbieter die lokale Ansicht aktualisieren kann, wenn der Benutzer einen neuen Zeitstempel angibt.  Die-Funktion Ruft eine Liste der Platzhalter ab, die der Anbieter für die Sicht erstellt hat, von der der Benutzer soeben geändert wurde, und aktualisiert den lokalen Cache Zustand basierend auf dem Zustand der einzelnen Platzhalter in der neuen Ansicht.  Aus Gründen der Übersichtlichkeit lässt diese Routine bestimmte Komplexitäten beim Umgang mit dem Dateisystem aus.  Beispielsweise ist in der alten Ansicht möglicherweise ein bestimmtes Verzeichnis mit einigen Dateien oder Verzeichnissen vorhanden. in der neuen Ansicht ist das Verzeichnis (und sein Inhalt) jedoch möglicherweise nicht mehr vorhanden.  Um zu vermeiden, dass in einer solchen Situation Fehler auftreten, sollte der Anbieter den Status der Datei und der Verzeichnisse unterhalb des virtualisierungsstamms in einer tiefen ersten Weise aktualisieren.

```C++
typedef struct MY_ON_DISK_PLACEHOLDER MY_ON_DISK_PLACEHOLDER;

typedef struct MY_ON_DISK_PLACEHOLDER {
    MY_ON_DISK_PLACEHOLDER* Next;
    PWSTR RelativePath;
} MY_ON_DISK_PLACEHOLDER;

HRESULT
MyViewUpdater(
    _In_ PRJ_CALLBACK_DATA callbackData,
    _In_ time_t newViewTime
    )
{
    HRESULT hr = S_OK;

    // MyGetOnDiskPlaceholders is a routine the provider might implement to produce
    // a pointer to a list of the placeholders the provider has created in the view.
    MY_ON_DISK_PLACEHOLDER* placeholder = MyGetOnDiskPlaceholders();
    while (placeholder != NULL)
    {
        // MyGetProjectedFileInfo is a routine the provider might implement to
        // determine whether a given file exists in its backing store at a
        // particular timestamp.  If it does, the routine returns a pointer to
        // a PRJ_PLACEHOLDER_INFO struct populated with information about the
        // file.
        PRJ_PLACEHOLDER_INFO* newViewPlaceholderInfo = NULL;
        UINT32 newViewPlaceholderInfoSize = 0;

        newViewPlaceholderInfo = MyGetProjectedFileInfo(placeholder->RelativePath,
                                                 newViewTime,
                                                 &newViewPlaceholderInfoSize);
        if (newViewPlaceholderInfo == NULL)
        {
            // The file no longer exists in the new view.  We want to remove its
            // placeholder from the local cache.
            PRJ_UPDATE_FAILURE_CAUSES deleteFailureReason;
            hr = PrjDeleteFile(callbackData->NamespaceVirtualizationContext,
                               placeholder->RelativePath,
                               PRJ_UPDATE_ALLOW_DIRTY_METADATA
                               | PRJ_UPDATE_ALLOW_DIRTY_DATA
                               | PRJ_UPDATE_ALLOW_TOMBSTONE,
                               &deleteFailureReason);

            if (hr == HRESULT_FROM_WIN32(ERROR_FILE_SYSTEM_VIRTUALIZATION_INVALID_OPERATION))
            {
                wprintf(L"Could not delete [%ls].\n", placeholder->RelativePath);
                wprintf(L"Failure reason: 0x%x", deleteFailureReason);
                return hr;
            }
            else
            {
                wprintf(L"Error deleting [%ls]: 0x%08x",
                        placeholder->RelativePath,
                        hr);
                return hr;
            }

            // MyRemovePlaceholderData is a routine the provider might implement
            // to remove an item from its list of placeholders it has created in
            // the view.
            MyRemovePlaceholderData(placeholder);
        }
        else
        {
            // The file exists in the new view.  Its local cache state may need
            // to be updated, for example if its content is different in this view.
            // As an optimization, the provider may compare the file's ContentID
            // in the new view (stored in newViewPlaceholderInfo->ContentId) with
            // the ContentID it had in the old view.  If they are the same, calling
            // PrjUpdateFileIfNeeded would not be needed.
            PRJ_UPDATE_FAILURE_CAUSES updateFailureReason;
            hr = PrjUpdateFileIfNeeded(callbackData->NamespaceVirtualizationContext,
                                       placeholder->RelativePath,
                                       newViewPlaceholderInfo,
                                       newViewPlaceholderInfoSize,
                                       PRJ_UPDATE_ALLOW_DIRTY_METADATA
                                       | PRJ_UPDATE_ALLOW_DIRTY_DATA
                                       | PRJ_UPDATE_ALLOW_TOMBSTONE,
                                       &updateFailureReason);

            if (hr == HRESULT_FROM_WIN32(ERROR_FILE_SYSTEM_VIRTUALIZATION_INVALID_OPERATION))
            {
                wprintf(L"Could not update [%ls].\n", placeholder->RelativePath);
                wprintf(L"Failure reason: 0x%x", updateFailureReason);
                return hr;
            }
            else
            {
                wprintf(L"Error updating [%ls]: 0x%08x",
                        placeholder->RelativePath,
                        hr);
                return hr;
            }

            // MyUpdatePlaceholderData is a routine the provider might implement
            // to update information about a placeholder it has created in the view.
            MyUpdatePlaceholderData(placeholder, newViewPlaceholderInfo);
        }

        placeholder = placeholder->Next;
    }

    return hr;
}
```