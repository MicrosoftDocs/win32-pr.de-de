---
title: Iwmpmedia Duration (Eigenschaft)
description: Die Duration-Eigenschaft ruft die Dauer des aktuellen Medien Elements in Sekunden ab.
ms.assetid: f8a0bf3e-eeaf-46f5-90c8-d3b11ce4eb39
keywords:
- Duration-Eigenschaften Fenster Media Player
- Duration-Eigenschaft, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, Duration-Eigenschaft
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
ms.openlocfilehash: f796cab042713082ce2066659f62736855e62787
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373969"
---
# <a name="iwmpmediaduration-property"></a>Iwmpmedia::d urationseigenschaft

Die **Duration** -Eigenschaft ruft die Dauer des aktuellen Medien Elements in Sekunden ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.Double duration {get;}
```


```VB

Public ReadOnly Property duration As System.Double
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Double** -Wert, der die Dauer in Sekunden angibt.

## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft mit einem anderen als dem in AxWindowsMediaPlayer. currentMedia angegebenen Medien Element verwendet wird, enthält Sie möglicherweise keinen gültigen Wert.

Zum Abrufen der Dauer für Dateien, die sich nicht in der Bibliothek des Benutzers befinden, müssen Sie auf das Öffnen der Datei durch Windows Media Player warten. Das heißt, dass der aktuelle **openstate** -Wert " **mediaopen**" entsprechen muss. Sie können dies überprüfen, indem Sie **AxWindowsMediaPlayer verarbeiten. \_ Wmpocxevents \_ OpenStateChange** -Ereignis oder durch regelmäßiges Überprüfen des Werts von **AxWindowsMediaPlayer. openstate**.

Bei Wiedergabelisten kann die Dauer der einzelnen Medienelemente abgerufen werden, wenn das einzelne Medien Element geöffnet wird, anstatt beim Öffnen der Wiedergabeliste.

Vor der Verwendung dieser Eigenschaft müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **Duration** verwendet, um die verbleibende Zeit im aktuellen Medien Element in einer Bezeichnung anzuzeigen. Ein Timer aktualisiert den Text in der Bezeichnung jede Sekunde.


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
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer. currentMedia (VB und c#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. openstate (VB und c#)**](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. OpenStateChange-Ereignis (VB und c#)**](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. durationString (VB und c#)**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)
</dt> </dl>

 

 





