---
title: Color
description: Farbe ist ein wichtiges visuelles Element der meisten Benutzeroberflächen.
ms.assetid: 30a60e9e-ebb4-40f2-8535-a9b58dc668a8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 9ade1c87606aa14831220e501a5f39f5d2ce2d1ebb4016ad04822634b7735c10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936754"
---
# <a name="color"></a>Color

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Farbe ist ein wichtiges visuelles Element der meisten Benutzeroberflächen. Neben reinen Ethiken hat Farbe auch bedeutungsbedingte Bedeutungen und löst emotionale Reaktionen aus. Um Verwechslungen in der Bedeutung zu vermeiden, muss Farbe konsistent verwendet werden. Um die gewünschten emotionalen Antworten zu erhalten, muss die Farbe entsprechend verwendet werden.

Farbe wird häufig als Farbraum betrachtet, wobei RGB (Rot, Grün, Blau), HSL (Farbton, Sättigung, Helligkeit) und HSV (Farbton, Sättigung, Wert) die am häufigsten verwendeten Farbräume sind.

![Abbildung eines Cubes mit Farbbeziehungen ](images/vis-color-image1.png)

Der RGB-Farbraum kann als Cube visualisiert werden.

Während die Anzeigetechnologie RGB-Werte verwendet und Entwickler daher häufig Farben in Bezug auf RGB betrachten, entspricht der RGB-Farbraum nicht der Art und Weise, wie Benutzer Farben erkennen. Wenn Sie z. B. "red" zu "dark cyan" hinzufügen, wird das Ergebnis nicht als roter, sondern als leichterer Cyan wahrgenommen.

![Abbildung von dunklen und hellen Cyanquadrat ](images/vis-color-image2.png)

In diesem Beispiel wird es durch hinzufügen von Rot zu dunklem Cyan leichter, nicht rot. Der RGB-Farbraum entspricht nicht der Wahrnehmung von Farben durch Personen.

Die HSL-/HSV-Farbräume bestehen aus drei Komponenten: Farbton, Sättigung und Helligkeit oder Wert. Diese Farbräume werden häufig anstelle von RGB verwendet, da sie besser mit der Wahrnehmung von Farben übereinstimmen.

Der HSL-Farbraum bildet einen doppelten Kegel, der oben weiß, unten schwarz und in der Mitte neutral ist:

-   **Hue:** Die Grundfarbe im Farbrad im Bereich von 0 bis 360 Grad, wobei sowohl 0 als auch 360 Grad rot sind.

    ![Abbildung eines Kreises mit Farbbeziehungen ](images/vis-color-image3.png)

    Das Farbrad, bei dem Rot 0 Grad, Gelb 60 Grad, Grün 120 Grad, Cyan 180 Grad, Blau 240 Grad und Magenta 300 Grad ist.

-   **Sättigung:** Wie rein (im Vergleich zu dull) die Farbe ist, die zwischen 0 und 100 liegt, wobei 100 vollständig und 0 grau ist.
-   **Helligkeit:** Wie hell die Farbe im Bereich von 0 bis 100 ist, wobei 100 so hell wie möglich ist (Weiß, unabhängig von Farbton und Sättigung) und 0 so dunkel wie möglich (Schwarz).

    ![Abbildung zur Veranschaulichung des hsl-Farbraums ](images/vis-color-image4.png)

    Der HSL-Farbraum kann als doppelter Kegel visualisiert werden.

Der HSV-Farbraum ist ähnlich, mit der Ausnahme, dass sein Raum einen einzelnen Kegel bildet:

-   **Hue:** Die Grundfarbe im Farbrad im Bereich von 0 bis 360 Grad, wobei sowohl 0 als auch 360 Grad rot sind.
-   **Sättigung:** Wie rein (im Vergleich zu dull) die Farbe ist, die zwischen 0 und 100 liegt, wobei 100 vollständig und 0 grau ist.
-   **Wert:** Wie hell die Farbe im Bereich von 0 bis 100 ist, wobei 100 so hell wie möglich ist (also halber Helligkeit im HSL-Raum) und 0 so dunkel wie möglich (schwarz).

    ![Abbildung zur Veranschaulichung des hsv-Farbraums ](images/vis-color-image5.png)

    Der HSV-Farbraum kann als einzelner Kegel visualisiert werden.

Wenn die Sättigung sowohl in HSL- als auch in HSV-Bereichen 0 ist, gibt die Helligkeit einen Grauton an. In Windows werden die HSL- und HSV-Leerzeichen in der Regel einer Skala zwischen 0 und 240 neu zugeordnet, sodass Farben mit einem 32-Bit-Wert dargestellt werden können.

**Hinweis:** Richtlinien für [Schriftarten](vis-fonts.md) und [Barrierefreiheit](inter-accessibility.md) werden in separaten Artikeln vorgestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

Die effektive Verwendung von Farben kann die Benutzeroberfläche Ihres Programms effektiver gestalten. Farbe kann Benutzern helfen, bestimmte Bedeutungen auf einen Blick zu verstehen. Farbe kann auch dazu bringen, dass Ihr Produkt ansprechender und feiner dargestellt wird.

Leider ist es zu einfach, Farben ineffektiv zu verwenden, insbesondere wenn Sie nicht im visuellen Design trainiert sind. Eine schlechte Verwendung von Farben führt zu Entwürfen, die unprofessionell, veraltet, verwirrend oder einfach hässlich aussehen. Eine schlechte Verwendung von Farben kann schlechter sein, als überhaupt keine Farbe zu verwenden.

In diesem Abschnitt wird erläutert, was Sie wissen müssen, um Farbe effektiv zu verwenden.

### <a name="how-color-is-used"></a>Verwendung der Farbe

Farbe wird in der Regel in der Benutzeroberfläche für die Kommunikation verwendet:

-   **Bedeutung.** Die Bedeutung einer Nachricht kann durch Farbe zusammengefasst werden. Beispielsweise wird Farbe häufig verwendet, um den Status zu kommunizieren, bei dem Rot ein Problem oder Fehler ist, Gelb ist Vorsicht oder Warnung, und Grün ist gut.
-   **Staat.** Der Zustand eines Objekts kann durch Farbe angegeben werden. Beispielsweise verwendet Windows Farbe, um Auswahl- und Mauszeigerzustände anzugeben. Links innerhalb von Webseiten verwenden blau für nicht aufgerufene und violette Für besucht.
-   **Differenzierung.** Es wird davon ausgegangen, dass es eine Beziehung zwischen Elementen der gleichen Farbe gibt, sodass die Farbcodierung eine effektive Möglichkeit ist, zwischen Objekten zu unterscheiden. Beispielsweise verwenden Aufgabenbereiche in einem Systemsteuerungselement einen grünen Hintergrund, um sie visuell vom Hauptinhalt zu trennen. Darüber hinaus ermöglicht Microsoft Outlook Benutzern, Nachrichten unterschiedliche farbige Flags zuzuweisen.
-   **Schwerpunkt.** Farbe kann verwendet werden, um die Aufmerksamkeit der Benutzer zu lenken. Beispielsweise verwendet Windows blaue [Hauptanweisungen,](text-ui.md) um sie vom anderen Text abzuheben.

Natürlich wird Farbe aus reinen optischen Gründen häufig in Grafiken verwendet. Obwohl Dies ist wichtig, sollten Sie die Farben von Benutzeroberflächenelementen in erster Linie basierend darauf auswählen, was sie bedeuten, nicht wie sie aussehen.

### <a name="color-interpretation"></a>Farbinterpretation

**Die Interpretation der Farbe durch benutzer ist häufig kulturabhängig.** In der USA ist beispielsweise die Färbung für die Färbung größtenteils mit der Farbe Weiß verknüpft, während Schwarz mit Färbungen verknüpft ist. In Japan war die Farbsymbolik jedoch vor langer Zeit genau das Gegenteil: Weiß war die vorherrschende Farbe bei Färbungen, und Schwarz wurde als Farbe angesehen, die guten Erfolg für Diebe bringt.

Allerdings **ist die Interpretation von Rot, Gelb und Grün für den Status global konsistent.** Dies ist auf die [CONVENTION on Road Signs and Signals](https://www.unece.org/trans/conventn/signalse.pdf)zurückzuführen, die die weltweite Konvention für Ampeln definiert (wobei Rot stopp, grün bedeutet fortfahren und gelb mit Vorsicht vorgeht). Sie können diese Statusfarben ohne Bedenken für kulturabhängige Interpretationen verwenden.

Über die Statusfarben hinaus weist Windows farbenbasierten Bedeutungen zu, wie im Abschnitt Richtlinien dieses Artikels beschrieben. Stellen Sie sicher, dass die Farbverwendung Ihres Programms mit diesen Farbkonventionen kompatibel ist.

### <a name="color-accessibility"></a>Farbbarrierefreiheit

Die Verwendung von Farben wirkt sich auf die Barrierefreiheit Ihrer Software für eine möglichst breite Zielgruppe aus. Benutzer mit Blindheit oder sehschwachen Personen können die Farben möglicherweise überhaupt nicht gut sehen. Ungefähr 8 Prozent der erwachsenen Märchen weisen eine Form von Farbverwechslungen auf (häufig fälschlicherweise als "Farbblindheit" bezeichnet), von denen Rot-Grün-Farbverwechslungen am häufigsten vorkommen.

![Abbildung mit primärer Farbe wie gewohnt ](images/vis-color-image6.png)

Die Primärfarben, die beim normalen Farbbild zu sehen sind.

![Abbildung, die die gleichen Farben wie bei Protantropie zeigt ](images/vis-color-image7.png)

Die Primärfarben wie bei Protantropie (1 % der legenen Bevölkerung).

![Abbildung, die die gleichen Farben zeigt, die mit deuteran colors zu sehen sind ](images/vis-color-image8.png)

Die Primärfarben, wie sie bei Deuterandominieren (6 % der legenen Bevölkerung) zu sehen sind.

![Abbildung, die die gleichen Farben wie bei Tritantropie zeigt ](images/vis-color-image9.png)

Die Primärfarben, die mit Tritantropie (1 % der legenen Bevölkerung) zu sehen sind.

Weitere Informationen finden Sie unter [Können Color-Blind Benutzer Ihre Website anzeigen?](/previous-versions/windows/internet-explorer/ie-developer/)

### <a name="use-color-to-reinforce-visually"></a>Verwenden von Farben zur visuellen Verstärkung

Die beste Lösung für farbliche Interpretations- und Barrierefreiheitsprobleme ist die Verwendung von Farbe, um die Bedeutung einer dieser primären Kommunikationsmethoden visuell zu verstärken:

-   **Text.** Präziser Text ist in der Regel die effektivste primäre Kommunikation, entweder direkt auf der Benutzeroberfläche oder über eine QuickInfo.

![Screenshot eines kleinen roten Symbols mit QuickInfo ](images/vis-color-image10.png)

In diesem Beispiel wird QuickInfo-Text verwendet, um die Bedeutung eines Symbols zu kommunizieren.

-   **Design.** Symbole lassen sich leicht durch die Entwürfe unterscheiden, insbesondere durch ihre Konturform.

![Screenshot von Symbolen in Graustufen (Graustufen) ](images/vis-color-image11.png)

In diesem Beispiel sind die Standardsymbole anhand ihrer Entwürfe leicht zu unterscheiden.

-   **Lage.** Es kann auch ein relativer Standort verwendet werden, aber dieser Ansatz ist schwächer als die Alternativen. Um effektiv zu sein, sollte der Standort standard und bekannt sein, wie bei Ampeln.

Obwohl Farbe das offensichtlichste Attribut vieler Entwürfe ist, muss sie immer redundant sein.

### <a name="designing-with-color"></a>Entwerfen mit Farbe

Ironischerweise besteht die beste Möglichkeit zum Entwerfen von Farben darin, mit dem Entwerfen ohne Farbe zu beginnen, entweder [wireframes](glossary.md) oder monocolore zu verwenden und später Farbe hinzuzufügen. Dadurch wird sichergestellt, dass Informationen nicht allein mithilfe von Farben kommuniziert werden. Außerdem wird sichergestellt, dass Ihre Drucke auf Monocolore-Druckern hervorragend aussehen.

### <a name="use-theme-or-system-colors"></a>Verwenden von Design- oder Systemfarben

Bei der effektiven Verwendung von Farben gibt es viele komplexe Faktoren, aber in Windows Benutzeroberfläche ist die Farbauswahl häufig darauf zurückzuführen, einfach die passende [Designfarbe](glossary.md) oder [Systemfarbe](glossary.md) gemäß einigen einfachen Regeln auszuwählen. Benutzer können diese Farbschemas anschließend auswählen und anpassen.

Dadurch können Sie nicht nur die Farbeinstellungen aller Benutzer berücksichtigen, sondern auch das perfekte Farbschema auswählen, das für alle Vorlieben, Stile und Kulturen geeignet ist (was natürlich andernfalls unmöglich ist).

**Wenn Sie nur eine Sache durchführen...**

Wählen Sie Farben aus, indem Sie die entsprechende Designfarbe oder Systemfarbe auswählen. Verwenden Sie Farbe nie als primäre Kommunikationsmethode, sondern als sekundäre Methode, um die Bedeutung visuell zu verstärken. Entwurf mit wireframes oder monocolore, um sicherzustellen, dass die Farbe sekundär ist.

### <a name="use-theme-or-system-colors-correctly"></a>Richtiges Verwenden von Design- oder Systemfarben

Angenommen, Benutzer wählen Design- oder Systemfarben basierend auf ihren persönlichen Anforderungen aus, und dass das Design oder die Systemfarben entsprechend erstellt werden. Wenn Sie basierend auf dieser Annahme immer Design- oder Systemfarben basierend auf ihrem beabsichtigten Zweck auswählen und Vordergrunde mit den zugehörigen Hintergründen koppeln, sind die Farben garantiert lesbar und berücksichtigen die Bedürfnisse der Benutzer in allen Videomodi, einschließlich des Modus mit [hohem Kontrast.](glossary.md) Beispielsweise ist die Systemfarbe des Fenstertexts für die Hintergrundsystemfarbe des Fensters garantiert lesbar.

Insbesondere immer:

-   **Wählen Sie Farben basierend auf ihrem Zweck aus.** Wählen Sie farben nicht basierend auf ihrer aktuellen Darstellung aus, da diese Darstellung vom Benutzer oder zukünftigen Versionen von Windows geändert werden kann.
-   **Übereinstimmung von Vordergrundfarben mit den zugehörigen Hintergrundfarben.** Vordergrundfarben sind garantiert nur für die zugehörigen Hintergrundfarben lesbar. Mischen Sie vordergrundfarbene Farben nicht mit anderen Hintergrundfarben oder noch schlechter mit anderen Vordergrundfarben, und passen Sie sie nicht an.
-   **Mischen Sie keine Farbtypen.** Das heißt, dass Designfarben immer mit den zugehörigen Designfarben, Systemfarben mit den zugehörigen Systemfarben und hartverkabelten Farben mit anderen hartverkabelten Farben übereinstimmen. Beispielsweise ist nicht garantiert, dass eine Designtextfarbe vor einem hartverkabelten Hintergrund lesbar ist.
-   **Wenn Sie farbenfest verkabeln müssen, behandeln Sie den Modus mit hohem Kontrast als Sonderfall.**

**Wenn Sie nur eine Sache durchführen...**

Wählen Sie immer Design- oder Systemfarben basierend auf ihrem beabsichtigten Zweck aus, und koppeln Sie Vordergrund mit den zugehörigen Hintergründen.

### <a name="using-other-colors"></a>Verwenden anderer Farben

Während das Windows Design einen umfassenden Satz von Designteilen definiert, stellen Sie möglicherweise fest, dass Ihr Programm Farben benötigt, die nicht in der Designdatei definiert sind. Sie können solche Farben zwar hart verkabeln, aber ein besserer Ansatz besteht darin, Farben aus dem Design oder den Systemfarben abzuleiten. Die strategische Verwendung dieses Ansatzes bietet Ihnen alle Vorteile der Verwendung von Design- und Systemfarben, aber mit viel mehr Flexibilität.

Angenommen, Sie benötigen einen Fensterhintergrund, der dunkler als die Hintergrundfarbe des Designfensters ist. Im HSL-Farbraum bedeutet eine dunkleere Farbe eine Farbe mit geringerer Helligkeit. Daher können Sie mithilfe der folgenden Schritte eine dunklere Hintergrundfarbe für das Fenster ableiten:

-   Rufen Sie die Rgb-Farbe für das Hintergrunddesign des Fensters ab.
-   Konvertieren Sie rgb in den HSL-Wert.
-   Reduzieren Sie den Helligkeitswert (z. B. um 20 Prozent).
-   Konvertieren Sie zurück in RGB-Werte.

Bei diesem Ansatz wird die abgeleitete Farbe garantiert als dunklerer Farbton der ursprünglichen Farbe wahrgenommen (es sei denn, die ursprüngliche Farbe war zu Beginn sehr dunkel.)

![Abbildung, die die Auswirkungen einer reduzierten Helligkeit zeigt ](images/vis-color-image12.png)

In diesem Beispiel wird eine dunklere Hintergrundfarbe des Fensters von der Designfarbe abgeleitet.

### <a name="testing-colors"></a>Testen von Farben

Um zu ermitteln, ob auf die Verwendung von Farbe durch Ihr Programm zugegriffen werden kann und nicht als primäre Kommunikationsmethode verwendet wird, empfehlen wir die Verwendung der [Dienstprogramme "ColorDoctor"](https://www.fujitsu.com/global/about/businesspolicy/tech/design/) oder ["Vischeck",](https://www.vischeck.com/) um Folgendes zu überprüfen:

-   Allgemeine Abhängigkeit von Farben mithilfe des Graustufenfilters.
-   Spezifische Farbkonfusionsprobleme bei Verwendung der Filter Protantropie, Deuterantropie und Tritantropie.

Um festzustellen, ob die Farbverwendung ihres Programms ordnungsgemäß programmiert ist, testen Sie das Programm in den folgenden Modi:

-   Theming enabled using the default Windows theme.net
-   Design aktiviert mit einem nicht standardmäßigen Design.
-   Design deaktiviert ("Windows klassischer Stil" im Design Einstellungen im Element Personalisierung Systemsteuerung).
-   hoher Kontrast Schwarz (weißer Text auf schwarzem Hintergrund).
-   hoher Kontrast Weiß (schwarzer Text auf weißem Hintergrund).

Alle Bildschirmelemente sollten lesbar sein und erwartungsgemäß angezeigt werden, auch unmittelbar nach der Änderung des Modus.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie Farbe nie als primäre Kommunikationsmethode,** sondern als sekundäre Methode, um die Bedeutung visuell zu verstärken.

### <a name="using-theme-and-system-colors"></a>Verwenden von Design- und Systemfarben

-   Wählen Sie nach Möglichkeit **Farben aus, indem Sie die entsprechende Designfarbe oder Systemfarbe auswählen.** Auf diese Weise können Sie immer die Farbpräferenz der Benutzer berücksichtigen.
-   **Wählen Sie Design- und Systemfarben basierend auf ihrem Zweck aus.** Wählen Sie farben nicht basierend auf ihrer aktuellen Darstellung aus, da diese Darstellung vom Benutzer oder zukünftigen Versionen von Windows geändert werden kann.
-   **Übereinstimmung von Vordergrundfarben mit den zugehörigen Hintergrundfarben.** Vordergrundfarben sind garantiert nur für die zugehörigen Hintergrundfarben lesbar. Mischen Sie vordergrundfarbene Farben nicht mit anderen Hintergrundfarben oder noch schlechter mit anderen Vordergrundfarben, und passen Sie sie nicht an.
-   **Mischen Sie keine Farbtypen.** Das heißt, dass Designfarben immer mit den zugehörigen Designfarben, Systemfarben mit den zugehörigen Systemfarben und hartverkabelten Farben mit anderen hartverkabelten Farben übereinstimmen. Beispielsweise ist nicht garantiert, dass eine Designtextfarbe vor einem hartverkabelten Hintergrund lesbar ist.
-   **Wenn Sie eine Farbe verwenden müssen, die kein Design oder keine Systemfarbe ist:**
    -   **Ziehen Sie es vor, die Farbe von einem Design oder einer Systemfarbe abzuleiten, als den Wert hartzu verkabeln.** Verwenden Sie den weiter oben in diesem Artikel beschriebenen Prozess unter Verwenden anderer Farben.
    -   **Behandeln Sie den Modus für hohen Kontrast als Sonderfall.**
-   **Behandeln von Designänderungen.** Designänderungen werden automatisch von Fenstern mit Standardfensterrahmen und allgemeinen Steuerelementen verarbeitet. Windows mit benutzerdefinierten Fensterrahmen, benutzerdefinierten Steuerelementen oder Steuerelementen zum Zeichnen mit Besitzer und anderer Verwendung von Farben müssen Designänderungen explizit behandeln.
    -   **Entwickler:** Sie können auf Designänderungsereignisse reagieren, indem Sie die WM \_ THEMECHANGED-Meldung behandeln.

### <a name="color-meaning"></a>Bedeutung der Farbe

-   Obwohl Sie nach Möglichkeit Design- und Systemfarben (oder abgeleitete Farben) verwenden sollten, stellen Sie sicher, dass jede andere Verwendung von Farben mit der folgenden Verwendung von Farben innerhalb Windows kompatibel ist.



| Farbton | Bedeutung | Verwenden in Windows  |
|--------------------------------------|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blau/grün<br/>                | Windows Marke<br/>                                                      | Hintergrund: Windows Branding.<br/>                                                                                                                        |
| glass, black, gray, white<br/> | Neutral<br/>                                                            | Hintergrund: Standardfensterrahmen, Startmenü, Taskleiste, Randleiste.<br/> Vordergrund: normaler Text.<br/>                                                |
| blue<br/>                      | Starten, Committen<br/>                                                      | Hintergrund: Standardbefehlsschaltflächen, Suchen, Anmelden.<br/> Symbole: Informationen, Hilfe.<br/> Vordergrund: Hauptanweisungen, Links.<br/>           |
| Rot<br/>                       | Error, Stop, vulnerable, critical, immediate attention, restricted<br/> | Hintergrund: Status, Status beendet (Statusanzeigen).<br/> Symbole: Fehler, Beenden, Fenster schließen, Löschen, erforderliche Eingabe, fehlend, nicht verfügbar.<br/>     |
| yellow<br/>                    | Warnung, Vorsicht, fragebar<br/>                                     | Hintergrund: Status, angehaltener Status (Statusanzeigen).<br/> Symbole: Warnung<br/>                                                                       |
| green<br/>                     | go, proceed, progress, safe<br/>                                        | Hintergrund: Status, normaler Status (Statusleisten).<br/> Symbole: go, done, refresh.<br/> Vordergrund: Pfade und URLs (in Suchergebnissen).<br/> |
| purple<br/>                    | Besucht<br/>                                                            | Vordergrund: Besuchte Links (für Links in Windows Internet Explorer und Dokumenten).<br/>                                                                |



 

-   **Um die Kommunikation mit den vorherigen Bedeutungen zu vermeiden, wählen Sie Farben mit hoher mittlerer bis niedriger Sättigung und hoher oder niedriger Helligkeit aus.** Benutzer ordnen die vorherigen Bedeutungen Farben mit voller oder hoher Sättigung und Helligkeit auf mittlerem Niveau zu, sodass Sie diese Zuordnungen vermeiden können, indem Sie unterschiedliche Schattierungen auswählen.

![Abbildung, die zeigt, wie die Helligkeit die Farbe beeinflusst ](images/vis-color-image13.png)

In diesem Beispiel gibt es drei verschiedene Gelbschattierungen, aber nur der stark überleerte Helligkeitston der mittleren Ebene gibt eine Warnung aus. Das gelbe Ordnersymbol sieht nicht wie eine Warnung aus.

### <a name="using-color-with-data"></a>Verwenden von Farbe mit Daten

-   Wenn dies hilfreich **ist, weisen Sie Daten Farbe zu, damit benutzer sie unterscheiden können.** Beachten Sie, dass Benutzer davon ausgehen, dass Daten mit ähnlichen Farben eine ähnliche Bedeutung haben.
-   **Weisen Sie standardmäßig Farben zu, die leicht zu unterscheiden sind.** Im Allgemeinen lassen sich Farben leicht unterscheiden, wenn sie in den HSL/HSV-Farbräumen weit voneinander entfernt sind, während gleichzeitig ein hoher Kontrast mit dem Hintergrund beibehalten wird:
    -   Wenn Sie Farben auswählen, bevorzugen Sie Triad-Färbungen oder ergänzende Farbtons, aber keine angrenzenden Farbtons.

        ![Abbildung, die zeigt, wie kontrastreiche Farben verwendet werden ](images/vis-color-image14.png)

        Wenn in diesem Beispiel die erste Farbzuweisung Rot ist, sollte die nächste Farbe blau, grün oder zyan, aber nicht Magenta, Violett, Orange oder Gelb sein.

    -   Farben haben einen hohen Kontrast, wenn der Farbton, die Sättigung oder die Helligkeit einen großen Unterschied haben.

        ![Abbildung, die eine Farbe auf unterschiedlichen Hintergründen zeigt ](images/vis-color-image15.png)

        In diesem Beispiel steht die hellblaue Basisfarbe im Gegensatz zu Hintergründen mit großen Unterschieden in Farbton, Sättigung oder Helligkeit.

    -   Die Verwendung eines weißen oder sehr hellen Hintergrunds erleichtert die Unterscheidung von Kontrastfarben im Vordergrund.

        ![Abbildung zur Veranschaulichung eines guten und schlechten Kontrasts ](images/vis-color-image16.png)

        In diesem Beispiel erleichtern weiße und helle Hintergrundfarben die Unterscheidung der Vordergrundfarbe.

-   **Ermöglichen Sie Es Benutzern, diese Farbzuweisungen anzupassen,** da die Farbauswahl privat und eine persönliche Vorliebe ist. Wenn viele koordinierte Farben verfügbar sind, können Benutzer sie mithilfe von Farbschemas als Gruppe ändern.
-   **Benutzern erlauben, diese Farbzuweisungen zu beschriften.** Auf diese Weise können sie leichter identifiziert und leichter zu finden sein.
-   **Im Gegensatz zu Benutzeroberflächenfarben sollten sich Daten nicht ändern, wenn sich die Systemfarben ändern.**

## <a name="documentation"></a>Dokumentation

-   **Verweisen Sie auf Benutzeroberflächenelemente nach ihren Namen, nicht nach ihren Farben.** Auf solche Verweise kann nicht zugegriffen werden, und die Systemfarben können sich ändern. Wenn der Name eines Benutzeroberflächenelements nicht bekannt oder nicht beschreibend genug ist, zeigen Sie zur Verdeutlichung einen Screenshot an.

**Richtig:**

![Screenshot der Nachricht mit der Informationsleiste ](images/vis-color-image17.png)

**Falsch:**

![Screenshot der Nachricht, die "gold bar" enthält ](images/vis-color-image18.png)

Im falschen Beispiel bezieht sich die Meldung auf die Windows Internet Explorer informationsleiste durch ihre Farbe anstelle ihres Namens.

