---
title: Iwmpmediacollection getbygenre-Methode
description: Die getbygenre-Methode gibt eine iwmpwiedergabe-Schnittstelle zurück, die den Zugriff auf Medienelemente des angegebenen Genres ermöglicht.
ms.assetid: 0681e5a2-b56d-4c33-95ce-d9ef3cd5473d
keywords:
- getbygenre-Methode, Windows-Media Player
- getbygenre-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection Interface, Windows Media Player, getbygenre-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByGenre
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb6477a4cd212f354f5af3ab7e50fc2a87092cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359802"
---
# <a name="iwmpmediacollectiongetbygenre-method"></a>Iwmpmediacollection:: getbygenre-Methode

Die- `getByGenre` Methode gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf Medienelemente des angegebenen Genres ermöglicht.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist getByGenre(
  System.String bstrGenre
);
```


```VB

Public Function getByGenre( _
  ByVal bstrGenre As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByGenre
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstringenre* \[ in\]
</dt> <dd>

Der **System. String** -Wert, der der Name des Genres ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die abgerufenen Medienelemente.

## <a name="remarks"></a>Bemerkungen

Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Es gibt zwei Möglichkeiten, wie Sie eine **iwmpmediacollection** -Schnittstelle abrufen können, und das Verhalten der- `getByGenre` Methode hängt davon ab, welche dieser beiden Methoden Sie verwenden. Wenn Sie die Schnittstelle abrufen, indem Sie [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)aufrufen, gibt die- `getByGenre` Methode alle Medienelemente in der Bibliothek zurück. Wenn Sie jedoch die-Schnittstelle abrufen, indem Sie [iwmplibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)aufrufen, `getByGenre` gibt die-Methode nur die Audioelemente in der Bibliothek zurück, die über das angegebene Attribut und den angegebenen Wert verfügen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird verwendet `getByGenre` , um eine Wiedergabeliste von Medien Elementen abzurufen, wenn der Benutzer auf eine Schaltfläche klickt. Die Wiedergabeliste enthält Elemente mit dem vom Benutzer angegebenen Genre in einem Textfeld. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void playGenre_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the genre that the user entered in the text box. 
    string genre = getGenre.Text;

    // Create the playlist using getByGenre. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByGenre(genre);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playGenre.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the genre that the user entered in the text box. 
    Dim genre As String = getGenre.Text

    &#39; Create the playlist using getByGenre. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByGenre(genre)

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

[**Iwmpmediacollection-Schnittstelle (VB und c#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





