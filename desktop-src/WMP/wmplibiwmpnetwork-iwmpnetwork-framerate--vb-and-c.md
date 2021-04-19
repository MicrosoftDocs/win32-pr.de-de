---
title: Iwmpnetwork-Framerate (Eigenschaft)
description: Die Framerate-Eigenschaft ruft die aktuelle Video Frame Rate ab.
ms.assetid: 800ecf3d-3b2c-48f9-8fc4-c7c32757749a
keywords:
- Eigenschaften Fenster "Framerate" Media Player
- Framerate-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, Framerate (Eigenschaft)
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
ms.openlocfilehash: c338a116588fa9f1c552feff15f220e08b0f66e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367565"
---
# <a name="iwmpnetworkframerate-property"></a>Iwmpnetwork:: Framerate (Eigenschaft)

Die **Framerate** -Eigenschaft ruft die aktuelle Video Frame Rate ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 frameRate {get; set;}
```


```VB

Public ReadOnly Property frameRate As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, bei dem es sich um die aktuelle Frame Rate in Frames pro hundert Sekunden handelt.

> [!Note]  
> Obwohl die **encodecodframerate** -Eigenschaft die codierte Frame Rate in Frames pro Sekunde misst, misst die Framerate-Eigenschaft die aktuelle **Framerate** in Frames pro hundert Sekunden. Siehe Hinweise.

 

## <a name="remarks"></a>Bemerkungen

Der aktuelle Frameraten Wert wird in Frames pro hundert Sekunden zurückgegeben. Der Wert 2998 gibt z. b. 29,98 Frames pro Sekunde (fps) an.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **Framerate** verwendet, um die beim Codieren der Datei angegebene Framerate anzuzeigen. Die Informationen werden in einer Bezeichnung als Reaktion auf das **PlayStateChange** -Ereignis angezeigt. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpnetwork-Schnittstelle (VB und c#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**Iwmpnetwork. encodedframerate (VB und c#)**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)
</dt> </dl>

 

 





