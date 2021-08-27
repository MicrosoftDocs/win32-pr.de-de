---
description: Legt den Stammsicherheitsbezeichner für den Microsoft Media Foundation HTTP-Bytestream fest.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: MFPKEY_HTTP_ByteStream_Urlmon_Security_Id-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d64b07dc7d419624bfe300b890b58554394a5cd3e8363ddcbc4d5be91d9e4b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738007"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a>MFPKEY- \_ \_ HTTP-ByteStream-URLmon-Sicherheits-ID-Eigenschaft \_ \_ \_

Legt den Stammsicherheitsbezeichner für den Microsoft Media Foundation HTTP-Bytestream fest.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**CAUB**

VT \_ VECTOR \| VT \_ UI1

**caub**



## <a name="remarks"></a>Hinweise

Verwenden Sie diese Eigenschaft, um den Media Foundation HTTP-Bytestream zu konfigurieren. Um die Eigenschaft festzulegen, übergeben Sie einen [**IPropertyStore-Zeiger**](/windows/win32/api/propsys/nn-propsys-ipropertystore) an den Quell resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

Diese Eigenschaft gilt nur, wenn die [MFPKEY \_ HTTP \_ ByteStream \_ Enable \_ Urlmon-Eigenschaft](mfpkey-http-bytestream-enable-urlmon.md) auf **VARIANT \_ TRUE** festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
