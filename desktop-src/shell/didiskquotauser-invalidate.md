---
description: Löscht die zwischengespeicherten Benutzerinformationen des Objekts.
title: DIDiskQuotaUser.Invalidate-Methode
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
ms.openlocfilehash: 9f8ad77c9697ed5d284cf782f431ec59b38ca415
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843271"
---
# <a name="didiskquotauserinvalidate-method"></a>DIDiskQuotaUser.Invalidate-Methode

Löscht die zwischengespeicherten Benutzerinformationen des Objekts.

## <a name="syntax"></a>Syntax


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode löscht die im Cache des Objekts gespeicherten Benutzerinformationen. Wenn das nächste Mal eine Anforderung für kontingentbezogene Informationen erfolgt, ruft das -Objekt die Informationen vom NTFS-Volume ab und aktualisiert den Cache.

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

 

 




