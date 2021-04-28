---
description: 'AVDecAudioDualMono-Eigenschaft: Gibt an, ob 2-Kanal-Audio als Stereo oder duales Mono codiert wird.'
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: AVDecAudioDualMono-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc84e19d41840b358e3e79576152dbc8527e2bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096568"
---
# <a name="avdecaudiodualmono-property"></a>AVDecAudioDualMono (Eigenschaft)

Gibt an, ob 2-Kanal-Audio als Stereo oder Dual Mono codiert wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecAudioDualMono**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eAVDecAudioDualMono-Enumeration.**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gilt nur, wenn der Eingabebitstream des Decoders Zweikanalaudiodaten enthält. Ein Zweikanal-Audiostream kann als Stereo oder duales Mono codiert werden. Wenn die Audiodaten dual mono sind, können Sie die [**AVDecAudioDualMonoReproMode-Eigenschaft**](avdecaudiodualmonorepromode-property.md) festlegen, um zu konfigurieren, wie der Decoder die Audiodaten reproduziert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | UWP-Apps für Windows 2000 \[ \| Professional-Desktop-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




