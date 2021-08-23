---
title: IWMPControls playItem-Methode
description: Die playItem-Methode gibt das angegebene Medienelement wieder. | IWMPControls playItem-Methode
ms.assetid: ddd4e4f7-475c-4964-a623-9123ed66be8e
keywords:
- playItem-Methode Windows Media Player
- playItem-Methode Windows Media Player , IWMPControls-Schnittstelle
- IWMPControls-Schnittstelle Windows Media Player , playItem-Methode
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
ms.openlocfilehash: 1fabab78fe60120110f72176885e3b5825699b83782272dfbef0b48c165d1d02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761030"
---
# <a name="iwmpcontrolsplayitem-method"></a>IWMPControls::p layItem-Methode

Die **playItem-Methode** gibt das angegebene Medienelement wieder.

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

*pIWMPMedia* \[ In\]
</dt> <dd>

Eine **WMPLib.IWMPMedia-Schnittstelle** für das Medienelement.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das Medienelement wird unabhängig vom Wert der **IWMPSettings.autoStart-Eigenschaft** automatisch geladen und wiedergegeben. Um ein Element zu laden, ohne es automatisch wiederzuspielen, legen **Sie IWMPSettings.autoStart** auf **false** fest, und weisen **Sie AxWindowsMediaPlayer.URL** einen Wert zu. Anschließend kann **IWMPControls.play** aufgerufen werden, um mit der Wiedergabe des Elements zu beginnen.

Hinweis

**playItem** funktioniert nur mit Elementen in **AxWindowsMediaPlayer.currentPlaylist.** Das Aufrufen von **playItem** mit einem Verweis auf ein gespeichertes Medienelement wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **playItem** verwendet, um ein Medienelement aus der aktuellen Wiedergabeliste wiederzuspielen. Das zu wiedergebende Element wird basierend auf seiner Position in der Wiedergabeliste ausgewählt. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer.currentPlaylist (VB und C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.URL (VB und C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPControls-Schnittstelle (VB und C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.Item (VB und C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.autoStart (VB und C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





