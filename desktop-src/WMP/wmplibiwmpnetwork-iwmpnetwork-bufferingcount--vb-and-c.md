---
title: Iwmpnetwork bufferingcount (Eigenschaft)
description: Die bufferingcount-Eigenschaft ruft die Häufigkeit ab, mit der die Pufferung während der Wiedergabe aufgetreten ist.
ms.assetid: 2e3a2914-fc38-4477-8c4c-15b4a2e424dc
keywords:
- bufferingcount-Eigenschaft, Windows-Media Player
- bufferingcount-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, bufferingcount (Eigenschaft)
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
ms.openlocfilehash: f4958892dd9784ee72b51adfedbbcdee81817b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373660"
---
# <a name="iwmpnetworkbufferingcount-property"></a>Iwmpnetwork:: bufferingcount (Eigenschaft)

Die **bufferingcount** -Eigenschaft ruft die Häufigkeit ab, mit der die Pufferung während der Wiedergabe aufgetreten ist.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 bufferingCount {get; set;}
```


```VB

Public ReadOnly Property bufferingCount As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die Puffer Anzahl ist.

## <a name="remarks"></a>Bemerkungen

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf Null zurückgesetzt. Wenn die Wiedergabe angehalten wird, wird Sie nicht zurückgesetzt.

Die Pufferung gilt nur für Streaminginhalte. Diese Eigenschaft ruft nur während der Laufzeit gültige Informationen ab, wenn die URL für die Wiedergabe mithilfe der **AxWindowsMediaPlayer. URL** -Eigenschaft festgelegt wird.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird *bufferingcount* verwendet, um anzuzeigen, wie oft Pufferung während der Wiedergabe auftritt. Die Informationen werden in einer Bezeichnung als Reaktion auf das Puffer Ereignis angezeigt. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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

 

 





