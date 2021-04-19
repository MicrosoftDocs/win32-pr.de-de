---
title: Iwmpsettings-Rate (Eigenschaft)
description: Mit der Eigenschaft Rate wird die aktuelle Wiedergabe Rate für Video abgerufen oder festgelegt.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- Rate der Eigenschaften Fenster Media Player
- Rate der Eigenschaften Fenster Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows-Media Player, Rate-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings.rate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f502bebdbd22523858637f8abccbe203db104cbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367596"
---
# <a name="iwmpsettingsrate-property"></a>Iwmpsettings:: Rate (Eigenschaft)

Mit der Eigenschaft **Rate** wird die aktuelle Wiedergabe Rate für Video abgerufen oder festgelegt.

## <a name="syntax"></a>Syntax


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Double** -Wert, der die Wiedergabe Rate mit dem Standardwert 1,0 ist.

## <a name="remarks"></a>Bemerkungen

Der von dieser Eigenschaft abgerufene Wert fungiert als Multiplikatorwert, mit dem Sie ein Medien Element schneller oder langsamer wiedergeben können. Der Standardwert 1,0 gibt die erstellte Geschwindigkeit an.

Beachten Sie, dass eine Audiospur bei Raten, die niedriger als 0,5 oder höher als 1,5 sind, schwer zu verstehen ist. Eine Wiedergabe Rate von 2 gibt die doppelte Geschwindigkeit der Wiedergabe an.

Windows Media Player versucht, die am effektivsten der folgenden vier verschiedenen Wiedergabe Modi zu verwenden.

-   Smooth Videowiedergabe mit gestelltem Audiobereich
-   Smooth-Videowiedergabe mit nicht gebeibehaltung audiotonhöhe
-   Smooth Videowiedergabe ohne Audiodaten
-   Keyframe-Videowiedergabe ohne Audiodaten

Der von Windows Media Player gewählte Modus hängt von zahlreichen Faktoren ab, einschließlich Dateityp und-Speicherort, Betriebssystem, Netzwerk und Server.

Es gelten auch weitere Überlegungen, abhängig vom Format des digitalen Mediums, das zum Erstellen des Inhalts verwendet wird:

-   **Windows Media Video (WMV) und ASF.** Optimale Werte für die **Rate** -Eigenschaft liegen zwischen 1 und 10 oder zwischen 1 und 10 für Reverse-Play. Werte zwischen 0,5 und 1,0 oder zwischen-0,5 und 1,0 funktionieren möglicherweise auch in Fällen, in denen audiotonhöhe beibehalten werden kann, z. b. bei der Wiedergabe von Dateien auf dem lokalen Computer. Werte mit einer absoluten Größe von mehr als 10 sind zulässig, sind jedoch nicht sehr sinnvoll.
-   **Andere Videoformate.** Die **Rate** -Eigenschaft kann zwischen 0 und 9 liegen. Negative Werte sind nicht zulässig. Werte kleiner als 1 stellen eine langsame Bewegung dar. Werte oberhalb von 9 sind zulässig, sind jedoch nicht sehr sinnvoll.

Die **iwmpcontrols. FastForward** -Methode ändert den Wert von **Rate** in 5,0, während die **iwmpcontrols. fastreverse** -Methode den Wert von **Rate** in 5,0 ändert.

Die Wiedergabe Rate einiger digitaler Medienformate kann nicht geändert werden. Verwenden Sie die **iwmpsettings. IsAvailable** -Eigenschaft (in c# die **iwmpsettings. get \_ IsAvailable** -Methode), um zu ermitteln, ob diese Eigenschaft für ein bestimmtes Medien Element angegeben werden kann.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein numerisches UpDown-Steuerelement verwendet, das es dem Benutzer ermöglicht, die Wiedergabegeschwindigkeit des aktuellen Mediums zu ändern. Wenn der Benutzer auf die nach-oben-oder nach-unten-Pfeile des Steuer Elements klickt, wird die Eigenschaft **Rate** auf den neuen Wert festgelegt. Der mögliche Wertebereich im Steuerelement ist 0,5 (halbe Geschwindigkeit) bis 2,0 (doppelte Geschwindigkeit). Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void playbackRate_Click(object sender, System.EventArgs e)
{
    // Get the new value of the control, and cast it from decimal to double.
    double newRate = (double)((System.Windows.Forms.NumericUpDown)sender).Value;

    // Test whether playback rate can be set. 
    if( player.settings.get_isAvailable("Rate") )
    {
        // Set the playback rate to the new value.
        player.settings.rate = newRate;
    }
}
```


```VB

Public Sub playbackRate_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playbackRate.Click

    &#39;  Get the new value of the control as a double.
    Dim nUpDown As System.Windows.Forms.NumericUpDown = sender
    Dim newRate As Double = nUpDown.Value

    &#39;  Test whether playback rate can be set. 
    If (player.settings.isAvailable(&quot;Rate&quot;)) Then

        &#39;  Set the playback rate to the new value.
        player.settings.rate = newRate

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

[**Iwmpcontrols. FastForward (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. fastreverse (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings-Schnittstelle (VB und c#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. IsAvailable (VB und c#)**](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. stumm (VB und c#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





