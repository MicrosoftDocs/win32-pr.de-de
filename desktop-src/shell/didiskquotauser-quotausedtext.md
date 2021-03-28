---
description: Ruft die aktuelle Datenträger Verwendung des Benutzers als Text Zeichenfolge ab.
title: Didiskquotauser. quotausedtext (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsedText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: be27a17c-77ec-4016-8c2e-16fbc88c7c7a
ms.openlocfilehash: 1091d7f2d75b264b085c09af1873ac7c8ebd1617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977208"
---
# <a name="didiskquotauserquotausedtext-property"></a>Didiskquotauser. quotausedtext (Eigenschaft)

Ruft die aktuelle Datenträger Verwendung des Benutzers als Text Zeichenfolge ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeichen folgen Wert, der auf den derzeit verwendeten Speicherplatz festgelegt ist. Wenn die NTFS-Dateikomprimierung aktiviert ist, gibt diese Eigenschaft die Menge an Speicherplatz an, die die Daten in einem unkomprimierten Zustand erfordern.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Didiskquotauser-Objekt**](didiskquotauser-object.md)
</dt> <dt>

[**Quotalimittext**](didiskquotauser-quotalimittext.md)
</dt> <dt>

[**Quotader OLDTEXT**](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[**QuotaUsed**](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




