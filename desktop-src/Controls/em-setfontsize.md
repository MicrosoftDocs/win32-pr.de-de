---
title: EM_SETFONTSIZE Meldung (RichEdit. h)
description: Legt den Schrift Grad für den ausgewählten Text in einem Rich-Edit-Steuerelement fest.
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- Windows-Steuerelemente für EM_SETFONTSIZE Meldung
topic_type:
- apiref
api_name:
- EM_SETFONTSIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb75276acbb86cbd452a8ad97698f1cd7382bd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476830"
---
# <a name="em_setfontsize-message"></a>EM \_ SetFontSize-Meldung

Legt den Schrift Grad für den ausgewählten Text in einem Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ändern der Punktgröße des ausgewählten Texts. Das Ergebnis wird entsprechend den in der folgenden Tabelle gezeigten Werten gerundet. Dieser Parameter sollte im Bereich von-1637 bis 1638 liegen. Die resultierende Schriftgröße liegt im Bereich von 1 bis 1638.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn kein Fehler aufgetreten ist, ist der Rückgabewert " **true**".

Wenn ein Fehler aufgetreten ist, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Sie können den Schrift Grad auf einfache Weise durch Senden der [**EM \_ getcharformat**](em-getcharformat.md) -Meldung erhalten.

Rich Edit fügt zuerst dem aktuellen Schrift Grad *wParam* hinzu und verwendet dann die resultierende Größe und die folgende Tabelle, um den Rundungs Wert zu bestimmen.



| Kreuz    | Rundungs Wert |
|---------|----------------|
| <= 12 | 1              |
| 28      | 2              |
| 36      | 0              |
| 48      | 0              |
| 72      | 0              |
| 80      | 0              |
| > 80 | 10             |



 

Wenn die resultierende Schriftgröße durch den Rundungs Wert nicht gleichmäßig teilbar ist, wird der Schrift Grad auf eine Zahl gerundet, die durch den Rundungs Wert gleichmäßig erkennbar ist. Wenn die Schriftgröße also kleiner oder gleich 12 ist, lautet der Rundungs Wert 1. Ebenso ist der Rundungs Wert 2, wenn der Schrift Grad kleiner oder gleich 28 ist. Bei Werten, die größer als 28 sind, werden die Schriftgrößen auf das nächste Band gerundet. Daher springt die Schriftgröße zu 36, 48, 72, 80. Nach 80 werden alle Rundungen in Schritten von zehn Punkten durchgeführt.

Der Schrift Grad ist abhängig vom Vorzeichen von *wParam* nach oben oder unten aufgerundet. Wenn *wParam* positiv ist, ist die Rundung immer auf dem neuesten Stand. Andernfalls ist die Rundung immer herunter. Wenn die aktuelle Schriftgröße den Wert 10 hat und *wParam* den Wert 3 hat, beträgt die resultierende Schriftgröße 14 (10 + 3 = 13, die nicht durch 2 teilbar ist, sodass die Größe auf 14 aufgerundet wird). Wenn die aktuelle Schriftgröße den Wert 14 hat und *wParam* den Wert-3 hat, ist die resultierende Schriftgröße 10 (14-3 = 11, der nicht durch 2 teilbar ist, sodass die Größe auf 10 gerundet).

Die Änderung wird auf jeden Teil der Auswahl angewendet. Wenn ein Teil des Texts 10 pt und 20 PT ist, werden die Schriftgrößen nach einem *wParam* -Aufrufsatz auf 1 festgelegt.

Weitere Beispiele sind in der folgenden Tabelle aufgeführt.



| Ursprünglicher Schrift Grad | *wParam* | Resultierende Schriftgröße |
|--------------------|----------|---------------------|
| 7                  | 1        | 8                   |
| 7                  | 3        | 10                  |
| 10                 | 3        | 14                  |
| 14                 | -3       | 10                  |
| 28                 | 1        | 36                  |
| 28                 | 3        | 36                  |
| 80                 | 1        | 90                  |
| 80                 | -1       | 72                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3,0<br/>                                                              |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ getcharformat**](em-getcharformat.md)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

**Licher**
</dt> <dt>

[Informationen zu Rich Edit-Steuerelementen](about-rich-edit-controls.md)
</dt> </dl>

 

 





