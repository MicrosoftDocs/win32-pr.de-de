---
title: Wrapper für Sensoradapter
description: Funktionen, die Sie verwenden können, um Funktionen auf Ihrem Sensoradapter aufzurufen. Diese Funktionen werden in Winbio \_ adapter.h definiert.
ms.assetid: 302a831c-38f7-4d32-8d9f-5ff58931224b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55a9e4ade931e10a93320d132662bb7622e62028299816eb6ad0e41fd7bff527
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683200"
---
# <a name="sensor-adapter-wrappers"></a>Wrapper für Sensoradapter

Die folgenden Wrapperfunktionen sind in Winbio \_ adapter.h definiert. Sie können sie verwenden, um Funktionen auf Ihrem Sensoradapter aufzurufen.



| Funktion                                     | Beschreibung                                                                                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioSensorAcceptCalibrationData<br/>   | Ruft die [**SensorAdapterAcceptCalibrationData-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn) auf.<br/> Diese Wrapperfunktion wird ab Windows 10 unterstützt.<br/>     |
| WbioSensorActivate<br/>                | Ruft die [**SensorAdapterActivate-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn) auf.<br/> Diese Wrapperfunktion wird ab Windows 10 unterstützt.<br/>                               |
| WbioSensorAttach<br/>                  | Ruft die [**SensorAdapterAttach-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn) auf.<br/>                                                                                                         |
| WbioSensorCancel<br/>                  | Ruft die [**SensorAdapterCancel-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn) auf.<br/>                                                                                                         |
| WbioSensorClearContext<br/>            | Ruft die [**SensorAdapterClearContext-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn) auf.<br/>                                                                                             |
| WbioSensorControlUnit<br/>             | Ruft die [**SensorAdapterControlUnit-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn) auf.<br/>                                                                                               |
| WbioSensorControlUnitPrivileged<br/>   | Ruft die [**SensorAdapterControlUnitPrivileged-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn) auf.<br/>                                                                           |
| WbioSensorDeactivate<br/>              | Ruft die [**SensorAdapterDeactivate-Funktion auf.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn)<br/> Diese Wrapperfunktion wird ab Windows 10 unterstützt.<br/>                           |
| WbioSensorDetach<br/>                  | Ruft die [**SensorAdapterDetach-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn) auf.<br/>                                                                                                         |
| WbioSensorExportSensorData<br/>        | Ruft die [**SensorAdapterExportSensorData-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn) auf.<br/>                                                                                     |
| WbioSensorFinishCapture<br/>           | Ruft die [**SensorAdapterFinishCapture-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn) auf.<br/>                                                                                           |
| WbioSensorNotifyPowerChange<br/>       | Ruft die [**SensorAdapterNotifyPowerChange-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn) auf.<br/> Diese Wrapperfunktion wird ab Windows 8 unterstützt.<br/>              |
| WbioSensorPipelineCleanup<br/>         | Ruft die [**SensorAdapterPipelineCleanup-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn) auf.<br/> Diese Wrapperfunktion wird ab Windows 10 unterstützt.<br/>                 |
| WbioSensorPipelineInit<br/>            | Ruft die [**SensorAdapterPipelineInit-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn) auf.<br/> Diese Wrapperfunktion wird ab Windows 10 unterstützt.<br/>                       |
| WbioSensorPushDataToEngine<br/>        | Ruft die [**SensorAdapterPushDataToEngine-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn) auf.<br/>                                                                                     |
| WbioSensorQueryCalibrationFormats<br/> | Ruft die [**SensorAdapterQueryCalibrationFormats-Funktion auf.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn)<br/> Diese Wrapperfunktion wird ab Windows 10 unterstützt.<br/> |
| WbioSensorQueryExtendedInfo<br/>       | Ruft die [**SensorAdapterQueryExtendedInfo-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn) auf.<br/> Diese Wrapperfunktion wird ab Windows 10 unterstützt.<br/>             |
| WbioSensorQueryStatus<br/>             | Ruft die [**SensorAdapterQueryStatus-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn) auf.<br/>                                                                                               |
| WbioSensorReset<br/>                   | Ruft die [**SensorAdapterReset-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn) auf.<br/>                                                                                                           |
| WbioSensorSetCalibrationFormat<br/>    | Ruft die [**SensorAdapterSetCalibrationFormat-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn) auf.<br/> Diese Wrapperfunktion wird ab Windows 10 unterstützt.<br/>       |
| WbioSensorSetMode<br/>                 | Ruft die [**SensorAdapterSetMode-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) auf.<br/>                                                                                                       |
| WbioSensorStartCapture<br/>            | Ruft die [**SensorAdapterStartCapture-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn) auf.<br/>                                                                                             |



 

Es gibt keine Wrapperfunktionen für die Funktionen [**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn) und [**SensorAdapterSetIndicatorStatus.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sensoradapterfunktionen](sensor-adapter-functions.md)
</dt> <dt>

[Plug-In-Funktionen](plug-in-functions.md)
</dt> </dl>

 

 





