---
title: Tastatur
description: Die Tastatur ist das primäre Eingabegerät, das für die Texteingabe in Microsoft Windows verwendet wird. Für Barrierefreiheit und Effizienz können die meisten Aktionen auch über die Tastatur ausgeführt werden.
ms.assetid: 27185c98-1233-4e26-a156-0ff080fd4db3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 4339dfd8d4d31d0d8859dcedd07fc287426b04c0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104564362"
---
# <a name="keyboard"></a>Tastatur

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Die Tastatur ist das primäre Eingabegerät, das für die Texteingabe in Microsoft Windows verwendet wird. Für Barrierefreiheit und Effizienz können die meisten Aktionen auch über die Tastatur ausgeführt werden.

Tastaturen können auch auf virtuelle, Bildschirmtastatur und das Schreiben von Pads verweisen, die von Computern ohne physische Tastatur verwendet werden, z. b. Tablet-basierte Computer.

![Screenshot der Bildschirmtastatur ](images/inter-keyboard-image1.png)

Die Windows-Tablet-und-Touchtechnologie auf der Bildschirmtastatur.

![Screenshot des Windows-Tablet-schreibaufads ](images/inter-keyboard-image2.png)

Der Windows-Tablet-und Touchtechnologie-Schreibvorgang.

Es gibt sechs grundlegende Arten von Schlüsseln:

-   Ein Zeichen Schlüssel sendet ein Literalzeichen an das Fenster mit dem Eingabefokus.
-   Eine Modifizierertaste, die mit einem anderen Schlüssel kombiniert ist, ändert die Bedeutung des zugeordneten Schlüssels, z. b. STRG, alt, Umschalttaste und Windows-Logo-Taste.
-   Bei den Navigations Schlüsseln handelt es sich um die direktionalen Pfeile sowie zu Startseite, Ende, Bild-auf und Bild-ab.
-   Die Bearbeitungs Schlüssel sind INSERT, Backspace und DELETE.
-   Die Funktionstasten sind F1 bis F12.
-   Systemschlüssel versetzen das System in einen Modus oder führen eine System Aufgabe aus, z. b. druckbildschirm, Feststell Sperre und Num-Sperre.

Zugriffsschlüssel sind Schlüssel oder Tastenkombinationen, die für den Zugriff auf die Interaktion mit allen Steuerelementen oder Menü Elementen mithilfe der Tastatur verwendet werden. Tastenkombinationen sind Schlüssel oder Tastenkombinationen, die von fortgeschrittenen Benutzern verwendet werden, um häufig verwendete Befehle für Effizienz auszuführen. Windows gibt Zugriffsschlüssel durch Unterstreichung der Zugriffsschlüssel Zuweisung an.

![Screenshot der Zugriffstasten und Tastenkombinationen ](images/inter-keyboard-image3.png)

Dieses Beispiel zeigt sowohl Zugriffsschlüssel als auch Tastenkombinationen.

Um die visuelle Übersichtlichkeit auszuschließen, verbirgt Windows standardmäßig Zugriffsschlüssel-Unterstriche und zeigt Sie nur an, wenn die Alt-Taste gedrückt wird. Um die Konsistenz mit Windows aufrechtzuerhalten, werden die Bilder im UX-Handbuch ebenfalls angezeigt, wenn die Zugriffstaste ausgeblendet ist, es sei denn, die Richtlinie umfasst Zugriffsschlüssel.

Um das Bewusstsein der Zugriffsschlüssel Zuweisungen in Ihrem Programm während des gesamten Entwicklungsprozesses zu verbessern, können Sie diese jederzeit anzeigen. Wechseln Sie in der Systemsteuerung zu Easy of Access Center, und klicken Sie auf **Tastatur leichter zu verwenden**. Aktivieren Sie dann das Kontrollkästchen **Tastenkombinationen und Zugriffstasten unterstreichen** .

**Hinweis:** Richtlinien im Zusammenhang mit [Barrierefreiheit](inter-accessibility.md) werden in einem separaten Artikel dargestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="elements-of-keyboard-navigation"></a>Elemente der Tastaturnavigation

Benutzer interagieren mit einem Fenster mithilfe der Tastatur, indem Sie zu den Steuerelementen navigieren, Auswahl treffen und Befehle ausführen. Die folgenden Elemente werden zusammen verwendet, um dies zu erreichen.

![Screenshot des Dialog Felds "Farben bearbeiten" ](images/inter-keyboard-image4.png)

Um die Elemente der Tastaturnavigation in der folgenden Liste zu veranschaulichen, wird dieses Dialogfeld angezeigt.

-   **Eingabefokus.** Das Steuerelement mit dem Eingabefokus erhält die meisten Tastatureingaben. Der Eingabefokus wird durch ein gepunktetes Rechteck mit dem Namen Fokus Rechteck angegeben. Einige Tastatureingaben werden an Steuerelemente gesendet, die keinen Eingabefokus haben, wie weiter unten erläutert.

    ![Screenshot der ersten Zeile im Dialogfeld "Farben bearbeiten" ](images/inter-keyboard-image5.png)

    Das erste Standardfarben-Steuerelement hat den Eingabefokus, wie durch ein gepunktetes Rechteck angegeben.

-   **Tab-Taste und Tabstopps.** Die Tab-Taste ist der primäre Mechanismus für die Navigation innerhalb eines Fensters. Die Tab-Taste greift nur auf die Steuerelemente mit einem Tabstopp zu. Alle interaktiven Steuerelemente (die nicht in einer Gruppe enthalten sind) sollten über Tabstopps verfügen, nicht interaktive Steuerelemente, z. B. Beschriftungen, dagegen nicht.
-   **Tab-Reihenfolge.** Alle Steuerelemente mit Tabstopps werden in der Aktivier Reihenfolge besucht. Durch Drücken der Tab-Taste wird der Eingabefokus auf das nächste Steuerelement in der Aktivier Reihenfolge verschoben, während durch Drücken der UMSCHALTTASTE + TAB der Eingabefokus
-   **Steuerelement Gruppen.** Eine Gruppe verwandter Steuerelemente kann in einer Gruppe erstellt werden, und Ihnen wird ein einzelner Tabstopp zugewiesen. Steuerelementgruppen werden für Steuerelemente verwendet, die sich wie ein einzelnes Steuerelement verhalten, z. B. Optionsfelder. Sie können auch verwendet werden, wenn es zu viele Steuerelemente für eine effiziente Navigation mit der TAB-TASTE allein gibt.

    ![Screenshot der Gruppen "Basic" und "Custom Colors" ](images/inter-keyboard-image6.png)

    Grundlegende Farben und benutzerdefinierte Farben sind Steuerelement Gruppen, die diesem Dialogfeld fünf Tabstopps geben. Es gibt so viele Steuerelemente, dass die Navigation ineffizient wäre, ohne Steuerungsgruppen zu verwenden.

-   **Pfeiltasten.** Die Pfeiltasten bewegen den Eingabefokus zwischen den Steuerelementen innerhalb einer Gruppe. Durch Drücken der nach-rechts-Taste wird der Eingabefokus auf das nächste Steuerelement in der Aktivier Reihenfolge verschoben, während durch Drücken des linken Pfeils der Eingabefokus auf das vorherige "Home", "End", "up" und "Down" haben auch das erwartete Verhalten innerhalb einer Gruppe. Benutzer können mithilfe von Pfeiltasten nicht aus einer Steuerelement Gruppe navigieren.
-   **Standard Schaltflächen.** Fenster mit Befehls Schaltflächen und Befehls Verknüpfungen haben eine einzelne Standard Schaltfläche, die durch einen markierten Rahmen angegeben wird. Dies ist die Schaltfläche, auf die beim Drücken der EINGABETASTE geklickt wird. Standardmäßig ist eine einzelne Standard Befehls Schaltfläche oder ein Befehls Link zugewiesen. Die Standard Schaltfläche wird jedoch verschoben, wenn der Benutzer auf eine andere Befehls Schaltfläche oder einen Befehls Link klickt. Folglich sind auch alle Befehls Schaltflächen oder Befehls Verknüpfungen mit dem Eingabefokus immer die Standard Schaltfläche.

    ![Screenshot der Schaltflächen "OK" und "Abbrechen" ](images/inter-keyboard-image7.png)

    Die Schaltfläche OK ist normalerweise die Standard Schaltfläche, die durch den markierten Rahmen angegeben wird. Wenn der Benutzer jedoch mit der Schaltfläche Abbrechen auf die Schaltfläche Abbrechen klickt, wird er zur Standard Schaltfläche, die mit der EINGABETASTE aktiviert wird.

-   **Leertaste, EINGABETASTE und ESC-Taste.** Die Leertaste aktiviert das Steuerelement mit dem Eingabefokus, während mit der EINGABETASTE die Standard Schaltfläche aktiviert wird. Durch Drücken der ESC-Taste wird das Fenster abgebrochen oder geschlossen.
-   **Zugriffsschlüssel.** Zugriffsschlüssel werden verwendet, um direkt mit Steuerelementen zu interagieren, anstatt mit der Registerkarte zu navigieren. Sie werden mit der Alt-Taste kombiniert und in ihrer Bezeichnung mit einem unterstrichenen Buchstaben angegeben.
-   **Zugriffsschlüssel Bezeichnungen.** Während einige Steuerelemente eigene Bezeichnungen enthalten, wie z. b. Befehls Schaltflächen, Kontrollkästchen und Options Felder, haben andere Steuerelemente externe Bezeichnungen, z. b. Listenfelder und Struktur Ansichten. Bei externen Bezeichnungen wird die Zugriffstaste der Bezeichnung zugewiesen, und wenn Sie aufgerufen wird, navigiert zum nächsten Steuerelement in der Aktivier Reihenfolge. Schaltflächen mit der Bezeichnung OK, Abbrechen und schließen werden keine Zugriffsschlüssel zugewiesen, da Sie mit Enter und ESC aufgerufen werden.

    ![Screenshot von Bezeichnungen mit "b" und "d" unterstrichen ](images/inter-keyboard-image8.png)

    Durch Drücken von ALT + B gelangen Sie zur ausgewählten Grundfarbe. Drücken Sie ALT + D, klicken Sie auf die Schaltfläche benutzerdefinierte Farben definieren, geben Sie die Schaltfläche OK ein, und ESC ruft Abbrechen auf.

-   **Zugriffsschlüssel Verhalten.** Wenn eine Zugriffstaste aufgerufen und eindeutig zugewiesen wird, wird auf das zugeordnete Steuerelement geklickt. Wenn die Zuweisung nicht eindeutig ist, erhält das zugeordnete Steuerelement den Eingabefokus. Wenn der Benutzer denselben Zugriffsschlüssel erneut eingibt, erhält das nächste Steuerelement in der Aktivier Reihenfolge mit derselben Zuweisung den Eingabefokus.

Dieser Mechanismus ist zwar recht kompliziert, aber auch recht intuitiv. Die meisten dieser Details werden von den Benutzern sofort übernommen, auch wenn nur wenige genau erklären können, wie Sie funktionieren.

### <a name="keyboard-support-for-accessibility-and-advanced-users"></a>Tastatur Unterstützung für Barrierefreiheit und fortgeschrittene Benutzer

**In Windows ist der Entwurf für die Tastatur auf die Bereitstellung einer gut entworfenen Tastaturnavigation, Zugriffstasten für Barrierefreiheit und Tastenkombinationen für fortgeschrittene Benutzer beschränkt.**

Um sicherzustellen, dass die Funktionalität Ihres Programms für die verschiedensten Benutzer, einschließlich derjenigen mit Behinderungen und Behinderungen, problemlos verfügbar ist, muss auf alle interaktiven Benutzeroberflächen Elemente (UI) zugegriffen werden können. Im Allgemeinen bedeutet dies, dass die am häufigsten verwendeten Benutzeroberflächen Elemente mithilfe eines einzelnen Zugriffsschlüssels oder einer Tastenkombination zugänglich sind, während weniger häufig verwendete Elemente eine zusätzliche Tab-oder Pfeiltasten Navigation erfordern können. Für diese Benutzer ist Vollständigkeit wichtiger als Konsistenz.

Um sicherzustellen, dass die Funktionalität Ihres Programms für erfahrene Benutzer effizient ist, sollten häufig verwendete Benutzeroberflächen Elemente auch Tastenkombinationen für den direkten Tastatur Zugriff aufweisen. Erfahrene Benutzer haben oftmals eine starke Vorliebe für die Verwendung der Tastatur, da tastaturbasierte Befehle viel schneller eingegeben werden können. Zudem ist es dafür nicht erforderlich, die Hände von der Tastatur wegzubewegen. Für diese Benutzer sind Effizienz und Konsistenz entscheidend. Die Vollständigkeit hingegen ist nur für am häufigsten verwendeten Befehle wichtig.

Es gibt feine Unterschiede beim Entwerfen des Tastatur Zugriffs für diese beiden Gruppen, weshalb Windows zwei unabhängige Mechanismen für den direkten Tastatur Zugriff bietet. Durch die effektive Verwendung von Zugriffs-und Tastenkombinationen können Sie Ihren Programmen einen effizienten, konsistenten und umfassenden Tastatur Zugriff bieten, der für alle Benutzer von Vorteil ist.

### <a name="access-keys"></a>Zugriffsschlüssel

Zugriffstasten weisen die folgenden Merkmale auf:

-   Sie verwenden ALT und eine alphanumerische Taste.
-   Sie dienen in erster Linie der Barrierefreiheit.
-   Sie sind allen Menüs und den meisten Dialogfeldsteuerelementen zugewiesen.
-   Ihre Speicherung ist nicht vorgesehen, daher werden sie direkt in der UI dokumentiert, indem das entsprechende Steuerelement-Beschriftungszeichen unterstrichen wird.
-   Sie wirken sich nur auf das aktuelle Fenster aus und navigieren zum entsprechenden Menüelement oder Steuerelement.
-   Sie werden nicht konsistent zugewiesen, da dies nicht immer möglich ist. Zugriffstasten sollten jedoch für die am häufigsten verwendeten Befehle, insbesondere für Schaltflächen für den Commit, konsistent zugewiesen werden.
-   Sie sind lokalisiert.

**Da Zugriffsschlüssel nicht für die Speicherung vorgesehen sind, werden Sie einem Zeichen zugewiesen, das sich früh in der Bezeichnung befindet, damit Sie leichter zu finden sind,** auch wenn ein Schlüsselwort vorhanden ist, das später in der Bezeichnung angezeigt wird.

**Richtig:**

![Screenshot des ersten Zeichens in der Bezeichnung unterstrichen ](images/inter-keyboard-image9.png)

**Falsch:**

![Screenshot von 20-ersten Zeichen unterstrichen ](images/inter-keyboard-image10.png)

Im richtigen Beispiel wird die Zugriffstaste einem Zeichen zugewiesen, das sich in der Bezeichnung frühzeitig in der Bezeichnung befindet.

### <a name="shortcut-keys"></a>Tastenkombinationen

Im Gegensatz dazu weisen Tastenkombinationen die folgenden Eigenschaften auf:

-   Sie verwenden primär die STRG- und Funktionstastensequenzen (Windows-Systemtastenkombinationen verwenden ebenfalls ALT in Verbindung mit nicht alphanumerischen Tasten und der Windows-Logo-Taste).
-   Sie dienen in erster Linie erweiterten Benutzer hinsichtlich Effizienz.
-   Sie werden nur den am häufigsten verwendeten Befehlen zugewiesen.
-   Ihre Speicherung ist vorgesehen, und sie werden nur in Menüs, QuickInfos und in der Hilfe dokumentiert.
-   Sie wirken sich auf das gesamte Programm aus, sie haben jedoch keine Auswirkung, wenn sie nicht angewendet werden.
-   Sie müssen konsistent zugewiesen werden, da sie gespeichert und nicht direkt dokumentiert werden.
-   Sie sind nicht lokalisiert.

**Da Tastenkombinationen für die Speicherung vorgesehen sind, werden die am häufigsten verwendeten Tastenkombinationen idealerweise Buchstaben aus den ersten oder am meisten einprägsamen Zeichen in den Schlüsselwörtern des Befehls verwendet,** wie z. b. STRG + C zum Kopieren und STRG + Q für die Anforderung.

Inkonsistente Bedeutungen für bekannte Tastenkombinationen sind frustrierend und verursachen Fehler.

**Falsch:**

![Screenshot der Schaltfläche "Vorwärts" mit unterstrichen "w" ](images/inter-keyboard-image11.png)

In diesem Beispiel ist STRG + F die Standard Verknüpfung für Find, sodass die Zuweisung zu weiterleiten frustrierend und fehleranfällig ist. STRG + W wäre eine bessere Wahl.

Und schließlich sind **anwendungsspezifische Tastenkombinationen nur für Programme und Features sinnvoll, die häufig genug ausgeführt werden, damit sich motivierte Benutzer merken können.** Nicht häufig verwendete Programme und Funktionen benötigen keine Tastenkombinationen. Beispielsweise benötigen Setup Programme und die meisten Assistenten keine speziellen Tastenkombinationen und auch nicht häufig verwendete Befehle in einer Produktivitäts Anwendung.

### <a name="assigning-access-keys-in-dialog-boxes"></a>Zuweisen von Zugriffs Schlüsseln in Dialogfeldern

Weisen Sie allen interaktiven Steuerelementen, sofern möglich, eindeutige Zugriffsschlüssel zu, mit Ausnahme derjenigen, denen normalerweise keine Zugriffsschlüssel zugewiesen werden. In englischer Sprache sind jedoch nur 26 Zeichen vorhanden. Einige Zeichen werden möglicherweise nicht in einer der Bezeichnungen angezeigt, und in allen Bezeichnungen sind möglicherweise nicht unterschiedliche Zeichen vorhanden, wodurch diese Zahl weiter reduziert wird. Außerdem sollten Sie ein paar nicht zugewiesene Zeichen planen, um die Lokalisierung zu vereinfachen. Folglich können Sie nur ungefähr 20 eindeutige Zugriffsschlüssel in einem einzelnen Dialogfeld zuweisen.

Wenn Sie über ein Dialogfeld mit mehr als 20 interaktiven Steuerelementen verfügen, weisen Sie einigen Steuerelementen entweder keine Zugriffstasten zu, oder weisen Sie in seltenen Fällen doppelte Zugriffsschlüssel zu.

![Screenshot der Schriftart (Dialogfeld) ](images/inter-keyboard-image12.png)

Wenn diese zahlreichen interaktiven Steuerelemente vorhanden sind, benötigen Sie keinen Zugriffsschlüssel.

Verwenden Sie das folgende allgemeine Verfahren, um Zugriffsschlüssel zuzuweisen:

-   Weisen Sie zuerst den [Commit-Schalt](glossary.md) Flächen und den Befehls Verknüpfungen Zugriffstasten zu. Verwenden Sie die Standard Zuweisungs Tabelle für Zugriffsschlüssel, wenn diese angewendet wird, und verwenden Sie andernfalls den ersten Buchstaben des ersten Worts.
-   Überspringen Sie die Steuerelemente, denen keine Zugriffsschlüssel zugewiesen werden.
-   Weisen Sie den verbleibenden Steuerelementen eindeutige Zugriffsschlüssel zu (beginnend mit dem am häufigsten verwendeten):
    -   Wenn möglich, weisen Sie den Zugriffsschlüssel entsprechend der Standard Zugriffsschlüssel-Zuweisungs Tabelle zu.
    -   Andernfalls:
        -   Bevorzugen Sie Zeichen, die früh in der Bezeichnung vorkommen, idealerweise das erste Zeichen des ersten oder zweiten Worts.
        -   Bevorzugen Sie einen unverwechselbaren Konsonanten oder einen vowel, z. b. "x" in "Exit".
        -   Zeichen mit breiter Breite, als w-, m-und Großbuchstaben bevorzugen.
        -   Vermeiden Sie die Verwendung von Zeichen, die die Unterstreichung schwer zu erkennen machen, z. b. Buchstaben mit einer Pixel Breite, Buchstaben mit untergeordneten Zeichen und Buchstaben neben einem Buchstaben mit einem descender.
-   Wenn nicht alle Steuerelemente über eindeutige Zugriffsschlüssel verfügen (beginnen Sie mit dem am häufigsten verwendeten):
    -   Wenn Gruppen verwandter Steuerelemente vorhanden sind, z. b.:
        -   Eine einzelne Gruppe von Options Feldern
        -   Eine Reihe verwandter Kontrollkästchen
        -   Ein Satz verwandter Steuerelemente in einem Gruppenfeld.

Zuweisen von Zugriffs Schlüsseln zu Gruppen Bezeichnungen anstelle der einzelnen Steuerelemente. Normalerweise würden Sie das Gegenteil tun. (Stellen Sie dabei sicher, dass für diese Steuerelemente eine Steuerelement Gruppe definiert ist.)

-   Wenn noch nicht alle Steuerelemente über eindeutige Zugriffsschlüssel verfügen:
    -   Sie können nicht eindeutige Zugriffsschlüssel zuweisen, wenn Folgendes der folgenden ist:
        -   Andernfalls wäre es zu schwierig, zu den Steuerelementen zu navigieren.
        -   Die nicht eindeutigen Zugriffsschlüssel stehen nicht in Konflikt mit den Zugriffs Schlüsseln häufig verwendeter Steuerelemente.
    -   Andernfalls können Sie mithilfe der Tabulator-und Pfeiltasten Navigation auf die restlichen Steuerelemente zugreifen.

![Screenshot von Gruppen mit unterschiedlichen Zugriffs Schlüsseln ](images/inter-keyboard-image13.png)

In diesem Beispiel gibt es wiederkehrende Steuerelemente, sodass den Optionsfeld Gruppen Zugriffsschlüssel zugewiesen werden.

### <a name="preventing-accidental-commands"></a>Verhindern zufälliger Befehle

Wenn ein Fenster, das außerhalb des Kontexts angezeigt wird (nicht vom Benutzer initiiert), den Eingabefokus stiehlt, besteht die Möglichkeit, dass dieses Fenster Eingaben empfängt, die für ein anderes Fenster vorgesehen sind. Außerdem treten Zugriffsschlüssel beim Drücken der Alt-Taste in Kraft, wenn das Dialogfeld keine Steuerelemente enthält, die Texteingaben (z. b. Textfelder und Listen) annehmen. Im folgenden Beispiel wird durch Drücken von "r" die Schaltfläche jetzt neu starten aktiviert.

Eine solche Eingabe kann erhebliche unbeabsichtigte Folgen haben.

**Falsch:**

![Screenshot der Schaltfläche "jetzt neu starten", "r" unterstrichen ](images/inter-keyboard-image14.png)

Wenn Sie in diesem Beispiel Text mit "Space", "r" oder "Enter" eingeben, werden die Fenster versehentlich neu gestartet.

Natürlich besteht die beste Lösung für dieses Problem darin, den Eingabefokus nicht zu stehlen. Verwenden Sie stattdessen entweder die Task leisten [Schaltfläche](winenv-taskbar.md) des Programms, oder zeigen Sie eine Benachrichtigung an, um die Aufmerksamkeit des Benutzers zu erhalten.

Wenn Sie ein solches Fenster anzeigen müssen, empfiehlt es sich jedoch, keine Standard Schaltflächen oder Zugriffstasten zuzuweisen und den ersten Eingabefokus einem anderen Steuerelement als einer Commit-Schaltfläche zu geben.

**Richtig:**

![Screenshot der Schaltfläche "neu starten", "r" nicht unterstrichen ](images/inter-keyboard-image15.png)

In diesem Beispiel ist das versehentliche Neustarten von Fenstern weitaus schwieriger.

**Wenn Sie nur sechs Dinge tun...**

1.  Entwerfen Sie eine gute Tastaturnavigation mit einer sinnvollen Aktivier Reihenfolge und entsprechenden Steuerelement Gruppen, dem ersten Eingabefokus und Standard Schaltflächen.
2.  Zuweisen von Zugriffs Schlüsseln zu allen Menüs und den meisten Steuerelementen.
3.  Weisen Sie die Zugriffstasten einem Zeichen zu, das früh in der Bezeichnung angezeigt wird, damit Sie leicht zu finden sind.
4.  Weisen Sie den am häufigsten verwendeten Befehlen Tastenkombinationen zu.
5.  Versuchen Sie, die Tastenkombinationen den ersten oder am meisten einprägsamen Zeichen innerhalb von Schlüsselwörtern zuzuweisen.
6.  Gibt eine konsistente Bedeutung von bekannten Tastenkombinationen.

## <a name="guidelines"></a>Richtlinien

### <a name="interaction"></a>Interaktion

-   **Verwenden Sie die UMSCHALTTASTE nicht, um Befehle in Menüs oder Dialogfeldern zu ändern.** Dies ist nicht auffundbar und unerwartet.

    **Falsch:**

    ![Screenshot des Dialog Felds "Ordner Ersetzung bestätigen" ](images/inter-keyboard-image16.png)

    In diesem Beispiel aus Windows XP ersetzt das halten der Umschalttaste ja zu all.

-   **Deaktivieren Sie ein Steuerelement mit dem Eingabefokus nicht. Dadurch kann verhindert werden, dass das Fenster Tastatureingaben empfängt.** Verschieben Sie stattdessen vor dem Deaktivieren eines Steuer Elements mit dem Eingabefokus den Eingabefokus auf ein anderes Steuerelement.
-   **Wenn ein Fenster außerhalb des Kontexts angezeigt wird, möglicherweise überraschende Benutzer, müssen Sie möglicherweise bedeutende unbeabsichtigte Folgen verhindern:**
    -   Weisen Sie keine Standard Schaltfläche zu.
    -   Weisen Sie keine Zugriffsschlüssel zu.
    -   Legen Sie den ersten Eingabefokus auf ein anderes Steuerelement als auf eine Commit-Schaltfläche.

### <a name="keyboard-navigation"></a>Tastaturnavigation

-   **Zeigt den Eingabefokus Indikator immer an. Ausnahme:** Sie können den Eingabefokus Indikator in folgenden Punkten vorübergehend unterdrücken:
    -   Der Eingabefokus Indikator ist visuell ablenkend (wie bei einer großen Listenansicht nicht in der Detailansicht).
    -   Bei der Verwendung der EINGABETASTE werden wahrscheinlich andere Tastatureingaben vorangestellt, z. b. alt oder Pfeiltasten.
    -   Der Eingabefokus Indikator wird bei jeder Tastatureingabe angezeigt.
-   **Weisen Sie dem Steuerelement den anfänglichen Eingabefokus zu, bei** dem es sich meist um das erste interaktive Steuerelement handelt. Wenn das erste interaktive Steuerelement keine gute Wahl ist, sollten Sie das Layout des Fensters ändern.
-   **Das Zuweisen von Registerkarten wird allen interaktiven Steuerelementen, einschließlich Schreib geschützter Bearbeitungsfelder, angehalten. Ausnahmen**
    -   Gruppen von verknüpften Steuerelementen, die sich als ein einzelnes Steuerelement Verhalten, z. b. Options Felder. Diese Gruppen verfügen über einen einzelnen Tabstopp.
    -   Enthält ordnungsgemäß Gruppen, sodass die Pfeiltasten in der Gruppe vorwärts und rückwärts und in der Gruppe bleiben.
-   **Die Aktivier Reihenfolge sollte der Lesefolge folgen, die im Allgemeinen von links nach rechts und von oben nach unten verläuft.** Sie sollten Ausnahmen für häufig verwendete Steuerelemente erstellen, indem Sie Sie zuvor in der Aktivier Reihenfolge platzieren. Die Registerkarte sollte alle Tabstopps in beide Richtungen durchlaufen, ohne zu beenden.
-   **Innerhalb einer Tabstopp Taste sollte die Reihenfolge der Pfeiltasten von links nach rechts, von oben nach unten und** ohne Ausnahmen abgeleitet werden. Die Pfeiltasten sollten alle Elemente in beiden Richtungen durchlaufen, ohne zu beenden.
-   **Stellen Sie die Commit-Schaltflächen in der folgenden Reihenfolge bereit:**
    -   OK/ \[ do \] /Yes
    -   \[Nicht \] /No
    -   Abbrechen
    -   Anwenden (falls vorhanden)

dabei \[ handelt es sich nicht \] \[ \] um spezielle Antworten auf die main-Anweisung.

-   **Wählen Sie das sicherste (um den Verlust von Daten oder den System Zugriff zu verhindern) und die sicherste Befehls Schaltfläche oder Befehls Verknüpfung als Standard aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequeme Antwort aus.
-   **Bei der Tastaturnavigation sollten keine Steuerelement Werte geändert werden, oder es wird keine Fehlermeldung angezeigt** Benutzer müssen den Anfangswert eines Steuer Elements während der Navigation nie ändern. Initialisieren Sie stattdessen Steuerelemente, die beim Beenden mit gültigen Werten validieren, und überprüfen Sie den Wert eines Steuer Elements nur, wenn es geändert wurde.

### <a name="access-keys"></a>Zugriffsschlüssel

-   **Weisen Sie, wenn möglich, Zugriffsschlüssel für häufig verwendete Befehle entsprechend der folgenden Tabelle zu.** Obwohl konsistente Zugriffsschlüssel Zuweisungen nicht immer möglich sind, werden Sie sicherlich besonders für häufig verwendete Befehle bevorzugt.

    |                           |                                           |
    |---------------------------|-------------------------------------------|
    | **Zugriffsschüssel**<br/> | **Befehl**<br/>                    |
    | A<br/>              | Info<br/>                          |
    | A<br/>              | Immer im Vordergrund<br/>                  |
    | A<br/>              | Anwenden<br/>                          |
    | B<br/>              | Zurück<br/>                           |
    | B<br/>              | Fett<br/>                           |
    | B oder r<br/>         | Durchsuchen<br/>                         |
    | C<br/>              | Schließen<br/>                          |
    | C<br/>              | Kopieren<br/>                           |
    | C<br/>              | Hier kopieren<br/>                      |
    | s<br/>              | Verknüpfung erstellen<br/>                |
    | s<br/>              | Verknüpfung hier erstellen<br/>           |
    | t<br/>              | Ausschneiden<br/>                            |
    | D<br/>              | Löschen<br/>                         |
    | D<br/>              | Dieses Element nicht \[ \] mehr anzeigen<br/> |
    | E<br/>              | Bearbeiten<br/>                           |
    | x<br/>              | Beenden<br/>                           |
    | E<br/>              | Erkunden<br/>                        |
    | F<br/>              | Weniger<br/>                          |
    | F<br/>              | File<br/>                           |
    | F<br/>              | Suchen<br/>                           |
    | n<br/>              | Weitersuchen<br/>                      |
    | F<br/>              | Schriftart<br/>                           |
    | F<br/>              | Weiter<br/>                        |
    | H<br/>              | Hilfe<br/>                           |
    | t<br/>              | Hilfethemen<br/>                    |
    | H<br/>              | Ausblenden<br/>                           |
    | I<br/>              | Einfügen<br/>                         |
    | o<br/>              | Einfügen eines Objekts<br/>                  |
    | I<br/>              | Kursiv<br/>                         |
    | L<br/>              | Link hier<br/>                      |
    | x<br/>              | Maximieren<br/>                       |
    | n<br/>              | Minimieren<br/>                       |
    | M<br/>              | Mehr<br/>                           |
    | M<br/>              | Move<br/>                           |
    | M<br/>              | Hierher ziehen<br/>                      |
    | N<br/>              | Neu<br/>                            |
    | N<br/>              | Nächste<br/>                           |
    | N<br/>              | Nein<br/>                             |
    | O<br/>              | Öffnen<br/>                           |
    | w<br/>              | Öffnen mit<br/>                      |
    | O<br/>              | Optionen<br/>                        |
    | u<br/>              | Seiteneinrichtung<br/>                     |
    | P<br/>              | Einfügen<br/>                          |
    | l<br/>              | Link einfügen<br/>                     |
    | s<br/>              | Verknüpfung einfügen<br/>                 |
    | s<br/>              | Sonderzeichen einfügen<br/>                  |
    | P<br/>              | Anhalten<br/>                          |
    | P<br/>              | Abspielen<br/>                           |
    | P<br/>              | Drucken<br/>                          |
    | P<br/>              | Hier drucken<br/>                     |
    | r<br/>              | Eigenschaften<br/>                     |
    | R<br/>              | Wiederholen<br/>                           |
    | R<br/>              | Repeat<br/>                         |
    | R<br/>              | Restore<br/>                        |
    | R<br/>              | Fortsetzen<br/>                         |
    | R<br/>              | Erneut versuchen<br/>                          |
    | R<br/>              | Ausführen<br/>                            |
    | E<br/>              | Speichern<br/>                           |
    | a<br/>              | Speichern unter<br/>                        |
    | a<br/>              | Alles auswählen<br/>                     |
    | n<br/>              | Senden an<br/>                        |
    | E<br/>              | Anzeigen<br/>                           |
    | E<br/>              | Size<br/>                           |
    | p<br/>              | Split<br/>                          |
    | E<br/>              | Stop<br/>                           |
    | T<br/>              | Tools<br/>                          |
    | U<br/>              | Underline<br/>                      |
    | U<br/>              | Rückgängig<br/>                           |
    | V<br/>              | Sicht<br/>                           |
    | W<br/>              | Fenster<br/>                         |
    | J<br/>              | Ja<br/>                            |

    

     

-   **Zeichen mit breiter Breite** (z. b. w, m und Großbuchstaben) bevorzugen.
-   **Bevorzugen Sie einen unverwechselbaren Konsonanten oder einen vowel,** z. b. "x" in "Exit".
-   **Vermeiden Sie die Verwendung von Zeichen, die die Unterstreichung schwer zu erkennen machen,** wie z. b. (vom problematischsten bis zum geringsten problematischen)
    -   Zeichen, die nur ein Pixel breit sind, z. b. i und l.
    -   Zeichen mit untergeordneten Zeichen, wie z. b. g, j, p, q und y.
    -   Zeichen neben einem Buchstaben mit einem descender.
-   Denken Sie beim Zuweisen von Zugriffs Schlüsseln auf Assistenten Seiten daran, "B" für "Back" und "N" für "Next" zu reservieren.
-   Beachten Sie beim Zuweisen von Zugriffs Schlüsseln in den Eigenschaften Seiten, dass Sie "A" für Apply, falls verwendet, reservieren.

### <a name="menu-access-keys"></a>Menü Zugriffstasten

-   **Weisen Sie allen Menü Elementen Zugriffstasten zu.** Keine Ausnahmen.
-   **Für dynamische Menü Elemente (z. b. zuletzt verwendete Dateien) weisen Sie Zugriffsschlüssel numerisch zu.**

    ![Screenshot von Menü Elementen mit numerischen Zugriffs Schlüsseln ](images/inter-keyboard-image17.png)

    In diesem Beispiel weist das Paint-Programm in Windows den kürzlich verwendeten Dateien numerische Zugriffstasten zu.

-   **Zuweisen von eindeutigen Zugriffs Schlüsseln innerhalb einer Menü Ebene.** Sie können Zugriffsschlüssel über verschiedene Menüebenen hinweg wieder verwenden.
-   **Machen Sie Zugriffsschlüssel leicht zu finden:**
    -   Wählen Sie für die am häufigsten verwendeten Menü Elemente die Zeichen am Anfang des ersten oder zweiten Worts der Bezeichnung aus, vorzugsweise das erste Zeichen.
    -   Wählen Sie für weniger häufig verwendete Menü Elemente Buchstaben aus, die eine unterschiedliche konsonante oder einen Vokal in der Bezeichnung darstellen.

### <a name="dialog-box-access-keys"></a>Zugriffsschlüssel für das Dialog Feld

-   **Weisen Sie allen interaktiven Steuerelementen oder deren Bezeichnungen nach Möglichkeit eindeutige Zugriffstasten zu.** Schreibgeschützte [Textfelder](ctrl-text-boxes.md) sind interaktive Steuerelemente (da Benutzer einen Bildlauf durchführen und Text kopieren können), sodass Sie von Zugriffs Schlüsseln profitieren. **Weisen Sie keinen Zugriffsschlüssel zu:**
    -   **Schaltflächen OK, Abbrechen und schließen.** Enter und ESC werden für Ihre Zugriffsschlüssel verwendet. Weisen Sie jedoch immer einen Zugriffsschlüssel einem Steuerelement zu, das "OK" oder "Abbrechen" bedeutet, aber eine andere Bezeichnung hat.

        ![Screenshot des Dialog Felds mit den Schaltflächen "Ja" und "Nein" ](images/inter-keyboard-image18.png)

        In diesem Beispiel ist der Schaltfläche positiver Commit eine Zugriffstaste zugewiesen.

    -   **Gruppen Bezeichnungen.** Normalerweise werden den einzelnen Steuerelementen innerhalb einer Gruppe Zugriffsschlüssel zugewiesen, sodass die Gruppen Bezeichnung keines benötigt. Weisen Sie der Gruppen Bezeichnung jedoch einen Zugriffsschlüssel zu, nicht die einzelnen Steuerelemente, wenn ein Mangel an Zugriffs Schlüsseln vorliegt.
    -   **Allgemeine Hilfe** Schaltflächen, auf die mit F1 zugegriffen wird.
    -   **Link Bezeichnungen.** Es gibt oft zu viele Verknüpfungen, um eindeutige Zugriffsschlüssel zuzuweisen, und Link-Unterstriche blenden die Zugriffsschlüssel Unterstriche aus. Lassen Sie die Benutzer stattdessen auf Verknüpfungen mit der Tab-Taste zugreifen.
    -   **Registerkarten Namen.** Registerkarten werden mithilfe von STRG + TAB und STRG + UMSCHALT + TAB mithilfe von STRG + UMSCHALTTASTE gedrückt.
    -   **Durchsuchen von Schaltflächen mit der Bezeichnung "...".** Diese können nicht eindeutig Zugriffs Schlüsseln zugewiesen werden.
    -   **Nicht beschriftete Steuerelemente,** wie z. b. Dreh Steuerelemente, grafische Befehls Schaltflächen und unbezeichnete Steuerelemente für progressives
    -   **Statischer Text oder Bezeichnungen ohne Bezeichnung für Steuerelemente, die nicht interaktiv sind,** z. b. Status leisten.

-   **Weisen Sie zuerst Zugriffsschlüssel für die Zugriffstaste zu, um sicherzustellen, dass Sie über die Standardschlüssel Zuweisungen verfügen** Wenn keine Standardschlüssel Zuweisung vorhanden ist, verwenden Sie den ersten Buchstaben des ersten Worts. Beispielsweise sollten die Schaltflächen Zugriffsschlüssel für Ja und kein Commit immer "Y" und "N" sein, unabhängig von den anderen Steuerelementen im Dialogfeld.
-   **Für negative Commit-Schaltflächen (außer Abbrechen), die als "nicht" formuliert sind, weisen Sie den Zugriffsschlüssel "n" in "nicht" zu.** Wenn Sie nicht als "nicht" formuliert ist, verwenden Sie die standardmäßige Zugriffsschlüssel Zuweisung, oder weisen Sie den ersten Buchstaben des ersten Worts zu. Dadurch haben alle "TS" und "No" eine konsistente Zugriffstaste.
-   Damit **Zugriffsschlüssel leicht zu finden sind, weisen Sie die Tastenkombinationen einem Zeichen zu, das früh in der Bezeichnung angezeigt wird,** idealerweise das erste Zeichen, auch wenn es ein Schlüsselwort gibt, das später in der Bezeichnung angezeigt wird.
-   **Weisen Sie höchstens 20 Zugriffsschlüssel zu,** sodass Sie einige nicht zugewiesene Zeichen haben, um die Lokalisierung zu vereinfachen.
-   **Wenn zu viele interaktive Steuerelemente vorhanden sind, um eindeutige Zugriffsschlüssel zuzuweisen, können Sie nicht eindeutige Zugriffsschlüssel zuweisen,** wenn Folgendes der Fall ist:
    -   Andernfalls wäre es zu schwierig, zu den Steuerelementen zu navigieren.
    -   Die nicht eindeutigen Zugriffsschlüssel stehen nicht in Konflikt mit den Zugriffs Schlüsseln häufig verwendeter Steuerelemente.
-   **Verwenden Sie keine Menüleisten in Dialogfeldern.** In diesem Fall ist es schwierig, eindeutige Zugriffstasten zuzuweisen, da die Dialogfeld Steuerelemente und Menü Elemente dieselben Zeichen aufweisen.

### <a name="shortcut-keys"></a>Tastenkombinationen

-   **Weisen Sie den am häufigsten verwendeten Befehlen Tastenkombinationen zu.** Nicht häufig verwendete Programme und Funktionen benötigen keine Tastenkombinationen, da Benutzer stattdessen Zugriffstasten verwenden können.
-   **Stellen Sie keine Tastenkombination als einzige Möglichkeit zum Ausführen einer Aufgabe dar.** Benutzer sollten auch die Maus oder die Tastatur mit Tab, Pfeil und Zugriffstasten verwenden können.
-   **Weisen Sie bekannten Tastenkombinationen keine unterschiedlichen Bedeutungen zu.** Da Sie gespeichert werden, sind nicht konsistente Bedeutungen für bekannte Verknüpfungen frustrierend und fehleranfällig.
-   **Versuchen Sie nicht, systemweite Programm-Tastenkombinationen zuzuweisen.** Die Tastenkombinationen des Programms werden nur wirksam, wenn das Programm den Eingabefokus besitzt.
-   **Dokumentieren Sie alle Tastenkombinationen.** Dokument Verknüpfungen in Menüleisten Elementen, Symbolleisten-Quick Infos und einen einzelnen Hilfeartikel, in dem alle verwendeten Tastenkombinationen dokumentiert werden. Auf diese Weise können Benutzer die Tastenkombinationen erlernen, die nicht geheim sein sollten.

    -   **Ausnahme:** Zeigen Sie keine Tastenkombinationen für Tastenkombinationen innerhalb von Kontextmenüs an. Kontextmenüs zeigen die Tastenkombinationen nicht an, da diese Menüs auf Effizienz optimiert sind.

    ![Screenshot der QuickInfo für Fett formatierte Tastenkombination ](images/inter-keyboard-image19.png)

    Die Tastenkombination wird in der QuickInfo dokumentiert.

-   **Wenn das Programm viele Tastenkombinationen zuweist, können Sie die Zuweisungen anpassen.** Auf diese Weise können Benutzer widersprüchliche Tastenkombinationen neu zuweisen und von anderen Produkten migrieren. Die meisten Programme weisen nicht genügend Tastenkombinationen zu, um dieses Feature zu benötigen.

### <a name="choosing-shortcut-keys"></a>Auswählen von Tastenkombinationen

-   **Verwenden Sie die Standard Zuweisungen für bekannte Tastenkombinationen.**
-   **Verwenden Sie für nicht standardmäßige schlüsselzuweisungen die folgenden empfohlenen Tastenkombinationen für häufig verwendete Befehle.** Diese Tastenkombinationen werden empfohlen, da Sie nicht mit den bekannten Verknüpfungen in Konflikt stehen und leicht zu drücken sind.
    -   STRG + G, J, K, L M, Q, R oder T
    -   STRG + beliebig
    -   F7, F8, F9 oder F12
    -   UMSCHALT + F2, F3, F4, F5, F7, F8, F9, F11 oder F12
    -   Alt + beliebige Funktionstaste außer F4
-   **Verwenden Sie die folgenden empfohlenen Tastenkombinationen für weniger häufig verwendete Befehle.** Diese Tastenkombinationen haben keine Konflikte, aber es ist schwieriger, auf zwei Hände zu drücken.
    -   STRG + beliebige Funktionstaste außer F4 und F6
    -   STRG + UMSCHALT + beliebiger Buchstabe oder Zahl
-   **Häufig verwendete Tastenkombinationen leicht zu merken:**
    -   Verwenden Sie anstelle von Zahlen oder Funktions Schlüsseln Buchstaben.
    -   Versuchen Sie, einen Buchstaben zu verwenden, der in den Schlüsselwörtern des Befehls das erste Wort oder das am meisten einprägsame Zeichen ist.
-   **Verwenden Sie Funktionstasten für Befehle, die einen kleinen Effekt aufweisen,** wie z. b. Befehle, die für das ausgewählte Objekt gelten. Beispielsweise benennt F2 das ausgewählte Element um.
-   **Verwenden Sie STRG-Tastenkombinationen für Befehle, die einen umfangreichen Effekt aufweisen,** z. b. Befehle, die für ein gesamtes Dokument gelten. Beispielsweise speichert STRG + S das aktuelle Dokument.
-   **Verwenden Sie UMSCHALT Tastenkombinationen für Befehle, mit denen die Aktionen der Standard-Tastenkombination erweitert oder ergänzt werden.** Beispielsweise wird mit der Tastenkombination Alt + Tab die öffnenden primären Fenster durchlaufen, wohingegen Alt + Umschalt + Tab in umgekehrter Reihenfolge angezeigt wird. Ebenso zeigt F1 die Hilfe an, während UMSCHALT + F1 kontextabhängige Hilfe anzeigt.
-   **Wenn Sie die Pfeiltasten zum Verschieben oder Ändern der Größe eines Elements verwenden, verwenden Sie STRG + Pfeiltasten für eine präzisetere Steuerung.**

### <a name="choosing-shortcut-keys-what-not-to-do"></a>Auswählen von Tastenkombinationen (was nicht zu tun ist)

-   **Unterscheiden Sie sich nicht zwischen wichtigen Speicherorten.** Beispielsweise kann Windows zwischen der linken und der rechten Umschalttaste, der Alt-Taste, der STRG-Taste, dem [Windows-Logo](glossary.md)und den [Anwendungs Schlüsseln](glossary.md)sowie den Schlüsseln auf der numerischen Tastatur unterscheiden. Das Zuweisen von Verhalten zu nur einem zentralen Speicherort ist verwirrend und unerwartet.
-   **Verwenden Sie nicht die Windows-logomodifizierertaste für Programm Tastenkombinationen.** Windows-Logo-Taste ist für die Verwendung durch Windows reserviert. Auch wenn Windows-Taste für die Tastenkombination jetzt nicht von Windows verwendet wird, kann es in der Zukunft liegen.
-   **Verwenden Sie den Anwendungs Schlüssel nicht als schlüsselmodifizierer.** Verwenden Sie stattdessen STRG, alt und Shift.
-   **Verwenden Sie keine Tastenkombinationen, die von Windows für Programm-Tastenkombinationen verwendet werden.** Dies führt zu einem Konflikt mit den Tastenkombinationen des Windows-Systems, wenn Ihr Programm den Eingabefokus besitzt.
-   **Verwenden Sie keine alt + alphanumerischen Tastenkombinationen für Tastenkombinationen.** Solche Tastenkombinationen können mit Zugriffs Schlüsseln in Konflikt stehen.
-   **Verwenden Sie die folgenden Zeichen nicht für Tastenkombinationen:** @ $ {} \[ \] \\  ~  \| ^ '  < >. Diese Zeichen erfordern unterschiedliche Schlüssel Kombinationen in verschiedenen Sprachen oder sind Gebiets Schema spezifisch.
-   **Vermeiden Sie komplexe Tastenkombinationen,** z. b. drei oder mehr Schlüssel (Beispiel: STRG + ALT + LEERTASTE) oder Schlüssel, die sich auf der Tastatur weit voneinander unterscheiden (Beispiel: STRG + F5). Verwenden Sie einfache Tastenkombinationen für häufig verwendete Befehle.
-   **Verwenden Sie STRG + ALT-Kombinationen nicht,** da Windows diese Kombination in einigen Sprachversionen als AltGr-Schlüssel interpretiert, der alphanumerische Zeichen generiert.

### <a name="keyboard-and-mouse-combinations"></a>Kombinationen von Tastatur und Maus

-   Verwenden Sie für Verknüpfungen UMSCHALT + Klicken, um mithilfe eines neuen Fensters zu navigieren, und drücken Sie Strg + Klick, um mithilfe einer neuen Registerkarte zu navigieren. Diese Vorgehensweise ist mit Windows Internet Explorer konsistent.

## <a name="documentation"></a>Dokumentation

Wenn Sie auf die Tastatur verweisen:

-   Verwenden Sie die Bildschirmtastatur, um auf eine Tastatur Darstellung auf dem Bildschirm zu verweisen, die der Benutzer für Eingabezeichen berührt.
-   Mit der Modifizierertaste beginnende Tastaturkombinationen. Modifizierertasten in der folgenden Reihenfolge präsentieren: Windows-Logo,-Anwendung, STRG, alt, Umschalttaste. Wenn der Numpad-Modifizierer verwendet wird, fügen Sie diesen direkt vor dem Schlüssel ein, den er ändert.
-   Verwenden Sie nicht alle Großbuchstaben für Tastenkombinationen. Befolgen Sie stattdessen die Groß-/Kleinschreibung, die von Standard Tastaturen verwendet wird, oder Kleinbuchstaben, wenn der Schlüssel nicht auf der Tastatur gekennzeichnet ist.
    -   Verwenden Sie für alphabetische Schlüssel Kombinationen einen Großbuchstaben.
    -   Rechtschreibprüfung für Bild-auf, Bild-ab, druckbildschirm und Scrollsperre.
    -   Rechtschreibprüfung Pluszeichen, Minuszeichen, Bindestrich, Zeitraum und Komma.
    -   Verwenden Sie für Pfeiltasten den Pfeil nach links, den Pfeil nach rechts, den Pfeil nach oben und den Pfeil nach unten. Verwenden Sie keine Grafik Bezeichnungen für die Pfeiltasten.
    -   Verwenden Sie die Windows-Taste und den Anwendungs Schlüssel, um auf die mit Symbolen gekennzeichneten Schlüssel zu verweisen. Verwenden Sie für diese Schlüssel keine Grafik Bezeichnungen.

**Richtig:**

Leertaste, Tab, EINGABETASTE, Seite nach oben, STRG + ALT + ENTF, Alt + W, STRG + Pluszeichen

**Falsch:**

Leertaste, Tab, EINGABETASTE, PG nach oben, STRG + ALT + ENTF, alt + w, STRG + +

-   Geben Sie Tastenkombinationen mit einem Pluszeichen ohne Leerzeichen an.

**Richtig:**

STRG + A, UMSCHALT + F5

**Falsch:**

STRG + A, UMSCHALT + F5

-   Wenn Sie eine Tastenkombination mit Interpunktions Zeichen anzeigen möchten, bei denen die Umschalttaste (z. b. das Fragezeichen) verwendet werden soll, fügen Sie der Kombination Umschalttaste hinzu, und geben Sie den Namen oder das Symbol der verschobenen Taste Die Verwendung des Namens des nicht gestuften Schlüssels, z. b. 4 anstelle von $, könnte für Benutzer verwirrend sein oder sogar falsch sein. beispielsweise? und/Zeichen werden nicht immer auf jeder Tastatur verschoben.

**Richtig:**

STRG + UMSCHALT +?, STRG + UMSCHALT + \* , STRG + UMSCHALT + Komma

**Falsch:**

STRG + UMSCHALT +/, STRG +?, STRG + UMSCHALT + 8, STRG +\*

-   Verwenden Sie zum ersten Mal den Schlüssel und mit dem Schlüsselnamen, falls dies für die Übersichtlichkeit z. b. die F1-Taste erforderlich ist. Verweisen Sie auf alle nachfolgenden Verweise nur über den Namen des Schlüssels, und drücken Sie F1.
-   Informationen zu Zugriffs Schlüsseln und Tastenkombinationen finden Sie unter Programmieren und andere technische Dokumentationen. Verwenden Sie keine Accelerator-, mnetmonic-oder Hot-Taste. Überall sonst verwenden Sie die Tastenkombination, insbesondere in der Benutzerdokumentation.

Beim Verweisen auf die Interaktion:

-   Verwenden Sie Press, nicht DEPRESS, Strike, Hit oder Type, beim Drücken und sofortigen Freigeben eines Schlüssels wird eine Aktion innerhalb des Programms initiiert oder innerhalb eines Dokuments oder einer Benutzeroberfläche navigiert.
-   Verwenden Sie den Typ, nicht die EINGABETASTE, um die Benutzer zum Typtext zu leiten.
-   Verwenden Sie die Verwendung in Situationen, in denen das Drücken von drücken möglicherweise verwirrend ist, z. b. beim Verweis auf einen Schlüsseltyp wie die Pfeiltasten oder Funktionstasten. Drücken Sie in solchen Fällen möglicherweise, dass die Benutzer denken, dass Sie alle Schlüssel gleichzeitig drücken müssen.
-   Verwenden Sie Hold beim Drücken und halten einer Taste, z. b. einer Modifizierertaste.
-   Verwenden Sie zum Klicken nicht als Synonym drücken.

Beispiele:

-   Geben Sie Ihren Namen ein, und drücken Sie dann die EINGABETASTE.
-   Drücken Sie STRG + F, und geben Sie dann den Text ein, nach dem Sie suchen möchten.
-   Drücken Sie Y, um die Datei zu speichern.
-   Verwenden Sie die Pfeiltasten, um die Einfügemarke zu verschieben.

 

