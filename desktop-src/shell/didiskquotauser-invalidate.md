---
description: Löscht die zwischengespeicherten Benutzerinformationen des-Objekts.
title: Didiskquotauser. Invalidate-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.Invalidate
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e0ffd5b7-db1d-40a4-810a-ff43549b0c9b
ms.openlocfilehash: 2b07ae6fd210b8722378a771cda97c2c04572c66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525343"
---
# <a name="didiskquotauserinvalidate-method"></a>Didiskquotauser. Invalidate-Methode

Löscht die zwischengespeicherten Benutzerinformationen des-Objekts.

## <a name="syntax"></a>Syntax


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode löscht die im Cache des Objekts gespeicherten Benutzerinformationen. Wenn Sie das nächste Mal eine Anforderung für Kontingent bezogene Informationen erhalten, ruft das-Objekt die Informationen vom NTFS-Volume ab und aktualisiert den Cache.

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

 

 




