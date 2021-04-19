---
title: Iwmpnetwork-Eigenschaft (Eigenschaft)
description: Die Eigenschaft "receptionquality" Ruft den Prozentsatz der in den letzten 30 Sekunden nicht verlorenen Pakete ab.
ms.assetid: 103e6b8f-e029-4f53-93ac-b516896a7594
keywords:
- Eigenschaften Fenster von "receptionquality" Media Player
- Eigenschaft "receptionquality", Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, Eigenschaft "receptionquality"
topic_type:
- apiref
api_name:
- IWMPNetwork.receptionQuality
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3703ffa29183937874c40053bd3c7ae3c85d75d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370840"
---
# <a name="iwmpnetworkreceptionquality-property"></a>Iwmpnetwork:: receptionquality (Eigenschaft)

Die Eigenschaft " **receptionquality** " Ruft den Prozentsatz der in den letzten 30 Sekunden nicht verlorenen Pakete ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 receptionQuality {get; set;}
```


```VB

Public ReadOnly Property receptionQuality As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System. Int32** , die die Empfangsqualität ist.

## <a name="remarks"></a>Bemerkungen

Die Anzahl der während des Streamings empfangenen, verlorenen und wiederhergestellten Pakete wird einmal pro Sekunde überwacht. Die Eigenschaft " **receptionquality** " Ruft den Prozentsatz der in den letzten 30 Sekunden nicht verlorenen Pakete ab.

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf Null zurückgesetzt. Der Wert wird nicht zurückgesetzt, wenn die Wiedergabe angehalten wurde.

Diese Eigenschaft ruft nur während der Laufzeit gültige Informationen ab, wenn die URL für die Wiedergabe mithilfe der **AxWindowsMediaPlayer. URL** -Eigenschaft festgelegt wird.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird " **receptionquality** " verwendet, um den Prozentsatz der Pakete anzuzeigen, die in einer Bezeichnung als Reaktion auf das **PlayStateChange** -Ereignis empfangen werden. Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test whether content is playing. 
    if (e.newState == 3)
    {
        // Start the timer. Update the display every 10 seconds.
        timer.Interval = 10000;
        timer.Start();
    }
    else
    {
        // Not playing; stop the timer.
        timer.Stop();
    }
}

private void UpdateReceptionQuality(object sender, EventArgs e)
{
    receptionQualityLabel.Text = ("Packets recovered: " + player.network.receptionQuality.ToString() + "%");
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

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

Public Sub UpdateReceptionQuality(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    receptionQualityLabel.Text = (&quot;Packets recovered: &quot; + player.network.receptionQuality.ToString() + &quot;%&quot;)

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

[**Iwmpnetwork-Schnittstelle (VB und c#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





