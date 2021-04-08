---
title: Systemmonitor. showvaluebar (Eigenschaft)
description: Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob der Wert Balken (der Satz von statistischen Werten unterhalb des Diagramms) auf dem Steuerelement angezeigt wird.
ms.assetid: 320fbbbb-c4ea-4772-9b10-1e123849c255
keywords:
- Showvaluebar-Eigenschaft (Sysmon)
- Showvaluebar-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse sysmon, showvaluebar (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.ShowValueBar
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f393b36162fae6aed996d2afaccd4749f22598f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740624"
---
# <a name="systemmonitorshowvaluebar-property"></a>Systemmonitor. showvaluebar (Eigenschaft)

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob der Wert Balken (der Satz von statistischen Werten unterhalb des Diagramms) auf dem Steuerelement angezeigt wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property ShowValueBar As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass die Wert Leiste auf dem Steuerelement angezeigt wird. andernfalls false. Der Standardwert dieser Eigenschaft ist „TRUE“.

## <a name="remarks"></a>Bemerkungen

Die angezeigten Statistiken enthalten den letzten Wert, den Durchschnittswert und die Mindest-und Höchstwerte des aktuell ausgewählten Zählers für das angezeigte Zeitintervall. Um die anzuzeigenden Werte für den anzuzeigenden Wert auszuwählen, muss der Benutzer den-Wert im Legenden Bereich des-Steuer Elements auswählen.

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

 

 





