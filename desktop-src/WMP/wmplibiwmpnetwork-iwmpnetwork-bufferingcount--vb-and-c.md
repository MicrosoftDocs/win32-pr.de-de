---
title: IWMPNetwork bufferingCount-Eigenschaft
description: Die bufferingCount-Eigenschaft ruft ab, wie oft die Pufferung während der Wiedergabe erfolgt ist.
ms.assetid: 2e3a2914-fc38-4477-8c4c-15b4a2e424dc
keywords:
- bufferingCount-Eigenschaft Windows Media Player
- bufferingCount-Eigenschaft Windows Media Player , IWMPNetwork-Schnittstelle
- IWMPNetwork-Schnittstelle Windows Media Player , bufferingCount-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b69169e950cf3794d613bfd1d79d4953ce8f8a8bb01efe9ff17d6fa5961071
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899970"
---
# <a name="iwmpnetworkbufferingcount-property"></a>IWMPNetwork::bufferingCount-Eigenschaft

Die **bufferingCount-Eigenschaft** ruft ab, wie oft die Pufferung während der Wiedergabe erfolgt ist.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 bufferingCount {get; set;}
```


```VB

Public ReadOnly Property bufferingCount As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Int32,** bei dem es sich um die Pufferanzahl handelt.

## <a name="remarks"></a>Hinweise

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf 0 (null) zurückgesetzt. Sie wird nicht zurückgesetzt, wenn die Wiedergabe angehalten wird.

Die Pufferung gilt nur für Streaminginhalte. Diese Eigenschaft ruft gültige Informationen nur während der Laufzeit ab, wenn die URL für die Wiedergabe mithilfe der **AxWindowsMediaPlayer.URL-Eigenschaft** festgelegt wird.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird *bufferingCount* verwendet, um die Anzahl der Pufferungen während der Wiedergabe anzuzeigen. Die Informationen werden als Reaktion auf das Pufferereignis in einer Bezeichnung angezeigt. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Display the bufferingCount when buffering has started.
    if (e.start == true)
    {
        bufferingCountLabel.Text = ("Buffering count: " + player.network.bufferingCount);
    }  
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Display the bufferingCount when buffering has started.
    If (e.start = True) Then

        bufferingCountLabel.Text = (&quot;Buffering count: &quot; + player.network.bufferingCount)

    End If

End Sub
```





## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer.URL (VB und C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork-Schnittstelle (VB und C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





