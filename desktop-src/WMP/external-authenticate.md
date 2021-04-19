---
title: Extern. Authenticate-Methode
description: Die authentifizieren-Methode initiiert den Versuch, den Benutzer zu authentifizieren.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- Authentifizieren von Methoden Fenster Media Player
- authentifizieren-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, authentifizieren-Methode
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
ms.openlocfilehash: aa2bba0afb80c4285ad8fa8d2c20191321315d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356492"
---
# <a name="externalauthenticate-method"></a>Extern. Authenticate-Methode

Die **Authentifizieren** -Methode initiiert den Versuch, den Benutzer zu authentifizieren.

## <a name="syntax"></a>Syntax


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Authenticationindex* \[ in\]
</dt> <dd>

**Number** (**Long**), der den Index einer Webseite mit Authentifizierungs Erfolg angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Bestimmte Links auf einer Ermittlungs Seite haben Ziele, die erst angezeigt werden sollen, nachdem der Benutzer authentifiziert wurde. Die Seite Ermittlung, Windows Media Player und das Plug-in für den Online Store führen die folgenden Schritte aus, um den Benutzer zu authentifizieren und die Zielwebseite anzuzeigen:

1.  Bei einem Skript auf einer Ermittlungs Seite wird die *externe* aufgerufen. **Authentifizieren** -Methode.
2.  Windows Media Player zeigt ein Dialogfeld an, in dem Sie einen Benutzernamen und ein Kennwort erhalten.
3.  Windows Media Player ruft [iwmpcontentpartner:: Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate)auf, wodurch der Authentifizierungs Versuch initiiert und sofort zurückgegeben wird.
4.  Wenn der Authentifizierungs Versuch abgeschlossen ist, ruft das Plug-in des Online Stores [iwmpcontentpartnercallback:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)auf und übergibt dabei wmpcnauthresult und einen booleschen Wert, der angibt, ob der Versuch erfolgreich war.
5.  Wenn der Authentifizierungs Versuch erfolgreich war, ruft Windows Media Player [iwmpcontentpartner:: getiteminfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)auf und übergibt g \_ sziteminfo \_ authenticationerfolgreiches URL, um die URL einer Webseite mit Authentifizierungs Erfolg zu erhalten. In diesem-Befehl übergibt Windows Media Player denselben Index, der von der Ermittlungs Seite an den *externen* weitergegeben wurde. **Authentifizieren** -Methode.
6.  Windows Media Player zeigt die Webseite Authentifizierung-Erfolg an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Extern.-Anmelde Name**](external-attemptlogin.md)
</dt> <dt>

[**Extern. userloggedin**](external-userloggedin.md)
</dt> </dl>

 

 





