---
description: Legt die Stamm Sicherheits-ID für den Microsoft Media Foundation http-Byte-Stream fest.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: MFPKEY_HTTP_ByteStream_Urlmon_Security_Id-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf23e0c3d4aa5ab25590cfdb207fd50f04ecaec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361482"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a>Mfpkey \_ http \_ Bytestream- \_ URLMON- \_ Sicherheits-ID ( \_ Eigenschaft)

Legt die Stamm Sicherheits-ID für den Microsoft Media Foundation http-Byte-Stream fest.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**Caub**

VT \_ Vector \| VT \_ UI1

**Caub**



## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Eigenschaft, um den Media Foundation http-Bytestream zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

Diese Eigenschaft wird nur angewendet, wenn die Eigenschaft [mfpkey \_ http \_ Bytestream \_ enable \_ URLMON](mfpkey-http-bytestream-enable-urlmon.md) auf **Variant \_ true** festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
