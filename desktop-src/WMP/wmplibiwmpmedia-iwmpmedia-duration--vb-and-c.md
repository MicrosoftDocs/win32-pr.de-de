---
title: IWMPMedia duration-Eigenschaft
description: Die duration-Eigenschaft ruft die Dauer des aktuellen Medienelements in Sekunden ab.
ms.assetid: f8a0bf3e-eeaf-46f5-90c8-d3b11ce4eb39
keywords:
- duration-Eigenschaft Windows Media Player
- duration-Eigenschaft Windows Media Player , IWMPMedia-Schnittstelle
- IWMPMedia-Schnittstelle Windows Media Player , duration-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPMedia.duration
- IWMPMedia.get_duration
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38703c37e73ba6312970b8e5b929441c3c5c9ccd1f034ab244dc97c36c2d2162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506020"
---
# <a name="iwmpmediaduration-property"></a>IWMPMedia::d uration-Eigenschaft

Die **duration-Eigenschaft** ruft die Dauer des aktuellen Medienelements in Sekunden ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.Double duration {get;}
```


```VB

Public ReadOnly Property duration As System.Double
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.Double-Datei,** die die Dauer in Sekunden ist.

## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft mit einem anderen Medienelement als dem in AxWindowsMediaPlayer.currentMedia angegebenen verwendet wird, enthält sie möglicherweise keinen gültigen Wert.

Um die Dauer für Dateien abzurufen, die sich nicht in der Bibliothek des Benutzers befinden, müssen Sie warten, bis Windows Media Player die Datei öffnet. Das bedeutet, dass der aktuelle **OpenState** gleich **MediaOpen** sein muss. Sie können dies überprüfen, indem Sie **axWindowsMediaPlayer behandeln. \_ WMPOCXEvents \_ OpenStateChange-Ereignis** oder durch regelmäßiges Überprüfen des Werts von **AxWindowsMediaPlayer.openState**.

Bei Wiedergabelisten kann die Dauer jedes Medienelements abgerufen werden, wenn das einzelne Medienelement geöffnet wird, anstatt die , wenn die Wiedergabeliste geöffnet wird.

Bevor Sie diese Eigenschaft verwenden können, benötigen Sie Lesezugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **duration** verwendet, um die verbleibende Zeit im aktuellen Medienelement in einer Bezeichnung anzuzeigen. Ein Timer aktualisiert den Text in der Bezeichnung jede Sekunde.


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 

private void TimerEventProcessor(object sender, System.EventArgs e)
{
    // Subtract the current position from the duration of the current media to get
    // the time remaining. Use the Math.floor method to round the result down to the
    // nearest whole number.
    double t = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition);

    // Display the time remaining in the current media.
    timeRemaining.Text = ("Seconds remaining: " + t.ToString());        
}
```


```VB

' Set the timer to fire an event every second and start the timer.
Timer.Interval = 1000
Timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a Select Case statement to
&#39; determine when to start and stop the timer. 

Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles Timer.Tick

    &#39; Subtract the current position from the duration of the current media to get
    &#39; the time remaining. Use the Math.Floor method to round the result down to the
    &#39; nearest whole number.
    Dim t As Double = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition)

    &#39; Display the time remaining in the current media.
    timeRemaining.Text = (&quot;Seconds remaining: &quot; + t.ToString())

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

[**AxWindowsMediaPlayer.currentMedia (VB und C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.openState (VB und C#)**](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.OpenStateChange-Ereignis (VB und C#)**](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.durationString (VB und C#)**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)
</dt> </dl>

 

 





