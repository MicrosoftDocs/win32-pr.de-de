---
title: Iwmpcontrols currentmarker (Eigenschaft)
description: Die currentmarker-Eigenschaft ruft die aktuelle Markernummer ab oder legt Sie fest.
ms.assetid: faf8c32a-66de-47ce-aa3d-6699d9f9bdda
keywords:
- currentmarker-Eigenschaft, Fenster Media Player
- currentmarker-Eigenschaft, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, currentmarker (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPControls.currentMarker
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfbcea42594b15b8da08248d38b5d8f72a1de29d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372459"
---
# <a name="iwmpcontrolscurrentmarker-property"></a>Iwmpcontrols:: currentmarker (Eigenschaft)

Die **currentmarker** -Eigenschaft ruft die aktuelle Markernummer ab oder legt Sie fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 currentMarker {get; set;}
```


```VB

Public Property currentMarker As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die Markernummer ist.

## <a name="remarks"></a>Bemerkungen

Das Festlegen von **currentmarker** bewirkt, dass die Wiedergabe vom angegebenen Marker gestartet wird. Stellen Sie vor dem Festlegen von **currentmarker** fest, ob eine Datei Marker hat und wie viele diese mithilfe von **iwmpmedia. markercount** hat. Wenn eine Datei keine Marker hat, führt die Festlegung von **currentmarker** auf alles, aber auf 0 (null) zu einem Fehler. Wenn **currentmarker** auf eine Zahl höher als **markercount** festgelegt wird, führt dies ebenfalls zu einem Fehler.

Die **currentmarker** -Eigenschaft gibt immer den aktuellen oder den letzten Marker zurück. Dies bedeutet, dass sich die tatsächliche Dateiposition entweder am aktuellen Marker oder vor dem nächsten Marker befinden kann. Marker werden beginnend mit 1 nummeriert. Wenn also eine Datei Marker enthält, können Sie **currentmarker** auf NULL festlegen, um die Dateiposition in NULL zu ändern.

Bis das aktuelle Medien Element festgelegt ist (mithilfe von **AxWindowsMediaPlayer. URL** oder **AxWindowsMediaPlayer. currentMedia**), gibt **currentmarker** 0 (null) zurück.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **currentmarker** verwendet, um die Videowiedergabe von dem Marker zu starten, der der SelectedIndex-Eigenschaft eines Listen Felds entspricht, das mit markerbezeichlern gefüllt wurde. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Fill the list box with the marker identifiers of the current media item.
markers.Items.Add("Begining");
markers.Items.Add("Sunrise");
markers.Items.Add("Car chase");
markers.Items.Add("Happy ending");

// Set the currentMarker to the marker selected from the list box.
private void markers_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedMarker = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    player.Ctlcontrols.currentMarker = selectedMarker;
}
```


```VB

' Fill the list box with the marker identifiers of the current media item.
markers.Items.Add(&quot;Begining&quot;)
markers.Items.Add(&quot;Sunrise&quot;)
markers.Items.Add(&quot;Car chase&quot;)
markers.Items.Add(&quot;Happy ending&quot;)

&#39; Set the currentMarker to the marker selected from the list box.
Public Sub markers_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles markers.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedMarker As Integer = lb.SelectedIndex

    player.Ctlcontrols.currentMarker = selectedMarker

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

[**AxWindowsMediaPlayer. currentMedia (VB und c#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB und c#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols-Schnittstelle (VB und c#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. markercount (VB und c#)**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





