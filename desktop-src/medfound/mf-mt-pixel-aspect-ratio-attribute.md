---
description: Pixel Seitenverhältnis für einen Video Medientyp.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: MF_MT_PIXEL_ASPECT_RATIO-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c0d28ea11ba664208fcfe5fc356f1f57f2878e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526600"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a>Attribut für das MF- \_ \_ Pixel- \_ Seiten \_ Verhältnis

Pixel Seitenverhältnis für einen Video Medientyp.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Bemerkungen

Die oberen 32 Bits enthalten den Zähler des Pixel Seitenverhältnisses und die unteren 32 Bits enthalten den Nenner. Der Zähler ist die horizontale Komponente des Seitenverhältnisses. der Nenner ist die vertikale Komponente.

Um dieses Attribut festzulegen, verwenden Sie die [**mfsetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) -Funktion. Um dieses Attribut zu erhalten, verwenden Sie die [**mfgetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) -Funktion.

Das Pixel Seitenverhältnis beschreibt die Form der Pixel im angezeigten Videobild. Legen Sie dieses Attribut fest, wenn das Bild nicht eckige Pixel enthält. Damit das Bild auf einem Anzeigegerät mit quadratischen Pixeln ordnungsgemäß angezeigt werden kann, muss es mit der Umkehrung des Pixel Seitenverhältnisses des Bilds skaliert werden.

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

[Medientyp Attribute](media-type-attributes.md)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Bildseiten Verhältnis](picture-aspect-ratio.md)
</dt> </dl>

 

 




