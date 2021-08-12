---
title: IWMPError.Item (VB und C )
description: Die Item-Eigenschaft (die get Item-Methode in C\ ) ruft eine IWMPErrorItem-Schnittstelle am angegebenen Index \_ in der Fehlerwarteschlange ab.
ms.assetid: acfaaaa5-eb13-4ba0-8417-4229adc62c5d
keywords:
- IWMPError.Item (VB und C ) Windows Media Player
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
ms.openlocfilehash: be8d212eca9e9e54770e7e2751df345d80bbfb6bfc1b12714e811c7795990725
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575632"
---
# <a name="iwmperroritem-vb-and-c"></a>IWMPError.Item (VB und C#)

Die **Item-Eigenschaft** (die **get \_ Item-Methode** in C#) ruft eine **IWMPErrorItem-Schnittstelle** am angegebenen Index in der Fehlerwarteschlange ab.


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

Ein **System.Int32,** das der nullbasierte Index einer **IWMPErrorItem-Schnittstelle** in der Fehlerwarteschlange ist.

## <a name="property-value"></a>Eigenschaftswert

Eine **WMPLib.IWMPErrorItem-Schnittstelle.**

## <a name="remarks"></a>Hinweise

Windows Media Player kann eine Reihe von Fehlern als Reaktion auf eine Fehlerbedingung generieren. Diese Eigenschaft ruft mithilfe einer Indexnummer einen bestimmten Fehler in der Warteschlange ab. Die Indexnummern für die Fehlerwarteschlange beginnen mit 0 (null).

Sie sollten **IWMPSettings.enableErrorDialogs** auf **FALSE** festlegen, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die **Item-Eigenschaft** (die **get \_ Item-Methode** in C#) in einem Error-Ereignishandler verwendet, um Informationen zum letzten Fehler in der Fehlerwarteschlange abzurufen und anzuzeigen. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPError-Schnittstelle (VB und C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**IWMPErrorItem-Schnittstelle (VB und C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.enableErrorDialogs (VB und C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





