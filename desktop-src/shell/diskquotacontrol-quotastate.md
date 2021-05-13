---
description: Legt den Zustand der Datenträgerkontingente des Volumes fest oder ruft den Status ab.
title: DiskQuotaControl.QuotaState-Eigenschaft
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
ms.openlocfilehash: 3580ad47a5ec6a5d0276dc0e30a4a6463aca2fb3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843191"
---
# <a name="diskquotacontrolquotastate-property"></a>DiskQuotaControl.QuotaState-Eigenschaft

Legt den Zustand der Datenträgerkontingente des Volumes fest oder ruft den Status ab.

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
| dqStateEnforce | 2     | Erzwingen Sie das Kontingentlimit.      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DiskQuotaControl-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




