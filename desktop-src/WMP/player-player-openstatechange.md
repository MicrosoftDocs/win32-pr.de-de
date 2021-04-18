---
title: Player. OpenStateChange-Ereignis
description: Das OpenStateChange-Ereignis tritt auf, wenn die openstate-Eigenschaft den Wert ändert. | Player. OpenStateChange-Ereignis
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- Media Player für OpenStateChange-Ereignisfenster
- OpenStateChange-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player der Player-Klasse, OpenStateChange-Ereignis
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
ms.openlocfilehash: 020a25a811623b9f7d7dd8f316c470cada6a142b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351255"
---
# <a name="playeropenstatechange-event"></a>Player. OpenStateChange-Ereignis

Das **OpenStateChange** -Ereignis tritt auf, wenn die **openstate** -Eigenschaft den Wert ändert.

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

**Zahl** (**Long**), die den neuen geöffneten Zustand angibt. Eine Tabelle mit Werten finden Sie unter [openstate](player-openstate.md) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Windows-Media Player können mehrere offene Zustände durchlaufen, während versucht wird, eine Netzwerkdatei zu öffnen, z. b. das Auffinden des Servers, das Herstellen einer Verbindung mit dem Server und schließlich das Öffnen der Datei. Dieses Ereignis wird jedes Mal ausgelöst, wenn sich der Status des geöffneten Zustands ändert.

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

Es ist nicht garantiert, dass Windows-Media Player Zustände in einer bestimmten Reihenfolge auftreten. Außerdem treten nicht alle Zustände notwendigerweise während einer Sequenz von Ereignissen auf. Sie sollten keinen Code schreiben, der auf der Status Reihenfolge basiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player. openstate**](player-openstate.md)
</dt> </dl>

 

 





