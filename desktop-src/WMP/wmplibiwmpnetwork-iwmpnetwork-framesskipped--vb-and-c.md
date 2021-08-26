---
title: IWMPNetwork framesSkipped-Eigenschaft
description: Die framesSkipped-Eigenschaft ruft die Gesamtanzahl von Frames ab, die während der Wiedergabe übersprungen wurden.
ms.assetid: eedecfa9-0c82-4800-979e-ca85fb78c480
keywords:
- framesSkipped-Eigenschaft Windows Media Player
- framesSkipped-Eigenschaft Windows Media Player , IWMPNetwork-Schnittstelle
- IWMPNetwork-Schnittstelle Windows Media Player , framesSkipped-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPNetwork.framesSkipped
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3640ff73eeadd1bf59eecc29045b0434f0885b7dc1eef319d6e6ee040442abdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999980"
---
# <a name="iwmpnetworkframesskipped-property"></a>IWMPNetwork::framesSkipped-Eigenschaft

Die **framesSkipped-Eigenschaft** ruft die Gesamtanzahl von Frames ab, die während der Wiedergabe übersprungen wurden.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 framesSkipped {get; set;}
```


```VB

Public ReadOnly Property framesSkipped As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Int32,** bei dem es sich um die Anzahl der übersprungenen Frames handelt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **framesSkipped** verwendet, um die Gesamtanzahl von Frames anzuzeigen, die während der Wiedergabe übersprungen wurden. Die Informationen werden in einer Bezeichnung angezeigt, wenn der Benutzer auf eine Schaltfläche klickt. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
private void showFramesSkipped_Click(object sender, System.EventArgs e)
{
    framesSkippedLabel.Text = ("Frames skipped: " + player.network.framesSkipped.ToString());
}
```


```VB

Public Sub showFramesSkipped_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showFramesSkipped.Click

    framesSkippedLabel.Text = (&quot;Frames skipped: &quot; + player.network.framesSkipped.ToString())

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
</dt> </dl>

 

 





