---
title: CurrentItemChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das CurrentItemChange-Ereignis tritt auf, wenn sich der Wert von IWMPControls.currentItem ändert.
ms.assetid: c5eeafd2-405b-4808-97d1-399a2344ca42
keywords:
- CurrentItemChange-Ereignis des AxWindowsMediaPlayer-Windows Media Player
topic_type:
- apiref
api_name:
- CurrentItemChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1786fab3e312f95550103cdc6cf4f2558e25e883df9c7be2d6f850a7f8a5ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582556"
---
# <a name="currentitemchange-event-of-the-axwindowsmediaplayer-object"></a>CurrentItemChange-Ereignis des AxWindowsMediaPlayer-Objekts

Das CurrentItemChange-Ereignis tritt auf, wenn der Wert von IWMPControls. **currentItem-Änderungen.**

``` syntax
[C#]
private void player_CurrentItemChange(
  object sender,
  _WMPOCXEvents_CurrentItemChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentItemChange(  
  sender As Object,
  e As _WMPOCXEvents_CurrentItemChangeEvent
) Handles player.CurrentItemChange
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ CurrentItemChangeEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ CurrentItemChangeEvent**, das die folgende Eigenschaft im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft   | BESCHREIBUNG                                                                                                   |
|------------|---------------------------------------------------------------------------------------------------------------|
| pdispMedia | System.ObjectDas neue aktuelle Medienelement. Sie können dies in eine IWMPMedia-Schnittstelle um casten, um darauf zu zugreifen.<br/> |



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Ereignishandler für das CurrentItemChange-Ereignis veranschaulicht. Das AxWMPLib.AxWindowsMediaPlayer-Objekt wird durch die Variable player dargestellt.


```CSharp
// Add a delegate for the CurrentItemChange event
player.CurrentItemChange += new AxWMPLib._WMPOCXEvents_CurrentItemChangeEventHandler(player_CurrentItemChange);

private void player_CurrentItemChange(object sender, AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent e)
{
    // Display the name of the new media item.
    mediaText.Text = player.currentMedia.name;
}
```


```VB

Public Sub player_CurrentItemChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent) Handles player.CurrentItemChange

    &#39; Display the name of the new media item.
    mediaText.Text = player.currentMedia.name

End Sub
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPControls.currentItem (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





