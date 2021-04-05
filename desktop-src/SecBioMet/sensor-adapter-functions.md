---
title: Sensor Adapter Funktionen
description: Ein Sensor Adapter schließt ein biometrisches Gerät ein und stellt eine Standardschnittstelle bereit, die es dem Windows-biometrischen Dienst ermöglicht, den Sensor zu konfigurieren, Beispiele zu erfassen und den Fluss biometrischer Daten an die Verarbeitungs-Engine zu steuern.
ms.assetid: 32cf28d3-cb78-442d-81db-7827f55b0ba8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cefc5e9221a56a7766e6af6a47449db4405b369
ms.sourcegitcommit: 8a30948ba97ab969fcaa7f7ff05b853f59d8bd5c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/14/2020
ms.locfileid: "103724324"
---
# <a name="sensor-adapter-functions"></a>Sensor Adapter Funktionen

Ein Sensor Adapter schließt ein biometrisches Gerät ein und stellt eine Standardschnittstelle bereit, die es dem Windows-biometrischen Dienst ermöglicht, den Sensor zu konfigurieren, Beispiele zu erfassen und den Fluss biometrischer Daten an die Verarbeitungs-Engine zu steuern. Die folgenden Funktionen müssen vom Entwickler des Adapters implementiert werden. Sie werden vom biometrischen Windows-Dienst aufgerufen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                           | BESCHREIBUNG                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Sensoradapterakzeptcalibrationdata**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn)<br/>     | Übergibt die Kalibrierungsdaten vom Engine-Adapter an den Sensor Adapter.<br/>                                                                                            |
| [**Sensoradapteraktivierungs**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn)<br/>                               | Gibt dem Sensor Adapter die Möglichkeit, alle notwendigen Aufgaben auszuführen, um die Sensor Komponente in den Leerlauf zu versetzen.<br/>                                                |
| [**Sensoradapterattach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn)<br/>                                   | Fügt der Verarbeitungs Pipeline der biometrischen Einheit einen Sensor Adapter hinzu.<br/>                                                                                           |
| [**Sensoradaptercancel**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn)<br/>                                   | Bricht alle ausstehenden Sensor Vorgänge ab.<br/>                                                                                                                            |
| [**Sensoradapterclearcontext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn)<br/>                       | Bereitet die Verarbeitungs Pipeline der biometrischen Einheit auf einen neuen Vorgang vor.<br/>                                                                                       |
| [**Sensoradaptercontrolunit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn)<br/>                         | Führt einen Hersteller definierten Steuerungs Vorgang aus, der keine erhöhten Berechtigungen erfordert.<br/>                                                                             |
| [**Sensoradaptercontrolunitprivilegiert**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn)<br/>     | Führt einen Hersteller definierten Steuerungs Vorgang aus, der erweiterte Berechtigungen erfordert.<br/>                                                                                     |
| [**Sensoradapterdeaktivieren**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn)<br/>                           | Gibt dem Sensor Adapter die Möglichkeit, alle Arbeit auszuführen, die erforderlich ist, um die Sensor Komponente in einen Leerlaufzustand zu versetzen.<br/>                                                    |
| [**Sensoradapterdetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn)<br/>                                   | Gibt adapterspezifische Ressourcen frei, die an die Pipeline angefügt sind.<br/>                                                                                                     |
| [**Sensoradapterexportsensordata**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn)<br/>               | Ruft das zuletzt erfasste biometrische Beispiel ab, das als Standard [**\_ Struktur von winbio**](winbio-bir.md) -Struktur formatiert ist.<br/>                                        |
| [**Sensoradapterfinishcapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn)<br/>                     | Wird vom Windows-Biometrieframework aufgerufen, um auf den Abschluss eines Aufzeichnungs Vorgangs zu warten, der von der sensoradapterstartcapture-Funktion initiiert wurde.<br/>                                                                                       |
| [**Sensoradaptergetindikatorstatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)<br/>           | Ruft einen Wert ab, der angibt, ob der Sensor Indikator ein-oder ausgeschaltet ist.<br/>                                                                                       |
| [*Sensoradapternotifypowerchange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn)<br/>               | Empfängt eine Benachrichtigung über eine Änderung im Energiezustand des Computers und bereitet den Sensor Adapter entsprechend vor.<br/>                                                     |
| [**Sensoradapterpipelinecleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn)<br/>                 | Ermöglicht dem Sensor Adapter die Ausführung beliebiger Bereinigungs Vorgänge in, die Hilfe von der Engine oder den Speicher Adapter Komponenten benötigen.<br/>                                   |
| [**Sensoradapterpipelineinit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn)<br/>                       | Ermöglicht dem Sensor Adapter die Ausführung beliebiger Initialisierungen, die unvollständig bleiben und die Hilfe von der Engine oder den Speicher Adapter Komponenten benötigen.<br/> |
| [**Sensoradapterpushdatatoengine**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn)<br/>               | Macht den aktuellen Inhalt des Beispiel Puffers für den Engine-Adapter verfügbar.<br/>                                                                                  |
| [**Sensoradapterquerycalibrationformats**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn)<br/> | Bestimmt den Satz von Kalibrierungs Formaten, der vom Sensor Adapter unterstützt wird.<br/>                                                                                        |
| [**Sensoradapterqueryextendedinfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn)<br/>             | Bestimmt die Funktionen und Einschränkungen der Komponente des biometrischen Sensors.<br/>                                                                                    |
| [**Sensoradapterquerystatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)<br/>                         | Ruft Informationen zum aktuellen Status des Sensor Geräts ab.<br/>                                                                                              |
| [**Sensoradapterreset**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn)<br/>                                     | Initialisiert den Sensor erneut.<br/>                                                                                                                                         |
| [**Sensoradaptersetcalibrationformat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn)<br/>       | Benachrichtigt den Sensor Adapter, dass ein bestimmtes Kalibrierungsdaten Format vom Engine-Adapter ausgewählt wurde.<br/>                                                    |
| [**Sensoradaptersetindikatorstatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)<br/>           | Schaltet den Sensor Indikator ein oder aus.<br/>                                                                                                                           |
| [**Sensoradaptersetmode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn)<br/>                                 | Legt den Sensor Adapter Modus fest.<br/>                                                                                                                                     |
| [**Sensoradapterstartcapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn)<br/>                       | Startet eine asynchrone biometrische Erfassung.<br/>                                                                                                                         |
| [**Wbioquerysensorinterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)<br/>                         | Ruft einen Zeiger auf die Struktur der [**winbio- \_ Sensor \_ Schnittstelle**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface) für den Sensor Adapter ab.<br/>                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Plug-in-Funktionen](plug-in-functions.md)
</dt> </dl>

 

 





