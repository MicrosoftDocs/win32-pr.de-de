---
description: Legt einen booleschen Wert fest, der angibt, ob ein System Ereignisprotokoll-Eintrag erfolgt, wenn ein Benutzer seinen zugewiesenen Kontingent Schwellenwert überschreitet, oder ruft diesen booleschen Wert ab.
ms.assetid: 93bf5a4b-a887-4403-8c61-9ca8ba430c47
title: Diskquotacontrol. logquotathreshold (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fbbf83ae978e46a3867d27c23e8b8f726ba0d7dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977168"
---
# <a name="diskquotacontrollogquotathreshold-property"></a>Diskquotacontrol. logquotathreshold (Eigenschaft)

Legt einen booleschen Wert fest, der angibt, ob ein System Ereignisprotokoll-Eintrag erfolgt, wenn ein Benutzer seinen zugewiesenen Kontingent Schwellenwert überschreitet, oder ruft diesen booleschen Wert ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
bLogQuotaThreshold = DiskQuotaControl.LogQuotaThreshold
DiskQuotaControl.LogQuotaThreshold = bLogQuotaThreshold
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft wird auf **true** festgelegt, wenn ein Eintrag des System Ereignis Protokolls durchgeführt wird, wenn der Benutzer den Schwellenwert für die Kontingent Warnung überschreitet, andernfalls **false** .

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Defaultquotathreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**Diskquotacontrol-Objekt**](diskquotacontrol-object.md)
</dt> <dt>

[**Logquotalimit**](diskquotacontrol-logquotalimit.md)
</dt> </dl>

 

 




