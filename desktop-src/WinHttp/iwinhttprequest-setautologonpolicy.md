---
description: Legt die aktuelle Richtlinie für die automatische Anmeldung fest.
ms.assetid: bc8e8c9c-574e-4392-b336-2c06947022ee
title: 'Iwinhttprequest:: "abtautologonpolicy"-Methode'
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
ms.openlocfilehash: cad8bd0080d10a1395a0a9d275951ff961a60bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350382"
---
# <a name="iwinhttprequestsetautologonpolicy-method"></a>Iwinhttprequest:: "abtautologonpolicy"-Methode

Die **setautologonpolicy** -Methode legt die aktuelle [Richtlinie für die automatische Anmeldung](authentication-in-winhttp.md)fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetAutoLogonPolicy(
  [in] WinHttpRequestAutoLogonPolicy AutoLogonPolicy
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Autologonpolicy* \[ in\]
</dt> <dd>

Gibt die aktuelle Richtlinie für die automatische Anmeldung an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.

## <a name="remarks"></a>Bemerkungen

Die Standard Richtlinie ist [**autologonpolicy \_ onlyifbypassproxy**](winhttprequestautologonpolicy.md).

Rufen Sie **setautologonpolicy** auf, um die automatische Anmelde Richtlinie festzulegen, bevor [**Sie Send**](iwinhttprequest-send.md) aufrufen, um die Anforderung zu senden.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispielskript wird veranschaulicht, wie die Richtlinie für die automatische Anmeldung so festgelegt wird, dass NTLM niemals verwendet oder die Authentifizierung automatisch ausgehandelt


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

[Authentifizierung in WinHTTP](authentication-in-winhttp.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




