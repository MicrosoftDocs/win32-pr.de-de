---
description: Ruft den Namen des Kontocontainers des Benutzers ab.
title: DIDiskQuotaUser.AccountContainerName (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountContainerName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b9b0355-ea69-4c34-b0be-fc8e5855ec73
ms.openlocfilehash: 1cb709ccc4fa0afcb56314bd097b1b0120b8b59a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843351"
---
# <a name="didiskquotauseraccountcontainername-property"></a>DIDiskQuotaUser.AccountContainerName (Eigenschaft)

Ruft den Namen des Kontocontainers des Benutzers ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeichenfolgenwert, der auf den Namen des Kontocontainers des Benutzers festgelegt ist.

## <a name="remarks"></a>Hinweise

Für Konten ohne Verzeichnisdienstinformationen enthält diese Eigenschaft den Domänennamen. Für Konten mit Verzeichnisdienstinformationen enthält diese Eigenschaft einen kanonischen Namen, bei dem der beendende Objektname entfernt wurde.

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

 

 




