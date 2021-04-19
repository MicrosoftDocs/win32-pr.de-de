---
title: Fehler Ereignis des AxWindowsMediaPlayer-Objekts
description: Das Error-Ereignis tritt auf, wenn das Windows Media Player-Steuerelement einen Fehlerzustand aufweist.
ms.assetid: d28c18a9-c650-4169-989b-8727b7a5a831
keywords:
- Fehler Ereignis der "AxWindowsMediaPlayer"-Objekt Fenster Media Player
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
ms.openlocfilehash: 6cfd3571538aa2cdd263a9f5d57e479e73818806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353803"
---
# <a name="error-event-of-the-axwindowsmediaplayer-object"></a>Fehler Ereignis des AxWindowsMediaPlayer-Objekts

Das Error-Ereignis tritt auf, wenn das Windows Media Player-Steuerelement einen Fehlerzustand aufweist.

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

Im folgenden Beispiel wird ein Ereignishandler für das Fehler Ereignis erstellt, um den Beschreibungstext für den ersten Fehler in der Fehler Warteschlange anzuzeigen. Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Iwmperror. Item (VB und c#)**](iwmperror-item--vb-and-c.md)
</dt> <dt>

[**Iwmperroritem. ErrorDescription (VB und c#)**](wmplibiwmperroritem-iwmperroritem-errordescription--vb-and-c.md)
</dt> </dl>

 

 





