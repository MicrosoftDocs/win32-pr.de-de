---
title: ErrorCode-Eigenschaft "IWMPErrorItem"
description: Die errorCode-Eigenschaft ruft den aktuellen Fehlercode ab.
ms.assetid: 00719067-685d-4ef2-9eec-72c7892fcdb9
keywords:
- errorCode-Eigenschaft Windows Media Player
- errorCode-Eigenschaft Windows Media Player , IWMPErrorItem-Schnittstelle
- IWMPErrorItem-Schnittstelle Windows Media Player , errorCode-Eigenschaft
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
ms.openlocfilehash: 9d7179684fb0332e25716282adfd47a5f769493f646f73c82d0391bbce4e6a91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031210"
---
# <a name="iwmperroritemerrorcode-property"></a>IWMPErrorItem::errorCode-Eigenschaft

Die **errorCode-Eigenschaft** ruft den aktuellen Fehlercode ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 errorCode {get; set;}
```


```VB

Public ReadOnly Property errorCode As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.Int32,die** der Fehlercode ist.

## <a name="remarks"></a>Hinweise

Sie sollten **IWMPSettings.enableErrorDialogs** auf **FALSE** festlegen, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **errorCode** in einem Error-Ereignishandler verwendet, um dem Benutzer den Fehlercode anzuzeigen. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPErrorItem-Schnittstelle (VB und C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.enableErrorDialogs (VB und C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





