---
title: Player. positionChange-Ereignis
description: Das Positions Change-Ereignis tritt auf, wenn die aktuelle Position des Medien Elements geändert wurde.
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- Positions Change-Ereignisfenster Media Player
- Positions Change-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse Windows Media Player, positionChange-Ereignis
topic_type:
- apiref
api_name:
- Player.PositionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ab7f64d6f5c4a081b8a81a14e3fcb353e1478e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360422"
---
# <a name="playerpositionchange-event"></a>Player. positionChange-Ereignis

Das **Positions Change** -Ereignis tritt auf, wenn die aktuelle Position des Medien Elements geändert wurde.

## <a name="syntax"></a>Syntax


```JScript
Player.PositionChange(
  oldPosition,
  newPosition
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*oldposition* 
</dt> <dd>

Number (**Double**), das die alte Position angibt.

</dd> <dt>

*neuposition* 
</dt> <dd>

**Number** (**Double**), das die neue Position angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird während der Wiedergabe nicht routinemäßig ausgelöst. Sie tritt nur dann auf, wenn die aktuelle Position des Wiedergabe-Medien Elements aktiv geändert wird, z. b. wenn der Benutzer das Such handle oder den Code verschiebt, der einen Wert für Steuer *Elemente* angibt. **CurrentPosition**.

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





