---
description: Legt einen Wert fest, der steuert, wie die Benutzer Sicherheits-ID (SID) in Benutzernamen aufgelöst wird, oder ruft ihn ab.
title: Diskquotacontrol. usernameresolution (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.UserNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: dc936421-e66d-4762-912a-c586f9cdace4
ms.openlocfilehash: fbe079680191937f022bd45a491fad054e1a9033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977505"
---
# <a name="diskquotacontrolusernameresolution-property"></a>Diskquotacontrol. usernameresolution (Eigenschaft)

Legt einen Wert fest, der steuert, wie die Benutzer Sicherheits-ID (SID) in Benutzernamen aufgelöst wird, oder ruft ihn ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.



| Lösungstyp | Wert | BESCHREIBUNG                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| dqresolvenone   | 0     | Informationen zu Benutzernamen nicht auflösen.                                                                                                                    |
| dqresolvesync   | 1     | Warten Sie, während Sie die Namen Informationen auflösen.                                                                                                                   |
| dqresolveasync  | 2     | Warten Sie nicht, während Sie die Namen Informationen auflösen. Das [**onusernamechanged**](diskquotacontrol-onusernamechanged.md) -Ereignis wird ausgelöst, wenn der Name aufgelöst wird. |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wirkt sich auf die Enumeration von [**didiskquotauser**](didiskquotauser-object.md) -Objekten sowie die Methoden " [**adduser**](diskquotacontrol-adduser.md) " und " [**FINDUSER**](diskquotacontrol-finduser.md) " aus.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Diskquotacontrol-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




