---
title: Bereitstellen von Dateidaten
description: Beschreibt, wie ein Anbieter Platzhalter Informationen und Datei Daten bereitstellt.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/01/2018
ms.topic: article
ms.openlocfilehash: 341a0f1c477b605b2a437edf311c380910744ac0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390688"
---
# <a name="providing-file-data"></a><span data-ttu-id="063e6-103">Bereitstellen von Dateidaten</span><span class="sxs-lookup"><span data-stu-id="063e6-103">Providing File Data</span></span>

<span data-ttu-id="063e6-104">Wenn ein Anbieter erstmalig einen virtualisierungsstamm erstellt, ist er auf dem lokalen System leer.</span><span class="sxs-lookup"><span data-stu-id="063e6-104">When a provider first creates a virtualization root it is empty on the local system.</span></span> <span data-ttu-id="063e6-105">Das heißt, keines der Elemente im Sicherungsdaten Speicher wurde noch auf dem Datenträger zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="063e6-105">That is, none of the items in the backing data store have yet been cached to disk.</span></span> <span data-ttu-id="063e6-106">Wenn Elemente geöffnet werden, fordert projfs Informationen vom Anbieter an, damit Platzhalter für diese Elemente im lokalen Dateisystem erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="063e6-106">As items are opened, ProjFS requests information from the provider to allow placeholders for those items to be created in the local file system.</span></span>  <span data-ttu-id="063e6-107">Beim Zugriff auf den Element Inhalt fordert projfs diese Inhalte vom Anbieter an.</span><span class="sxs-lookup"><span data-stu-id="063e6-107">As item contents are accessed, ProjFS requests those contents from the provider.</span></span>  <span data-ttu-id="063e6-108">Das Ergebnis ist, dass virtualisierte Dateien und Verzeichnisse aus Sicht des Benutzers ähnlich wie normale Dateien und Verzeichnisse angezeigt werden, die sich bereits im lokalen Dateisystem befinden.</span><span class="sxs-lookup"><span data-stu-id="063e6-108">The result is that from the user's perspective, virtualized files and directories appear similar to normal files and directories that already reside on the local file system.</span></span>

## <a name="placeholder-creation"></a><span data-ttu-id="063e6-109">Platzhalter Erstellung</span><span class="sxs-lookup"><span data-stu-id="063e6-109">Placeholder Creation</span></span>

<span data-ttu-id="063e6-110">Wenn eine Anwendung versucht, ein Handle für eine virtualisierte Datei zu öffnen, ruft projfs den **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** Rückruf für jedes Element des Pfads auf, der noch nicht auf dem Datenträger vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="063e6-110">When an application attempts to open a handle to a virtualized file, ProjFS calls the **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** callback for each item of the path that does not yet exist on disk.</span></span>  <span data-ttu-id="063e6-111">Wenn z. b. versucht wird, eine Anwendung zu öffnen `C:\virtRoot\dir1\dir2\file.txt` , aber nur der Pfad auf dem Daten `C:\virtRoot\dir1` Träger vorhanden ist, empfängt der Anbieter einen Rückruf für `C:\virtRoot\dir1\dir2` und dann für `C:\virtRoot\dir1\dir2\file.txt` .</span><span class="sxs-lookup"><span data-stu-id="063e6-111">For example, if an application tries to open `C:\virtRoot\dir1\dir2\file.txt`, but only the path `C:\virtRoot\dir1` exists on disk, then the provider will receive a callback for `C:\virtRoot\dir1\dir2`, then for `C:\virtRoot\dir1\dir2\file.txt`.</span></span>

<span data-ttu-id="063e6-112">Wenn projfs den **PRJ_GET_PLACEHOLDER_INFO_CB** Rückruf des Anbieters aufruft, führt der Anbieter die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="063e6-112">When ProjFS calls the provider's **PRJ_GET_PLACEHOLDER_INFO_CB** callback, the provider performs the following actions:</span></span>

1. <span data-ttu-id="063e6-113">Der Anbieter bestimmt, ob der angeforderte Name im Sicherungs Speicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="063e6-113">The provider determines whether the requested name exists in its backing store.</span></span>  <span data-ttu-id="063e6-114">Der Anbieter sollte **[prjdatamecompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** als Vergleichs Routine beim Durchsuchen des Sicherungs Speicher verwenden, um zu bestimmen, ob der angeforderte Name im Sicherungs Speicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="063e6-114">The provider should use **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** as the comparison routine when searching its backing store to determine whether the requested name exists in the backing store.</span></span>  <span data-ttu-id="063e6-115">Wenn dies nicht der Fall ist, gibt der Anbieter HRESULT_FROM_WIN32 (ERROR_FILE_NOT_FOUND) aus dem Rückruf zurück.</span><span class="sxs-lookup"><span data-stu-id="063e6-115">If it does not, the provider returns HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) from the callback.</span></span>

1. <span data-ttu-id="063e6-116">Wenn der angeforderte Name im Sicherungs Speicher vorhanden ist, füllt der Anbieter eine [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) Struktur mit den Dateisystem Metadaten des Elements auf und ruft **[prjschreiteplaceholderinfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** auf, um die Daten an projfs zu senden.</span><span class="sxs-lookup"><span data-stu-id="063e6-116">If the requested name does exist in the backing store, the provider populates a [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) structure with the item's file system metadata and calls **[PrjWritePlaceholderInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** to send the data to ProjFS.</span></span>  <span data-ttu-id="063e6-117">Diese Informationen werden von projfs verwendet, um einen Platzhalter im lokalen Dateisystem für das Element zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="063e6-117">ProjFS will use that information to create a placeholder in the local file system for the item.</span></span>

    > <span data-ttu-id="063e6-118">Projfs verwendet alle FILE_ATTRIBUTE Flags, die der Anbieter im **filebasicinfo. fileattributmember** von PRJ_PLACEHOLDER_INFO mit Ausnahme von FILE_ATTRIBUTE_DIRECTORY enthält. Er legt den korrekten Wert für FILE_ATTRIBUTE_DIRECTORY im **filebasicinfo. fileattributmember** gemäß dem angegebenen Wert des Elements **filebasicinfo. IsDirectory** fest.</span><span class="sxs-lookup"><span data-stu-id="063e6-118">ProjFS will use whatever FILE_ATTRIBUTE flags the provider sets in the **FileBasicInfo.FileAttributes** member of PRJ_PLACEHOLDER_INFO except for FILE_ATTRIBUTE_DIRECTORY; it will set the correct value for FILE_ATTRIBUTE_DIRECTORY in the **FileBasicInfo.FileAttributes** member according to the supplied value of the **FileBasicInfo.IsDirectory** member.</span></span>

    > <span data-ttu-id="063e6-119">Wenn der Sicherungs Speicher symbolische Verknüpfungen unterstützt, muss der Anbieter **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** verwenden, um die Platzhalter Daten an projfs zu senden.</span><span class="sxs-lookup"><span data-stu-id="063e6-119">If the backing store supports symbolic links, the provider must use **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** to send the placeholder data to ProjFS.</span></span>  <span data-ttu-id="063e6-120">**PrjWritePlaceholderInfo2** unterstützt eine zusätzliche Puffer Eingabe, die es dem Anbieter ermöglicht, anzugeben, dass der Platzhalter eine symbolische Verknüpfung und das Ziel ist.</span><span class="sxs-lookup"><span data-stu-id="063e6-120">**PrjWritePlaceholderInfo2** supports an extra buffer input that allows the provider to specify that the placeholder is a symbolic link and what its target is.</span></span>  <span data-ttu-id="063e6-121">Andernfalls verhält es sich wie oben beschrieben für **prjschreiteplaceholderinfo**.</span><span class="sxs-lookup"><span data-stu-id="063e6-121">It otherwise behaves as described above for **PrjWritePlaceholderInfo**.</span></span>  <span data-ttu-id="063e6-122">Im folgenden Beispiel wird veranschaulicht, wie **PrjWritePlaceholderInfo2** verwendet wird, um symbolische Verknüpfungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="063e6-122">The following sample illustrates how to use **PrjWritePlaceholderInfo2** to provide support for symbolic links.</span></span>
    >
    > <span data-ttu-id="063e6-123">Beachten Sie, dass **PrjWritePlaceholderInfo2** ab Windows 10, Version 2004, unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="063e6-123">Note that **PrjWritePlaceholderInfo2** is supported as of Windows 10, version 2004.</span></span>  <span data-ttu-id="063e6-124">Ein Anbieter sollte überprüfen, ob PrjWritePlaceholderInfo2 vorhanden ist, z. . mithilfe von **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span><span class="sxs-lookup"><span data-stu-id="063e6-124">A provider should probe for the existence of **PrjWritePlaceholderInfo2**, for instance by using **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span></span>

```C++
HRESULT
MyGetPlaceholderInfoCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData
    )
{
    // MyGetItemInfo is a routine the provider might implement to get
    // information from its backing store for a given file path.  The first
    // parameter is an _In_ parameter that supplies the name to look for.
    // If the item exists the routine provides the file information in the
    // remaining parameters, all of which are annotated _Out_:
    // * 2nd parameter: the name as it appears in the backing store
    // * 3rd-9th parameters: basic file info
    // * 10th parameter: if the item is a symbolic link, a pointer to a 
    //   NULL-terminated string identifying the link's target
    //
    // Note that the routine returns the name that is in the backing
    // store.  This is because the input file path may not be in the same
    // case as what is in the backing store.  The provider should create
    // the placeholder with the name it has in the backing store.
    //
    // Note also that this example does not provide anything beyond basic
    // file information and a possible symbolic link target.
    HRESULT hr;
    WCHAR* backingStoreName = NULL;
    WCHAR* symlinkTarget = NULL;
    PRJ_PLACEHOLDER_INFO placeholderInfo = {};
    hr = MyGetItemInfo(callbackData->FilePathName,
                       &backingStoreName,
                       &placeholderInfo.FileBasicInfo.IsDirectory,
                       &placeholderInfo.FileBasicInfo.FileSize,
                       &placeholderInfo.FileBasicInfo.CreationTime,
                       &placeholderInfo.FileBasicInfo.LastAccessTime,
                       &placeholderInfo.FileBasicInfo.LastWriteTime,
                       &placeholderInfo.FileBasicInfo.ChangeTime,
                       &placeholderInfo.FileBasicInfo.FileAttributes,
                       &symlinkTarget);

    if (FAILED(hr))
    {
        // If callbackData->FilePathName doesn't exist in our backing store then
        // MyGetItemInfo should HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND).
        // If this is some other error, e.g. E_OUTOFMEMORY because MyGetItemInfo
        // couldn't allocate space for backingStoreName, we return that.
        return hr;
    }

    // If the file path is for a symbolic link, pass that in with the placeholder info.
    if (symlinkTarget != NULL)
    {
        PRJ_EXTENDED_INFO extraInfo = {};

        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
        extraInfo.Symlink.TargetName = symlinkTarget;

        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo2(callbackData->NamespaceVirtualizationContext,
                                      backingStoreName,
                                      &placeholderInfo,
                                      sizeof(placeholderInfo),
                                      &extraInfo);
    }
    else
    {
        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo(callbackData->NamespaceVirtualizationContext,
                                     backingStoreName,
                                     &placeholderInfo,
                                     sizeof(placeholderInfo));
    }

    free(backingStoreName);

    if (symlinkTarget != NULL)
    {
        free(symlinkTarget);
    }

    return hr;
}
```

## <a name="providing-file-contents"></a><span data-ttu-id="063e6-125">Bereitstellen von Dateiinhalten</span><span class="sxs-lookup"><span data-stu-id="063e6-125">Providing File Contents</span></span>

<span data-ttu-id="063e6-126">Wenn projfs sicherstellen muss, dass eine virtualisierte Datei Daten enthält, z. b. Wenn eine Anwendung versucht, aus der Datei zu lesen, ruft projfs den **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** Rückruf für dieses Element auf, um anzufordern, dass der Anbieter den Inhalt der Datei bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="063e6-126">When ProjFS needs to ensure that a virtualized file contains data, such as when an application attempts to read from the file, ProjFS calls the **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** callback for that item to request that the provider supply the file's contents.</span></span>  <span data-ttu-id="063e6-127">Der Anbieter Ruft die Daten der Datei aus dem Sicherungs Speicher ab und verwendet **[prjschreitefiledata](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** , um die Daten an das lokale Dateisystem zu senden.</span><span class="sxs-lookup"><span data-stu-id="063e6-127">The provider retrieves the file's data from its backing store and uses **[PrjWriteFileData](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** to send the data to the local file system.</span></span>

> <span data-ttu-id="063e6-128">Wenn dieser Rückruf von projfs aufgerufen wird, gibt das **FilePathName** -Element des _callBackData_ -Parameters den Namen an, den die Datei bei der Erstellung des Platzhalters enthielt.</span><span class="sxs-lookup"><span data-stu-id="063e6-128">When ProjFS calls this callback, the **FilePathName** member of the _callbackData_ parameter supplies the name the file had when its placeholder was created.</span></span>  <span data-ttu-id="063e6-129">Das heißt, wenn die Datei umbenannt wurde, seit der Platzhalter erstellt wurde, stellt der Rückruf den ursprünglichen Namen (vor dem Umbenennen) und nicht den aktuellen Namen (nach dem Umbenennen) bereit.</span><span class="sxs-lookup"><span data-stu-id="063e6-129">That is, if the file has been renamed since its placeholder was created, the callback supplies the original (pre-rename) name, not the current (post-rename) name.</span></span>  <span data-ttu-id="063e6-130">Bei Bedarf kann der Anbieter den **VERSIONINFO** -Member des _callBackData_ -Parameters verwenden, um zu bestimmen, welche Datei Daten angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="063e6-130">If necessary, the provider can use the **VersionInfo** member of the _callbackData_ parameter to determine which file's data is being requested.</span></span>
>
> <span data-ttu-id="063e6-131">Weitere Informationen zur Verwendung des **VERSIONINFO** -Members von PRJ_CALLBACK_DATA finden Sie in der Dokumentation zu [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) und im Thema [Bearbeiten von Änderungs Änderungen](handling-view-changes.md) .</span><span class="sxs-lookup"><span data-stu-id="063e6-131">For more information on how the **VersionInfo** member of PRJ_CALLBACK_DATA may be used, see the documentation for [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) and the [Handling View Changes](handling-view-changes.md) topic.</span></span>

<span data-ttu-id="063e6-132">Der Anbieter darf den Bereich der im **PRJ_GET_FILE_DATA_CB** Rückruf angeforderten Daten in mehrere Aufrufe von **prjschreitefiledata** aufteilen, die jeweils einen Teil des angeforderten Bereichs bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="063e6-132">The provider is allowed to split the range of data requested in the **PRJ_GET_FILE_DATA_CB** callback into multiple calls to **PrjWriteFileData**, each supplying a portion of the requested range.</span></span>  <span data-ttu-id="063e6-133">Der Anbieter muss jedoch den gesamten angeforderten Bereich angeben, bevor der Rückruf abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="063e6-133">However, the provider must supply the entire requested range before completing the callback.</span></span>  <span data-ttu-id="063e6-134">Wenn der Rückruf z. b. 10 MB von _Byteoffset_ 0 für die _Länge_ 10.485.760 anfordert, kann der Anbieter die Daten in 10 Aufrufen an **prjschreitefiledata** bereitstellen, die jeweils 1 MB senden.</span><span class="sxs-lookup"><span data-stu-id="063e6-134">For example, if the callback requests 10 MB of data from _byteOffset_ 0 for _length_ 10,485,760, the provider may choose to supply the data in 10 calls to **PrjWriteFileData**, each sending 1 MB.</span></span>

<span data-ttu-id="063e6-135">Der Anbieter kann auch mehr als den angeforderten Bereich angeben, bis zur Länge der Datei.</span><span class="sxs-lookup"><span data-stu-id="063e6-135">The provider is also free to supply more than the requested range, up to the length of the file.</span></span>  <span data-ttu-id="063e6-136">Der Bereich, den der Anbieter bereitstellt, muss den angeforderten Bereich abdecken.</span><span class="sxs-lookup"><span data-stu-id="063e6-136">The range the provider supplies must cover the requested range.</span></span>  <span data-ttu-id="063e6-137">Wenn der Rückruf z. b. 1 MB Daten von _Byteoffset_ 4096 für die _Länge_ 1.052.672 anfordert und die Datei eine Gesamtgröße von 10 MB hat, kann der Anbieter die Rückgabe von 2 MB Daten ab dem Offset 0 auswählen.</span><span class="sxs-lookup"><span data-stu-id="063e6-137">For example, if the callback requests 1 MB of data from _byteOffset_ 4096 for _length_ 1,052,672, and the file has a total size of 10 MB, the provider could choose to return 2 MB of data starting at offset 0.</span></span>

### <a name="buffer-alignment-considerations"></a><span data-ttu-id="063e6-138">Überlegungen zur Puffer Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="063e6-138">Buffer Alignment Considerations</span></span>

<span data-ttu-id="063e6-139">Projfs verwendet die [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) des Aufrufers, der die Daten zum Schreiben der Daten in das lokale Dateisystem benötigt.</span><span class="sxs-lookup"><span data-stu-id="063e6-139">ProjFS uses the [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) from the caller who requires the data to write the data to the local file system.</span></span>  <span data-ttu-id="063e6-140">Projfs kann jedoch nicht steuern, ob diese FILE_OBJECT für gepufferte oder nicht gepufferte e/a-Vorgänge geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="063e6-140">However ProjFS cannot control whether that FILE_OBJECT was opened for buffered or unbuffered I/O.</span></span>  <span data-ttu-id="063e6-141">Wenn die FILE_OBJECT für nicht gepufferte e/a-Vorgänge geöffnet wurde, müssen Lese-und Schreibvorgänge in die Datei bestimmte Ausrichtungs Anforderungen einhalten.</span><span class="sxs-lookup"><span data-stu-id="063e6-141">If the FILE_OBJECT was opened for unbuffered I/O, reads and writes to the file must adhere to certain alignment requirements.</span></span>  <span data-ttu-id="063e6-142">Der Anbieter kann diese Ausrichtungs Anforderungen durch zwei Dinge erfüllen:</span><span class="sxs-lookup"><span data-stu-id="063e6-142">The provider can meet those alignment requirements by doing two things:</span></span>

1. <span data-ttu-id="063e6-143">Verwenden Sie **[prjallocatealignedbuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** , um den Puffer zuzuweisen, der in den _Puffer_ Parameter **prjschreitefiledata** übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="063e6-143">Use **[PrjAllocateAlignedBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** to allocate the buffer to pass in **PrjWriteFileData**'s _buffer_ parameter.</span></span>
1. <span data-ttu-id="063e6-144">Stellen Sie sicher, dass die Parameter " _Byteoffset_ " und " _length_ " von " **prjschreitefiledata** " ein ganzzahliges Vielfache der Ausrichtungs Anforderung des Speichergeräts sind (Beachten Sie, dass der _length_ -Parameter diese Anforderung nicht erfüllen muss, wenn die _Byteoffset_-  +  _Länge_ gleich dem Dateiende ist).</span><span class="sxs-lookup"><span data-stu-id="063e6-144">Ensure that the _byteOffset_ and _length_ parameters of **PrjWriteFileData** are integer multiples of the storage device's alignment requirement (note that the _length_ parameter does not have to meet this requirement if _byteOffset_ + _length_ is equal to the end of the file).</span></span>  <span data-ttu-id="063e6-145">Der Anbieter kann **[prjgetvirtualizationinstanceinfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** verwenden, um die Ausrichtungs Anforderung des Speichergeräts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="063e6-145">The provider can use **[PrjGetVirtualizationInstanceInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** to retrieve the storage device's alignment requirement.</span></span>

<span data-ttu-id="063e6-146">Projfs verlässt den Anbieter, um die richtige Ausrichtung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="063e6-146">ProjFS leaves it up to the provider to calculate proper alignment.</span></span>  <span data-ttu-id="063e6-147">Dies liegt daran, dass bei der Verarbeitung eines **PRJ_GET_FILE_DATA_CB** Rückrufs der Anbieter die angeforderten Daten möglicherweise über mehrere **prjwrite tefiledata** -Aufrufe zurückgibt, die jeweils einen Teil der gesamten angeforderten Daten zurückgeben, bevor Sie den Rückruf abschließen.</span><span class="sxs-lookup"><span data-stu-id="063e6-147">This is because when processing a **PRJ_GET_FILE_DATA_CB** callback the provider may opt to return the requested data across multiple **PrjWriteFileData** calls, each returning part of the total requested data, before completing the callback.</span></span>

> <span data-ttu-id="063e6-148">Wenn der Anbieter einen einzelnen Befehl an **prjschreitefiledata** verwenden soll, um entweder die gesamte Datei zu schreiben, d. h. von _Byteoffset_ = 0 bis _length_ = Größe der Datei, oder wenn der genaue Bereich zurückgegeben werden soll, der im **PRJ_GET_FILE_DATA_CB** Rückruf angefordert wurde, muss der Anbieter keine Ausrichtungs Berechnungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="063e6-148">If the provider is going to use a single call to **PrjWriteFileData** to either write the entire file, i.e. from _byteOffset_ = 0 to _length_ = size of the file, or to return the exact range requested in the **PRJ_GET_FILE_DATA_CB** callback, the provider does not have to do any alignment calculations.</span></span>  <span data-ttu-id="063e6-149">Es muss jedoch weiterhin **prjzuzucatealignedbuffer** verwendet werden, um sicherzustellen, dass der _Puffer_ den Ausrichtungs Anforderungen des Speichergeräts entspricht.</span><span class="sxs-lookup"><span data-stu-id="063e6-149">However, it must still use **PrjAllocateAlignedBuffer** to ensure that _buffer_ meets the storage device’s alignment requirements.</span></span>

<span data-ttu-id="063e6-150">Weitere Informationen zu gepufferten und nicht gepufferten e/a-Vorgängen finden Sie im Thema [Datei Pufferung](/windows/desktop/FileIO/file-buffering) .</span><span class="sxs-lookup"><span data-stu-id="063e6-150">See the topic [File Buffering](/windows/desktop/FileIO/file-buffering) for more information on buffered vs. unbuffered I/O.</span></span>

```C++
//  BlockAlignTruncate(): Aligns P on the previous V boundary (V must be != 0).
#define BlockAlignTruncate(P,V) ((P) & (0-((UINT64)(V))))

// This sample illustrates both returning the entire requested range in a
// single call to PrjWriteFileData(), and splitting it up into smaller 
// units.  Note that the provider must return all the requested data before
// completing the PRJ_GET_FILE_DATA_CB callback with S_OK.
HRESULT
MyGetFileDataCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ UINT64 byteOffset,
    _In_ UINT32 length
    )
{
    HRESULT hr;

    // For the purposes of this sample our provider has a 1 MB limit to how
    // much data it can return at once (perhaps its backing store imposes such
    // a limit).
    UINT64 writeStartOffset;
    UINT32 writeLength;
    if (length <= 1024*1024)
    {
        // The range requested in the callback is less than 1MB, so we can return
        // the data in a single call, without doing any alignment calculations.
        writeStartOffset = byteOffset;
        writeLength = length;
    }
    else
    {
        // The range requested is more than 1MB.  Retrieve the device alignment
        // and calculate a transfer size that conforms to the device alignment and
        // is <= 1MB.
        PRJ_VIRTUALIZATION_INSTANCE_INFO instanceInfo;
        UINT32 infoSize = sizeof(instanceInfo);
        hr = PrjGetVirtualizationInstanceInfo(callbackData->NamespaceVirtualizationContext,
                                              &infoSize,
                                              &instanceInfo);

        if (FAILED(hr))
        {
            return hr;
        }

        // The first transfer will start at the beginning of the requested range,
        // which is guaranteed to have the correct alignment.
        writeStartOffset = byteOffset;

        // Ensure our transfer size is aligned to the device alignment, and is
        // no larger than 1 MB (note this assumes the device alignment is less
        // than 1 MB).
        UINT64 writeEndOffset = BlockAlignTruncate(writeStartOffset + 1024*1024,
                                                   instanceInfo->WriteAlignment);
        assert(writeEndOffset > 0);
        assert(writeEndOffset > writeStartOffset);

        writeLength = writeEndOffset - writeStartOffset;
    }

    // Allocate a buffer that adheres to the needed memory alignment.
    void* writeBuffer = NULL;
    writeBuffer = PrjAllocateAlignedBuffer(callbackData->NamespaceVirtualizationContext,
                                           writeLength);

    if (writeBuffer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    do
    {
        // MyGetFileDataFromStore is a routine the provider might implement to copy
        // data for the specified file from the provider's backing store to a
        // buffer.  The routine finds the file located at callbackData->FilePathName
        // and copies writeLength bytes of its data, starting at writeStartOffset,
        // to the buffer pointed to by writeBuffer.
        hr = MyGetFileDataFromStore(callbackData->FilePathName,
                                    writeStartOffset,
                                    writeLength,
                                    writeBuffer);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // Write the data to the file in the local file system.
        hr = PrjWriteFileData(callbackData->NamespaceVirtualizationContext,
                              callbackData->DataStreamId,
                              writeBuffer,
                              writeStartOffset,
                              writeLength);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // The length parameter to the callback is guaranteed to be either
        // correctly aligned or to result in a write to the end of the file.
        length -= writeLength;
        if (length < writeLength)
        {
            writeLength = length;
        }
    }
    while (writeLength > 0);

    PrjFreeAlignedBuffer(writeBuffer);
    return hr;
}
```