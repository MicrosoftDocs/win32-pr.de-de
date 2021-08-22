---
title: Fehlerereignis des AxWindowsMediaPlayer-Objekts
description: Das Error-Ereignis tritt auf, wenn das Windows Media Player-Steuerelement eine Fehlerbedingung aufweist.
ms.assetid: d28c18a9-c650-4169-989b-8727b7a5a831
keywords:
- Fehlerereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
topic_type:
- apiref
api_name:
- Error Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a146f58276ab433fa11b4c5b212af43a92511328e22f70b93d0a45779f4eaa24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582158"
---
# <a name="error-event-of-the-axwindowsmediaplayer-object"></a>Fehlerereignis des AxWindowsMediaPlayer-Objekts

Das Error-Ereignis tritt auf, wenn das Windows Media Player-Steuerelement eine Fehlerbedingung aufweist.

``` syntax
[C#]
private void player_ErrorEvent(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_ErrorEvent(  
  sender As Object,  
  e As System.EventArgs
) Handles player.ErrorEvent
```

## <a name="event-data"></a>Ereignisdaten

Dieses Ereignis enthält keine Daten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Ereignishandler für das Error-Ereignis erstellt, um den Beschreibungstext für den ersten Fehler in der Fehlerwarteschlange anzuzeigen. Das AxWMPLib.AxWindowsMediaPlayer-Objekt wird durch die Variable player dargestellt.


```CSharp
// Add a delegate for the Error event.
player.ErrorEvent += new EventHandler(player_ErrorEvent);

private void player_ErrorEvent(object sender, System.EventArgs e)
{
    // Get the description of the first error. 
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the description of the first error. 
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

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

[**IWMPError.Item (VB und C#)**](iwmperror-item--vb-and-c.md)
</dt> <dt>

[**IWMPErrorItem.errorDescription (VB und C#)**](wmplibiwmperroritem-iwmperroritem-errordescription--vb-and-c.md)
</dt> </dl>

 

 





