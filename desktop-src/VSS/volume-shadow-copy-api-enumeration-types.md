---
description: Die folgenden Enumerationen werden in der Volumeschattenkopie-API definiert.
ms.assetid: f2f09791-b17e-4f54-9d29-83a4189bffc1
title: Volumeschattenkopie-API-Enumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ade0af4637e9c057c9743dfaf0778e86b3d81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353084"
---
# <a name="volume-shadow-copy-api-enumerations"></a>Volumeschattenkopie-API-Enumerationen

Die folgenden Enumerationen werden in der Volumeschattenkopie-API definiert.



| Name                                                                           | BESCHREIBUNG                                                                                                                                                        |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**alternativer VSS- \_ \_ Schreiber \_ Status**](/windows/desktop/api/VsWriter/ne-vswriter-vss_alternate_writer_state)            | Definiert den Satz gültiger Zustände, mit denen angegeben wird, ob ein Writer über einen zugeordneten alternativen Writer verfügt.                                                              |
| [**VSS- \_ Anwendungs \_ Ebene**](/windows/desktop/api/Vss/ne-vss-vss_application_level)                       | Definiert den Satz gültiger Anwendungsebenen.                                                                                                                       |
| [**VSS- \_ Sicherungs \_ Schema**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)                               | Definiert den Satz von Sicherungs Schemas – Vorgänge, an denen ein Writer teilnehmen kann.                                                                                          |
| [**VSS \_ - \_ Sicherungstyp**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)                                   | Definiert den Satz von Sicherungs Typen.                                                                                                                                   |
| [**VSS \_ - \_ Komponentenflags**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)                           | Gibt die Unterstützung für die automatische Wiederherstellung an.                                                                                                                               |
| [**VSS \_ - \_ Komponententyp**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)                             | Definiert den Satz von Komponenten Typen.                                                                                                                                |
| [**Status der VSS- \_ Datei \_ Wiederherstellung \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_file_restore_status)                  | Definiert den Satz von Statusangaben für einen Datei Wiederherstellungs Vorgang.                                                                                                           |
| [**Sicherungstyp der VSS- \_ Datei \_ Spezifikation \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)             | Definiert den Satz von Sicherungs Vorgängen, die von Writer unterstützt werden.                                                                                                         |
| [**\_VSS- \_ Hardware \_ Optionen**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)                      | Definiert LUN-Flags für die Schattenkopie.                                                                                                                                     |
| [**VSS- \_ Mgmt- \_ \_ Objekttyp**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_mgmt_object_type)                        | Diskriminant für die [**VSS- \_ Mgmt- \_ Objekt \_ Union**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001) -Union innerhalb der [**VSS- \_ Mgmt- \_ Objekt- \_ Prop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) -Struktur. |
| [**VSS \_ - \_ Objekttyp**](/windows/desktop/api/Vss/ne-vss-vss_object_type)                                   | Dient zum Identifizieren eines Objekts als Schattenkopiesatz, Schatten Kopie oder Anbieter.                                                                                         |
| [**VSS- \_ Schutz \_ Fehler**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)                         | Definiert den Satz von Fehlern beim Schutz vor Schatten Kopien.                                                                                                                  |
| [**VSS- \_ Schutz \_ Ebene**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)                         | Definiert die Menge der Volumeschattenkopie-Schutz Ebenen.                                                                                                           |
| [**VSS- \_ Anbieter \_ Funktionen**](/windows/desktop/api/vss/ne-vss-vss_provider_capabilities)              | Für die zukünftige Verwendung reserviert.                                                                                                                                           |
| [**VSS \_ - \_ Anbietertyp**](/windows/desktop/api/Vss/ne-vss-vss_provider_type)                               | Definiert den Satz von Anbieter Typen.                                                                                                                                 |
| [**VSS- \_ Wiederherstellungs \_ Optionen**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)                         | Wird von einem Anforderer verwendet, um anzugeben, wie ein Vorgang zur erneuten Synchronisierung ausgeführt werden soll.                                                                               |
| [**VSS- \_ Wiederherstellungs \_ Ziel**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target)                             | Definiert den Satz von Wiederherstellungs Zielen.                                                                                                                                |
| [**VSS \_ - \_ Wiederherstellungstyp**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)                                 | Definiert den Satz von Wiederherstellungs Vorgängen, der ausgeführt werden soll.                                                                                                              |
| [**VSS \_ restoremethod-Aufzählung \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)                     | Definiert den Satz von Standardmethoden für die Dateiwiederherstellung für einen Writer.                                                                                                      |
| [**VSS- \_ Rollforward- \_ Typ**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)                         | Wird von einem Anforderer verwendet, um den Typ des Roll Forward-Vorgangs anzugeben, der ausgeführt werden soll.                                                                         |
| [**Kompatibilität von VSS- \_ Momentaufnahmen \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_compatibility)             | Definiert den Satz von volumesteuerungs-oder Datei-e/a-Vorgängen, die für ein Volume deaktiviert werden können, das als Schatten kopiert wurde.                                            |
| [**\_VSS- \_ Momentaufnahme \_ Kontext**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)                      | Gibt an, wie eine Schatten Kopie erstellt, abgefragt oder gelöscht werden soll und welcher Grad an Writer beteiligt ist.                                                            |
| [**VSS- \_ Momentaufnahme \_ Status**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state)                             | Definiert den Satz von Zuständen eines schattenkopievorgangs.                                                                                                              |
| [**VSS \_ - \_ Quelltyp**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)                                   | Definiert den Satz von Datentypen, die ein Writer verwalten kann.                                                                                                         |
| [**VSS- \_ Abonnement \_ Maske**](/windows/desktop/api/VsWriter/ne-vswriter-vss_subscribe_mask)                             | Definiert den Satz von Ereignissen, der von einem Writer empfangen werden kann.                                                                                                               |
| [**VSS \_ - \_ Verwendungstyp**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type)                                     | Gibt an, wie das Host System die von einem Writer verwalteten Daten verwendet.                                                                                                   |
| [**\_VSS \_ - \_ volumesnapshotattribute \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) | Definiert den Satz von Attributen einer Schatten Kopie.                                                                                                                    |
| [**VSS \_ Writer- \_ Status**](/windows/desktop/api/Vss/ne-vss-vss_writer_state)                                 | Definiert den Satz von Zuständen des Writers.                                                                                                                           |
| [**VSS- \_ Write-Restore-Aufzählung \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)                     | Definiert den Satz von Bedingungen, unter denen ein Writer Ereignisse behandelt, die während eines Wiederherstellungs Vorgangs generiert werden.                                                        |



 

 

 



