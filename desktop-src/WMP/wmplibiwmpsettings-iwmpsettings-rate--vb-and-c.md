---
title: IWMPSettings-Rate-Eigenschaft
description: Die Rate-Eigenschaft ruft die aktuelle Wiedergaberate für Video ab oder legt sie fest.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- rate-Eigenschaft Windows Media Player
- rate-Eigenschaft Windows Media Player , IWMPSettings-Schnittstelle
- IWMPSettings-Schnittstelle Windows Media Player , rate-Eigenschaft
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
ms.openlocfilehash: cc053861b9061df676455e10b011cd0ffe0fe9f06052b129ec163e00d4c8d71f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999700"
---
# <a name="iwmpsettingsrate-property"></a>IWMPSettings::rate-Eigenschaft

Die **Rate-Eigenschaft** ruft die aktuelle Wiedergaberate für Video ab oder legt sie fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.Double-Datei,** die die Wiedergaberate mit einem Standardwert von 1,0 ist.

## <a name="remarks"></a>Hinweise

Der von dieser Eigenschaft abgerufene Wert fungiert als Multiplikatorwert, mit dem Sie ein Medienelement schneller oder langsamer wiedergeben können. Der Standardwert 1,0 gibt die erstellte Geschwindigkeit an.

Beachten Sie, dass eine Audiospur mit Raten kleiner als 0,5 oder höher als 1,5 schwer zu verstehen ist. Eine Wiedergaberate von 2 gibt das Doppelte der normalen Wiedergabegeschwindigkeit an.

Windows Media Player versucht, die effektivsten der folgenden vier verschiedenen Wiedergabemodi zu verwenden.

-   Smooth video playback with audio pitch maintained (Reibungslose Videowiedergabe mit beibehaltener Audiowiedergabe)
-   Smooth video playback with audio pitch not maintained (Reibungslose Videowiedergabe mit nicht verwalteter Audiowiedergabe)
-   Reibungslose Videowiedergabe ohne Audio
-   Keyframe-Videowiedergabe ohne Audio

Der von Windows Media Player gewählte Modus hängt von zahlreichen Faktoren ab, einschließlich Dateityp und Speicherort, Betriebssystem, Netzwerk und Server.

Abhängig vom digitalen Medienformat, das zum Erstellen des Inhalts verwendet wird, gelten auch andere Überlegungen:

-   **Windows Media Video (WMV) und ASF.** Die optimalen Werte für die **Rate-Eigenschaft** liegen zwischen 1 und 10 bzw. zwischen 1 und 10 für das Reverseplay. Werte von 0,5 bis 1,0 oder von -0,5 bis -1,0 können auch in Fällen gut funktionieren, in denen audio pitch beibehalten werden kann, z. B. beim Wiedergeben von Dateien, die sich auf dem lokalen Computer befinden. Werte mit einer absoluten Größe größer als 10 sind zulässig, aber nicht sehr aussagekräftig.
-   **Andere Videoformate.** Die **Rate-Eigenschaft** kann zwischen 0 und 9 liegen. Negative Werte sind nicht zulässig. Werte kleiner als 1 stellen langsame Bewegung dar. Werte über 9 sind zulässig, aber nicht sehr aussagekräftig.

Die **IWMPControls.fastForward-Methode** ändert den Wert der **Rate** in 5.0, während die **IWMPControls.fastReverse-Methode** den Wert der **Rate** in 5,0 ändert.

Die Wiedergaberate einiger digitaler Medienformate kann nicht geändert werden. Verwenden Sie die **IWMPSettings.isAvailable-Eigenschaft** (in C# die **IWMPSettings.get \_ isAvailable-Methode),** um zu ermitteln, ob diese Eigenschaft für ein bestimmtes Medienelement angegeben werden kann.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein numerisches Updown-Steuerelement verwendet, mit dem der Benutzer die Wiedergabegeschwindigkeit der aktuellen Medien ändern kann. Wenn der Benutzer auf die Pfeile nach oben oder unten des Steuerelements klickt, wird die **Rate-Eigenschaft** auf den neuen Wert festgelegt. Der mögliche Wertebereich im Steuerelement ist 0,5 (Halbgeschwindigkeit) bis 2,0 (Doppelte Geschwindigkeit). Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPControls.fastForward (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls.fastReverse (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[**IWMPSettings-Schnittstelle (VB und C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.isAvailable (VB und C#)**](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.mute (VB und C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





