---
description: Die Gammakorrektur oder kurz Gamma ist der Name eines nicht linearen Vorgangs, den Systeme verwenden, um Pixelwerte in Bildern zu codieren und zu decodieren.
ms.assetid: 97ACDAE3-514E-4AAF-A27D-E5FFC162DB2A
title: Verwenden der Gammakorrektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c5f5d3af8550f86280e6203858444469a5aa8caaab462f560da152caaa2a76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118288964"
---
# <a name="using-gamma-correction"></a>Verwenden der Gammakorrektur

Die Gammakorrektur oder kurz Gamma ist der Name eines nicht linearen Vorgangs, den Systeme verwenden, um Pixelwerte in Bildern zu codieren und zu decodieren.

-   [Was ist Gamma, und wozu dient es?](#what-is-gamma-and-what-is-it-for)
-   [Hintergrund des Gammas auf Windows](#background-of-gamma-on-windows)
-   [Entwicklung der Anzeigehardware](#evolution-of-display-hardware)
-   [Gamma-Steuerungsfunktionen in DXGI](#gamma-control-capabilities-in-dxgi)
-   [Festlegen des Gammasteuerelements mit DXGI](#setting-gamma-control-with-dxgi)
-   [Praktische Praktischkeiten der Gammasteuerung](#gamma-control-practicalities)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-gamma-and-what-is-it-for"></a>Was ist Gamma, und wozu dient es?

Am Ende der Grafikpipeline, genau dort, wo das Bild den Computer verlässt, um die Reise entlang des Überwachungskabels zu unternehmen, gibt es ein kleines Hardwareelement, das Pixelwerte im Flug transformieren kann. Diese Hardware verwendet in der Regel eine Nachschlagetabelle, um die Pixel zu transformieren. Diese Hardware verwendet die roten, grünen und blauen Werte, die von der Angezeigten Oberfläche stammen, um nach gammakorrigierten Werten in der Tabelle zu suchen, und sendet dann die korrigierten Werte anstelle der tatsächlichen Oberflächenwerte an den Monitor. Daher ist diese Nachschlagetabelle eine Möglichkeit, jede Farbe durch eine andere Farbe zu ersetzen. Während die Tabelle über diese Leistungsstufe verfügt, besteht die typische Verwendung darin, Bilder subtly zu optimieren, um Unterschiede in der Reaktion des Monitors zu kompensieren. Die Antwort des Monitors ist die Funktion, die den numerischen Wert der roten, grünen und blauen Komponenten eines Pixels mit der angezeigten Helligkeit dieses Pixels verknüpft.

Dies war für diese Tabelle vorgesehen, aber Spielentwickler haben für sie eine kreativ nutzungsreiche Anwendung gefunden, z. B. das Rot blinken des gesamten Bildschirms, um den Effekt zu erzielen. In modernen Spiele-Apps bieten wir im Rahmen der Nachverarbeitung der einzelnen Frames in der Regel andere Möglichkeiten, solche Dinge zu tun. Tatsächlich wird empfohlen, die Gammatabelle in Ruhe zu lassen, da sie möglicherweise verwendet wird, um die Reaktion des Monitors zu kalibrieren, und durch die änderbaren Änderungen an der Gamma-Rampe wird diese sorgfältige Kalibrierung zerstört.

Die wissenschaftliche Natur der Bestimmung der Gammakorrektur ist komplex und wird hier nur dargestellt, um herauszufinden, woher der Name "gamma" stammt. Die Antwort eines CRT-Monitors (d. h. eines altmodischen Glassers) ist eine komplexe Funktion, aber die Physikalischen Daten dieser Monitore bedeuten, dass sie eine Antwort zeigen, die durch diese Energiefunktion mäßig dargestellt werden kann:

brightness( input ) = input<sup>gamma</sup>

Der Gammawert liegt in der Regel nahe an einem Wert von 2,0. MONITOR-Monitore und alle anderen neueren Technologien sind speziell so konzipiert, dass sie eine ähnliche Reaktion zeigen, sodass unsere gesamte Software und unsere Images nicht für diese neuen Technologien neu entwickelt werden müssen. Der sRGB-Standard deklariert, dass dieser Gammawert genau 2,2 ist, und dieser Wert ist zu einem weit verbreiteten Standard geworden.

Das menschliche Auge verfügt auch über eine Antwortfunktion, die die CRT-Energiefunktion ungefähr umkehrt. Dies bedeutet, dass die wahrgenommene Helligkeit eines Pixels sehr ungefähr linear mit den RGB-Werten in diesem Pixel steigt.

Da ein Gammawert von 2,2 zu einem De-facto-Standard geworden ist, müssen wir uns in der Regel nicht zu sehr um die in dieser Tabelle codierte Gammakurve kümmern und können sie als lineare 1:1-Zuordnung belassen. Für den richtigen Farbabgleich ist bei dieser Funktion natürlich vorsichtshalber erforderlich, aber diese Diskussion geht über den Rahmen dieses Themas hinaus. Windows enthält ein Tool, mit dem Benutzer ihre Displays auf Gamma 2.2 kalibrieren können. Dieses Tool verwendet die Nachschlagetabellenhardware, um eine sorgfältig ausgewählte kleine Optimierung für ihre Computer abzuleiten. Benutzer können dieses Tool ausführen, indem sie nach "Kalibrierung der Farbe" suchen. Es gibt auch klar definierte Farbprofile für bestimmte Monitore, die diesen Prozess automatisieren. Das Tool "Kalibrierung der Farbe" kann diese neueren Monitore erkennen und Benutzer darüber informieren, dass die Kalibrierung bereits vorhanden ist.

Dieses Konzept der Codierung eines Potenzrechtes in Farbwerte ist auch an anderer Stelle in der Grafikpipeline nützlich, insbesondere in Texturen. Für Texturen möchten Sie aufgrund der logarithmischen menschlichen Augenantwort, über die wir gerade gesprochen haben, eine größere Genauigkeit bei dunkleren Farben erreichen. Die sorgfältige Behandlung von Gamma in diesem Teil der Pipeline ist wichtig. Weitere Informationen finden Sie unter [Konvertieren von Daten für den Farbraum](converting-data-color-space.md).

Der Rest dieses Themas konzentriert sich nur auf die Gammakorrektur in diesem letzten Teil der Pipeline zwischen den Framepufferdaten und dem Monitor. Wenn Sie einen Kalibrierungs-Assistenten schreiben oder Sondereffekte in einer Vollbild-App erstellen möchten, bei der ein Nachbearbeitungsschritt nicht praktikabel ist, finden Sie hier die informationen, die Sie benötigen.

## <a name="background-of-gamma-on-windows"></a>Hintergrund des Gammas auf Windows

Windows Computer verfügen in der Regel über eine Gammatabelle, bei der es sich um eine Nachschlagetabelle handelt, die ein Triplet von Bytes annimmt und ein Triplet von Bytes ausgibt. Diese Dreier sind 768 (256 x 3) Bytes RAM. Dies ist in Ordnung, wenn Ihr Anzeigeformat ein Triplet von RGB-BYTE-Werten enthält, aber nicht ausdrucksreich genug ist, um die Transformationen zu beschreiben, die Sie möglicherweise benötigen, wenn das Anzeigeformat einen größeren Bereich als \[ 0,1 auf \] hat, z. B. Gleitkommawerte. Die APIs in Windows, die Gamma steuern, haben eine Weiterentwicklung mit zunehmender Komplexität der Anzeigeformate verfolgt.

Die ersten Windows APIs, die gamma steuern, sind [**setDeviceGammaRamp (SetDeviceGammaRamp)**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp) und [**GetDeviceGammaRamp (GDI)**](/windows/win32/api/wingdi/nf-wingdi-getdevicegammaramp)von Windows Graphics Device Interface . Diese APIs funktionieren mit drei 256-Eintragsarrays von WORDs, wobei jede WORD-Codierung null bis 1 ist, dargestellt durch die WORD-Werte 0 und 65535. Die zusätzliche Genauigkeit eines WORD-Ausdrucks ist in der Regel nicht in tatsächlichen Hardwares lookup-Tabellen verfügbar, aber diese APIs sollten flexibel sein. Diese APIs lassen im Gegensatz zu den weiter unten in diesem Abschnitt beschriebenen APIs nur eine kleine Abweichung von einer Identitätsfunktion zu. Tatsächlich muss jeder Eintrag in der Rampe innerhalb von 32768 des Identitätswerts sein. Diese Einschränkung bedeutet, dass keine App die Anzeige vollständig schwarz oder in eine andere nicht lesbare Farbe umwandeln kann.

Die nächste API ist [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)von Microsoft Direct3D 9, das dem gleichen Muster und Datenformat wie [**SetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp)folgt. Der Standardwert der Gamma-Rampe Direct3D 9 ist nicht besonders nützlich. dabei handelt es sich um eine Rampe von WORDs, die mit 0-255 und nicht mit 0-65535 initialisiert wurde, obwohl die API im Hinblick auf 0-65535 definiert ist.

Die neueste API ist [**IDXGIOutput::SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol). Diese API verfügt über ein flexibleres Schema zum Ausdrücken des Gammasteuerelements, wie es dem erhöhten Satz von Anzeigeformaten von DXGI entspricht, einschließlich zehn ganzzahliger Bits pro Kanal, 16-Bit-Gleitkommaformaten und dem erweiterten XR \_ BIAS-Bereichsformat.

Alle diese APIs arbeiten auf derselben Hardware und ändern die gleichen Werte. Die Direct3D 9- und DXGI-APIs sind "schreibgeeist". Sie können den Wert der Hardware nicht lesen, ändern und anschließend festlegen. Sie können nur die Rampe festlegen. Darüber hinaus können Sie Gamma nur festlegen, wenn die App im Vollbildmodus angezeigt wird. Diese Einschränkung ist eine weitere Möglichkeit, sicherzustellen, dass der Desktop immer lesbar ist. Das heißt, die App kann ihre eigene Anzeige stören, aber Windows stellt die vorherige Gamma-Rampe wieder her, wenn die App den Vollbildmodus verliert (z. B. über ALT-TAB oder STRG+ALT-TASTE).

## <a name="evolution-of-display-hardware"></a>Entwicklung der Anzeigehardware

Einige neuere Monitore können eine Vielzahl von Intensitäten anzeigen. Wenn das Anzeigeformat jedoch nur Werte zwischen 0 und 1 darstellen kann, muss die Anzeige 0 (null) dem dunkelsten Wert und eins dem hellsten Wert zuordnen. Dieser hellste Wert ist möglicherweise viel zu hell für die komfortable Anzeige von Webseiten mit schwarzem Text auf einem weißen Hintergrund, eignet sich aber hervorragend für überhändige Sondereffekte, z. B. das Anzeigen von Licht aus einem See oder das Blitzen des Himmels. Daher benötigen wir eine Möglichkeit, diese größeren Bereiche auszudrücken. DXGI 1.1 und höher enthält Anzeigeformatwerte, mit denen 1.0 einen komfortablen weißen Wert darstellen kann und größere Anzeigeformatwerte für überbreite Sondereffekte reserviert. DXGI 1.1 unterstützt zwei Anzeigeformate, die diese breiteren Werte ausdrücken können: DXGI \_ FORMAT \_ R10G10B10 \_ XR \_ BIAS \_ A2 \_ UNORM und 16-Bit-Gleitkomma. Eine vollständige Erläuterung dieser Formate finden Sie unter [Details des erweiterten Formats](/windows-hardware/drivers/display/details-of-the-extended-format). Als Nächstes sehen wir uns an, warum die [**DXGI-API IDXGIOutput::SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) gamma Pixelwerte größer als 1.0 benötigt.

## <a name="gamma-control-capabilities-in-dxgi"></a>Gamma-Steuerungsfunktionen in DXGI

DXGI ermöglicht dem Anzeigetreiber, seine Gammasteuerelemente als schrittweise lineare Funktion auszudrücken. Diese schrittweise lineare Funktion wird durch die Steuerungspunkte dieser Funktion, den Wertebereich, in den die Funktion konvertiert werden kann, und einen zusätzlichen optionalen Skalierungs- und Offsetvorgang definiert, der nach der Konvertierung angewendet werden kann. Eine App kann die [**IDXGIOutput::GetGammaControlCapabilities-Methode**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) aufrufen, um alle diese Steuerungsfunktionen in der [**DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES-Struktur**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) abzurufen.

Dieses Diagramm zeigt eine lineare Funktion mit nur vier Kontrollpunkten.

![lineare Gammakorrekturfunktion](images/gamma-linear-function.png)

DXGI definiert Steuerungspunkte anhand ihrer Position entlang der Oberflächenfarbachse. Im vorherigen Diagramm sind die Positionen der Kontrollpunkte 0, 0,5, 0,75 und 1,0. Diese Kontrollpunkte geben an, dass die Hardware Werte im Bereich 0 bis 1,0 konvertieren kann. DXGI listet diese Steuerpunkte im **ControlPointPositions-Arraymember** von [**DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) auf und deklariert sie immer in zunehmender Reihenfolge. DXGI füllt nur die ersten Elemente des **ControlPointPositions-Arrays** und gibt die Anzahl der Elemente mit dem **NumGammaControlPoints-Member** von **DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES** an. Wenn **NumGammaControlPoints** kleiner als 1025 ist, lässt DXGI die restlichen **ControlPointPositions-Elemente** nicht definiert.

Die durch dieses Diagramm dargestellte Hardware kann Werte in einen Bereich von 0 bis 1,25 konvertieren. DXGI legt also die Member **MinConvertedValue** und **MaxConvertedValue** auf 0,0f bzw. 1,25f fest.

DXGI legt den **ScaleAndOffsetSupported-Member** von [**DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) fest, um anzugeben, ob die Hardware die Skalierungs- und Offsetfunktion unterstützt. Wenn Hardware Skalierung und Offset unterstützt, behält sie eine einfache 1:1-Nachschlagetabelle bei, passt dann aber die Ausgabe der Tabelle so an, dass die Ausgabe auf einen Bereich größer als \[ 0,1 gestreckt \] wird. Die Hardware skaliert zuerst die Werte, die aus der Nachschlagetabelle stammen, und versetzt sie dann.

> [!Note]  
> Verschiedene Monitore, die mit demselben Computer verbunden sind, verfügen möglicherweise über unterschiedliche Gammasteuerungsfunktionen. Darüber hinaus können sich die Gammasteuerfunktionen je nach Anzeigemodus der Ausgabe tatsächlich ändern. Daher wird empfohlen, immer [**IDXGIOutput::GetGammaControlCapabilities**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) aufzurufen, um Gammasteuerungsfunktionen abzufragen, nachdem Ihre App in den Vollbildmodus wechselt.

 

Sie können diese Gammasteuerelementfunktionswerte verwenden, um Steuerungswerte abzuleiten, die Sie dann mithilfe der [**IDXGIOutput::SetGammaControl-API**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) festlegen können.

## <a name="setting-gamma-control-with-dxgi"></a>Festlegen des Gammasteuerelements mit DXGI

Zum Festlegen von Gammasteuerelementen übergeben Sie einen Zeiger auf eine [**DXGI \_ GAMMA \_ CONTROL-Struktur,**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) wenn Sie die [**IDXGIOutput::SetGammaControl-API**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) aufrufen.

Sie legen die **Elemente Skalierung** und **Offset** von [**DXGI \_ GAMMA \_ CONTROL**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) fest, um die Skalierungs- und Offsetwerte anzugeben, die die Hardware auf die Werte anwenden soll, die Sie aus der Nachschlagetabelle erhalten. Sie können **Skalierung** sicher auf 1 und **Offset** auf 0 (d. h. eine Skalierung nach 1 hat keine Auswirkung und ein Offset von 0 hat keine Auswirkungen) festlegen, wenn Sie die Skalierungs- und Offsetfunktion nicht verwenden möchten oder wenn die Hardware nicht über diese Funktion verfügt.

Sie legen das **GammaCurve-Arrayelement** von [**DXGI \_ GAMMA \_ CONTROL**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) auf eine Liste von [**DXGI \_ RGB-Strukturen**](/previous-versions/windows/desktop/legacy/bb173071(v=vs.85)) für die Punkte in der Gammakurve fest. Jedes **DXGI \_ RGB-Element** gibt die gleitkommawerte an, die die roten, grünen und blauen Komponenten für diesen Punkt darstellen. Die Gammakurve verwendet keine Alphawerte. Sie verwenden die Zahl, die Sie von **NumGammaControlPoints** von [**DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) erhalten haben, um diese Anzahl von Elementen im **GammaCurve-Array zu** füllen. Jedes Element, das Sie im **GammaCurve-Array** platzieren, ist die Höhe für jeden Kontrollpunkt.

Beachten Sie im vorangehenden Diagramm, dass Sie nun die vertikale Platzierung der einzelnen Kontrollpunkt steuern können und dass Sie ein separates Steuerelement für Rot, Grün und Blau haben. Beispielsweise können Sie alle grünen und blauen Werte auf 0 (null) und die roten Werte auf einen aufsteigenden 1-1-Wert festlegen. In diesem Szenario zeigt das angezeigte Bild nur seine roten Teile an, und blau und grün werden schwarz dargestellt. Sie können auch eine absteigende Färbung für alle Farben festlegen, was zu einer invertierten Anzeige führt. Jeder Wert, den Sie im **GammaCurve-Array** platzieren, muss sich inklusiv innerhalb der Werte enthalten, die Sie aus den **MinConvertedValue-** und **MaxConvertedValue-Membern** von [**DXGI \_ GAMMA CONTROL CAPABILITIES \_ erhalten \_ haben.**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85))

## <a name="gamma-control-practicalities"></a>Praktische Praxis der Gammasteuerung

Die Gammasteuerelemente von DXGI gelten nur, solange die App vollbildig ist. Windows wird der vorherige Status der Anzeige wiederhergestellt, wenn die App beendet wird oder in den Fenstermodus zurückkehrt. Allerdings Windows der Gammazustand Ihrer App nicht wiederhergestellt, wenn die App wieder in den Vollbildmodus eintritt. Ihre App muss ihren Gammazustand explizit wiederherstellen, wenn sie wieder in den Vollbildmodus eintritt.

Nicht alle Adapter unterstützen die Gammasteuerung. Wenn ein Adapter die Gammasteuerung nicht unterstützt, ignoriert er Aufrufe zum Festlegen einer Gamma-Rampe.

Apps, die unter Remotedesktop ausgeführt werden, können Gamma überhaupt nicht steuern.

Der Mauszeiger reagiert in der Regel nicht auf die Gammaeinstellung, wenn er in der Hardware implementiert ist (wie die meisten sind).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch für DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
