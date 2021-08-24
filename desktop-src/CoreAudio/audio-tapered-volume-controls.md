---
description: Audio-Tapered Volumesteuerelemente
ms.assetid: 3b1adef5-40e9-4527-aa79-5a71f201fdfc
title: Audio-Tapered Volumesteuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb4856b4f25ad33ae61e9cb250a6b84f0e8799bb9d11d33c1770593bcf3714a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750789"
---
# <a name="audio-tapered-volume-controls"></a>Audio-Tapered Volumesteuerelemente

Die [**IAudioEndpointVolume-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) verwaltet Volumesteuerelemente, die mit Audio verjippt sind. Diese Steuerelemente eignen sich gut für Windows Anwendungen, die Lautstärkeregler anzeigen. Bei einem Lautstärkeregler, der an ein Audio-Tapering-Lautstärkeregler gebunden ist, erzeugt jede Änderung der Position des Schiebereglers eine Änderung der wahrgenommenen Lautheit, die proportional zur Entfernung des Schiebereglers ist. Für eine bestimmte Reiseentfernung ist die Menge, um die die wahrgenommene Lautstärke steigt oder abnimmt, ungefähr gleich, unabhängig davon, ob die Schiebereglerbewegung im unteren, oberen oder mittleren Teil des Bewegungsbereichs des Schiebereglers auftritt. Die wahrgenommene Lautheit variiert ungefähr linear mit dem Logarithmus der Audiosignalleistung.

Der Begriff *Audio taper* bezieht sich ursprünglich auf die konterierte Form des widerstandsfähigen Elements in einem Messgerät, das als Lautstärkeregler in einem Audiogerät verwendet wird. Ein audioverkniffenes widerstandsfähiges Element ist an der Nullvolumeposition am breitesten und an der maximalen Volumeposition am engsten. Der Stromzähler steuert den Spannungspegel des Audiosignals, das das Gerät über seine Lautsprecher abspielt. Das Bandband ist so konzipiert, dass eine ungefähr lineare Beziehung zwischen der Position des Tapeiometer-Wipers und der wahrgenommenen Lautheit an den Lautsprechern entsteht. Die Beziehung zwischen der Löschposition und der Stromversorgung an den Lautsprechern ist nicht linear.

Im Gegensatz dazu hat ein widerstandsfähiges Element mit einem linearen Taper eine einheitliche Breite über dem Bewegungsbereich des Wischmessers. Daher variiert die Spannung an den Lautsprechern linear mit der Position des Löschers. Die Beziehung zwischen der Position des Löschers und der Lautstärke ist nicht linear.

Ebenso definiert eine Windows Anwendung, die einen Lautstärkeregler anzeigt, eine Beziehung zwischen der Position des Schiebereglers und der Ausgabesignalebene auf den Lautsprechern. Die Beziehung kann in der Tat linear kontered oder audio tapered sein.

Das folgende Diagramm zeigt die Zuordnung der Schiebereglerposition zur Ausgangsspannung und zur wahrgenommenen Lautheit für eine linear verjippte Lautstärkeregler.

![Ausgabediagramm für ein linear verjipptes Volumesteuerelement](images/taper1.jpg)

Auf der linken Seite des vorherigen Diagramms erhöht sich die Ausgangsspannung des Audio-DAC (Digital-to-Analog Converter) linear, wenn sich der Lautstärkeregler von seiner Minimalposition (mit der Bezeichnung Min) bis zur maximalen Position (mit der Bezeichnung Max) bewegt. Die Bezeichnung V<sub>FS</sub> auf der vertikalen Achse stellt die DAC-Ausgangsspannung in voller Skalierung dar.

Die wahrgenommene Lautheit variiert jedoch ungefähr wie der Logarithmus der Leistung des Audiosignals, wie auf der rechten Seite des vorherigen Diagramms dargestellt. Daher führt die Bewegung des Schiebereglers über ein Intervall in der Nähe der Minimaleinstellung zu einer relativ großen Änderung der wahrgenommenen Lautheit, aber die Schiebereglerbewegung über ein Intervall derselben Breite in der Nähe der maximalen Einstellung führt zu einer relativ kleinen Änderung der wahrgenommenen Lautheit.

Auf der rechten Seite des vorherigen Diagramms wird die Lautstärke auf der vertikalen Achse in Decibel (dB) relativ zur Vollskalierungseinstellung (bei 0 Dezibel) gemessen. Die Lautheitskurve überschneidet die vertikale Achse bei minus unendlich, aber nur der Teil der Kurve von 0 Dezibel bis –96 Dezibel wird im Diagramm angezeigt. Die Entscheidung, nur diesen Teil der Kurve anzuzeigen, ist etwas willkürlich, aber –96 Dezibel stellt praktischerweise die Leistung auf der nächst- bis untersten Ausgabeebene einer 16-Bit-DAC relativ zur Vollleistung dar. Dieser Wert wird als 20<sup>berechnet.</sup> log₁₀(1/65535).

Da kleine Änderungen an der Position des Schiebereglers in der Nähe der Minimaleinstellung im vorherigen Diagramm zu großen Änderungen in der Lautstärke führen, kann es für den Benutzer schwierig sein, das Volumen über diesen Bereich zu steuern. Relativ kleine Schiebereglerbewegungen können das Volume weit über oder unter die gewünschte Ebene bewegen. Eine verbesserte Lautstärkeregler würde eine linearere Beziehung zwischen Schiebereglerposition und Lautstärke bereitstellen.

Das folgende Diagramm zeigt die Zuordnung der Schiebereglerposition zur Ausgabespannung und zur wahrgenommenen Lautheit für ein Audio-Tapered Volume Control.

![Ausgabediagramm für audioverknippte Lautstärkeregler](images/taper2.jpg)

Wie auf der rechten Seite des vorherigen Diagramms dargestellt, variiert die wahrgenommene Lautstärke mit Änderungen an der Schiebereglerposition ungefähr linear. Damit dies geschieht, muss die DAC-Stromversorgung nicht linear mit der Position variieren, wie auf der linken Seite des Diagramms dargestellt. Die Kurve nähert sich asymptotisch 0(e) 0(n), wenn sich der Schieberegler von der maximalen Einstellung nach links bewegt. Die Spannung an der minimalen Schiebereglerposition ist sehr klein, aber möglicherweise nicht genau 0 (null).

Die folgenden Methoden in der **IAudioEndpointVolume-Schnittstelle** verwenden Volumeeinstellungen, die in Decibel gemessen werden:

-   [**IAudioEndpointVolume::GetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevel)
-   [**IAudioEndpointVolume::GetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevel)
-   [**IAudioEndpointVolume::SetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**IAudioEndpointVolume::SetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)

Diese Methoden erzeugen eine ungefähr lineare Beziehung zwischen der Lautstärkeeinstellung und der wahrgenommenen Lautheit. Der Lautstärkebereich der Volumesteuerelemente, die von diesen Methoden verwaltet werden, hängt vom Audioendpunktgerät ab. Um den Volumebereich für ein bestimmtes Gerät zu bestimmen, rufen Sie die [**IAudioEndpointVolume::GetVolumeRange-Methode**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange) auf.

Im Gegensatz dazu folgen die Volumeeinstellungen für die folgenden Methoden in der **IAudioEndpointVolume-Schnittstelle** einer stärker verjengten Kurve über den Volumebereich:

-   [**IAudioEndpointVolume::GetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::GetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevelscalar)
-   [**IAudioEndpointVolume::SetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**IAudioEndpointVolume::VolumeStepDown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**IAudioEndpointVolume::VolumeStepUp**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

In Windows Vista verwenden diese Methoden eine Kurve, die zwischen der im vorherigen Diagramm gezeigten audioverknippten Kurve und einer linearen konterierten Kurve liegt. Beachten Sie, dass sich die Form der Kurve in zukünftigen Versionen von Windows ändern kann. Die ersten vier Methoden in der obigen Liste geben Volumenebenen als normalisierte Werte im Bereich von 0,0 (Mindestvolumen) bis 1,0 (maximales Volume) aus. Rufen Sie für die letzten beiden Methoden in der Liste die [**IAudioEndpointVolume::GetVolumeStepInfo-Methode**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumestepinfo) auf, um die Anzahl der Schritte im Volumebereich abzurufen.

Die folgenden Schnittstellen verwenden lineare krümmende Kurven für ihre Volumeeinstellungen:

-   [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
-   [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)
-   [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)

Weitere Informationen zu diesen Schnittstellen finden Sie unter [Sitzungsvolumesteuerelemente.](session-volume-controls.md) Informationen zu den Volumebereichen und den Standardvolumeebenen in den verschiedenen Versionen von Windows finden Sie unter [Standardaudiovolume Einstellungen](/windows-hardware/drivers/audio/default-audio-volume-settings).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lautstärkeregler](volume-controls.md)
</dt> </dl>

 

 
