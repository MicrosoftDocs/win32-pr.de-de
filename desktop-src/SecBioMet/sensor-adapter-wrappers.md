---
title: Sensor Adapter-Wrapper
description: Funktionen, die Sie verwenden können, um Funktionen auf dem Sensor Adapter aufzurufen. Diese Funktionen sind in winbio \_ Adapter. h definiert.
ms.assetid: 302a831c-38f7-4d32-8d9f-5ff58931224b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8887da38a7142c830f19a83b5950abea15791b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100754"
---
# <a name="sensor-adapter-wrappers"></a>Sensor Adapter-Wrapper

Die folgenden Wrapper Funktionen sind in winbio \_ Adapter. h definiert. Sie können Sie verwenden, um Funktionen auf dem Sensor Adapter aufzurufen.



| Funktion                                     | BESCHREIBUNG                                                                                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wbiosensorakzeptcalibrationdata<br/>   | Ruft die [**sensoradapteraccept tcalibrationdata**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>     |
| Wbiosensoraktivierungs<br/>                | Ruft die [**sensoradapteraktivierungs**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>                               |
| Wbiosensorattach<br/>                  | Ruft die [**sensoradapterattach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn) -Funktion auf.<br/>                                                                                                         |
| Wbiosensorcancel<br/>                  | Ruft die [**sensoradaptercancel**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn) -Funktion auf.<br/>                                                                                                         |
| Wbiosensorclearcontext<br/>            | Ruft die [**sensoradapterclearcontext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn) -Funktion auf.<br/>                                                                                             |
| Wbiosensorcontrolunit<br/>             | Ruft die [**sensoradaptercontrolunit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn) -Funktion auf.<br/>                                                                                               |
| Wbiosensorcontrolunitprivilegiert<br/>   | Ruft die [**sensoradaptercontrolunitprivilegierte**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn) -Funktion auf.<br/>                                                                           |
| Wbiosensordeaktivieren<br/>              | Ruft die [**sensoradapterdeaktiviert**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>                           |
| Wbiosensordetach<br/>                  | Ruft die [**sensoradapterdetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn) -Funktion auf.<br/>                                                                                                         |
| Wbiosensorexportsensordata<br/>        | Ruft die [**sensoradapterexportsensordata**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn) -Funktion auf.<br/>                                                                                     |
| Wbiosensorfinishcapture<br/>           | Ruft die [**sensoradapterfinishcapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn) -Funktion auf.<br/>                                                                                           |
| Wbiosensornotifypowerchange<br/>       | Ruft die [**sensoradapternotifypowerchange**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 8 unterstützt.<br/>              |
| Wbiosensorpipelinecleanup<br/>         | Ruft die [**sensoradapterpipelinecleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>                 |
| Wbiosensorpipelineinit<br/>            | Ruft die [**sensoradapterpipelineinit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>                       |
| Wbiosensorpushdatatoengine<br/>        | Ruft die [**sensoradapterpushdatatoengine**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn) -Funktion auf.<br/>                                                                                     |
| Wbiosensorquerycalibrationformats<br/> | Ruft die [**sensoradapterquerycalibrationformats**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/> |
| Wbiosensorqueryextendedinfo<br/>       | Ruft die [**sensoradapterqueryextendedinfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>             |
| Wbiosensorquerystatus<br/>             | Ruft die [**sensoradapterquerystatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn) -Funktion auf.<br/>                                                                                               |
| Wbiosensorreset<br/>                   | Ruft die [**sensoradapterreset**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn) -Funktion auf.<br/>                                                                                                           |
| Wbiosensorsetcalibrationformat<br/>    | Ruft die [**sensoradaptersetcalibrationformat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn) -Funktion auf.<br/> Diese Wrapper Funktion wird ab Windows 10 unterstützt.<br/>       |
| Wbiosensorsetmode<br/>                 | Ruft die [**sensoradaptersetmode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) -Funktion auf.<br/>                                                                                                       |
| Wbiosensorstartcapture<br/>            | Ruft die [**sensoradapterstartcapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn) -Funktion auf.<br/>                                                                                             |



 

Es sind keine Wrapper Funktionen für die Funktionen [**sensoradaptergetder orstatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn) und [**sensoradaptersetindikatorstatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn) vorhanden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sensor Adapter Funktionen](sensor-adapter-functions.md)
</dt> <dt>

[Plug-in-Funktionen](plug-in-functions.md)
</dt> </dl>

 

 





