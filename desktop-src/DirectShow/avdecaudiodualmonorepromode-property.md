---
description: Gibt an, wie der Decoder duale Mono-Audiodaten reproduziert.
ms.assetid: 3ef1f52c-13b2-4d9f-99fe-3317846be8a0
title: AVDecAudioDualMonoReproMode-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9151ed6b996ec4ab92791221b7fb4c920913c818eac4a079ee6f40d04591a9db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917060"
---
# <a name="avdecaudiodualmonorepromode-property"></a>AVDecAudioDualMonoReproMode (Eigenschaft)

Gibt an, wie der Decoder duale Mono-Audiodaten reproduziert.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecAudioDualMonoReproMode**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eAVDecAudioDualMonoReproMode-Enumeration.**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode)

## <a name="remarks"></a>Hinweise

Diese Eigenschaften gelten nur, wenn der Eingabebitstream des Decoders duale Mono-Audiodaten enthält. Um diese Bedingung zu testen, erhalten Sie den Wert der [AVDecAudioDualMono-Eigenschaft.](avdecaudiodualmono-property.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




