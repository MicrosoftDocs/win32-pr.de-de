---
title: Player. playlistcollectionplaylistadded-Ereignis
description: Das playlistcollectionplaylistadded-Ereignis tritt auf, wenn der Wiedergabelisten Auflistung eine Wiedergabeliste hinzugefügt wird. | Player. playlistcollectionplaylistadded-Ereignis
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- Playlistcollectionplaylistadded-Ereignisfenster Media Player
- Playlistcollectionplaylistadded-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, playlistcollectionplaylistadded-Ereignis
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a229aff95d29ae93433dab538521d88c50c1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366730"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a>Player. playlistcollectionplaylistadded-Ereignis

Das **playlistcollectionplaylistadded** -Ereignis tritt auf, wenn der Wiedergabelisten Auflistung eine Wiedergabeliste hinzugefügt wird.

## <a name="syntax"></a>Syntax


```JScript
Player.PlaylistCollectionPlaylistAdded(
  bstrPlaylistName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrauplaylistname* 
</dt> <dd>

Eine **Zeichenfolge** , die den Namen der hinzugefügten Wiedergabeliste angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Name der hinzugefügten Wiedergabeliste kann verwendet werden, um das entsprechende **Wiedergabe** Listen Objekt mithilfe von *playlistcollection* abzurufen. **getByName** -Methode.

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

[**Playlistcollection. getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





