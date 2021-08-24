---
title: IWMPNetwork sourceProtocol (Eigenschaft)
description: Die sourceProtocol-Eigenschaft ruft das Quellprotokoll ab, das zum Empfangen von Daten verwendet wird.
ms.assetid: db1d7651-3f25-4ac9-a3e1-dc3a8ddf8c40
keywords:
- sourceProtocol-Windows Media Player
- sourceProtocol-Eigenschaft Windows Media Player , IWMPNetwork-Schnittstelle
- IWMPNetwork-Schnittstelle Windows Media Player , sourceProtocol-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPNetwork.sourceProtocol
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 737bc0a5a4417735c795fc1058a7b821ee52489cf838be9eb934546f0fabacc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760850"
---
# <a name="iwmpnetworksourceprotocol-property"></a>IWMPNetwork::sourceProtocol (Eigenschaft)

Die **sourceProtocol-Eigenschaft** ruft das Quellprotokoll ab, das zum Empfangen von Daten verwendet wird.

## <a name="syntax"></a>Syntax


```CSharp
public System.String sourceProtocol {get; set;}
```


```VB

Public ReadOnly Property sourceProtocol As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.String,** die der Name des Quellprotokolls ist.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ruft eine Zeichenfolge der Länge 0 ("") ab, wenn eine CD oder DVD wiedergibt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **sourceProtocol** verwendet, um das Quellprotokoll anzuzeigen, das zum Empfangen von Daten verwendet wird. Die Informationen werden als Reaktion auf das **PlayStateChange-Ereignis** in einer Bezeichnung angezeigt. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the network source protocol when the player is playing by testing for a 
    // play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3. 
    if (e.newState == 3) 
    {
        sourceProtocolLabel.Text = ("Source protocol: " + player.network.sourceProtocol);
    } 
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the network source protocol when the player is playing by testing for a 
    &#39; play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3.
    If (e.newState = 3) Then

        sourceProtocolLabel.Text = (&quot;Source protocol: &quot; + player.network.sourceProtocol)

    End If

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

[**IWMPNetwork-Schnittstelle (VB und C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





