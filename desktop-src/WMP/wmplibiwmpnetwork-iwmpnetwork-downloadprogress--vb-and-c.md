---
title: IWMPNetwork downloadProgress(Eigenschaft)
description: Die downloadProgress-Eigenschaft ruft den Prozentsatz des abgeschlossenen Downloads ab.
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- downloadProgress-Windows Media Player
- downloadProgress-Eigenschaft Windows Media Player , IWMPNetwork-Schnittstelle
- IWMPNetwork interface Windows Media Player , downloadProgress-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPNetwork.downloadProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96c2b47895d595a570191d9aa66b90b1cdc53392f8f111d64307074e5689f2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331979"
---
# <a name="iwmpnetworkdownloadprogress-property"></a>IWMPNetwork::d ownloadProgress-Eigenschaft

Die **downloadProgress-Eigenschaft** ruft den Prozentsatz des abgeschlossenen Downloads ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Int32,** bei dem es sich um den Downloadfortschritt in Prozent handelt.

## <a name="remarks"></a>Hinweise

Wenn das Windows Media Player-Steuerelement mit einer digitalen Mediendatei verbunden ist, die gleichzeitig abgespielt und heruntergeladen werden kann, ruft die **downloadProgress-Eigenschaft** den Prozentsatz der gesamten heruntergeladenen Datei ab. Dieses Feature wird derzeit nur für digitale Mediendateien unterstützt, die von Webservern heruntergeladen wurden. Eine Datei mit einem der folgenden Formate kann heruntergeladen und gleichzeitig abgespielt werden:

-   Advanced Systems Format (ASF)
-   Windows Media Audio (WMA)
-   Windows Media Video (WMV)
-   MP3
-   Mpeg
-   WAV

Darüber hinaus können einige AVI-Dateien heruntergeladen und gleichzeitig abgespielt werden.

Verwenden Sie **axWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent,** um zu bestimmen, wann die Pufferung beginnt oder beendet wird.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **downloadProgress** verwendet, um den Prozentsatz des abgeschlossenen Downloads anzuzeigen. Die Informationen werden als Reaktion auf das Pufferungsereignis in einer **Bezeichnung** angezeigt. Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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

// Update the download progress in a timer event handler.
private void UpdateDownloadProgress(object sender, EventArgs e)
{
    downloadProgressLabel.Text = ("Download progress: " + player.network.downloadProgress + " percent complete");
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

&#39; Update the download progress in a timer event handler.
Public Sub UpdateDownloadProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    downloadProgressLabel.Text = (&quot;Download progress: &quot; + player.network.downloadProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer.Buffering-Ereignis (VB und C#)**](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[**IWMPNetwork-Schnittstelle (VB und C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





