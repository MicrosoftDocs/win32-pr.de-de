---
title: Player. KeyDown-Ereignis
description: Das KeyDown-Ereignis tritt auf, wenn eine Taste gedrückt wird. | Player. KeyDown-Ereignis
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- KeyDown-Ereignisfenster Media Player
- KeyDown-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse Windows Media Player, KeyDown-Ereignis
topic_type:
- apiref
api_name:
- Player.KeyDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226430421977a58eca02b7a42cf0349f2a5ff520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372691"
---
# <a name="playerkeydown-event"></a>Player. KeyDown-Ereignis

Das **KeyDown** -Ereignis tritt auf, wenn eine Taste gedrückt wird.

## <a name="syntax"></a>Syntax


```JScript
Player.KeyDown(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nKeyCode* 
</dt> <dd>

**Number** (**int**), der angibt, welcher physische Schlüssel gedrückt wird. Mögliche Werte finden Sie im Abschnitt „Hinweise“.

</dd> <dt>

*nshiftstate* 
</dt> <dd>

**Number** (**int**): gibt ein Bitfeld mit den geringsten signifikanten Bits an, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 und 4. Das Shift-Argument gibt den Zustand dieser Schlüssel an. Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das *nKeyCode* -Argument gibt einen physischen Schlüssel an. In den folgenden Tabellen sind die möglichen Werte für die Hauptschlüssel auf einer Standardtastatur aufgeführt.

Werte für die Hauptschlüssel.



| Schlüssel                     | Wert   |
|-------------------------|---------|
| A-Z                     | 65-90   |
| 0-9                     | 48-56   |
| F1-F12                  | 112-123 |
| ESC                     | 27      |
| TAB                     | 9       |
| Feststelltaste               | 20      |
| Shift (links oder rechts)   | 16      |
| STRG (links oder rechts)    | 17      |
| ALT (links oder rechts)     | 18      |
| SPACE                   | 32      |
| RÜCKTASTE               | 8       |
| EINGABETASTE                   | 13      |
| Windows-Taste, Links  | 91      |
| Windows-Taste, rechts | 92      |
| Anwendungsschlüssel         | 93      |



 

Werte für die Zahlen Füll Tasten.



| Schlüssel               | Wert  |
|-------------------|--------|
| 0-9               | 96-105 |
| NUM-Sperre          | 144    |
| Dividieren (/)        | 111    |
| Multiplizieren ( \* )     | 106    |
| Subtraktion (-)      | 109    |
| Hinzufügen (+)           | 107    |
| Trennzeichen (EINGABETASTE) | 108    |
| Dezimalzahl (.)       | 110    |



 

Werte für die Navigationstasten.



| Schlüssel         | Wert |
|-------------|-------|
| INSERT      | 45    |
| Delete      | 46    |
| POS1        | 36    |
| ENDE         | 35    |
| BILD-AUF     | 33    |
| BILD-AB   | 34    |
| NACH-OBEN-TASTE    | 38    |
| NACH-UNTEN-TASTE  | 40    |
| NACH-LINKS-TASTE  | 37    |
| NACH-RECHTS-TASTE | 39    |



 

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





