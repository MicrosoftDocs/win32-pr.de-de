---
description: Legt das aktuelle Kontingentlimit des Benutzers fest oder ruft es ab.
title: DIDiskQuotaUser.QuotaLimit-Eigenschaft
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
ms.openlocfilehash: db0b6154d6eb6940a83434c010e7da1e124110f94cae7637d340621c86e7a30c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224730"
---
# <a name="didiskquotauserquotalimit-property"></a>DIDiskQuotaUser.QuotaLimit-Eigenschaft

Legt das aktuelle [**Kontingentlimit**](diskquotacontrol-object.md)des Benutzers fest oder ruft es ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
iQuotaLimit = DIDiskQuotaUser.QuotaLimit
DIDiskQuotaUser.QuotaLimit = iQuotaLimit
```



## <a name="property-value"></a>Eigenschaftswert

Ein **Ganzzahlwert,** der das aktuelle Kontingentlimit des Benutzers in Bytes angibt oder empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimitText**](didiskquotauser-quotalimittext.md)
</dt> </dl>

 

 




