---
description: Gibt die ursprüngliche URL für einen Bytestream an.
ms.assetid: 31d7de71-5bbb-4c29-8ce0-df3684c56916
title: MF_BYTESTREAM_ORIGIN_NAME Attribut (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc485beeaf2b3fb80b7dc231dedf4082b848e003d0128c0cf4c73e8c2c5cc3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941060"
---
# <a name="mf_bytestream_origin_name-attribute"></a>MF \_ BYTESTREAM \_ ORIGIN \_ NAME-Attribut

Gibt die ursprüngliche URL für einen Bytestream an.

## <a name="data-type"></a>Datentyp

Breitzeichenfolge

## <a name="remarks"></a>Hinweise

Dateibasierte Bytestreams können dieses Attribut unterstützen. Der Attributwert wird festgelegt, wenn der Bytestream erstellt wird. Um den Attributwert abzurufen, fragen Sie das Bytestreamobjekt für die [**SCHNITTSTELLE "ATTRIBUTESAttributes"**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) ab.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Bytestreamattribute](byte-stream-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**ATTRIBUTEAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**GIGABYTEByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




