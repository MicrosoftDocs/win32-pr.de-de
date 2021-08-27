---
description: Legt den Status der Datenträgerkontingente des Volumes fest oder ruft sie ab.
title: DiskQuotaControl.QuotaState (Eigenschaft)
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
ms.openlocfilehash: cb2117237cd3072163447ee80895cbbb8bb854d7ad4424da83854b28ffa96196
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090630"
---
# <a name="diskquotacontrolquotastate-property"></a>DiskQuotaControl.QuotaState (Eigenschaft)

Legt den Status der Datenträgerkontingente des Volumes fest oder ruft sie ab.

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
| dqStateDisable | 0     | Datenträgerkontingente sind deaktiviert. |
| dqStateTrack   | 1     | Datenträgerkontingente sind deaktiviert. |
| dqStateEnforce | 2     | Erzwingen sie eine Kontingentgrenze.      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DiskQuotaControl-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




