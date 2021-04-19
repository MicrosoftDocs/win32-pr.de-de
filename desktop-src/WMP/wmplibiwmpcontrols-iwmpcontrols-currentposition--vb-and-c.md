---
title: Iwmpcontrols CurrentPosition (Eigenschaft)
description: Die CurrentPosition-Eigenschaft ruft die aktuelle Position im Medien Element in Sekunden ab oder legt diese fest.
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- CurrentPosition-Eigenschaft, Fenster Media Player
- CurrentPosition-Eigenschaft, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, CurrentPosition (Eigenschaft)
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
ms.openlocfilehash: fee8c2c8244d6034069f21033978ce2883ff852d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370808"
---
# <a name="iwmpcontrolscurrentposition-property"></a>Iwmpcontrols:: CurrentPosition (Eigenschaft)

Die **CurrentPosition** -Eigenschaft ruft die aktuelle Position im Medien Element in Sekunden ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Double** -Wert, der die aktuelle Position ist.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **CurrentPosition** verwendet, um eine vom Benutzer bereitgestellte Position zu suchen. Als Reaktion auf einen Klick auf eine Schaltfläche wird **CurrentPosition** auf den Wert festgelegt, der in einem Textfeld mit dem Namen newPosition eingegeben wurde. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcontrols-Schnittstelle (VB und c#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. currentpositionstring (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 





