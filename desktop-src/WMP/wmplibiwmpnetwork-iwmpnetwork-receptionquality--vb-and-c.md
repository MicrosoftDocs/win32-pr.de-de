---
title: IWMPNetwork-Empfangsqualität (Eigenschaft)
description: Die eigenschaft "receptionQuality" ruft den Prozentsatz der Pakete ab, die in den letzten 30 Sekunden nicht verloren gegangen sind.
ms.assetid: 103e6b8f-e029-4f53-93ac-b516896a7594
keywords:
- eigenschafteneigenschaft Windows Media Player
- -Eigenschaft für die Windows Media Player , IWMPNetwork-Schnittstelle
- IWMPNetwork interface Windows Media Player , receptionQuality-Eigenschaft
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
ms.openlocfilehash: e5ea62391df07ed0e5e2c27752f668fda95a19d17dc6322fb7375ef5d3ed440f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098720"
---
# <a name="iwmpnetworkreceptionquality-property"></a>IWMPNetwork::receptionQuality -Eigenschaft

Die **eigenschaft "receptionQuality"** ruft den Prozentsatz der Pakete ab, die in den letzten 30 Sekunden nicht verloren gegangen sind.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 receptionQuality {get; set;}
```


```VB

Public ReadOnly Property receptionQuality As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Int32,** das die Empfangsqualität ist.

## <a name="remarks"></a>Hinweise

Die Anzahl der empfangenen, verlorenen und wiederhergestellten Pakete während des Streamings wird einmal pro Sekunde überwacht. Die **eigenschaft "receptionQuality"** ruft den Prozentsatz der Pakete ab, die in den letzten 30 Sekunden nicht verloren gegangen sind.

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf 0 (null) zurückgesetzt. Der Wert wird nicht zurückgesetzt, wenn die Wiedergabe angehalten wird.

Diese Eigenschaft ruft gültige Informationen nur zur Laufzeit ab, wenn die URL für die Wiedergabe mithilfe der **AxWindowsMediaPlayer.URL-Eigenschaft festgelegt** wird.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **"receivedQuality"** verwendet, um den Prozentsatz der in einer Bezeichnung empfangenen Pakete als Reaktion auf das **PlayStateChange-Ereignis** anzuzeigen. Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer.URL (VB und C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork-Schnittstelle (VB und C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





