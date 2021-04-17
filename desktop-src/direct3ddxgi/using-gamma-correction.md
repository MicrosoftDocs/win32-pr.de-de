---
description: Gammakorrektur (oder Gamma) ist der Name eines nichtlinearen Vorgangs, den Systeme zum Codieren und Decodieren von Pixelwerten in Bildern verwenden.
ms.assetid: 97ACDAE3-514E-4AAF-A27D-E5FFC162DB2A
title: Verwenden von Gammakorrektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c940db1a94fb41e9babecbeb3075aa9e01b3732
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104553908"
---
# <a name="using-gamma-correction"></a>Verwenden von Gammakorrektur

Gammakorrektur (oder Gamma) ist der Name eines nichtlinearen Vorgangs, den Systeme zum Codieren und Decodieren von Pixelwerten in Bildern verwenden.

-   [Was ist Gamma und wozu dient es?](#what-is-gamma-and-what-is-it-for)
-   [Hintergrund von Gamma unter Windows](#background-of-gamma-on-windows)
-   [Entwicklung von Anzeige Hardware](#evolution-of-display-hardware)
-   [Gamma-Steuerungsfunktionen in DXGI](#gamma-control-capabilities-in-dxgi)
-   [Festlegen von Gamma Control mit DXGI](#setting-gamma-control-with-dxgi)
-   [Praktikabilität von Gamma Steuerelementen](#gamma-control-practicalities)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-gamma-and-what-is-it-for"></a>Was ist Gamma und wozu dient es?

Am Ende der Grafik Pipeline gibt es eine kleine Hardware, mit der die Pixelwerte dynamisch transformiert werden können, wenn das Image den Computer verlässt, um das Überwachungs Kabel zu erreichen. Diese Hardware verwendet in der Regel eine Nachschlage Tabelle, um die Pixel zu transformieren. Diese Hardware verwendet die roten, grünen und blauen Werte aus der-Oberfläche, die angezeigt werden, um die von Gamma korrigierten Werte in der Tabelle nachzuschlagen und die korrigierten Werte dann an den Monitor anstelle der tatsächlichen Oberflächen Werte zu senden. Diese Nachschlage Tabelle ist also eine Möglichkeit, beliebige Farben durch andere Farben zu ersetzen. Obwohl die Tabelle diese Menge an Leistung aufweist, besteht die typische Verwendung darin, Bilder zu optimieren, um Unterschiede in der Reaktion des Monitors auszugleichen. Die Antwort des Monitors ist die Funktion, die den numerischen Wert der roten, grünen und blauen Komponenten eines Pixels mit der angezeigten Helligkeit dieses Pixels verknüpft.

Diese Tabelle wurde für gedacht, aber Spieleentwickler fanden kreative Verwendungsmöglichkeiten, wie z. b. das Blinken des gesamten Bildschirms für die psychologische Wirkung. In modernen Spiel-Apps bieten wir in der Regel weitere Möglichkeiten, um solche Aufgaben durchzuführen. Es wird empfohlen, dass Sie die Gamma Tabelle unverändert lassen, da Sie möglicherweise verwendet wird, um die Antwort des Monitors zu kalibrieren. durch eine großflächige Änderung an der Gamma Rampe wird diese sorgfältige Kalibrierung zerstört.

Die Wissenschaft zur Bestimmung der Gammakorrektur ist komplex und wird hier nicht dargestellt, außer um zu erkennen, wo der Name "Gamma" stammt. Eine CRT-Antwort (d. h. die Antwort eines alten Messers) ist eine komplexe Funktion, aber die Physik dieser Monitore bedeutet, dass Sie eine Antwort aufweisen, die durch diese Energie Funktion grob dargestellt werden kann:

Helligkeit (Eingabe) = Eingabe<sup>Gamma</sup>

Der Gamma Wert liegt in der Regel nahe dem Wert 2,0. LCD-Monitore und alle anderen neueren Technologien werden speziell so konzipiert, dass Sie eine ähnliche Reaktion aufweisen, sodass die gesamte Software und Images für diese neuen Technologien nicht neu zugeordnet werden müssen. Der sRGB-Standard deklariert, dass dieser Gamma Wert exakt 2,2 ist, und dieser Wert wurde zu einem weit verbreiteten Standard.

Das menschliche Auge verfügt auch über eine Response-Funktion, die die CRT-Funktion ungefähr einkehrt. Dies bedeutet, dass die wahrgenommene Helligkeit eines Pixels bei den RGB-Werten in diesem Pixel sehr ungefähr linear verläuft.

Da ein Gamma-Wert von 2,2 ein de-facto-Standard geworden ist, müssen wir uns in der Regel nicht zu viel über die in dieser Tabelle codierte Gamma Kurve Gedanken machen und Sie als eine lineare 1-zu-Eins-Zuordnung belassen. Die ordnungsgemäße Farb Übereinstimmung erfordert natürlich eine besondere Sorgfalt bei dieser Funktion, aber diese Erörterung geht über den Rahmen dieses Themas hinaus. Windows enthält ein Tool, mit dem Benutzer Ihre Anzeige in Gamma 2,2 kalibrieren können, und dieses Tool verwendet die Hardware der Nachschlage Tabelle, um eine sorgfältig ausgewählte, feine Optimierung für Ihre Computer abzuleiten. Benutzer können dieses Tool ausführen, indem Sie nach "Kalibrieren der Farbe" suchen. Es gibt auch klar definierte Farbprofile für bestimmte Monitore, die diesen Prozess automatisieren. Mit dem Tool "Kalibrieren der Farbe" können diese neueren Monitore erkannt werden, und die Benutzer werden darüber informiert, dass die Kalibrierung bereits vorhanden ist.

Dieses Konzept der Codierung eines Energiegesetzes in Farbwerte ist auch an anderer Stelle in der Grafik Pipeline hilfreich, insbesondere in Texturen. Bei Texturen ist die Genauigkeit bei dunkleren Farben aufgrund der logarithmischen Menschen Perspektive, über die wir soeben gesprochen haben, genauer. Die sorgfältige Behandlung von Gamma in diesem Teil der Pipeline ist wichtig. Weitere Informationen finden Sie unter " [Daten für den Farbraum](converting-data-color-space.md)"

Im weiteren Verlauf dieses Themas liegt der Schwerpunkt auf der Gammakorrektur in diesem letzten Teil der Pipeline zwischen den Frame Puffer Daten und dem Monitor. Wenn Sie einen Kalibrierungs-Assistenten schreiben oder besondere Effekte in einer voll Bild-app erstellen möchten, bei der ein Nachbearbeitungsschritt nicht praktikabel ist, finden Sie hier die Informationen, die Sie benötigen.

## <a name="background-of-gamma-on-windows"></a>Hintergrund von Gamma unter Windows

Windows-Computer verfügen in der Regel über eine Gamma Tabelle, bei der es sich um eine Nachschlage Tabelle handelt, bei der es sich um ein Dreieck von Bytes handelt Diese drei-und-drei-Bytes sind 768 (256 x 3) RAM. Dies ist in Ordnung, wenn das Anzeige Format ein Dreier von RGB-Byte-Werten enthält, jedoch nicht Ausdrucks genug ist, um die Transformationen zu beschreiben, die Sie möglicherweise wünschen, wenn das Anzeige Format einen größeren Bereich als \[ 0, 1 aufweist \] , z. b. Gleit Komma Werte. Die APIs in Windows, die Gamma steuern, verfolgten eine Weiterentwicklung, da Anzeige Formate komplexer werden.

Die ersten Windows-APIs für die Gamma Steuerung sind die Windows Graphics Device Interface (GDI) [**setdevicegammaramp**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp) und [**getdevicegammaramp**](/windows/win32/api/wingdi/nf-wingdi-getdevicegammaramp). Diese APIs können mit 3 256-Eingabe Arrays von Wörtern verwendet werden, wobei jedes Wort eine Null bis eins darstellt, dargestellt durch die Wort Werte 0 und 65535. Die zusätzliche Genauigkeit eines Worts ist in den eigentlichen Hardware Nachschlage Tabellen normalerweise nicht verfügbar, aber diese APIs waren als flexibel gedacht. Diese APIs erlauben im Gegensatz zu den anderen, die weiter unten in diesem Abschnitt beschrieben werden, nur eine kleine Abweichung von einer Identitäts Funktion. Tatsächlich muss jeder Eintrag in der Rampe innerhalb von 32768 des Identitäts Werts liegen. Diese Einschränkung bedeutet, dass keine app die Anzeige vollständig schwarz oder in eine andere nicht lesbare Farbe umwandeln kann.

Bei der nächsten API handelt es sich um das [**setgammaramp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)von Microsoft Direct3D 9, bei dem es sich um das gleiche Muster und Datenformat wie [**setdevicegammaramp**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp)handelt. Der Standardwert der Direct3D 9-Gamma-Rampe ist nicht besonders nützlich. Dabei handelt es sich um eine Anlauf Folge von Wörtern, die mit 0-255 und nicht 0-65535 initialisiert werden, auch wenn die API in Bezug auf 0-65535 definiert ist.

Die neueste API ist " [**idxgioutput:: setgammacontrol**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol)". Diese API verfügt über ein flexibleres Schema zum Ausdrücken von Gamma Control, wie es den erweiterten DXGI-Anzeige Formaten entspricht, einschließlich zehn ganzzahligen Bits-pro-Channel-und 16-Bit-Gleit Komma Formaten sowie des \_ erweiterten Bereichs Formats XR-Bias.

Alle diese APIs arbeiten auf derselben Hardware und ändern dieselben Werte. Die APIs Direct3D 9 und DXGI sind schreibgeschützt. Sie können den Wert der Hardware nicht lesen, ändern und dann festlegen. Sie können nur die-Rampe festlegen. Außerdem können Sie nur Gamma festlegen, wenn die APP den Vollbildmodus hat. Diese Einschränkung stellt eine andere Möglichkeit dar, um sicherzustellen, dass der Desktop immer lesbar ist. Das heißt, die APP kann Ihre eigene Anzeige stören, aber Windows stellt die vorherige Gamma-Rampe wieder her, wenn die APP den Vollbildmodus verliert (z. b. über Alt + Tab oder STRG + ALT + ENTF).

## <a name="evolution-of-display-hardware"></a>Entwicklung von Anzeige Hardware

In einigen neueren Monitoren kann eine breite Palette von Intensitäten angezeigt werden. Wenn das Anzeige Format jedoch nur Werte zwischen 0 (null) und eins darstellen kann, muss die Anzeige NULL dem dunkelsten Wert und einem Wert mit dem besten Wert zuordnen. Dieser hervorragende Wert ist möglicherweise für eine bequeme Anzeige von Webseiten mit schwarzem Text auf weißem Hintergrund viel zu hell, eignet sich jedoch hervor artig für übermäßig helle besondere Effekte, wie z. b. das Anzeigen des Sonnenlichts, das aus einem-oder-Blitz hervorgeht. Daher benötigen wir eine Möglichkeit, diese umfassenderen Bereiche auszudrücken. DXGI 1,1 und höher enthält Anzeige Format Werte, mit denen 1,0 einen bequemen weißen Wert darstellen und größere Anzeige Format Werte für über helle besondere Effekte reserviert. DXGI 1,1 unterstützt zwei Anzeige Formate, die diese umfassenderen Werte Ausdrücken können: DXGI \_ \_ -Format R10G10B10 \_ XR \_ Bias \_ a2 \_ unorm und 16-Bit-Gleit Komma Zahl. Eine vollständige Erläuterung dieser Formate finden Sie unter [Details zum erweiterten Format](/windows-hardware/drivers/display/details-of-the-extended-format). Als nächstes sehen wir uns an, warum die [**idxgioutput:: setgammacontrol**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) -Gamma-API von DXGI Pixel-Werte größer als 1,0 benötigt.

## <a name="gamma-control-capabilities-in-dxgi"></a>Gamma-Steuerungsfunktionen in DXGI

Mit DXGI kann der Anzeigetreiber seine Gamma Steuerelemente als schrittweise lineare Funktion Ausdrücken. Diese schrittweise lineare Funktion wird durch die Steuerungs Punkte dieser Funktion, den Wertebereich, in den die Funktion konvertiert werden kann, und einen zusätzlichen optionalen Skalierungs-und Offset Vorgang definiert, der nach der Konvertierung angewendet werden kann. Eine APP kann die [**idxgioutput:: getgammacontrolfunktionalitäten**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) -Methode aufrufen, um alle diese Steuerungsfunktionen in der Struktur der [**DXGI- \_ Gamma \_ Steuerelement \_ Funktionen**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) abzurufen.

Dieses Diagramm zeigt eine lineare Funktion mit nur vier Steuerungs Punkten.

![lineare Funktion der Gammakorrektur](images/gamma-linear-function.png)

DXGI definiert Steuerungs Punkte an ihrer Position entlang der Oberflächen farbachse. Im vorangehenden Diagramm sind die Speicherorte der Steuerungs Punkte 0, 0,5, 0,75 und 1,0. Diese Steuerungs Punkte geben an, dass die Hardware Werte im Bereich von 0 bis 1,0 konvertieren kann. DXGI listet diese Steuerungs Punkte im **controlpointpositions** -Array-Member der [**DXGI- \_ Gamma \_ Steuerungs \_ Funktionen**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) auf und deklariert Sie immer in aufsteigender Reihenfolge. DXGI füllt nur die ersten Elemente des **controlpointpositions** -Arrays aus und gibt die Anzahl der Elemente mit dem **numgammacontrolpoints** -Member der **DXGI- \_ Gamma \_ Steuerungs \_ Funktionen** an. Wenn **numgammacontrolpoints** kleiner als 1025 ist, lässt DXGI den Rest der **controlpointpositions** -Elemente nicht definiert.

Die von diesem Diagramm dargestellte Hardware kann Werte in einen Bereich von 0 bis 1,25 konvertieren. Daher legt DXGI die Member **minconvertedvalue** und **maxconvertedvalue** auf 0,0 f bzw. 1,25 f fest.

DXGI legt den **scaleandoffsetsupported** -Member der [**DXGI- \_ Gamma \_ Steuerungs \_ Funktionen**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) fest, um anzugeben, ob die Hardware die Skalierungs-und Offset Funktion unterstützt. Wenn die Hardware die Skalierung und den Offset unterstützt, behält Sie eine einfache 1-zu-eins-Nachschlage Tabelle bei und passt dann die Ausgabe der Tabelle an, um die Ausgabe auf einen Bereich größer als \[ 0, 1 auszudehnen \] . Die Hardware skaliert zuerst die Werte, die aus der Nachschlage Tabelle stammen, und versetzt Sie dann Offsets.

> [!Note]  
> Verschiedene Monitore, die mit demselben Computer verbunden sind, verfügen möglicherweise über unterschiedliche Gamma Steuerungsfunktionen. Darüber hinaus können sich die Gamma-Steuerelement Funktionen in Abhängigkeit vom Anzeigemodus der Ausgabe ändern. Daher wird empfohlen, dass Sie immer [**idxgioutput:: getgammacontrolfunktionen**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) aufrufen, um die Gamma-Steuerungsfunktionen abzufragen, nachdem Ihre APP in den Vollbildmodus wechselt.

 

Mithilfe dieser Funktions Werte für Gamma Steuerelemente können Sie Steuerungs Werte ableiten, die Sie dann mithilfe der [**idxgioutput:: setgammacontrol**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) -API festlegen können.

## <a name="setting-gamma-control-with-dxgi"></a>Festlegen von Gamma Control mit DXGI

Um Gamma Steuerelemente festzulegen, übergeben Sie einen Zeiger an eine [**DXGI- \_ Gamma \_ Steuer**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) Elementstruktur, wenn Sie die [**idxgioutput:: setgammacontrol**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) -API aufrufen.

Sie legen die Dezimalstellen und **Offset** -Member des [**DXGI \_ Gamma \_ Control**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) fest, um die Skalierungs **-und Offset** Werte anzugeben, auf die die Hardware auf die Werte angewendet werden soll, die Sie aus der Nachschlage Tabelle abrufen. Sie können die **Skalierung** auf 1 und den **Offset** auf NULL festlegen (d. h. eine Skalierung um eins hat keine Auswirkungen und ein Offset von NULL hat keine Auswirkung), wenn Sie die Skalierungs-und Offset Funktion nicht verwenden möchten, oder wenn die Hardware nicht über diese Funktion verfügt.

Sie legen das **gammacurve** -Arraymember des [**DXGI- \_ Gamma- \_ Steuer**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) Elements auf eine Liste von [**DXGI \_ RGB**](/previous-versions/windows/desktop/legacy/bb173071(v=vs.85)) -Strukturen für die Punkte in der Gamma Kurve fest. Jedes **DXGI \_ RGB** -Element gibt die float-Werte an, die die roten, grünen und blauen Komponenten für diesen Punkt darstellen. Die Gamma Kurve verwendet keine Alpha-Werte. Verwenden Sie die Zahl, die Sie aus den **numgammacontrolpoints** der [**DXGI- \_ Gamma \_ Steuerungs \_ Funktionen**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) erhalten haben, um diese Anzahl von Elementen im **gammacurve** -Array auszufüllen. Jedes Element, das Sie im **gammacurve** -Array platzieren, ist die Höhe für jeden Steuerungspunkt.

Beachten Sie im vorangehenden Diagramm, dass Sie nun die vertikale Platzierung der einzelnen Kontrollpunkte steuern können, und Sie haben ein separates Steuerelement für Rot, grün und blau. Beispielsweise können Sie alle grünen und blauen Werte auf 0 (null) festlegen und die roten Werte auf eine aufsteigende Treppe zwischen null und eins festlegen. In diesem Szenario zeigt das angezeigte Bild nur seine roten Teile, wobei blau und Grün als schwarz angezeigt werden. Sie können auch für alle Farben eine absteigende Treppe festlegen, die zu einer umgekehrten Anzeige führt. Jeder Wert, den Sie im **gammacurve** -Array platzieren, muss in den Werten enthalten sein, die Sie aus den Membern **minconvertedvalue** und **maxconvertedvalue** der [**DXGI- \_ Gamma \_ Steuerungs \_ Funktionen**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85))abgerufen haben.

## <a name="gamma-control-practicalities"></a>Praktikabilität von Gamma Steuerelementen

Die Gamma Steuerelemente von DXGI gelten nur, solange die APP voll Bildschirm ist. Windows stellt den vorherigen Zustand der Anzeige wieder her, wenn die APP beendet wird oder zum Fenstermodus zurückkehrt. Windows stellt den Gamma Status Ihrer APP jedoch nicht wieder her, wenn die APP erneut in den Vollbildmodus wechselt. Ihre APP muss ihren Gamma Zustand explizit wiederherstellen, wenn Sie den Vollbildmodus wieder eingibt.

Die Gamma Steuerung wird nicht von allen Adaptern unterstützt. Wenn ein Adapter kein Gamma-Steuerelement unterstützt, werden Aufrufe zum Festlegen einer Gamma-Rampe ignoriert.

Apps, die unter Remote Desktop ausgeführt werden, können Gamma überhaupt nicht kontrollieren.

Der Mauszeiger, wenn er in der Hardware (in den meisten Fällen) implementiert ist, antwortet in der Regel nicht auf die Gamma-Einstellung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmier Handbuch für DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
