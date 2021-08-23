---
description: 'AVDecAudioDualMono-Eigenschaft: Gibt an, ob 2-Kanal-Audio als Stereo oder Dual Mono codiert ist.'
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: AVDecAudioDualMono-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a26bd6685cb9c9f326babbc01120019c93760fd7e1f9bf33f2a540d488300ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873390"
---
# <a name="avdecaudiodualmono-property"></a>AVDecAudioDualMono-Eigenschaft

Gibt an, ob 2-Kanal-Audio als Stereo oder Dual Mono codiert wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecAudioDualMono**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eAVDecAudioDualMono-Enumeration.**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gilt nur, wenn der Eingabebitstream des Decoders zweikanalige Audiodaten enthält. Ein Zweikanal-Audiostream kann als Stereo oder als duales Mono codiert werden. Wenn die Audiodatei dual mono ist, können Sie die [**AVDecAudioDualMonoReproMode-Eigenschaft**](avdecaudiodualmonorepromode-property.md) festlegen, um zu konfigurieren, wie der Decoder die Audiodaten reproduziert.

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

 

 




