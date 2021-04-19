---
title: Iwmperroritem ErrorDescription-Eigenschaft
description: Die ErrorDescription-Eigenschaft ruft eine Beschreibung des Fehlers ab.
ms.assetid: a9914c24-1d10-422a-bcba-80be9fb85108
keywords:
- ErrorDescription-Eigenschaft, Windows-Media Player
- ErrorDescription-Eigenschaft, Windows Media Player, iwmperroritem-Schnittstelle
- Iwmperroritem-Schnittstelle Windows Media Player, ErrorDescription-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8725099d1ce49eae8f378b2571dc4030f60611e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373970"
---
# <a name="iwmperroritemerrordescription-property"></a>Iwmperroritem:: ErrorDescription-Eigenschaft

Die **ErrorDescription** -Eigenschaft ruft eine Beschreibung des Fehlers ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.String errorDescription {get; set;}
```


```VB

Public ReadOnly Property errorDescription As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. String** -Wert, der die Fehlerbeschreibung ist.

## <a name="remarks"></a>Bemerkungen

Sie sollten **iwmpsettings. enableerrordialogs** auf **false** festlegen, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **ErrorDescription** in einem Fehler Ereignishandler verwendet, um die Fehlerbeschreibung für den Benutzer anzuzeigen. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void player_ErrorEvent_errorDescription(object sender, System.EventArgs e)
{
    // Get the error description for the first error item.
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show("Error: " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorDescription(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error description for the first error item.
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(&quot;Error: &quot; + errDesc)

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

 

 





