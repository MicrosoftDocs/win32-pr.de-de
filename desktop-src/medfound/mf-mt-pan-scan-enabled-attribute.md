---
description: Gibt an, ob der Pan/Scan-Modus aktiviert ist.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: MF_MT_PAN_SCAN_ENABLED-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b347c898ce827ff37796a9698e843f6321db8a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528754"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a>Das MF \_ MT \_ Pan Scan- \_ \_ aktiviertes Attribut

Gibt an, ob der Pan/Scan-Modus aktiviert ist.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut den Wert **true** hat, sollte nur der Pan/Scan-Bereich des Videos angezeigt werden. Der Pan/Scan-Bereich wird durch das [**MF \_ MT \_ Pan \_ Scan \_ Aperture**](mf-mt-pan-scan-aperture-attribute.md) -Attribut angegeben.

Wenn dieses Attribut **false** ist oder nicht festgelegt ist, sollte die gesamte Anzeige Öffnung des Videos angezeigt werden. Die Anzeige Öffnung wird durch das [**MF \_ MT- \_ minimale \_ Display \_ Aperture**](mf-mt-minimum-display-aperture-attribute.md) -Attribut angegeben.

Wenn Sie dieses Attribut auf " **true**" festlegen, legen Sie auch den Wert des [**MF \_ MT \_ Pan \_ Scan \_ Aperture**](mf-mt-pan-scan-aperture-attribute.md) -Attributs fest.

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
</dt> <dt>

[Bildseiten Verhältnis](picture-aspect-ratio.md)
</dt> </dl>

 

 




