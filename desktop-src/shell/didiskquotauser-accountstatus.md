---
description: Ruft den Status des Benutzerkontos ab.
title: DIDiskQuotaUser.AccountStatus-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ff2234f7-4758-43c7-a3c2-8fb980b27c04
ms.openlocfilehash: e27e86fadab02616f91a4838acfc4be93e985ebd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841651"
---
# <a name="didiskquotauseraccountstatus-property"></a>DIDiskQuotaUser.AccountStatus-Eigenschaft

Ruft den Status des Benutzerkontos ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft kann einen der folgenden Werte annehmen.



| Status            | Wert | BESCHREIBUNG                         |
|-------------------|-------|-------------------------------------|
| dqAcctResolved    | 0     | Kontoinformationen werden aufgelöst.    |
| dqAcctUnavailable | 1     | Kontoinformationen sind nicht verfügbar. |
| dqAcctDeleted     | 2     | Das Konto wurde gelöscht.           |
| dqAcctInvalid     | 3     | Das Konto ist ungültig.                 |
| dqAcctUnknown     | 4     | Das Konto wurde nicht gefunden.            |
| dqAcctUnresolved  | 5     | Kontoinformationen sind nicht aufgelöst.  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md)
</dt> </dl>

 

 




