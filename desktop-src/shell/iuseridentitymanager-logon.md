---
description: IUserIdentityManager::Logon wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop.
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: IUserIdentityManager::Logon-Methode (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logon
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: e5be9402dbbbf7c46528ceeab944317fa35857f9521db41b621ab246c8da86be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821130"
---
# <a name="iuseridentitymanagerlogon-method"></a>IUserIdentityManager::Logon-Methode

\[**IUserIdentityManager::Logon** wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop](fastuserswitching.md).\]

Zeigt eine Benutzeroberfläche für den Benutzer an, sodass der Benutzer eine Benutzeridentität auswählen kann. Bei Erfolg wird die Benutzeridentität angemeldet und abgerufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT Logon(
  [in]  HWND          hwndParent,
  [in]  DWORD         dwFlags,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ In\]
</dt> <dd>

Typ: **HWND**

Ein **HWND-Wert,** der ein Fenster identifiziert, das nach dem Schließen der Anmeldebenutzeroberfläche in den Vordergrund gestellt wird.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Typ: **DWORD**

Optionale Flags zum Definieren des Verhaltens der Benutzeroberfläche. Legen Sie UIL \_ FORCE \_ UI fest, um die Anzeige der Benutzeroberfläche zu erzwingen, auch wenn bereits eine Identität ausgewählt wurde.

</dd> <dt>

*ppIdentity* \[ out\]
</dt> <dd>

Typ: **[ **IUserIdentity**](iuseridentity.md)\*\***

Die Adresse des Zeigers, der die ausgewählte Benutzeridentität empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Ergebnis des Anmeldevorgangs. Wenn erfolgreich, wird S \_ OK zurückgegeben. Andernfalls wird einer der folgenden Fehlercodes zurückgegeben.



| Rückgabecode                                                                                            | Beschreibung                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**\_E-BENUTZER \_ ABGEBROCHEN**</dt> </dl>      | Der Benutzer hat den Anmeldevorgang über die Benutzeroberfläche abgebrochen.<br/>                               |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Die Benutzeridentität konnte nicht erstellt werden.<br/>                                          |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>           | Unerwarteter Fehler beim Vorgang.<br/>                                               |
| <dl> <dt>**DEAKTIVIERTE \_ E-IDENTITÄTEN \_**</dt> </dl> | Die Identitätsverwaltung ist auf dem System deaktiviert.<br/>                                   |
| <dl> <dt>**DEAKTIVIERTE \_ S-IDENTITÄTEN \_**</dt> </dl> | Die Identitätsverwaltung ist auf dem System deaktiviert.<br/>                                   |
| <dl> <dt>**E \_ IDENTITY \_ CHANGING**</dt> </dl>   | Das System wechselt derzeit die Identitäten und kann den Vorgang nicht abschließen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IUserIdentityManager::Logoff**](iuseridentitymanager-logoff.md)
</dt> <dt>

[**IUserIdentityManager::ManageIdentities**](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




