---
title: External.attemptLogin-Methode
description: Die attemptLogin-Methode zeigt ein Dialogfeld an, damit sich der Benutzer beim Onlineshop anmelden kann.
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- attemptLogin-Windows Media Player
- attemptLogin-Methode Windows Media Player , Externe Klasse
- Externe Klasse Windows Media Player , attemptLogin-Methode
topic_type:
- apiref
api_name:
- External.attemptLogin
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f967e812ff76dd11dfd9b4ff07a542d2575548519c3a52816fadf6302a719d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649540"
---
# <a name="externalattemptlogin-method"></a>External.attemptLogin-Methode

Die **attemptLogin-Methode** zeigt ein Dialogfeld an, damit sich der Benutzer beim Onlineshop anmelden kann.

## <a name="syntax"></a>Syntax


```JScript
External.attemptLogin()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn der Anmeldeversuch zu einer Änderung des Anmeldestatus führt, löst Windows Media Player [OnLoginChange-Ereignis](external-onloginchange-event.md) aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlinespeicher vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.OnLoginChange-Ereignis**](external-onloginchange-event.md)
</dt> <dt>

[**External.userLoggedIn**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner::Login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**Verwalten der Anmeldung**](managing-login.md)
</dt> </dl>

 

 





