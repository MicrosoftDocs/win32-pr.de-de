---
title: Iwmpnetwork, lostpakete (Eigenschaft)
description: Die lostpaketen-Eigenschaft ruft die Anzahl der verlorenen Pakete ab.
ms.assetid: 611218d3-c4d3-4d4e-835c-1e7a956b2718
keywords:
- Eigenschaften Fenster von "lostpakete" Media Player
- lostpaketen-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, lostpakete (Eigenschaft)
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
ms.openlocfilehash: cd1adac5f4aa8b1f58c023a556af04b8eae4bd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361337"
---
# <a name="iwmpnetworklostpackets-property"></a>Iwmpnetwork:: lostpakete (Eigenschaft)

Die **lostpaketen** -Eigenschaft ruft die Anzahl der verlorenen Pakete ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 lostPackets {get; set;}
```


```VB

Public ReadOnly Property lostPackets As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die Anzahl verlorener Pakete ist.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft umfasst nur das Streaming von Medien Paketen und gibt 0 (null) zurück, wenn das HTTP-Protokoll verwendet wird, das verlustfrei ist.

Pakete können aus verschiedenen Gründen verloren gehen, z. b. Art und Qualität der Netzwerkverbindung.

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf Null zurückgesetzt. Der Wert wird nicht zurückgesetzt, wenn die Wiedergabe angehalten wurde. Diese Eigenschaft ruft nur während der Laufzeit gültige Informationen ab, wenn die URL für die Wiedergabe mithilfe der **AxWindowsMediaPlayer. URL** -Eigenschaft festgelegt wird.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **lostpakete** verwendet, um die Gesamtanzahl der während der Wiedergabe verlorenen Pakete anzuzeigen. Die Informationen werden in einer Bezeichnung angezeigt, wenn der Benutzer auf eine Schaltfläche klickt. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpnetwork-Schnittstelle (VB und c#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB und c#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> </dl>

 

 





