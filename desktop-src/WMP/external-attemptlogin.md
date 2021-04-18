---
title: Extern.-Anmelde Methode
description: Mit der Methode "Methode" wird ein Dialogfeld angezeigt, in dem der Benutzer versuchen kann, sich beim Online Shop anzumelden.
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- Media Player der Methode "Methode"
- Methode "-Anmeldung", Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, Methode "Methode anmelden"
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
ms.openlocfilehash: 86958c241f2399efbe342371b8cd4cfd376ff628
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357688"
---
# <a name="externalattemptlogin-method"></a>Extern.-Anmelde Methode

Mit **der Methode "** Methode" wird ein Dialogfeld angezeigt, in dem der Benutzer versuchen kann, sich beim Online Shop anzumelden.

## <a name="syntax"></a>Syntax


```JScript
External.attemptLogin()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der Anmeldeversuch zu einer Änderung des Anmeldestatus führt, löst Windows Media Player das [onloginchange](external-onloginchange-event.md) -Ereignis aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Externes. onloginchange-Ereignis**](external-onloginchange-event.md)
</dt> <dt>

[**Extern. userloggedin**](external-userloggedin.md)
</dt> <dt>

[**Iwmpcontentpartner:: Login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**Verwalten der Anmeldung**](managing-login.md)
</dt> </dl>

 

 





