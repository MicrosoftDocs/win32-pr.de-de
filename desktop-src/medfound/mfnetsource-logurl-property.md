---
description: Liste der URLs, an die die Netzwerkquelle Protokollierungsinformationen sendet.
ms.assetid: 772c5b57-273d-4289-9229-ef7a199c6473
title: MFNETSOURCE_LOGURL -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b855475e17264682ffc49a391894bb6acc6a721712b8ce6e4c01d98b1d216d48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874634"
---
# <a name="mfnetsource_logurl-property"></a>MFNETSOURCE \_ LOGURL-Eigenschaft

Liste der URLs, an die die Netzwerkquelle Protokollierungsinformationen sendet.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

Array von Breitzeichenzeichenfolgen (**CALPWSTR**)

VT \_ VECTOR \| VT \_ LPWSTR

**calpwstr**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ LOGURL** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Übergeben Sie zum Festlegen der -Eigenschaft einen **IPropertyStore-Zeiger** an den Quellre resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




