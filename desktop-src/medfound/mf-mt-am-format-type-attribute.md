---
description: Enthält eine DirectShow-Format-GUID für einen Medientyp.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: MF_MT_AM_FORMAT_TYPE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a8faf88128075e5c5b51c1b5ace39329d4e1fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344569"
---
# <a name="mf_mt_am_format_type-attribute"></a>MF \_ MT \_ am \_ \_ formatType-Attribut

Enthält eine DirectShow-Format-GUID für einen Medientyp.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann festgelegt werden, wenn ein DirectShow-Medientyp in einen Media Foundation Medientyp konvertiert wird. Das-Attribut gibt den ursprünglichen DirectShow-Formattyp an. Der Wert entspricht dem Format Type-Member der [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur.

Bei einem Audioformat kann das [**MF \_ MT- \_ Benutzer \_ Daten**](mf-mt-user-data-attribute.md) Attribut den ursprünglichen Format Block enthalten, wenn der DirectShow-Formattyp nicht erkannt wurde.

Legen Sie dieses Attribut nicht für einen Medientyp fest, es sei denn, Sie wandeln eine DirectShow-Format Struktur um.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> <dt>

[Medientyp Konvertierungen](media-type-conversions.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> <dt>

[**Imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**Imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**MF-Datei (MF)**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
