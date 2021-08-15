---
description: Gibt den MIME-Typ eines Bytestreams an.
ms.assetid: bcf86ece-2673-4ed8-98fd-cd0e2154b4a8
title: MF_BYTESTREAM_CONTENT_TYPE Attribut (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901f3d9d2b46e503bcf8f66127eb94383710a7c1055c04fccb97f6d935d463b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974009"
---
# <a name="mf_bytestream_content_type-attribute"></a>MF \_ BYTESTREAM \_ CONTENT \_ TYPE-Attribut

Gibt den MIME-Typ eines Bytestreams an.

## <a name="data-type"></a>Datentyp

Breitzeichenfolge

## <a name="remarks"></a>Hinweise

Um den Attributwert abzurufen, fragen Sie das Bytestreamobjekt für die [**SCHNITTSTELLE "ATTRIBUTESAttributes"**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) ab.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

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

 

 




