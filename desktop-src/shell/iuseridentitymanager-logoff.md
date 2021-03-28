---
description: Die Abmeldung wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: e03fb15c-47d3-40ba-ae70-b7b0ba010004
title: 'Iuseridentitymanager:: Logoff-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logoff
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 4266e6116e43b7b792c3040d7c86a60037ca4c44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104976992"
---
# <a name="iuseridentitymanagerlogoff-method"></a>Iuseridentitymanager:: Logoff-Methode

\[Die Abmeldung **wird nicht** unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

Veraltet. Melden Sie sich von der aktuellen Identität ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Logoff(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Typ: **HWND**

Ein **HWND** -Wert, der ein Fenster identifiziert, das nach Abschluss der Abmeldung in den Vordergrund gestellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

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

[**Iuseridentitymanager:: manageidentities**](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




