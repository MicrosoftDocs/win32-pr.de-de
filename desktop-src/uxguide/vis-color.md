---
title: Color
description: Color ist ein wichtiges visuelles Element der meisten Benutzeroberflächen.
ms.assetid: 30a60e9e-ebb4-40f2-8535-a9b58dc668a8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ae58ddf232a3d8311a917ea0475c7aca1bae8949
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104132132"
---
# <a name="color"></a>Color

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Color ist ein wichtiges visuelles Element der meisten Benutzeroberflächen. Neben der reinen Ästhetik hat die Farbe Bedeutungen, und es werden emotionale Reaktionen hervorgerufen. Um Verwirrung zu vermeiden, muss die Farbe konsistent verwendet werden. Um die gewünschten emotionalen Antworten zu erhalten, muss die Farbe entsprechend verwendet werden.

Die Farbe wird häufig in Bezug auf einen Farbraum betrachtet, bei dem RGB (rot, grün, blau), HSL (Hue, Sättigung, Helligkeit) und HSV (Hue, Sättigung, Wert) die am häufigsten verwendeten Farbbereiche sind.

![Abbildung eines Cubes, der Farb Beziehungen anzeigt ](images/vis-color-image1.png)

Der RGB-Farbraum kann als Cube visualisiert werden.

Bei der Anzeige Technologie werden RGB-Werte verwendet, und die Entwickler betrachten daher häufig Farben in Bezug auf RGB. der RGB-Farbraum entspricht nicht der Art und Weise, in der die Farbe der Farben Wenn Sie z. b. "dunkel cyan" rot hinzufügen, wird das Ergebnis nicht als rot, sondern als heller Cyan wahrgenommen.

![Abbildung von dunklen und hellen Zyan-Quadraten ](images/vis-color-image2.png)

In diesem Beispiel ist das Hinzufügen von rot zu dunkel Zyan heller, nicht mehr rot. Der RGB-Farbraum entspricht nicht der Art und Weise, wie Benutzer die Farbe erkennen.

Die HSL/HSV-Farbbereiche bestehen aus drei Komponenten: Hue, Sättigung und Helligkeit oder Wert. Diese Farbbereiche werden häufig anstelle von RGB verwendet, da Sie besser mit der Wahrnehmung von Farben in Einklang stehen.

Der HSL-Farbraum bildet einen doppelten Kegel, der in der Mitte weiß, schwarz unten und neutral in der Mitte ist:

-   **Farbton:** Die Grundfarbe im Farbrad, die zwischen 0 und 360 Grad liegt, wobei 0 und 360 Grad rot sind.

    ![Abbildung eines Kreises, der Farb Beziehungen anzeigt ](images/vis-color-image3.png)

    Das Farbrad, bei dem rot 0 Grad beträgt, gelb 60 Grad, grün 120 Grad, Zyan 180 Grad, blau ist 240 Grad und Magenta ist 300 Grad.

-   **Sättigung:** Gibt an, wie rein (oder langweilig) die Farbe ist, von 0 bis 100, wobei 100 vollständig ausgelastet und 0 grau ist.
-   **Helligkeit:** Wie hell die Farbe ist, liegt zwischen 0 und 100, wobei 100 so hell wie möglich ist (weiß, unabhängig von Farbton und Sättigung) und 0 so dunkel wie möglich (schwarz) ist.

    ![Abbildung zur Veranschaulichung des HSL-Farbraum ](images/vis-color-image4.png)

    Der HSL-Farbraum kann als doppelter Kegel visualisiert werden.

Der HSV-Farbraum ist ähnlich, mit dem Unterschied, dass sein Bereich einen einzelnen Kegel bildet:

-   **Farbton:** Die Grundfarbe im Farbrad, die zwischen 0 und 360 Grad liegt, wobei 0 und 360 Grad rot sind.
-   **Sättigung:** Gibt an, wie rein (oder langweilig) die Farbe ist, von 0 bis 100, wobei 100 vollständig ausgelastet und 0 grau ist.
-   **Wert:** Die Farbe der Farbe liegt zwischen 0 und 100, wobei 100 so hell wie möglich ist (d. h. die Hälfte der Leuchtkraft im HSL-Bereich) und 0 so dunkel wie möglich (schwarz) ist.

    ![Abbildung der HSV-Farbraum ](images/vis-color-image5.png)

    Der HSV-Farbraum kann als einzelner Kegel visualisiert werden.

In HSL-und HSV-Leerzeichen, wenn Sättigung gleich 0 ist, gibt die Helligkeit einen grauen Farbton an. In Windows werden die HSL-und die HSV-Leerzeichen in der Regel einer Skala zwischen 0 und 240 neu zugeordnet, damit Farben mit einem 32-Bit-Wert dargestellt werden können.

**Hinweis:** Richtlinien, die sich auf [Schriftarten](vis-fonts.md) und [Barrierefreiheit](inter-accessibility.md) beziehen, werden in separaten Artikeln dargestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

Durch die effektive Verwendung von Color kann die Benutzeroberfläche des Programms effektiver werden. Die Farbe kann Benutzern helfen, bestimmte Bedeutungen auf einen Blick zu verstehen. Durch die Farbe kann Ihr Produkt auch ästhetisch ansprechend und verfeinert erscheinen.

Leider ist es ganz einfach, die Farbe ineffektiv zu verwenden, insbesondere, wenn Sie nicht im visuellen Design geschult sind. Schlechte Verwendung von Farben führt zu Entwürfen, die Unprofessional, veraltet, verwirrend oder einfach hässlich betrachten. Eine schlechte Verwendung von Farben kann schlimmer sein als die Verwendung der Farbe überhaupt nicht.

In diesem Abschnitt wird erläutert, was Sie wissen müssen, um die Farbe effektiv zu verwenden.

### <a name="how-color-is-used"></a>Verwendung der Farbe

Die Farbe wird normalerweise in der Benutzeroberfläche für die Kommunikation verwendet:

-   **D.h..** Die Bedeutung einer Nachricht kann durch Farbe zusammengefasst werden. Beispielsweise wird "Color" häufig verwendet, um den Status zu kommunizieren, bei dem "Red" ein Problem oder Fehler ist, gelb "Vorsicht" oder "Warnung" ist und grün ist
-   **Land.** Der Zustand eines Objekts kann durch Farbe angegeben werden. Beispielsweise verwendet Windows Color zum Angeben von Auswahl-und Hover-Zuständen. Links innerhalb von Webseiten verwenden Blue für nicht besuchte und lila für den Besuch.
-   **Zierungen.** Es wird davon ausgegangen, dass es eine Beziehung zwischen Elementen derselben Farbe gibt, sodass die Farbcodierung eine effektive Möglichkeit zur Unterscheidung zwischen Objekten ist. Beispielsweise verwenden Aufgabenbereiche in einem System Steuerungselement einen grünen Hintergrund, um Sie visuell vom Hauptinhalt zu trennen. Außerdem ermöglicht Microsoft Outlook Benutzern das Zuweisen verschiedener farbiger Flags zu Nachrichten.
-   **Akzente.** Die Farbe kann verwendet werden, um die Aufmerksamkeit von Benutzern zu zeichnen. Windows verwendet z. b. blaue [Haupt Anweisungen](text-ui.md) , um Sie beim Einstieg aus dem anderen Text zu unterstützen.

Natürlich wird die Farbe aus rein ästhetischen Gründen häufig in Grafiken verwendet. Obwohl die Ästhetik wichtig ist, sollten Sie die Farben der UI-Elemente in erster Linie auf Grundlage ihrer Bedeutung, nicht wie Sie aussehen.

### <a name="color-interpretation"></a>Farb Interpretation

**Die Interpretation der Farbe von Benutzern ist oft von der Kultur abhängig.** Beispielsweise ist in der USA das Hochzeits Zeichen für die Braut größtenteils mit der Farbe weiß verknüpft, während "Black" den Bestattungs Zeichen zugeordnet ist. Vor langer Zeit in Japan war die Farbsymbolik nur das Gegenteil: weiß war die vorherrschende Farbe bei der Beerdigung, und Black wurde als eine Farbe angesehen, die für das hoch-und hoch-und hoch-bis zu einem guten Erfolg sorgt

Das heißt, **die Interpretation von rot, gelb und grün für den Status ist global global.** Dies liegt an der [UNESCO-Wien-Konvention auf Straßen Vorzeichen und Signalen](https://www.unece.org/trans/conventn/signalse.pdf), die die weltweite Konvention für Verkehrs Leuchten definiert (wobei rot das Ende bedeutet, Grün bedeutet fortfahren, und Gelb bedeutet, dass Sie mit Vorsicht fortfahren). Diese Status Farben können ohne Rücksicht auf Kultur abhängige Interpretationen verwendet werden.

Neben den Status Farben weist Windows den Farben auf der Grundlage der Konvention Bedeutungen zu, wie im Abschnitt "Richtlinien" in diesem Artikel dargestellt. Stellen Sie sicher, dass die Farbverwendung des Programms mit diesen Farb Konventionen kompatibel ist.

### <a name="color-accessibility"></a>Farb Barrierefreiheit

Die Verwendung von Color wirkt sich auf den Zugriff ihrer Software auf die größtmögliche Zielgruppe aus. Benutzer mit Blindheit oder Sehbehinderung sind möglicherweise nicht in der Lage, die Farben zu erkennen, wenn überhaupt. Ungefähr 8 Prozent der Erwachsenen Männer haben eine Form von Farb Verwirrung (häufig fälschlicherweise als "Farb Blindheit" bezeichnet), von der rot-grün-Farb Verwirrung am häufigsten ist.

![Darstellung der in der Regel angezeigten Primärfarben ](images/vis-color-image6.png)

Die Primärfarben, wie Sie mit normaler Farbvision sichtbar sind.

![Abbildung der gleichen Farben wie bei Protanopia ](images/vis-color-image7.png)

Die Primärfarben wie bei Protanopia (1% der männlichen Population).

![Abbildung der gleichen Farben wie bei Deuteranopia ](images/vis-color-image8.png)

Die Primärfarben, wie Sie mit Deuteranopia (6% der männlichen Population) angezeigt werden.

![Abbildung der gleichen Farben wie bei tritanopia ](images/vis-color-image9.png)

Die Primärfarben wie bei tritanopia (1% der männlichen Population).

Weitere Informationen finden Sie unter [können Color-Blind Benutzer Ihre Website sehen?](/previous-versions/windows/internet-explorer/ie-developer/)

### <a name="use-color-to-reinforce-visually"></a>Farben zur visuellen Verstärkung verwenden

Die beste Lösung für die Farb Interpretation und Barrierefreiheits Probleme ist die Verwendung von Farben, um die Bedeutung einer dieser primären Kommunikationsmethoden visuell zu verstärken:

-   **Text.** Beim präzisen Text handelt es sich in der Regel um die effektivste primäre Kommunikation entweder direkt auf der Benutzeroberfläche oder über eine QuickInfo.

![Screenshot eines kleinen roten Symbols mit QuickInfo ](images/vis-color-image10.png)

In diesem Beispiel wird der QuickInfo-Text verwendet, um die Bedeutung eines Symbols zu kommunizieren.

-   **Ausge.** Symbole lassen sich leicht durch die Entwürfe unterscheiden, insbesondere die Konturform.

![Screenshot der Symbole in Graustufen (Graustufen) ](images/vis-color-image11.png)

In diesem Beispiel können die Standardsymbole basierend auf ihren Entwürfen leicht unterschieden werden.

-   **Hotels.** Der relative Speicherort kann auch verwendet werden, aber dieser Ansatz ist schwächer als die Alternativen. Um effektiv zu sein, sollte der Speicherort "Standard" und "bekannt" lauten, wie bei Verkehrs Leuchten.

Obwohl Color das offensichtlichste Attribut von vielen Entwürfen ist, muss es immer redundant sein.

### <a name="designing-with-color"></a>Entwerfen mit Farbe

Ironischerweise ist die beste Methode zum Entwerfen von Farben zunächst das Entwerfen ohne Farbe, die Verwendung von [Draht Modelle](glossary.md) oder Chrome und das anschließende Hinzufügen von Farben zu einem späteren Zeitpunkt. Dadurch wird sichergestellt, dass die Informationen nicht allein mithilfe von Farben kommuniziert werden. Außerdem können Sie sicherstellen, dass Ihre Ausdrucke in Monochrom-Druckern hervorragend aussehen.

### <a name="use-theme-or-system-colors"></a>Design-oder Systemfarben verwenden

Obwohl es viele komplexe Faktoren bei der effektiven Verwendung von Farben gibt, wird in der Windows-Benutzeroberfläche die Auswahl von Farbe häufig auf die Auswahl der passenden Design [Farbe](glossary.md) oder der [System Farbe](glossary.md) nach einigen einfachen Regeln beschränkt. Benutzer können dann diese Farbschemas auswählen und anpassen.

Auf diese Weise können Sie nicht nur die Farbeinstellungen aller Benutzer abdecken, sondern Sie können auch das richtige Farbschema auswählen, das für alle Geschmacksrichtungen, Stile und Kulturen geeignet ist (was natürlich nicht möglich ist).

**Wenn Sie nur eine Aktion ausführen...**

Wählen Sie Farben aus, indem Sie die entsprechende Design Farbe oder System Farbe auswählen. Verwenden Sie die Farbe nie als primäre Kommunikationsmethode, sondern als sekundäre Methode, um die Bedeutung visuell zu verstärken. Entwerfen Sie mithilfe von Draht Modelle oder Chrome, um sicherzustellen, dass die Farbe sekundär ist.

### <a name="use-theme-or-system-colors-correctly"></a>Design-oder Systemfarben ordnungsgemäß verwenden

Angenommen, Benutzer wählen Design-oder Systemfarben auf der Grundlage Ihrer persönlichen Anforderungen aus, und das Design oder die Systemfarben sind entsprechend konstruiert. Wenn Sie auf der Grundlage dieser Annahme immer Design-oder Systemfarben auf der Grundlage ihres vorgesehenen zwecks und ihrer zugehörigen Hintergründe auswählen, sind die Farben garantiert lesbar und berücksichtigen die Anforderungen der Benutzer in allen Video Modi, einschließlich des [Modus für hohe Kontraste](glossary.md). Beispielsweise ist es garantiert, dass die Fenster Text-System Farbe für die Hintergrundsystem Farbe des Fensters lesbar ist.

Insbesondere immer:

-   **Wählen Sie die Farben auf Grundlage ihres Zwecks aus.** Wählen Sie auf der Grundlage ihrer aktuellen Darstellung keine Farben aus, da diese Darstellung vom Benutzer oder von zukünftigen Windows-Versionen geändert werden kann.
-   **Vergleichen Sie die Vorder Grundfarben mit ihren zugeordneten Hintergrundfarben.** Vorder Grundfarben sind garantiert nur für die zugehörigen Hintergrundfarben lesbar. Kombinieren Sie nicht die Vorder Grundfarben mit anderen Hintergrundfarben oder noch schlimmer, andere Vordergrund Farben.
-   **Farben Typen nicht kombinieren.** Das heißt, Sie sollten immer Design Farben mit den zugehörigen Design Farben, Systemfarben mit den zugeordneten Systemfarben und hart verdrahteten Farben mit anderen hart verdrahteten Farben vergleichen. Beispielsweise ist es nicht garantiert, dass eine Design Textfarbe für einen hart verdrahteten Hintergrund lesbar ist.
-   **Wenn Sie Farben hart verdrahtet müssen, behandeln Sie den Modus für hohe Kontraste als Sonderfall.**

**Wenn Sie nur eine Aktion ausführen...**

Wählen Sie immer Design-oder Systemfarben auf Grundlage ihres beabsichtigten Zwecks aus, und koppeln Sie die zugehörigen Hintergründe.

### <a name="using-other-colors"></a>Verwenden von anderen Farben

Während das Windows-Design einen umfassenden Satz von Design Teilen definiert, stellen Sie möglicherweise fest, dass das Programm Farben benötigt, die nicht in der Designdatei definiert sind. Obwohl Sie diese Farben hart übertragen konnten, empfiehlt es sich, Farben aus dem Design oder den Systemfarben abzuleiten. Bei der strategischen Verwendung dieses Ansatzes erhalten Sie alle Vorteile der Verwendung von Design-und Systemfarben, aber mit viel mehr Flexibilität.

Nehmen Sie beispielsweise an, dass Sie einen Fenster Hintergrund benötigen, der dunkler als die Hintergrundfarbe des Design Fensters ist. Im HSL-Farbraum bedeutet eine dunklere Farbe eine Farbe mit einer niedrigeren Helligkeit. Daher können Sie mithilfe der folgenden Schritte eine dunklere Fenster Hintergrundfarbe ableiten:

-   Ruft das Hintergrunddesign Color RGB des Fensters ab.
-   Konvertieren Sie den RGB-Wert in seinen HSL-Wert.
-   Verringern Sie den Wert für die Helligkeit (etwa 20 Prozent).
-   Konvertieren Sie zurück in RGB-Werte.

Bei diesem Ansatz wird die abgeleitete Farbe garantiert als dunkler Farbton der ursprünglichen Farbe wahrgenommen (es sei denn, die ursprüngliche Farbe war sehr dunkel, um mit zu beginnen).

![Darstellung der Auswirkungen der reduzierten Helligkeit ](images/vis-color-image12.png)

In diesem Beispiel wird die Hintergrundfarbe des dunkleren Fensters von der Design Farbe abgeleitet.

### <a name="testing-colors"></a>Testen von Farben

Um festzustellen, ob die Verwendung von Color auf das Programm zugänglich ist und nicht als primäre Kommunikationsmethode verwendet wird, empfehlen wir die Verwendung der [Fujitsu colordoctor](https://www.fujitsu.com/global/about/businesspolicy/tech/design/) -oder der [Vischeck](https://www.vischeck.com/) -Hilfsprogramme, um Folgendes zu überprüfen:

-   Gesamt Abhängigkeit von der Farbe mit dem grauen Skalierungs Filter.
-   Bestimmte Farb Verwirrungen bei der Verwendung der Filter "Protanopia", "Deuteranopia" und "tritanopia".

Testen Sie Ihr Programm in den folgenden Modi, um zu bestimmen, ob die Verwendung von Color in Ihrem Programm ordnungsgemäß programmiert ist:

-   Design aktiviert mit dem standardmäßigen Windows-Design.
-   Design aktiviert mit einem nicht standardmäßigen Design.
-   Design deaktiviert ("klassisches Windows-Format" in den Design Einstellungen im System Steuerungselement der Personalisierung).
-   Hoher Kontrast Schwarz (weißer Text in schwarzem Hintergrund).
-   Hoher Kontrast weiß (schwarzer Text auf einem weißen Hintergrund).

Alle Bildschirmelemente sollten lesbar und erwartungsgemäß angezeigt werden, auch unmittelbar nach dem Ändern des Modus.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie die Farbe nie als primäre Kommunikationsmethode,** sondern als sekundäre Methode, um die Bedeutung visuell zu verstärken.

### <a name="using-theme-and-system-colors"></a>Verwenden von Design-und Systemfarben

-   **Wählen Sie nach Möglichkeit Farben aus, indem Sie die entsprechende Design Farbe oder System Farbe auswählen.** Auf diese Weise können Sie die Farbeinstellung der Benutzer immer respektieren.
-   **Wählen Sie Design-und Systemfarben auf Grundlage ihres Zwecks aus.** Wählen Sie auf der Grundlage ihrer aktuellen Darstellung keine Farben aus, da diese Darstellung vom Benutzer oder von zukünftigen Windows-Versionen geändert werden kann.
-   **Vergleichen Sie die Vorder Grundfarben mit ihren zugeordneten Hintergrundfarben.** Vorder Grundfarben sind garantiert nur für die zugehörigen Hintergrundfarben lesbar. Kombinieren Sie nicht die Vorder Grundfarben mit anderen Hintergrundfarben oder noch schlimmer, andere Vordergrund Farben.
-   **Farben Typen nicht kombinieren.** Das heißt, Sie sollten immer Design Farben mit den zugehörigen Design Farben, Systemfarben mit den zugeordneten Systemfarben und hart verdrahteten Farben mit anderen hart verdrahteten Farben vergleichen. Beispielsweise ist es nicht garantiert, dass eine Design Textfarbe für einen hart verdrahteten Hintergrund lesbar ist.
-   **Wenn Sie eine Farbe verwenden müssen, die kein Design oder keine System Farbe ist:**
    -   **Ziehen Sie es vor, die Farbe von einem Design oder einer System Farbe zu ableiten, wenn Sie Ihren Wert hart verknüpfen.** Verwenden Sie den weiter oben in diesem Artikel beschriebenen Prozess, in dem Sie andere Farben verwenden.
    -   **Behandeln Sie den Modus für hohe Kontraste als Sonderfall.**
-   **Behandeln von Designänderungen.** Designänderungen werden von Windows automatisch mit Standardfenster Frames und allgemeinen Steuerelementen behandelt. Fenster mit benutzerdefinierten Fensterrahmen, benutzerdefinierten Steuerelementen oder Steuerelementen für den Besitzer zeichnen und andere Farbverwendung müssen Designänderungen explizit verarbeiten.
    -   **Entwickler:** Sie können auf Design Änderungs Ereignisse reagieren, indem Sie die WM- \_ Nachricht verarbeiten.

### <a name="color-meaning"></a>Farbe, Bedeutung

-   Sie sollten zwar immer Design-und Systemfarben (oder abgeleitete Farben) verwenden, stellen Sie jedoch sicher, dass jede andere Verwendung von Color mit der folgenden Verwendung von Farbe in Windows kompatibel ist.



|                                      |                                                                               |                                                                                                                                                                 |
|--------------------------------------|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Farbton**<br/>                   | **Bedeutung**<br/>                                                        | **Verwendung in Windows**<br/>                                                                                                                                   |
| blau/grün<br/>                | Windows-Marke<br/>                                                      | Hintergrund: Windows-Branding.<br/>                                                                                                                        |
| Glas, schwarz, grau, weiß<br/> | Neutral<br/>                                                            | Hintergrund: Standardfenster Rahmen, Startmenü, Taskleiste, Rand Leiste.<br/> Vordergrund: normaler Text.<br/>                                                |
| blue<br/>                      | starten, Commit<br/>                                                      | Hintergrund: Standard Befehls Schaltflächen, suchen, anmelden.<br/> Symbole: Informationen, Hilfe.<br/> Vordergrund: Haupt Anweisungen, Links.<br/>           |
| Rot<br/>                       | Fehler, Beendigung, anfällig, kritisch, unmittelbare Aufmerksamkeit, eingeschränkt<br/> | Hintergrund: Status, Status wird beendet (Statusanzeige).<br/> Symbole: Fehler, beenden, Fenster schließen, löschen, erforderliche Eingabe, fehlt, nicht verfügbar.<br/>     |
| yellow<br/>                    | Warnung, Vorsicht, fragwürdig<br/>                                     | Hintergrund: Status, angehaltene Status (Status leisten).<br/> Symbole: Warnung<br/>                                                                       |
| green<br/>                     | Los, fortfahren, Status, sicher<br/>                                        | Hintergrund: Status, normaler Status (Status leisten).<br/> Symbole: Gehe zu, abgeschlossen, aktualisieren.<br/> Vordergrund: Pfade und URLs (in den Suchergebnissen).<br/> |
| purple<br/>                    | besichtigt<br/>                                                            | Vordergrund: besuchte Links (für Links in Windows Internet Explorer und Dokumenten).<br/>                                                                |



 

-   **Um die Kommunikation mit der vorherigen Bedeutung zu vermeiden, wählen Sie Farben mit hoher oder niedriger Sättigung und hoher oder niedriger Helligkeit aus.** Benutzer ordnen die vorherige Bedeutungen Farben zu, die über eine vollständige oder hohe Sättigung und mittelgroße Helligkeit verfügen, sodass Sie diese Zuordnungen vermeiden können, indem Sie unterschiedliche Schattierungen auswählen.

![Abbildung, die zeigt, wie sich Helligkeit auf Farbe auswirkt ](images/vis-color-image13.png)

In diesem Beispiel gibt es drei verschiedene Schattierungen von gelb, aber nur der stark satte, Mittelwert Ende Helligkeit gibt eine Warnung aus. Das gelbe Ordnersymbol hat keine Warnung.

### <a name="using-color-with-data"></a>Verwenden von Color mit Daten

-   Wenn dies hilfreich ist, **weisen Sie Daten zu, damit Sie von Benutzern unterschieden** werden können. Beachten Sie, dass die Benutzer davon ausgehen, dass Daten mit ähnlichen Farben eine ähnliche Bedeutung haben.
-   **Weisen Sie standardmäßig Farben zu, die leicht zu unterscheiden sind.** Im Allgemeinen sind Farben leicht zu unterscheiden, wenn Sie sich in den HSL/HSV-Farbräumen weit voneinander unterscheiden, während Sie einen hohen Kontrast mit dem Hintergrund behalten:
    -   Wenn Sie Farben auswählen, bevorzugen Sie Triad-Harmonien oder ergänzende Schattierungen, aber keine angrenzenden Farben.

        ![Abbildung zeigt, wie Kontrastfarben ausgewählt werden ](images/vis-color-image14.png)

        Wenn die erste Farb Zuweisung in diesem Beispiel rot ist, sollte die nächste Farbe blau, grün oder Cyan lauten, aber nicht Magenta, lila, Orange oder gelb.

    -   Farben haben einen hohen Kontrast, wenn ein großer Unterschied in Ihrem Farbton, der Sättigung oder der Helligkeit vorliegt.

        ![Abbildung, die eine Farbe auf verschiedenen Hintergründen anzeigt ](images/vis-color-image15.png)

        In diesem Beispiel steht die helle blaue Basis Farbe im Gegensatz zu Hintergründen mit großen Unterschieden in Farbton, Sättigung oder Helligkeit.

    -   Durch die Verwendung eines weißen oder sehr hellen Hintergrunds können gegensätzliche Vorder Grundfarben leichter unterschieden werden.

        ![Abbildung zur Veranschaulichung von gutem und mangelhafter Kontrast ](images/vis-color-image16.png)

        In diesem Beispiel wird die Vordergrundfarbe durch weiße und helle Hintergrundfarben leichter zu unterscheiden.

-   **Ermöglicht es Benutzern, diese Farbzuweisungen anzupassen, weil die** Farbauswahl subjektivere und persönliche Vorlieben ist. Wenn viele koordinierte Farben vorhanden sind, können Sie es Benutzern ermöglichen, Sie mithilfe von Farbschemas als Gruppe zu ändern.
-   **Ermöglicht es Benutzern, diese Farbzuweisungen zu bezeichnen.** Auf diese Weise können Sie leichter identifizieren und Auffinden.
-   **Anders als Benutzeroberflächen Farben sollten sich Daten nicht ändern, wenn sich die Systemfarben ändern.**

## <a name="documentation"></a>Dokumentation

-   **Verweisen Sie auf Benutzeroberflächen Elemente anhand ihrer Namen, nicht anhand ihrer Farben.** Verweise auf solche Verweise sind nicht verfügbar, und die Systemfarben können sich ändern. Wenn der Name eines Benutzeroberflächen Elements nicht bekannt ist oder nicht aussagekräftig genug ist, zeigen Sie einen Screenshot, um ihn zu verdeutlichen.

**Richtig:**

![Screenshot der Nachricht mit der Informationsleiste ](images/vis-color-image17.png)

**Falsch:**

![Screenshot der Nachricht mit "Gold Bar" ](images/vis-color-image18.png)

Im falschen Beispiel bezieht sich die Meldung auf die Informationsleiste von Windows Internet Explorer und nicht auf Ihren Namen.

