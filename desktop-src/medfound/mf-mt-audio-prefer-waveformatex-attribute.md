---
description: Gibt die bevorzugte Legacyformatstruktur an, die beim Konvertieren eines Audiomedientyps verwendet werden soll.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: MF_MT_AUDIO_PREFER_WAVEFORMATEX -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23e2aeb00e2967b3f031a2aafe3a01f3846d7db077ba344a59680508bd385fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035298"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a>MF \_ MT AUDIO PREFER \_ \_ \_ WAVEFORMATEX-Attribut

Gibt die bevorzugte Legacyformatstruktur an, die beim Konvertieren eines Audiomedientyps verwendet werden soll.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Dieses Attribut stellt einen Hinweis für die [**MFCreateWaveFormatExFromMFMediaType-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) zur Unterstützung von . Wenn das Attribut **TRUE ist,** konvertiert die Funktion den Audiomedientyp nach Möglichkeit in eine [**WAVEFORMATEX-Struktur,**](/previous-versions/dd757713(v=vs.85)) anstatt ihn in eine [**WAVEFORMATEXTENSIBLE-Struktur zu**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) konvertieren.

Die [**MFInitMediaTypeFromWaveFormatEx-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) legt dieses Attribut fest. Sie können den Wert dieses Attributs überschreiben, aber das Festlegen dieses Attributs auf **TRUE** garantiert nicht, dass ein Audiomedientyp in [**WAVEFORMATEX-Form konvertiert werden**](/previous-versions/dd757713(v=vs.85)) kann.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

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

 

 
