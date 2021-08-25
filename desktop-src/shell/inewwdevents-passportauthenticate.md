---
description: Ermöglicht es serverseitigen Seiten, die in einem Assistenten gehostet werden, zu überprüfen, ob der Benutzer über eine Microsoft-Konto.
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: NewWDEvents.PassportAuthenticate-Methode (Shldisp.h)
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
ms.openlocfilehash: f462053281efd97b75422c55ce23829688d18ac153ecb92c7544eafb8f356b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942400"
---
# <a name="newwdeventspassportauthenticate-method"></a>NewWDEvents.PassportAuthenticate-Methode

Ermöglicht es serverseitigen Seiten, die in einem Assistenten gehostet werden, zu überprüfen, ob der Benutzer über eine Microsoft-Konto.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrSignInUrl* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine Zeichenfolge, die die URL einer Webseite enthält, die an die Microsoft-Konto-Benutzeroberfläche umleiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **Boolesch**

Wird auf **TRUE festgelegt,** wenn die Authentifizierung erfolgreich ist, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Diese Methode kann auch dann aufgerufen werden, wenn ein Benutzer bereits bei einem Benutzer angemeldet Microsoft-Konto. In diesem Fall gibt die -Methode **TRUE zurück,** ohne die Microsoft-Konto der Benutzeroberfläche anzuzeigen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 6.0 oder höher)</dt> </dl> |



 

 
