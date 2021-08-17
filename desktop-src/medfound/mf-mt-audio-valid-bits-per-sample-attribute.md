---
description: Anzahl der gültigen Bits von Audiodaten in jedem Audiobeispiel.
ms.assetid: b5b97700-c98a-4394-a184-661852add0b4
title: MF_MT_AUDIO_VALID_BITS_PER_SAMPLE -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f84fa3938e4d74473da70bd28e5ccbb1bab71441c694b670cdb8b54bead31c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973579"
---
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a>MF \_ MT AUDIO VALID BITS PER \_ \_ \_ \_ \_ SAMPLE-Attribut

Anzahl der gültigen Bits von Audiodaten in jedem Audiobeispiel.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Das **MF \_ MT AUDIO VALID BITS PER \_ \_ \_ \_ \_ SAMPLE-Attribut** wird für Audioformate verwendet, die nach jedem Audiobeispiel Auf padding enthalten. Die Gesamtgröße jedes Audiobeispiels, einschließlich der Auf padding Bits, wird im [**MF \_ MT AUDIO BITS PER \_ \_ \_ \_ SAMPLE-Attribut**](mf-mt-audio-bits-per-sample-attribute.md) angegeben.

Wenn das **MF \_ MT AUDIO VALID BITS PER \_ \_ \_ \_ \_ SAMPLE-Attribut** nicht festgelegt ist, verwenden Sie das [**MF MT AUDIO BITS \_ \_ PER \_ \_ \_ SAMPLE-Attribut,**](mf-mt-audio-bits-per-sample-attribute.md) um die Anzahl der gültigen Bits pro Stichprobe zu finden.

Wenn ein Audioformat keine Aufpaddingbits enthält, sollte dieses Attribut nicht festgelegt oder auf denselben Wert wie das [**MF \_ MT AUDIO BITS PER \_ \_ \_ \_ SAMPLE-Attribut**](mf-mt-audio-bits-per-sample-attribute.md) festgelegt werden.

Dieses Attribut entspricht dem **wValidBitsPerSample-Member** der [**WAVEFORMATEXTENSIBLE-Struktur.**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**VERERBungstyp**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 
