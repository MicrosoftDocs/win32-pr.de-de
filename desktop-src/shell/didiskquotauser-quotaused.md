---
description: Ruft die aktuelle Datenträgerverwendung des Benutzers in Bytes ab.
title: DIDiskQuotaUser.QuotaUsed (Eigenschaft)
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
ms.openlocfilehash: c1584f2abd7fbb6d11d345ec78499b08dc0337e0ddd6bd6300e42a4ec3c2acec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459931"
---
# <a name="didiskquotauserquotaused-property"></a>DIDiskQuotaUser.QuotaUsed (Eigenschaft)

Ruft die aktuelle Datenträgerverwendung des Benutzers in Bytes ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a>Eigenschaftswert

Der  Ganzzahlwert, der auf die Menge des derzeit verwendeten Speicherplatzes festgelegt ist. Wenn die NTFS-Dateikomprimierung aktiviert ist, **gibt QuotaUsed** den Speicherplatz an, den die Daten in einem unkomprimierten Zustand benötigen würden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**QuotaThreshold**](didiskquotauser-quotathreshold.md)
</dt> <dt>

[**QuotaUsedText**](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




