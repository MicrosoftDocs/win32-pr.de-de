---
title: Iwmperror. Item (VB und C)
description: Die Item-Eigenschaft (die get \_ Item-Methode in C \) Ruft eine iwmperroritem-Schnittstelle am angegebenen Index in der Fehler Warteschlange ab.
ms.assetid: acfaaaa5-eb13-4ba0-8417-4229adc62c5d
keywords:
- Iwmperror. Item (VB und C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPError.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9217ec772512171c828dd0dad06ec8fe3704dba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370149"
---
# <a name="iwmperroritem-vb-and-c"></a>Iwmperror. Item (VB und c#)

Die **Item** -Eigenschaft (die **get \_ Item** -Methode in c#) Ruft eine **iwmperroritem** -Schnittstelle am angegebenen Index in der Fehler Warteschlange ab.


```
[Visual Basic]
ReadOnly Property Item(
  dwIndex As System.Integer
) As IWMPErrorItem
```




```
[C#]
IWMPErrorItem get_Item (
  System.Int32 dwIndex
);
```



## <a name="parameters"></a>Parameter

*dwIndex*

Ein **System. Int32** -Wert, der der null basierte Index einer **iwmperroritem** -Schnittstelle in der Fehler Warteschlange ist.

## <a name="property-value"></a>Eigenschaftswert

Eine **WMPLib. iwmperroritem** -Schnittstelle.

## <a name="remarks"></a>Bemerkungen

Windows Media Player kann als Reaktion auf eine Fehlerbedingung eine Reihe von Fehlern generieren. Diese Eigenschaft ruft einen bestimmten Fehler in der Warteschlange mit einer Indexnummer ab. Die Indexnummern für die Fehler Warteschlange beginnen mit 0 (null).

Sie sollten **iwmpsettings. enableerrordialogs** auf **false** festlegen, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die **Item** -Eigenschaft (die **get \_ Item** -Methode in c#) in einem Fehler Ereignishandler verwendet, um Informationen zum letzten Fehler in der Fehler Warteschlange abzurufen und anzuzeigen. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void player_ErrorEvent_get_Item(object sender, System.EventArgs e)
{
    // Store the index of the most recent error.
    int max = (player.Error.errorCount - 1);

    // Get an interface for the most recent error item. Cast it to
    // a WMPLib.IWMPErrorItem2 interface to get all of the available functionality.
    WMPLib.IWMPErrorItem2 errItem = (WMPLib.IWMPErrorItem2)player.Error.get_Item(max);

    // Use the interface to access and store the error info.
    int errNum = errItem.errorCode;
    string errDesc = errItem.errorDescription;

    // Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + ":  " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_get_Item(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the index of the most recent error.
    Dim max As Integer = (player.Error.errorCount - 1)

    &#39; Get an interface for the most recent error item. 
    Dim errItem As WMPLib.IWMPErrorItem2 = player.Error.Item(max)

    &#39; Use the interface to access and store the error info.
    Dim errNum As Integer = errItem.errorCode
    Dim errDesc As String = errItem.errorDescription

    &#39; Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + &quot;:  &quot; + errDesc)

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

[**Iwmperror-Schnittstelle (VB und c#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**Iwmperroritem-Schnittstelle (VB und c#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. enableerrordialogs (VB und c#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





