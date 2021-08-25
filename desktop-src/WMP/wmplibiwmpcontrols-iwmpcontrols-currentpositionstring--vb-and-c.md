---
title: IWMPControls currentPositionString (Eigenschaft)
description: Die currentPositionString-Eigenschaft ruft die aktuelle Position im Medienelement als als HH MM SS formatierte Zeichenfolge ab (Stunden, Minuten und Sekunden).
ms.assetid: cd28dafa-b6a4-4bed-aa5d-7e7be6af1426
keywords:
- currentPositionString-Windows Media Player
- currentPositionString-Eigenschaft Windows Media Player , IWMPControls-Schnittstelle
- IWMPControls-Schnittstelle Windows Media Player , currentPositionString-Eigenschaft
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
ms.openlocfilehash: 61e3c98937a12c145742895979ccccb8118f8349f82b2840c902dfe625ad0472
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861910"
---
# <a name="iwmpcontrolscurrentpositionstring-property"></a>IWMPControls::currentPositionString (Eigenschaft)

Die **currentPositionString-Eigenschaft** ruft die aktuelle Position im Medienelement als als HH:MM:SS formatierte Zeichenfolge ab (Stunden, Minuten und Sekunden).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.String currentPositionString {get;}
```


```VB

Public ReadOnly Property currentPositionString As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Ein **formatiertes System.String,** das die aktuelle Position ist.

## <a name="remarks"></a>Hinweise

Wenn das Medienelement weniger als eine Stunde lang ist, wird die aktuelle Position als MM:SS (Minuten und Sekunden) formatiert.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein Timer gestartet, der ein Ereignis in Intervallen von einer Sekunde auslöst. Im Timerereignishandler wird eine Bezeichnung mit **currentPositionString aktualisiert.** Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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

[**IWMPControls-Schnittstelle (VB und C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.currentPosition (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





