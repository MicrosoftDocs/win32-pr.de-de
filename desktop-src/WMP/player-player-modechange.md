---
title: Player. modechange-Ereignis
description: Das modechange-Ereignis tritt auf, wenn ein Windows Media Player-Modus geändert wird. | Player. modechange-Ereignis
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- Modechange-Ereignisfenster Media Player
- Modechange-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse Windows Media Player, modechange-Ereignis
topic_type:
- apiref
api_name:
- Player.ModeChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb202672c7fce6705b8e86889c0ca44d7004a19e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366931"
---
# <a name="playermodechange-event"></a>Player. modechange-Ereignis

Das **modechange** -Ereignis tritt auf, wenn ein Windows Media Player-Modus geändert wird.

## <a name="syntax"></a>Syntax


```JScript
Player.ModeChange(
  ModeName,
  NewValue
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*"Name"* 
</dt> <dd>

**Zeichenfolge** , die den Modus angibt, der geändert wurde. Enthält einen der folgenden Werte.



| Wert   | BESCHREIBUNG                                         |
|---------|-----------------------------------------------------|
| Shuffle | Spuren werden in zufälliger Reihenfolge wiedergegeben.                  |
| loop    | Die gesamte Sequenz von Spuren wird wiederholt wiedergegeben. |



 

</dd> <dt>

*NewValue* 
</dt> <dd>

**Boolescher** Wert, der den neuen Zustand des angegebenen Modus angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Settings. getMode**](settings-getmode.md)
</dt> <dt>

[**Settings. setmode**](settings-setmode.md)
</dt> </dl>

 

 





