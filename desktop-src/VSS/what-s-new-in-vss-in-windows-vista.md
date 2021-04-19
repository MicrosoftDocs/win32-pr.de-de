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
# <a name="whats-new-in-vss-in-windows-vista"></a>Neues in VSS in Windows Vista

In Windows Vista werden die folgenden Änderungen am Volumeschattenkopie-Dienst eingeführt.

Beachten Sie, dass alle Änderungen für Windows Vista auch für Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) gelten.

## <a name="new-vss-interfaces"></a>Neue VSS-Schnittstellen

[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[**Ivsscomponstex**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[**IVssCreateWriterMetadataEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[**IVssDifferentialSoftwareSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[**IVssExamineWriterMetadataEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a>Neue VSS-Klassen

[**Cvssbeschreiterex**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a>Neue VSS-Enumerationen

[**VSS- \_ Rollforward- \_ Typ**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a>Vorhandene Änderungen der VSS-Enumeration

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ Sicherungs \_ Schema**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) -Enumeration
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:
</dt> <dd>

\_ \_ autorisierende \_ Wiederherstellung in VSS

\_ \_ \_ System \_ Status von VSS-SB (unabhängig)

Umbenennen von VSS- \_ \_ \_ Benennungen

VSS- \_ SB- \_ Roll Forward- \_ Wiederherstellung

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS \_ \_Komponentenflags**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags) -Enumeration
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:
</dt> <dd>

VSS \_ CF \_ nicht \_ System \_ Status

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeration der [**\_ VSS- \_ volumemomentaufnahme- \_ \_ Attribute**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:
</dt> <dd>

VSS \_ Volsnap \_ attr \_ No \_ AutoRecovery

VSS- \_ Volsnap- \_ attr \_ nicht \_ transaktiv

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>VSS-Ereignis Ablauf Verfolgung und Protokollierung

-   Die VSS-Ablauf Verfolgungs Datei kann sich jetzt auf einem beliebigen lokalen Volume befinden. In Windows-Versionen vor Windows Vista konnte die VSS-Ablauf Verfolgungs Datei nicht auf einem Volume gefunden werden, das sich im Schattenkopiesatz befand.
-   Viele Ereignisprotokoll Einträge wurden neu formuliert, um sie übersichtlicher zu machen.
-   Alle VSS-Ereignisprotokoll Einträge enthalten nun Kontextinformationen.

## <a name="vss-error-reporting"></a>VSS-Fehlerberichterstattung

-   Beschreibungen aller VSS-Fehlercodes können jetzt durch Aufrufen der [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ \_ \_ im *dwFlags* -Parameter angegebenen Flag "Format Message from HMODULE" abgerufen werden.
-   Die VSS-Fehlercode Meldungen sind in vsstrace.dll enthalten. Ein Handle für dieses Modul muss im *lpSource* -Parameter angegeben werden.

## <a name="excluding-files-from-shadow-copies"></a>Ausschließen von Dateien aus Schatten Kopien

Anwendungen oder Dienste können den Registrierungsschlüssel filesnottosnapshot verwenden, um Dateien anzugeben, die aus neu erstellten Schatten Kopien gelöscht werden sollen. Weitere Informationen finden Sie unter [Ausschließen von Dateien aus Schatten Kopien](excluding-files-from-shadow-copies.md).

## <a name="backup-and-restore-application-compatibility"></a>Sichern und Wiederherstellen der Anwendungs Kompatibilität

Entwickler von Sicherungs-und Wiederherstellungs Anwendungen müssen bestimmte neue Features in Windows Vista und Windows Server 2008 kennen. Eine Checkliste zur Anwendungs Kompatibilität finden Sie unter [Anwendungs Kompatibilität für die Sicherung und Wiederherstellung](application-compatibility-for-backup-and-restore.md).

 

 
