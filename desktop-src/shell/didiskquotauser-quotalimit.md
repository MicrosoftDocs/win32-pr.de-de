---
description: Legt die aktuelle Kontingent Grenze des Benutzers fest oder ruft diese ab.
title: Didiskquotauser. quotalimit (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 7eee1be7-8ad5-4796-910c-987fe3fd6338
ms.openlocfilehash: 6c13c0d38c3c5f4387b7ee90165057edb111124a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977224"
---
# <a name="didiskquotauserquotalimit-property"></a>Didiskquotauser. quotalimit (Eigenschaft)

Legt die aktuelle [**Kontingent Grenze**](diskquotacontrol-object.md)des Benutzers fest oder ruft diese ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
iQuotaLimit = DIDiskQuotaUser.QuotaLimit
DIDiskQuotaUser.QuotaLimit = iQuotaLimit
```



## <a name="property-value"></a>Eigenschaftswert

Ein **ganzzahliger** Wert, der die aktuelle Kontingent Grenze des Benutzers in Bytes angibt oder empfängt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Defaultquotalimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**Didiskquotauser**](didiskquotauser-object.md)
</dt> <dt>

[**Quotalimittext**](didiskquotauser-quotalimittext.md)
</dt> </dl>

 

 




