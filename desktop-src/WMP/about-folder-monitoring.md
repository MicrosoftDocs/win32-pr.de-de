---
title: Informationen zur Ordner Überwachung
description: Informationen zur Ordner Überwachung
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Windows Media Player, Ordner Überwachung
- Windows Media Player-Objektmodell, Ordner Überwachung
- Objektmodell, Ordner Überwachung
- Windows Media Player ActiveX-Steuerelement, Ordner Überwachung
- ActiveX-Steuerelement, Ordner Überwachung
- Windows Media Player Mobile ActiveX-Steuerelement, Ordner Überwachung
- Windows Media Player Mobile, Ordner Überwachung
- Ordner Überwachung
- Überwachen von Ordnern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3d6af341df706cd85c4158197b27babad09c86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389833"
---
# <a name="about-folder-monitoring"></a><span data-ttu-id="a8ba1-112">Informationen zur Ordner Überwachung</span><span class="sxs-lookup"><span data-stu-id="a8ba1-112">About Folder Monitoring</span></span>

<span data-ttu-id="a8ba1-113">Windows-Media Player können Ordner überwachen, die digitale Mediendateien enthalten, und die Bibliothek aktualisieren, wenn Dateien hinzugefügt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-113">Windows Media Player can monitor folders that contain digital media files and update the library when files are added or removed.</span></span> <span data-ttu-id="a8ba1-114">Diese Ordner Überwachungsfunktion wird von der [iwmpfoldermonitorservices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) -Schnittstelle bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-114">This folder monitoring functionality is provided by the [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) interface.</span></span>

<span data-ttu-id="a8ba1-115">Um die Ordner Überwachungsdienste verwenden zu können, müssen Sie das Player-Objekt in einem Remote Zustand erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-115">To use the folder monitoring services, you must create the Player object in a remote state.</span></span> <span data-ttu-id="a8ba1-116">Weitere Informationen zum Remoting finden Sie unter [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span><span class="sxs-lookup"><span data-stu-id="a8ba1-116">For more information about remoting, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span> <span data-ttu-id="a8ba1-117">Nachdem Sie eine Remote Instanz des Players erstellt haben, können Sie einen Zeiger auf die **iwmpfoldermonitorservices** -Schnittstelle abrufen, indem Sie **QueryInterface** auf der [iwmpplayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) -Schnittstelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-117">After you have created a remoted instance of the player, obtain a pointer to the **IWMPFolderMonitorServices** interface by calling **QueryInterface** on the [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) interface.</span></span>

<span data-ttu-id="a8ba1-118">Windows Media Player eine Liste der überwachten Ordner beibehält.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-118">Windows Media Player keeps a list of folders that are being monitored.</span></span> <span data-ttu-id="a8ba1-119">Um eine Liste der überwachten Ordner zu erhalten, verwenden Sie die [iwmpfoldermonitorservices:: get \_ count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) -Methode und die [iwmpfoldermonitorservices:: Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-119">To get a list of monitored folders, use the [IWMPFolderMonitorServices::get\_count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) and [IWMPFolderMonitorServices::item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) methods.</span></span> <span data-ttu-id="a8ba1-120">Um der Liste Ordner hinzuzufügen oder Sie aus der Liste zu entfernen, verwenden Sie die [iwmpfoldermonitorservices:: Add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) -Methode bzw. die [Remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-120">To add folders to the list or remove them from the list, use the [IWMPFolderMonitorServices::add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) and [remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) methods, respectively.</span></span>

<span data-ttu-id="a8ba1-121">**Starten eines Scans**</span><span class="sxs-lookup"><span data-stu-id="a8ba1-121">**Starting a Scan**</span></span>

<span data-ttu-id="a8ba1-122">Die Überwachung von Ordnern ist normalerweise ein Hintergrundprozess, der nicht explizit aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-122">Monitoring of folders is normally a background process that does not need to be called explicitly.</span></span> <span data-ttu-id="a8ba1-123">Wenn Sie einen Ordner aktiv scannen möchten, nennen Sie [iwmpfoldermonitorservices:: StartScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan).</span><span class="sxs-lookup"><span data-stu-id="a8ba1-123">If you want to actively scan a folder, call [IWMPFolderMonitorServices::startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan).</span></span> <span data-ttu-id="a8ba1-124">Sie können eine laufende Überprüfung mit der [iwmpfoldermonitorservices:: StopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) -Methode beenden.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-124">You can stop a scan in progress with the [IWMPFolderMonitorServices::stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) method.</span></span>

<span data-ttu-id="a8ba1-125">**Der Ordner Überwachungs Status wird abgerufen.**</span><span class="sxs-lookup"><span data-stu-id="a8ba1-125">**Retrieving the Folder Monitoring Status**</span></span>

<span data-ttu-id="a8ba1-126">**Iwmpfoldermonitorservices** stellt Funktionen zum Abrufen des Status des Ordner Überwachungsprozesses bereit.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-126">**IWMPFolderMonitorServices** provides functionality for retrieving the status of the folder monitoring process.</span></span>

<span data-ttu-id="a8ba1-127">Die Ordner Überprüfung erfolgt in zwei Durchläufen.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-127">Folder scanning is done in two passes.</span></span> <span data-ttu-id="a8ba1-128">Im ersten Durchlauf scannt der Spieler die Ordner in der Liste der überwachten Ordner nacheinander und erstellt eine Liste der Dateien, die der Bibliothek hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-128">In the first pass, the Player scans the folders named in the monitored folders list one by one and builds a list of files to be added to the library.</span></span> <span data-ttu-id="a8ba1-129">Im zweiten Durchlauf durchläuft er die Liste der Dateien und fügt die Dateien der Bibliothek hinzu. Außerdem werden alle Medienelemente aus der Bibliothek entfernt, deren zugehörige physische Dateien aus dem Dateisystem gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-129">In the second pass, it goes through the list of files and adds the files to the library, and also removes any media items from the library whose corresponding physical files have been deleted from the file system.</span></span>

<span data-ttu-id="a8ba1-130">Das [folderscanstatechange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) -Ereignis wird verwendet, um das Programm zu benachrichtigen, wenn der Player in einen neuen Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-130">The [FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) event is used to notify your program whenever the Player switches to a new state.</span></span> <span data-ttu-id="a8ba1-131">Sie können den aktuellen Status auch abrufen, indem Sie [get \_ ScanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-131">You can also retrieve the current state by calling [get\_scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate).</span></span> <span data-ttu-id="a8ba1-132">Wenn der erste Durchlauf gestartet wird, lautet der aktuelle Zustandswert "wmpfssscan".</span><span class="sxs-lookup"><span data-stu-id="a8ba1-132">When the first pass starts, the current state value is wmpfssScanning.</span></span> <span data-ttu-id="a8ba1-133">Während des zweiten Durchlauf wechselt der Status zu "wmpfssupdating".</span><span class="sxs-lookup"><span data-stu-id="a8ba1-133">During the second pass, the state switches to wmpfssUpdating.</span></span> <span data-ttu-id="a8ba1-134">Nachdem der Vorgang abgeschlossen ist, ändert sich der Status in wmpfssbeendet.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-134">After the process is finished, the state changes to wmpfssStopped.</span></span>

<span data-ttu-id="a8ba1-135">Während der Player die überwachten Ordner beim ersten Durchlauf scannt, muss [get \_ scannedfilescount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) aufgerufen werden, um zu überprüfen, wie viele Dateien gescannt wurden.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-135">While the Player is scanning the monitored folders on the first pass, call [get\_scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) to check how many files have been scanned.</span></span> <span data-ttu-id="a8ba1-136">Mit der [get \_ CurrentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) -Methode wird angezeigt, welcher Ordner gerade gescannt wird.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-136">The [get\_currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) method will tell you which folder is currently being scanned.</span></span>

<span data-ttu-id="a8ba1-137">Nachdem der zweite Durchlauf gestartet wurde, können Sie [get \_ addedfilescount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) abrufen, um zu überprüfen, wie viele Dateien der Bibliothek hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-137">After the second pass starts, call [get\_addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) to check how many files have been added to the library.</span></span> <span data-ttu-id="a8ba1-138">Die [get \_ UpdateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) -Methode informiert Sie über den Status des zweiten Durchlauf, als Prozentwert zwischen 0 und 100.</span><span class="sxs-lookup"><span data-stu-id="a8ba1-138">The [get\_updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) method will tell you the progress of the second pass, as a percentage from 0 to 100.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8ba1-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a8ba1-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8ba1-140">**Informationen zum Player-Objektmodell**</span><span class="sxs-lookup"><span data-stu-id="a8ba1-140">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="a8ba1-141">**Iwmpfoldermonitorservices-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a8ba1-141">**IWMPFolderMonitorServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




