---
description: GetIdentityByCookie wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop.
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: IUserIdentityManager::GetIdentityByCookie-Methode (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.GetIdentityByCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: a077f3e6a65a04e4c018198dde39b80c5a6e5acbee282c9e2cc282642526894b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678154"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a>IUserIdentityManager::GetIdentityByCookie-Methode

\[**GetIdentityByCookie** wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop](fastuserswitching.md).\]

Ruft eine bestimmte Benutzeridentität durch das Cookie ab, das zur eindeutigen Identifizierung verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIdentityByCookie(
  [in]  GUID          *uidCookie,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uidCookie* \[ In\]
</dt> <dd>

Typ: **GUID \***

Die Adresse eines **GUID-Werts,** der das Cookie für die Identität darstellt, die Sie abrufen möchten.

</dd> <dt>

*ppIdentity* \[ out\]
</dt> <dd>

Typ: **[ **IUserIdentity**](iuseridentity.md)\*\***

Die Adresse des Zeigers, der das Benutzeridentitätsobjekt empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Das Ergebnis der Abrufanforderung. Wenn erfolgreich, wird S \_ OK zurückgegeben. Andernfalls wird einer der folgenden Fehlercodes zurückgegeben.



| Rückgabecode                                                                                            | Beschreibung                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**E \_ IDENTITY NOT FOUND (E-IDENTITÄT NICHT \_ \_ GEFUNDEN)**</dt> </dl> | Die angeforderte Identität wurde nicht gefunden.<br/>     |
| <dl> <dt>**DEAKTIVIERTE \_ E-IDENTITÄTEN \_**</dt> </dl> | Die Identitätsverwaltung ist auf dem System deaktiviert.<br/> |



 

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



 

 




