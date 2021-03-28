---
description: Ruft den Status des Benutzerkontos ab.
title: Didiskquotauser. accountStatus (Eigenschaft)
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
ms.openlocfilehash: 155ae627d70c5125fd0d1d501062224450fc8e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977257"
---
# <a name="didiskquotauseraccountstatus-property"></a>Didiskquotauser. accountStatus (Eigenschaft)

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
| dqacctregelöst    | 0     | Die Kontoinformationen wurden aufgelöst.    |
| dqacctunavailable | 1     | Kontoinformationen sind nicht verfügbar. |
| dqacctdeleted     | 2     | Das Konto wurde gelöscht.           |
| dqacctinvalid     | 3     | Das Konto ist ungültig.                 |
| dqacctunknown     | 4     | Das Konto wurde nicht gefunden.            |
| dqacctunaufgelöst  | 5     | Die Kontoinformationen sind nicht aufgelöst.  |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Didiskquotauser-Objekt**](didiskquotauser-object.md)
</dt> </dl>

 

 




