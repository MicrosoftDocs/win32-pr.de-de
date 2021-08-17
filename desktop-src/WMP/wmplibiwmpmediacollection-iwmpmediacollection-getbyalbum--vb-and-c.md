---
title: IWMPMediaCollection getByMedia-Methode
description: Die getByGibt-Methode gibt eine IWMPPlaylist-Schnittstelle zurück, die zugriff auf Medienelemente aus dem angegebenen Album ermöglicht.
ms.assetid: 26f004c0-de46-4792-8212-9d4ac749bb21
keywords:
- getBy-Methode Windows Media Player
- getBy-Methode Windows Media Player , IWMPMediaCollection-Schnittstelle
- IWMPMediaCollection-Schnittstelle Windows Media Player , getByMedia-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAlbum
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07137068961447b9f311dbdb765d34fbf2689ca80fd2035e8a60ebe27e4037bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929763"
---
# <a name="iwmpmediacollectiongetbyalbum-method"></a>IWMPMediaCollection::getByMedia-Methode

Die **getByGibt-Methode** gibt eine **IWMPPlaylist-Schnittstelle** zurück, die zugriff auf Medienelemente aus dem angegebenen Album ermöglicht.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist getByAlbum(
  System.String bstrAlbum
);
```


```VB

Public Function getByAlbum( _
  ByVal bstrAlbum As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAlbum
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrZeichenfolge* \[ In\]
</dt> <dd>

Die **System.String,** die der Titel des Albums ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib.IWMPPlaylist-Schnittstelle** für die abgerufenen Medienelemente.

## <a name="remarks"></a>Hinweise

Bevor Sie diese Methode aufrufen, müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Es gibt zwei Möglichkeiten, wie Sie eine **IWMPMediaCollection-Schnittstelle** abrufen können, und das Verhalten der **getByMedia-Methode** hängt davon ab, welche dieser beiden Methoden Sie verwenden. Wenn Sie die Schnittstelle abrufen, indem Sie [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)aufrufen, gibt die **getBy Auflistungsmethode** alle Medienelemente in der Bibliothek zurück. Wenn Sie die Schnittstelle jedoch durch Aufrufen von [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)abrufen, gibt die **getBy Audio-Methode** nur die Audioelemente in der Bibliothek zurück, die zum angegebenen Album gehören.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **getByProfil verwendet,** um eine Wiedergabeliste von Medienelementen zu erstellen, wenn der Benutzer auf eine Schaltfläche klickt. Die Wiedergabeliste enthält Elemente mit dem vom Benutzer angegebenen Album in einem Textfeld. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
private void playAlbum_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the album title text that the user entered in the text box. 
    string album = getAlbum.Text;

    // Create the playlist using getByAlbum. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAlbum(album);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAlbum_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAlbum.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the album title text that the user entered in the text box. 
    Dim album As String = getAlbum.Text

    &#39; Create the playlist using getByAlbum. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAlbum(album)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
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
</dt> </dl>

 

 





