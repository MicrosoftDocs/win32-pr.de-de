---
title: AxWindowsMediaPlayer. currentMedia (Eigenschaft)
description: Die currentMedia-Eigenschaft ruft die iwmpmedia-Schnittstelle ab, die dem aktuellen Medien Element entspricht, oder legt diese fest.
ms.assetid: 814ccb1d-713d-4b91-b225-d2199a7c9b6b
keywords:
- currentMedia-Eigenschaften Fenster Media Player
- currentMedia-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, currentMedia-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3720a36d2a1969c652ed757f31301cf6a9ead706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354723"
---
# <a name="axwindowsmediaplayercurrentmedia-property"></a>AxWindowsMediaPlayer. currentMedia (Eigenschaft)

Die currentMedia-Eigenschaft ruft die iwmpmedia-Schnittstelle ab, die dem aktuellen Medien Element entspricht, oder legt diese fest.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPMedia currentMedia {get; set;}
```


```VB

Public Property currentMedia As IWMPMedia
```





## <a name="property-value"></a>Eigenschaftswert

Die WMPLib. iwmpmedia-Schnittstelle, die Zugriff auf das aktuelle Medien Element bereitstellt.

## <a name="remarks"></a>Bemerkungen

Wenn AxWindowsMediaPlayer. Settings. die **Autostart** -Eigenschaft ist "true". die Wiedergabe beginnt automatisch, wenn Sie **currentMedia** festlegen.

Sie können eine iwmpmedia-Schnittstelle für ein bestimmtes Medien Element über die iwmpwiedergabe. Item-Eigenschaft (die iwmpwiedergabe. get \_ Item-Methode in c#) abrufen. Wenn Sie ein Medien Element mithilfe eines Datei namens laden möchten, legen Sie die URL-Eigenschaft fest, oder verwenden Sie newmedia.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das erste Medien Element in der Bibliothek abgerufen und die currentMedia-Eigenschaft verwendet, um das abgerufene Medien Element als Aktuelles Medien Element festzulegen und seinen Namen anzuzeigen. Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Get an interface to the first media item in the library. 
WMPLib.IWMPMedia3 firstMedia = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Make the retrieved media item the current media item.
player.currentMedia = firstMedia;

// Display the name of the current media item.
currentMediaLabel.Text = ("Found first media item. Name = " + player.currentMedia.name);
```


```VB

' Get an interface to the first media item in the library. 
Dim firstMedia As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Make the retrieved media item the current media item.
player.currentMedia = firstMedia

&#39; Display the name of the current media item.
currentMediaLabel.Text = (&quot;Found first media item. Name = &quot; + player.currentMedia.name)
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. newmedia (VB und c#)**](axwmplib-axwindowsmediaplayer-newmedia.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB und c#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe. Item (VB und c#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. Autostart (VB und c#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





