---
title: IWMPMediaCollection getByAttribute-Methode
description: Die getByAttribute-Methode gibt eine IWMPPlaylist-Schnittstelle zurück, die dem angegebenen Attribut mit dem angegebenen Wert entspricht.
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- getByAttribute-Windows Media Player
- getByAttribute-Methode Windows Media Player , IWMPMediaCollection-Schnittstelle
- IWMPMediaCollection-Schnittstelle Windows Media Player , getByAttribute-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAttribute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fb8dab44cd1f26c080d438c15f545c882d2e4427af7fa04049b539ce8b3cf13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735020"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a>IWMPMediaCollection::getByAttribute-Methode

Die **getByAttribute-Methode** gibt eine **IWMPPlaylist-Schnittstelle** zurück, die dem angegebenen Attribut mit dem angegebenen Wert entspricht.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist getByAttribute(
  System.String bstrAttribute,
  System.String bstrValue
);
```


```VB

Public Function getByAttribute( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAttribute
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrAttribute* \[ In\]
</dt> <dd>

Die **System.String,** die das angegebene Attribut ist.

</dd> <dt>

*bstrValue* \[ In\]
</dt> <dd>

Die **System.String,** die der angegebene Wert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib.IWMPPlaylist-Schnittstelle** für die abgerufenen Medienelemente.

## <a name="remarks"></a>Hinweise

Diese Methode kann verwendet werden, um eine generische Abfrage für Medienelemente zu erstellen, die mit einem Wert für ein Attribut in der Bibliothek übereinstimmen. Dies ist bei benutzerdefinierten Attributen nützlich. Wenn das Attribut nicht vorhanden ist, tritt ein Fehler auf.

Sie können diese Methode verwenden, um alle Medienelemente eines bestimmten Typs abzurufen. Verwenden Sie den Attributnamen **MediaType** und einen der folgenden Werte.



| Wert    | Beschreibung                                               |
|----------|-----------------------------------------------------------|
| Audio    | Musik und andere Nur-Audio-Elemente                          |
| Sonstige    | Andere Elemente, z. B. eine ASF-Datei oder die URL eines Streams. |
| Foto    | Fotoelemente. Erfordert Windows Media Player 10.            |
| Playlist | Wiedergabelisten, die als Medienelemente dargestellt werden.                     |
| radio    | Radiostationselemente. Wird nicht von Windows Media Player 10 verwendet. |
| video    | Videoelemente.                                              |



 

Bevor Sie diese Methode aufrufen, müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attributreferenz.](attribute-reference.md)

Es gibt zwei Möglichkeiten, wie Sie eine **IWMPMediaCollection-Schnittstelle** abrufen können, und das Verhalten der **getByAttribute-Methode** hängt davon ab, welche dieser beiden Methoden Sie verwenden. Wenn Sie die Schnittstelle durch Aufrufen von [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)abrufen, gibt die **getByAttribute-Methode** alle Medienelemente in der Bibliothek zurück. Wenn Sie die Schnittstelle jedoch durch Aufrufen von [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)abrufen, gibt die **getByAttribute-Methode** nur die Audioelemente in der Bibliothek zurück, die über das angegebene Attribut und den angegebenen Wert verfügen.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **getByAttribute** verwendet, um alle Inhalte aus der Bibliothek des Interpreten namens Attributde 48 wieder zu spielen. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// Get an interface to a playlist that contains media items by a particular artist.
WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
player.currentPlaylist = pl;

// Play the media items in the current playlist. 
player.Ctlcontrols.play();
```


```VB

' Get an interface to a playlist that contains media items by a particular artist.
Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAttribute(&quot;Artist&quot;, &quot;Triode 48&quot;)

&#39; Make the new playlist the current one.
player.currentPlaylist = pl

&#39; Play the media items in the current playlist. 
player.Ctlcontrols.play()
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPMediaCollection-Schnittstelle (VB und C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.getAll (VB und C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 





