---
description: Zusammenfassung der VSS-API-Änderungen in Windows Server 2003
ms.assetid: 35572fc6-9147-4726-ae7a-d78292683ba0
title: Zusammenfassung der VSS-API-Änderungen in Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9154da0ac67dd7a599064ed3b5cf1dc7285b0fb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358833"
---
# <a name="summary-of-vss-api-changes-in-windows-server-2003"></a><span data-ttu-id="f4e27-103">Zusammenfassung der VSS-API-Änderungen in Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f4e27-103">Summary of VSS API Changes in Windows Server 2003</span></span>

## <a name="changes-in-the-vss-service"></a><span data-ttu-id="f4e27-104">Änderungen im VSS-Dienst</span><span class="sxs-lookup"><span data-stu-id="f4e27-104">Changes in the VSS Service</span></span>

<dl> <dt>

<span data-ttu-id="f4e27-105"><span id="Events_added_"></span><span id="events_added_"></span><span id="EVENTS_ADDED_"></span>Hinzugefügte Ereignisse:</span><span class="sxs-lookup"><span data-stu-id="f4e27-105"><span id="Events_added_"></span><span id="events_added_"></span><span id="EVENTS_ADDED_"></span>Events added:</span></span>
</dt> <dd>

[<span data-ttu-id="f4e27-106">*BackupShutdown*</span><span class="sxs-lookup"><span data-stu-id="f4e27-106">*BackupShutdown*</span></span>](vssgloss-b.md)

</dd> </dl>

## <a name="changes-in-vss-functionality"></a><span data-ttu-id="f4e27-107">Änderungen an der VSS-Funktionalität</span><span class="sxs-lookup"><span data-stu-id="f4e27-107">Changes in VSS Functionality</span></span>

<dl> <dt>

<span data-ttu-id="f4e27-108"><span id="Additional_functionality_"></span><span id="additional_functionality_"></span><span id="ADDITIONAL_FUNCTIONALITY_"></span>Zusätzliche Funktionen:</span><span class="sxs-lookup"><span data-stu-id="f4e27-108"><span id="Additional_functionality_"></span><span id="additional_functionality_"></span><span id="ADDITIONAL_FUNCTIONALITY_"></span>Additional functionality:</span></span>
</dt> <dd>

[<span data-ttu-id="f4e27-109">*Unterstützung für Teil Dateien*</span><span class="sxs-lookup"><span data-stu-id="f4e27-109">*partial file support*</span></span>](vssgloss-p.md)

[<span data-ttu-id="f4e27-110">*gesteuerte Ziel Ausrichtung*</span><span class="sxs-lookup"><span data-stu-id="f4e27-110">*directed targeting*</span></span>](vssgloss-d.md)

</dd> </dl>

## <a name="new-vss-interfaces"></a><span data-ttu-id="f4e27-111">Neue VSS-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f4e27-111">New VSS Interfaces</span></span>

[<span data-ttu-id="f4e27-112">**Ivsswmabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="f4e27-112">**IVssWMDependency**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="f4e27-113">Vorhandene Änderungen der VSS-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f4e27-113">Existing VSS Interface Modifications</span></span>

<dl> <dt>

<span data-ttu-id="f4e27-114"><span id="IVssAsync_interface"></span><span id="ivssasync_interface"></span><span id="IVSSASYNC_INTERFACE"></span>[**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync) -Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f4e27-114"><span id="IVssAsync_interface"></span><span id="ivssasync_interface"></span><span id="IVSSASYNC_INTERFACE"></span>[**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="f4e27-115"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Geänderte Methoden:</span><span class="sxs-lookup"><span data-stu-id="f4e27-115"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Methods modified:</span></span>
</dt> <dd>

[<span data-ttu-id="f4e27-116">**IVssAsync:: Wait**</span><span class="sxs-lookup"><span data-stu-id="f4e27-116">**IVssAsync::Wait**</span></span>](/windows/desktop/api/Vss/nf-vss-ivssasync-wait)

</dd> </dl> </dd> <dt>

<span data-ttu-id="f4e27-117"><span id="IVssBackupComponents_interface"></span><span id="ivssbackupcomponents_interface"></span><span id="IVSSBACKUPCOMPONENTS_INTERFACE"></span>[**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f4e27-117"><span id="IVssBackupComponents_interface"></span><span id="ivssbackupcomponents_interface"></span><span id="IVSSBACKUPCOMPONENTS_INTERFACE"></span>[**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="f4e27-118"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Hinzugefügte Methoden:</span><span class="sxs-lookup"><span data-stu-id="f4e27-118"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="f4e27-119">**IVssBackupComponents:: addnewtarget**</span><span class="sxs-lookup"><span data-stu-id="f4e27-119">**IVssBackupComponents::AddNewTarget**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)

[<span data-ttu-id="f4e27-120">**IVssBackupComponents:: queryrevertstatus**</span><span class="sxs-lookup"><span data-stu-id="f4e27-120">**IVssBackupComponents::QueryRevertStatus**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-queryrevertstatus)

[<span data-ttu-id="f4e27-121">**IVssBackupComponents:: revertum Snapshot**</span><span class="sxs-lookup"><span data-stu-id="f4e27-121">**IVssBackupComponents::RevertToSnapshot**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-reverttosnapshot)

[<span data-ttu-id="f4e27-122">**IVssBackupComponents:: Servername FilePath**</span><span class="sxs-lookup"><span data-stu-id="f4e27-122">**IVssBackupComponents::SetRangesFilePath**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)

[<span data-ttu-id="f4e27-123">**IVssBackupComponents:: abtrestorestate**</span><span class="sxs-lookup"><span data-stu-id="f4e27-123">**IVssBackupComponents::SetRestoreState**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)

</dd> </dl> </dd> <dt>

<span data-ttu-id="f4e27-124"><span id="IVssCreateWriterMetadata_interface"></span><span id="ivsscreatewritermetadata_interface"></span><span id="IVSSCREATEWRITERMETADATA_INTERFACE"></span>[**Ivsskreateschreitermetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) -Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f4e27-124"><span id="IVssCreateWriterMetadata_interface"></span><span id="ivsscreatewritermetadata_interface"></span><span id="IVSSCREATEWRITERMETADATA_INTERFACE"></span>[**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="f4e27-125"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Hinzugefügte Methoden:</span><span class="sxs-lookup"><span data-stu-id="f4e27-125"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="f4e27-126">**Ivsskreateschreitermetadata:: AddComponentDependency**</span><span class="sxs-lookup"><span data-stu-id="f4e27-126">**IVssCreateWriterMetadata::AddComponentDependency**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency)

[<span data-ttu-id="f4e27-127">**Ivsskreateschreitermetadata:: setbackupschema**</span><span class="sxs-lookup"><span data-stu-id="f4e27-127">**IVssCreateWriterMetadata::SetBackupSchema**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)

</dd> <dt>

<span data-ttu-id="f4e27-128"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Geänderte Methoden:</span><span class="sxs-lookup"><span data-stu-id="f4e27-128"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Methods modified:</span></span>
</dt> <dd>

[<span data-ttu-id="f4e27-129">**Ivsskreateschreitermetadata:: addComponent**</span><span class="sxs-lookup"><span data-stu-id="f4e27-129">**IVssCreateWriterMetadata::AddComponent**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)

[<span data-ttu-id="f4e27-130">**Ivsskreateschreitermetadata:: adddatabasefiles**</span><span class="sxs-lookup"><span data-stu-id="f4e27-130">**IVssCreateWriterMetadata::AddDatabaseFiles**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)

[<span data-ttu-id="f4e27-131">**Ivsskreateschreitermetadata:: adddatabaselogfiles**</span><span class="sxs-lookup"><span data-stu-id="f4e27-131">**IVssCreateWriterMetadata::AddDatabaseLogFiles**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)

[<span data-ttu-id="f4e27-132">**Ivsskreateschreitermetadata:: addfilestofilegroup**</span><span class="sxs-lookup"><span data-stu-id="f4e27-132">**IVssCreateWriterMetadata::AddFilesToFileGroup**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)

</dd> </dl> </dd> <dt>

<span data-ttu-id="f4e27-133"><span id="IVssExamineWriterMetadata_interface"></span><span id="ivssexaminewritermetadata_interface"></span><span id="IVSSEXAMINEWRITERMETADATA_INTERFACE"></span>[**Ivssexaminewrite Metadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) -Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f4e27-133"><span id="IVssExamineWriterMetadata_interface"></span><span id="ivssexaminewritermetadata_interface"></span><span id="IVSSEXAMINEWRITERMETADATA_INTERFACE"></span>[**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="f4e27-134"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Hinzugefügte Methoden:</span><span class="sxs-lookup"><span data-stu-id="f4e27-134"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="f4e27-135">**Ivssexaminewrite Metadata:: getbackupschema**</span><span class="sxs-lookup"><span data-stu-id="f4e27-135">**IVssExamineWriterMetadata::GetBackupSchema**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)

</dd> </dl> </dd> <dt>

<span data-ttu-id="f4e27-136"><span id="IVssComponent_interface"></span><span id="ivsscomponent_interface"></span><span id="IVSSCOMPONENT_INTERFACE"></span>[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f4e27-136"><span id="IVssComponent_interface"></span><span id="ivsscomponent_interface"></span><span id="IVSSCOMPONENT_INTERFACE"></span>[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="f4e27-137"><span id="Methods_removed_"></span><span id="methods_removed_"></span><span id="METHODS_REMOVED_"></span>Entfernte Methoden:</span><span class="sxs-lookup"><span data-stu-id="f4e27-137"><span id="Methods_removed_"></span><span id="methods_removed_"></span><span id="METHODS_REMOVED_"></span>Methods removed:</span></span>
</dt> <dd>

<span data-ttu-id="f4e27-138">**IVssComponent:: addnewtarget**</span><span class="sxs-lookup"><span data-stu-id="f4e27-138">**IVssComponent::AddNewTarget**</span></span>

</dd> <dt>

<span data-ttu-id="f4e27-139"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Hinzugefügte Methoden:</span><span class="sxs-lookup"><span data-stu-id="f4e27-139"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="f4e27-140">**IVssComponent:: AddDifferencedFilesByLastModifyTime**</span><span class="sxs-lookup"><span data-stu-id="f4e27-140">**IVssComponent::AddDifferencedFilesByLastModifyTime**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)

[<span data-ttu-id="f4e27-141">**IVssComponent:: getdifferencedfile**</span><span class="sxs-lookup"><span data-stu-id="f4e27-141">**IVssComponent::GetDifferencedFile**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)

[<span data-ttu-id="f4e27-142">**IVssComponent:: getdifferencedfilescount**</span><span class="sxs-lookup"><span data-stu-id="f4e27-142">**IVssComponent::GetDifferencedFilesCount**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)

</dd> <dt>

<span data-ttu-id="f4e27-143"><span id="Methods_no_longer_reserved_"></span><span id="methods_no_longer_reserved_"></span><span id="METHODS_NO_LONGER_RESERVED_"></span>Nicht mehr reservierte Methoden:</span><span class="sxs-lookup"><span data-stu-id="f4e27-143"><span id="Methods_no_longer_reserved_"></span><span id="methods_no_longer_reserved_"></span><span id="METHODS_NO_LONGER_RESERVED_"></span>Methods no longer reserved:</span></span>
</dt> <dd>

[<span data-ttu-id="f4e27-144">**IVssComponent:: adddirectedtarget**</span><span class="sxs-lookup"><span data-stu-id="f4e27-144">**IVssComponent::AddDirectedTarget**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)

[<span data-ttu-id="f4e27-145">**IVssComponent:: getdirectedtarget**</span><span class="sxs-lookup"><span data-stu-id="f4e27-145">**IVssComponent::GetDirectedTarget**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)

</dd> </dl> </dd> <dt>

<span data-ttu-id="f4e27-146"><span id="IVssWMComponent_interface"></span><span id="ivsswmcomponent_interface"></span><span id="IVSSWMCOMPONENT_INTERFACE"></span>[**Ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) -Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f4e27-146"><span id="IVssWMComponent_interface"></span><span id="ivsswmcomponent_interface"></span><span id="IVSSWMCOMPONENT_INTERFACE"></span>[**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="f4e27-147"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Hinzugefügte Methoden:</span><span class="sxs-lookup"><span data-stu-id="f4e27-147"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="f4e27-148">**Ivsswmcomponent:: getabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="f4e27-148">**IVssWMComponent::GetDependency**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency)

</dd> </dl> </dd> <dt>

<span data-ttu-id="f4e27-149"><span id="IVssWMFiledesc_interface"></span><span id="ivsswmfiledesc_interface"></span><span id="IVSSWMFILEDESC_INTERFACE"></span>[**Ivsswmfiledebug**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) -Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f4e27-149"><span id="IVssWMFiledesc_interface"></span><span id="ivsswmfiledesc_interface"></span><span id="IVSSWMFILEDESC_INTERFACE"></span>[**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="f4e27-150"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Hinzugefügte Methoden:</span><span class="sxs-lookup"><span data-stu-id="f4e27-150"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="f4e27-151">**Ivsswmfiledebug:: getbackuptypemask**</span><span class="sxs-lookup"><span data-stu-id="f4e27-151">**IVssWMFiledesc::GetBackupTypeMask**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)

</dd> </dl> </dd> </dl>

## <a name="existing-vss-class-modifications"></a><span data-ttu-id="f4e27-152">Vorhandene Änderungen der VSS-Klasse</span><span class="sxs-lookup"><span data-stu-id="f4e27-152">Existing VSS Class Modifications</span></span>

<dl> <dt>

<span data-ttu-id="f4e27-153"><span id="CVssWriter_class"></span><span id="cvsswriter_class"></span><span id="CVSSWRITER_CLASS"></span>[**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) -Klasse</span><span class="sxs-lookup"><span data-stu-id="f4e27-153"><span id="CVssWriter_class"></span><span id="cvsswriter_class"></span><span id="CVSSWRITER_CLASS"></span>[**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) class</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="f4e27-154"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Geänderte Methoden:</span><span class="sxs-lookup"><span data-stu-id="f4e27-154"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Methods modified:</span></span>
</dt> <dd>

[<span data-ttu-id="f4e27-155">**CVssWriter:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="f4e27-155">**CVssWriter::Initialize**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)

</dd> <dt>

<span data-ttu-id="f4e27-156"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Hinzugefügte Methoden:</span><span class="sxs-lookup"><span data-stu-id="f4e27-156"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="f4e27-157">**CVssWriter:: GetContext**</span><span class="sxs-lookup"><span data-stu-id="f4e27-157">**CVssWriter::GetContext**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext)

[<span data-ttu-id="f4e27-158">**CVssWriter:: getrestoretype**</span><span class="sxs-lookup"><span data-stu-id="f4e27-158">**CVssWriter::GetRestoreType**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)

[<span data-ttu-id="f4e27-159">**CVssWriter:: geznapshotdevicename**</span><span class="sxs-lookup"><span data-stu-id="f4e27-159">**CVssWriter::GetSnapshotDeviceName**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)

[<span data-ttu-id="f4e27-160">**CVssWriter:: OnBackupShutdown**</span><span class="sxs-lookup"><span data-stu-id="f4e27-160">**CVssWriter::OnBackupShutdown**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)

</dd> </dl> </dd> </dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="f4e27-161">Neue VSS-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="f4e27-161">New VSS Enumerations</span></span>

<dl> <dt>

<span data-ttu-id="f4e27-162"><span id="VSS_BACKUP_SCHEMA"></span><span id="vss_backup_schema"></span>[**VSS- \_ Sicherungs \_ Schema**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)</span><span class="sxs-lookup"><span data-stu-id="f4e27-162"><span id="VSS_BACKUP_SCHEMA"></span><span id="vss_backup_schema"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f4e27-163"><span id="VSS_COMPONENT_FLAGS"></span><span id="vss_component_flags"></span>[**VSS \_ - \_ Komponentenflags**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)</span><span class="sxs-lookup"><span data-stu-id="f4e27-163"><span id="VSS_COMPONENT_FLAGS"></span><span id="vss_component_flags"></span>[**VSS\_COMPONENT\_FLAGS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f4e27-164"><span id="VSS_FILE_SPEC_BACKUP_TYPE"></span><span id="vss_file_spec_backup_type"></span>[**Sicherungstyp der VSS- \_ Datei \_ Spezifikation \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)</span><span class="sxs-lookup"><span data-stu-id="f4e27-164"><span id="VSS_FILE_SPEC_BACKUP_TYPE"></span><span id="vss_file_spec_backup_type"></span>[**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f4e27-165"><span id="VSS_RESTORE_TYPE"></span><span id="vss_restore_type"></span>[**VSS \_ - \_ Wiederherstellungstyp**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)</span><span class="sxs-lookup"><span data-stu-id="f4e27-165"><span id="VSS_RESTORE_TYPE"></span><span id="vss_restore_type"></span>[**VSS\_RESTORE\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)</span></span>
<span data-ttu-id="f4e27-166"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f4e27-166"></dt> <dd></dd> </dl></span></span>

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="f4e27-167">Vorhandene Änderungen der VSS-Enumeration</span><span class="sxs-lookup"><span data-stu-id="f4e27-167">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="f4e27-168"><span id="VSS_BACKUP_TYPE_enumeration"></span><span id="vss_backup_type_enumeration"></span><span id="VSS_BACKUP_TYPE_ENUMERATION"></span>[**VSS \_ \_Sicherungstyp**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) -Enumeration</span><span class="sxs-lookup"><span data-stu-id="f4e27-168"><span id="VSS_BACKUP_TYPE_enumeration"></span><span id="vss_backup_type_enumeration"></span><span id="VSS_BACKUP_TYPE_ENUMERATION"></span>[**VSS\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="f4e27-169"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:</span><span class="sxs-lookup"><span data-stu-id="f4e27-169"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="f4e27-170">VSS \_ BT- \_ Kopie</span><span class="sxs-lookup"><span data-stu-id="f4e27-170">VSS\_BT\_COPY</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f4e27-171"><span id="VSS_RESTORE_TARGET_enumeration"></span><span id="vss_restore_target_enumeration"></span><span id="VSS_RESTORE_TARGET_ENUMERATION"></span>[**VSS \_ \_Zielenumeration wiederherstellen**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target)</span><span class="sxs-lookup"><span data-stu-id="f4e27-171"><span id="VSS_RESTORE_TARGET_enumeration"></span><span id="vss_restore_target_enumeration"></span><span id="VSS_RESTORE_TARGET_ENUMERATION"></span>[**VSS\_RESTORE\_TARGET**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="f4e27-172"><span id="Removed_values_"></span><span id="removed_values_"></span><span id="REMOVED_VALUES_"></span>Entfernte Werte:</span><span class="sxs-lookup"><span data-stu-id="f4e27-172"><span id="Removed_values_"></span><span id="removed_values_"></span><span id="REMOVED_VALUES_"></span>Removed values:</span></span>
</dt> <dd>

<span data-ttu-id="f4e27-173">VSS \_ RT \_ neu</span><span class="sxs-lookup"><span data-stu-id="f4e27-173">VSS\_RT\_NEW</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f4e27-174"><span id="VSS_RESTOREMETHOD_ENUM_enumeration"></span><span id="vss_restoremethod_enum_enumeration"></span><span id="VSS_RESTOREMETHOD_ENUM_ENUMERATION"></span>[**VSS \_ Restoremethod \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) -Enumeration</span><span class="sxs-lookup"><span data-stu-id="f4e27-174"><span id="VSS_RESTOREMETHOD_ENUM_enumeration"></span><span id="vss_restoremethod_enum_enumeration"></span><span id="VSS_RESTOREMETHOD_ENUM_ENUMERATION"></span>[**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="f4e27-175"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:</span><span class="sxs-lookup"><span data-stu-id="f4e27-175"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="f4e27-176">VSS- \_ RME- \_ Wiederherstellung \_ beim \_ Neustart, \_ Wenn \_ nicht \_ ersetzen kann</span><span class="sxs-lookup"><span data-stu-id="f4e27-176">VSS\_RME\_RESTORE\_AT\_REBOOT\_IF\_CANNOT\_REPLACE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f4e27-177"><span id="VSS_SNAPSHOT_STATE_enumeration"></span><span id="vss_snapshot_state_enumeration"></span><span id="VSS_SNAPSHOT_STATE_ENUMERATION"></span>[**VSS \_ Snapshot \_ State**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state) -Enumeration</span><span class="sxs-lookup"><span data-stu-id="f4e27-177"><span id="VSS_SNAPSHOT_STATE_enumeration"></span><span id="vss_snapshot_state_enumeration"></span><span id="VSS_SNAPSHOT_STATE_ENUMERATION"></span>[**VSS\_SNAPSHOT\_STATE**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="f4e27-178"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:</span><span class="sxs-lookup"><span data-stu-id="f4e27-178"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="f4e27-179">VSS \_ SS- \_ Verarbeitungs \_ postcommit</span><span class="sxs-lookup"><span data-stu-id="f4e27-179">VSS\_SS\_PROCESSING\_POSTCOMMIT</span></span>

<span data-ttu-id="f4e27-180">\_prefinalcommit für VSS SS- \_ Verarbeitung \_</span><span class="sxs-lookup"><span data-stu-id="f4e27-180">VSS\_SS\_PROCESSING\_PREFINALCOMMIT</span></span>

<span data-ttu-id="f4e27-181">VSS \_ SS \_ prefinalcommit</span><span class="sxs-lookup"><span data-stu-id="f4e27-181">VSS\_SS\_PREFINALCOMMITTED</span></span>

<span data-ttu-id="f4e27-182">VSS \_ SS- \_ Verarbeitung von \_ postfinalcommit</span><span class="sxs-lookup"><span data-stu-id="f4e27-182">VSS\_SS\_PROCESSING\_POSTFINALCOMMIT</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f4e27-183"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeration der [**\_ VSS- \_ volumemomentaufnahme- \_ \_ Attribute**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)</span><span class="sxs-lookup"><span data-stu-id="f4e27-183"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="f4e27-184"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:</span><span class="sxs-lookup"><span data-stu-id="f4e27-184"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="f4e27-185">VSS \_ Volsnap \_ attr \_ AutoRecover</span><span class="sxs-lookup"><span data-stu-id="f4e27-185">VSS\_VOLSNAP\_ATTR\_AUTORECOVER</span></span>

</dd> <dt>

<span data-ttu-id="f4e27-186"><span id="Reserved_values_now_support_"></span><span id="reserved_values_now_support_"></span><span id="RESERVED_VALUES_NOW_SUPPORT_"></span>Reservierte Werte unterstützen jetzt:</span><span class="sxs-lookup"><span data-stu-id="f4e27-186"><span id="Reserved_values_now_support_"></span><span id="reserved_values_now_support_"></span><span id="RESERVED_VALUES_NOW_SUPPORT_"></span>Reserved values now support:</span></span>
</dt> <dd>

<span data-ttu-id="f4e27-187">VSS \_ Volsnap \_ attr \_ Hardware unter \_ stützt</span><span class="sxs-lookup"><span data-stu-id="f4e27-187">VSS\_VOLSNAP\_ATTR\_HARDWARE\_ASSISTED</span></span>

<span data-ttu-id="f4e27-188">VSS- \_ Volsnap- \_ attr \_ importiert</span><span class="sxs-lookup"><span data-stu-id="f4e27-188">VSS\_VOLSNAP\_ATTR\_IMPORTED</span></span>

<span data-ttu-id="f4e27-189">lokales VSS- \_ Volsnap- \_ attr \_ \_</span><span class="sxs-lookup"><span data-stu-id="f4e27-189">VSS\_VOLSNAP\_ATTR\_EXPOSED\_LOCALLY</span></span>

<span data-ttu-id="f4e27-190">VSS- \_ Volsnap- \_ attr \_ \_ Remote verfügbar gemacht</span><span class="sxs-lookup"><span data-stu-id="f4e27-190">VSS\_VOLSNAP\_ATTR\_EXPOSED\_REMOTELY</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f4e27-191"><span id="VSS_WRITER_STATE_enumeration"></span><span id="vss_writer_state_enumeration"></span><span id="VSS_WRITER_STATE_ENUMERATION"></span>[**VSS \_ Writer \_ State**](/windows/desktop/api/Vss/ne-vss-vss_writer_state) -Enumeration</span><span class="sxs-lookup"><span data-stu-id="f4e27-191"><span id="VSS_WRITER_STATE_enumeration"></span><span id="vss_writer_state_enumeration"></span><span id="VSS_WRITER_STATE_ENUMERATION"></span>[**VSS\_WRITER\_STATE**](/windows/desktop/api/Vss/ne-vss-vss_writer_state) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="f4e27-192"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:</span><span class="sxs-lookup"><span data-stu-id="f4e27-192"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="f4e27-193">Fehler bei VSS \_ WS \_ \_ bei \_ BackupShutdown.</span><span class="sxs-lookup"><span data-stu-id="f4e27-193">VSS\_WS\_FAILED\_AT\_BACKUPSHUTDOWN</span></span>

</dd> </dl> </dd> </dl>

## <a name="changes-to-vss-structures"></a><span data-ttu-id="f4e27-194">Änderungen an VSS-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f4e27-194">Changes to VSS Structures</span></span>

<dl> <dt>

<span data-ttu-id="f4e27-195"><span id="VSS_COMPONENTINFO_structure"></span><span id="vss_componentinfo_structure"></span><span id="VSS_COMPONENTINFO_STRUCTURE"></span>[**VSS \_ ComponentInfo**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) -Struktur</span><span class="sxs-lookup"><span data-stu-id="f4e27-195"><span id="VSS_COMPONENTINFO_structure"></span><span id="vss_componentinfo_structure"></span><span id="VSS_COMPONENTINFO_STRUCTURE"></span>[**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="f4e27-196"><span id="Added_members_"></span><span id="added_members_"></span><span id="ADDED_MEMBERS_"></span>Hinzugefügte Mitglieder:</span><span class="sxs-lookup"><span data-stu-id="f4e27-196"><span id="Added_members_"></span><span id="added_members_"></span><span id="ADDED_MEMBERS_"></span>Added members:</span></span>
</dt> <dd>

<span data-ttu-id="f4e27-197">**bselectableforrestore**</span><span class="sxs-lookup"><span data-stu-id="f4e27-197">**bSelectableForRestore**</span></span>

<span data-ttu-id="f4e27-198">**dwcomponentflags**</span><span class="sxs-lookup"><span data-stu-id="f4e27-198">**dwComponentFlags**</span></span>

<span data-ttu-id="f4e27-199">**cabhängigkeiten**</span><span class="sxs-lookup"><span data-stu-id="f4e27-199">**cDependencies**</span></span>

</dd> </dl> </dd> </dl>

 

 



