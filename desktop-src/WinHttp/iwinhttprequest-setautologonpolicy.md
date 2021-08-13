---
description: Legt die aktuelle Richtlinie für die automatische Anmeldung fest.
ms.assetid: bc8e8c9c-574e-4392-b336-2c06947022ee
title: IWinHttpRequest::SetAutoLogonPolicy-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetAutoLogonPolicy
- WinHttpRequest.SetAutoLogonPolicy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: b6375d5c5b6c9b6c8acebcdd05a2ad778bb37e75c067a44100a5c67a92876248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562886"
---
# <a name="iwinhttprequestsetautologonpolicy-method"></a>IWinHttpRequest::SetAutoLogonPolicy-Methode

Die **SetAutoLogonPolicy-Methode** legt die aktuelle [Richtlinie für die automatische Anmeldung fest.](authentication-in-winhttp.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetAutoLogonPolicy(
  [in] WinHttpRequestAutoLogonPolicy AutoLogonPolicy
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AutoLogonPolicy* \[ In\]
</dt> <dd>

Gibt die aktuelle Richtlinie für die automatische Anmeldung an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist **S \_ OK bei** Erfolg oder andernfalls ein Fehlerwert.

## <a name="remarks"></a>Hinweise

Die Standardrichtlinie ist [**AutoLogonPolicy \_ OnlyIfBypassProxy.**](winhttprequestautologonpolicy.md)

Rufen **Sie SetAutoLogonPolicy auf,** um die Richtlinie für die automatische Anmeldung vor dem Aufruf [**von Send**](iwinhttprequest-send.md) zum Senden der Anforderung zu festlegen.

> [!Note]  
> Informationen Windows XP und Windows 2000 finden Sie im Abschnitt Laufzeitanforderungen der [WinHTTP-Startseite.](winhttp-start-page.md)

 

## <a name="examples"></a>Beispiele

Das folgende Skriptbeispiel zeigt, wie Sie die Richtlinie für die automatische Anmeldung so festlegen, dass die NTLM- oder Negotiate-Authentifizierung nie automatisch verwendet wird.


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Do not automatically send user credentials.
HttpReq.SetAutoLogonPolicy(2);

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5.0 und Internet Explorer 5.01 oder höher unter Windows XP und Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Authentifizierung in WinHTTP](authentication-in-winhttp.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




