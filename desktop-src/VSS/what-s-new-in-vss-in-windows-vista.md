---
description: Windows Vista
ms.assetid: 3b16744d-b9c2-4462-a409-de94d9103c39
title: Neues in VSS in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 122caa350ede984d5b05eb7eedd6039d82a76f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356768"
---
# <a name="whats-new-in-vss-in-windows-vista"></a><span data-ttu-id="b6517-103">Neues in VSS in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6517-103">What's New in VSS in Windows Vista</span></span>

<span data-ttu-id="b6517-104">In Windows Vista werden die folgenden Änderungen am Volumeschattenkopie-Dienst eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b6517-104">Windows Vista introduces the following changes to the Volume Shadow Copy Service.</span></span>

<span data-ttu-id="b6517-105">Beachten Sie, dass alle Änderungen für Windows Vista auch für Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) gelten.</span><span class="sxs-lookup"><span data-stu-id="b6517-105">Note that all changes for Windows Vista also apply to Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

## <a name="new-vss-interfaces"></a><span data-ttu-id="b6517-106">Neue VSS-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b6517-106">New VSS Interfaces</span></span>

[<span data-ttu-id="b6517-107">**IVssBackupComponentsEx2**</span><span class="sxs-lookup"><span data-stu-id="b6517-107">**IVssBackupComponentsEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[<span data-ttu-id="b6517-108">**Ivsscomponstex**</span><span class="sxs-lookup"><span data-stu-id="b6517-108">**IVssComponentEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[<span data-ttu-id="b6517-109">**IVssCreateWriterMetadataEx**</span><span class="sxs-lookup"><span data-stu-id="b6517-109">**IVssCreateWriterMetadataEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[<span data-ttu-id="b6517-110">**IVssDifferentialSoftwareSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="b6517-110">**IVssDifferentialSoftwareSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[<span data-ttu-id="b6517-111">**IVssExamineWriterMetadataEx2**</span><span class="sxs-lookup"><span data-stu-id="b6517-111">**IVssExamineWriterMetadataEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a><span data-ttu-id="b6517-112">Neue VSS-Klassen</span><span class="sxs-lookup"><span data-stu-id="b6517-112">New VSS Classes</span></span>

[<span data-ttu-id="b6517-113">**Cvssbeschreiterex**</span><span class="sxs-lookup"><span data-stu-id="b6517-113">**CVssWriterEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a><span data-ttu-id="b6517-114">Neue VSS-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="b6517-114">New VSS Enumerations</span></span>

[<span data-ttu-id="b6517-115">**VSS- \_ Rollforward- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="b6517-115">**VSS\_ROLLFORWARD\_TYPE**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="b6517-116">Vorhandene Änderungen der VSS-Enumeration</span><span class="sxs-lookup"><span data-stu-id="b6517-116">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="b6517-117"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ Sicherungs \_ Schema**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) -Enumeration</span><span class="sxs-lookup"><span data-stu-id="b6517-117"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="b6517-118"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:</span><span class="sxs-lookup"><span data-stu-id="b6517-118"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="b6517-119">\_ \_ autorisierende \_ Wiederherstellung in VSS</span><span class="sxs-lookup"><span data-stu-id="b6517-119">VSS\_BS\_AUTHORITATIVE\_RESTORE</span></span>

<span data-ttu-id="b6517-120">\_ \_ \_ System \_ Status von VSS-SB (unabhängig)</span><span class="sxs-lookup"><span data-stu-id="b6517-120">VSS\_BS\_INDEPENDENT\_SYSTEM\_STATE</span></span>

<span data-ttu-id="b6517-121">Umbenennen von VSS- \_ \_ \_ Benennungen</span><span class="sxs-lookup"><span data-stu-id="b6517-121">VSS\_BS\_RESTORE\_RENAME</span></span>

<span data-ttu-id="b6517-122">VSS- \_ SB- \_ Roll Forward- \_ Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="b6517-122">VSS\_BS\_ROLLFORWARD\_RESTORE</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="b6517-123"><span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS \_ \_Komponentenflags**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags) -Enumeration</span><span class="sxs-lookup"><span data-stu-id="b6517-123"><span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS\_COMPONENT\_FLAGS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="b6517-124"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:</span><span class="sxs-lookup"><span data-stu-id="b6517-124"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="b6517-125">VSS \_ CF \_ nicht \_ System \_ Status</span><span class="sxs-lookup"><span data-stu-id="b6517-125">VSS\_CF\_NOT\_SYSTEM\_STATE</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="b6517-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeration der [**\_ VSS- \_ volumemomentaufnahme- \_ \_ Attribute**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)</span><span class="sxs-lookup"><span data-stu-id="b6517-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="b6517-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:</span><span class="sxs-lookup"><span data-stu-id="b6517-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="b6517-128">VSS \_ Volsnap \_ attr \_ No \_ AutoRecovery</span><span class="sxs-lookup"><span data-stu-id="b6517-128">VSS\_VOLSNAP\_ATTR\_NO\_AUTORECOVERY</span></span>

<span data-ttu-id="b6517-129">VSS- \_ Volsnap- \_ attr \_ nicht \_ transaktiv</span><span class="sxs-lookup"><span data-stu-id="b6517-129">VSS\_VOLSNAP\_ATTR\_NOT\_TRANSACTED</span></span>

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a><span data-ttu-id="b6517-130">VSS-Ereignis Ablauf Verfolgung und Protokollierung</span><span class="sxs-lookup"><span data-stu-id="b6517-130">VSS Event Tracing and Logging</span></span>

-   <span data-ttu-id="b6517-131">Die VSS-Ablauf Verfolgungs Datei kann sich jetzt auf einem beliebigen lokalen Volume befinden.</span><span class="sxs-lookup"><span data-stu-id="b6517-131">The VSS trace file can now be located on any local volume.</span></span> <span data-ttu-id="b6517-132">In Windows-Versionen vor Windows Vista konnte die VSS-Ablauf Verfolgungs Datei nicht auf einem Volume gefunden werden, das sich im Schattenkopiesatz befand.</span><span class="sxs-lookup"><span data-stu-id="b6517-132">On versions of Windows prior to Windows Vista, the VSS trace file could not be located on a volume that was in the shadow copy set.</span></span>
-   <span data-ttu-id="b6517-133">Viele Ereignisprotokoll Einträge wurden neu formuliert, um sie übersichtlicher zu machen.</span><span class="sxs-lookup"><span data-stu-id="b6517-133">Many event log entries have been reworded to make them clearer.</span></span>
-   <span data-ttu-id="b6517-134">Alle VSS-Ereignisprotokoll Einträge enthalten nun Kontextinformationen.</span><span class="sxs-lookup"><span data-stu-id="b6517-134">All VSS event log entries now contain context information.</span></span>

## <a name="vss-error-reporting"></a><span data-ttu-id="b6517-135">VSS-Fehlerberichterstattung</span><span class="sxs-lookup"><span data-stu-id="b6517-135">VSS Error Reporting</span></span>

-   <span data-ttu-id="b6517-136">Beschreibungen aller VSS-Fehlercodes können jetzt durch Aufrufen der [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ \_ \_ im *dwFlags* -Parameter angegebenen Flag "Format Message from HMODULE" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b6517-136">Descriptions of all VSS error codes can now be retrieved by calling the [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_HMODULE flag specified in the *dwFlags* parameter.</span></span>
-   <span data-ttu-id="b6517-137">Die VSS-Fehlercode Meldungen sind in vsstrace.dll enthalten.</span><span class="sxs-lookup"><span data-stu-id="b6517-137">The VSS error code messages are contained in vsstrace.dll.</span></span> <span data-ttu-id="b6517-138">Ein Handle für dieses Modul muss im *lpSource* -Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b6517-138">A handle to this module must be specified in the *lpSource* parameter.</span></span>

## <a name="excluding-files-from-shadow-copies"></a><span data-ttu-id="b6517-139">Ausschließen von Dateien aus Schatten Kopien</span><span class="sxs-lookup"><span data-stu-id="b6517-139">Excluding Files from Shadow Copies</span></span>

<span data-ttu-id="b6517-140">Anwendungen oder Dienste können den Registrierungsschlüssel filesnottosnapshot verwenden, um Dateien anzugeben, die aus neu erstellten Schatten Kopien gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b6517-140">Applications or services can use the FilesNotToSnapshot registry key to specify files to be deleted from newly created shadow copies.</span></span> <span data-ttu-id="b6517-141">Weitere Informationen finden Sie unter [Ausschließen von Dateien aus Schatten Kopien](excluding-files-from-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="b6517-141">For more information, see [Excluding Files from Shadow Copies](excluding-files-from-shadow-copies.md).</span></span>

## <a name="backup-and-restore-application-compatibility"></a><span data-ttu-id="b6517-142">Sichern und Wiederherstellen der Anwendungs Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="b6517-142">Backup and Restore Application Compatibility</span></span>

<span data-ttu-id="b6517-143">Entwickler von Sicherungs-und Wiederherstellungs Anwendungen müssen bestimmte neue Features in Windows Vista und Windows Server 2008 kennen.</span><span class="sxs-lookup"><span data-stu-id="b6517-143">Developers of backup and restore applications need to be aware of certain new features in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="b6517-144">Eine Checkliste zur Anwendungs Kompatibilität finden Sie unter [Anwendungs Kompatibilität für die Sicherung und Wiederherstellung](application-compatibility-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="b6517-144">For an application compatibility checklist, see [Application Compatibility for Backup and Restore](application-compatibility-for-backup-and-restore.md).</span></span>

 

 
