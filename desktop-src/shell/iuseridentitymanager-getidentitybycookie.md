---
description: Getidentitybycookie wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: 'Iuseridentitymanager:: getidentitybycookie-Methode (Msident. h)'
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
ms.openlocfilehash: eb4e5ad5bda349a5b1650b090abc44a9fd1e6332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524440"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a>Iuseridentitymanager:: getidentitybycookie-Methode

\[**Getidentitybycookie** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

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

*uidcookie* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **GUID \** _

Die Adresse eines _ *GUID**-Werts, der das Cookie für die Identität darstellt, die Sie abrufen möchten.

</dd> <dt>

*ppIdentity* \[ vorgenommen\]
</dt> <dd>

Type: **[ **iuseridentity**](iuseridentity.md)\*\***

Die Adresse des Zeigers, der das Benutzer Identitäts Objekt empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Das Ergebnis der Abruf Anforderung. Bei erfolgreicher Ausführung wird S OK zurückgegeben \_ . Andernfalls wird einer der folgenden Fehlercodes zurückgegeben.



| Rückgabecode                                                                                            | Beschreibung                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**E- \_ Identität \_ nicht \_ gefunden**</dt> </dl> | Die angeforderte Identität konnte nicht gefunden werden.<br/>     |
| <dl> <dt>**E- \_ Identitäten \_ deaktiviert**</dt> </dl> | Die Identitätsverwaltung ist im System deaktiviert.<br/> |



 

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



 

 




