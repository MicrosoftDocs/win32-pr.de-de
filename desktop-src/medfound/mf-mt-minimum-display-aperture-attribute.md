---
description: Definiert die Anzeige Öffnung, bei der es sich um den Bereich eines Video Rahmens handelt, der gültige Bilddaten enthält.
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: MF_MT_MINIMUM_DISPLAY_APERTURE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d13252378422081044d7f2cb21e5a31098702a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348198"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a>Das MF \_ MT- \_ Minimal Anzeige-Aperture- \_ \_ Attribut

Definiert die Anzeige Öffnung, bei der es sich um den Bereich eines Video Rahmens handelt, der gültige Bilddaten enthält.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Der Attribut Wert ist eine [**MF Video Area**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) -Struktur.

Die minimale Anzeige Öffnung ist der Bereich, der den gültigen Teil des Signals enthält. Die Pixel außerhalb der Öffnung enthalten ungültige Daten und sollten nicht angezeigt werden.

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

[Bildseiten Verhältnis](picture-aspect-ratio.md)
</dt> <dt>

[Video Medientypen](video-media-types.md)
</dt> <dt>

[**Imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**\_geometrische Monte-MT- \_ \_ Öffnung**](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[**MF- \_ MT- \_ Schwenken- \_ Überprüfung \_**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




