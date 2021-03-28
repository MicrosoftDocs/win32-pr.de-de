---
description: Legt den Status der Datenträger Kontingente des Volumes fest oder ruft ihn ab.
title: Diskquotacontrol. quotastate (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaState
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b0766ecf-6e22-4481-a6a7-df873a277bc2
ms.openlocfilehash: 460decc1068642ae797723b31f7350082f591d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485523"
---
# <a name="diskquotacontrolquotastate-property"></a>Diskquotacontrol. quotastate (Eigenschaft)

Legt den Status der Datenträger Kontingente des Volumes fest oder ruft ihn ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.



| State          | Wert | BESCHREIBUNG               |
|----------------|-------|---------------------------|
| dqstatedeaktivieren | 0     | Datenträger Kontingente sind deaktiviert. |
| dqstatetrack   | 1     | Datenträger Kontingente sind deaktiviert. |
| dqstateerzwingen | 2     | Kontingent Limit erzwingen.      |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Diskquotacontrol-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




