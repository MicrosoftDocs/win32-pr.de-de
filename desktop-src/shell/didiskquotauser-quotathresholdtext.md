---
description: Ruft den Warnungsschwellenwert des Benutzers als Textzeichenfolge ab.
ms.assetid: 55b53ad0-e7cd-4417-9087-297ac96e245f
title: DIDiskQuotaUser.QuotaThresholdText-Eigenschaft
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
ms.openlocfilehash: ca2136936d45850726e64b61c4fae62889d2b5e5ea30cd2b9c3a98357006e962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224675"
---
# <a name="didiskquotauserquotathresholdtext-property"></a>DIDiskQuotaUser.QuotaThresholdText-Eigenschaft

Ruft den Warnungsschwellenwert des Benutzers als Textzeichenfolge ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
QuotaThresholdText = DIDiskQuotaUser.QuotaThresholdText
```



## <a name="property-value"></a>Eigenschaftswert

Der Zeichenfolgenwert, der den Warnungsschwellenwert des Benutzers enthält. Wenn die Datenträgerverwendung eines Benutzers diesen Wert überschreitet und die [**LogQuotaThreshold-Eigenschaft**](diskquotacontrol-logquotathreshold.md) auf **TRUE** festgelegt ist, generiert das System einen Ereignisprotokolleintrag.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDiskQuotaUser-Objekt**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**QuotaLimitText**](didiskquotauser-quotalimittext.md)
</dt> <dt>

[**QuotaThreshold**](didiskquotauser-quotathreshold.md)
</dt> </dl>

 

 




