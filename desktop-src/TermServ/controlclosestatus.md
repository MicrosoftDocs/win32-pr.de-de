---
title: Controlclosestatus-Enumeration
description: Gibt an, ob die Anwendung, die das Steuerelement enthält, das Steuerelement sofort schließen kann
ms.assetid: ac2e1c68-81b1-4b51-aa7e-0ff703e619a2
ms.tgt_platform: multiple
keywords:
- Controlclosestatus-Enumeration Remotedesktopdienste
topic_type:
- apiref
api_name:
- ControlCloseStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b94e0ce5cd040a2ade970f566897d2eac339dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949511"
---
# <a name="controlclosestatus-enumeration"></a>Controlclosestatus-Enumeration

Gibt an, ob die Anwendung, die das Steuerelement enthält, das Steuerelement sofort schließen kann

## <a name="syntax"></a>Syntax


```C++
enum ControlCloseStatus {
  controlCloseCanProceed     = 0x0000, 
  controlCloseWaitForEvents  = 0x0001 

};
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlclosecanfortsetzung**
</dt> <dd>

Der Container kann sofort geschlossen werden. Dies kann vorkommen, wenn das Steuerelement nicht verbunden ist.

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlclosewaitforevents**
</dt> <dd>

Der Container sollte auf Ereignisse mit [**imstscaxevents:: ongetrennte**](imstscaxevents-ondisconnected.md) oder [**imstscaxevents:: onconfirmclose**](imstscaxevents-onconfirmclose.md)warten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                      |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclient:: RequestClose**](imsrdpclient-requestclose.md)
</dt> <dt>

[**Imstscaxevents:: onconfirmclose**](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[**Imstscaxevents:: ongetrennte**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





