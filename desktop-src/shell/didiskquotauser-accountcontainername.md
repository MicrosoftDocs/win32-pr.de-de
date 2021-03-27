---
description: Ruft den Namen des Konto Containers des Benutzers ab.
title: Didiskquotauser. accountcontainername-Eigenschaft
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
ms.openlocfilehash: ef96b296d77979e5ef72c2804ad24628f0b0d8f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750225"
---
# <a name="didiskquotauseraccountcontainername-property"></a>Didiskquotauser. accountcontainername-Eigenschaft

Ruft den Namen des Konto Containers des Benutzers ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeichen folgen Wert, der auf den Konto Container Namen des Benutzers festgelegt ist.

## <a name="remarks"></a>Bemerkungen

Für Konten ohne Informationen zu Verzeichnisdiensten enthält diese Eigenschaft den Domänen Namen. Bei Konten mit Verzeichnisdienst Informationen enthält diese Eigenschaft einen kanonischen Namen, bei dem der abschließende Objektname entfernt wurde.

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

 

 




