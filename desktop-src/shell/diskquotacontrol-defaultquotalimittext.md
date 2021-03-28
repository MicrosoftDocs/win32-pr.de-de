---
description: Ruft die Standard Kontingent Grenze als Text Zeichenfolge ab.
title: Diskquotacontrol. defaultquotalimittext-Eigenschaft
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
ms.openlocfilehash: 442e9094c62f22c3d990cf1112d145a1b2838e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128441"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a>Diskquotacontrol. defaultquotalimittext-Eigenschaft

Ruft die Standard Kontingent Grenze als Text Zeichenfolge ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeichen folgen Wert, der die Standard Kontingent Grenze für neue Benutzer des Volumes enthält. Wenn das Standard Kontingent beispielsweise 10,5 MB beträgt, lautet der Wert der Eigenschaft "10,5 MB". Wenn für das Volume kein Standard Kontingent festgelegt ist, wird die-Eigenschaft auf "No Limit" oder die lokalisierte Entsprechung festgelegt.

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

[**Diskquotacontrol**](diskquotacontrol-object.md)
</dt> </dl>

 

 




