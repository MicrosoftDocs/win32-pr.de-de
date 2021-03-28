---
description: Ruft die aktuelle Datenträger Verwendung des Benutzers in Bytes ab.
title: Didiskquotauser. quotaused (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3e3ade59-b925-4ff5-ae7e-ed97eff506c7
ms.openlocfilehash: 7d5068e6f80fd2b0b435d04583e99da929e17fce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128448"
---
# <a name="didiskquotauserquotaused-property"></a>Didiskquotauser. quotaused (Eigenschaft)

Ruft die aktuelle Datenträger Verwendung des Benutzers in Bytes ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a>Eigenschaftswert

Der **ganzzahlige** Wert, der auf den derzeit verwendeten Speicherplatz festgelegt wird. Wenn die NTFS-Dateikomprimierung aktiviert ist, gibt **quotaused** die Menge an Speicherplatz an, die die Daten in einem unkomprimierten Zustand erfordern.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Didiskquotauser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**Quotathreshold**](didiskquotauser-quotathreshold.md)
</dt> <dt>

[**Quotausedtext**](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




