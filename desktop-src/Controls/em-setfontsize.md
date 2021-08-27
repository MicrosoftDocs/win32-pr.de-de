---
title: EM_SETFONTSIZE Nachricht (Richedit.h)
description: Legt den Schriftgrad für den ausgewählten Text in einem Rich Edit-Steuerelement fest.
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- EM_SETFONTSIZE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: e646d58626a034f4764d6b9636e5b4b3eedba5befd7986eade9979c1f4a4fd5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048460"
---
# <a name="em_setfontsize-message"></a>EM \_ SETFONTSIZE-Meldung

Legt den Schriftgrad für den ausgewählten Text in einem Rich Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ändern Sie die Punktgröße des ausgewählten Texts. Das Ergebnis wird entsprechend den in der folgenden Tabelle dargestellten Werten gerundet. Dieser Parameter sollte im Bereich von -1637 bis 1638 liegen. Der resultierende Schriftgrad liegt im Bereich von 1 bis 1638.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn kein Fehler aufgetreten ist, ist der Rückgabewert **TRUE.**

Wenn ein Fehler aufgetreten ist, lautet der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Sie können den Schriftgrad problemlos abrufen, indem Sie die [**EM \_ GETCHARFORMAT-Nachricht**](em-getcharformat.md) senden.

Rich Edit fügt zuerst *wParam* zum aktuellen Schriftgrad hinzu und verwendet dann die resultierende Größe und die folgende Tabelle, um den Rundungswert zu bestimmen.



| Band    | Rundungswert |
|---------|----------------|
| <=12 | 1              |
| 28      | 2              |
| 36      | 0              |
| 48      | 0              |
| 72      | 0              |
| 80      | 0              |
| > 80 | 10             |



 

Wenn der resultierende Schriftgrad durch den Rundungswert nicht gleichmäßig geteilt werden kann, wird der Schriftgrad auf eine Zahl gerundet, die durch den Rundungswert gleichmäßig dividiert werden kann. Wenn der Schriftgrad also kleiner oder gleich 12 ist, ist der Rundungswert 1. Ebenso ist der Rundungswert 2, wenn der Schriftgrad kleiner oder gleich 28 ist. Bei Werten größer als 28 werden Schriftgrade auf das nächste Band gerundet. Der Schriftgrad springt also zu 36, 48, 72, 80. Nach 80 erfolgt die gesamte Rundung in Schritten von zehn Punkten.

Der Schriftgrad wird abhängig vom Vorzeichen von *wParam aufgerundet* oder heruntergerundet. Wenn *wParam* positiv ist, wird die Rundung immer hochgerundet. Andernfalls ist die Rundung immer nach unten. Wenn der aktuelle Schriftgrad also 10 und *wParam* 3 ist, beträgt der resultierende Schriftgrad 14 (10 + 3 = 13, was nicht durch 2 geteilt werden kann, sodass die Größe auf 14 aufgerundet wird). Wenn der aktuelle Schriftgrad dagegen 14 und *wParam* -3 ist, beträgt der resultierende Schriftgrad 10 (14 - 3 = 11, was nicht durch 2 geteilt werden kann, sodass die Größe auf 10 abgerundet wird).

Die Änderung wird auf jeden Teil der Auswahl angewendet. Wenn also ein Teil des Texts 10pt und einige 20pt sind, werden die Schriftgrade nach einem Aufruf mit *wParam* auf 1 festgelegt, 11pt bzw. 22pt.

Weitere Beispiele finden Sie in der folgenden Tabelle.



| Ursprünglicher Schriftgrad | *wParam* | Resultierender Schriftgrad |
|--------------------|----------|---------------------|
| 7                  | 1        | 8                   |
| 7                  | 3        | 10                  |
| 10                 | 3        | 14                  |
| 14                 | -3       | 10                  |
| 28                 | 1        | 36                  |
| 28                 | 3        | 36                  |
| 80                 | 1        | 90                  |
| 80                 | –1       | 72                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ GETCHARFORMAT**](em-getcharformat.md)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Informationen zu Rich Edit-Steuerelementen](about-rich-edit-controls.md)
</dt> </dl>

 

 





