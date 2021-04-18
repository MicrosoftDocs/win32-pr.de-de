---
title: Iwmpnetwork receivedpakete (Eigenschaft)
description: Die receivedpaketen-Eigenschaft ruft die Anzahl der empfangenen Pakete ab.
ms.assetid: 2a79dc81-4c7a-45d6-bc2b-b19ff5704c3b
keywords:
- receivedpaketen-Eigenschaft, Windows Media Player
- receivedpaketen-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, receivedpakete (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.receivedPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c62b4d90039f07177e8fcdc971cb66e0044aee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354822"
---
# <a name="iwmpnetworkreceivedpackets-property"></a>Iwmpnetwork:: receivedpakete (Eigenschaft)

Die **receivedpaketen** -Eigenschaft ruft die Anzahl der empfangenen Pakete ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 receivedPackets {get; set;}
```


```VB

Public ReadOnly Property receivedPackets As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die Anzahl der empfangenen Pakete ist.

## <a name="remarks"></a>Bemerkungen

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf Null zurückgesetzt. Der Wert wird nicht zurückgesetzt, wenn die Wiedergabe angehalten wurde.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **receivedpakete** verwendet, um die Anzahl der empfangenen Pakete anzuzeigen. Die Informationen werden in einer Bezeichnung als Reaktion auf das **PlayStateChange** -Ereignis angezeigt. Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test whether packets may be arriving.
    switch (e.newState)
    {
        // If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
        // or Transitioning then stop the timer. 
        case 1: 
        case 2: 
        case 4: 
        case 5: 
        case 7: 
        case 8: 
        case 9: 
            timer.Stop();
            break;

        // If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        default:
            timer.Interval = 1000;
            timer.Start();
            break;
    }
}

private void UpdateReceivedPackets(object sender, EventArgs e)
{
    receivedPacketsLabel.Text = ("Packets received: " + player.network.receivedPackets.ToString());
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

Public Sub UpdateReceivedPackets(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    receivedPacketsLabel.Text = (&quot;Packets received: &quot; + player.network.receivedPackets.ToString())

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
</dt> </dl>

 

 





