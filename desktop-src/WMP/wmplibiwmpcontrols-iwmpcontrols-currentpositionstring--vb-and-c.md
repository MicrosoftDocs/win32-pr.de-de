---
title: Iwmpcontrols currentpositionstring (Eigenschaft)
description: Die currentpositionstring-Eigenschaft ruft die aktuelle Position im Medien Element als Zeichenfolge ab, die als hh mm SS (Stunden, Minuten und Sekunden) formatiert ist.
ms.assetid: cd28dafa-b6a4-4bed-aa5d-7e7be6af1426
keywords:
- currentpositionstring-Eigenschaft, Windows-Media Player
- currentpositionstring-Eigenschaft, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, currentpositionstring (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPControls.currentPositionString
- IWMPControls.get_currentPositionString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e941fceb61e4f00393b05f96489ec7ac8e950f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370316"
---
# <a name="iwmpcontrolscurrentpositionstring-property"></a>Iwmpcontrols:: currentpositionstring (Eigenschaft)

Die **currentpositionstring** -Eigenschaft ruft die aktuelle Position im Medien Element als Zeichenfolge ab, die als hh: mm: SS (Stunden, Minuten und Sekunden) formatiert ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.String currentPositionString {get;}
```


```VB

Public ReadOnly Property currentPositionString As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Ein formatiertes **System. String** -Wert, der die aktuelle Position ist.

## <a name="remarks"></a>Bemerkungen

Wenn das Medien Element weniger als eine Stunde lang ist, wird die aktuelle Position als mm: SS (Minuten und Sekunden) formatiert.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Timer gestartet, der ein Ereignis in Intervallen von einer Sekunde auslöst. Im Timer-Ereignishandler wird eine Bezeichnung mit **currentpositionstring** aktualisiert. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 
   
// Update the text of the label with the currentPositionString.
private void TimerEventProcessor(object sender, System.EventArgs e)
{
    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString;
}
```


```VB

' Set the timer to fire an event every second and start the timer.
timer.Interval = 1000
timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
&#39; determine when to start and stop the timer. 

&#39; Update the text of the label with the currentPositionString.
Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString

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

[**Iwmpcontrols-Schnittstelle (VB und c#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. CurrentPosition (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





