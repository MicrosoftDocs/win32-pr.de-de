---
description: Ermöglicht dem Microsoft Media Foundation http-Bytestream, URL-Moniker (auch Urlmon genannt) zu verwenden.
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: MFPKEY_HTTP_ByteStream_Enable_Urlmon-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1858f34a5f719caba1a48f049b95f2031b400240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359256"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a>Mfpkey \_ http \_ Bytestream \_ enable \_ URLMON (Eigenschaft)

Ermöglicht dem Microsoft Media Foundation http-Bytestream, URL-Moniker (auch *URLMON* genannt) zu verwenden.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**Variant \_ bool**

VT \_ bool

**Boolesche Werte**



## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Eigenschaft, um den Media Foundation http-Bytestream zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

Wenn der Wert **Variant \_ true** ist, verwendet der http-Bytestream Urlmon für den HTTP-Transport. Andernfalls verwendet der Bytestream WinHTTP, wenn der Wert **Variant \_ false** ist.

Der Standardwert ist **Variant \_ true** für Windows Store-Apps und **Variant \_ false** für Windows-Desktop Anwendung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
