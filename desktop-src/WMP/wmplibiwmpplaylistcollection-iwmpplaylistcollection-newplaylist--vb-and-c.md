---
title: Iwmpplaylistcollection newwiedergabe-Methode
description: Die newwiedergabe-Methode gibt eine iwmpwiedergabe-Schnittstelle für eine neue, leere Wiedergabeliste in der Bibliothek zurück.
ms.assetid: cc0cb356-9a90-421c-8d1a-b79585f71124
keywords:
- newwiedergabe-Methode, Windows-Media Player
- newwiedergabe-Methode, Windows Media Player, iwmpplaylistcollection-Schnittstelle
- Iwmpplaylistcollection-Schnittstelle Windows Media Player, newwiedergabe-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.newPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc455c5815cee1aaac139886bca1d847ddc62b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367543"
---
# <a name="iwmpplaylistcollectionnewplaylist-method"></a>Iwmpplaylistcollection:: newwiedergabe-Methode

Die **newwiedergabe** -Methode gibt eine **iwmpwiedergabe** -Schnittstelle für eine neue, leere Wiedergabeliste in der Bibliothek zurück.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.newPlaylist
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrinname* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der der Name der neuen Wiedergabeliste ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die neue Wiedergabeliste.

## <a name="remarks"></a>Bemerkungen

Diese Methode erstellt eine leere Wiedergabeliste in der Bibliothek. Um die Wiedergabeliste mit Medien Elementen zu füllen, verwenden Sie **iwmpwiedergabe. appendItem** oder **iwmpwiedergabe. InsertItem**.

In der Bibliothek sind mehrere Wiedergabelisten mit dem gleichen Namen zulässig. Um zu vermeiden, dass mit dieser Methode ein doppelter Wiedergabelisten Name erstellt wird, verwenden Sie die **getByName** -Methode und **iwmpplaylistarray. count** , um zu ermitteln, ob bereits eine Wiedergabeliste mit einem bestimmten Namen vorhanden ist.

Führende und nachfolgende Leerzeichen sind in Wiedergabelisten Namen nicht zulässig und werden automatisch aus dem für den *bstrinname* -Parameter angegebenen Wert entfernt.

Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine neue leere Wiedergabeliste mit dem Namen "threelist" erstellt, der Wiedergabeliste hinzugefügt und eine Schnittstelle zurückgegeben. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Add a new empty playlist, named ThreeList, to the playlist collection.
WMPLib.IWMPPlaylist newList = player.playlistCollection.newPlaylist("ThreeList");
```


```VB

'  Add a new empty playlist, named ThreeList, to the playlist collection.
Dim newList As WMPLib.IWMPPlaylist = player.playlistCollection.newPlaylist(&quot;ThreeList&quot;)
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9 oder höher.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe. appendItem (VB und c#)**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe. InsertItem (VB und c#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistarray. Count (VB und c#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection-Schnittstelle (VB und c#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection. getByName (VB und c#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





