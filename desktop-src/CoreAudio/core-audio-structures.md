---
description: Kernaudiostrukturen
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: Kernaudiostrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8ea83d0de4c07c1a3d36bab169d5cb581e82cf60e84e308d04dff49af0dac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407214"
---
# <a name="core-audio-structures"></a>Kernaudiostrukturen

In diesem Abschnitt werden die Strukturen beschrieben, die von den Core Audio-APIs in Windows Vista und höher verwendet werden.



| Struktur                                                                     | Beschreibung                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AUDIO \_ VOLUME \_ NOTIFICATION \_ DATA**](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | Beschreibt eine Änderung der Lautstärkeebene oder des Veränderungszustands eines Audioendpunktgeräts.                                                                                 |
| [**DIRECTX \_ AUDIO \_ ACTIVATION \_ PARAMS**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | Gibt die Initialisierungsparameter für einen DirectSound-Stream an.                                                                                                   |
| [**KSJACK \_ DESCRIPTION**](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | Abgerufen über [**IKsJackDescription::GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); beschreibt eine Audiobuchse.                                 |
| [**KSJACK \_ DESCRIPTION2**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | Abgerufen über [**IKsJackDescription2::GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); beschreibt eine Audiobuchse. <br/>                 |
| [**KSJACK-SENKENINFORMATIONEN \_ \_**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | Abgerufen über [**IKsJackSinkInformation::GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); beschreibt eine Audiobuchsesenke.<br/> |
| [**Luid**](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | Speichert den Videoportbezeichner.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierverzeichnis](programming-reference.md)
</dt> </dl>

 

 




