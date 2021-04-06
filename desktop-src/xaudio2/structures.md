---
title: XAudio2-Strukturen
description: Dieser Abschnitt enthält Informationen zu Strukturen, die von der Microsoft XAudio2-API bereitgestellt werden.
ms.assetid: 3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b67e0312c5ac6b753881d895dff3972564f2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759475"
---
# <a name="xaudio2-structures"></a>XAudio2-Strukturen

Dieser Abschnitt enthält Informationen zu Strukturen, die von der Microsoft XAudio2-API bereitgestellt werden.



| Struktur                                                                                 | BESCHREIBUNG                                                                                                                                    |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)                                                 | Stellt einen audiodatenpuffer dar.<br/>                                                                                                    |
| [**XAUDIO2- \_ Puffer- \_ WMA**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer_wma)                                        | Stellt einen WMA-audiodatenpuffer dar.<br/>                                                                                                 |
| [**XAUDIO2 \_ - \_ Debugkonfiguration**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration)                      | Legt eine neue globale Debugkonfiguration für XAudio2 fest, wenn Sie von der setdebugconfiguration-Funktion verwendet wird.                                             |
| [**XAUDIO2- \_ Effekt \_ Kette**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain)                                    | Definiert eine Wirkungskette.<br/>                                                                                                            |
| [**XAUDIO2- \_ Effekt \_ Deskriptor**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)                          | Definiert einen Effekt.<br/>                                                                                                                  |
| [**XAUDIO2 \_ Filter \_ Parameter**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)                          | Definiert Filter Parameter für eine Quell Stimme.<br/>                                                                                       |
| [**\_Leistungs \_ Daten XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_performance_data)                            | Ruft Leistungsinformationen ab.<br/>                                                                                                  |
| [**XAUDIO2- \_ Sende \_ Deskriptor**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor)                              | Beschreibt ein sprach Sende Ziel.<br/>                                                                                                 |
| [**XAUDIO2- \_ sprach \_ Details**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_details)                                  | Enthält Informationen zu den erstellungsflags, den Eingabe Kanälen und der Samplingrate einer Stimme.<br/>                                          |
| [**XAUDIO2- \_ sprach \_ Sendungen**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)                                      | Definiert eine Gruppe von Stimmen, mit denen Daten von einer einzelnen Ausgabesprache empfangen werden können.<br/>                                                                 |
| [**XAUDIO2- \_ sprach \_ Zustand**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_state)                                      | Gibt die aktuellen Zustands-und Cursor Positionsdaten der Stimme zurück.<br/>                                                                         |
| [**XAUDIO2FX \_ Reverb \_ I3DL2 \_ Parameter**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_i3dl2_parameters)         | Beschreibt I3DL2 (interaktive 3D-audiorenderführungs-Richtlinien Level 2,0) Parameters für die Verwendung in der ReverbConvertI3DL2ToNative-Funktion.           |
| [**XAUDIO2FX- \_ Reverb- \_ Parameter**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters)                      | Beschreibt Parameter für die Verwendung im Reverb-APO.                                                                                                |
| [**XAUDIO2FX \_ volumemeter- \_ Ebenen**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_volumemeter_levels)                    | Beschreibt Parameter für die Verwendung mit dem Volume Meter-APO.                                                                                        |
| [**xapo \_ lockforprocess- \_ Puffer \_ Parameter**](/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters) | Definiert Puffer Parameter, die konstant bleiben, während ein xapo gesperrt ist.<br/>                                                             |
| [**xapo- \_ Prozess \_ Puffer \_ Parameter**](/windows/desktop/api/xapo/ns-xapo-xapo_process_buffer_parameters)               | Definiert Puffer Parameter, die sich möglicherweise von einem aufzurufenden aufgerufen haben.<br/>                                                                |
| [**xapo- \_ Registrierungs \_ Eigenschaften**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)                    | Beschreibt die allgemeinen Eigenschaften eines xapo.<br/>                                                                                       |
| [**fxecho \_ initdata**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_initdata)                                               | Initialisierungs Parameter für die Verwendung mit dem fxecho xapo.<br/>                                                                             |
| [**fxecho- \_ Parameter**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                                           | Parameter für die Verwendung mit dem fxecho xapo.<br/>                                                                                            |
| [**f- \_ Parameter**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                                               | Parameter für die Verwendung mit dem "f"-xapo.<br/>                                                                                              |
| [**fxmasteringlimiter- \_ Parameter**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters)                   | Parameter für die Verwendung mit dem fxmasteringlimiter xapo.<br/>                                                                                |
| [**fxreverb- \_ Parameter**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                                       | Parameter für die Verwendung mit dem fxreverb-xapo.<br/>                                                                                          |
| [**X3DAUDIO- \_ Kegel**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)                                                   | Gibt die Direktionalität für einen nicht-LFE-Emitter eines einzelnen Kanals an, indem das DSP-Verhalten in Bezug auf die Ausrichtung des Emitters skaliert wird.<br/>    |
| [**X3DAUDIO- \_ Entfernungs \_ Kurve**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve)                              | Definiert eine explizite schrittweise Kurve, die aus linearen Segmenten besteht und das DSP-Verhalten in Bezug auf die normalisierte Entfernung direkt definiert.<br/> |
| [**X3DAUDIO- \_ Entfernungs \_ Kurven \_ Punkt**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve_point)                 | Definiert eine DSP-Einstellung für eine angegebene normalisierte Entfernung.<br/>                                                                               |
| [**X3DAUDIO \_ DSP- \_ Einstellungen**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)                                  | Empfängt die Ergebnisse von einem X3DAudioCalculate-aufzurufenden.<br/>                                                                              |
| [**X3DAUDIO- \_ Emitter**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)                                             | Definiert eine einzelne oder Multipoint 3D-Audioquelle, die mit einer beliebigen Anzahl von Audiokanälen verwendet wird.<br/>                                    |
| [**X3DAUDIO- \_ Listener**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener)                                           | Definiert einen Punkt der 3D-Audioaufnahme.<br/>                                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierverzeichnis](programming-reference.md)
</dt> </dl>

 

 




