---
description: Legt das Standardkontingentlimit fest oder ruft es ab.
title: DiskQuotaControl.DefaultQuotaLimit-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 7d123bff-5dae-4430-be22-a822e231e43e
ms.openlocfilehash: 87c6bfdf9321b0746cdff96de60f29aa3ec9c93e9c3222d4bc262ae211ece147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860871"
---
# <a name="diskquotacontroldefaultquotalimit-property"></a>DiskQuotaControl.DefaultQuotaLimit-Eigenschaft

Legt das Standardkontingentlimit fest oder ruft es ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
iDefaultQuotaLimit = DiskQuotaControl.DefaultQuotaLimit
DiskQuotaControl.DefaultQuotaLimit = iDefaultQuotaLimit
```



## <a name="property-value"></a>Eigenschaftswert

Ein **Ganzzahlwert,** der die Standardkontingentgrenze für neue Benutzer in Bytes angibt oder empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DefaultQuotaLimitText**](diskquotacontrol-defaultquotalimittext.md)
</dt> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




