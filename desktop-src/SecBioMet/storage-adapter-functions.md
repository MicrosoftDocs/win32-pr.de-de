---
title: Storage Adapterfunktionen
description: Ein Speicheradapter verwaltet Vorlagendatenbanken.
ms.assetid: bfb0c9e5-a95e-4054-bc83-98ff682994a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7072847c6d1ca653bd9e8edad9c51b7736354b447feeafda7c465973d4c25aea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911802"
---
# <a name="storage-adapter-functions"></a>Storage Adapterfunktionen

Ein Speicheradapter verwaltet Vorlagendatenbanken. Die folgenden Funktionen müssen vom Adapterentwickler implementiert werden. Sie werden vom biometrischen Dienst Windows aufgerufen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                         | BESCHREIBUNG                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**StorageAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn)<br/>                           | Gibt dem Storage-Adapter die Möglichkeit, alle Aufgaben durchzuführen, die erforderlich sind, um die Speicherkomponente aus dem Leerlaufzustand zu bringen.<br/>         |
| [**StorageAdapterAddRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn)<br/>                         | Fügt der Datenbank eine Vorlage hinzu.<br/>                                                                                             |
| [**StorageAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn)<br/>                               | Fügt der Verarbeitungspipeline der biometrischen Einheit einen Speicheradapter hinzu.<br/>                                                     |
| [**StorageAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn)<br/>                   | Bereitet die Verarbeitungspipeline der biometrischen Einheit für einen neuen Vorgang vor.<br/>                                                  |
| [**StorageAdapterCloseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn)<br/>                 | Schließt die Datenbank, die der Pipeline zugeordnet ist, und gibt alle zugehörigen Ressourcen frei.<br/>                                            |
| [**StorageAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn)<br/>                     | Führt einen vom Anbieter definierten Steuerungsvorgang aus, für den keine erhöhten Rechte erforderlich sind.<br/>                                        |
| [**StorageAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn)<br/> | Führt einen vom Anbieter definierten Steuerungsvorgang aus, der erhöhte Rechte erfordert.<br/>                                                |
| [**StorageAdapterCreateDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn)<br/>               | Erstellt und konfiguriert eine neue Datenbank.<br/>                                                                                       |
| [**StorageAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn)<br/>                       | Gibt dem Storage-Adapter die Möglichkeit, alle Aufgaben durchzuführen, die erforderlich sind, um die Speicherkomponente in den Leerlaufzustand zu bringen.<br/>             |
| [**StorageAdapterDeleteRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn)<br/>                   | Löscht eine oder mehrere Vorlagen aus der Datenbank.<br/>                                                                             |
| [**StorageAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn)<br/>                               | Gibt adapterspezifische Ressourcen frei, die an die Pipeline angefügt sind.<br/>                                                                |
| [**StorageAdapterEraseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn)<br/>                 | Löscht die Datenbank und markiert sie zum Löschen.<br/>                                                                               |
| [**StorageAdapterFirstRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn)<br/>                     | Positioniert den ResultSet-Cursor auf dem ersten Datensatz im Satz.<br/>                                                              |
| [**StorageAdapterGetCurrentRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn)<br/>           | Ruft den Inhalt des aktuellen Datensatzes im Pipeline-Resultset ab.<br/>                                                     |
| [**StorageAdapterGetDatabaseSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn)<br/>             | Ruft die Datenbankgröße und den verfügbaren Speicherplatz ab.<br/>                                                                             |
| [**StorageAdapterGetDataFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn)<br/>                 | Ruft Format- und Versionsinformationen ab, die von der aktuellen Datenbank verwendet werden, die der Pipeline zugeordnet ist.<br/>                          |
| [**StorageAdapterGetRecordCount**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn)<br/>               | Ruft die Anzahl der Vorlagendatensätze im Pipeline-Resultset ab.<br/>                                                         |
| [**StorageAdapterNextRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn)<br/>                       | Setzt den ResultSet-Cursor um einen Datensatz nach vorn.<br/>                                                                                |
| [*StorageAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn)<br/>           | Empfängt eine Benachrichtigung über eine Änderung des Computerleistungsstatus und bereitet den Speicheradapter entsprechend vor.<br/>               |
| [**StorageAdapterOpenDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn)<br/>                   | Öffnet eine Datenbank für die Verwendung durch den Speicheradapter.<br/>                                                                             |
| [**StorageAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn)<br/>             | Gibt dem Storage-Adapter die Möglichkeit, eine Bereinigung durchzuführen, um das Schließen der Vorlagendatenbank zu vorbereiten.<br/>                |
| [**StorageAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn)<br/>                   | Gibt dem Storage-Adapter die Möglichkeit, eine initialisierung durchzuführen, die unvollständig bleibt.<br/>                                  |
| [**StorageAdapterQueryByContent**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn)<br/>               | Fragt die derzeit geöffnete Datenbank nach Vorlagen ab, die einem angegebenen Indexvektor zugeordnet sind.<br/>                          |
| [**StorageAdapterQueryBySubject**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn)<br/>               | Fragt die derzeit geöffnete Datenbank nach Vorlagen ab, die einer angegebenen Identität und einem unteren Faktor zugeordnet sind.<br/>               |
| [**StorageAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn)<br/>         | Bestimmt die Funktionen und Einschränkungen der biometrischen Speicherkomponente.<br/>                                              |
| [**WbioQueryStorageInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)<br/>                     | Ruft einen Zeiger auf die [**WINBIO \_ STORAGE \_ INTERFACE-Struktur**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface) für den Speicheradapter ab.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Plug-In-Funktionen](plug-in-functions.md)
</dt> </dl>

 

 





