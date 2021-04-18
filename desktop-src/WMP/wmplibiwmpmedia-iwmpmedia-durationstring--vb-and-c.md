---
title: Iwmpmedia durationString-Eigenschaft
description: Die durationString-Eigenschaft ruft eine Zeichenfolge ab, die die Dauer des aktuellen Medien Elements im hh mm ss-Format angibt.
ms.assetid: de33c737-d73e-41f0-9c1b-944279194738
keywords:
- durationString-Eigenschaft, Fenster Media Player
- durationString-Eigenschaft, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, durationString (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPMedia.durationString
- IWMPMedia.get_durationString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e6bc732388036aa9e79aeedd988de94fa263bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358746"
---
# <a name="iwmpmediadurationstring-property"></a>Iwmpmedia::d urationstring-Eigenschaft

Die **durationString** -Eigenschaft ruft eine Zeichenfolge ab, die die Dauer des aktuellen Medien Elements im Format "hh: mm: SS" angibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.String durationString {get;}
```


```VB

Public ReadOnly Property durationString As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. String** -Wert, der die Dauer ist.

## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft mit einem anderen als dem in AxWindowsMediaPlayer. currentMedia angegebenen Medien Element verwendet wird, enthält Sie möglicherweise keinen gültigen Wert. Wenn das Medien Element weniger als eine Stunde lang ist, wird der Stunden Teil des Rückgabewerts ausgelassen.

Vor der Verwendung dieser Eigenschaft müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **durationString** verwendet, um die Dauer des aktuellen Medien Elements als formatierten Text in einer Bezeichnung anzuzeigen. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Display the formatted duration string in the label.
         mediaDuration.Text = player.currentMedia.durationString;
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = 13) Then

        &#39; Display the formatted duration string in the label.
        mediaDuration.Text = player.currentMedia.durationString

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

[**AxWindowsMediaPlayer. currentMedia (VB und c#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. Duration (VB und c#)**](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)
</dt> </dl>

 

 





