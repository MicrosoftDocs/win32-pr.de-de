---
title: Storage Adapter-Wrapper
description: Funktionen, mit denen Sie Funktionen auf Ihrem Speicheradapter aufrufen können. Diese Funktionen werden in Winbio \_ adapter.h definiert.
ms.assetid: 3e7ff098-b8f3-4745-aa75-712a392c6c78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6308dda71cd279ae07e0849c0760526f116de6295bb0555f530f31a0033a5851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911603"
---
# <a name="storage-adapter-wrappers"></a>Storage Adapter-Wrapper

Die folgenden Wrapperfunktionen sind in Winbio \_ adapter.h definiert. Sie können sie zum Aufrufen von Funktionen auf Ihrem Speicheradapter verwenden.



| Funktion                                    | BESCHREIBUNG                                                                                                                                                                     |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioStorageActivate<br/>              | Ruft die [**StorageAdapterActivate-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn) auf.<br/> Diese Wrapperfunktion wird ab Windows 10.<br/>                   |
| WbioStorageAddRecord<br/>             | Ruft die [**StorageAdapterAddRecord-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn) auf.<br/>                                                                                       |
| WbioStorageAttach<br/>                | Ruft die [**StorageAdapterAttach-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn) auf.<br/>                                                                                             |
| WbioStorageClearContext<br/>          | Ruft die [**StorageAdapterClearContext-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn) auf.<br/>                                                                                 |
| WbioStorageCloseDatabase<br/>         | Ruft die [**StorageAdapterCloseDatabase-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn) auf.<br/>                                                                               |
| WbioStorageControlUnit<br/>           | Ruft die [**StorageAdapterControlUnit-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn) auf.<br/>                                                                                   |
| WbioStorageControlUnitPrivileged<br/> | Ruft die [**StorageAdapterControlUnitPrivileged-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn) auf.<br/>                                                               |
| WbioStorageCreateDatabase<br/>        | Ruft die [**StorageAdapterCreateDatabase-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn) auf.<br/>                                                                             |
| WbioStorageDeactivate<br/>            | Ruft die [**StorageAdapterDeactivate-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn) auf.<br/> Diese Wrapperfunktion wird ab Windows 10.<br/>               |
| WbioStorageDeleteRecord<br/>          | Ruft die [**StorageAdapterDeleteRecord-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn) auf.<br/>                                                                                 |
| WbioStorageDetach<br/>                | Ruft die [**StorageAdapterDetach-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn) auf.<br/>                                                                                             |
| WbioStorageEraseDatabase<br/>         | Ruft die [**StorageAdapterEraseDatabase-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn) auf.<br/>                                                                               |
| WbioStorageFirstRecord<br/>           | Ruft die [**StorageAdapterFirstRecord-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn) auf.<br/>                                                                                   |
| WbioStorageGetCurrentRecord<br/>      | Ruft die [**StorageAdapterGetCurrentRecord-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn) auf.<br/>                                                                         |
| WbioStorageGetDatabaseSize<br/>       | Ruft die [**StorageAdapterGetDatabaseSize-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn) auf.<br/>                                                                           |
| WbioStorageGetDataFormat<br/>         | Ruft die [**StorageAdapterGetDataFormat-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn) auf.<br/>                                                                               |
| WbioStorageGetRecordCount<br/>        | Ruft die [**StorageAdapterGetRecordCount-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn) auf.<br/>                                                                             |
| WbioStorageNextRecord<br/>            | Ruft die [**StorageAdapterNextRecord-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn) auf.<br/>                                                                                     |
| WbioStorageNotifyPowerChange<br/>     | Ruft die [*StorageAdapterNotifyPowerChange-Funktion*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn) auf.<br/> Diese Wrapperfunktion wird ab Windows 8.<br/>    |
| WbioStorageOpenDatabase<br/>          | Ruft die [**StorageAdapterOpenDatabase-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn) auf.<br/>                                                                                 |
| WbioStoragePipelineCleanup<br/>       | Ruft die [**StorageAdapterPipelineCleanup-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn) auf.<br/> Diese Wrapperfunktion wird ab Windows 10.<br/>     |
| WbioStoragePipelineInit<br/>          | Ruft die [**StorageAdapterPipelineInit-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn) auf.<br/> Diese Wrapperfunktion wird ab Windows 10.<br/>           |
| WbioStorageQueryByContent<br/>        | Ruft die [**StorageAdapterQueryByContent-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn) auf.<br/>                                                                             |
| WbioStorageQueryBySubject<br/>        | Ruft die [**StorageAdapterQueryBySubject-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn) auf.<br/>                                                                             |
| WbioStorageQueryExtendedInfo<br/>     | Ruft die [**StorageAdapterQueryExtendedInfo-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn) auf.<br/> Diese Wrapperfunktion wird ab Windows 10.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Storage Adapterfunktionen](storage-adapter-functions.md)
</dt> <dt>

[Plug-In-Funktionen](plug-in-functions.md)
</dt> </dl>

 

 





