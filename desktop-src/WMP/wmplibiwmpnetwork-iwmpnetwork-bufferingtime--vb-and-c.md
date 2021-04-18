---
title: Iwmpnetwork BufferingTime (Eigenschaft)
description: Die BufferingTime-Eigenschaft ruft die Zeitspanne in Millisekunden ab, die zum Puffern eingehender Daten vor Beginn der Wiedergabe reserviert wird, oder legt Sie fest.
ms.assetid: b5936b21-a17b-4801-a5fc-c6d6521e05aa
keywords:
- BufferingTime-Eigenschaft, Windows-Media Player
- BufferingTime-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, BufferingTime (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8594d53797b028dd74a8ef11cb8f2fa64b3654cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352828"
---
# <a name="iwmpnetworkbufferingtime-property"></a>Iwmpnetwork:: BufferingTime (Eigenschaft)

Die **BufferingTime** -Eigenschaft ruft die Zeitspanne in Millisekunden ab, die zum Puffern eingehender Daten vor Beginn der Wiedergabe reserviert wird, oder legt Sie fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 bufferingTime {get; set;}
```


```VB

Public Property bufferingTime As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die Pufferzeit in Millisekunden angibt, die zwischen 0 und 60.000 und dem Standardwert 5.000 liegt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **BufferingTime** verwendet, um die Anzahl der Sekunden anzugeben, die für die Pufferung eingehender Daten reserviert werden. Ein Textfeld ermöglicht dem Benutzer, einen neuen Wert für **BufferingTime** einzugeben, und die-Eigenschaft wird als Reaktion auf das Click-Ereignis einer Schaltfläche aktualisiert. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void setBufTime_Click(object sender, System.EventArgs e)
{
    // Retrieve input from the user and convert it to an integer.
    int newTime = System.Convert.ToInt32(bufText.Text);

    // Test whether the integer is within the valid range. 
    if (newTime >= 0 & newTime <= 60) 
    {
        // Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000);
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("Buffering time must be between 0 and 60.");
    }
}
```


```VB

Public Sub setBufTime_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setBufTime.Click

    &#39; Retrieve input from the user and convert it to an integer.
    Dim newTime As Integer = System.Convert.ToInt32(bufText.Text)

    &#39; Test whether the integer is within the valid range. 
    If (newTime >= 0 And newTime <= 60) Then

        &#39; Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000)

    Else

        System.Windows.Forms.MessageBox.Show(&quot;Buffering time must be between 0 and 60.&quot;)

    End If

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
</dt> </dl>

 

 





