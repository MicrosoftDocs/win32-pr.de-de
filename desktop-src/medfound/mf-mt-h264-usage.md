---
description: Gibt den Verwendungsmodus für einen UVC H.264-Encoder an.
ms.assetid: 05158F47-CE01-4C99-8FFA-6BBD4F829B59
title: MF_MT_H264_USAGE Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24bbe8668cf7e6d077586d8fc7e7eaaf4ec8087ad231014499e08ec0479f07e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877243"
---
# <a name="mf_mt_h264_usage-attribute"></a>MF \_ MT \_ H264 \_ USAGE-Attribut

Gibt den Verwendungsmodus für einen UVC H.264-Encoder an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Medientypen für H.264-Streams, die über USB übertragen werden. Der Wert entspricht dem Feld **bUsage** im UVC 1.2 H.264-Test-/Commit-Steuerelement.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 




