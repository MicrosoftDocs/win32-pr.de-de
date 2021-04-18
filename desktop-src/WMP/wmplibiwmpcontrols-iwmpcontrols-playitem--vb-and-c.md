---
title: Iwmpcontrols-PlayItem-Methode
description: Die PlayItem-Methode gibt das angegebene Medien Element wieder. | Iwmpcontrols-PlayItem-Methode
ms.assetid: ddd4e4f7-475c-4964-a623-9123ed66be8e
keywords:
- PlayItem-Methoden Fenster Media Player
- PlayItem-Methode, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols-Schnittstelle, Windows Media Player, PlayItem-Methode
topic_type:
- apiref
api_name:
- IWMPControls.playItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2ac11f93409128eccc88c1d916144615d77476
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371311"
---
# <a name="iwmpcontrolsplayitem-method"></a>Iwmpcontrols::p layitem-Methode

Die **PlayItem** -Methode gibt das angegebene Medien Element wieder.

## <a name="syntax"></a>Syntax


```CSharp
public void playItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub playItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPControls.playItem
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*piwmpmedia* \[ in\]
</dt> <dd>

Eine **WMPLib. iwmpmedia** -Schnittstelle für das Medien Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das Medien Element wird unabhängig vom Wert der **iwmpsettings. Autostart** -Eigenschaft automatisch geladen und abgespielt. Wenn Sie ein Element ohne automatische Wiedergabe laden möchten, legen Sie " **iwmpsettings. Autostart** " auf " **false** " fest, und weisen Sie " **AxWindowsMediaPlayer. URL**" einen Wert zu, nachdem " **iwmpcontrols. Play** " aufgerufen werden kann, um die Wiedergabe des Elements

Hinweis

**PlayItem** funktioniert nur mit Elementen in **AxWindowsMediaPlayer. currentwiedergabe**. Das Aufrufen von **PlayItem** mit einem Verweis auf ein gespeichertes Medien Element wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **PlayItem** verwendet, um ein Medien Element aus der aktuellen Wiedergabeliste wiederzugeben. Das Element, das abgespielt werden soll, wird basierend auf seiner Position in der Wiedergabeliste ausgewählt. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
int index = 3;

// Get the media item at the fourth position in the current playlist.
WMPLib.IWMPMedia media = player.currentPlaylist.get_Item(index);

// Play the media item.
player.Ctlcontrols.playItem(media);
```


```VB

' Declare a variable to hold the position of the media item 
&#39; in the current playlist. An arbitrary value is supplied here.
Dim index As Integer = 3

&#39; Get the media item at the fourth position in the current playlist.
Dim Media As WMPLib.IWMPMedia = player.currentPlaylist.Item(index)

&#39; Play the media item.
player.Ctlcontrols.playItem(Media)
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer. currentwiedergabe (VB und c#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB und c#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols-Schnittstelle (VB und c#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. Play (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe. Item (VB und c#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. Autostart (VB und c#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





