---
description: IUserIdentityManager::ManageIdentities wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop.
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: IUserIdentityManager::ManageIdentities-Methode (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.ManageIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: a816ee16e128b992b18be274d814fe3369e1a59c0204201a9c6bd4a6cbc23857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859238"
---
# <a name="iuseridentitymanagermanageidentities-method"></a>IUserIdentityManager::ManageIdentities-Methode

\[**IUserIdentityManager::ManageIdentities** wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop](fastuserswitching.md).\]

Zeigt dem Benutzer eine Benutzeroberfläche an, die es dem Benutzer ermöglicht, Benutzeridentitäten zu verwalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT ManageIdentities(
  [in] HWND  hwndParent,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ In\]
</dt> <dd>

Typ: **HWND**

Ein **HWND-Wert,** der ein Fenster identifiziert, das in den Vordergrund gestellt wird, nachdem die Benutzeroberfläche verworfen wurde.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Typ: **DWORD**

Optionale Flags, um das Verhalten der Benutzeroberfläche zu definieren. Legen Sie auf UIMI \_ CREATE \_ NEW IDENTITY \_ fest, um den Benutzer zum Erstellen einer neuen Identität aufzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Das Ergebnis des Verwaltungsvorgang. Wenn der Fehler erfolgreich ist, wird S \_ OK zurückgegeben. Andernfalls wird einer der folgenden Fehlercodes zurückgegeben.



| Rückgabecode                                                                                            | Beschreibung                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_E-IDENTITÄTEN \_ DEAKTIVIERT**</dt> </dl> | Die Identitätsverwaltung ist auf dem System deaktiviert.<br/> |
| <dl> <dt>**E \_ USER \_ CANCELLED**</dt> </dl>      | Der Benutzer hat das Dialogfeld abgebrochen.<br/>                  |



 

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

[**IUserIdentityManager::Logon**](iuseridentitymanager-logon.md)
</dt> <dt>

[**IUserIdentityManager::Logoff**](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 




