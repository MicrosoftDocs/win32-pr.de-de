---
description: Gibt das Codierungsschema an.
ms.assetid: a26951d6-67fb-43fb-849f-331416e9d7c2
title: AVEncCodecType-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3727ff8cc2a59208d63874de173e3e44e89e3e6f2ebc37201218f9656aa09cd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084610"
---
# <a name="avenccodectype-property"></a>AVEncCodecType-Eigenschaft

Gibt das Codierungsschema an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCodecType**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein **BSTR,** der die Zeichenfolgendarstellung einer GUID enthält. Die folgenden GUIDs sind definiert.



| GUID                                      | Beschreibung                                        |
|-------------------------------------------|----------------------------------------------------|
| CODECAPI \_ GUID \_ AVEncGuibyDigitalConsumer | Dolby Digital Consumer-Audio                       |
| CODECAPI \_ GUID \_ AVEncGuibyDigitalPlus     | Dolby Digital Plus-Audio                           |
| CODECAPI \_ GUID \_ AVEncGuibyDigitalPro      | Dolby Digital Pro Audio                            |
| CODECAPI \_ GUID \_ AVEncDTS                  | DTS-Audio                                          |
| CODECAPI \_ GUID \_ AVEncDTSHD                | DTS-HD-Audio                                       |
| CODECAPI \_ GUID \_ AVEncDV                   | DV-Video                                           |
| CODECAPI \_ GUID \_ AVEncH264Video            | H.264-Video                                        |
| CODECAPI \_ GUID \_ AVEncMLP                  | MlP-Audio (Lossless Packing, Verlustloses Packen) von Meridian              |
| CODECAPI \_ GUID \_ AVEncMPEG1Audio           | MPEG-1-Audio                                       |
| CODECAPI \_ GUID \_ AVEncMPEG1Video           | MPEG-1-Video                                       |
| CODECAPI \_ GUID \_ AVEncMPEG2Audio           | MPEG-2-Audio                                       |
| CODECAPI \_ GUID \_ AVEncMPEG2Video           | MPEG-2-Video                                       |
| CODECAPI \_ GUID \_ AVEncPCM                  | PCM-Audio                                          |
| CODECAPI \_ GUID \_ AVEncSDDS                 | Dvd Dynamic Digital Sound (SDDS) audio (Dynamic Digital Sound, SDDS)-Audio            |
| CODECAPI \_ GUID \_ AVEncWMALossless          | Windows Medienaudio 9 Verlustfreie Audiodaten               |
| CODECAPI \_ GUID \_ AVEncWMAPro               | Windows Audio von Media Audio 9 Professional (WMA Pro) |
| CODECAPI \_ GUID \_ AVEncWMAVoice             | Windows Medienaudio 9– Sprachaudio                  |
| CODECAPI \_ GUID \_ AVEncWMV                  | Windows Medienvideo                                |
| CODECAPI \_ GUID \_ AVEndMPEG4Video           | MPEG-4-Video                                       |



 

## <a name="remarks"></a>Hinweise

Anwendungen können diese Eigenschaft festlegen, um anzugeben, welches Codierungsschema verwendet werden soll. Codecs können diese Eigenschaft auch als Funktion zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




