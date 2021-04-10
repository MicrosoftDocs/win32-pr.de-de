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
# <a name="handling-view-changes"></a><span data-ttu-id="3fc76-103">Behandeln von Änderungen der Ansicht</span><span class="sxs-lookup"><span data-stu-id="3fc76-103">Handling View Changes</span></span>

<span data-ttu-id="3fc76-104">Wenn Dateien und Verzeichnisse unterhalb des virtualisierungsstamms geöffnet werden, erstellt der Anbieter Platzhalter auf dem Datenträger</span><span class="sxs-lookup"><span data-stu-id="3fc76-104">As files and directories under the virtualization root are opened, the provider creates placeholders on disk, and as files are read the placeholders are hydrated with contents.</span></span>  <span data-ttu-id="3fc76-105">Diese Platzhalter stellen den Zustand des Sicherungs Speicher zu dem Zeitpunkt dar, zu dem Sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="3fc76-105">These placeholders represent the state of the backing store at the time they were created.</span></span>  <span data-ttu-id="3fc76-106">Diese zwischengespeicherten Elemente in Kombination mit den Elementen, die vom Anbieter in Enumerationen projiziert werden, bilden die "Ansicht" des Sicherungs Speicher des Clients.</span><span class="sxs-lookup"><span data-stu-id="3fc76-106">These cached items, combined with the items projected by the provider in enumerations, constitute the client's "view" of the backing store.</span></span>  <span data-ttu-id="3fc76-107">Von Zeit zu Zeit kann der Anbieter die Client Ansicht aktualisieren, ob aufgrund von Änderungen im Sicherungs Speicher oder aufgrund expliziter Maßnahmen durch den Benutzer zum Ändern der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="3fc76-107">From time to time the provider may wish to update the client's view, whether because of changes in the backing store, or because of explicit action taken by the user to change their view.</span></span>

> <span data-ttu-id="3fc76-108">Wenn der Anbieter die Ansicht proaktiv aktualisiert, wenn sich der Sicherungs Speicher ändert, empfiehlt es sich, die Anzeige von Änderungen relativ selten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3fc76-108">If the provider updates the view proactively, as the backing store changes, it is recommended that view changes be relatively infrequent.</span></span>  <span data-ttu-id="3fc76-109">Dies liegt daran, dass eine Ansicht für ein Element, das geöffnet wurde und daher einen Platzhalter hat, auf dem Datenträger erstellt wurde, erfordert, dass das Element auf dem Datenträger entweder aktualisiert oder gelöscht wird, um die Sicht Änderung widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="3fc76-109">This is because a view change to an item that has been opened, and therefore had a placeholder created on disk, requires that the on-disk item be either updated or deleted to reflect the view change.</span></span>  <span data-ttu-id="3fc76-110">Häufige Updates können zu zusätzlichen Datenträger Aktivitäten führen, die sich negativ auf die Systemleistung auswirken können.</span><span class="sxs-lookup"><span data-stu-id="3fc76-110">Frequent updates may result in extra disk activity that can negatively impact system performance.</span></span>

## <a name="item-versioning"></a><span data-ttu-id="3fc76-111">Element Versionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="3fc76-111">Item Versioning</span></span>

<span data-ttu-id="3fc76-112">Um die Verwaltung mehrerer Ansichten zu unterstützen, stellt projfs die **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** Struktur bereit.</span><span class="sxs-lookup"><span data-stu-id="3fc76-112">To support maintaining multiple views, ProjFS provides the **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** struct.</span></span>  <span data-ttu-id="3fc76-113">Ein Anbieter verwendet diese Struktur eigenständig in Aufrufen von **[prjmarkdirectoryasplachalter](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** und ist in den **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** und **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** Strukturen eingebettet.</span><span class="sxs-lookup"><span data-stu-id="3fc76-113">A provider uses this struct standalone in calls to **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)**, and it is embedded in the **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** and **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** structs.</span></span>  <span data-ttu-id="3fc76-114">Der **PRJ_PLACEHOLDER_VERSION_INFO**. Im Feld "contentid" speichert der Anbieter bis zu 128 Bytes Versionsinformationen für eine Datei oder ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="3fc76-114">The **PRJ_PLACEHOLDER_VERSION_INFO**.ContentID field is where the provider stores up to 128 bytes of version information for a file or directory.</span></span>  <span data-ttu-id="3fc76-115">Der Anbieter kann diesen Wert dann intern einem Wert zuordnen, der eine bestimmte Ansicht identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3fc76-115">The provider may then internally associate this value to some value that identifies a particular view.</span></span>

<span data-ttu-id="3fc76-116">Ein Anbieter, der ein Quellcodeverwaltungs-Repository virtualisiert, könnte z. b. einen Hash des Datei Inhalts verwenden, der als contentid dient, und kann Zeitstempel verwenden, um die Ansichten des Repository zu verschiedenen Zeitpunkten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3fc76-116">For example, a provider that virtualizes a source control repository might choose to use a hash of a file's contents to serve as the ContentID, and it might use timestamps to identify views of the repository at various points in time.</span></span>  <span data-ttu-id="3fc76-117">Die Zeitstempel sind möglicherweise die Zeiten, in denen Commits in das Repository durchgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="3fc76-117">The timestamps might be the times that commits to the repository were performed.</span></span>

<span data-ttu-id="3fc76-118">Wenn Sie das Beispiel für ein Zeitstempel indiziertes Repository verwenden, könnte ein typischer Ablauf für die Verwendung der contentid eines Elements wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="3fc76-118">Using the example of a timestamp-indexed repository, a typical flow for using an item's ContentID might be:</span></span>

1. <span data-ttu-id="3fc76-119">Der Client legt eine Ansicht fest, indem er den Zeitstempel angibt, bei dem der Inhalt des Repository angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3fc76-119">The client establishes a view by specifying the timestamp at which to present the repository contents.</span></span>  <span data-ttu-id="3fc76-120">Dies erfolgt über eine Schnittstelle, die vom Anbieter implementiert wird, nicht über eine projfs-API.</span><span class="sxs-lookup"><span data-stu-id="3fc76-120">This would be done through some interface implemented by the provider, not via a ProjFS API.</span></span>  <span data-ttu-id="3fc76-121">Der Anbieter kann z. b. über ein Befehlszeilen Tool verfügen, das verwendet werden kann, um dem Anbieter mitzuteilen, welche die Benutzer Wünsche anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3fc76-121">For example, the provider may have a command-line tool that could be used to tell the provider which view the user desires.</span></span>
1. <span data-ttu-id="3fc76-122">Wenn der Client ein Handle für eine virtualisierte Datei oder ein virtualisiertes Verzeichnis erstellt, erstellt der Anbieter mithilfe von Dateisystem Metadaten aus dem Sicherungs Speicher einen Platzhalter dafür.</span><span class="sxs-lookup"><span data-stu-id="3fc76-122">When the client creates a handle to a virtualized file or directory, the provider creates a placeholder for it, using file system metadata from the backing store.</span></span>  <span data-ttu-id="3fc76-123">Der jeweilige verwendete Satz von Metadaten wird durch den contentid-Wert identifiziert, der mit dem Zeitstempel der gewünschten Ansicht verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="3fc76-123">The particular set of metadata it uses is identified by the ContentID value associated with the timestamp of the desired view.</span></span>  <span data-ttu-id="3fc76-124">Wenn der Anbieter **[prjschreiteplaceholderinfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** aufruft, um die Platzhalter Informationen zu schreiben, liefert er die contentid im VERSIONINFO-Member des _placeholderinfo_ -Arguments.</span><span class="sxs-lookup"><span data-stu-id="3fc76-124">When the provider calls **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** to write the placeholder information, it supplies the ContentID in the VersionInfo member of the _placeholderInfo_ argument.</span></span>  <span data-ttu-id="3fc76-125">Der Anbieter sollte dann aufzeichnen, dass in dieser Ansicht ein Platzhalter für die Datei oder das Verzeichnis erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3fc76-125">The provider should then record that a placeholder for that file or directory was created in this view.</span></span>
1. <span data-ttu-id="3fc76-126">Wenn der Client aus einem Platzhalter liest, wird der **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** Rückruf des Anbieters aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3fc76-126">When the client reads from a placeholder, the provider's **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** callback is invoked.</span></span>  <span data-ttu-id="3fc76-127">Der VERSIONINFO-Member des _callBackData_ -Parameters enthält die contentid des Anbieters, der in **prjschreiteplaceholderinfo** angegeben wurde, als der Datei Platzhalter erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3fc76-127">The _callbackData_ parameter's VersionInfo member contains the ContentID the provider specified in **PrjWritePlaceholderInfo** when it created the file placeholder.</span></span>  <span data-ttu-id="3fc76-128">Der Anbieter verwendet diese contentid, um den korrekten Inhalt der Datei aus dem Sicherungs Speicher abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3fc76-128">The provider uses that ContentID to retrieve the correct contents of the file from its backing store.</span></span>
1. <span data-ttu-id="3fc76-129">Der Client fordert eine Ansichts Änderung an, indem er einen neuen Zeitstempel angibt.</span><span class="sxs-lookup"><span data-stu-id="3fc76-129">The client requests a view change by specifying a new timestamp.</span></span>  <span data-ttu-id="3fc76-130">Für jeden Platzhalter, den der in der vorherigen Ansicht erstellte Anbieter enthält, kann der Anbieter den Platzhalter auf dem Datenträger durch einen aktualisierten ersetzen, dessen contentid dem neuen Zeitstempel durch Aufrufen von **[prjupdatefijecbenötigter](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)** zugeordnet ist, wenn in der neuen Ansicht eine andere Version der Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3fc76-130">For each placeholder the provider created in the previous view, if a different version of that file exists in the new view the provider may replace the placeholder on disk with an updated one whose ContentID is associated with the new timestamp by calling **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.</span></span>  <span data-ttu-id="3fc76-131">Alternativ kann der Anbieter den Platzhalter durch Aufrufen von **[prjdeletefile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** löschen, damit die neue Ansicht der Datei in Enumerationen projiziert wird.</span><span class="sxs-lookup"><span data-stu-id="3fc76-131">Alternatively, the provider may delete the placeholder by calling **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** so that the new view of the file will be projected in enumerations.</span></span>  <span data-ttu-id="3fc76-132">Wenn die Datei in der neuen Ansicht nicht vorhanden ist, muss Sie vom Anbieter durch Aufrufen von **prjdeletefile** gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="3fc76-132">If the file does not exist in the new view, the provider must delete it by calling **PrjDeleteFile**.</span></span>

<span data-ttu-id="3fc76-133">Beachten Sie, dass der Anbieter sicherstellen muss, dass der Anbieter, wenn der Client ein Verzeichnis auflistet, den Inhalt bereitstellt, der der Sicht des Clients entspricht.</span><span class="sxs-lookup"><span data-stu-id="3fc76-133">Note that the provider must ensure that when the client enumerates a directory, the provider will supply the contents that correspond to the client's view.</span></span>  <span data-ttu-id="3fc76-134">Der Anbieter könnte z. b. den VERSIONINFO-Member des _callBackData_ -Parameters des **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** und **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** Rückrufe verwenden, um Verzeichnisinhalte im Handumdrehen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3fc76-134">For example, the provider could use the VersionInfo member of the _callbackData_ parameter of the **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** and **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** callbacks to retrieve directory contents on the fly.</span></span>  <span data-ttu-id="3fc76-135">Alternativ kann es eine Verzeichnisstruktur für diese Sicht im Sicherungs Speicher als Teil der Einrichtung der Ansicht erstellen und diese Struktur dann einfach auflisten.</span><span class="sxs-lookup"><span data-stu-id="3fc76-135">Alternatively it could build a directory structure for that view in its backing store as part of establishing the view, and then simply enumerate that structure.</span></span>

> <span data-ttu-id="3fc76-136">Wenn ein Anbieter Rückruf für einen Platzhalter oder eine partielle Datei aufgerufen wird, wird der vom Anbieter beim Erstellen des Elements angegebene Versionsinformationen im VERSIONINFO-Member des _callBackData_ -Parameters des Rückrufs bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3fc76-136">Whenever a provider callback is invoked for a placeholder or partial file, the version information the provider specified when creating the item is provided in the VersionInfo member of the callback's _callbackData_ parameter.</span></span>

## <a name="updating-the-view"></a><span data-ttu-id="3fc76-137">Aktualisieren der Ansicht</span><span class="sxs-lookup"><span data-stu-id="3fc76-137">Updating the View</span></span>

<span data-ttu-id="3fc76-138">Im folgenden finden Sie eine Beispiel Funktion, die veranschaulicht, wie ein Anbieter die lokale Ansicht aktualisieren kann, wenn der Benutzer einen neuen Zeitstempel angibt.</span><span class="sxs-lookup"><span data-stu-id="3fc76-138">Below is a sample function illustrating how a provider might update the local view when the user specifies a new timestamp.</span></span>  <span data-ttu-id="3fc76-139">Die-Funktion Ruft eine Liste der Platzhalter ab, die der Anbieter für die Sicht erstellt hat, von der der Benutzer soeben geändert wurde, und aktualisiert den lokalen Cache Zustand basierend auf dem Zustand der einzelnen Platzhalter in der neuen Ansicht.</span><span class="sxs-lookup"><span data-stu-id="3fc76-139">The function retrieves a list of the placeholders the provider created for the view the user has just changed from, and updates the local cache state based on each placeholder's state in the new view.</span></span>  <span data-ttu-id="3fc76-140">Aus Gründen der Übersichtlichkeit lässt diese Routine bestimmte Komplexitäten beim Umgang mit dem Dateisystem aus.</span><span class="sxs-lookup"><span data-stu-id="3fc76-140">For clarity, this routine omits certain complexities of dealing with the file system.</span></span>  <span data-ttu-id="3fc76-141">Beispielsweise ist in der alten Ansicht möglicherweise ein bestimmtes Verzeichnis mit einigen Dateien oder Verzeichnissen vorhanden. in der neuen Ansicht ist das Verzeichnis (und sein Inhalt) jedoch möglicherweise nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3fc76-141">For example, in the old view a given directory may have existed with some files or directories in it, but in the new view that directory (and its contents) may no longer exist.</span></span>  <span data-ttu-id="3fc76-142">Um zu vermeiden, dass in einer solchen Situation Fehler auftreten, sollte der Anbieter den Status der Datei und der Verzeichnisse unterhalb des virtualisierungsstamms in einer tiefen ersten Weise aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3fc76-142">To avoid encountering errors in such a situation the provider should update the state of the file and directories beneath the virtualization root in a depth-first fashion.</span></span>

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