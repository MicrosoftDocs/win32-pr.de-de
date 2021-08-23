---
description: Enthält eine DirectShow-Format-GUID für einen Medientyp.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: MF_MT_AM_FORMAT_TYPE-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eff59e148f7532cc07e47acf033de91b5eaeb8969f0c39376850738fd54e758e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973629"
---
# <a name="mf_mt_am_format_type-attribute"></a>MF \_ MT AM FORMAT \_ \_ \_ TYPE-Attribut

Enthält eine DirectShow-Format-GUID für einen Medientyp.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Hinweise

Dieses Attribut kann festgelegt werden, wenn ein DirectShow-Medientyp in einen Media Foundation Medientyp konvertiert wird. Das Attribut gibt den ursprünglichen DirectShow-Formattyp an. Der Wert entspricht dem Formattypmember der [**AM \_ MEDIA \_ TYPE-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

Bei einem Audioformat kann das [**MF \_ MT USER \_ \_ DATA-Attribut**](mf-mt-user-data-attribute.md) den ursprünglichen Formatblock enthalten, wenn der DirectShow-Formattyp nicht erkannt wurde.

Legen Sie dieses Attribut nur für einen Medientyp fest, wenn Sie eine DirectShow-Formatstruktur konvertieren.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> <dt>

[Medientypkonvertierungen](media-type-conversions.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> <dt>

[**SPRECHATTRIBUTE::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**ATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**MFCreateMediaTypeFromRepresentation**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
