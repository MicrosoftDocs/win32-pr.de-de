---
description: Erklärt den Cache des Benutzernamens der Sicherheits-ID für ungültig.
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: DiskQuotaControl.InvalidateSidNameCache-Methode (Dskquota.h)
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
ms.openlocfilehash: 1a171aaaf8f3faa45f967f29bf0f9d742aa0fe0221b46ae4ba4f8527d9cf9715
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455890"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a>DiskQuotaControl.InvalidateSidNameCache-Methode

Erklärt den Cache des Benutzernamens der Sicherheits-ID für ungültig.

## <a name="syntax"></a>Syntax


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Benutzernamen und zugeordnete Sicherheits-IDs werden in einem Cache gespeichert. Sie können diesen Cache löschen, indem Sie **InvalidateSidNameCache** aufrufen. Wenn Sie anschließend ein neues Benutzerobjekt erstellen, müssen die Informationen vom Domänencontroller abgerufen werden, und der Cache muss wiederhergestellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Dskquota.h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DiskQuotaControl-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




