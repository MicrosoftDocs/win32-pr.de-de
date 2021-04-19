---
description: Enthält mögliche Einstellungen für die Richtlinie für die automatische Anmeldung.
ms.assetid: dad4f6a7-8e84-4f4f-b962-4189e3dc01f7
title: Winhttprequestautologonpolicy-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestAutoLogonPolicy
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: dab3dc14dd194e36b9b4d1225f77161005b9d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345726"
---
# <a name="winhttprequestautologonpolicy-enumeration"></a>Winhttprequestautologonpolicy-Enumeration

Die **winhttprequestautologonpolicy** -Enumeration enthält mögliche Einstellungen für die [Richtlinie für die automatische Anmeldung](authentication-in-winhttp.md).

## <a name="syntax"></a>Syntax


```C++
typedef enum WinHttpRequestAutoLogonPolicy { 
  AutoLogonPolicy_Always             = 0,
  AutoLogonPolicy_OnlyIfBypassProxy  = 1,
  AutoLogonPolicy_Never              = 2
} WinHttpRequestAutoLogonPolicy;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**Autologonpolicy \_ immer**
</dt> <dd>

Eine authentifizierte Anmeldung, bei der die Standard Anmelde Informationen verwendet werden, wird für alle Anforderungen ausgeführt.

</dd> <dt>

<span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**Autologonpolicy \_ onlyifbypassproxy**
</dt> <dd>

Eine authentifizierte Anmeldung, bei der die Standard Anmelde Informationen verwendet werden, wird nur für Anforderungen im lokalen Intranet ausgeführt. Das lokale Intranet gilt als beliebiger Server in der Proxy Umgehungs Liste in der aktuellen Proxykonfiguration.

</dd> <dt>

<span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**Autologonpolicy \_ nie**
</dt> <dd>

Die Authentifizierung wird nicht automatisch verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um die Richtlinie für die automatische Anmeldung festzulegen, nennen Sie die [**setautologonpolicy**](iwinhttprequest-setautologonpolicy.md) -Methode, und geben Sie eine der vorangehenden Konstanten an.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Startseite.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




