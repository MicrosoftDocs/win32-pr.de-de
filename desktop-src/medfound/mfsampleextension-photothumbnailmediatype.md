---
description: Enthält den imemediatype, der den Bild Formattyp beschreibt, der im "MF SampleExtension photominiatur"-Attribut enthalten ist \_ .
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: MFSampleExtension_PhotoThumbnailMediaType-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0e415fb0d3b062b4a5064006d3873cd42ea593
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366552"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a>MF SampleExtension- \_ photothumbnailmediatype-Attribut

Enthält den [**imemediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , der den Bild Formattyp beschreibt, der im " [MF SampleExtension \_ photominiatur](mfsampleextension-photothumbnail.md) "-Attribut enthalten ist.

## <a name="data-type"></a>Datentyp

" **IUnknown** " wurde als " **IMF MediaType** " gespeichert

## <a name="remarks"></a>Bemerkungen

Wenn das Attribut " [mfsampleextension \_ photominiatur](mfsampleextension-photothumbnail.md) " im Photo Sample vorhanden ist, ist mfsampleextension " \_ photothumbnailmediatype" erforderlich und muss mindestens einen MF [MT- \_ \_ \_ Haupttyp](mf-mt-major-type-attribute.md), den [MF \_ MT- \_ Untertyp](mf-mt-subtype-attribute.md) und die [MF-MT- \_ \_ Frame \_ Größe](mf-mt-frame-size-attribute.md) enthalten, die die Miniaturansicht beschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MF SampleExtension- \_ Fotoansicht](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




