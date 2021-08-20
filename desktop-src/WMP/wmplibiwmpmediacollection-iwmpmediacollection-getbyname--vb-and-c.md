---
title: IWMPMediaCollection getByName-Methode
description: Die getByName-Methode gibt eine IWMPPlaylist-Schnittstelle zurück, die Zugriff auf Medienelemente mit dem angegebenen Namen bietet.
ms.assetid: 137e938c-eb9f-4a87-8962-880e71a11ca2
keywords:
- getByName-Methode Windows Media Player
- getByName-Methode Windows Media Player , IWMPMediaCollection-Schnittstelle
- IWMPMediaCollection-Schnittstelle Windows Media Player , getByName-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c2e9eba2f4aa55e650a7e69572cc884fa237eb72869a0bbd882a42b546634c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053588"
---
# <a name="iwmpmediacollectiongetbyname-method"></a>IWMPMediaCollection::getByName-Methode

Die `getByName` -Methode gibt eine **IWMPPlaylist-Schnittstelle** zurück, die Zugriff auf Medienelemente mit dem angegebenen Namen bietet.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByName
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrName* \[ In\]
</dt> <dd>

Die **System.String,** die dem angegebenen Namen entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib.IWMPPlaylist-Schnittstelle** für die abgerufenen Medienelemente.

## <a name="remarks"></a>Hinweise

Vor dem Aufrufen dieser Methode benötigen Sie Lesezugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Es gibt zwei Möglichkeiten, wie Sie eine **IWMPMediaCollection-Schnittstelle** abrufen können, und das Verhalten der `getByName` Methode hängt davon ab, welche dieser beiden Methoden Sie verwenden. Wenn Sie die Schnittstelle durch Aufrufen von [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)abrufen, gibt die `getByName` Methode alle Medienelemente in der Bibliothek zurück. Wenn Sie jedoch die Schnittstelle durch Aufrufen von [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)abrufen, gibt die `getByName` Methode nur die Audioelemente in der Bibliothek zurück, die das angegebene Attribut und den angegebenen Wert aufweisen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird `getByName` verwendet, um drei Elemente aus der Bibliothek abzurufen. Jedes Element wird dann an die aktuelle Wiedergabeliste angefügt. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get an interface to a playlist that contains an Internet URL.
WMPLib.IWMPPlaylist one = player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");

// Get an interface to a playlist that contains a file on a network server.
WMPLib.IWMPPlaylist two = player.mediaCollection.getByName("Jeanne");

// Get an interface to a playlist that contains a file on a local drive.
WMPLib.IWMPPlaylist three = player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use the get_Item
// method with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.get_Item(0));
player.currentPlaylist.appendItem(two.get_Item(0));
player.currentPlaylist.appendItem(three.get_Item(0));
```


```VB

' In each case, use the name exactly as it appears in the library.
&#39; Windows Media Player does not include file name extensions or file paths
&#39; in the name. Internet URLs include the entire path, but not the 
&#39; file name extension.

&#39; Get an interface to a playlist that contains an Internet URL.
Dim one As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;https://www.proseware.com/Media/Laure&quot;)

&#39; Get an interface to a playlist that contains a file on a network server.
Dim two As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;Jeanne&quot;)

&#39; Get an interface to a playlist that contains a file on a local drive.
Dim three As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;house&quot;)

&#39; Append each item to the current playlist. Since each playlist retrieved
&#39; using getByName contains one digital media item, use the Item
&#39; property with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.Item(0))
player.currentPlaylist.appendItem(two.Item(0))
player.currentPlaylist.appendItem(three.Item(0))
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPMediaCollection-Schnittstelle (VB und C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





