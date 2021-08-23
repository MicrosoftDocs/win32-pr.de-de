---
description: Gibt an, ob die Audiostreams in einer Präsentation eine variable Bitrate aufweisen.
ms.assetid: 2bd7eee1-5a93-4bde-8b58-80b6395a094e
title: MF_PD_AUDIO_ISVARIABLEBITRATE-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb5c8c15c12bcd867342fb11f5e753c196f9954aea0393b2a461e1804f411339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664190"
---
# <a name="mf_pd_audio_isvariablebitrate-attribute"></a>MF \_ PD \_ AUDIO \_ ISVARIABLEBITRATE-Attribut

Gibt an, ob die Audiostreams in einer Präsentation eine variable Bitrate aufweisen.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für

[**PRESENTPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Hinweise

Dies ist ein optionales Attribut für Präsentationsdeskriptoren. Wenn das Attribut **TRUE** (ungleich 0) ist, enthält die Darstellung mindestens einen VBR-Audiostream (Variable Bit-Rate). Wenn das Attribut **FALSE** ist, weisen alle Audiostreams eine konstante Bitrate auf.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Darstellungsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




