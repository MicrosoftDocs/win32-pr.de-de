---
description: Pixel-Seitenverhältnis für einen Videomedientyp.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: MF_MT_PIXEL_ASPECT_RATIO -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230e14e07a8011f89d16b095728bc80cbe19faa16ef9427156868f93c2ccb412
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060490"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a>MF \_ MT PIXEL ASPECT \_ \_ \_ RATIO-Attribut

Pixel-Seitenverhältnis für einen Videomedientyp.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Hinweise

Die oberen 32 Bits enthalten den Zähler des Pixel-Seitenverhältnisses, und die unteren 32 Bits enthalten den Nenner. Der Zähler ist die horizontale Komponente des Seitenverhältnisses. der Nenner ist die vertikale Komponente.

Verwenden Sie zum Festlegen dieses Attributs die [**MFSetAttributeRatio-Funktion.**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) Um dieses Attribut zu erhalten, verwenden Sie die [**MFGetAttributeRatio-Funktion.**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio)

Das Pixel-Seitenverhältnis beschreibt die Form der Pixel im angezeigten Videobild. Legen Sie dieses Attribut fest, wenn das Bild über nicht quadratische Pixel verfügt. Um auf einem Anzeigegerät mit quadratischen Pixeln ordnungsgemäß angezeigt zu werden, muss das Bild um die Umkehrung des Pixel-Seitenverhältnisses des Bilds skaliert werden.

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

[Medientypattribute](media-type-attributes.md)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Bild-Seitenverhältnis](picture-aspect-ratio.md)
</dt> </dl>

 

 




