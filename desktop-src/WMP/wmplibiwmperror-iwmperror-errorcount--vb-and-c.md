---
title: Iwmperror errorCount (Eigenschaft)
description: Die errorCount-Eigenschaft ruft die Anzahl der Fehler in der Fehler Warteschlange ab.
ms.assetid: a30750c8-2025-4087-bd2b-f313ccbde38c
keywords:
- errorCount-Eigenschaft, Windows Media Player
- errorCount-Eigenschaft, Windows Media Player, iwmperror-Schnittstelle
- Iwmperror-Schnittstelle, Windows Media Player, errorCount (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPError.errorCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62c16f07260847c91f1c9f18885587444a4ceb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371308"
---
# <a name="iwmperrorerrorcount-property"></a>Iwmperror:: errorCount (Eigenschaft)

Die **errorCount** -Eigenschaft ruft die Anzahl der Fehler in der Fehler Warteschlange ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 errorCount {get; set;}
```


```VB

Public ReadOnly Property errorCount As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die Anzahl der Fehler ist.

## <a name="remarks"></a>Bemerkungen

Sie sollten **iwmpsettings. enableerrordialogs** auf **false** festlegen, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **errorCount** in einem Fehler Ereignishandler verwendet, um den Benutzer über den letzten Fehler in der Fehler Warteschlange zu benachrichtigen. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void player_ErrorEvent_errorCount(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Get the description of the last error. Error items start at zero,
    // so the item index will always be one less than the error count.
    string errDesc = player.Error.get_Item(max-1).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorCount(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Get the description of the last error. Error items start at zero,
    &#39; so the item index will always be one less than the error count.
    Dim errDesc As String = player.Error.Item(max - 1).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

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

[**Iwmpsettings. enableerrordialogs (VB und c#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





