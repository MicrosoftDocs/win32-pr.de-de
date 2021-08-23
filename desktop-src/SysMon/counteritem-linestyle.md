---
title: CounterItem.LineStyle-Eigenschaft
description: Ruft den Linienstil ab, der zum Diagramm des Indikatorwerts verwendet wird, oder legt diesen fest.
ms.assetid: 5801f0f8-37e5-4b15-a13f-24c71fea550d
keywords:
- LineStyle-Eigenschaft SysMon
- LineStyle-Eigenschaft SysMon , CounterItem-Klasse
- CounterItem-Klasse SysMon , LineStyle-Eigenschaft
topic_type:
- apiref
api_name:
- CounterItem.LineStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a60ce0c96f9e3eb25639cad9251d8cf3969d022001962e14ec9c3ef4d157ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883705"
---
# <a name="counteritemlinestyle-property"></a>CounterItem.LineStyle-Eigenschaft

Ruft den Linienstil ab, der zum Diagramm des Indikatorwerts verwendet wird, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Property LineStyle As Long
```



## <a name="property-value"></a>Eigenschaftswert

Der Linienstil, der zum Diagramm des Indikatorwerts verwendet wird. Die Werte entsprechen den in der folgenden Tabelle gezeigten Systemkonst konstanten.



| Wert                                                                                                                                                                                                                                                                                                                                                                               | Bedeutung                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="System.Drawing.Drawing2D.DashStyle.Solid"></span><span id="system.drawing.drawing2d.dashstyle.solid"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.SOLID"></span><dl> <dt>**System.Drawing.Drawing2D.DashStyle.Solid**</dt> <dt>0</dt> </dl>                     | Durchgehende Linie. Dies ist der Standardwert.<br/>                |
| <span id="System.Drawing.Drawing2D.DashStyle.Dash"></span><span id="system.drawing.drawing2d.dashstyle.dash"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASH"></span><dl> <dt>**System.Drawing.Drawing2D.DashStyle.Dash**</dt> <dt>1</dt> </dl>                         | Gepunktete Linie mit langen Segmenten und schmalen Leerzeichen.<br/>     |
| <span id="System.Drawing.Drawing2D.DashStyle.Dot"></span><span id="system.drawing.drawing2d.dashstyle.dot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DOT"></span><dl> <dt>**System.Drawing.Drawing2D.DashStyle.Dot**</dt> <dt>2</dt> </dl>                             | Gepunktete Linie mit einheitlichen Segmenten und Leerzeichen.<br/>         |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOT"></span><dl> <dt>**System.Drawing.Drawing2D.DashStyle.DashDot**</dt> <dt>3</dt> </dl>             | Gepunktete Linie mit abwechselnden kurzen und langen Segmenten.<br/> |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDotDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdotdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOTDOT"></span><dl> <dt>**System.Drawing.Drawing2D.DashStyle.DashDotDot**</dt> <dt>4</dt> </dl> | Gepunktete Linie mit abwechselnden Bindestrichen und doppelten Punkten.<br/>  |



 

## <a name="exceptions"></a>Ausnahmen



| Ausnahmetyp               | Bedingung                              |
|------------------------------|----------------------------------------|
| **System.ArgumentException** | Das angegebene Linienformat ist ungültig. |



 

## <a name="remarks"></a>Hinweise

Um einen anderen Wert als DashStyle.Solid anzugeben, [**muss CounterItem.Width**](counteritem-width.md) auf 1 festgelegt werden. Wenn die Breite größer als 1 ist, ignoriert SYSMON den angegebenen Linienstil und verwendet DashStyle.Solid.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





