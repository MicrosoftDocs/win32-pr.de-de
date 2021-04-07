---
description: Audio-Tapered volumesteuerelemente
ms.assetid: 3b1adef5-40e9-4527-aa79-5a71f201fdfc
title: Audio-Tapered volumesteuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cca0879d27d0eba3d49ca22b019442f882bf917
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748440"
---
# <a name="audio-tapered-volume-controls"></a>Audio-Tapered volumesteuerelemente

Die [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) -Schnittstelle verwaltet volumensteuerelemente, die Audiodaten enthalten. Diese Steuerelemente eignen sich gut für Windows-Anwendungen, die Lautstärkeregler angezeigt werden. Bei einem volumeschiebe Regler, der an ein Audiosteuer Element gebunden ist, ergibt jede Änderung an der Position des Schiebereglers eine Änderung der wahrgenommenen Lautstärke, die proportional zu der Entfernung des Schiebereglers ist. Bei einer bestimmten Reise Entfernung ist der Betrag, um den die wahrgenommene Lautstärke zunimmt oder abnimmt, ungefähr gleich, unabhängig davon, ob die Schieberegler-Bewegung im unteren, oberen oder mittleren Bereich des Schiebereglers liegt. Die wahrgenommene Lautstärke variiert ungefähr linear mit dem Logarithmus der audiosignalpotenz.

Der Begriff " *audiotaper* " bezog sich ursprünglich auf die Form des resivetenelements in einem potenzimesser, das als volumesteuerelement in einem Audioelektronik-Gerät verwendet wird. Ein Audioelement, das resistive ist, ist an der NULL-volumeposition am größten und an der maximalen volumeposition am engsten. Das-Element steuert die Spannungsebene des Audiosignals, das das Gerät über seine Sprecher spielt. Die taperung ist so konzipiert, dass Sie eine ungefähr lineare Beziehung zwischen der Position des potenzimessers Wischer und der wahrgenommenen Lautstärke bei den Referenten erzeugt. Die Beziehung zwischen der Wischer-Position und der Spannung bei den Referenten ist nicht linear.

Im Gegensatz dazu hat ein resikationselement mit einem linearen anzupassen eine einheitliche Breite über dem Bereich der Bewegung des potenzitmessers. Folglich variiert die Spannung in den Referenten linear mit der Wischer-Position. Die Beziehung zwischen der Wischer-Position und der Lautstärke ist nicht linear.

Ebenso definiert eine Windows-Anwendung, die einen volumeschiebe Regler anzeigt, eine Beziehung zwischen der Schieberegler-Position und der Ausgabesignal Ebene bei den Referenten. Die Beziehung kann im Endeffekt linear oder in der Audiodatei angezeigt werden.

Das folgende Diagramm zeigt die Zuordnung der Schieberegler-Position zu Ausgabe Spannung und die wahrgenommene Lautstärke für ein lineares Steuerelement.

![Ausgabe Diagramm für ein lineares Steuerelement mit einem Steuerelement](images/taper1.jpg)

Auf der linken Seite des vorangehenden Diagramms nimmt die Ausgabe Spannungsebene des audiodigital-to-Analog-Konverters (DAC) linear zu, wenn der volumeschiebe Regler von der minimalen Position (mit der Bezeichnung min) bis zur maximalen Position (mit der Bezeichnung max) wechselt. Die Bezeichnung V<sub>FS</sub> auf der vertikalen Achse stellt die vollständig skalierbare DAC-Ausgabe Spannung dar.

Die wahrgenommene Lautstärke variiert jedoch ungefähr wie der Logarithmus der Leistungsfähigkeit des Audiosignals, wie auf der rechten Seite des vorangehenden Diagramms dargestellt. Folglich führt die Verschiebung des Schiebereglers über ein Intervall in der Nähe der minimalen Einstellung zu einer relativ großen Änderung der wahrgenommenen Lautstärke, aber die Schieberegler-Bewegung über ein Intervall mit derselben Breite in der Nähe der maximalen Einstellung bewirkt eine relativ kleine Änderung der wahrgenommenen Lautstärke.

Auf der rechten Seite des vorangehenden Diagramms wird die Lautstärke auf der vertikalen Achse in Dezimalstellen (DB) relativ zur vollständigen Energie Einstellung (bei 0 Dezimalstellen) gemessen. Die Lautstärke Kurve schneidet die vertikale Achse bei minus unendlich ab, aber nur der Teil der Kurve von 0 Dezibel bis – 96 Dezibel wird im Diagramm angezeigt. Die Entscheidung, nur diesen Teil der Kurve anzuzeigen, ist willkürlich, aber – 96 Dezibel stellt die Leistung auf der nächstniedrigsten Ausgabe Ebene einer 16-Bit-DAC relativ zur vollen Leistung dar. Dieser Wert wird als 20 berechnet<sup>.</sup> Log ₁ ₀ (1/65535).

Da kleine Änderungen an der Schiebereglerposition in der Nähe der minimalen Einstellung im vorangehenden Diagramm zu großen Änderungen bei der Lautstärke führen, kann der Benutzer das Volume möglicherweise nur schwer steuern. Relativ kleine Schieberegler-Bewegungen können das Volume über oder unterhalb der gewünschten Ebene verschieben. Ein verbessertes Volume-Steuerelement würde eine lineare Beziehung zwischen der Schieberegler-Position und der Lautstärke bereitstellen.

Im folgenden Diagramm wird die Zuordnung der Schieberegler-Position zu Ausgabe Spannung und der wahrgenommenen Lautstärke für ein Audiosteuer Element angezeigt.

![Ausgabe Diagramm für das Audiosteuer Element-volumensteuerelement](images/taper2.jpg)

Wie auf der rechten Seite des vorangehenden Diagramms gezeigt, variiert die wahrgenommene Lautstärke ungefähr linear mit Änderungen an der Position des Schiebereglers. Damit dies geschehen kann, muss die DAC-Spannung nicht linear mit der Position variieren, wie auf der linken Seite des Diagramms dargestellt. Die Kurve nähert sich bei 0 Volt, wenn sich der Schieberegler nach links von der maximalen Einstellung bewegt. Die Spannung an der minimalen Schieberegler-Position ist sehr klein, Sie ist jedoch möglicherweise nicht genau null.

Die folgenden Methoden in der **iaudioendpointvolume** -Schnittstelle verwenden Volumeeinstellungen, die in Dezimalstellen gemessen werden:

-   [**Iaudioendpointvolume:: getchannelvolumelevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevel)
-   [**Iaudioendpointvolume:: getmastervolumelevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevel)
-   [**Iaudioendpointvolume:: setchannelvolumelevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**Iaudioendpointvolume:: setmastervolumelevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)

Diese Methoden ergeben eine ungefähr lineare Beziehung zwischen der volumeeinstellung und der wahrgenommenen Lautstärke. Der volumebereich in Dezimalstellen der volumesteuerelemente, die von diesen Methoden verwaltet werden, hängt vom audioendpunkttyp ab. Um den volumebereich für ein bestimmtes Gerät zu ermitteln, müssen Sie die [**iaudioendpointvolume:: getvolumerange**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange) -Methode aufrufen.

Im Gegensatz dazu folgen die volumeinstellungeneinstellungen für die folgenden Methoden in der **iaudioendpointvolume** -Schnittstelle einer schonteren Kurve über dem volumebereich:

-   [**Iaudioendpointvolume:: getchannelvolumelevelscalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevelscalar)
-   [**Iaudioendpointvolume:: getmastervolumelevelscalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevelscalar)
-   [**Iaudioendpointvolume:: setchannelvolumelevelscalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**Iaudioendpointvolume:: setmastervolumelevelscalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**Iaudioendpointvolume:: volumestepdown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**Iaudioendpointvolume:: volumestepup**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

In Windows Vista verwenden diese Methoden eine Kurve, die zwischen der im vorangehenden Diagramm gezeigten audiotasterkurve und einer linear-Kegel-Kurve zwischen und verläuft. Beachten Sie, dass sich die Form der Kurve in zukünftigen Versionen von Windows möglicherweise ändert. Mit den ersten vier Methoden in der obigen Liste werden die volumeebenen als normalisierte Werte im Bereich von 0,0 (minimal Volume) bis 1,0 (maximales Volume) ausgedrückt. Rufen Sie für die letzten beiden Methoden in der Liste die [**iaudioendpointvolume:: getvolumestepinfo**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumestepinfo) -Methode auf, um die Anzahl der Schritte im volumebereich zu erhalten.

Die folgenden Schnittstellen verwenden linear-kegelförmige Kurven für Ihre Volumeeinstellungen:

-   [**Isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
-   [**Ichannelaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)
-   [**Iaudiostreamvolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)

Weitere Informationen zu diesen Schnittstellen finden Sie unter [Sitzungs Volume](session-volume-controls.md)-Steuerelemente. Informationen zu den volumebereichen und den Standard Volume-Ebenen in den verschiedenen Versionen von Windows finden Sie unter [Standardeinstellungen für audiovolumes](/windows-hardware/drivers/audio/default-audio-volume-settings).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lautstärkeregler](volume-controls.md)
</dt> </dl>

 

 
