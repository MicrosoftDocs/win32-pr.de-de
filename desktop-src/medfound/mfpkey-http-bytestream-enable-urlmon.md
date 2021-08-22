---
description: Ermöglicht dem Microsoft Media Foundation HTTP-Bytestream die Verwendung von URL-Monikern (auch urlmon genannt).
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: MFPKEY_HTTP_ByteStream_Enable_Urlmon -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ede2b9109a7345f3a0d764f6a8fa68952686c5ca05207d01bb0a2e54cea4d32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344380"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a>MFPKEY \_ HTTP \_ ByteStream \_ Enable \_ Urlmon (Eigenschaft)

Ermöglicht dem Microsoft Media Foundation HTTP-Bytestream die Verwendung von URL-Monikern (auch *urlmon genannt).*



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>Hinweise

Verwenden Sie diese Eigenschaft, um Media Foundation HTTP-Bytestream zu konfigurieren. Übergeben Sie zum Festlegen der -Eigenschaft einen [**IPropertyStore-Zeiger**](/windows/win32/api/propsys/nn-propsys-ipropertystore) an den Quellre resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

Wenn der Wert **VARIANT \_ TRUE ist,** verwendet der HTTP-Bytestream Urlmon für den HTTP-Transport. Andernfalls verwendet der Bytestream WinHTTP, wenn der Wert **VARIANT \_ FALSE** ist.

Der Standardwert ist **VARIANT \_ TRUE für** Windows Store-Apps und VARIANT **\_ FALSE** für Windows Desktopanwendung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
