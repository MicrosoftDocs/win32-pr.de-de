---
title: Einführung in die 10-Fuß-Erfahrung für entwickler von Windows Spielen
description: In diesem Artikel wird die 10-Fuß-Erfahrung vorgestellt und die Liste der Punkte erläutert, die Sie zuerst über dieses neue Interaktionsmuster berücksichtigen sollten, auch wenn Sie nicht erwarten, dass Ihr Spiel auf diese Weise wiedergegeben wird.
ms.assetid: 126a0aae-6a7a-8cda-5748-c364e54c304e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049cbbe839509681f8f8629144511853d2984bbabafbf989611d1ed1db32e686
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963620"
---
# <a name="introduction-to-the-10-foot-experience-for-windows-game-developers"></a>Einführung in die 10-Fuß-Erfahrung für entwickler von Windows Spielen

Eine wachsende Anzahl von Personen verwendet ihre PCs auf völlig neue Weise. Wenn Sie sich eine typische Interaktion mit einem Windows-basierten Computer vorstellen, möchten Sie wahrscheinlich an einem Tisch mit einem Monitor und mit einer Maus und Tastatur (oder vielleicht einem Gerätegerät) an einem Arbeitsplatz platzen. dies wird als 2-Fuß-Erfahrung bezeichnet und ist immer noch das häufigste Szenario für Windows Gaming, aber es gibt einen weiteren Trend, von dem Sie wahrscheinlich mehr hören werden: die 10-Fuß-Erfahrung, die die Verwendung Ihres Computers als Unterhaltungsgerät mit Ausgabe an einen Fernseher beschreibt. In diesem Artikel wird die 10-Fuß-Erfahrung vorgestellt und die Liste der Punkte erläutert, die Sie zuerst über dieses neue Interaktionsmuster berücksichtigen sollten, auch wenn Sie nicht erwarten, dass Ihr Spiel auf diese Weise wiedergegeben wird. Ein Teil Ihrer Kunden führt Ihr Windows-basiertes Spiel auf einem Computer aus, auf dem Windows Media Center ausgeführt wird. Es ist besser, dass Sie wissen, wie diese Erfahrung aussehen wird, bevor Ihre Kunden es ausprobieren.

-   [Was ist Windows Media Center?](#what-is-windows-media-center)
-   [Die 10-Fuß-Benutzeroberfläche](#the-10-foot-experience)
    -   [Installation](#installation)
    -   [Benutzereingabe](#user-input)
    -   [Anzeige](#display)
-   [Seitenverhältnis und Widescreen](#aspect-ratio-and-widescreen)
-   [Title-Tresor Region](#title-safe-region)
-   [NTSC-Vorschläge](#ntsc-suggestions)
    -   [Zusammenfügen der RGB-Farbkomponentenwerte zwischen 16 und 235](#clamp-the-rgb-color-component-values-between-16-and-235)
    -   [Vermeiden sie ähnliche Farben, die möglicherweise identisch erscheinen.](#avoid-similar-colors-that-might-appear-identical)
    -   [Vermeiden von starken Unterschieden im Kontrast](#avoid-sharp-differences-in-contrast)
-   [Zusammenfassung](#conclusion)

## <a name="what-is-windows-media-center"></a>Was ist Windows Media Center?

Windows Media Center kann als Schnittstelle zu den Multimediafunktionen des Hostcomputers fungieren. Die Website für dieses [Feature, Windows Media Center Home,](https://windows.microsoft.com/windows/products/windows-media-center/)bietet eine umfassende Einführung und zeigt alle guten Inhalte, die in der neuesten Version verfügbar sind. Media Center ist in Windows XP Media Center Edition, Windows Vista Home Premium, Windows Vista Ultimate und den meisten Editionen von Windows 7 enthalten.

In der Vergangenheit bestand die einzige Möglichkeit, Windows Media Center zu erhalten, darin, einen Media Center-PC von einem Tier-1-Systemhersteller zu erwerben. Da jedoch Windows Media Center jetzt in zwei Editionen von Windows Vista enthalten ist, ist der potenzielle Marketplace jetzt viel größer.

## <a name="the-10-foot-experience"></a>Die 10-Fuß-Benutzeroberfläche

Windows Media Center wurde auf die Idee ausgelegt, dass Benutzer Windows für ein umfangreiches Unterhaltungserlebnis im Leben nutzen können. Daraus folgt, dass die meisten Benutzer es vorziehen, anders mit Windows Media Center zu interagieren als mit herkömmlichen Computeranwendungen. Wenn der Kunde beispielsweise den Computer im Haus zur Unterhaltung verwendet, wird wahrscheinlich ein Video auf einem anderen Bildschirm als einem herkömmlichen Computermonitor angezeigt: analoge TVs, digitale High-Definition-TVs und eine beliebige Anzahl von DISPLAYS sind wahrscheinlich Kandidaten. Diese Arten von Anzeigen werden in der Regel aus einer Entfernung von ungefähr 10 Fuß angezeigt, sodass die Bezeichnung *10-Fuß-Erfahrung hat.*

Die 10-Fuß-Benutzeroberfläche ist nicht auf Benutzer von Windows Media Center beschränkt. Es ist in den letzten Jahren üblich, dass Benutzer ihre Arbeitsstation oder ihren Notebookcomputer mit ihrem TV- und Audiosystem verbinden. Es kommt immer häufiger vor, dass Consumeranzeigegeräte RGB- oder DVI-Verbindungen verfügbar machen, die Standard-Videoausgabeports auf Computern. Darüber hinaus sind S-Video-Ports ein typisches Feature von High-End-Grafikkarten und bieten eine einfache Möglichkeit, auf einem alternativen Anzeigegerät auszugeben.

Es gibt einige wichtige Entwurfsrichtlinien, die für eine ansprechende 10-Fuß-Benutzeroberfläche berücksichtigt werden sollten: Installation, Benutzereingabe und Anzeige.

### <a name="installation"></a>Installation

Während der durchschnittlichen 2-Fuß-Benutzeroberfläche befindet sich der Benutzer innerhalb der Reichweite des Computers. Wenn der Benutzer während des Start- oder Spielvorgangs Medien einfügen oder wechseln muss, kann der Benutzer mindestens auf dem Platz bleiben. Die durchschnittliche 10-Fuß-Erfahrung versetzt den Computer durch den Raum des Benutzers. Daher zwingt alles, was den Benutzer zur physischen Interaktion mit dem Computer benötigt, den Benutzer, den Raum auf- und zu passieren. Aus diesem Grund sollten Entwickler vermeiden, den Benutzer zum Wechseln von Medien zu zwingen. Erwägen Sie, eine vollständige Installation Ihrer Anwendung auf der Festplatte zuzulassen.

### <a name="user-input"></a>Benutzereingaben

Ein weiteres Feature von Windows Media Center ist die Unterstützung für eine Standard-Remotesteuerung, die das im Allgemeinen bevorzugte Eingabegerät ist. Obwohl das Genre Ihres Spieltitels größtenteils entscheidet, ob die Remotesteuerung für die Bereitstellung von Spieleingaben geeignet ist, sollten Sie dem Benutzer dennoch erlauben, das Spiel anzuhalten und über die Remotesteuerung auf Die Menüs im Spiel zuzugreifen. Stellen Sie jedoch sicher, dass Sie dem Benutzer auch erlauben, die Menüs mithilfe des primären Spieleingabegeräts zu steuern. Weitere Informationen zum Entwerfen und Entwickeln für Windows Media Center und dessen Geräte finden Sie [unter Windows Media Center Software Development Kit](/previous-versions/msdn10/bb895967(v=msdn.10)) auf MSDN.

Vermeiden Sie physische Interaktionen zwischen dem Benutzer und dem Computer oder seinen Peripheriegeräten. Es ist nicht wünschenswert, dass der Benutzer während des Gamings die Eingabecontroller ändern muss, da er sich wahrscheinlich nur in der Nähe des primären Eingabegeräts befindet.

Microsoft hat allgemeine Gamepadcontroller für die Verwendung mit Windows und Xbox 360 erstellt– die Xbox 360 Controller für Windows und die Xbox 360 Wireless Controller für Windows. Wenn Sie sicherstellen, dass Ihr Titel auf den gängigen Controllern gut wiedergegeben wird, können Sie einige der Schwierigkeiten im Zusammenhang mit dem Testen Ihres Spiels mit potenziellen Eingabegeräten vereinfachen.

### <a name="display"></a>Anzeige

Die vielzahl von potenziellen Anzeigegeräten bietet Hinweise zur Anzeige von Herausforderungen, und jeder Gerätetyp weist besondere Einschränkungen auf. Einige Probleme im Zusammenhang mit bestimmten Anzeigetechnologien werden später in diesem Artikel vorgestellt. Unabhängig vom Videoausgabegerät ist es wichtig, dass Schriftarten und Benutzeroberflächengrafiken groß genug sind, um eine komfortable Lesbarkeit in einer Entfernung von 10 Fuß zu erreichen. Beachten Sie auch, dass gealiaste Schriftarten im Allgemeinen eine bessere Lesbarkeit bieten.

Sie sollten auch horizontale Linien und statische Benutzeroberflächenelemente mit einer Einpixelstärke oder Details vermeiden. Ältere Fernsehgeräte zeigen möglicherweise keine detaillierten Informationen an, und selbst auf den neuesten Anzeigegeräten flackert Ihr Inhalt, wenn er im Interlacingmodus ausgeführt wird, da eine einzelne Pixelzeile nur die Hälfte der Zeit sichtbar ist. Als Ersatz für kleine Details erkennen Sie, dass eine graue 2-Pixel-Linie schlanker als eine 2-Pixel-Weißlinie erscheint. (Dies entspricht im Wesentlichen dem Weichzeichnen einer weißen 1-Pixel-Linie.)

## <a name="aspect-ratio-and-widescreen"></a>Seitenverhältnis und Widescreen

Das Seitenverhältnis beschreibt die Breite und den Höhenanteil der Anzeige. Standard-TV- und Computermonitoranzeigen weisen ein Seitenverhältnis von 4:3 auf, was bedeutet, dass sich für alle vier Pixel, die entlang der Breite des Rahmenpuffers ausgeführt werden, 3 Pixel entlang der Höhe befinden (manchmal auch als 1,33 dargestellt).

Mit der Einführung von QUOTE hat sich ein Seitenverhältnis von 16:9 ( auch als Breitbildschirm bezeichnet) zum Standard für die Zukunft des Tv entwickelt, und zusammen mit dem TV mit erweiterter Definition (Enhanced Definition TV, EDTV) gibt es drei Anzeigemodi, auf die Sie wahrscheinlich stoßen werden:

<dl> <dt>

<span id="480p_EDTV"></span><span id="480p_edtv"></span><span id="480P_EDTV"></span>480p EDTV
</dt> <dd>

480 Scanzeilen werden progressiv angezeigt. Dieser Modus kann entweder 4:3 (mit einer Framepufferauflösung von 640×480) oder 16:9 (720×480) ausgeben.

</dd> <dt>

<span id="720p_HDTV"></span><span id="720p_hdtv"></span><span id="720P_HDTV"></span>720p- UND 720p-720p
</dt> <dd>

720 Scanzeilen werden progressiv dargestellt. Dieser Modus ist immer 16:9 (1280×720).

</dd> <dt>

<span id="1080i_HDTV"></span><span id="1080i_hdtv"></span><span id="1080I_HDTV"></span>1.080i- UND -REGEL
</dt> <dd>

1080 Scanzeilen mit Zeilensprung dargestellt. Dieser Modus ist immer 16:9 (1920×1080 oder 1920×540, wenn die Interlacefelder separat gerendert werden.

</dd> </dl>

Wenn Ihr Spiel hart codiert ist, um in einem Seitenverhältnis von 4:3 zu arbeiten, verfügt ein Benutzer, der Das Spiel auf einem 16:9-Bildschirm anzeigt, wahrscheinlich über drei Optionen zum Anzeigen des Bilds, von denen keine besonders zufrieden ist:

<dl> <dt>

<span id="Stretch"></span><span id="stretch"></span><span id="STRETCH"></span>Strecke
</dt> <dd>

Der 4:3-Framepuffer wird gestreckt, um die native Auflösung von 16:9 der Anzeige perfekt abzudecken, sodass Ihre Szenenobjekte breiter als gewünscht angezeigt werden. Einige TVs bieten zusätzliche Stretchingmodi, die versuchen, das Seitenverhältnis in der Nähe der Mitte des Bildschirms beizubehalten und die Streckung an den Bildseiten schrittweise zu erhöhen.

</dd> <dt>

<span id="Center"></span><span id="center"></span><span id="CENTER"></span>Center
</dt> <dd>

Der 4:3-Framepuffer wird in der Mitte der Anzeige ungestortiert angezeigt, wobei volltonfarbene Balken die verbleibenden Pixel an den Seiten füllen.

</dd> <dt>

<span id="Zoom"></span><span id="zoom"></span><span id="ZOOM"></span>Zoom
</dt> <dd>

Der 4:3-Framepuffer wird auf einen 16:9-Bereich zugeschnitten, der dann die native Anzeigeauflösung ohne Verzerrung ausfüllt. Beachten Sie, dass die Pixel oberhalb und unterhalb des Cliprechtecks vollständig verworfen werden. Dies sind allgemeine Bereiche für die Benutzeroberflächenelemente eines Spiels.

</dd> </dl>

Ein besserer Ansatz besteht darin, Ihrem Spiel Unterstützung für die Breitbildanzeige hinzuzufügen. Die wichtigste Änderung besteht darin, die Projektionstransformation der Spielkamera so festzulegen, dass ein Seitenverhältnis von 16:9 verwendet wird, wodurch die Stretchingverzerrung vermieden wird. Selbst wenn Sie den Hintergrundpuffer bei einer Auflösung von 4:3 belassen, verbessert das Umschalten der Projektionstransformation zur Verwendung von 16:9 die wahrgenommene Genauigkeit des gerenderten Bilds erheblich. natürlich wird das endgültige Bild gefiltert, um die Auflösung des 4:3-Hintergrundpuffers so hochzuskalieren, dass sie der nativen Anzeigeauflösung von 16:9 entspricht. Dies ist jedoch ein weniger wahrnehmbares Artefakt als die stretch-Verzerrung, die durch einen Konflikt der Seitenverhältnisse verursacht wird.

Die Kosten für das Rendern der Szene über eine 16:9-Kamera können höher sein als eine 4:3-Kamera (auch bei identischen Auflösungen), da mehr Szenenobjekte im Frustum der breiteren Ansicht sichtbar sind. Sie sollten auch wissen, wie sich der vergrößerte sichtbare Bereich auf das Spiel auswirken kann. Beispielsweise würde eine Spielkamera mit einem Verhältnis von 16:9 mehr ihrer Spielwelt als eine 4:3-Kamera anzeigen.

Um die besten Ergebnisse bei einer 16:9-Anzeige zu erzielen, sollten Sie in einen 16:9-Hintergrundpuffer rendern, aber dies erfordert natürlich das Auffüllen weiterer Pixel. Der Unterschied zwischen 640×480 und 720×480 beträgt fast 38.400 Pixel, was einem Gewinn von 12,5 % entspricht. Wenn Sie sich die Kosten für das Auffüllen dieses größeren Bereichs leisten können, wird dringend empfohlen, dies zu tun.

## <a name="title-safe-region"></a>Title-Safe Region

Der Bildrahmenpuffer wird vom Benutzer möglicherweise teilweise verdeckt, da einige Pixel um den Rahmen häufig durch die Vorderblende der Anzeige abgedeckt werden. Um sicherzustellen, dass wichtige Benutzeroberflächenelemente auf einer Vielzahl von Anzeigehardware sichtbar sind, sollten Sie die Anforderungen an die titelsichere Region für Ihren Zielanzeigemodus beachten. Bei Nicht-MODI entspricht der titelsichere Bereich dem inneren 85 Prozent des Framepuffers, und bei DEN MODI IST der titelsichere Bereich der innere Bereich von 90 Prozent. Aus Gründen der größtmöglichen Kompatibilität mit der aktuellen und zukünftigen Anzeigehardware sollten Sie daher alle wichtigen Benutzeroberflächenelemente und Anzeigeindikatoren für die Kopf-auf-Kopf-Benutzeroberfläche innerhalb der inneren 85 Prozent des Framepuffers beibehalten.

## <a name="ntsc-suggestions"></a>NTSC-Vorschläge

Da NTSC der gängigste Videostandard im USA für Consumeranzeigehardware ist, ist es wichtig, einige der Richtlinien zu kennen, die Sie für Ihr Ausgabebild befolgen sollten.

### <a name="clamp-the-rgb-color-component-values-between-16-and-235"></a>Zusammenfügen der RGB-Farbkomponentenwerte zwischen 16 und 235

Farben außerhalb des Bereichs von 16 bis 235 können sicherlich an ntsc tv gesendet werden, aber es ist wahrscheinlich, dass diese Werte außerhalb des Bereichs als Audiodaten interpretiert werden. Dies wird häufig als *Audioton* bezeichnet und ist am offensichtlichsten, wenn Ihre Inhalte auf einem soliden weißen Hintergrund dargestellt werden. Sie können das Anbinden von Ausgabefarben innerhalb eines Pixel-Shaders problemlos implementieren.

### <a name="avoid-similar-colors-that-might-appear-identical"></a>Vermeiden sie ähnliche Farben, die möglicherweise identisch erscheinen.

Die NTSC-Farbpalette bietet nicht die gleiche Palette wie ein typischer Computermonitor. Vermeiden Sie daher die Verwendung ähnlicher Farben überall dort, wo das Spiel erfordert, dass der Spieler den Unterschied erkennen muss.

### <a name="avoid-sharp-differences-in-contrast"></a>Vermeiden von starken Unterschieden im Kontrast

Obwohl diese Richtlinie nicht immer praktisch zu befolgen ist, können Sie einige der Farbunterstärkungen auf NTSC-Displays (auch bekannt als *Durchforstung von Durchforstungselementen* der Benutzeroberfläche) verringern, indem Sie die richtigen Farben für Ihre Vordergrund- und Hintergrundelemente der Benutzeroberfläche auswählen. Weißer Text auf einem farbigen Hintergrund liefert wahrscheinlich bessere Ergebnisse als kontrastreiche Farben.

## <a name="conclusion"></a>Zusammenfassung

Dieser Artikel bot einen Blick auf die 10-Fuß-Erfahrung aus der Perspektive eines Windows Spieleentwicklers, ist aber keinesfalls eine umfassende Umfrage. Sie sollten diese Themen weiter untersuchen, wenn Sie einen Windows Spieltitel entwickeln (auch wenn er nicht für die Verwendung mit Windows Media Center vorgesehen ist). Der echte Test besteht darin, Ihr Spiel auf einer Vielzahl von Videoanzeigen zu testen, um sicherzustellen, dass Ihr Spiel ein ansprechendes Erlebnis für jedes bietet. Basierend auf der typischen Lebensdauer eines Windows-basierten Spiels und dem vorhergesagten Wachstum bei der Nutzung von Windows Media Center ist es fast garantiert, dass ein Spiel, das Sie heute veröffentlichen, Teil der 10-Fuß-Erfahrung eines Benutzers ist – ob Kunden Ihr Spiel von der Benutzeroberfläche der Couch aus spielen können oder sie gezwungen sind, sich an Den Schaltern zu befinden, liegt größtenteils bei Ihnen.

 

 