---
description: Anzahl gültiger Bits von Audiodaten in jedem Audiobeispiel.
ms.assetid: b5b97700-c98a-4394-a184-661852add0b4
title: MF_MT_AUDIO_VALID_BITS_PER_SAMPLE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4e5efb41bf3b79d4feded2872b601eea43723a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349919"
---
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a>Zulässige "MF \_ \_ -MT-Audioinhalte" \_ \_ \_ pro \_ Beispiel Attribut

Anzahl gültiger Bits von Audiodaten in jedem Audiobeispiel.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Für Audioformate, die nach jedem Audiosample Auffüll Zeichen enthalten, wird das für die audioformatierung **\_ \_ \_ gültigen \_ Bits \_ pro \_ Beispiel** Attribut verwendet. Die Gesamtgröße der einzelnen Audiobeispiele einschließlich Auffüll Bits ist im [**MF \_ MT \_ - \_ audiobits \_ pro \_ Sample-**](mf-mt-audio-bits-per-sample-attribute.md) Attribut angegeben.

Wenn das für das **MF \_ \_ -MT-Paket \_ gültige \_ Bits \_ pro \_ Sample-** Attribut nicht festgelegt ist, verwenden Sie das [**MF \_ MT \_ - \_ audiobits \_ pro \_ Sample-**](mf-mt-audio-bits-per-sample-attribute.md) Attribut, um die Anzahl gültiger Bits pro Stichprobe zu ermitteln.

Wenn ein Audioformat keine Auffüll Bits enthält, sollte dieses Attribut nicht festgelegt werden, oder es sollte auf denselben Wert festgelegt werden wie das [**MF \_ MT \_ - \_ audiobits \_ pro \_ Sample-**](mf-mt-audio-bits-per-sample-attribute.md) Attribut.

Dieses Attribut entspricht dem **wvalidbitspersample** -Member der [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) -Struktur.

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

 

 
