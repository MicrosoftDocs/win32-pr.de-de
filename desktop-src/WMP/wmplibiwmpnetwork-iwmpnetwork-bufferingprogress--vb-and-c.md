---
title: Iwmpnetwork BufferingProgress (Eigenschaft)
description: Die BufferingProgress-Eigenschaft ruft den Prozentsatz der abgeschlossenen Pufferung ab.
ms.assetid: 8dc9f31e-7c34-4714-a633-d92c3da3052b
keywords:
- BufferingProgress-Eigenschaften Fenster Media Player
- BufferingProgress-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, BufferingProgress (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da8a27ba41e5c4e201a5bdf0197992c30bce80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370157"
---
# <a name="iwmpnetworkbufferingprogress-property"></a>Iwmpnetwork:: BufferingProgress (Eigenschaft)

Die **BufferingProgress** -Eigenschaft ruft den Prozentsatz der abgeschlossenen Pufferung ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 bufferingProgress {get; set;}
```


```VB

Public ReadOnly Property bufferingProgress As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der der Puffer Status ist, ausgedrückt als Prozentsatz.

## <a name="remarks"></a>Bemerkungen

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf Null zurückgesetzt. Wenn die Wiedergabe angehalten wird, wird Sie nicht zurückgesetzt.

Die Pufferung gilt nur für Streaminginhalte. Diese Eigenschaft ruft nur während der Laufzeit gültige Informationen ab, wenn die URL für die Wiedergabe mithilfe der **AxWindowsMediaPlayer. URL** -Eigenschaft festgelegt wird.

Verwenden Sie den **AxWindowsMediaPlayer. \_ Wmpocxevents \_ bufferingevent** , um zu bestimmen, wann die Pufferung gestartet oder angehalten wird.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **BufferingProgress** verwendet, um den Prozentsatz der in einer Bezeichnung abgeschlossenen Pufferung als Reaktion auf das Puffer Ereignis anzuzeigen. Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the buffering progress in a timer event handler.
private void UpdateBufferingProgress(object sender, EventArgs e)
{
    bufferingProgressLabel.Text = ("Buffering progress: " + player.network.bufferingProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

&#39; Update the buffering progress in a timer event handler.
Public Sub UpdateBufferingProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    bufferingProgressLabel.Text = (&quot;Buffering progress: &quot; + player.network.bufferingProgress + &quot; percent complete&quot;)

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

[**AxWindowsMediaPlayer. URL (VB und c#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. buffereing-Ereignis (VB und c#)**](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[**Iwmpnetwork-Schnittstelle (VB und c#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





