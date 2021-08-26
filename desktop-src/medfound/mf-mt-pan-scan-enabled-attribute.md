---
description: Gibt an, ob der Schwenk-/Scanmodus aktiviert ist.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: MF_MT_PAN_SCAN_ENABLED -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1e78c38cd15f5d735d49b5689905a40d74614b46817a8621ce1dabcdc5a1b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955490"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a>MF \_ MT PAN SCAN \_ \_ \_ ENABLED-Attribut

Gibt an, ob der Schwenk-/Scanmodus aktiviert ist.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Wenn dieses Attribut **TRUE ist,** sollte nur der Schwenk-/Scanbereich des Videos angezeigt werden. Der Schwenk-/Scanbereich wird durch das [**MF \_ MT PAN \_ SCAN \_ \_ APERTURE-Attribut**](mf-mt-pan-scan-aperture-attribute.md) angegeben.

Wenn dieses Attribut FALSE **ist** oder nicht festgelegt ist, sollte die gesamte Anzeigeperperkette des Videos angezeigt werden. Die Anzeigeblende wird durch das [**MF \_ MT MINIMUM \_ DISPLAY \_ \_ APERTURE-Attribut**](mf-mt-minimum-display-aperture-attribute.md) angegeben.

Wenn Sie dieses Attribut auf **TRUE festlegen,** legen Sie auch den Wert des [**MF \_ MT PAN \_ SCAN \_ \_ APERTURE-Attributs**](mf-mt-pan-scan-aperture-attribute.md) fest.

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

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**VERERBungstyp**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> <dt>

[Bild-Seitenverhältnis](picture-aspect-ratio.md)
</dt> </dl>

 

 




