---
title: External.authenticate-Methode
description: Die Authenticate-Methode initiiert einen Versuch, den Benutzer zu authentifizieren.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- Authentifizierungsmethode Windows Media Player
- authenticate-Methode Windows Media Player , External-Klasse
- Externe Klasse Windows Media Player , Authentifizierungsmethode
topic_type:
- apiref
api_name:
- External.authenticate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b72c4d20cdd8232746175d966856a616bca9629657ca66c35727b8af8e21178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649550"
---
# <a name="externalauthenticate-method"></a>External.authenticate-Methode

Die **Authenticate-Methode** initiiert einen Versuch, den Benutzer zu authentifizieren.

## <a name="syntax"></a>Syntax


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AuthenticationIndex* \[ In\]
</dt> <dd>

**Number** (**long**), die den Index einer Webseite mit erfolgreichem Authentifizierungserfolg angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Bestimmte Links auf einer Ermittlungsseite verfügen über Ziele, die erst nach der Authentifizierung des Benutzers angezeigt werden sollten. Die Ermittlungsseite, Windows Media Player und das Plug-In des Onlineshops verwenden die folgenden Schritte, um den Benutzer zu authentifizieren und die Zielwebseite anzuzeigen:

1.  Das Skript auf einer Ermittlungsseite ruft die *externe auf.* **authenticate-Methode.**
2.  Windows Media Player zeigt ein Dialogfeld zum Abrufen eines Benutzernamens und Kennworts an.
3.  Windows Media Player ruft [IWMPContentPartner::Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate)auf, wodurch der Authentifizierungsversuch initiiert und sofort zurückgegeben wird.
4.  Nach Abschluss des Authentifizierungsversuchs ruft das Plug-In des Onlineshops [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)auf und übergibt wmpcnAuthResult und einen booleschen Wert, der angibt, ob der Versuch erfolgreich war.
5.  Wenn der Authentifizierungsversuch erfolgreich war, ruft Windows Media Player [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)auf und übergibt g \_ szItemInfo \_ AuthenticationSuccessURL, um die URL einer Webseite mit erfolg der Authentifizierung abzurufen. In diesem Aufruf übergibt Windows Media Player denselben Index, den die Ermittlungsseite an die *externe* übergeben hat. **authenticate-Methode.**
6.  Windows Media Player wird die Webseite zur erfolgreichen Authentifizierung angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlineshops vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**External.userLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





