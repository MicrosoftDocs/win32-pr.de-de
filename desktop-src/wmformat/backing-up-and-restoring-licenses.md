---
title: Sichern und Wiederherstellen von Lizenzen
description: Sichern und Wiederherstellen von Lizenzen
ms.assetid: 59be02fe-f207-4161-8765-9a88a8050248
keywords:
- Windows Media-Format-SDK, Sichern von Lizenzen
- Windows Media-Format-SDK, Wiederherstellen von Lizenzen
- Windows Media-Format-SDK, Lizenz Sicherung und-Wiederherstellung
- Advanced Systems Format (ASF), Sichern von Lizenzen
- ASF (Advanced Systems Format), Sichern von Lizenzen
- Advanced Systems Format (ASF), Wiederherstellen von Lizenzen
- ASF (Advanced Systems Format), Wiederherstellen von Lizenzen
- Advanced Systems Format (ASF), Lizenz Sicherung und-Wiederherstellung
- ASF (Advanced Systems Format), Lizenz Sicherung und-Wiederherstellung
- Digital Rights Management (DRM), Sichern von Lizenzen
- DRM (Digital Rights Management), Sichern von Lizenzen
- Digital Rights Management (DRM), Wiederherstellen von Lizenzen
- DRM (Digital Rights Management), Wiederherstellen von Lizenzen
- Digital Rights Management (DRM), Lizenz Sicherung und-Wiederherstellung
- DRM (Digital Rights Management), Lizenz Sicherung und-Wiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10d8e76c191225288a1021e08e4c77e7e14f3c6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723528"
---
# <a name="backing-up-and-restoring-licenses"></a><span data-ttu-id="33330-118">Sichern und Wiederherstellen von Lizenzen</span><span class="sxs-lookup"><span data-stu-id="33330-118">Backing Up and Restoring Licenses</span></span>

<span data-ttu-id="33330-119">Die Sicherungs-und Wiederherstellungs Prozesse sind asynchron.</span><span class="sxs-lookup"><span data-stu-id="33330-119">The backup and restore processes are asynchronous.</span></span> <span data-ttu-id="33330-120">Sie werden ausgelöst, wenn der Benutzer einen Menübefehl oder eine Option in der Anwendung auswählt, um Lizenzen zu sichern oder wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="33330-120">They are triggered when the user selects a menu command or option in the application to back up or restore licenses.</span></span> <span data-ttu-id="33330-121">Sie sollten zulassen, dass der Benutzer die Orte angeben kann, an denen Lizenzen gesichert und wieder hergestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="33330-121">You should allow the user to specify the locations where licenses must be backed up to and restored from.</span></span>

<span data-ttu-id="33330-122">So sichern Sie Lizenzen:</span><span class="sxs-lookup"><span data-stu-id="33330-122">To back up licenses:</span></span>

1.  <span data-ttu-id="33330-123">Verwenden Sie die [**wmkreatebackuprestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) -Funktion, um das Backup Restorer-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="33330-123">Use the [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) function to create the backup restorer object.</span></span>
2.  <span data-ttu-id="33330-124">Rufen Sie die [**iwmbackuprestoreprop:: setprop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) -Methode auf, um den Sicherungs Pfad (den Speicherort, an den Sie die Dateien schreiben, z \\ . b. A: oder D: \\ Licenses) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="33330-124">Call the [**IWMBackupRestoreProps::SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) method to set the backup path (the location where you will write the files, such as A:\\ or D:\\Licenses).</span></span>
3.  <span data-ttu-id="33330-125">Nennen Sie die [**iwmlicenlbackup:: backuplicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) -Methode, um die Lizenzen im angegebenen Pfad zu sichern.</span><span class="sxs-lookup"><span data-stu-id="33330-125">Call the [**IWMLicenseBackup::BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) method to back up the licenses to the specified path.</span></span>

<span data-ttu-id="33330-126">Die folgenden Ereignisse werden an die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode gesendet:</span><span class="sxs-lookup"><span data-stu-id="33330-126">The following events are sent to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method:</span></span>

-   <span data-ttu-id="33330-127">**WMT \_ Backuprestore \_ Begin** gibt an, dass der Sicherungs Vorgang gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="33330-127">**WMT\_BACKUPRESTORE\_BEGIN** indicates the backup process has started.</span></span>
-   <span data-ttu-id="33330-128">**WMT \_ Backuprestore- \_ Ende** gibt an, dass der Sicherungs Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="33330-128">**WMT\_BACKUPRESTORE\_END** indicates the backup process has been completed.</span></span>
-   <span data-ttu-id="33330-129">**WMT \_ Eingeschränkte \_** Lizenzen gibt an, dass eine oder mehrere Lizenzen nicht gesichert werden können, da das Recht vom Besitzer des Inhalts nicht zugelassen wurde.</span><span class="sxs-lookup"><span data-stu-id="33330-129">**WMT\_RESTRICTED\_LICENSE** indicates that one or more licenses cannot be backed up because the right has been disallowed by the content owner.</span></span>

<span data-ttu-id="33330-130">Die Schlüssel-ID ist auch in dieser Nachricht enthalten.</span><span class="sxs-lookup"><span data-stu-id="33330-130">The key ID is also included in this message.</span></span> <span data-ttu-id="33330-131">Wenn Sie eine Datenbank für geschützte Dateien implementiert haben, die die Schlüssel-ID und die Metadaten enthält, können Sie dem Benutzer eine Meldung mit dem jeweiligen Titel (z. b. einem Buchtitel) anzeigen, für die die Lizenz nicht gesichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="33330-131">If you have implemented a database for protected files that includes the key ID and metadata, you can display a message to the user with the specific title (such as a song title) for which the license cannot be backed up.</span></span> <span data-ttu-id="33330-132">Andernfalls muss die Nachricht generisch sein und den Benutzer darüber informieren, dass einige Lizenzen nicht gesichert werden können.</span><span class="sxs-lookup"><span data-stu-id="33330-132">Otherwise, the message must be generic and inform the user that some licenses cannot be backed up.</span></span>

<span data-ttu-id="33330-133">So stellen Sie Lizenzen wieder her:</span><span class="sxs-lookup"><span data-stu-id="33330-133">To restore licenses:</span></span>

1.  <span data-ttu-id="33330-134">Verwenden Sie die **wmkreatebackuprestorer** -Funktion, um das Backup Restorer-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="33330-134">Use the **WMCreateBackupRestorer** function to create the backup restorer object.</span></span>
2.  <span data-ttu-id="33330-135">Rufen Sie die **iwmbackuprestoreprop:: setprop** -Methode auf, um den Wiederherstellungs Pfad auf den Speicherort festzulegen, an dem Lizenzen gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="33330-135">Call the **IWMBackupRestoreProps::SetProp** method to set the restore path to the location where licenses are backed up.</span></span>
3.  <span data-ttu-id="33330-136">Rufen Sie die [**iwmlicenserestore:: restorelicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) -Methode auf, um Lizenzen von diesem Speicherort wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="33330-136">Call the [**IWMLicenseRestore::RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) method to restore licenses from that location.</span></span>

<span data-ttu-id="33330-137">Die folgenden Ereignisse werden an die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode gesendet:</span><span class="sxs-lookup"><span data-stu-id="33330-137">The following events are sent to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method:</span></span>

-   <span data-ttu-id="33330-138">**WMT \_ Backuprestore- \_ Verbindung** gibt an, dass die Anwendung eine Verbindung mit dem Lizenz Verwaltungsdienst herstellt.</span><span class="sxs-lookup"><span data-stu-id="33330-138">**WMT\_BACKUPRESTORE\_CONNECTING** indicates that the application is connecting to the License Management Service.</span></span>
-   <span data-ttu-id="33330-139">**WMT \_ Durch die \_ Trennung von backuprestore** wird angegeben, dass die Verbindung mit dem Lizenz Verwaltungsdienst getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="33330-139">**WMT\_BACKUPRESTORE\_DISCONNECTING** indicates that the application is disconnecting from the License Management Service.</span></span>
-   <span data-ttu-id="33330-140">**WMT \_ Backuprestore \_ Begin** gibt an, dass der Wiederherstellungs Vorgang gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="33330-140">**WMT\_BACKUPRESTORE\_BEGIN** indicates the restore process has started.</span></span>
-   <span data-ttu-id="33330-141">**WMT \_ Backuprestore- \_ Ende** gibt an, dass der Wiederherstellungs Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="33330-141">**WMT\_BACKUPRESTORE\_END** indicates the restore process has been completed.</span></span>

> [!Note]  
> <span data-ttu-id="33330-142">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="33330-142">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="33330-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33330-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33330-144">**Features digitaler Rights Management**</span><span class="sxs-lookup"><span data-stu-id="33330-144">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="33330-145">**Iwmbackuprestoredie-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="33330-145">**IWMBackupRestoreProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[<span data-ttu-id="33330-146">**Iwmlicenabbackup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="33330-146">**IWMLicenseBackup Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[<span data-ttu-id="33330-147">**Iwmlicenserestore-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="33330-147">**IWMLicenseRestore Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 




