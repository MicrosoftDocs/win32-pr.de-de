---
title: Player.ModeChange-Ereignis
description: Das ModeChange-Ereignis tritt auf, wenn ein Modus Windows Media Player geändert wird. | Player.ModeChange-Ereignis
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- ModeChange-Windows Media Player
- ModeChange-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , ModeChange-Ereignis
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
ms.openlocfilehash: e4a1102d49064c602d04915f77eda7ecfa1c748d4aea000cef1271679da1ec62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054358"
---
# <a name="playermodechange-event"></a>Player.ModeChange-Ereignis

Das **ModeChange-Ereignis** tritt auf, wenn ein Modus Windows Media Player geändert wird.

## <a name="syntax"></a>Syntax


```JScript
Player.ModeChange(
  ModeName,
  NewValue
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ModeName* 
</dt> <dd>

**Eine Zeichenfolge,** die den geänderten Modus angibt. Enthält einen der folgenden Werte.



| Wert   | Beschreibung                                         |
|---------|-----------------------------------------------------|
| Shuffle | Spuren werden in zufälliger Reihenfolge abgespielt.                  |
| loop    | Die gesamte Sequenz von Spuren wird wiederholt abgespielt. |



 

</dd> <dt>

*NewValue* 
</dt> <dd>

**Boolescher Wert,** der den neuen Zustand des angegebenen Modus angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens auf eine Methode in einer importierten JScript-Datei zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt typisieren, einschließlich Groß- und Groß-/Schreibanforderungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Einstellungen.getMode**](settings-getmode.md)
</dt> <dt>

[**Einstellungen.setMode**](settings-setmode.md)
</dt> </dl>

 

 





