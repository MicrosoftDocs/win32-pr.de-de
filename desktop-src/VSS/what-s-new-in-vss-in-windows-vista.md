---
description: Windows Vista
ms.assetid: 3b16744d-b9c2-4462-a409-de94d9103c39
title: Neues in VSS in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9e0780b092b2bed0235ba62377da9a4f7f0b53bded9e3f7feb5d412f5ab982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751142"
---
# <a name="whats-new-in-vss-in-windows-vista"></a>Neues in VSS in Windows Vista

Windows Vista führt die folgenden Änderungen an der Volumeschattenkopie-Dienst ein.

Beachten Sie, dass alle Änderungen für Windows Vista auch für Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) gelten.

## <a name="new-vss-interfaces"></a>Neue VSS-Schnittstellen

[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[**IVssComponentEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[**IVssCreateWriterMetadataEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[**IVssDifferentialSoftwareSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[**IVssExwriterMetadataEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a>Neue VSS-Klassen

[**CVssWriterEx**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a>Neue VSS-Enumerationen

[**VSS \_ \_ ROLLFORWARD-TYP**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a>Vorhandene VSS-Enumerationsänderungen

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ BACKUP \_ SCHEMA-Enumeration**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:
</dt> <dd>

\_AUTORITATIVE \_ WIEDERHERSTELLUNG VON VSS BS \_

VSS \_ BS \_ INDEPENDENT \_ SYSTEM \_ STATE

VSS \_ BS \_ RESTORE \_ RENAME

VSS \_ BS \_ ROLLFORWARD \_ RESTORE

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS \_ COMPONENT \_ FLAGS-Enumeration**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:
</dt> <dd>

VSS \_ CF \_ NOT \_ SYSTEM \_ STATE

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_ VSS \_ VOLUME \_ SNAPSHOT \_ ATTRIBUTES-Enumeration**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:
</dt> <dd>

VSS \_ VOLSNAP \_ ATTR \_ NO \_ AUTORECOVERY

VSS \_ VOLSNAP \_ ATTR \_ NOT \_ TRANSACTED

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>VSS-Ereignisablaufverfolgung und -protokollierung

-   Die VSS-Ablaufverfolgungsdatei kann jetzt auf jedem lokalen Volume gespeichert werden. In Versionen von Windows vor Windows Vista konnte sich die VSS-Ablaufverfolgungsdatei nicht auf einem Volume befinden, das sich im Schattenkopiesatz befand.
-   Viele Ereignisprotokolleinträge wurden umgeschrieben, um sie übersichtlicher zu machen.
-   Alle VSS-Ereignisprotokolleinträge enthalten jetzt Kontextinformationen.

## <a name="vss-error-reporting"></a>VSS-Fehlerberichterstattung

-   Beschreibungen aller VSS-Fehlercodes können jetzt durch Aufrufen der [**FormatMessage-Funktion**](/windows/win32/api/winbase/nf-winbase-formatmessage) mit dem \_ im \_ \_ *dwFlags-Parameter* angegebenen FORMAT MESSAGE FROM HMODULE-Flag abgerufen werden.
-   Die VSS-Fehlermeldungen sind in vsstrace.dll enthalten. Ein Handle für dieses Modul muss im *lpSource-Parameter* angegeben werden.

## <a name="excluding-files-from-shadow-copies"></a>Ausschließen von Dateien aus Schattenkopien

Anwendungen oder Dienste können den Registrierungsschlüssel FilesNotToSnapshot verwenden, um Dateien anzugeben, die aus neu erstellten Schattenkopien gelöscht werden sollen. Weitere Informationen finden Sie unter [Ausschließen von Dateien aus Schattenkopien.](excluding-files-from-shadow-copies.md)

## <a name="backup-and-restore-application-compatibility"></a>Sicherungs- und Wiederherstellungsanwendungskompatibilität

Entwickler von Sicherungs- und Wiederherstellungsanwendungen müssen bestimmte neue Features in Windows Vista und Windows Server 2008 kennen. Eine Prüfliste für die Anwendungskompatibilität finden Sie unter [Anwendungskompatibilität für Sicherung und Wiederherstellung.](application-compatibility-for-backup-and-restore.md)

 

 
