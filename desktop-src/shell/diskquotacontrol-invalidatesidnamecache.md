---
description: Macht den Benutzernamen Cache für die Sicherheits-ID ungültig.
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: Diskquotacontrol. invalidatesidnamecache-Methode (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.InvalidateSidNameCache
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e7202c1293d32d55e12e88671ed9960d376f63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958769"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a>Diskquotacontrol. invalidatesidnamecache-Methode

Macht den Benutzernamen Cache für die Sicherheits-ID ungültig.

## <a name="syntax"></a>Syntax


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Benutzernamen und zugehörige Sicherheits-IDs werden in einem Cache gespeichert. Sie können diesen Cache durch Aufrufen von **invalidatesidnamecache** löschen. Wenn Sie anschließend ein neues Benutzerobjekt erstellen, müssen die Informationen vom Domänen Controller abgerufen werden, und der Cache muss wieder hergestellt werden.

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

 

 




