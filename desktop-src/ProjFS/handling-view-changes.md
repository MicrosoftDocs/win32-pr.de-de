---
title: Behandeln von Ansichtsänderungen
description: Beschreibt, wie die Clientansicht des Hintergrundspeichers eines Anbieters aktualisiert wird.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/09/2018
ms.topic: article
ms.openlocfilehash: 99ace7849b8967748f26210d9d6b770e424c349359aa39e828c8ad9af36a65af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792647"
---
# <a name="handling-view-changes"></a>Behandeln von Ansichtsänderungen

Wenn Dateien und Verzeichnisse unter dem Virtualisierungsstamm geöffnet werden, erstellt der Anbieter Platzhalter auf dem Datenträger, und wenn Dateien gelesen werden, werden die Platzhalter mit Inhalten aufgelesen.  Diese Platzhalter stellen den Zustand des Hintergrundspeichers zum Zeitpunkt ihrer Erstellen dar.  Diese zwischengespeicherten Elemente bilden in Kombination mit den Elementen, die vom Anbieter in Enumerationen projiziert werden, die "Ansicht" des Hintergrundspeichers des Clients.  Von Zeit zu Zeit möchte der Anbieter möglicherweise die Clientansicht aktualisieren, sei es aufgrund von Änderungen im Hintergrundspeicher oder aufgrund einer expliziten Aktion, die der Benutzer zum Ändern seiner Ansicht ausgeführt hat.

> Wenn der Anbieter die Ansicht proaktiv aktualisiert, wenn sich der Hintergrundspeicher ändert, wird empfohlen, dass Ansichtsänderungen relativ selten vorgenommen werden.  Dies liegt daran, dass eine Ansichtsänderung an einem Element, das geöffnet wurde und daher einen Platzhalter auf dem Datenträger erstellt hat, erfordert, dass das Element auf dem Datenträger aktualisiert oder gelöscht wird, um die Ansichtsänderung widerzubilden.  Häufige Updates können zu zusätzlichen Datenträgeraktivitäten führen, die sich negativ auf die Systemleistung auswirken können.

## <a name="item-versioning"></a>Elementversionsierung

Um die Verwaltung mehrerer Ansichten zu unterstützen, stellt ProjFS **[die](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** PRJ_PLACEHOLDER_VERSION_INFO-Struktur.  Ein Anbieter verwendet diese eigenständige Struktur in Aufrufen von **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** und ist **[](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** in die PRJ_PLACEHOLDER_INFO und PRJ_CALLBACK_DATA eingebettet. **[](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)**  Der **PRJ_PLACEHOLDER_VERSION_INFO**. Im Feld ContentID speichert der Anbieter bis zu 128 Byte an Versionsinformationen für eine Datei oder ein Verzeichnis.  Der Anbieter kann diesen Wert dann intern einem Wert zuordnen, der eine bestimmte Ansicht identifiziert.

Beispielsweise kann ein Anbieter, der ein Quellcodeverwaltungsrepository virtualisiert, einen Hash des Inhalts einer Datei als ContentID verwenden und Zeitstempel verwenden, um Ansichten des Repositorys zu verschiedenen Zeitpunkten zu identifizieren.  Die Zeitstempel können die Zeiten sein, zu denen Commits für das Repository ausgeführt wurden.

Am Beispiel eines repositorys mit Zeitstempelindizierung kann ein typischer Ablauf für die Verwendung der ContentID eines Elements sein:

1. Der Client erstellt eine Sicht durch Angabe des Zeitstempels, an dem der Repositoryinhalt angezeigt werden soll.  Dies erfolgt über eine vom Anbieter implementierte Schnittstelle, nicht über eine ProjFS-API.  Beispielsweise kann der Anbieter über ein Befehlszeilentool verfügen, das verwendet werden kann, um den Anbieter darüber zu informieren, welche Benutzer wünschen.
1. Wenn der Client ein Handle für eine virtualisierte Datei oder ein virtualisiertes Verzeichnis erstellt, erstellt der Anbieter unter Verwendung von Dateisystemmetadaten aus dem Hintergrundspeicher einen Platzhalter dafür.  Der bestimmte Satz von Metadaten, die er verwendet, wird durch den ContentID-Wert identifiziert, der dem Zeitstempel der gewünschten Sicht zugeordnet ist.  Wenn der Anbieter **[PrjWritePlaceholderInfo aufruft,](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** um die Platzhalterinformationen zu schreiben, stellt er die ContentID im VersionInfo-Member des _placeholderInfo-Arguments_ zur Verfügung.  Der Anbieter sollte dann aufzeichnen, dass in dieser Ansicht ein Platzhalter für diese Datei oder dieses Verzeichnis erstellt wurde.
1. Wenn der Client aus einem Platzhalter liest, wird der PRJ_GET_FILE_DATA_CB **[des](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** Anbieters aufgerufen.  Das _VersionInfo-Element des callbackData-Parameters_ enthält die ContentID, die der Anbieter in **PrjWritePlaceholderInfo** beim Erstellen des Dateiplatzhalters angegeben hat.  Der Anbieter verwendet diese ContentID, um den richtigen Inhalt der Datei aus seinem Hintergrundspeicher abzurufen.
1. Der Client fordert eine Ansichtsänderung an, indem ein neuer Zeitstempel angegeben wird.  Für jeden Platzhalter, den der Anbieter in der vorherigen Ansicht erstellt hat, kann der Anbieter den Platzhalter auf dem Datenträger durch einen aktualisierten Platzhalter ersetzen, dessen ContentID dem neuen Zeitstempel zugeordnet ist, indem **[er PrjUpdateFileIfNeeded aufruft.](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**  Alternativ kann der Anbieter den Platzhalter löschen, indem er **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** aufruft, sodass die neue Ansicht der Datei in Enumerationen projiziert wird.  Wenn die Datei in der neuen Ansicht nicht vorhanden ist, muss sie vom Anbieter durch Aufrufen von **PrjDeleteFile gelöscht werden.**

Beachten Sie, dass der Anbieter sicherstellen muss, dass beim Aufzählen eines Verzeichnisses durch den Client der Inhalt der Clientansicht angezeigt wird.  Beispielsweise kann der Anbieter den VersionInfo-Member des _callbackData-Parameters_ der **[](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** **[PRJ_START_DIRECTORY_ENUMERATION_CB-](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** und PRJ_GET_DIRECTORY_ENUMERATION_CB-Rückrufe verwenden, um Verzeichnisinhalte im Handzeraden abzurufen.  Alternativ kann sie eine Verzeichnisstruktur für diese Ansicht im Hintergrundspeicher erstellen, um die Ansicht zu erstellen, und diese Struktur dann einfach aufzählen.

> Wenn ein Anbieterrückruf für einen Platzhalter oder eine Teildatei aufgerufen wird, werden die Versionsinformationen, die der Anbieter beim Erstellen des Elements angegeben hat, im VersionInfo-Element des _rückruf-Parameters callbackData_ bereitgestellt.

## <a name="updating-the-view"></a>Aktualisieren der Ansicht

Im Folgenden finden Sie eine Beispielfunktion, die veranschaulicht, wie ein Anbieter die lokale Ansicht aktualisieren kann, wenn der Benutzer einen neuen Zeitstempel angibt.  Die Funktion ruft eine Liste der Platzhalter ab, die der Anbieter für die Sicht erstellt hat, aus der sich der Benutzer gerade geändert hat, und aktualisiert den lokalen Cachezustand basierend auf dem Zustand jedes Platzhalters in der neuen Ansicht.  Aus Gründen der Übersichtlichkeit lässt diese Routine bestimmte Komplexitäten des Umgangs mit dem Dateisystem aus.  Beispielsweise kann in der alten Ansicht ein bestimmtes Verzeichnis mit einigen Dateien oder Verzeichnissen vorhanden sein, aber in der neuen Sicht ist dieses Verzeichnis (und sein Inhalt) möglicherweise nicht mehr vorhanden.  Um Fehler in einer solchen Situation zu vermeiden, sollte der Anbieter den Zustand der Datei und der Verzeichnisse unterhalb des Virtualisierungsstamms in einer Tiefen-zuerst-Weise aktualisieren.

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