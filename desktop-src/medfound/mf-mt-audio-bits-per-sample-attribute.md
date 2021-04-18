---
description: Anzahl von Bits pro audiostich Probe in einem audiomedientyp.
ms.assetid: d78a8c4d-377e-45eb-9cf6-2d61b34e82d6
title: MF_MT_AUDIO_BITS_PER_SAMPLE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 896e77c937269b63208cb4bff73482a8df8596aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357451"
---
# <a name="mf_mt_audio_bits_per_sample-attribute"></a>MF \_ \_ -MT- \_ audiobits \_ pro Sample- \_ Attribut

Anzahl von Bits pro audiostich Probe in einem audiomedientyp.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut entspricht dem **wbitspersample** -Member der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur.

Wenn einige Bits Auffüll Zeichen enthalten, legen Sie die für die [**MF \_ \_ -MT-Audiodatei \_ gültigen \_ Bits \_ pro \_ Sample-**](mf-mt-audio-valid-bits-per-sample-attribute.md) Attribut fest, um die Anzahl der Bits gültiger Audiodaten in jedem Beispiel anzugeben.

Wenn die Audiodatei 8 Bits pro Stichprobe enthält, sind die Audiobeispiele nicht signierte Werte. (Jedes Audiobeispiel hat den Bereich 0 – 255.) Wenn die Audiodatei 16 Bits pro Stichprobe oder höher enthält, sind die Audiobeispiele signierte Werte.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 
