---
description: Legt einen Wert fest, der steuert, wie die Benutzersicherheits-ID (SID) in Benutzernamen aufgelöst wird, oder ruft diesen ab.
title: DiskQuotaControl.UserNameResolution-Eigenschaft
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
ms.openlocfilehash: cfc86f7f7da03ea4ffb092d50b51ef0c69349935cdae40586e08ae50f6ea251b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224613"
---
# <a name="diskquotacontrolusernameresolution-property"></a>DiskQuotaControl.UserNameResolution-Eigenschaft

Legt einen Wert fest, der steuert, wie die Benutzersicherheits-ID (SID) in Benutzernamen aufgelöst wird, oder ruft diesen ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.



| Auflösungstyp | Wert | BESCHREIBUNG                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| dqResolveNone   | 0     | Lösen Sie keine Benutzernameninformationen auf.                                                                                                                    |
| dqResolveSync   | 1     | Warten Sie, während Die Namensinformationen aufgelöst werden.                                                                                                                   |
| dqResolveAsync  | 2     | Warten Sie nicht, während Sie Namensinformationen auflösen. Das [**OnUserNameChanged-Ereignis**](diskquotacontrol-onusernamechanged.md) wird ausgelöst, wenn der Name aufgelöst wird. |



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wirkt sich auf die Enumeration von [**DIDiskQuotaUser-Objekten**](didiskquotauser-object.md) und die [**AddUser-**](diskquotacontrol-adduser.md) und [**FindUser-Methoden**](diskquotacontrol-finduser.md) aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DiskQuotaControl-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




