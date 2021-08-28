---
title: IWMPNetwork lostPackets (Eigenschaft)
description: Die lostPackets-Eigenschaft ruft die Anzahl verlorener Pakete ab.
ms.assetid: 611218d3-c4d3-4d4e-835c-1e7a956b2718
keywords:
- lostPackets-Windows Media Player
- lostPackets-Eigenschaft Windows Media Player , IWMPNetwork-Schnittstelle
- IWMPNetwork-Schnittstelle Windows Media Player , lostPackets-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPNetwork.lostPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a60c85920d647f99ed8ba8478da51183c3ba63efa733c0bc627c16b040b70965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745911"
---
# <a name="iwmpnetworklostpackets-property"></a>IWMPNetwork::lostPackets-Eigenschaft

Die **lostPackets-Eigenschaft** ruft die Anzahl verlorener Pakete ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 lostPackets {get; set;}
```


```VB

Public ReadOnly Property lostPackets As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Int32,** das die Anzahl verloren gegangener Pakete ist.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft schließt nur Streamingmedienpakete ein und gibt bei Verwendung des verlustlosen HTTP-Protokolls null zurück.

Pakete können aus einer Reihe von Gründen verloren gehen, z. B. dem Typ und der Qualität der Netzwerkverbindung.

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf 0 (null) zurückgesetzt. Der Wert wird nicht zurückgesetzt, wenn die Wiedergabe angehalten wird. Diese Eigenschaft ruft gültige Informationen nur zur Laufzeit ab, wenn die URL für die Wiedergabe mithilfe der **AxWindowsMediaPlayer.URL-Eigenschaft festgelegt** wird.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **lostPackets verwendet,** um die Gesamtzahl der pakete anzuzeigen, die während der Wiedergabe verloren gegangen sind. Die Informationen werden in einer Bezeichnung angezeigt, wenn der Benutzer auf eine Schaltfläche klickt. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
private void showLostPackets_Click(object sender, System.EventArgs e)
{
    lostPacketsLabel.Text = ("Packets lost: " + player.network.lostPackets.ToString());
}
```


```VB

Public Sub showLostPackets_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showLostPackets.Click

    lostPacketsLabel.Text = (&quot;Packets lost: &quot; + player.network.lostPackets.ToString())

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

[**IWMPNetwork-Schnittstelle (VB und C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.URL (VB und C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> </dl>

 

 





