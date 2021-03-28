---
description: Ruft den Warnungs Schwellenwert des Benutzers als Text Zeichenfolge ab.
ms.assetid: 55b53ad0-e7cd-4417-9087-297ac96e245f
title: Didiskquotauser. quotader OLDTEXT-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 511829233b93dbe164ce2feccd1247ccebf3ec3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977217"
---
# <a name="didiskquotauserquotathresholdtext-property"></a>Didiskquotauser. quotader OLDTEXT-Eigenschaft

Ruft den Warnungs Schwellenwert des Benutzers als Text Zeichenfolge ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
QuotaThresholdText = DIDiskQuotaUser.QuotaThresholdText
```



## <a name="property-value"></a>Eigenschaftswert

Der Zeichen folgen Wert, der den Warnungs Schwellenwert des Benutzers enthält. Wenn die Datenträger Nutzung eines Benutzers diesen Wert überschreitet und die [**logquotathreshold**](diskquotacontrol-logquotathreshold.md) -Eigenschaft auf **true** festgelegt ist, generiert das System einen Ereignisprotokoll Eintrag.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Idiskquotauser-Objekt**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**Quotalimittext**](didiskquotauser-quotalimittext.md)
</dt> <dt>

[**Quotathreshold**](didiskquotauser-quotathreshold.md)
</dt> </dl>

 

 




