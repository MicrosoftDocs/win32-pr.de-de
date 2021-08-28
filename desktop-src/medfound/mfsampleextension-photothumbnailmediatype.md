---
description: Enthält den FORMATSMediaType, der den Bildformattyp beschreibt, der im MFSampleExtension \_ PhotoThumbnail-Attribut enthalten ist.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: MFSampleExtension_PhotoThumbnailMediaType Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77496340d598c7caf1064df0d3fc7e1ae7f112309bf6fbba6a66f3d5516e3828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713600"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a>MFSampleExtension \_ PhotoThumbnailMediaType-Attribut

Enthält den [**FORMATSMediaType,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) der den Bildformattyp beschreibt, der im [MFSampleExtension \_ PhotoThumbnail-Attribut](mfsampleextension-photothumbnail.md) enthalten ist.

## <a name="data-type"></a>Datentyp

**IUnknown,** gespeichert als **"WFMediaType"**

## <a name="remarks"></a>Hinweise

Wenn das [MFSampleExtension \_ PhotoThumbnail-Attribut](mfsampleextension-photothumbnail.md) im Fotobeispiel vorhanden ist, ist MFSampleExtension \_ PhotoThumbnailMediaType erforderlich und muss mindestens [MF MT MAJOR \_ \_ \_ TYPE,](mf-mt-major-type-attribute.md) [MF MT \_ \_ SUBTYPE](mf-mt-subtype-attribute.md) und [MF MT FRAME \_ \_ \_ SIZE](mf-mt-frame-size-attribute.md) enthalten, die die Miniaturansicht beschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 \|Desktop-Apps UWP-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




