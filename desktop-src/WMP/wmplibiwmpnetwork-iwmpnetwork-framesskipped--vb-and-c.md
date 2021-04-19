---
title: Iwmpnetwork-framesskipped (Eigenschaft)
description: Die framesskipped-Eigenschaft ruft die Gesamtanzahl der Frames ab, die während der Wiedergabe übersprungen wurden.
ms.assetid: eedecfa9-0c82-4800-979e-ca85fb78c480
keywords:
- Eigenschaften Fenster für "framesskipped" Media Player
- framesskipped-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, framesskipped (Eigenschaft)
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
ms.openlocfilehash: 8409cec50089111184f96e4463f57cc9c4fbae07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366699"
---
# <a name="iwmpnetworkframesskipped-property"></a>Iwmpnetwork:: framesskipped (Eigenschaft)

Die **framesskipped** -Eigenschaft ruft die Gesamtanzahl der Frames ab, die während der Wiedergabe übersprungen wurden.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 framesSkipped {get; set;}
```


```VB

Public ReadOnly Property framesSkipped As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die Anzahl der übersprungenen Frames ist.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **framesskipped** verwendet, um die Gesamtzahl der Rahmen anzuzeigen, die während der Wiedergabe ausgelassen wurden. Die Informationen werden in einer Bezeichnung angezeigt, wenn der Benutzer auf eine Schaltfläche klickt. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpnetwork-Schnittstelle (VB und c#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





