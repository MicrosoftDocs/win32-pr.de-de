---
description: Ruft den Entitäts Text der Antwort als Array nicht signierter Bytes ab.
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: 'Iwinhttprequest:: responenbody-Eigenschaft'
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
ms.openlocfilehash: 5a608f2744ad2880ecf7c4862b03821afcef9630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351539"
---
# <a name="iwinhttprequestresponsebody-property"></a>Iwinhttprequest:: responenbody-Eigenschaft

Die Response **Body** -Eigenschaft ruft den Text der Antwort Entität als Array nicht signierter Bytes ab.

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

Ein **Variant** -Wert, der den Entitäts Text der Antwort als Array nicht signierter Bytes empfängt. Dieses Array enthält die Rohdaten, die direkt vom Server empfangen werden.

## <a name="error-codes"></a>Fehlercodes

Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt die Antwortdaten in einem Array nicht signierter Bytes zurück. Wenn die Antwort keinen Antworttext enthält, wird eine leere Variante zurückgegeben. Diese Eigenschaft kann nur aufgerufen werden, nachdem die [**Send**](iwinhttprequest-send.md) -Methode aufgerufen wurde.

> [!Note]  
> Weitere Informationen zur Implementierung für Windows XP und Windows 2000 finden Sie unter [Lauf Zeitanforderungen](winhttp-start-page.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwinhttprequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[**ResponseStream**](iwinhttprequest-responsestream.md)
</dt> <dt>

[**Response Text**](iwinhttprequest-responsetext.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




