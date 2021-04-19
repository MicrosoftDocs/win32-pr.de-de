---
description: Block Ausrichtung (in Byte) für einen audiomedientyp. Die Block Ausrichtung ist die minimale atomarische Einheit von Daten für das Audioformat.
ms.assetid: 7d304826-ad81-4243-a675-2f55b668b348
title: MF_MT_AUDIO_BLOCK_ALIGNMENT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21efb14cbb89d1773fe9bc3b5ade8d0a50555a1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356243"
---
# <a name="mf_mt_audio_block_alignment-attribute"></a>Das MF \_ MT \_ - \_ Audioblock- \_ Ausrichtungs Attribut

Block Ausrichtung (in Byte) für einen audiomedientyp. Die Block Ausrichtung ist die minimale atomarische Einheit von Daten für das Audioformat.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Bei PCM-Audioformaten ist die Block Ausrichtung gleich der Anzahl der Audiokanäle multipliziert mit der Anzahl der Bytes pro audiostich Probe.

Dieses Attribut entspricht dem **nBlockAlign** -Member der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur.

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

 

 
