---
description: Gibt das aktuelle Eingabeformat für den Decoder an.
ms.assetid: 8fddf8c3-268e-4706-9003-e4bfb03d5278
title: AVDecCommonInputFormat-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187e923be9c53cebbb55663d55ec6351be38f84c33f8c03277f587d61a4db719
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079490"
---
# <a name="avdeccommoninputformat-property"></a>AVDecCommonInputFormat (Eigenschaft)

Gibt das aktuelle Eingabeformat für den Decoder an.

Diese Eigenschaft ist schreibgeschützt.

## <a name="data-type"></a>Datentyp

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecCommonInputFormat**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein **BSTR,** der die Zeichenfolgendarstellung einer GUID enthält. Die folgenden GUIDs sind definiert.



| **GUID**                                            | BESCHREIBUNG                                    |
|-----------------------------------------------------|------------------------------------------------|
| **CODECAPI \_ GUID \_ AVDecAudioInputAAC**              | Erweiterte Audiocodierung (Advanced Audio Coding, AAC)                    |
| **CODECAPI \_ GUID \_ AVDecAudioInput ÜberdigitalPlus** | Dolby Digital Plus-Audio                       |
| **\_CODECAPI-GUID \_ AVDecAudioInputStellbarby**            | Dolby-Audio                                    |
| **CODECAPI \_ GUID \_ AVDecAudioInputDTS**              | DTS-Audio                                      |
| **\_CODECAPI-GUID \_ AVDecAudioInputHEAAC**            | High-Efficiency Advanced Audio Coding (HE-AAC) |
| **CODECAPI \_ GUID \_ AVDecAudioInputMPEG**             | MPEG-Audio                                     |
| **CODECAPI \_ GUID \_ AVDecAudioInputPCM**              | PCM-Audio                                      |
| **CODECAPI \_ GUID \_ AVDecAudioInputWMA**              | Windows Media Audio                            |
| **CODECAPI \_ GUID \_ AVDecAudioInputWMAPro**           | Windows Media Audio 9 Professional (WMA Pro)   |



 

## <a name="requirements"></a>Requirements (Anforderungen)



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

 

 




