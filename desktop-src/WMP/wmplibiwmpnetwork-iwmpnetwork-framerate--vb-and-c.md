---
title: IWMPNetwork frameRate-Eigenschaft
description: Die frameRate-Eigenschaft ruft die aktuelle Videobildrate ab.
ms.assetid: 800ecf3d-3b2c-48f9-8fc4-c7c32757749a
keywords:
- frameRate-Eigenschaft Windows Media Player
- frameRate-Eigenschaft Windows Media Player , IWMPNetwork-Schnittstelle
- IWMPNetwork-Schnittstelle Windows Media Player , frameRate-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPNetwork.frameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3169cc21eee2317da45db3cb3ca9ceffffa01c85479312defe63cda1fa09796f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956160"
---
# <a name="iwmpnetworkframerate-property"></a>IWMPNetwork::frameRate-Eigenschaft

Die **frameRate-Eigenschaft** ruft die aktuelle Videobildrate ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 frameRate {get; set;}
```


```VB

Public ReadOnly Property frameRate As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.Int32-Datei,** die die aktuelle Bildfrequenz in Frames pro hundert Sekunden ist.

> [!Note]  
> Obwohl die **encodedFrameRate-Eigenschaft** die codierte Framerate in Frames pro Sekunde misst, misst die **frameRate-Eigenschaft** die aktuelle Bildfrequenz in Frames pro hundert Sekunden. Siehe Hinweise.

 

## <a name="remarks"></a>Hinweise

Der aktuelle Bildfrequenzwert wird in Frames pro hundert Sekunden zurückgegeben. Der Wert 2998 gibt beispielsweise 29,98 Frames pro Sekunde (fps) an.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **frameRate** verwendet, um die Framerate anzuzeigen, die beim Codieren der Datei angegeben wurde. Die Informationen werden als Reaktion auf das **PlayStateChange-Ereignis** in einer Bezeichnung angezeigt. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the frameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.frameRate != 0)
            {
                frameRateLabel.Text = "Current Frame Rate: " + player.network.frameRate + " K bits/second";
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

    &#39; Display the frameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.frameRate <> 0) Then

                frameRateLabel.Text = &quot;Current Frame Rate: &quot; + player.network.frameRate + &quot; K bits/second&quot;

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

[**IWMPNetwork.encodedFrameRate (VB und C#)**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)
</dt> </dl>

 

 





