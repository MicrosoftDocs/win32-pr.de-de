---
title: Systemmonitor. Appearance (Eigenschaft)
description: Ruft die Darstellung des Steuer Elements ab oder legt diese fest, um dreidimensionale Anzeige Effekte einzuschließen oder auszulassen.
ms.assetid: cbc1f17f-991a-4b35-9c64-7750a17b42c8
keywords:
- Darstellungs Eigenschaft (Sysmon)
- Darstellungs Eigenschaft "sysmon", Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", Darstellungs Eigenschaft
topic_type:
- apiref
api_name:
- SystemMonitor.Appearance
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200c66f83a47f15421480967e8ea1ae9509b13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340308"
---
# <a name="systemmonitorappearance-property"></a>Systemmonitor. Appearance (Eigenschaft)

Ruft die Darstellung des Steuer Elements ab oder legt diese fest, um dreidimensionale Anzeige Effekte einzuschließen oder auszulassen.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property Appearance As Long
```



## <a name="property-value"></a>Eigenschaftswert

Der Darstellungs Wert, der bestimmt, ob das Steuerelement mit dreidimensionalen Effekten gezeichnet wird.

Sie können diese Eigenschaft auf einen der folgenden Werte festlegen.



| Wert                                                                        | Bedeutung                                                                                  |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Zeichnet das Steuerelement ohne visuelle Effekte.<br/>                                    |
| <dl> <dt>1</dt> </dl> | Zeichnet das-Steuerelement mit dreidimensionalen Effekten. Dies ist der Standardwert.<br/> |



 

## <a name="exceptions"></a>Ausnahmen



| Ausnahmetyp               | Bedingung                                    |
|------------------------------|----------------------------------------------|
| **System.ArgumentException** | Der angegebene Darstellungs Wert ist ungültig. |



 

## <a name="remarks"></a>Bemerkungen

Dies ist eine Ambient-Eigenschaft. Der Wert dieser Eigenschaft wird vom Container bestimmt. Das Festlegen des Werts dieser Eigenschaft kann sich auf die Illusion des Steuer Elements und Containers auswirken, die eine einzelne Anwendung sind.

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

 

 





