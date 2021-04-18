---
title: Player. KeyPress-Ereignis
description: Das KeyPress-Ereignis tritt auf, wenn eine Taste gedrückt und freigegeben wird. | Player. KeyPress-Ereignis
ms.assetid: fc51dfd3-7968-464a-a4e2-669ffcb52a59
keywords:
- KeyPress-Ereignisfenster Media Player
- KeyPress-Ereignisfenster Media Player, Player-Klasse
- Windows Media Player Player-Klasse, KeyPress-Ereignis
topic_type:
- apiref
api_name:
- Player.KeyPress
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b72dd703c13019c71b23af53790aa974927f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371030"
---
# <a name="playerkeypress-event"></a>Player. KeyPress-Ereignis

Das **KeyPress** -Ereignis tritt auf, wenn eine Taste gedrückt und freigegeben wird.

## <a name="syntax"></a>Syntax


```JScript
Player.KeyPress(
  nKeyAscii
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nkeyascii* 
</dt> <dd>

**Number** (**int**) gibt den standardmäßigen numerischen ANSI-Code für das Zeichen an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis tritt auf, wenn die Tastatureingabe ein beliebiges druckbares Tastatur Zeichen ergibt, die STRG-Taste mit einem Zeichen aus dem Standard Alphabet oder einem von einigen Sonderzeichen und der Eingabe-oder RÜCKTASTE gedrückt wird.

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

 

 





