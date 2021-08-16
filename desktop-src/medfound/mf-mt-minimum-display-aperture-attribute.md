---
description: Definiert die Anzeigeaufblendung, die den Bereich eines Videoframes darstellt, der gültige Bilddaten enthält.
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: MF_MT_MINIMUM_DISPLAY_APERTURE Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ff6dd226492c848bd2347ccc2bac17c2dd8824467e661e83be06d590f65c0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012940"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a>MF \_ MT MINIMUM DISPLAY \_ \_ \_ APERTURE-Attribut

Definiert die Anzeigeaufblendung, die den Bereich eines Videoframes darstellt, der gültige Bilddaten enthält.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Hinweise

Der Attributwert ist eine [**MFVideoArea-Struktur.**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea)

Die minimale Anzeigeblende ist der Bereich, der den gültigen Teil des Signals enthält. Die Pixel außerhalb der Öffnung enthalten ungültige Daten und sollten nicht angezeigt werden.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> <dt>

[Bildseitenverhältnis](picture-aspect-ratio.md)
</dt> <dt>

[Videomedientypen](video-media-types.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**MF \_ MT \_ GEOMETRIC \_ APERTURE**](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




