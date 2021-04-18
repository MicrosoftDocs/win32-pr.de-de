---
title: Player. openplaylistswitch-Ereignis
description: Das openplaylistswitch-Ereignis tritt auf, wenn die Wiedergabe eines Titels auf einer DVD beginnt. | Player. openplaylistswitch-Ereignis
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- Media Player für openplaylistswitch-Ereignisfenster
- Openplaylistswitch-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, openplaylistswitch-Ereignis
topic_type:
- apiref
api_name:
- Player.OpenPlaylistSwitch
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d35d4568356365cc9276c13ea33f866e937da1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364642"
---
# <a name="playeropenplaylistswitch-event"></a>Player. openplaylistswitch-Ereignis

Das **openplaylistswitch** -Ereignis tritt auf, wenn die Wiedergabe eines Titels auf einer DVD beginnt.

## <a name="syntax"></a>Syntax


```JScript
Player.OpenPlaylistSwitch(
  pItem
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pitem* 
</dt> <dd>

**Wiedergabe** Listen Objekt, das den Titel darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





