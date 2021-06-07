---
title: Color
description: Farbe ist ein wichtiges visuelles Element der meisten Benutzeroberflächen.
ms.assetid: 30a60e9e-ebb4-40f2-8535-a9b58dc668a8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 598654c7e96f025bbcc1ff2a97c96df1a328c046
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444641"
---
# <a name="color"></a>Color

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Farbe ist ein wichtiges visuelles Element der meisten Benutzeroberflächen. Neben reinen Ethiken hat Farbe auch bedeutungsbedingte Bedeutungen und löst emotionale Reaktionen aus. Um Verwechslungen in der Bedeutung zu vermeiden, muss Farbe konsistent verwendet werden. Um die gewünschten emotionalen Antworten zu erhalten, muss die Farbe entsprechend verwendet werden.

Farbe wird häufig als Farbraum betrachtet, wobei RGB (Rot, Grün, Blau), HSL (Farbton, Sättigung, Helligkeit) und HSV (Farbton, Sättigung, Wert) die am häufigsten verwendeten Farbräume sind.

![Abbildung eines Cubes mit Farbbeziehungen ](images/vis-color-image1.png)

Der RGB-Farbraum kann als Cube visualisiert werden.

Während die Anzeigetechnologie RGB-Werte verwendet und Entwickler daher häufig Farben in Bezug auf RGB betrachten, entspricht der RGB-Farbraum nicht der Art und Weise, wie Menschen Farben erkennen. Wenn Sie z. B. "red" zu "dark cyan" hinzufügen, wird das Ergebnis nicht als roter, sondern als leichterer Cyan wahrgenommen.

![Abbildung von dunklen und hellen Cyan-Quadraten ](images/vis-color-image2.png)

In diesem Beispiel wird es durch hinzufügen von Rot zu dunklem Cyan leichter, nicht rot. Der RGB-Farbraum entspricht nicht der Wahrnehmung von Farben durch Personen.

Die HSL-/HSV-Farbräume bestehen aus drei Komponenten: Farbton, Sättigung und Helligkeit oder Wert. Diese Farbräume werden häufig anstelle von RGB verwendet, da sie besser mit der Wahrnehmung von Farben übereinstimmen.

Der HSL-Farbraum bildet einen doppelten Kegel, der oben weiß, unten schwarz und in der Mitte neutral ist:

-   **Hue:** Die Grundfarbe im Farbrad im Bereich von 0 bis 360 Grad, wobei sowohl 0 als auch 360 Grad rot sind.

    ![Abbildung eines Kreises mit Farbbeziehungen ](images/vis-color-image3.png)

    Das Farbrad, bei dem Rot 0 Grad, Gelb 60 Grad, Grün 120 Grad, Cyan 180 Grad, Blau 240 Grad und Magenta 300 Grad ist.

-   **Sättigung:** Wie rein (im Vergleich zu dull) die Farbe ist, die zwischen 0 und 100 liegt, wobei 100 vollständig ausgelastet und 0 grau ist.
-   **Helligkeit:** Wie hell die Farbe im Bereich von 0 bis 100 ist, wobei 100 so hell wie möglich ist (Weiß, unabhängig von Farbton und Sättigung) und 0 so dunkel wie möglich (Schwarz).

    ![Abbildung zur Veranschaulichung des hsl-Farbraums ](images/vis-color-image4.png)

    Der HSL-Farbraum kann als doppelter Kegel visualisiert werden.

Der HSV-Farbraum ist ähnlich, mit der Ausnahme, dass sein Raum einen einzelnen Kegel bildet:

-   **Hue:** Die Grundfarbe im Farbrad im Bereich von 0 bis 360 Grad, wobei sowohl 0 als auch 360 Grad rot sind.
-   **Sättigung:** Wie rein (im Vergleich zu dull) die Farbe ist, die zwischen 0 und 100 liegt, wobei 100 vollständig ausgelastet und 0 grau ist.
-   **Wert:** Wie hell die Farbe im Bereich von 0 bis 100 ist, wobei 100 so hell wie möglich ist (also halber Helligkeit im HSL-Raum) und 0 so dunkel wie möglich (Schwarz).

    ![Abbildung zur Veranschaulichung des hsv-Farbraums ](images/vis-color-image5.png)

    Der HSV-Farbraum kann als einzelner Kegel visualisiert werden.

Wenn die Sättigung sowohl in HSL- als auch in HSV-Bereichen 0 ist, gibt die Helligkeit einen Grauton an. In Windows werden die HSL- und HSV-Leerzeichen in der Regel einer Skala zwischen 0 und 240 neu zugeordnet, sodass Farben mit einem 32-Bit-Wert dargestellt werden können.

**Hinweis:** Richtlinien für [Schriftarten](vis-fonts.md) und [Barrierefreiheit](inter-accessibility.md) werden in separaten Artikeln vorgestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

Die effektive Verwendung von Farben kann die Benutzeroberfläche Ihres Programms effektiver gestalten. Farbe kann Benutzern helfen, bestimmte Bedeutungen auf einen Blick zu verstehen. Farbe kann auch dazu sorgen, dass Ihr Produkt ansprechender und feiner dargestellt wird.

Leider ist es zu einfach, Farben ineffektiv zu verwenden, insbesondere wenn Sie nicht im visuellen Design trainiert sind. Eine schlechte Verwendung von Farben führt zu Entwürfen, die unprofessionell, veraltet, verwirrend oder einfach hässlich aussehen. Eine schlechte Verwendung der Farbe kann schlechter sein, als überhaupt keine Farbe zu verwenden.

In diesem Abschnitt wird erläutert, was Sie wissen müssen, um Farbe effektiv zu verwenden.

### <a name="how-color-is-used"></a>Verwendung der Farbe

Farbe wird in der Regel in der Benutzeroberfläche für die Kommunikation verwendet:

-   **Bedeutung.** Die Bedeutung einer Nachricht kann anhand der Farbe zusammengefasst werden. Beispielsweise wird Farbe häufig verwendet, um den Status zu kommunizieren, bei dem Rot ein Problem oder Fehler ist, Gelb vorsichtshalber oder Warnung ist und Grün gut ist.
-   **Staat.** Der Zustand eines Objekts kann durch Farbe angegeben werden. Windows verwendet z. B. Farbe, um Auswahl- und Mauszeigerzustände anzugeben. Links innerhalb von Webseiten verwenden blau für nicht aufgerufene und violette Für besucht.
-   **Differenzierung.** Personen gehen davon aus, dass es eine Beziehung zwischen Elementen der gleichen Farbe gibt, sodass die Farbcodierung eine effektive Möglichkeit ist, zwischen Objekten zu unterscheiden. Beispielsweise verwenden Aufgabenbereiche in einem Systemsteuerungselement einen grünen Hintergrund, um sie visuell vom Hauptinhalt zu trennen. Darüber hinaus ermöglicht Microsoft Outlook Benutzern, Nachrichten unterschiedliche farbige Flags zuzuweisen.
-   **Schwerpunkt.** Farbe kann verwendet werden, um die Aufmerksamkeit der Benutzer zu lenken. Windows verwendet beispielsweise blaue [Hauptanweisungen,](text-ui.md) um sie vom anderen Text abzuheben.

Natürlich wird Farbe aus reinen optischen Gründen häufig in Grafiken verwendet. Obwohl Dies ist wichtig, sollten Sie die Farben von Benutzeroberflächenelementen in erster Linie basierend darauf auswählen, was sie bedeuten, nicht wie sie aussehen.

### <a name="color-interpretation"></a>Farbinterpretation

**Die Interpretation der Farbe durch benutzer ist häufig kulturabhängig.** In der USA ist beispielsweise die Färbung für die Färbung größtenteils mit der Farbe Weiß verknüpft, während Schwarz mit Färbungen verknüpft ist. In Japan war die Farbsymbolik jedoch vor langer Zeit genau das Gegenteil: Weiß war die vorherrschende Farbe bei Färbungen, und Schwarz wurde als Farbe angesehen, die guten Erfolg für Diebe bringt.

Allerdings **ist die Interpretation von Rot, Gelb und Grün für den Status global konsistent.** Dies ist auf die [CONVENTION on Road Signs and Signals](https://www.unece.org/trans/conventn/signalse.pdf)zurückzuführen, die die weltweite Konvention für Ampeln definiert (wobei Rot stopp, grün bedeutet fortfahren und gelb mit Vorsicht vorgeht). Sie können diese Statusfarben ohne Bedenken für kulturabhängige Interpretationen verwenden.

Über die Statusfarben hinaus weist Windows Farben gemäß der Konvention Bedeutungen zu, wie im Abschnitt Richtlinien dieses Artikels beschrieben. Stellen Sie sicher, dass die Farbverwendung Ihres Programms mit diesen Farbkonventionen kompatibel ist.

### <a name="color-accessibility"></a>Farbbarrierefreiheit

Die Verwendung von Farben wirkt sich auf die Barrierefreiheit Ihrer Software für eine möglichst breite Zielgruppe aus. Benutzer mit Blindheit oder sehschwachen Sehvermögen können die Farben möglicherweise nicht gut sehen, wenn überhaupt. Ungefähr 8 Prozent der erwachsenen Märchen weisen eine Form von Farbverwechslungen auf (häufig fälschlicherweise als "Farbblindheit" bezeichnet), von denen Rot-Grün-Farbverwechslungen am häufigsten vorkommen.

![Abbildung mit primärer Farbe wie gewohnt ](images/vis-color-image6.png)

Die Primärfarben, die bei normalem Farbbild zu sehen sind.

![Abbildung, die die gleichen Farben wie bei Protantropie zeigt ](images/vis-color-image7.png)

Die Primärfarben wie bei Protantropie (1 % der legenen Bevölkerung).

![Abbildung mit den gleichen Farben, die mit deuteran colors zu sehen sind ](images/vis-color-image8.png)

Die Primärfarben, wie sie bei Deuterantropie (6 % der legenen Bevölkerung) zu sehen sind.

![Abbildung, die die gleichen Farben wie bei Tritantropie zeigt ](images/vis-color-image9.png)

Die Primärfarben, die mit Tritantropie (1 % der legenen Bevölkerung) zu sehen sind.

Weitere Informationen finden Sie unter [Können Color-Blind Benutzer Ihre Website anzeigen?](/previous-versions/windows/internet-explorer/ie-developer/)

### <a name="use-color-to-reinforce-visually"></a>Verwenden von Farben zur visuellen Verstärkung

Die beste Lösung für farbliche Interpretations- und Barrierefreiheitsprobleme ist die Verwendung von Farbe, um die Bedeutung einer dieser primären Kommunikationsmethoden visuell zu verstärken:

-   **Text.** Präziser Text ist in der Regel die effektivste primäre Kommunikation entweder direkt auf der Benutzeroberfläche oder über eine QuickInfo.

![Screenshot eines kleinen roten Symbols mit QuickInfo ](images/vis-color-image10.png)

In diesem Beispiel wird QuickInfo-Text verwendet, um die Bedeutung eines Symbols zu kommunizieren.

-   **Design.** Symbole lassen sich leicht durch die Entwürfe unterscheiden, insbesondere durch ihre Konturform.

![Screenshot von Symbolen in Graustufen (Graustufen) ](images/vis-color-image11.png)

In diesem Beispiel sind die Standardsymbole anhand ihrer Entwürfe leicht zu unterscheiden.

-   **Lage.** Es kann auch ein relativer Standort verwendet werden, aber dieser Ansatz ist schwächer als die Alternativen. Um effektiv zu sein, sollte der Standort standard und bekannt sein, wie bei Ampeln.

Obwohl Farbe das offensichtlichste Attribut vieler Entwürfe ist, muss sie immer redundant sein.

### <a name="designing-with-color"></a>Entwerfen mit Farbe

Ironischerweise besteht die beste Möglichkeit zum Entwerfen von Farben darin, mit dem Entwerfen ohne Farbe zu beginnen, entweder [wireframes](glossary.md) oder monocolore zu verwenden und später Farbe hinzuzufügen. Dadurch wird sichergestellt, dass Informationen nicht nur mithilfe von Farben kommuniziert werden. Außerdem wird sichergestellt, dass Ihre Drucke auf monofarbigen Druckern gut aussehen.

### <a name="use-theme-or-system-colors"></a>Verwenden von Design- oder Systemfarben

Obwohl es viele komplexe Faktoren bei der effektiven Verwendung von Farben gibt, geht [](glossary.md) es [](glossary.md) bei der Auswahl der Farbe auf der Windows-Benutzeroberfläche häufig nur um die Auswahl der passenden Designfarbe oder Systemfarbe gemäß einigen einfachen Regeln. Benutzer können diese Farbschemas dann nach Bewählen auswählen und anpassen.

Auf diese Weise berücksichtigen Sie nicht nur die Farbeinstellungen aller Benutzer, sondern auch die Auswahl eines perfekten Farbschemas, das für alle Vorlieben, Stile und Kulturen geeignet ist (was natürlich andernfalls unmöglich ist).

**Wenn Sie nur eine Sache tun...**

Wählen Sie Farben aus, indem Sie die entsprechende Designfarbe oder Systemfarbe auswählen. Verwenden Sie niemals Farbe als primäre Kommunikationsmethode, sondern als sekundäre Methode, um die Bedeutung visuell zu verstärken. Entwerfen Sie mithilfe von Wireframes oder monofarbig, um sicherzustellen, dass farbe sekundär ist.

### <a name="use-theme-or-system-colors-correctly"></a>Design- oder Systemfarben richtig verwenden

Angenommen, Benutzer wählen Design- oder Systemfarben basierend auf ihren persönlichen Anforderungen aus und das Design oder die Systemfarben werden entsprechend erstellt. Wenn Sie basierend auf dieser Annahme immer Design- oder Systemfarben basierend auf ihrem beabsichtigten Zweck auswählen und Vordergrund mit den zugehörigen Hintergründen koppeln, sind die Farben garantiert lesbar und achten in allen Videomodi, einschließlich des Modus mit hohem Kontrast, auf die Bedürfnisse der [Benutzer.](glossary.md) Beispielsweise ist sichergestellt, dass die Systemfarbe des Fenstertexts für die Systemfarbe des Fensterhintergrunds lesbar ist.

Insbesondere immer:

-   **Wählen Sie Farben basierend auf ihrem Zweck aus.** Wählen Sie Farben nicht basierend auf ihrer aktuellen Darstellung aus, da diese Darstellung vom Benutzer oder zukünftigen Versionen von Windows geändert werden kann.
-   **Übereinstimmung von Vordergrundfarben mit den zugeordneten Hintergrundfarben.** Vordergrundfarben sind garantiert nur für ihre zugeordneten Hintergrundfarben lesbar. Kombinieren Sie keine Vordergrundfarben mit anderen Hintergrundfarben oder noch schlechter noch anderen Vordergrundfarben, und passen Sie sie nicht an.
-   **Mischen Sie keine Farbtypen.** Dies bedeutet, dass Designfarben immer mit ihren zugeordneten Designfarben, Systemfarben mit den zugehörigen Systemfarben und hartverkabelten Farben mit anderen hartverkabelten Farben übereinstimmen. Beispielsweise ist nicht garantiert, dass eine Designtextfarbe vor einem hartverkabelten Hintergrund lesbar ist.
-   **Wenn Sie Hardwirefarben verwenden müssen, behandeln Sie den Modus mit hohem Kontrast als Sonderfall.**

**Wenn Sie nur eine Sache tun...**

Wählen Sie immer Design- oder Systemfarben basierend auf ihrem beabsichtigten Zweck aus, und koppeln Sie Vordergrund mit ihren zugeordneten Hintergründen.

### <a name="using-other-colors"></a>Verwenden anderer Farben

Obwohl das Windows-Design einen umfassenden Satz von Designteilen definiert, stellen Sie möglicherweise fest, dass Ihr Programm Farben benötigt, die nicht in der Designdatei definiert sind. Sie können solche Farben zwar verkabeln, aber ein besserer Ansatz besteht in der Ableitung von Farben aus dem Design oder den Systemfarben. Die strategische Verwendung dieses Ansatzes bietet Ihnen alle Vorteile der Verwendung von Design- und Systemfarben, aber mit viel mehr Flexibilität.

Angenommen, Sie benötigen einen Fensterhintergrund, der dunkler als die Hintergrundfarbe des Designfensters ist. Im HSL-Farbraum bedeutet eine dunklere Farbe eine Farbe mit einer geringeren Helligkeit. Daher können Sie mithilfe der folgenden Schritte eine dunklere Hintergrundfarbe für das Fenster ableiten:

-   Abrufen der Hintergrunddesignfarbe des Fensters RGB.
-   Konvertieren Sie rgb in den HSL-Wert.
-   Reduzieren Sie den Helligkeitswert (z. B. um 20 Prozent).
-   Konvertieren Sie zurück in RGB-Werte.

Bei diesem Ansatz wird die abgeleitete Farbe garantiert als dunklerer Schattierung der ursprünglichen Farbe wahrgenommen (es sei denn, die ursprüngliche Farbe war zu Beginn sehr dunkel.)

![Abbildung der Auswirkungen einer reduzierten Helligkeit ](images/vis-color-image12.png)

In diesem Beispiel wird eine dunklere Hintergrundfarbe des Fensters von der Designfarbe abgeleitet.

### <a name="testing-colors"></a>Testen von Farben

Um zu ermitteln, ob auf die Verwendung von Farben ihres Programms zugegriffen werden kann und nicht als primäre Kommunikationsmethode verwendet wird, empfiehlt es sich, den [ColorDoctor von ColorDoctor](https://www.fujitsu.com/global/about/businesspolicy/tech/design/) oder [die Vischeck-Hilfsprogramme](https://www.vischeck.com/) zu verwenden, um nach Folgenden zu überprüfen:

-   Gesamtabhängigkeit von Farben mithilfe des Graustufenfilters.
-   Spezifische Farbverwechslungsprobleme mithilfe der Filter Protanppe, Deuteranphy und Tritan verwechslungen.

Um festzustellen, ob die Farbnutzung ihres Programms ordnungsgemäß programmiert ist, testen Sie das Programm in den folgenden Modi:

-   Das Design ist mithilfe des Windows-Standarddesigns aktiviert.
-   Das Design ist mit einem nicht standardmäßigen Design aktiviert.
-   Das Design ist deaktiviert ("Klassischer Windows-Stil" in den Designeinstellungen im Personalisierungselement Systemsteuerung).
-   hoher Kontrast Schwarz (weißer Text auf schwarzem Hintergrund).
-   hoher Kontrast Weiß (schwarzer Text auf weißem Hintergrund).

Alle Bildschirmelemente sollten lesbar sein und erwartungsgemäß angezeigt werden, auch unmittelbar nachdem sich der Modus geändert hat.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie niemals Farbe als primäre Kommunikationsmethode, sondern** als sekundäre Methode, um die Bedeutung visuell zu verstärken.

### <a name="using-theme-and-system-colors"></a>Verwenden von Design- und Systemfarben

-   Wählen Sie nach **Möglichkeit Farben aus, indem Sie die entsprechende Design- oder Systemfarbe auswählen.** Dadurch können Sie die Farbpräferenz der Benutzer immer achten.
-   **Wählen Sie Design- und Systemfarben basierend auf ihrem Zweck aus.** Wählen Sie Farben nicht basierend auf ihrer aktuellen Darstellung aus, da diese Darstellung vom Benutzer oder zukünftigen Versionen von Windows geändert werden kann.
-   **Übereinstimmung von Vordergrundfarben mit den zugeordneten Hintergrundfarben.** Vordergrundfarben sind garantiert nur für ihre zugeordneten Hintergrundfarben lesbar. Kombinieren Sie keine Vordergrundfarben mit anderen Hintergrundfarben oder noch schlechter noch anderen Vordergrundfarben, und passen Sie sie nicht an.
-   **Mischen Sie keine Farbtypen.** Dies bedeutet, dass Designfarben immer mit ihren zugeordneten Designfarben, Systemfarben mit den zugehörigen Systemfarben und hartverkabelten Farben mit anderen hartverkabelten Farben übereinstimmen. Beispielsweise ist nicht garantiert, dass eine Designtextfarbe vor einem hartverkabelten Hintergrund lesbar ist.
-   **Wenn Sie eine Farbe verwenden müssen, die kein Design oder keine Systemfarbe ist:**
    -   **Ziehen Sie es vor, die Farbe von einem Design oder einer Systemfarbe zu leiten, als den Wert fest zu verkabeln.** Verwenden Sie den weiter oben in diesem Artikel beschriebenen Prozess unter Verwenden anderer Farben.
    -   **Behandeln Sie den Modus mit hohem Kontrast als Sonderfall.**
-   **Behandeln sie Designänderungen.** Designänderungen werden automatisch von Fenstern mit Standardfensterrahmen und allgemeinen Steuerelementen verarbeitet. Fenster mit benutzerdefinierten Fensterrahmen, benutzerdefinierten Steuerelementen oder Steuerelementen zum Zeichnen von Besitzern und anderer Verwendung von Farben müssen Designänderungen explizit verarbeiten.
    -   **Entwickler:** Sie können auf Designänderungsereignisse reagieren, indem Sie die WM \_ THEMECHANGED-Nachricht behandeln.

### <a name="color-meaning"></a>Farbbeeindruckung

-   Sie sollten zwar nach Möglichkeit Design- und Systemfarben (oder abgeleitete Farben) verwenden, stellen Sie jedoch sicher, dass jede andere Verwendung von Farben mit der folgenden Verwendung von Farben in Windows kompatibel ist.



| Farbton | Bedeutung | Verwenden in Windows  |
|--------------------------------------|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Blau/Grün<br/>                | Windows-Marke<br/>                                                      | Hintergrund: Windows-Branding.<br/>                                                                                                                        |
| Glass, black, gray, white<br/> | Neutral<br/>                                                            | Hintergrund: Standardfensterrahmen, Startmenü, Taskleiste, Randleiste.<br/> Vordergrund: normaler Text.<br/>                                                |
| blue<br/>                      | start, commit<br/>                                                      | Hintergrund: Standardbefehlsschaltflächen, Suche, Anmeldung.<br/> Symbole: Informationen, Hilfe.<br/> Vordergrund: Hauptanweisungen, Links.<br/>           |
| Rot<br/>                       | error, stop, vulnerable, critical, immediate attention, restricted<br/> | Hintergrund: Status, Status beendet (Statusleisten).<br/> Symbole: error, stop, close window, delete, required input, missing, unavailable.<br/>     |
| yellow<br/>                    | Warnung, Vorsicht, fragebar<br/>                                     | Hintergrund: Status, angehaltener Fortschritt (Statusleisten).<br/> Symbole: Warnung<br/>                                                                       |
| green<br/>                     | go, proceed, progress, safe<br/>                                        | Hintergrund: Status, normaler Status (Statusleisten).<br/> Symbole: go, done, refresh.<br/> Vordergrund: Pfade und URLs (in Suchergebnissen).<br/> |
| purple<br/>                    | Besucht<br/>                                                            | Vordergrund: Besuchte Links (für Links in Windows Internet Explorer und Dokumenten).<br/>                                                                |



 

-   **Um die Kommunikation mit den vorherigen Bedeutungen zu vermeiden, wählen Sie Farben mit hoher mittlerer bis niedriger Sättigung und hoher oder niedriger Helligkeit aus.** Benutzer ordnen die vorherigen Bedeutungen Farben mit voller oder hoher Sättigung und Helligkeit auf mittlerem Niveau zu, sodass Sie diese Zuordnungen vermeiden können, indem Sie unterschiedliche Schattierungen auswählen.

![Abbildung, die zeigt, wie die Helligkeit die Farbe beeinflusst ](images/vis-color-image13.png)

In diesem Beispiel gibt es drei verschiedene Gelbschattierungen, aber nur der stark überleerte Helligkeitston der mittleren Ebene gibt eine Warnung aus. Das gelbe Ordnersymbol sieht nicht wie eine Warnung aus.

### <a name="using-color-with-data"></a>Verwenden von Farben mit Daten

-   Wenn dies hilfreich **ist, weisen Sie Daten Farbe zu, damit benutzer sie unterscheiden können.** Beachten Sie, dass Benutzer davon ausgehen, dass Daten mit ähnlichen Farben eine ähnliche Bedeutung haben.
-   **Weisen Sie standardmäßig Farben zu, die leicht zu unterscheiden sind.** Im Allgemeinen lassen sich Farben leicht unterscheiden, wenn sie in den HSL/HSV-Farbräumen weit voneinander entfernt sind, während gleichzeitig ein hoher Kontrast zum Hintergrund beibehalten wird:
    -   Wenn Sie Farben auswählen, bevorzugen Sie Triad-Färbungen oder ergänzende Farbtons, aber keine angrenzenden Farbtons.

        ![Abbildung, die zeigt, wie kontrastreiche Farben verwendet werden ](images/vis-color-image14.png)

        Wenn in diesem Beispiel die erste Farbzuweisung Rot ist, sollte die nächste Farbe Blau, Grün oder Zyan, aber nicht Magenta, Violett, Orange oder Gelb sein.

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

Im falschen Beispiel bezieht sich die Meldung auf die Windows-Internet Explorer informationsleiste durch ihre Farbe und nicht durch ihren Namen.

