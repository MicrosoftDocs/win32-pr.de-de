---
title: Player. mediachange-Ereignis
description: Das mediachange-Ereignis tritt auf, wenn ein Medien Element geändert wird. | Player. mediachange-Ereignis
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- Media Player "mediachange-Ereignisfenster"
- Mediachange-Ereignisfenster Media Player, Player-Klasse
- Player-Klasse Windows Media Player, mediachange-Ereignis
topic_type:
- apiref
api_name:
- Player.MediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99a63e087356b5d39ae8d751236b8128330c4f3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372690"
---
# <a name="playermediachange-event"></a>Player. mediachange-Ereignis

Das **mediachange** -Ereignis tritt auf, wenn ein Medien Element geändert wird.

## <a name="syntax"></a>Syntax


```JScript
Player.MediaChange(
  Item
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Element* 
</dt> <dd>

**Medien** Objekt, das das geänderte Element darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird ein HTML-div-Element mit dem Namen "MEDIANAME" verwendet, um den Namen des aktuellen Medien Elements anzuzeigen. Der Code aktualisiert den Text im div-Element mit jedem Vorkommen des **mediachange** -Ereignisses. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<!-- Create an event handler for media change. -->
<SCRIPT FOR = "Player" EVENT = "mediaChange(Item)">
   // Test whether a valid currentMedia object exists.
   if (Player.currentMedia){
      // Display the name of the current media item.
      MediaName.innerHTML = Player.currentMedia.name;
   }
</SCRIPT>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





