---
description: Platziert das angegebene Benutzerobjekt für die Namensauflösung in der nächsten Zeile.
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
title: Diskquotacontrol. giveusernameresolutionpriority-Methode (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.GiveUserNameResolutionPriority
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1acf50e0cec59a7ee14fbd9d7760fb68b27c4de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525331"
---
# <a name="diskquotacontrolgiveusernameresolutionpriority-method"></a>Diskquotacontrol. giveusernameresolutionpriority-Methode

Platziert das angegebene Benutzerobjekt für die Namensauflösung in der nächsten Zeile.

## <a name="syntax"></a>Syntax


```JScript
DiskQuotaControl.GiveUserNameResolutionPriority(
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

Wenn die asynchrone Namensauflösung aktiviert ist, werden Benutzer Objekte in eine Warteschlange eingefügt. Standardmäßig werden Sie in der Reihenfolge gewartet, in der Sie in die Warteschlange gestellt werden. Mit der **giveusernameresolutionpriority** -Methode wird ein Objekt an den Anfang der Warteschlange verschoben, sodass es in der Reihe ist, gewartet zu werden.

Verwenden Sie die [**usernameresolution**](diskquotacontrol-usernameresolution.md) -Eigenschaft, um die asynchrone Namensauflösung zu aktivieren.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Diskquotacontrol-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




