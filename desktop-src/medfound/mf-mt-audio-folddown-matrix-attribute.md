---
description: Gibt an, wie ein Audiodecoder Multichannel-Audiodaten in Stereoausgabe umwandeln soll. Dieser Prozess wird auch als "fold-down" bezeichnet.
ms.assetid: 6dfe2b97-1ebc-4954-b478-85b3bbba89e3
title: MF_MT_AUDIO_FOLDDOWN_MATRIX-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bb8aa00835ab31f6c05eaa9a1d0e5d9d126b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347054"
---
# <a name="mf_mt_audio_folddown_matrix-attribute"></a>Attribut "MF \_ MT \_ - \_ audiofolddown- \_ Matrix"

Gibt an, wie ein Audiodecoder Multichannel-Audiodaten in Stereoausgabe umwandeln soll. Dieser Prozess wird auch als " *Fold-Down*" bezeichnet.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für audiomedientypen.

Der Wert dieses Attributs ist eine [**mffolddown- \_ Matrix**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) Struktur.

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

[**Imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




