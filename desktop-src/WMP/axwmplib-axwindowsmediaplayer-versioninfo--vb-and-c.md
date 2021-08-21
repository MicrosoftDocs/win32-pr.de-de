---
title: AxWindowsMediaPlayer.versionInfo-Eigenschaft
description: Die versionInfo-Eigenschaft ruft einen Wert ab, der die Version des Windows Media Player angibt.
ms.assetid: e128bec5-1ae9-4710-800e-4f97df362909
keywords:
- versionInfo-Eigenschaft Windows Media Player
- versionInfo-Eigenschaft Windows Media Player , AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse Windows Media Player , versionInfo-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.versionInfo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fd7491af0fc102f03da9855b78ecef79ac0a09ca9b3ab8b49f9bf6b948f0d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118841161"
---
# <a name="axwindowsmediaplayerversioninfo-property"></a>AxWindowsMediaPlayer.versionInfo-Eigenschaft

Die versionInfo-Eigenschaft ruft einen Wert ab, der die Version des Windows Media Player angibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.String versionInfo {get;}
```


```VB

Public ReadOnly Property versionInfo As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Eine System.String, bei der es sich um versionsinformationen im folgenden Format handelt: "*X*.0.0. *YYYY*", wobei *X* die Hauptversionsnummer und *YYYY* die Buildnummer darstellt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Schaltfläche erstellt, die beim Klicken ein Meldungsfeld mit den Versionsinformationen für Windows Media Player anzeigt. Das AxWMPLib.AxWindowsMediaPlayer-Objekt wird durch die Variable player dargestellt.


```CSharp
private void showVersion_Click(object sender, System.EventArgs e)
{
    // Build the message containing the version info. 
    string message = ("Windows Media Player Version: " + player.versionInfo);

    // Display the message. 
    System.Windows.Forms.MessageBox.Show(message);
}
```


```VB

Public Sub showVersion_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showVersion.Click

    &#39; Build the message containing the version info. 
    Dim message As String = (&quot;Windows Media Player Version: &quot; + player.versionInfo)

    &#39; Display the message. 
    System.Windows.Forms.MessageBox.Show(message)

End Sub
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





