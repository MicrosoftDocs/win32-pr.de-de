---
title: Player.OpenStateChange-Ereignis
description: Das OpenStateChange-Ereignis tritt auf, wenn die openState-Eigenschaft den Wert ändert. | Player.OpenStateChange-Ereignis
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- OpenStateChange-Ereignis Windows Media Player
- OpenStateChange-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , OpenStateChange-Ereignis
topic_type:
- apiref
api_name:
- Player.OpenStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65436dee60a5207e09a57a39c32dc479ce110e1dafb07a7dbd7cab86e4f0a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003220"
---
# <a name="playeropenstatechange-event"></a>Player.OpenStateChange-Ereignis

Das **OpenStateChange-Ereignis** tritt auf, wenn die **openState-Eigenschaft** den Wert ändert.

## <a name="syntax"></a>Syntax


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewState* 
</dt> <dd>

**Number** (**long**), die den neuen geöffneten Zustand angibt. Eine Tabelle mit Werten finden Sie unter [openState.](player-openstate.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Windows Media Player können mehrere offene Zustände durchlaufen, während versucht wird, eine Netzwerkdatei zu öffnen, z. B. den Server zu suchen, eine Verbindung mit dem Server herzustellen und schließlich die Datei zu öffnen. Dieses Ereignis wird jedes Mal ausgelöst, wenn sich der Öffnungszustand ändert.

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens in einer importierten JScript-Datei auf eine Methode zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt eingegeben werden, einschließlich Der Groß-/Großschreibung.

Windows Media Player Zustände werden in keiner bestimmten Reihenfolge garantiert. Darüber hinaus tritt nicht jeder Zustand notwendigerweise während einer Abfolge von Ereignissen auf. Sie sollten keinen Code schreiben, der von der Zustandsreihenfolge abhängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player.openState**](player-openstate.md)
</dt> </dl>

 

 





