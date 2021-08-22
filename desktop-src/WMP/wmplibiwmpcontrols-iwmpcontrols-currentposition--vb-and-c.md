---
title: IWMPControls currentPosition-Eigenschaft
description: Die currentPosition-Eigenschaft ruft die aktuelle Position im Medienelement in Sekunden ab dem Anfang ab oder legt diese fest.
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- currentPosition-Eigenschaft Windows Media Player
- currentPosition-Eigenschaft Windows Media Player , IWMPControls-Schnittstelle
- IWMPControls-Schnittstelle Windows Media Player , currentPosition-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPControls.currentPosition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8eca861240256899fa19513fc1fb64cd540d47acb213f718674ebbda2d5f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053668"
---
# <a name="iwmpcontrolscurrentposition-property"></a>IWMPControls::currentPosition-Eigenschaft

Die **currentPosition-Eigenschaft** ruft die aktuelle Position im Medienelement in Sekunden ab dem Anfang ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.Double-Datei,** die die aktuelle Position ist.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **currentPosition** verwendet, um nach einer vom Benutzer angegebenen Position zu suchen. Als Reaktion auf einen **Schaltflächenklick** wird currentPosition auf den Wert festgelegt, der in ein Textfeld namens newPosition eingegeben wurde. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
private void setPosition_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text);
}
```


```VB

Public Sub setPosition_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setPosition.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text)

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

[**IWMPControls-Schnittstelle (VB und C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.currentPositionString (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 





