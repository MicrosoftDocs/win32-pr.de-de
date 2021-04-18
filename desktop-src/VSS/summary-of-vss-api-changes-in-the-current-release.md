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
# <a name="summary-of-vss-api-changes-in-windows-server-2003"></a>Zusammenfassung der VSS-API-Änderungen in Windows Server 2003

## <a name="changes-in-the-vss-service"></a>Änderungen im VSS-Dienst

<dl> <dt>

<span id="Events_added_"></span><span id="events_added_"></span><span id="EVENTS_ADDED_"></span>Hinzugefügte Ereignisse:
</dt> <dd>

[*BackupShutdown*](vssgloss-b.md)

</dd> </dl>

## <a name="changes-in-vss-functionality"></a>Änderungen an der VSS-Funktionalität

<dl> <dt>

<span id="Additional_functionality_"></span><span id="additional_functionality_"></span><span id="ADDITIONAL_FUNCTIONALITY_"></span>Zusätzliche Funktionen:
</dt> <dd>

[*Unterstützung für Teil Dateien*](vssgloss-p.md)

[*gesteuerte Ziel Ausrichtung*](vssgloss-d.md)

</dd> </dl>

## <a name="new-vss-interfaces"></a>Neue VSS-Schnittstellen

[**Ivsswmabhängigkeit**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)

## <a name="existing-vss-interface-modifications"></a>Vorhandene Änderungen der VSS-Schnittstelle

<dl> <dt>

<span id="IVssAsync_interface"></span><span id="ivssasync_interface"></span><span id="IVSSASYNC_INTERFACE"></span>[**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync) -Schnittstelle
</dt> <dd>

<dl> <dt>

<span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Geänderte Methoden:
</dt> <dd>

[**IVssAsync:: Wait**](/windows/desktop/api/Vss/nf-vss-ivssasync-wait)

</dd> </dl> </dd> <dt>

<span id="IVssBackupComponents_interface"></span><span id="ivssbackupcomponents_interface"></span><span id="IVSSBACKUPCOMPONENTS_INTERFACE"></span>[**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Hinzugefügte Methoden:
</dt> <dd>

[**IVssBackupComponents:: addnewtarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)

[**IVssBackupComponents:: queryrevertstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-queryrevertstatus)

[**IVssBackupComponents:: revertum Snapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-reverttosnapshot)

[**IVssBackupComponents:: Servername FilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)

[**IVssBackupComponents:: abtrestorestate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)

</dd> </dl> </dd> <dt>

<span id="IVssCreateWriterMetadata_interface"></span><span id="ivsscreatewritermetadata_interface"></span><span id="IVSSCREATEWRITERMETADATA_INTERFACE"></span>[**Ivsskreateschreitermetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) -Schnittstelle
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Hinzugefügte Methoden:
</dt> <dd>

[**Ivsskreateschreitermetadata:: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency)

[**Ivsskreateschreitermetadata:: setbackupschema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)

</dd> <dt>

<span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Geänderte Methoden:
</dt> <dd>

[**Ivsskreateschreitermetadata:: addComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)

[**Ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)

[**Ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)

[**Ivsskreateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)

</dd> </dl> </dd> <dt>

<span id="IVssExamineWriterMetadata_interface"></span><span id="ivssexaminewritermetadata_interface"></span><span id="IVSSEXAMINEWRITERMETADATA_INTERFACE"></span>[**Ivssexaminewrite Metadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) -Schnittstelle
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Hinzugefügte Methoden:
</dt> <dd>

[**Ivssexaminewrite Metadata:: getbackupschema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)

</dd> </dl> </dd> <dt>

<span id="IVssComponent_interface"></span><span id="ivsscomponent_interface"></span><span id="IVSSCOMPONENT_INTERFACE"></span>[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle
</dt> <dd>

<dl> <dt>

<span id="Methods_removed_"></span><span id="methods_removed_"></span><span id="METHODS_REMOVED_"></span>Entfernte Methoden:
</dt> <dd>

**IVssComponent:: addnewtarget**

</dd> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Hinzugefügte Methoden:
</dt> <dd>

[**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)

[**IVssComponent:: getdifferencedfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)

[**IVssComponent:: getdifferencedfilescount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)

</dd> <dt>

<span id="Methods_no_longer_reserved_"></span><span id="methods_no_longer_reserved_"></span><span id="METHODS_NO_LONGER_RESERVED_"></span>Nicht mehr reservierte Methoden:
</dt> <dd>

[**IVssComponent:: adddirectedtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)

[**IVssComponent:: getdirectedtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)

</dd> </dl> </dd> <dt>

<span id="IVssWMComponent_interface"></span><span id="ivsswmcomponent_interface"></span><span id="IVSSWMCOMPONENT_INTERFACE"></span>[**Ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) -Schnittstelle
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Hinzugefügte Methoden:
</dt> <dd>

[**Ivsswmcomponent:: getabhängigkeit**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency)

</dd> </dl> </dd> <dt>

<span id="IVssWMFiledesc_interface"></span><span id="ivsswmfiledesc_interface"></span><span id="IVSSWMFILEDESC_INTERFACE"></span>[**Ivsswmfiledebug**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) -Schnittstelle
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Hinzugefügte Methoden:
</dt> <dd>

[**Ivsswmfiledebug:: getbackuptypemask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)

</dd> </dl> </dd> </dl>

## <a name="existing-vss-class-modifications"></a>Vorhandene Änderungen der VSS-Klasse

<dl> <dt>

<span id="CVssWriter_class"></span><span id="cvsswriter_class"></span><span id="CVSSWRITER_CLASS"></span>[**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) -Klasse
</dt> <dd>

<dl> <dt>

<span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Geänderte Methoden:
</dt> <dd>

[**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)

</dd> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Hinzugefügte Methoden:
</dt> <dd>

[**CVssWriter:: GetContext**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext)

[**CVssWriter:: getrestoretype**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)

[**CVssWriter:: geznapshotdevicename**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)

[**CVssWriter:: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)

</dd> </dl> </dd> </dl>

## <a name="new-vss-enumerations"></a>Neue VSS-Enumerationen

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA"></span><span id="vss_backup_schema"></span>[**VSS- \_ Sicherungs \_ Schema**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd></dd> <dt>

<span id="VSS_COMPONENT_FLAGS"></span><span id="vss_component_flags"></span>[**VSS \_ - \_ Komponentenflags**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
</dt> <dd></dd> <dt>

<span id="VSS_FILE_SPEC_BACKUP_TYPE"></span><span id="vss_file_spec_backup_type"></span>[**Sicherungstyp der VSS- \_ Datei \_ Spezifikation \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)
</dt> <dd></dd> <dt>

<span id="VSS_RESTORE_TYPE"></span><span id="vss_restore_type"></span>[**VSS \_ - \_ Wiederherstellungstyp**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)
</dt> <dd></dd> </dl>

## <a name="existing-vss-enumeration-modifications"></a>Vorhandene Änderungen der VSS-Enumeration

<dl> <dt>

<span id="VSS_BACKUP_TYPE_enumeration"></span><span id="vss_backup_type_enumeration"></span><span id="VSS_BACKUP_TYPE_ENUMERATION"></span>[**VSS \_ \_Sicherungstyp**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) -Enumeration
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:
</dt> <dd>

VSS \_ BT- \_ Kopie

</dd> </dl> </dd> <dt>

<span id="VSS_RESTORE_TARGET_enumeration"></span><span id="vss_restore_target_enumeration"></span><span id="VSS_RESTORE_TARGET_ENUMERATION"></span>[**VSS \_ \_Zielenumeration wiederherstellen**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target)
</dt> <dd>

<dl> <dt>

<span id="Removed_values_"></span><span id="removed_values_"></span><span id="REMOVED_VALUES_"></span>Entfernte Werte:
</dt> <dd>

VSS \_ RT \_ neu

</dd> </dl> </dd> <dt>

<span id="VSS_RESTOREMETHOD_ENUM_enumeration"></span><span id="vss_restoremethod_enum_enumeration"></span><span id="VSS_RESTOREMETHOD_ENUM_ENUMERATION"></span>[**VSS \_ Restoremethod \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) -Enumeration
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:
</dt> <dd>

VSS- \_ RME- \_ Wiederherstellung \_ beim \_ Neustart, \_ Wenn \_ nicht \_ ersetzen kann

</dd> </dl> </dd> <dt>

<span id="VSS_SNAPSHOT_STATE_enumeration"></span><span id="vss_snapshot_state_enumeration"></span><span id="VSS_SNAPSHOT_STATE_ENUMERATION"></span>[**VSS \_ Snapshot \_ State**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state) -Enumeration
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:
</dt> <dd>

VSS \_ SS- \_ Verarbeitungs \_ postcommit

\_prefinalcommit für VSS SS- \_ Verarbeitung \_

VSS \_ SS \_ prefinalcommit

VSS \_ SS- \_ Verarbeitung von \_ postfinalcommit

</dd> </dl> </dd> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeration der [**\_ VSS- \_ volumemomentaufnahme- \_ \_ Attribute**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:
</dt> <dd>

VSS \_ Volsnap \_ attr \_ AutoRecover

</dd> <dt>

<span id="Reserved_values_now_support_"></span><span id="reserved_values_now_support_"></span><span id="RESERVED_VALUES_NOW_SUPPORT_"></span>Reservierte Werte unterstützen jetzt:
</dt> <dd>

VSS \_ Volsnap \_ attr \_ Hardware unter \_ stützt

VSS- \_ Volsnap- \_ attr \_ importiert

lokales VSS- \_ Volsnap- \_ attr \_ \_

VSS- \_ Volsnap- \_ attr \_ \_ Remote verfügbar gemacht

</dd> </dl> </dd> <dt>

<span id="VSS_WRITER_STATE_enumeration"></span><span id="vss_writer_state_enumeration"></span><span id="VSS_WRITER_STATE_ENUMERATION"></span>[**VSS \_ Writer \_ State**](/windows/desktop/api/Vss/ne-vss-vss_writer_state) -Enumeration
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:
</dt> <dd>

Fehler bei VSS \_ WS \_ \_ bei \_ BackupShutdown.

</dd> </dl> </dd> </dl>

## <a name="changes-to-vss-structures"></a>Änderungen an VSS-Strukturen

<dl> <dt>

<span id="VSS_COMPONENTINFO_structure"></span><span id="vss_componentinfo_structure"></span><span id="VSS_COMPONENTINFO_STRUCTURE"></span>[**VSS \_ ComponentInfo**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) -Struktur
</dt> <dd>

<dl> <dt>

<span id="Added_members_"></span><span id="added_members_"></span><span id="ADDED_MEMBERS_"></span>Hinzugefügte Mitglieder:
</dt> <dd>

**bselectableforrestore**

**dwcomponentflags**

**cabhängigkeiten**

</dd> </dl> </dd> </dl>

 

 



