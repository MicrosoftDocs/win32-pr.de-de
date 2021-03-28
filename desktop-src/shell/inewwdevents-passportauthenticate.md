---
description: Aktiviert serverseitige Seiten, die in einem Assistenten gehostet werden, um zu überprüfen, ob der Benutzer über eine Microsoft-Konto authentifiziert wurde.
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: Newwdevents. passportauthenticate-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewWDEvents.PassportAuthenticate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 48e6cfbcbf525784fe33520702bbd9c05226f353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760513"
---
# <a name="newwdeventspassportauthenticate-method"></a>Newwdevents. passportauthenticate-Methode

Aktiviert serverseitige Seiten, die in einem Assistenten gehostet werden, um zu überprüfen, ob der Benutzer über eine Microsoft-Konto authentifiziert wurde.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrausigninurl* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine Zeichenfolge, die die URL einer Webseite enthält, die zur Microsoft-Konto Log on UI umgeleitet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **Boolean**

Auf **true** festgelegt, wenn die Authentifizierung erfolgreich ist, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Diese Methode kann auch aufgerufen werden, wenn ein Benutzer bereits bei einem Microsoft-Konto angemeldet ist. In diesem Fall gibt die Methode **true** zurück, ohne die Microsoft-Konto Log on UI anzuzeigen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 6,0 oder höher)</dt> </dl> |



 

 
