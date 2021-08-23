---
description: Anzahl der Bits pro Audiobeispiel in einem Audiomedientyp.
ms.assetid: d78a8c4d-377e-45eb-9cf6-2d61b34e82d6
title: MF_MT_AUDIO_BITS_PER_SAMPLE Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9697ff5ce97bc7dd9066b57f94e41ff02a599fcf14d1ea8f51c9dea69efc7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104556"
---
# <a name="mf_mt_audio_bits_per_sample-attribute"></a>MF \_ MT \_ AUDIO \_ BITS PER \_ \_ SAMPLE-Attribut

Anzahl der Bits pro Audiobeispiel in einem Audiomedientyp.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut entspricht dem **wBitsPerSample-Member** der [**WAVEFORMATEX-Struktur.**](/previous-versions/dd757713(v=vs.85))

Wenn einige Bits Auffüllung enthalten, legen Sie das [**MF MT AUDIO VALID \_ \_ \_ \_ BITS PER \_ \_ SAMPLE-Attribut**](mf-mt-audio-valid-bits-per-sample-attribute.md) fest, um die Anzahl der Bits gültiger Audiodaten in jedem Beispiel anzugeben.

Wenn das Audio 8 Bits pro Stichprobe enthält, sind die Audiobeispiele Werte ohne Vorzeichen. (Jedes Audiobeispiel hat den Bereich 0 bis 255.) Wenn das Audio 16 Bit pro Stichprobe oder höher enthält, sind die Audiobeispiele signierte Werte.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 
