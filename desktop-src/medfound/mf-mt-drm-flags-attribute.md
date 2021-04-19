---
description: Gibt an, ob für einen Video Medientyp die Erzwingung des Kopierschutzes erforderlich ist.
ms.assetid: fb12ba38-a4f4-44fe-bf31-e731c56bb145
title: MF_MT_DRM_FLAGS-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ef771cb72050b2273d822ce799092ce51e64c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364078"
---
# <a name="mf_mt_drm_flags-attribute"></a>MF \_ MT \_ DRM- \_ Flags-Attribut

Gibt an, ob für einen Video Medientyp die Erzwingung des Kopierschutzes erforderlich ist.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Member der [**mfvideodrmflags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) -Enumeration.

Dieses Attribut stellt einen Hinweis für die Anwendung bereit. Er wird nicht verwendet, um den Kopierschutz zu erzwingen oder den Kopierschutzmechanismus anzugeben.

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

[MF \_ SD- \_ geschützt](mf-sd-protected-attribute.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




