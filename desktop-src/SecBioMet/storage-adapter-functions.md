---
title: Speicher Adapter Funktionen
description: Ein Speicher Adapter verwaltet Vorlagen Datenbanken.
ms.assetid: bfb0c9e5-a95e-4054-bc83-98ff682994a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b5b864ab37416bb215769a700bae410c9b882c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342271"
---
# <a name="storage-adapter-functions"></a>Speicher Adapter Funktionen

Ein Speicher Adapter verwaltet Vorlagen Datenbanken. Die folgenden Funktionen müssen vom Adapter Entwickler implementiert werden. Sie werden vom biometrischen Windows-Dienst aufgerufen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                         | BESCHREIBUNG                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Storageadapteraktivierungs**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn)<br/>                           | Gibt dem Speicher Adapter die Möglichkeit, alle Arbeit auszuführen, die erforderlich ist, um die Speicherkomponente in den Leerlauf zu versetzen.<br/>         |
| [**Storageadapteraddrecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn)<br/>                         | Fügt der Datenbank eine Vorlage hinzu.<br/>                                                                                             |
| [**Storageadapterattach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn)<br/>                               | Fügt der Verarbeitungs Pipeline der biometrischen Einheit einen Speicher Adapter hinzu.<br/>                                                     |
| [**Storageadapterclearcontext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn)<br/>                   | Bereitet die Verarbeitungs Pipeline der biometrischen Einheit auf einen neuen Vorgang vor.<br/>                                                  |
| [**Storageadapterclosedatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn)<br/>                 | Schließt die der Pipeline zugeordnete Datenbank und gibt alle zugehörigen Ressourcen frei.<br/>                                            |
| [**Storageadaptercontrolunit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn)<br/>                     | Führt einen Hersteller definierten Steuerungs Vorgang aus, der keine erhöhten Berechtigungen erfordert.<br/>                                        |
| [**Storageadaptercontrolunitprivilegiert**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn)<br/> | Führt einen Hersteller definierten Steuerungs Vorgang aus, der erweiterte Berechtigungen erfordert.<br/>                                                |
| [**Storageadapterkreatedatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn)<br/>               | Erstellt und konfiguriert eine neue Datenbank.<br/>                                                                                       |
| [**Storageadapterdeaktivieren**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn)<br/>                       | Gibt dem Speicher Adapter die Möglichkeit, alle Arbeit auszuführen, die erforderlich ist, um die Speicherkomponente in einen Leerlaufzustand zu versetzen.<br/>             |
| [**Storageadapterdeleterecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn)<br/>                   | Löscht eine oder mehrere Vorlagen aus der Datenbank.<br/>                                                                             |
| [**Storageadapterdetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn)<br/>                               | Gibt adapterspezifische Ressourcen frei, die an die Pipeline angefügt sind.<br/>                                                                |
| [**Storageadaptererasedatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn)<br/>                 | Löscht die Datenbank und markiert Sie zum Löschen.<br/>                                                                               |
| [**Storageadapterfirstrecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn)<br/>                     | Positioniert den resultsetcursor auf dem ersten Datensatz im Satz.<br/>                                                              |
| [**Storageadaptergetcurrentrecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn)<br/>           | Ruft den Inhalt des aktuellen Datensatzes im Pipeline-Resultset ab.<br/>                                                     |
| [**Storageadaptergetdatabasesize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn)<br/>             | Ruft die Datenbankgröße und den verfügbaren Speicherplatz ab.<br/>                                                                             |
| [**Storageadaptergetdataformat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn)<br/>                 | Ruft Format-und Versionsinformationen ab, die von der aktuellen, der Pipeline zugeordneten Datenbank verwendet werden.<br/>                          |
| [**Storageadaptergetrecordcount**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn)<br/>               | Ruft die Anzahl der Vorlagen Datensätze im Pipeline-Resultset ab.<br/>                                                         |
| [**Storageadapternextrecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn)<br/>                       | Verschiebt den resultsetcursor um einen Datensatz.<br/>                                                                                |
| [*Storageadapternotifypowerchange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn)<br/>           | Empfängt eine Benachrichtigung über eine Änderung im Energiezustand des Computers und bereitet den Speicher Adapter entsprechend vor.<br/>               |
| [**Storageadapteropendatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn)<br/>                   | Öffnet eine Datenbank, die vom Speicher Adapter verwendet werden soll.<br/>                                                                             |
| [**Storageadapterpipelinecleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn)<br/>             | Gibt dem Speicher Adapter die Möglichkeit, alle Bereinigungs Vorgänge auszuführen, um die Vorlagen Datenbank zu schließen.<br/>                |
| [**Storageadapterpipelineinit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn)<br/>                   | Ermöglicht dem Speicher Adapter die Ausführung beliebiger Initialisierungen, die unvollständig bleiben.<br/>                                  |
| [**Storageadapterquerybycontent**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn)<br/>               | Fragt die Datenbank ab, die derzeit für Vorlagen geöffnet ist, die einem angegebenen Index Vektor zugeordnet sind.<br/>                          |
| [**Storageadapterquerybysubject**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn)<br/>               | Fragt die Datenbank ab, die derzeit für Vorlagen geöffnet ist, die einer angegebenen Identität und einem untergeordneten Faktor zugeordnet sind.<br/>               |
| [**Storageadapterqueryextendedinfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn)<br/>         | Bestimmt die Funktionen und Einschränkungen der biometrischen Speicherkomponente.<br/>                                              |
| [**Wbioquerystorageinterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)<br/>                     | Ruft einen Zeiger auf die Struktur der [**winbio- \_ Speicher \_ Schnittstelle**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface) für den Speicher Adapter ab.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Plug-in-Funktionen](plug-in-functions.md)
</dt> </dl>

 

 





