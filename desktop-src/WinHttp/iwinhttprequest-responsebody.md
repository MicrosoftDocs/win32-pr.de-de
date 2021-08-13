---
description: Ruft den Antwortentitätstext als Array von Bytes ohne Vorzeichen ab.
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: IWinHttpRequest::ResponseBody-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseBody
- IWinHttpRequest.get_ResponseBody
- WinHttpRequest.ResponseBody
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 56eac42d41054cf7c01ff0c69ffcb82353db7182acf15765b25149560d5f7391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563228"
---
# <a name="iwinhttprequestresponsebody-property"></a>IWinHttpRequest::ResponseBody-Eigenschaft

Die **ResponseBody-Eigenschaft** ruft den Antwortentitätstext als Array von Bytes ohne Vorzeichen ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ResponseBody(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseBody = WinHttpRequest.ResponseBody
```





## <a name="property-value"></a>Eigenschaftswert

Ein **Variant-Wert,** der den Antwortentitätstext als Array von Bytes ohne Vorzeichen empfängt. Dieses Array enthält die Rohdaten, die direkt vom Server empfangen werden.

## <a name="error-codes"></a>Fehlercodes

Der Rückgabewert ist bei Erfolg **S \_ OK,** andernfalls ein Fehlerwert.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt die Antwortdaten in einem Array von Bytes ohne Vorzeichen zurück. Wenn die Antwort keinen Antworttext enthält, wird eine leere Variante zurückgegeben. Diese Eigenschaft kann nur aufgerufen werden, nachdem die [**Send-Methode**](iwinhttprequest-send.md) aufgerufen wurde.

> [!Note]  
> Weitere Informationen zur Implementierung für Windows XP und Windows 2000 finden Sie unter [Laufzeitanforderungen.](winhttp-start-page.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5.0 und Internet Explorer 5.01 oder höher auf Windows XP und Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[**ResponseStream**](iwinhttprequest-responsestream.md)
</dt> <dt>

[**Responsetext**](iwinhttprequest-responsetext.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




