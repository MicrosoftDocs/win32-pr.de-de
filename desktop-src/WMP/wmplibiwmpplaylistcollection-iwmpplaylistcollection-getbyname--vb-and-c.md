---
title: Iwmpplaylistcollection getByName-Methode
description: Die getByName-Methode gibt eine iwmpplaylistarray-Schnittstelle zurück, die Zugriff auf Wiedergabelisten mit dem angegebenen Namen bietet, sofern vorhanden.
ms.assetid: d41afab1-4103-4f59-a432-21a502499444
keywords:
- getByName-Methode, Windows-Media Player
- getByName-Methode, Windows Media Player, iwmpplaylistcollection-Schnittstelle
- Iwmpplaylistcollection-Schnittstelle Windows Media Player, getByName-Methode
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
ms.openlocfilehash: e51f83b4db019286c04762a081e649fec282135e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352064"
---
# <a name="iwmpplaylistcollectiongetbyname-method"></a>Iwmpplaylistcollection:: getByName-Methode

Die **getByName** -Methode gibt eine **iwmpplaylistarray** -Schnittstelle zurück, die Zugriff auf Wiedergabelisten mit dem angegebenen Namen bietet, sofern vorhanden.

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

*bstrinname* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der der Name der Wiedergabeliste ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib. iwmpplaylistarray** -Schnittstelle für das abgerufene Array von Wiedergabelisten.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie **iwmpplaylistarray. count** , um zu bestimmen, ob eine Wiedergabeliste vorhanden ist. Wenn **count** 0 (null) ist, ist das Array leer.

Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **getByName** verwendet, um die Wiedergabelisten Auflistung auf eine Wiedergabeliste mit dem Namen "Favoriten--4 und 5 Sterne bewertet" zu überprüfen. Wenn eine Wiedergabeliste mit diesem Namen vorhanden ist, wird Sie von **getByName** als aktuelle Wiedergabeliste festgelegt. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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
| Version<br/>   | Windows Media Player 9 oder höher.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpplaylistarray-Schnittstelle (VB und c#)**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistarray. Count (VB und c#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection-Schnittstelle (VB und c#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





