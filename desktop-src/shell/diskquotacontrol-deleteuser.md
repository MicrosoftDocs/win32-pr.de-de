---
description: Löscht einen Benutzer aus dem Volume.
ms.assetid: 56a07388-b7d8-41a4-b29a-8a57fe0b9d19
title: Diskquotacontrol. DeleteUser-Methode (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DeleteUser
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c159375727ef115631a8a047d69ce235a5b8f2a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214426"
---
# <a name="diskquotacontroldeleteuser-method"></a>Diskquotacontrol. DeleteUser-Methode

Löscht einen Benutzer aus dem Volume.

## <a name="syntax"></a>Syntax


```JScript
DiskQuotaControl.DeleteUser(
  oUser
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*oUser* 
</dt> <dd>

Type: **Object**

Ein Objekt Ausdruck, der das [**didiskquotauser**](didiskquotauser-object.md) -Objekt des Benutzers ergibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode schlägt fehl, wenn der Benutzer über Speicherplatz auf dem Volume verfügt. Bevor Sie einen Benutzer aus einem Volume löschen, muss der gesamte Speicher für diesen Benutzer gelöscht, auf ein anderes Volume verschoben werden, oder der Besitz muss an einen anderen Benutzer übertragen werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AddUser**](diskquotacontrol-adduser.md)
</dt> <dt>

[**Diskquotacontrol**](diskquotacontrol-object.md)
</dt> </dl>

 

 




