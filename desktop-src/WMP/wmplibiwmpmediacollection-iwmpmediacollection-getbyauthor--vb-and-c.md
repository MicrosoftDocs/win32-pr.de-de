---
title: IWMPMediaCollection getByAuthor-Methode
description: Die getByAuthor-Methode gibt eine IWMPPlaylist-Schnittstelle zurück, die den Zugriff auf die Medienelemente durch den angegebenen Autor ermöglicht.
ms.assetid: eb3793f6-bad1-4c80-991e-c6d0093ae57f
keywords:
- getByAuthor-Windows Media Player
- getByAuthor-Methode Windows Media Player , IWMPMediaCollection-Schnittstelle
- IWMPMediaCollection-Schnittstelle Windows Media Player , getByAuthor-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAuthor
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829232e6cd9fb64fec1d209991c3734ad435b4b69d0d7b66b135ab9cca1fe4a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053608"
---
# <a name="iwmpmediacollectiongetbyauthor-method"></a>IWMPMediaCollection::getByAuthor-Methode

Die `getByAuthor` -Methode gibt eine **IWMPPlaylist-Schnittstelle** zurück, die den Zugriff auf die Medienelemente durch den angegebenen Autor ermöglicht.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist getByAuthor(
  System.String bstrAuthor
);
```


```VB

Public Function getByAuthor( _
  ByVal bstrAuthor As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAuthor
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrAuthor* \[ In\]
</dt> <dd>

Die **System.String,** die der Name des Autors ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib.IWMPPlaylist-Schnittstelle** für die abgerufenen Medienelemente.

## <a name="remarks"></a>Hinweise

Bevor Sie diese Methode aufrufen, müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Es gibt zwei Möglichkeiten, wie Sie eine **IWMPMediaCollection-Schnittstelle** abrufen können, und das Verhalten der Methode hängt davon ab, `getByAuthor` welche dieser beiden Methoden Sie verwenden. Wenn Sie die Schnittstelle durch Aufrufen von [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)abrufen, gibt die Methode alle Medienelemente `getByAuthor` in der Bibliothek zurück. Wenn Sie die Schnittstelle jedoch durch Aufrufen von [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)abrufen, gibt die Methode nur die Audioelemente in der Bibliothek zurück, die über das angegebene Attribut und `getByAuthor` den angegebenen Wert verfügen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird `getByAuthor` verwendet, um eine Wiedergabeliste von Medienelementen zu erstellen, wenn der Benutzer auf eine Schaltfläche klickt. Die Wiedergabeliste enthält Elemente, die mit dem vom Benutzer angegebenen Namen des Autors in einem Textfeld übereinstimmen. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
private void playAuthor_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the author's name from the text box. 
    string author = getAuthor.Text;

    // Create the playlist using getByAuthor. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAuthor(author);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAuthor_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAuthor.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the author&#39;s name from the text box. 
    Dim author As String = getAuthor.Text

    &#39; Create the playlist using getByAuthor. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAuthor(author)

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPMediaCollection-Schnittstelle (VB und C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





