---
title: Eigenschaften von iwmpcontrols-Eigenschaften
description: Mit der Eigenschaft "ustitem" wird das aktuelle Medien Element in einer Wiedergabeliste abgerufen oder festgelegt.
ms.assetid: 0a331b1f-95bd-48ea-b951-1ca35cc96865
keywords:
- Eigenschaften Fenster für "Eigenschaften" Media Player
- Eigenschaft "Eigenschaften" Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, Eigenschaft "Impact Item"
topic_type:
- apiref
api_name:
- IWMPControls.currentItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae04eb333e2fd347fa6f88b33ec2482a4dd8fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358750"
---
# <a name="iwmpcontrolscurrentitem-property"></a>Iwmpcontrols:: accesstitem (Eigenschaft)

Mit der Eigenschaft " **ustitem** " wird das aktuelle Medien Element in einer Wiedergabeliste abgerufen oder festgelegt.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPMedia currentItem {get; set;}
```


```VB

Public Property currentItem As IWMPMedia
```





## <a name="property-value"></a>Eigenschaftswert

Eine **WMPLib. iwmpmedia** -Schnittstelle, die das Medien Element darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft funktioniert nur mit Elementen in der aktuellen Wiedergabeliste. Das Festlegen von " **ustitem** " auf die Schnittstelle eines gespeicherten Medien Elements wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das aktuelle Medien Element des Players mithilfe von " **ustitem** " auf ein aus einem Listenfeld ausgewähltes Element festgelegt. Das Listenfeld wurde mit allen Elementen in der aktuellen Wiedergabeliste gefüllt. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void playItem_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedItem = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop();

    // Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.get_Item(selectedItem);
    
    // Play the current item.
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playItem_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles playItem.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedItem As Integer = lb.SelectedIndex

    &#39; Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop()

    &#39; Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.Item(selectedItem)

    &#39; Play the current item.
    player.Ctlcontrols.play()

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

[**Iwmpcontrolsinterface (VB und c#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Iwmpmediainterface (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection. getByName (VB und c#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





