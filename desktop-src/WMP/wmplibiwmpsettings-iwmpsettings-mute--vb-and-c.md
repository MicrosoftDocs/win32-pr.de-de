---
title: Iwmpsettings-Eigenschaft stumm schalten
description: Mit der Eigenschaft stumm wird ein Wert abgerufen oder festgelegt, der angibt, ob Audiodaten stumm sind
ms.assetid: d99e47db-70cc-41e0-aca9-b765b075e7b4
keywords:
- Eigenschaften Fenster Media Player stumm schalten
- stumm Eigenschaften Fenster Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows Media Player, Eigenschaft stumm schalten
topic_type:
- apiref
api_name:
- IWMPSettings.mute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67518bb9a6eccee13e4cc262f37341d30689439e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374039"
---
# <a name="iwmpsettingsmute-property"></a>Iwmpsettings:: stumm (Eigenschaft)

Mit der Eigenschaft **stumm** wird ein Wert abgerufen oder festgelegt, der angibt, ob Audiodaten stumm sind

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean mute {get; set;}
```


```VB

Public Property mute As System.Boolean
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Boolean** -Wert, der angibt, ob Audiodaten stumm geschaltet werden. Der Standardwert ist **FALSE**.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Kontrollkästchen erstellt, und die **stumm** Eigenschaft wird zum stumm schalten und Aufheben der stumm Schaltung gewechselt, wenn der aktivierte Zustand des Felds geändert wird. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void Mute_CheckStateChanged(object sender, System.EventArgs e)
{
    System.Windows.Forms.CheckBox Mute = (System.Windows.Forms.CheckBox)sender;

    // Change the check box text depending on the checked state.
    Mute.Text = Mute.Checked ? "Un-mute Audio" : Mute.Text = "Mute Audio";

    // Use the checked state to set the mute property. 
    player.settings.mute = Mute.Checked;
}
```


```VB

Public Sub Mute_CheckStateChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles Mute.CheckStateChanged

    Dim cb As System.Windows.Forms.CheckBox = sender

    &#39;  Change the check box text depending on the checked state.
    If (cb.Checked) Then

        cb.Text = &quot;Un-mute Audio&quot;

    Else

        cb.Text = &quot;Mute Audio&quot;

    End If

    &#39;  Use the checked state to set the mute property. 
    player.settings.mute = cb.Checked

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

[**Iwmpsettings-Schnittstelle (VB und c#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. Rate (VB und c#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





