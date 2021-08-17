---
description: Gibt die maximale Audiobitrate für die Mediensenke der Digital Living Network Alliance (DLNA) an.
ms.assetid: d0ae573a-7ce3-49e8-9609-f72d067f1ce1
title: MF_MP2DLNA_AUDIO_BIT_RATE Attribut (Mfmp2dlna.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed622a2f826e061dc4b909eec09490974fe83a7ac850cd0fcdfcede0abd578b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104766"
---
# <a name="mf_mp2dlna_audio_bit_rate-attribute"></a>MF \_ MP2DLNA \_ AUDIO BIT \_ \_ RATE-Attribut

Gibt die maximale Audiobitrate für die Mediensenke der Digital Living Network Alliance (DLNA) an.

## <a name="data-type"></a>Datentyp

**UINT32**

Der Wert ist die maximale Zielbitrate für den codierten Audiostream in Bits pro Sekunde. Der Wert muss eine der Bitraten sein, die für MPEG-2 Layer 2-Audio für DLNA zulässig sind. Der Standardwert ist 192000 (192 KBit/s).

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Um dieses Attribut für die DLNA-Mediensenke festzulegen, fragen Sie die Mediensenke nach der [**SCHNITTSTELLE "ATTRIBUTESAttributes"**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) ab. Legen Sie das Attribut fest, bevor das Streaming beginnt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmp2dlna.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




