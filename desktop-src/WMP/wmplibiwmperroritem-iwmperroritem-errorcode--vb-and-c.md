---
title: Iwmperroritem ErrorCode-Eigenschaft
description: Die ErrorCode-Eigenschaft ruft den aktuellen Fehlercode ab.
ms.assetid: 00719067-685d-4ef2-9eec-72c7892fcdb9
keywords:
- Eigenschaften Fenster für ErrorCode-Eigenschaft Media Player
- ErrorCode-Eigenschaft, Windows Media Player, iwmperroritem-Schnittstelle
- Iwmperroritem-Schnittstelle Windows Media Player, ErrorCode-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorCode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f284d5655fc1f4007695a1f681c744a9c5c6fc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365646"
---
# <a name="iwmperroritemerrorcode-property"></a>Iwmperroritem:: ErrorCode-Eigenschaft

Die **errorCode** -Eigenschaft ruft den aktuellen Fehlercode ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 errorCode {get; set;}
```


```VB

Public ReadOnly Property errorCode As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** , das den Fehlercode ist.

## <a name="remarks"></a>Bemerkungen

Sie sollten **iwmpsettings. enableerrordialogs** auf **false** festlegen, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **errorCode** in einem Fehler Ereignishandler verwendet, um den Fehlercode für den Benutzer anzuzeigen. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void player_ErrorEvent_errorCode(object sender, System.EventArgs e)
{
    // Get the error code for the first error item.
    int errCode = player.Error.get_Item(0).errorCode;

    // Display the error code.
    System.Windows.Forms.MessageBox.Show("Error number: " + errCode.ToString());
}
```


```VB

Public Sub player_ErrorEvent_errorCode(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error code for the first error item.
    Dim errCode As Integer = player.Error.Item(0).errorCode

    &#39; Display the error code.
    System.Windows.Forms.MessageBox.Show(&quot;Error number: &quot; + errCode.ToString())

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

[**Iwmperroritem-Schnittstelle (VB und c#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. enableerrordialogs (VB und c#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





