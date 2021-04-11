---
description: Gibt in einem audiomedientyp die Zuweisung von Audiokanälen zu Redner Positionen an.
ms.assetid: fa5f6baa-0a21-4162-8870-38e71763aba0
title: MF_MT_AUDIO_CHANNEL_MASK-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5293f5387a2c293b97ee32db54fcfb3f3ff304d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041954"
---
# <a name="mf_mt_audio_channel_mask-attribute"></a>MF \_ MT \_ - \_ Audiokanal- \_ Attribut Maske

Gibt in einem audiomedientyp die Zuweisung von Audiokanälen zu Redner Positionen an.

## <a name="data-type"></a>Datentyp

**UINT32**

Der Wert dieses Attributs ist ein bitweises **or** der folgenden Flags, die in der Header Datei "mmreg. h" definiert sind.

<dl> <dt>

<span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**Sprecher \_ Front- \_ Links** (0x1)
</dt> <dt>

<span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**Sprecher \_ Front- \_ right** (0x2)
</dt> <dt>

<span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**Sprecher \_ Front- \_ Center** (0x4)
</dt> <dt>

<span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**Sprecher \_ Niedrige \_ Häufigkeit** (0x8)
</dt> <dt>

<span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**Sprecher \_ Zurück \_ Links** (0x10)
</dt> <dt>

<span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**Sprecher \_ Zurück \_ Rechts** (0x20)
</dt> <dt>

<span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**Sprecher \_ Vordere \_ linke \_ \_ Mitte** (0x40)
</dt> <dt>

<span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**Sprecher \_ Vorder \_ Seite \_ von \_ Mitte** (0x80)
</dt> <dt>

<span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**Sprecher \_ \_Backcenter** (0x100)
</dt> <dt>

<span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**Sprecher \_ Seite \_ Links** (0x200)
</dt> <dt>

<span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**Sprecher \_ Side \_ right** (0x400)
</dt> <dt>

<span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**Sprecher \_ Top \_ Center** (0x800)
</dt> <dt>

<span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**Sprecher \_ Obere \_ Vorder \_** Seite (0x1000)
</dt> <dt>

<span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**Sprecher \_ Top- \_ Front- \_ Center** (0x2000)
</dt> <dt>

<span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**Sprecher \_ Obere \_ Vorder \_** Seite (0x4000)
</dt> <dt>

<span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**Sprecher \_ Oben \_ \_ Links** (0X8000)
</dt> <dt>

<span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**Sprecher \_ Top- \_ Back- \_ Center** (0x10000)
</dt> <dt>

<span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**Sprecher \_ Oben \_ \_ Rechts** (0x20000)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Attribut entspricht dem **dwchannelmask** -Member der [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) -Struktur.

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

 

 
