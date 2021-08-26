---
title: IWMPNetwork-Eigenschaft "encodedFrameRate"
description: Die encodedFrameRate-Eigenschaft ruft die vom Inhaltsautor angegebene Videobildrate ab.
ms.assetid: 4faf5675-5bf3-485d-802f-a1f900ddae63
keywords:
- encodedFrameRate-Eigenschaft Windows Media Player
- encodedFrameRate-Eigenschaft Windows Media Player , IWMPNetwork-Schnittstelle
- IWMPNetwork-Schnittstelle Windows Media Player , encodedFrameRate-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPNetwork.encodedFrameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f8a08572f65e1e44027ed25d84acfe7d917f92bf4bb63d5d9b8cca1e1201d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000010"
---
# <a name="iwmpnetworkencodedframerate-property"></a>IWMPNetwork::encodedFrameRate-Eigenschaft

Die **encodedFrameRate-Eigenschaft** ruft die vom Inhaltsautor angegebene Videobildrate ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 encodedFrameRate {get; set;}
```


```VB

Public ReadOnly Property encodedFrameRate As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Int32,** das die codierte Framerate in Frames pro Sekunde (fps) ist.

> [!Note]  
> Obwohl die **encodedFrameRate-Eigenschaft** die codierte Framerate in Frames pro Sekunde misst, misst die **frameRate-Eigenschaft** die aktuelle Bildfrequenz in Frames pro hundert Sekunden.

 

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **encodedFrameRate** verwendet, um die Framerate anzuzeigen, die beim Codieren der Datei angegeben wurde. Die Informationen werden als Reaktion auf das **PlayStateChange-Ereignis** in einer Bezeichnung angezeigt. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the encodedFrameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.encodedFrameRate != 0)
            {
                encodedFrameRateLabel.Text = "Current Encoded Frame Rate: " + player.network.encodedFrameRate + " K bits/second";
            }
            break;

        default:
            break;
    }
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the encodedFrameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.encodedFrameRate <> 0) Then

                encodedFrameRateLabel.Text = &quot;Current Encoded Frame Rate: &quot; + player.network.encodedFrameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPNetwork-Schnittstelle (VB und C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.frameRate (VB und C#)**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)
</dt> </dl>

 

 





