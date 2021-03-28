---
description: 'Iuseridentitymanager:: manageidentities wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.'
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: 'Iuseridentitymanager:: manageidentities-Methode (Msident. h)'
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
ms.openlocfilehash: b5b782a56324faf19dd1527d2cd363d26f0e337c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342438"
---
# <a name="iuseridentitymanagermanageidentities-method"></a>Iuseridentitymanager:: manageidentities-Methode

\[**Iuseridentitymanager:: manageidentities** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

Zeigt dem Benutzer eine Benutzeroberfläche an und ermöglicht dem Benutzer die Verwaltung von Benutzer Identitäten.

## <a name="syntax"></a>Syntax


```C++
HRESULT ManageIdentities(
  [in] HWND  hwndParent,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Typ: **HWND**

Ein **HWND** -Wert, der ein Fenster identifiziert, das nach dem verwerfen der Benutzeroberfläche in den Vordergrund gestellt wird.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Typ: **DWORD**

Optionale Flags, um zu definieren, wie sich die Benutzeroberfläche verhält. Legen Sie auf uimi \_ \_ neue \_ Identität erstellen fest, um den Benutzer zur Erstellung einer neuen Identität aufzufordern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Das Ergebnis des Verwaltungs Vorgangs. Bei erfolgreicher Ausführung wird S OK zurückgegeben \_ . Andernfalls wird einer der folgenden Fehlercodes zurückgegeben.



| Rückgabecode                                                                                            | Beschreibung                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**E- \_ Identitäten \_ deaktiviert**</dt> </dl> | Die Identitätsverwaltung ist im System deaktiviert.<br/> |
| <dl> <dt>**E- \_ Benutzer \_ abgebrochen**</dt> </dl>      | Der Benutzer hat das Dialogfeld abgebrochen.<br/>                  |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Iuseridentitymanager**](iuseridentitymanager.md)
</dt> <dt>

[**Iuseridentitymanager:: LOGON**](iuseridentitymanager-logon.md)
</dt> <dt>

[**Iuseridentitymanager:: abmelden**](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 




