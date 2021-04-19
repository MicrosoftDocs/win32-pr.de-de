---
description: Definiert die schwenken-/Scan-Aperture. Dies ist der 4&\# 215; 3 Bereich von Video, der im Pan/Scan-Modus angezeigt werden soll.
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: MF_MT_PAN_SCAN_APERTURE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a798ba96315126daab94ba92e8791bfeac77db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348238"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a>Das MF \_ MT \_ Pan-Scan-Aperture- \_ \_ Attribut

Definiert die schwenken-/Scan-Aperture. Dies ist der 4 × 3-Bereich des Videos, der im Pan/Scan-Modus angezeigt werden soll.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Der Attribut Wert ist eine [**MF Video Area**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) -Struktur.

Dieses Attribut wird verwendet, um ein Grafik Video zu einem 4:3-Seitenverhältnis zu schneiden. Die Pan/Scan-Öffnung wird nur im Pan/Scan-Modus verwendet, der aktiviert wird, indem das [**MF \_ MT \_ Pan \_ Scan \_ aktivierte**](mf-mt-pan-scan-enabled-attribute.md) Attribut auf " **true**" festgelegt wird.

Wenn der Pan/Scan-Modus nicht aktiviert ist, verwenden Sie die Anzeige Öffnung, die durch das Attribut " [**MF \_ MT \_ minimal \_ Display \_ Aperture**](mf-mt-minimum-display-aperture-attribute.md) " angegeben wird.

Wenn dieses Attribut nicht festgelegt ist, wird angenommen, dass es sich bei der Pan/Scan-Öffnung um den gesamten Videorahmen handelt.

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

[**minimale Anzahl von MF- \_ MT- \_ \_ anzeigen \_**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**MF- \_ MT- \_ Schwenken- \_ Scan \_ aktiviert**](mf-mt-pan-scan-enabled-attribute.md)
</dt> </dl>

 

 




