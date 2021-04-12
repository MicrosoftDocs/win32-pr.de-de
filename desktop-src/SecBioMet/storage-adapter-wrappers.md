---
title: Wrapper für Speicher Adapter
description: Funktionen, die Sie verwenden können, um Funktionen auf Ihrem Speicher Adapter aufzurufen. Diese Funktionen sind in winbio \_ Adapter. h definiert.
ms.assetid: 3e7ff098-b8f3-4745-aa75-712a392c6c78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5dfdf562546e1520ee85c5a9a0164acdff53904
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388367"
---
# <a name="storage-adapter-wrappers"></a>Wrapper für Speicher Adapter

Die folgenden Wrapper Funktionen sind in winbio \_ Adapter. h definiert. Sie können Sie verwenden, um Funktionen auf Ihrem Speicher Adapter aufzurufen.



| Funktion                                    | BESCHREIBUNG                                                                                                                                                                     |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wbiostorageaktivierungs<br/>              | Ruft die [**storageadapteraktivierungs**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>                   |
| Wbiostorageaddrecord<br/>             | Ruft die [**storageadapteraddrecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn) -Funktion auf.<br/>                                                                                       |
| Wbiostorageattach<br/>                | Ruft die [**storageadapterattach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn) -Funktion auf.<br/>                                                                                             |
| Wbiostorageclearcontext<br/>          | Ruft die [**storageadapterclearcontext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn) -Funktion auf.<br/>                                                                                 |
| Wbiostorageclosedatabase<br/>         | Ruft die [**storageadapterclosedatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn) -Funktion auf.<br/>                                                                               |
| Wbiostoragecontrolunit<br/>           | Ruft die [**storageadaptercontrolunit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn) -Funktion auf.<br/>                                                                                   |
| Wbiostoragecontrolunitprivilegiert<br/> | Ruft die [**storageadaptercontrolunitprivilegierte**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn) -Funktion auf.<br/>                                                               |
| Wbiostoragekreatedatabase<br/>        | Ruft die [**storageadapterkreatedatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn) -Funktion auf.<br/>                                                                             |
| Wbiostoragedeaktivieren<br/>            | Ruft die [**storageadapterdeaktivieren**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>               |
| Wbiostoragedeleterecord<br/>          | Ruft die [**storageadapterdeleterecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn) -Funktion auf.<br/>                                                                                 |
| Wbiostoragedetach<br/>                | Ruft die [**storageadapterdetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn) -Funktion auf.<br/>                                                                                             |
| Wbiostorageerasedatabase<br/>         | Ruft die [**storageadaptererasedatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn) -Funktion auf.<br/>                                                                               |
| Wbiostoragefirstrecord<br/>           | Ruft die [**storageadapterfirstrecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn) -Funktion auf.<br/>                                                                                   |
| Wbiostoragegetcurrentrecord<br/>      | Ruft die [**storageadaptergetcurrentrecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn) -Funktion auf.<br/>                                                                         |
| Wbiostoragegetdatabasesize<br/>       | Ruft die [**storageadaptergetdatabasesize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn) -Funktion auf.<br/>                                                                           |
| Wbiostoragegetdataformat<br/>         | Ruft die [**storageadaptergetdataformat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn) -Funktion auf.<br/>                                                                               |
| Wbiostoragegetrecordcount<br/>        | Ruft die [**storageadaptergetrecordcount**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn) -Funktion auf.<br/>                                                                             |
| Wbiostoragenextrecord<br/>            | Ruft die [**storageadapternextrecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn) -Funktion auf.<br/>                                                                                     |
| Wbiostoragenotifypowerchange<br/>     | Ruft die [*storageadapternotifypowerchange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 8 unterstützt.<br/>    |
| Wbiostorageopendatabase<br/>          | Ruft die [**storageadapteropendatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn) -Funktion auf.<br/>                                                                                 |
| Wbiostoragepipelinecleanup<br/>       | Ruft die [**storageadapterpipelinecleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>     |
| Wbiostoragepipelineinit<br/>          | Ruft die [**storageadapterpipelineinit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>           |
| Wbiostoragequerybycontent<br/>        | Ruft die [**storageadapterquerybycontent**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn) -Funktion auf.<br/>                                                                             |
| Wbiostoragequerybysubject<br/>        | Ruft die [**storageadapterquerybysubject**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn) -Funktion auf.<br/>                                                                             |
| Wbiostoragequeryextendedinfo<br/>     | Ruft die [**storageadapterqueryextendedinfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Speicher Adapter Funktionen](storage-adapter-functions.md)
</dt> <dt>

[Plug-in-Funktionen](plug-in-functions.md)
</dt> </dl>

 

 





