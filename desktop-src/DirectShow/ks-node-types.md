---
description: Die folgenden global eindeutigen Bezeichner (GUIDs) definieren Knoten Typen für Kernel Modus-Filter. Um den Knotentyp zu suchen, Fragen Sie den Filter nach der Schnittstelle "IKsTopologyInfo" ab.
ms.assetid: 0e133ce3-8815-47d1-a5c3-577a98963912
title: KS-Knoten Typen (ksmedia. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSNODETYPE_DEV_SPECIFIC
- KSNODETYPE_VIDEO_CAMERA_TERMINAL
- KSNODETYPE_VIDEO_INPUT_MTT
- KSNODETYPE_VIDEO_INPUT_TERMINAL
- KSNODETYPE_VIDEO_OUTPUT_MTT
- KSNODETYPE_VIDEO_OUTPUT_TERMINAL
- KSNODETYPE_VIDEO_PROCESSING
- KSNODETYPE_VIDEO_SELECTOR
- KSNODETYPE_VIDEO_STREAMING
api_type:
- HeaderDef
api_location:
- Ksmedia.h
ms.openlocfilehash: eadae4fdd70fd80115ea4e8902ba1bb2aa7bf53b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357600"
---
# <a name="ks-node-types"></a>Knoten Typen von ""

Die folgenden global eindeutigen Bezeichner (GUIDs) definieren Knoten Typen für Kernel Modus-Filter. Um den Knotentyp zu suchen, Fragen Sie den Filter nach der Schnittstelle " [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) " ab.



| GUID                                                                                                                                                                                                                     | Beschreibung                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KSNODETYPE_DEV_SPECIFIC"></span><span id="ksnodetype_dev_specific"></span><dl> <dt>**ksnodetype \_ dev- \_ spezifisch**</dt> </dl>                             | Stellt eine oder mehrere gerätespezifische Verarbeitungsfunktionen dar. Der Knoten verfügt über eine Eingabe-und eine Ausgabe Verbindung.<br/> Der Knoten kann eine benutzerdefinierte COM-Schnittstelle über ein ksproxy-Plug-in verfügbar machen, wenn er vom Gerätehersteller bereitgestellt wird.<br/>                                            |
| <span id="KSNODETYPE_VIDEO_CAMERA_TERMINAL"></span><span id="ksnodetype_video_camera_terminal"></span><dl> <dt>**ksnodetype- \_ Video \_ Kamera- \_ Terminal**</dt> </dl> | Stellt Daten dar, die von einem Kamerasensor unabhängig vom USB-Bus in das Gerät verschoben werden. Der Knoten verfügt über eine einzige Ausgabe Verbindung.<br/> Der Knoten macht die [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) -Schnittstelle und die [**ICameraControl**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-icameracontrol) -Schnittstelle zum Steuern der Kamera verfügbar.<br/> |
| <span id="KSNODETYPE_VIDEO_INPUT_MTT"></span><span id="ksnodetype_video_input_mtt"></span><dl> <dt>**ksnodetype- \_ Video \_ Eingabe \_ MTT**</dt> </dl>                   | Stellt Daten dar, die von einem sequenziellen Medien Transport (z. b. einem VTR-Band) unabhängig vom USB-Bus in das Gerät verschoben werden. Der Knoten verfügt über eine einzige Ausgabe Verbindung.<br/> Der Knoten macht die [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) -Schnittstelle zum Steuern des Transportmechanismus verfügbar.<br/>   |
| <span id="KSNODETYPE_VIDEO_INPUT_TERMINAL"></span><span id="ksnodetype_video_input_terminal"></span><dl> <dt>**ksnodetype- \_ Video \_ Eingabe \_ Terminal**</dt> </dl>    | Stellt Daten dar, die unabhängig vom USB-Bus in das Gerät verschoben werden. Dieser Knoten kann z. b. einen analogen audiowagen oder S/PDIF-Jack darstellen. Der Knoten verfügt über eine einzige Ausgabe Verbindung.<br/>                                                                                                             |
| <span id="KSNODETYPE_VIDEO_OUTPUT_MTT"></span><span id="ksnodetype_video_output_mtt"></span><dl> <dt>**ksnodetype- \_ Video \_ Ausgabe \_ MTT**</dt> </dl>                | Stellt Daten dar, die vom Gerät zu einem sequenziellen Medien Transport (z. b. ein VTR-Band) unabhängig vom USB-Bus verschoben werden. Der Knoten verfügt über eine Eingabe Verbindung.<br/> Der Knoten macht die [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) -Schnittstelle zum Steuern des Transportmechanismus verfügbar.<br/>      |
| <span id="KSNODETYPE_VIDEO_OUTPUT_TERMINAL"></span><span id="ksnodetype_video_output_terminal"></span><dl> <dt>**ksnodetype- \_ Video \_ Ausgabe \_ Terminal**</dt> </dl> | Stellt Daten dar, die unabhängig vom USB-Bus vom Gerät verschoben werden. Dieser Knoten kann z. b. einen analogen audiowagen oder S/PDIF-Jack darstellen. Der Knoten verfügt über eine Eingabe Verbindung.<br/>                                                                                                              |
| <span id="KSNODETYPE_VIDEO_PROCESSING"></span><span id="ksnodetype_video_processing"></span><dl> <dt>**ksnodetype- \_ Video \_ Verarbeitung**</dt> </dl>                 | Stellt eine oder mehrere Video Verarbeitungsfunktionen dar. Der Knoten verfügt über eine Eingabe-und eine Ausgabe Verbindung.<br/> Der Knoten macht die Schnittstellen [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) und [**ivideoprocamp**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ivideoprocamp) verfügbar, um die Qualität des Videosignals anzupassen.<br/> |
| <span id="KSNODETYPE_VIDEO_SELECTOR"></span><span id="ksnodetype_video_selector"></span><dl> <dt>**ksnodetype- \_ Video \_ Auswahl**</dt> </dl>                       | Stellt einen Mechanismus zum Auswählen des Eingabe Pfads aus mindestens zwei möglichen Quellen dar. Der Knoten verfügt über zwei oder mehr Eingabe Verbindungen und eine Ausgabe Verbindung.<br/> Der Knoten macht die [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) -Schnittstelle für die Auswahl zwischen Eingaben verfügbar.<br/>                               |
| <span id="KSNODETYPE_VIDEO_STREAMING"></span><span id="ksnodetype_video_streaming"></span><dl> <dt>**ksnodetype- \_ Video \_ Streaming**</dt> </dl>                    | Stellt Daten dar, die zwischen dem Host und dem Gerät verschoben werden. Bei UVC-Geräten stellt dieser Knoten einen USB-Endpunkt dar. Eingabe Endpunkte verfügen über eine Eingabe Verbindung; Ausgabe Endpunkte verfügen über eine Ausgabe Verbindung.<br/>                                                                                         |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Ksmedia. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konstanten und GUIDs](constants-and-guids.md)
</dt> </dl>

 

 




