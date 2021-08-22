---
description: Legt einen booleschen Wert fest oder ruft einen booleschen Wert ab, der angibt, ob ein Systemereignisprotokolleintrag erfolgt, wenn ein Benutzer sein zugewiesenes Kontingentlimit überschreitet.
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: DiskQuotaControl.LogQuotaLimit-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f10710c5a16feb946caa78394d5e57e5d7d4884a50d45dc3e37291f40e7d283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455880"
---
# <a name="diskquotacontrollogquotalimit-property"></a>DiskQuotaControl.LogQuotaLimit-Eigenschaft

Legt einen booleschen Wert fest oder ruft einen booleschen Wert ab, der angibt, ob ein Systemereignisprotokolleintrag erfolgt, wenn ein Benutzer sein zugewiesenes Kontingentlimit überschreitet.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft wird auf **TRUE** festgelegt, wenn ein Systemereignisprotokolleintrag erfolgt, wenn der Benutzer sein Kontingentlimit überschreitet, oder andernfalls **FALSE.**

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

[**DiskQuotaControl-Objekt**](diskquotacontrol-object.md)
</dt> <dt>

[**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




