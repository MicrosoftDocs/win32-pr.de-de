---
title: Systemmonitor. BorderStyle (Eigenschaft)
description: Ruft die Rahmenart des Steuer Elements ab oder legt diese fest.
ms.assetid: 9151a3f6-71fb-43ea-b7f6-cc35048145cb
keywords:
- BorderStyle-Eigenschaften-sysmon
- BorderStyle-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse sysmon, BorderStyle (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.BorderStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5dd0cec7e4d0d6d3223da4486d4569f8bc611e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858844"
---
# <a name="systemmonitorborderstyle-property"></a>Systemmonitor. BorderStyle (Eigenschaft)

Ruft die Rahmenart des Steuer Elements ab oder legt diese fest.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property BorderStyle As Long
```



## <a name="property-value"></a>Eigenschaftswert

Rahmenart des Steuer Elements.

Sie können diese Eigenschaft auf einen der folgenden Werte festlegen.



| Wert                                                                                                                                                                                                                                                                                                                                                                                                   | Bedeutung                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="System.Windows.Forms.FormBorderStyle.VbBSNone"></span><span id="system.windows.forms.formborderstyle.vbbsnone"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBBSNONE"></span><dl> <dt>**System. Windows. Forms. FormBorderStyle. vbbsnone**</dt> <dt>0</dt> </dl>                     | Kein Rahmen. Dies ist der Standardwert.<br/> |
| <span id="System.Windows.Forms.FormBorderStyle.VbFixedSingle"></span><span id="system.windows.forms.formborderstyle.vbfixedsingle"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBFIXEDSINGLE"></span><dl> <dt>**System. Windows. Forms. FormBorderStyle. vbfixedsingle**</dt> <dt>1</dt> </dl> | Fixed, Single Border.<br/>                 |



 

## <a name="exceptions"></a>Ausnahmen



| Ausnahmetyp               | Bedingung                                |
|------------------------------|------------------------------------------|
| **System.ArgumentException** | Die angegebene Rahmenart ist ungültig. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**System Monitor**](systemmonitor.md)
</dt> </dl>

 

 





