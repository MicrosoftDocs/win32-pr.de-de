---
description: Ruft die Standardkontingentgrenze als Textzeichenfolge ab.
title: DiskQuotaControl.DefaultQuotaLimitText-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimitText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ea1b02e0-c480-4ef1-b6e0-1ec202d5f3c5
ms.openlocfilehash: 378d06286a0334cf6ca3056038f45be3a5919b4fd2aa88934957122bc751c141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094227"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a>DiskQuotaControl.DefaultQuotaLimitText-Eigenschaft

Ruft die Standardkontingentgrenze als Textzeichenfolge ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeichenfolgenwert, der die Standardkontingentgrenze für neue Benutzer des Volumes enthält. Wenn das Standardkontingent beispielsweise 10,5 MB beträgt, ist der Wert der Eigenschaft "10,5 MB". Wenn das Volume über kein Standardkontingent verfügt, wird die -Eigenschaft auf "No Limit" oder die lokalisierte Entsprechung festgelegt.

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

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




