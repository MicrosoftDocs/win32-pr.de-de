---
title: Player. currentplaylistitemavailable-Ereignis
description: Das currentplaylistitemavailable-Ereignis tritt auf, wenn die aktuelle Wiedergabeliste verfügbar wird. | Player. currentplaylistitemavailable-Ereignis
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- Currentplaylistitemavailable-Ereignisfenster Media Player
- Currentplaylistitemavailable-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, currentplaylistitemavailable-Ereignis
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe5809e50d572cfb8eb7a36220d083ec18a0a76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361291"
---
# <a name="playercurrentplaylistitemavailable-event"></a>Player. currentplaylistitemavailable-Ereignis

Das **currentplaylistitemavailable** -Ereignis tritt auf, wenn die aktuelle Wiedergabeliste verfügbar wird.

## <a name="syntax"></a>Syntax


```JScript
Player.CurrentPlaylistItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstritemname* 
</dt> <dd>

**Zeichenfolge** , die den Namen des aktuellen Wiedergabelisten Elements enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Name der aktuellen Wiedergabeliste kann verwendet werden, um das entsprechende **Wiedergabe** Listen Objekt mithilfe von *playlistcollection* abzurufen. **getByName** -Methode.

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
</dt> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> <dt>

[**Playlistcollection. getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





