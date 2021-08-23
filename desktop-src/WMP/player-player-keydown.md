---
title: Player.KeyDown-Ereignis
description: Das KeyDown-Ereignis tritt auf, wenn eine Taste gedrückt wird. | Player.KeyDown-Ereignis
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- KeyDown-Windows Media Player
- KeyDown-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , KeyDown-Ereignis
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
ms.openlocfilehash: a067e0125bea6bcabec591d6c1f3ec6fc5a2ee1b0d649a02009690c89d68952e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134773"
---
# <a name="playerkeydown-event"></a>Player.KeyDown-Ereignis

Das **KeyDown-Ereignis** tritt auf, wenn eine Taste gedrückt wird.

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

**Number** (**int**) gibt an, welcher physische Schlüssel gedrückt wird. Mögliche Werte finden Sie im Abschnitt „Hinweise“.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Number** (**int**) gibt ein Bitfeld mit den am wenigsten signifikanten Bits an, die der UMSCHALTTASTE (Bit 0), der STRG-Taste (Bit 1) und der ALT-Taste (Bit 2) entspricht. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Das Shift-Argument gibt den Zustand dieser Schlüssel an. Einige, alle oder keine der Bits können festgelegt werden, was darauf hinweist, dass einige, alle oder keine der Tasten gedrückt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das *nKeyCode-Argument* gibt einen physischen Schlüssel an. Die folgenden Tabellen zeigen die möglichen Werte für die Haupttasten auf einer Standardtastatur.

Werte für die Hauptschlüssel.



| Key                     | Wert   |
|-------------------------|---------|
| A-Z                     | 65-90   |
| 0-9                     | 48-56   |
| F1-F12                  | 112-123 |
| ESC                     | 27      |
| TAB                     | 9       |
| Feststelltaste               | 20      |
| UMSCHALT (links oder rechts)   | 16      |
| STRG (links oder rechts)    | 17      |
| ALT (links oder rechts)     | 18      |
| SPACE                   | 32      |
| RÜCKTASTE               | 8       |
| EINGABETASTE                   | 13      |
| Windows,links  | 91      |
| Windows Logo-TASTE rechts | 92      |
| Anwendungsschlüssel         | 93      |



 

Werte für die Nummernpadtasten.



| Key               | Wert  |
|-------------------|--------|
| 0-9               | 96-105 |
| NUM-SPERRE          | 144    |
| DIVIDE (/)        | 111    |
| MULTIPLY ( \* )     | 106    |
| SUBTRAHIEREN (-)      | 109    |
| ADD (+)           | 107    |
| TRENNZEICHEN (EINGABETASTE) | 108    |
| DECIMAL (.)       | 110    |



 

Werte für die Navigationsschlüssel.



| Key         | Wert |
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



 

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens auf eine Methode in einer importierten JScript datei zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt typisieren, einschließlich Groß- und Groß-/Schreibanforderungen.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





