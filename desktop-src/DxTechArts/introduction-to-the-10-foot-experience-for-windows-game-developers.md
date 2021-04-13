---
title: Einführung in die 10-Fuß-Darstellung für Windows-Spielentwickler
description: In diesem Artikel werden die 10-Fuß-Funktionen vorgestellt und die Liste der Dinge erläutert, die Sie zuerst zu diesem neuen Interaktionsmuster berücksichtigen sollten, auch wenn Sie nicht erwarten, dass Ihr Spiel auf diese Weise wiedergegeben wird.
ms.assetid: 126a0aae-6a7a-8cda-5748-c364e54c304e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4814c76aeefdadbe1fd8bf9dc4c21cd84612671
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104391141"
---
# <a name="introduction-to-the-10-foot-experience-for-windows-game-developers"></a>Einführung in die 10-Fuß-Darstellung für Windows-Spielentwickler

Eine wachsende Anzahl von Menschen verwendet Ihre persönlichen Computer auf ganz neue Weise. Wenn Sie eine typische Interaktion mit einem Windows-basierten Computer in Betracht ziehen, können Sie sich auf einem Schreibtisch mit einem Monitor und einer Maus und Tastatur (oder vielleicht einem Joystick Gerät) vorstellen. Dies wird als 2-Fuß-Erlebnis bezeichnet und ist immer noch das gängigste Szenario für Windows Gaming, aber es gibt noch einen weiteren Trend, den Sie wahrscheinlich mehr über die 10-Fuß-Darstellung erfahren, in der die Verwendung Ihres Computers als Unterhaltungsgerät mit Ausgabe an ein TV beschrieben wird. In diesem Artikel werden die 10-Fuß-Funktionen vorgestellt und die Liste der Dinge erläutert, die Sie zuerst zu diesem neuen Interaktionsmuster berücksichtigen sollten, auch wenn Sie nicht erwarten, dass Ihr Spiel auf diese Weise wiedergegeben wird. Ein Teil ihrer Kunden führt Ihr Windows-basiertes Spiel auf einem Computer aus, auf dem Windows Media Center ausgeführt wird – es ist besser, dass Sie wissen, wie diese Vorgehensweise aussehen wird, bevor Sie von ihren Kunden ausprobiert werden.

-   [Was ist Windows Media Center?](#what-is-windows-media-center)
-   [Die 10-Fuß-Darstellung](#the-10-foot-experience)
    -   [Installation](#installation)
    -   [Benutzereingabe](#user-input)
    -   [Anzeige](#display)
-   [Seitenverhältnis und Widescreen](#aspect-ratio-and-widescreen)
-   [Titel sicherer Bereich](#title-safe-region)
-   [NTSC-Vorschläge](#ntsc-suggestions)
    -   [Werte der RGB-Farbkomponente zwischen 16 und 235 einspannen](#clamp-the-rgb-color-component-values-between-16-and-235)
    -   [Vermeiden Sie ähnliche Farben, die möglicherweise identisch angezeigt werden.](#avoid-similar-colors-that-might-appear-identical)
    -   [Vermeiden von deutlichen Unterschieden im Gegensatz dazu](#avoid-sharp-differences-in-contrast)
-   [Zusammenfassung](#conclusion)

## <a name="what-is-windows-media-center"></a>Was ist Windows Media Center?

Windows Media Center kann als Schnittstelle zu den Multimediafunktionen des Host Computers fungieren. Die Website für dieses Feature, [Windows Media Center Home](https://windows.microsoft.com/windows/products/windows-media-center/), bietet eine gründliche Einführung und zeigt alle in der aktuellen Version verfügbaren guten Inhalte an. Media Center ist in Windows XP Media Center Edition, Windows Vista Home Premium, Windows Vista Ultimate und den meisten Editionen von Windows 7 enthalten.

In der Vergangenheit war die einzige Möglichkeit zum erwerben von Windows Media Center das Kaufen eines Media Center-PCs von einem Systemhersteller der Ebene 1, aber da Windows Media Center nun in zwei Editionen von Windows Vista enthalten ist, ist der potenzielle Marketplace nun viel größer.

## <a name="the-10-foot-experience"></a>Die 10-Fuß-Darstellung

Das Windows Media Center wurde entwickelt, um zu verstehen, dass Benutzer Windows für eine umfassende Unterhaltungsumgebung verwenden konnten. Es folgt, dass die meisten Benutzer die Interaktion mit Windows Media Center anders als herkömmliche Computeranwendungen bevorzugen. Wenn der Kunde den Computer im Lebensraum für die Unterhaltung verwendet, wird es wahrscheinlich sein, dass Video auf einem anderen Computer als einem herkömmlichen Computermonitor angezeigt wird: analoge Fernsehgeräte, digitale High-Definition-Fernsehgeräte und beliebig viele LCD-anzeigen. Diese Anzeigetypen werden normalerweise aus einer Entfernung von ungefähr 10 Metern angezeigt, sodass die Bezeichnung *10-Fuß-* Leistung aufweist.

Die 10-Fuß-Darstellung ist nicht auf Benutzer von Windows Media Center beschränkt. Es ist in den letzten Jahren üblich, dass Benutzer Ihre Arbeitsstation oder Ihren Notebook-Computer mit dem TV-und Audiosystem verbinden. Es ist immer häufiger üblich, dass Consumer-Geräte RGB-oder DVI-Verbindungen verfügbar machen, die Standard-Video-Ausgabeports auf Computern. Darüber hinaus sind S-videports eine typische Funktion von High-End-Videokarten und bieten eine einfache Möglichkeit, auf ein alternatives Anzeigegerät auszugeben.

Es gibt einige wichtige Entwurfs Richtlinien, die für eine angenehme 10-Fuß-Version berücksichtigt werden sollten: Installation, Benutzereingabe und Anzeige.

### <a name="installation"></a>Installation

Während der durchschnittlichen 2-Fuß-Darstellung liegt der Benutzer in der Entfernung des Computers. Wenn der Benutzer während des Starts oder Spiels ein Medium einfügen oder Umschalten muss, kann der Benutzer zumindest auf dem anderen Platz sitzen. Die durchschnittliche 10-Fuß-Umgebung versetzt den Computer vom Benutzer in den Raum, und aus diesem Grund zwingt alles, was den Benutzer physisch mit dem Computer interagieren muss, den Benutzer in den Raum zu bringen und den Raum zu überschreiten. Aus diesem Grund sollten Entwickler den Benutzer nicht zwingen, die Medien zu ändern. Es empfiehlt sich, eine komplette Installation der Anwendung auf der Festplatte zuzulassen.

### <a name="user-input"></a>Benutzereingaben

Ein weiteres Feature von Windows Media Center ist die Unterstützung einer Standard-Remote Steuerung, bei der es sich um das allgemein bevorzugte Eingabegerät handelt. Obwohl das Genre Ihres Spiel Titels größtenteils entscheidet, ob die Remote Steuerung für die Bereitstellung von Spiel Eingaben geeignet ist, können Sie es dem Benutzer trotzdem gestatten, das Spiel anzuhalten und auf in-Game-Menüs zuzugreifen, indem Sie die Remote Steuerung verwenden. Stellen Sie jedoch sicher, dass Sie dem Benutzer auch ermöglichen, die Menüs mithilfe des primären Spiel Eingabe Geräts zu steuern. Weitere Informationen zum Entwerfen und entwickeln für Windows Media Center und seine Geräte finden Sie im [Windows Media Center Software Development Kit](/previous-versions/msdn10/bb895967(v=msdn.10)) auf MSDN.

Vermeiden Sie eine physische Interaktion zwischen dem Benutzer und dem Computer oder seinen Peripheriegeräten. Es ist nicht wünschenswert, dass der Benutzer die Eingabe Controller während des Spiels ändern muss, da er wahrscheinlich nur in der Nähe des primären Eingabe Geräts ist.

Microsoft hat gemeinsame Gamepad-Controller für die Verwendung mit Windows und Xbox 360 erstellt – den Xbox 360-Controller für Windows und den Xbox 360-drahtlos Controller für Windows. Wenn Sie sicherstellen, dass Ihr Titel auf den gemeinsamen Controllern gut abgespielt wird, werden einige der Probleme, die mit dem Testen Ihres Spiels gegen potenzielle Eingabegeräte verbunden sind,

### <a name="display"></a>Anzeige

Die große Bandbreite potenzieller Anzeigegeräte gibt Ratschläge zur Herausforderung der Anzeige, und jede Art von Gerät weist besondere Vorsichtsmaßnahmen auf. Einige der Probleme im Zusammenhang mit bestimmten Anzeigetechnologien werden später in diesem Artikel vorgestellt. Unabhängig vom Videoausgabe Gerät ist es wichtig, dass Schriftarten und UI-Grafiken groß genug sind, um eine bessere Lesbarkeit bei einer Entfernung von 10 Metern zu erreichen. Beachten Sie auch, dass Antialiasing-Schriftarten eine bessere Lesbarkeit bieten.

Sie sollten auch horizontale Linien und statische Benutzeroberflächen Elemente mit einer Stärke oder einem Detail von einem Pixel vermeiden. Ältere Fernsehgeräte zeigen möglicherweise keine detaillierten Details an, und auch auf den neuesten Anzeigegeräten wird der Inhalt bei Ausführung im Zeilen Sprung Modus Flimmern, da eine einzelne Zeile von Pixel nur in der Hälfte der Zeit sichtbar ist. Um kleine Details zu ersetzen, stellen Sie fest, dass eine graue Linie mit zwei Pixeln dünner als eine weiße Linie mit 2 Pixeln ist. (Dies ist im Wesentlichen identisch mit der verwischt einer 1-Pixel-weißen Linie.)

## <a name="aspect-ratio-and-widescreen"></a>Seitenverhältnis und Widescreen

Seitenverhältnis beschreibt den breiten-und Höhen Anteil der Anzeige. Der Standard-TV-und Computermonitor zeigt ein Seitenverhältnis von 4:3 an. Dies bedeutet, dass für jede 4 Pixel, die entlang der Breite des Frame Puffers ausgeführt werden, drei Pixel entlang der Höhe vorhanden sind (manchmal auch als 1,33 dargestellt).

Mit der Einführung von HDTV ist ein Seitenverhältnis von 16:9 – auch als Wide Screen bezeichnet – zum Standard für die Zukunft des Fernseh ERS geworden. zusammen mit Enhanced Definition TV (EDTV) gibt es drei Anzeigemodi, die Sie wahrscheinlich treffen:

<dl> <dt>

<span id="480p_EDTV"></span><span id="480p_edtv"></span><span id="480P_EDTV"></span>480p-EDTV
</dt> <dd>

480 übergebene Überprüfungs Linien werden progressiv angezeigt. In diesem Modus kann entweder 4:3 (mit einer Frame Puffer Auflösung von 640 × 480) oder 16:9 (720 × 480) ausgegeben werden.

</dd> <dt>

<span id="720p_HDTV"></span><span id="720p_hdtv"></span><span id="720P_HDTV"></span>720p HDTV
</dt> <dd>

720 übergebene Überprüfungs Linien werden progressiv angezeigt. Dieser Modus ist immer 16:9 (1280 × 720).

</dd> <dt>

<span id="1080i_HDTV"></span><span id="1080i_hdtv"></span><span id="1080I_HDTV"></span>1080i-HDTV
</dt> <dd>

1080 übergebene Überprüfungs Linien sind Zeilen Sprung dargestellt. Dieser Modus ist immer 16:9 (1920 × 1080 oder 1920 × 540, wenn die damit-Felder separat gerendert werden).

</dd> </dl>

Wenn Ihr Spiel hart codiert ist, damit es in einem 4:3-Seitenverhältnis funktioniert, hat ein Benutzer, der Ihr Spiel auf einem 16:9-Bildschirm anzeigt, wahrscheinlich drei Optionen zum Anzeigen des Bilds, von denen keines besonders zufriedenstellend ist:

<dl> <dt>

<span id="Stretch"></span><span id="stretch"></span><span id="STRETCH"></span>Tre
</dt> <dd>

Der 4:3-Frame Puffer wird gestreckt, um die systemeigene Auflösung von 16:9 vollständig abzudecken, was dazu führt, dass Ihre Szenen Objekte breiter als gewünscht erscheinen. Einige Fernsehgeräte bieten zusätzliche streckungs Modi, bei denen versucht wird, das Seitenverhältnis in der Mitte der Anzeige beizubehalten und die Streckung allmählich auf der Bild Seite zu vergrößern.

</dd> <dt>

<span id="Center"></span><span id="center"></span><span id="CENTER"></span>Tagesstätte
</dt> <dd>

Der 4:3-Frame Puffer wird in der Mitte der Anzeige ungeverzerrt angezeigt, wobei die verbleibenden Pixel auf den Seiten mit voll Tonfarbe aufgefüllt werden.

</dd> <dt>

<span id="Zoom"></span><span id="zoom"></span><span id="ZOOM"></span>Skala
</dt> <dd>

Der 4:3-Frame Puffer wird auf einen 16:9-Bereich zugeschnitten, der dann die native Bildschirmauflösung ohne Verzerrung füllt. Beachten Sie, dass die Pixel oberhalb und unterhalb des Clip Rechtecks vollständig verworfen werden. Dies sind allgemeine Bereiche für die Benutzeroberflächen Elemente eines Spiels.

</dd> </dl>

Ein besserer Ansatz besteht darin, dem Spiel Unterstützung für die Breite des Bildschirms hinzuzufügen. Die wichtigste Änderung besteht darin, die Projektions Transformation der Spiel Kamera so festzulegen, dass Sie ein 16:9-Seitenverhältnis verwendet, das die Streckung der Streckung vermeidet. Auch wenn Sie den Hintergrund Puffer bei einer 4:3-Auflösung belassen, verbessert das Umschalten der Projektions Transformation zur Verwendung von 16:9 die wahrgenommene Genauigkeit des gerenderten Bilds erheblich. Natürlich wird das endgültige Bild gefiltert, um die 4:3-zurück-Puffer Auflösung hoch zu skalieren, um die systemeigene Bildschirmauflösung von 16:9 zu erreichen, aber dies ist ein weniger merkbares Element als die durch einen Konflikt zwischen den Seitenverhältnissen verursachte streckungs Verzerrung.

Die Kosten für das Rendern der Szene über die 16:9-Kamera können höher als eine 4:3 Kamera sein (auch bei identischen Auflösungen), da weitere Szenen Objekte in der umfassenderen Ansicht "Frustum" sichtbar sind. Sie sollten auch wissen, wie sich der erweiterbare sichtbare Bereich auf das-Spiel auswirken kann. Beispielsweise würde eine Spiel Kamera mit einem 16:9-Verhältnis mehr von ihrer Spiel Welt als eine 4:3-Kamera offenlegen.

Um die besten Ergebnisse für eine 16:9-Anzeige zu erzielen, sollten Sie in einen 16:9-Back-Puffer Rendering, aber dies erfordert offensichtlich mehr Pixel. Der Unterschied zwischen 640 × 480 und 720 × 480 beträgt fast 38.400 Pixel, ein Gewinn von 12,5%. Wenn Sie sich die Kosten für das Ausfüllen dieses größeren Bereichs leisten können, wird dringend empfohlen, dies zu tun.

## <a name="title-safe-region"></a>Title-Safe Region

Der Bild Rahmen Puffer kann teilweise vom Benutzer verdeckt werden, da einige Pixel um den Rahmen häufig durch die Vorderseite der Anzeige abgedeckt werden. Um sicherzustellen, dass wichtige Benutzeroberflächen Elemente auf einer Vielzahl von Anzeige Hardware sichtbar sind, sollten Sie die Anforderungen für den Titel sicheren Bereich des Zielanzeige Modus beachten. Bei nicht--HDTV-Modi ist der Titel sichere Bereich der interne 85-Prozentsatz des Frame Puffers, und für den HDTV-Modus ist der Titel sichere Bereich der innere 90 Prozent. Daher sollten Sie alle kritischen Benutzeroberflächen Elemente und Heads-Up-Anzeige Indikatoren innerhalb der inneren 85 Prozent des Frame Puffers aufbewahren, damit Sie über die aktuelle und zukünftige Anzeige Hardware verfügen.

## <a name="ntsc-suggestions"></a>NTSC-Vorschläge

Da NTSC der gängigste Videostandard im USA für die Benutzer Anzeige Hardware ist, ist es wichtig, sich über einige der Richtlinien zu informieren, die Sie für Ihr Ausgabe Image befolgen sollten.

### <a name="clamp-the-rgb-color-component-values-between-16-and-235"></a>Werte der RGB-Farbkomponente zwischen 16 und 235 einspannen

Farben außerhalb des Bereichs von 16-235 können sicherlich an ein NTSC-TV gesendet werden, aber es ist wahrscheinlich, dass diese Werte außerhalb des gültigen Bereichs als Audiodaten interpretiert werden. Dies wird häufig als *audiobuzz* bezeichnet und ist am offensichtlichsten, wenn Ihre Inhalte über einen voll tonweißen Hintergrund dargestellt werden. Sie können die Ausgabe Farb Klammer innerhalb eines Pixelshaders problemlos implementieren.

### <a name="avoid-similar-colors-that-might-appear-identical"></a>Vermeiden Sie ähnliche Farben, die möglicherweise identisch angezeigt werden.

Der NTSC-Farb Farbskala bietet nicht dieselbe Palette wie ein typischer Computermonitor. vermeiden Sie daher die Verwendung ähnlicher Farben, wenn das Spiel erfordert, dass der Spieler den Unterschied erkennt.

### <a name="avoid-sharp-differences-in-contrast"></a>Vermeiden von deutlichen Unterschieden im Gegensatz dazu

Obwohl diese Richtlinie nicht immer praktikabel ist, können Sie einige der Farb Blutungs Ärgernisse in NTSC-anzeigen (auch als *Chroma Crawl* bezeichnet) verringern, indem Sie die richtigen Farben für die Vordergrund-und Hintergrundelemente der Benutzeroberfläche auswählen. weißer Text auf einem farbigen Hintergrund liefert wahrscheinlich bessere Ergebnisse als Kontrastfarben.

## <a name="conclusion"></a>Zusammenfassung

Dieser Artikel bietet einen Überblick über die 10-Fuß-Darstellung aus der Perspektive eines Windows-Spielentwicklers, aber es handelt sich nicht um eine umfassende Umfrage. Sie sollten diese Themen weiter untersuchen, wenn Sie einen Windows-Spieltitel entwickeln (auch wenn dieser nicht für die Verwendung mit Windows Media Center gedacht ist). Der wahre Test besteht darin, das Spiel auf einer Vielzahl von Video Anzeigen auszuprobieren, um sicherzustellen, dass Ihr Spiel eine angenehme benutzerfreundliche Darstellung bietet. Basierend auf der typischen Lebensspanne eines Windows-basierten Spiels und der vorhergesagten Zunahme der Verwendung von Windows Media Center ist es fast garantiert, dass ein Spiel, das Sie heute freigeben, Teil der 10-Fuß-Umgebung eines Benutzers ist – ob Kunden Ihr Spiel von den Komfort von Couches spielen können oder ob Sie auf dem Tisch sitzen müssen.

 

 