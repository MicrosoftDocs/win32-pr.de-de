---
title: XAudio2-Strukturen
description: Dieser Abschnitt enthält Informationen zu Strukturen, die von der Microsoft XAudio2-API bereitgestellt werden.
ms.assetid: 3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59dcbdf454f282ca696a040aa7c1a3fe84c372ca4e0607c0a60f18b59d5f5e42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962589"
---
# <a name="xaudio2-structures"></a>XAudio2-Strukturen

Dieser Abschnitt enthält Informationen zu Strukturen, die von der Microsoft XAudio2-API bereitgestellt werden.



| Struktur                                                                                 | BESCHREIBUNG                                                                                                                                    |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XAUDIO2 \_ BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)                                                 | Stellt einen Audiodatenpuffer dar.<br/>                                                                                                    |
| [**XAUDIO2 \_ BUFFER \_ WMA**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer_wma)                                        | Stellt einen WMA-Audiodatenpuffer dar.<br/>                                                                                                 |
| [**\_XAUDIO2-DEBUGKONFIGURATION \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration)                      | Legt eine neue globale Debugkonfiguration für XAudio2 fest, wenn sie von der SetDebugConfiguration-Funktion verwendet wird.                                             |
| [**XAUDIO2 \_ EFFECT \_ CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain)                                    | Definiert eine Effektkette.<br/>                                                                                                            |
| [**XAUDIO2 \_ \_ EFFECT-DESKRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)                          | Definiert einen Effekt.<br/>                                                                                                                  |
| [**\_XAUDIO2-FILTERPARAMETER \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)                          | Definiert Filterparameter für eine Quellstimme.<br/>                                                                                       |
| [**\_XAUDIO2-LEISTUNGSDATEN \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_performance_data)                            | Ruft Leistungsinformationen ab.<br/>                                                                                                  |
| [**XAUDIO2 \_ SEND \_ DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor)                              | Beschreibt ein Sprachsendenziel.<br/>                                                                                                 |
| [**\_XAUDIO2-SPRACHDETAILS \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_details)                                  | Enthält Informationen zu den Erstellungsflags, Eingabekanälen und der Abtastrate einer Stimme.<br/>                                          |
| [**XAUDIO2 \_ VOICE \_ SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)                                      | Definiert einen Satz von Stimmen, um Daten von einer einzelnen Ausgabestimme zu empfangen.<br/>                                                                 |
| [**\_XAUDIO2-SPRACHZUSTAND \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_state)                                      | Gibt die aktuellen Zustands- und Cursorpositionsdaten der Stimme zurück.<br/>                                                                         |
| [**XAUDIO2FX \_ REVERB \_ I3DL2-PARAMETER \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_i3dl2_parameters)         | Beschreibt I3DL2-Parameter (Interactive 3D Audio Rendering Guidelines Level 2.0) zur Verwendung in der ReverbConvertI3DL2ToNative-Funktion.           |
| [**\_XAUDIO2FX-REVERB-PARAMETER \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters)                      | Beschreibt Parameter für die Verwendung im Hall-APO.                                                                                                |
| [**XAUDIO2FX \_ \_ VOLUMEMETER-EBENEN**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_volumemeter_levels)                    | Beschreibt Parameter für die Verwendung mit dem Volumenzähler-APO.                                                                                        |
| [**XAPO \_ \_ LOCKFORPROCESS-PUFFERPARAMETER \_**](/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters) | Definiert Pufferparameter, die konstant bleiben, während ein XAPO gesperrt ist.<br/>                                                             |
| [**\_XAPO-PROZESSPUFFERPARAMETER \_ \_**](/windows/desktop/api/xapo/ns-xapo-xapo_process_buffer_parameters)               | Definiert Pufferparameter, die sich von einem Aufruf zum nächsten ändern können.<br/>                                                                |
| [**EIGENSCHAFTEN \_ DER XAPO-REGISTRIERUNG \_**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)                    | Beschreibt allgemeine Merkmale eines XAPO.<br/>                                                                                       |
| [**FXECHO \_ INITDATA**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_initdata)                                               | Initialisierungsparameter für die Verwendung mit fxecho XAPO.<br/>                                                                             |
| [**\_FXECHO-PARAMETER**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                                           | Parameter für die Verwendung mit fxecho XAPO.<br/>                                                                                            |
| [**\_FXEQ-PARAMETER**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                                               | Parameter für die Verwendung mit fxeq XAPO.<br/>                                                                                              |
| [**FXMASTERINGLIMITER-PARAMETER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters)                   | Parameter für die Verwendung mit dem FXMasteringLimiter-XAPO.<br/>                                                                                |
| [**FXREVERB-PARAMETER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                                       | Parameter für die Verwendung mit der FXReverb-XAPO.<br/>                                                                                          |
| [**X3DAUDIO \_ CONE**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)                                                   | Gibt die Richtung für einen Einkanal-Nicht-LFE-Emitter an, indem das DSP-Verhalten in Bezug auf die Ausrichtung des Emitters skaliert wird.<br/>    |
| [**\_X3DAUDIO-ENTFERNUNGSKURVE \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve)                              | Definiert eine explizite schrittweise Kurve, die aus linearen Segmenten besteht und das DSP-Verhalten in Bezug auf die normalisierte Entfernung direkt definiert.<br/> |
| [**X3DAUDIO \_ DISTANCE \_ CURVE \_ POINT**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve_point)                 | Definiert eine DSP-Einstellung in einem bestimmten normalisierten Abstand.<br/>                                                                               |
| [**\_X3DAUDIO-DSP-EINSTELLUNGEN \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)                                  | Empfängt die Ergebnisse von einem Aufruf von X3DAudioCalculate.<br/>                                                                              |
| [**\_X3DAUDIO-EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)                                             | Definiert eine ein- oder mehrpunktige 3D-Audioquelle, die mit einer beliebigen Anzahl von Soundkanälen verwendet wird.<br/>                                    |
| [**X3DAUDIO \_ LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener)                                           | Definiert einen Punkt mit 3D-Audioempfang.<br/>                                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierverzeichnis](programming-reference.md)
</dt> </dl>

 

 




