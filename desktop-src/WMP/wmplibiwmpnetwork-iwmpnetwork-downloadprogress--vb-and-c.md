---
title: Iwmpnetwork DownloadProgress (Eigenschaft)
description: Die DownloadProgress-Eigenschaft ruft den Prozentsatz des abgeschlossenen Downloads ab.
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- Download Progress-Eigenschaften Fenster Media Player
- Download Progress-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, Download Progress (Eigenschaft)
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
ms.openlocfilehash: 4b10b767845ac951e1364e15c7f6f1d729882e0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358222"
---
# <a name="iwmpnetworkdownloadprogress-property"></a>Iwmpnetwork::d ownloadprogress-Eigenschaft

Die **DownloadProgress** -Eigenschaft ruft den Prozentsatz des abgeschlossenen Downloads ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der den Download Fortschritt als Prozentsatz ausgedrückt.

## <a name="remarks"></a>Bemerkungen

Wenn das Windows Media Player-Steuerelement mit einer digitalen Mediendatei verbunden ist, die gleichzeitig abgespielt und heruntergeladen werden kann, ruft die **DownloadProgress** -Eigenschaft den Prozentsatz der gesamten heruntergeladenen Datei ab. Diese Funktion wird zurzeit nur für digitale Mediendateien unterstützt, die von Webservern heruntergeladen werden. Eine Datei mit einem der folgenden Formate kann heruntergeladen und gleichzeitig abgespielt werden:

-   Advanced Systems Format (ASF)
-   Windows Media Audio (WMA)
-   Windows Media Video (WMV)
-   MP3
-   MPEG
-   WAV

Darüber hinaus können einige AVI-Dateien gleichzeitig heruntergeladen und abgespielt werden.

Verwenden Sie den **AxWindowsMediaPlayer. \_ Wmpocxevents \_ bufferingevent** , um zu bestimmen, wann die Pufferung gestartet oder angehalten wird.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **Download Progress** verwendet, um den Prozentsatz des abgeschlossenen Downloads anzuzeigen. Die Informationen werden in einer Bezeichnung als Reaktion auf das **Puffer** Ereignis angezeigt. Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer. buffereing-Ereignis (VB und c#)**](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[**Iwmpnetwork-Schnittstelle (VB und c#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





