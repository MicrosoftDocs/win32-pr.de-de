---
title: Player. playlistcollectionplaylistreverschogereignis
description: Das playlistcollectionplaylistrebewegungs-Ereignis tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelisten Auflistung entfernt wird. | Player. playlistcollectionplaylistreverschogereignis
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- Media Player "playlistcollectionplaylistreverschoder Ereignisfenster"
- Playlistcollectionplaylistregerührt-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, playlistcollectionplaylistreverschoeignis
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a449a7b00516f4fee613722d1cc126eb74227948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371528"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a>Player. playlistcollectionplaylistreverschogereignis

Das **playlistcollectionplaylistrebewegungs-Ereignis** tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelisten Auflistung entfernt wird.

## <a name="syntax"></a>Syntax


```JScript
Player.PlaylistCollectionPlaylistRemoved(
  bstrPlaylistName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrauplaylistname* 
</dt> <dd>

Eine **Zeichenfolge** , die den Namen der entfernten Wiedergabeliste angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

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

 

 





