---
description: Gibt den Quantisierungsparameter (QP) an, der zum Codieren eines Videobeispiels verwendet wurde.
ms.assetid: F7C4FEFC-FEE7-4614-BC90-4F9D5D878F49
title: MFSampleExtension_VideoEncodeQP -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f86253b29dfa93b3699d5175b5c5ef198b4ab24e862901572caafcc55fd62d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777020"
---
# <a name="mfsampleextension_videoencodeqp-attribute"></a>MFSampleExtension \_ VideoEncodeQP-Attribut

Gibt den Quantisierungsparameter (QP) an, der zum Codieren eines Videobeispiels verwendet wurde.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT64 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT64 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)

## <a name="applies-to"></a>Gilt für:

[**DURCHSCHN.Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Hinweise

Der [**H.264 Video Encoder legt**](h-264-video-encoder.md) dieses Attribut für die von ihm generierten Ausgabebeispiele fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**H.264 Video Encoder**](h-264-video-encoder.md)
</dt> <dt>

[Beispielattribute](sample-attributes.md)
</dt> <dt>

[Medienbeispiele](media-samples.md)
</dt> </dl>

 

 




