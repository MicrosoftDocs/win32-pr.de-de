---
description: Legt einen booleschen Wert fest, der angibt, ob ein Eintrag des System Ereignis Protokolls durchgeführt wird, wenn ein Benutzer sein zugewiesenes Kontingent Limit überschreitet, oder ruft ihn ab.
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: Diskquotacontrol. logquotalimit (Eigenschaft)
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
ms.openlocfilehash: 3db64d7fb06ed8bfb7ba8c2483eb413f3f01a224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977169"
---
# <a name="diskquotacontrollogquotalimit-property"></a>Diskquotacontrol. logquotalimit (Eigenschaft)

Legt einen booleschen Wert fest, der angibt, ob ein Eintrag des System Ereignis Protokolls durchgeführt wird, wenn ein Benutzer sein zugewiesenes Kontingent Limit überschreitet, oder ruft ihn ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft wird auf **true** festgelegt, wenn ein Eintrag des System Ereignis Protokolls durchgeführt wird, wenn der Benutzer das Kontingent Limit überschreitet, andernfalls **false** .

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

[**Diskquotacontrol-Objekt**](diskquotacontrol-object.md)
</dt> <dt>

[**Logquotathreshold**](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




