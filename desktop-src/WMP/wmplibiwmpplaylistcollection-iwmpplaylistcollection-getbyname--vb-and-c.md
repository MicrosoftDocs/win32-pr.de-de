---
title: IWMPPlaylistCollection getByName-Methode
description: Die getByName-Methode gibt eine IWMPPlaylistArray-Schnittstelle zurück, die den Zugriff auf Wiedergabelisten mit dem angegebenen Namen ermöglicht, sofern vorhanden.
ms.assetid: d41afab1-4103-4f59-a432-21a502499444
keywords:
- getByName-Windows Media Player
- getByName-Methode Windows Media Player , IWMPPlaylistCollection-Schnittstelle
- IWMPPlaylistCollection-Schnittstelle Windows Media Player , getByName-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fcee45af3ef55d53a05bab290fa92d3e6842fbb097358235b6720cbb1b54e0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999740"
---
# <a name="iwmpplaylistcollectiongetbyname-method"></a>IWMPPlaylistCollection::getByName-Methode

Die **getByName-Methode** gibt eine **IWMPPlaylistArray-Schnittstelle** zurück, die den Zugriff auf Wiedergabelisten mit dem angegebenen Namen ermöglicht, sofern vorhanden.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylistArray getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getByName
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrName* \[ In\]
</dt> <dd>

Eine **System.String,** die der Name der Wiedergabeliste ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib.IWMPPlaylistArray-Schnittstelle** für das abgerufene Array von Wiedergabelisten.

## <a name="remarks"></a>Hinweise

Verwenden **Sie IWMPPlaylistArray.count,** um zu bestimmen, ob eine Wiedergabeliste vorhanden ist. Wenn **count** 0 (null) ist, ist das Array leer.

Bevor Sie diese Methode aufrufen, müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **getByName** verwendet, um die Wiedergabelistensammlung auf eine Wiedergabeliste mit dem Namen "Favoriten - 4 und 5 sterngewertet" zu überprüfen. Wenn eine Wiedergabeliste mit diesem Namen vorhanden ist, **legt getByName** diese als aktuelle Wiedergabeliste fest. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// Get the count of the playlists named "Favorites -- 4 and 5 star rated".
int checkit = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").count;

// Since duplicate playlist names are allowed, the count returned
// will be either zero (no playlist) or greater than zero (playlist exists).
if (checkit > 0)
{
    // Retrieve a playlist array containing "Favorites -- 4 and 5 star rated".
    // Assume that there is only one playlist with that name, and assign it to the 
    // current playlist.
    player.currentPlaylist = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").Item(0);
}
```


```VB

'  Get the count of the playlists named &quot;Favorites -- 4 and 5 star rated&quot;.
Dim checkit As Integer = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).count

&#39;  Since duplicate playlist names are allowed, the count returned
&#39;  will be either zero (no playlist) or greater than zero (playlist exists).
If (checkit > 0) Then

    &#39;  Retrieve a playlist array object containing &quot;Favorites -- 4 and 5 star rated&quot;.
    &#39;  Assume that there is only one playlist with that name, and assign it to the 
    &#39;  current playlist.
    player.currentPlaylist = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).Item(0)

End If
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPPlaylistArray-Schnittstelle (VB und C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray.count (VB und C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection-Schnittstelle (VB und C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





