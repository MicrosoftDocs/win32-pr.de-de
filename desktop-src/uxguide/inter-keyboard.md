---
title: Tastatur
description: Die Tastatur ist das primäre Eingabegerät, das für die Texteingabe in Microsoft Windows verwendet wird. Aus Barrierefreiheit und Effizienz können die meisten Aktionen auch über die Tastatur ausgeführt werden.
ms.assetid: 27185c98-1233-4e26-a156-0ff080fd4db3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c1554ca1a9769b562f154498cd0871bc1b813067
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524295"
---
# <a name="keyboard"></a>Tastatur

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere aktuelle [Entwurfsanleitung wider.](/windows/uwp/design/)

Die Tastatur ist das primäre Eingabegerät, das für die Texteingabe in Microsoft Windows verwendet wird. Aus Barrierefreiheit und Effizienz können die meisten Aktionen auch über die Tastatur ausgeführt werden.

Tastaturen können auch auf virtuelle Bildschirmtastaturen und Schreibpads verweisen, die von Computern ohne physische Tastatur verwendet werden, z. B. tabletbasierte Computer.

![Screenshot der Bildschirmtastatur ](images/inter-keyboard-image1.png)

Die Windows Tablet- und Touchtechnologie-Tastatur auf dem Bildschirm.

![Screenshot des Windows-Tablet-Schreibpads ](images/inter-keyboard-image2.png)

Das Windows-Tablet- und Touchtechnologie-Schreibpad.

Es gibt sechs grundlegende Schlüsseltypen:

-   Ein Zeichenschlüssel sendet ein Literalzeichen mit dem Eingabefokus an das Fenster.
-   Eine Modifizierertaste in Kombination mit einer anderen Taste ändert die Bedeutung der zugehörigen Taste, z. B. STRG, ALT, UMSCHALT UND DIE WINDOWS-TASTE.
-   Die Navigationsschlüssel sind die Richtungspfeile sowie Home, End, Page Up und Page Down.
-   Die Bearbeitungsschlüssel sind Insert, Backspace und Delete.
-   Die Funktionstasten sind F1 bis F12.
-   Systemtasten setzen das System in einen Modus oder führen eine Systemaufgabe aus, z. B. Druckbildschirm, Sperre für Schließleisten und Num-Sperre.

Zugriffsschlüssel sind Tasten oder Tastenkombinationen, die für die Barrierefreiheit verwendet werden, um mit allen Steuerelementen oder Menüelementen über die Tastatur zu interagieren. Tastenkombinationen sind Schlüssel oder Tastenkombinationen, die von erweiterten Benutzern verwendet werden, um häufig verwendete Befehle zur Effizienz auszuführen. Windows gibt Zugriffsschlüssel an, indem die Zuweisung des Zugriffsschlüssels unterstreicht wird.

![Screenshot von Zugriffsschlüsseln und Tastenkombinationen ](images/inter-keyboard-image3.png)

Dieses Beispiel zeigt sowohl Zugriffsschlüssel als auch Tastenkombinationen.

Um visuelle Unübersichtlichkeit zu vermeiden, blendet Windows standardmäßig Die Unterstreichungen der Zugriffsschlüssel aus und zeigt sie nur an, wenn die ALT-TASTE gedrückt wird. Um die Konsistenz mit Windows zu gewährleisten, werden die Bilder im UX-Leitfaden auch mit ausgeblendeten Zugriffsschlüsseln angezeigt, es sei denn, die Richtlinie umfasst Zugriffsschlüssel.

Um das Bewusstsein für die Zugriffsschlüsselzuweisungen in Ihrem Programm während des gesamten Entwicklungsprozesses zu verbessern, können Sie sie jederzeit anzeigen. Wechseln Systemsteuerung zum Center für erleicherte Bedienung, und klicken Sie auf **Einfachere Verwendung der Tastatur.** aktivieren Sie dann das **Kontrollkästchen Tastenkombinationen und Zugriffstasten** unterstrichen.

**Hinweis:** Richtlinien im Zusammenhang [mit der Barrierefreiheit](inter-accessibility.md) werden in einem separaten Artikel vorgestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="elements-of-keyboard-navigation"></a>Elemente der Tastaturnavigation

Benutzer interagieren mit einem Fenster über die Tastatur, indem sie zu Steuerelementen navigieren, Auswahl treffen und Befehle ausführen. Die folgenden Elemente arbeiten zusammen, um dies zu ermöglichen.

![Screenshot des Dialogfelds "Farben bearbeiten" ](images/inter-keyboard-image4.png)

Um die Elemente der Tastaturnavigation in der folgenden Liste zu veranschaulichen, verweisen wir auf dieses Dialogfeld.

-   **Eingabefokus.** Das Steuerelement mit dem Eingabefokus empfängt die meisten Tastatureingaben. Der Eingabefokus wird mit einem gepunkteten Rechteck angegeben, das als Fokusrechteck bezeichnet wird. Einige Tastatureingaben werden an Steuerelemente gesendet, die keinen Eingabefokus haben, wie später erläutert.

    ![Screenshot der ersten Zeile im Dialogfeld "Farben bearbeiten" ](images/inter-keyboard-image5.png)

    Das erste Standardfarben-Steuerelement hat den Eingabefokus, wie mit einem gepunkteten Rechteck angegeben.

-   **Tabulatortaste und Tabstopps.** Die TAB-TASTE ist der primäre Mechanismus für die Navigation innerhalb eines Fensters. Die TAB-TASTE besucht nur die Steuerelemente mit einem Tabstopp. Alle interaktiven Steuerelemente (die nicht in einer Gruppe enthalten sind) sollten über Tabstopps verfügen, nicht interaktive Steuerelemente, z. B. Beschriftungen, dagegen nicht.
-   **Tabulator reihenfolge.** Alle Steuerelemente mit Tabstopps werden in der Reihenfolge der Registerkarten besucht. Durch Drücken der TAB-TASTE wird der Eingabefokus in der Tabulator reihenfolge auf das nächste Steuerelement verschoben, während durch Drücken von UMSCHALT+TAB der Eingabefokus auf das vorherige Steuerelement verschoben wird.
-   **Steuerelementgruppen.** Ein Satz verwandter Steuerelemente kann zu einer Gruppe gemacht und einem einzelnen Registerkartenstopp zugewiesen werden. Steuerelementgruppen werden für Steuerelemente verwendet, die sich wie ein einzelnes Steuerelement verhalten, z. B. Optionsfelder. Sie können auch verwendet werden, wenn es zu viele Steuerelemente für eine effiziente Navigation mit der TAB-TASTE allein gibt.

    ![Screenshot von einfachen und benutzerdefinierten Farbgruppen ](images/inter-keyboard-image6.png)

    Grundfarben und benutzerdefinierte Farben sind Steuerelementgruppen, die diesem Dialogfeld fünf Registerkartenstopps geben. Es gibt so viele Steuerelemente, dass die Navigation ohne Verwendung von Steuerelementgruppen ineffizient wäre.

-   **Pfeiltasten.** Die Pfeiltasten verschieben den Eingabefokus zwischen den Steuerelementen innerhalb einer Gruppe. Wenn Sie die NACH-RECHTS-TASTE drücken, wird der Eingabefokus in der Tabulator reihenfolge auf das nächste Steuerelement bewegt, während das Drücken des Pfeils nach links den Eingabefokus auf das vorherige Steuerelement verschiebt. Home, End, Up und Down haben auch das erwartete Verhalten innerhalb einer Gruppe. Benutzer können nicht mithilfe von Pfeiltasten aus einer Steuerelementgruppe navigieren.
-   **Standardschaltflächen.** Fenster mit Befehlsschaltflächen und Befehlslinks verfügen über eine einzelne Standardschaltfläche, die durch einen hervorgehobenen Rahmen gekennzeichnet ist. Dies ist die Schaltfläche, auf die geklickt wird, wenn die EINGABETASTE gedrückt wird. Standardmäßig ist eine einzelne Standardbefehlsschaltfläche oder ein Befehlslink zugewiesen. Die Standardschaltfläche wird jedoch bewegt, wenn der Benutzer mit der Tabulatortaste zu einer anderen Befehlsschaltfläche oder einem anderen Befehlslink wechselt. Folglich ist jede Befehlsschaltfläche oder jeder Befehlslink mit eingabefokus auch immer die Standardschaltfläche.

    ![Screenshot der Schaltflächen "OK" und "Abbrechen" ](images/inter-keyboard-image7.png)

    Die Schaltfläche OK ist normalerweise die Standardschaltfläche, wie durch den hervorgehobenen Rahmen angegeben. Wenn der Benutzer jedoch mit der Tabulatortaste zur Schaltfläche Abbrechen gelangen würde, würde er zur Standardschaltfläche werden und mit der EINGABETASTE aktiviert werden.

-   **Die Tasten "SPACEBAR", "ENTER" und "ESC".** Die Leerzeichenleiste aktiviert das Steuerelement mit dem Eingabefokus, während die EINGABETASTE die Standardschaltfläche aktiviert. Durch Drücken der ESC-TASTE wird das Fenster abgebrochen oder geschlossen.
-   **Zugriffsschlüssel** Zugriffsschlüssel werden verwendet, um direkt mit Steuerelementen zu interagieren, anstatt mit der Tabulatortaste zu navigieren. Sie werden mit der ALT-TASTE kombiniert und mit einem unterstrichenen Buchstaben in ihrer Bezeichnung gekennzeichnet.
-   **Zugreifen auf Schlüsselbezeichnungen.** Während einige Steuerelemente eigene Bezeichnungen wie Befehlsschaltflächen, Kontrollkästchen und Optionsfelder enthalten, verfügen andere Steuerelemente über externe Bezeichnungen, z. B. Listenfelder und Strukturansichten. Bei externen Bezeichnungen wird der Zugriffsschlüssel der Bezeichnung zugewiesen und navigiert bei Aufruf zum nächsten Steuerelement in der Registerkarten reihenfolge. Schaltflächen mit den Bezeichnungen OK, Abbrechen und Schließen werden keine Zugriffsschlüssel zugewiesen, da sie mit EINGABETASTE und ESC aufgerufen werden.

    ![Screenshot von Bezeichnungen mit unterstrichenen Bezeichnungen "b" und "d" ](images/inter-keyboard-image8.png)

    Durch Drücken von ALT+B wird zur ausgewählten Grundfarbe navigiert. Wenn Sie ALT+D drücken, klicken Sie auf die Schaltfläche Benutzerdefinierte Farben definieren, die EINGABETASTE ruft die Schaltfläche OK auf, und ESC ruft Abbrechen auf.

-   **Verhalten des Zugriffsschlüssels.** Wenn ein Zugriffsschlüssel aufgerufen und eindeutig zugewiesen wird, wird auf das zugeordnete Steuerelement geklickt. Wenn die Zuweisung nicht eindeutig ist, erhält das zugeordnete Steuerelement den Eingabefokus. Wenn der Benutzer denselben Zugriffsschlüssel erneut ein gibt, erhält das nächste Steuerelement in der Registerkarten reihenfolge mit der gleichen Zuweisung den Eingabefokus.

Dieser Mechanismus ist zwar recht kompliziert, aber auch recht intuitiv. Benutzer wählen die meisten dieser Details sofort aus, obwohl nur wenige erklären können, wie sie genau funktionieren.

### <a name="keyboard-support-for-accessibility-and-advanced-users"></a>Tastaturunterstützung für Barrierefreiheit und fortgeschrittene Benutzer

**Unter Windows geht es beim Entwerfen für die Tastatur um die Bereitstellung von gut entworfener Tastaturnavigation, Zugriffstasten für Barrierefreiheit und Tastenkombinationen für fortgeschrittene Benutzer.**

Um sicherzustellen, dass die Funktionalität Ihres Programms für eine breite Palette von Benutzern leicht verfügbar ist, einschließlich der Benutzer mit Behinderungen und Beeinträchtigungen, muss auf alle Elemente der interaktiven Benutzeroberfläche (UI) über die Tastatur zugegriffen werden können. Im Allgemeinen bedeutet dies, dass auf die am häufigsten verwendeten Benutzeroberflächenelemente über eine einzelne Tastenkombination oder eine Tastenkombination zugegriffen werden kann, wohingegen weniger häufig verwendete Elemente möglicherweise eine zusätzliche Navigation durch Tabstopps oder Pfeiltasten erfordern. Für diese Benutzer ist Vollständigkeit wichtiger als Konsistenz.

Um sicherzustellen, dass die Funktionalität Ihres Programms für erfahrene Benutzer effizient ist, sollten häufig verwendete Benutzeroberflächenelemente auch Tastenkombinationen für den direkten Tastaturzugriff enthalten. Erfahrene Benutzer haben oftmals eine starke Vorliebe für die Verwendung der Tastatur, da tastaturbasierte Befehle viel schneller eingegeben werden können. Zudem ist es dafür nicht erforderlich, die Hände von der Tastatur wegzubewegen. Für diese Benutzer sind Effizienz und Konsistenz entscheidend. Die Vollständigkeit hingegen ist nur für am häufigsten verwendeten Befehle wichtig.

Beim Entwerfen des Tastaturzugriffs für diese beiden Gruppen gibt es kleine Unterschiede, weshalb Windows zwei unabhängige direkte Tastaturzugriffsmechanismen bietet. Indem Sie sowohl Zugriffs- als auch Tastenkombinationen effektiv verwenden, können Sie Ihren Programmen effizienten, konsistenten und umfassenden Tastaturzugriff bieten, der allen Vorteilen bietet.

### <a name="access-keys"></a>Zugriffsschlüssel

Zugriffstasten weisen die folgenden Merkmale auf:

-   Sie verwenden ALT und eine alphanumerische Taste.
-   Sie dienen in erster Linie der Barrierefreiheit.
-   Sie sind allen Menüs und den meisten Dialogfeldsteuerelementen zugewiesen.
-   Ihre Speicherung ist nicht vorgesehen, daher werden sie direkt in der UI dokumentiert, indem das entsprechende Steuerelement-Beschriftungszeichen unterstrichen wird.
-   Sie wirken sich nur auf das aktuelle Fenster aus und navigieren zum entsprechenden Menüelement oder Steuerelement.
-   Sie werden nicht konsistent zugewiesen, da dies nicht immer möglich ist. Zugriffstasten sollten jedoch für die am häufigsten verwendeten Befehle, insbesondere für Schaltflächen für den Commit, konsistent zugewiesen werden.
-   Sie sind lokalisiert.

**Da Zugriffsschlüssel nicht auswendig gelernt werden sollen, werden sie einem Zeichen zugewiesen, das sich früh in der Bezeichnung befindet, damit sie leicht zu finden sind,** auch wenn es ein Schlüsselwort gibt, das später in der Bezeichnung angezeigt wird.

**Richtig:**

![Screenshot des ersten Zeichens in der Bezeichnung unterstrichen ](images/inter-keyboard-image9.png)

**Falsch:**

![Screenshot des 21. Zeichens unterstrichen ](images/inter-keyboard-image10.png)

Im richtigen Beispiel wird der Zugriffsschlüssel einem Zeichen zugewiesen, das sich früh in der Bezeichnung befindet.

### <a name="shortcut-keys"></a>Tastenkombinationen

Im Gegensatz dazu weisen Tastenkombinationen die folgenden Merkmale auf:

-   Sie verwenden primär die STRG- und Funktionstastensequenzen (Windows-Systemtastenkombinationen verwenden ebenfalls ALT in Verbindung mit nicht alphanumerischen Tasten und der Windows-Logo-Taste).
-   Sie dienen in erster Linie erweiterten Benutzer hinsichtlich Effizienz.
-   Sie werden nur den am häufigsten verwendeten Befehlen zugewiesen.
-   Ihre Speicherung ist vorgesehen, und sie werden nur in Menüs, QuickInfos und in der Hilfe dokumentiert.
-   Sie wirken sich auf das gesamte Programm aus, sie haben jedoch keine Auswirkung, wenn sie nicht angewendet werden.
-   Sie müssen konsistent zugewiesen werden, da sie gespeichert und nicht direkt dokumentiert werden.
-   Sie sind nicht lokalisiert.

**Da Tastenkombinationen auswendig gelernt werden sollen, verwenden die am häufigsten verwendeten Tastenkombinationen idealerweise Buchstaben aus den ersten oder einprägsamsten Zeichen in den Schlüsselwörtern des Befehls,** z. B. STRG+C für Kopieren und STRG+Q für Anforderung.

Inkonsistente Bedeutungen für bekannte Tastenkombinationen sind frustrierend und verursachen Fehler.

**Falsch:**

![Screenshot der Vorwärtsschaltfläche mit unterstrichener "w" ](images/inter-keyboard-image11.png)

In diesem Beispiel ist STRG+F die Standardverknüpfung für Suchen, sodass die Zuweisung zu Vorwärts frustrierend und fehleranfällig ist. STRG+W wäre eine bessere, einprägsame Wahl.

Da sie sich merken sollen, sind **anwendungsspezifische Tastenkombinationen schließlich nur für Programme und Features sinnvoll, die häufig genug ausgeführt werden, damit sich bewegte Benutzer sich merken können.** Selten verwendete Programme und Features benötigen keine Tastenkombinationen. Beispielsweise benötigen Setupprogramme und die meisten Assistenten weder spezielle Tastenkombinationszuweisungen noch selten verwendete Befehle in einer Produktivitätsanwendung.

### <a name="assigning-access-keys-in-dialog-boxes"></a>Zuweisen von Zugriffsschlüsseln in Dialogfeldern

Weisen Sie nach Möglichkeit allen interaktiven Steuerelementen mit Ausnahme derjenigen, denen normalerweise keine Zugriffsschlüssel zugewiesen sind, eindeutige Zugriffsschlüssel zu. Im Englischen gibt es jedoch nur 26 Zeichen. Einige Zeichen werden möglicherweise nicht in einer der Bezeichnungen angezeigt, und es gibt möglicherweise nicht unterschiedliche Zeichen in allen Bezeichnungen, wodurch diese Zahl weiter reduziert wird. Außerdem sollten Sie einige nicht zugewiesene Zeichen verwenden, um die Lokalisierung zu vereinfachen. Folglich können Sie nur etwa 20 eindeutige Zugriffsschlüssel in einem einzelnen Dialogfeld zuweisen.

Wenn Sie über ein Dialogfeld mit mehr als 20 interaktiven Steuerelementen verfügen, weisen Sie einigen Steuerelementen entweder keine Zugriffsschlüssel zu, oder weisen Sie in seltenen Fällen doppelte Zugriffsschlüssel zu.

![Screenshot des Dialogfelds "Schriftart" ](images/inter-keyboard-image12.png)

Wenn es so viele interaktive Steuerelemente gibt, benötigen nicht alle einen zugewiesenen Zugriffsschlüssel.

Verwenden Sie das folgende allgemeine Verfahren, um Zugriffsschlüssel zuzuweisen:

-   Weisen Sie zunächst den [Commitschaltflächen und Befehlslinks](glossary.md) Zugriffsschlüssel zu. Verwenden Sie bei der Anwendung die Standardtabelle für Zugriffsschlüsselzuweisungen, andernfalls den ersten Buchstaben des ersten Worts.
-   Überspringen Sie die Steuerelemente, denen keine Zugriffsschlüssel zugewiesen sind.
-   Weisen Sie den verbleibenden Steuerelementen eindeutige Zugriffsschlüssel zu (beginnend mit den am häufigsten verwendeten):
    -   Weisen Sie den Zugriffsschlüssel nach Möglichkeit gemäß der Standardtabelle für Zuweisungen von Zugriffsschlüsseln zu.
    -   Andernfalls:
        -   Bevorzugen Sie Zeichen, die früh in der Bezeichnung angezeigt werden, idealerweise das erste Zeichen des ersten oder zweiten Worts.
        -   Bevorzugen Sie einen typischen Konsonanten oder einen Vokal, z. B. "x" in "Exit".
        -   Bevorzugen Sie Zeichen mit breiten Breiten wie w, m und Großbuchstaben.
        -   Vermeiden Sie die Verwendung von Zeichen, die die Unterstreichung schwierig zu erkennen machen, z. B. Buchstaben, die ein Pixel breit sind, Buchstaben mit Nachfolgern und Buchstaben neben einem Buchstaben mit einem Nachfolger.
-   Wenn nicht alle Steuerelemente eindeutige Zugriffsschlüssel aufweisen können (beginnen Sie mit der am wenigsten häufig verwendeten):
    -   Wenn Gruppen verwandter Steuerelemente vorhanden sind, z. B.:
        -   Eine einzelne Gruppe von Optionsfeldern
        -   Eine Reihe verwandter Kontrollkästchen
        -   Eine Gruppe verwandter Steuerelemente innerhalb eines Gruppenfelds

Zuweisen von Zugriffsschlüsseln zu Gruppenbezeichnungen anstelle der einzelnen Steuerelemente. Normalerweise würden Sie das Gegenteil tun. (Stellen Sie dabei sicher, dass für diese Steuerelemente eine Steuerelementgruppe definiert ist.)

-   Wenn noch nicht alle Steuerelemente eindeutige Zugriffsschlüssel haben können:
    -   Sie können nicht eindeutige Zugriffsschlüssel zuweisen, wenn:
        -   Andernfalls wäre die Navigation zu den Steuerelementen zu schwierig.
        -   Die nicht eindeutigen Zugriffsschlüssel verursachen keinen Konflikt mit den Zugriffsschlüsseln häufig verwendeter Steuerelemente.
    -   Andernfalls kann über die Navigation mit der TAB- und PFEILTASTE auf die verbleibenden Steuerelemente zugegriffen werden.

![Screenshot von Gruppen mit unterschiedlichen Zugriffsschlüsseln ](images/inter-keyboard-image13.png)

In diesem Beispiel gibt es wiederkehrende Steuerelemente, sodass den Optionsfeldgruppen Zugriffsschlüssel zugewiesen werden.

### <a name="preventing-accidental-commands"></a>Verhindern versehentlicher Befehle

Wenn ein außerhalb des Kontexts angezeigtes Fenster (nicht vom Benutzer initiiert) den Eingabefokus stiehlt, besteht die Wahrscheinlichkeit, dass dieses Fenster Eingaben empfängt, die für ein anderes Fenster vorgesehen sind. Darüber hinaus werden Zugriffsschlüssel wirksam, wenn sie gedrückt werden, ohne die ALT-TASTE zu drücken, wenn das Dialogfeld keine Steuerelemente enthält, die Texteingaben (z. B. Textfelder und Listen) annehmen. Im folgenden Beispiel aktiviert das Drücken von "r" die Schaltfläche Jetzt neu starten.

Natürlich kann eine solche Eingabe erhebliche unbeabsichtigte Folgen haben.

**Falsch:**

![Screenshot der Schaltfläche "Jetzt neu starten", "r" unterstrichen ](images/inter-keyboard-image14.png)

In diesem Beispiel wird Windows versehentlich neu gestartet, wenn Sie Text mit Leerzeichen, "r" oder EINGABETASTE eingeben.

Natürlich besteht die beste Lösung für dieses Problem nicht darin, den Eingabefokus zu stehlen. Blinken Sie stattdessen entweder die [Taskleistenschaltfläche](winenv-taskbar.md) des Programms, oder zeigen Sie eine Benachrichtigung an, um die Aufmerksamkeit des Benutzers zu erhalten.

Wenn Sie jedoch ein solches Fenster anzeigen müssen, besteht der beste Ansatz darin, keine Standardschaltfläche oder Zugriffsschlüssel zuzuweisen und einen anfänglichen Eingabefokus auf ein anderes Steuerelement als eine Commitschaltfläche zu legen.

**Richtig:**

![Screenshot der Schaltfläche "Neu starten", "r" nicht unterstrichen ](images/inter-keyboard-image15.png)

In diesem Beispiel ist es viel schwieriger, Windows versehentlich neu zu starten.

**Wenn Sie nur sechs Dinge tun...**

1.  Entwerfen Sie eine gute Tastaturnavigation mit einer sinnvollen Registerkartenreihenfolge und geeigneten Steuerelementgruppen, dem anfänglichen Eingabefokus und Standardschaltflächen.
2.  Weisen Sie allen Menüs und den meisten Steuerelementen Zugriffsschlüssel zu.
3.  Weisen Sie die Zugriffsschlüssel einem Zeichen zu, das früh in der Bezeichnung angezeigt wird, damit sie leicht zu finden sind.
4.  Weisen Sie den am häufigsten verwendeten Befehlen Tastenkombinationen zu.
5.  Versuchen Sie, die Tastenkombinationen den ersten oder einprägsamsten Zeichen innerhalb von Schlüsselwörtern zuzuweisen.
6.  Geben Sie bekannten Tastenkombinationen eine konsistente Bedeutung.

## <a name="guidelines"></a>Richtlinien

### <a name="interaction"></a>Interaktion

-   **Verwenden Sie die UMSCHALTTASTE nicht, um Befehle in Menüs oder Dialogfeldern zu ändern.** Dies ist nicht behebbar und unerwartet.

    **Falsch:**

    ![Screenshot des Dialogfelds "Ordner ersetzen bestätigen" ](images/inter-keyboard-image16.png)

    In diesem Beispiel von Windows XP ersetzt die Umschalttaste Ja in Alle durch Nein zu Alle.

-   **Deaktivieren Sie kein Steuerelement mit Eingabefokus. Dadurch kann verhindert werden, dass das Fenster Tastatureingaben empfängt.** Verschieben Sie stattdessen den Eingabefokus auf ein anderes Steuerelement, bevor Sie ein Steuerelement mit Eingabefokus deaktivieren.
-   **Wenn ein Fenster außerhalb des Kontexts angezeigt wird( möglicherweise überraschende Benutzer), müssen Sie möglicherweise erhebliche unbeabsichtigte Folgen verhindern:**
    -   Weisen Sie keine Standardschaltfläche zu.
    -   Weisen Sie keine Zugriffsschlüssel zu.
    -   Geben Sie einem Steuerelement, das keine Commitschaltfläche ist, den anfänglichen Eingabefokus.

### <a name="keyboard-navigation"></a>Tastaturnavigation

-   **Zeigen Sie immer den Eingabefokusindikator an. Ausnahme: Sie** können den Eingabefokusindikator vorübergehend unterdrücken, wenn:
    -   Der Eingabefokusindikator ist visuell ablenkend (wie bei einer großen Listenansicht, nicht in der Detailansicht).
    -   Der Verwendung der EINGABETASTE wird wahrscheinlich eine andere Tastatureingabe vorangehende, z. B. ALT- oder Pfeiltasten.
    -   Die Eingabefokusanzeige wird bei jeder Tastatureingabe angezeigt.
-   **Weisen Sie dem Steuerelement,** mit dem Benutzer höchstwahrscheinlich zuerst interagieren, den anfänglichen Eingabefokus zu. Dies ist häufig das erste interaktive Steuerelement. Wenn das erste interaktive Steuerelement keine gute Wahl ist, sollten Sie das Layout des Fensters ändern.
-   **Zuweisen von Registerkartenstopps zu allen interaktiven Steuerelementen, einschließlich schreibgeschützter Bearbeitungsfelder. Ausnahmen:**
    -   Gruppen von verwandten Steuerelementen, die sich wie ein einzelnes Steuerelement verhalten, z. B. Optionsfelder. Solche Gruppen verfügen über einen einzelnen Tabstopp.
    -   Sie müssen Gruppen ordnungsgemäß enthalten, damit die Pfeiltasten innerhalb der Gruppe vorwärts und rückwärts zyklen und innerhalb der Gruppe bleiben.
-   **Die Tabulator reihenfolge sollte der Lese reihenfolge folgen, die in der Regel von links nach rechts, von oben nach unten fließt.** Erwägen Sie, Ausnahmen für häufig verwendete Steuerelemente zu machen, indem Sie sie früher in der Reihenfolge der Registerkarten setzen. Die Registerkarte sollte alle Registerkartenstopps in beide Richtungen durchzyklen, ohne anzuhalten.
-   **Innerhalb eines Tabstopps sollte die Reihenfolge der Pfeiltasten** ohne Ausnahmen von links nach rechts, von oben nach unten fließen. Die Pfeiltasten sollten alle Elemente in beide Richtungen durchzyklen, ohne anzuhalten.
-   **Stellen Sie die Commitschaltflächen in der folgenden Reihenfolge vor:**
    -   OK/ \[ Do it \] /Yes
    -   \[Don't do it \] /No
    -   Abbrechen
    -   Übernehmen (falls vorhanden)

Dabei handelt es sich bei "Do it" und \[ \] \[ "Don't do" \] um spezifische Antworten auf die Main-Anweisung.

-   **Wählen Sie die sicherste (um Datenverlust oder Systemzugriff zu verhindern) und die sicherste Befehlsschaltfläche oder den sichersten Befehlslink als Standard aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequemste Antwort aus.
-   **Die Tastaturnavigation sollte die Steuerungswerte nicht ändern oder zu einer Fehlermeldung führen.** Erfordern Sie niemals, dass Benutzer den Anfangswert eines Steuerelements während der Navigation ändern. Initialisieren Sie stattdessen Steuerelemente, die beim Beenden mit gültigen Werten überprüfen, und überprüfen Sie den Wert eines Steuerelements nur, wenn er geändert wurde.

### <a name="access-keys"></a>Zugriffsschlüssel

-   **Weisen Sie nach Möglichkeit Zugriffsschlüssel für häufig verwendete Befehle gemäß der folgenden Tabelle zu.** Obwohl konsistente Zuweisungen von Zugriffsschlüsseln nicht immer möglich sind, werden sie insbesondere für häufig verwendete Befehle bevorzugt.

    |  Zugriffsschüssel         | Befehl                             |
    |---------------------------|-------------------------------------------|
    | Ein<br/>              | Info<br/>                          |
    | Ein<br/>              | Immer oben<br/>                  |
    | Ein<br/>              | Anwenden<br/>                          |
    | B<br/>              | Zurück<br/>                           |
    | B<br/>              | Fett<br/>                           |
    | B oder r<br/>         | Durchsuchen<br/>                         |
    | C<br/>              | Schließen<br/>                          |
    | C<br/>              | Kopieren<br/>                           |
    | C<br/>              | Hier kopieren<br/>                      |
    | s<br/>              | Verknüpfung erstellen<br/>                |
    | s<br/>              | Erstellen Sie hier eine Verknüpfung.<br/>           |
    | t<br/>              | Ausschneiden<br/>                            |
    | D<br/>              | Löschen<br/>                         |
    | D<br/>              | Dieses Element nicht mehr \[ \] anzeigen<br/> |
    | E<br/>              | Bearbeiten<br/>                           |
    | x<br/>              | Beenden<br/>                           |
    | E<br/>              | Erkunden<br/>                        |
    | F<br/>              | Weniger<br/>                          |
    | F<br/>              | Datei<br/>                           |
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
    | s<br/>              | Einfügen der Verknüpfung<br/>                 |
    | s<br/>              | Spezielles Einfügen<br/>                  |
    | P<br/>              | Anhalten<br/>                          |
    | P<br/>              | Abspielen<br/>                           |
    | P<br/>              | Drucken<br/>                          |
    | P<br/>              | Drucken Sie hier.<br/>                     |
    | r<br/>              | Eigenschaften<br/>                     |
    | R<br/>              | Wiederholen<br/>                           |
    | R<br/>              | Repeat<br/>                         |
    | R<br/>              | Restore<br/>                        |
    | R<br/>              | Fortsetzen<br/>                         |
    | R<br/>              | Erneut versuchen<br/>                          |
    | R<br/>              | Ausführen<br/>                            |
    | E<br/>              | Speichern<br/>                           |
    | a<br/>              | Speichern unter<br/>                        |
    | a<br/>              | Alle auswählen<br/>                     |
    | n<br/>              | Senden an<br/>                        |
    | E<br/>              | Anzeigen<br/>                           |
    | E<br/>              | Size<br/>                           |
    | p<br/>              | Split<br/>                          |
    | E<br/>              | Beenden<br/>                           |
    | T<br/>              | Tools<br/>                          |
    | U<br/>              | Underline<br/>                      |
    | U<br/>              | Rückgängig<br/>                           |
    | V<br/>              | Sicht<br/>                           |
    | W<br/>              | Fenster<br/>                         |
    | „Y“ zugeordnet ist<br/>              | Ja<br/>                            |

    

     

-   **Bevorzugen Sie Zeichen mit breiten Zeichen,** z. B. w, m und Großbuchstaben.
-   **Bevorzugen Sie einen konsonanten Konsonanten oder einen Vokal,** z. B. "x" in "Exit".
-   **Vermeiden Sie die Verwendung von Zeichen, die** die Unterstriche schwer zu erkennen machen, z. B. (von den problematischsten zu den am wenigsten problematischen):
    -   Zeichen, die nur ein Pixel breit sind, z. B. i und l.
    -   Zeichen mit absteigenden Zeichen, z. B. g, j, p, q und y.
    -   Zeichen neben einem Buchstaben mit einem absteigenden Zeichen.
-   Denken Sie beim Zuweisen von Zugriffsschlüsseln auf Assistentenseiten daran, "B" für "Zurück" und "N" für "Weiter" zu reservieren.
-   Denken Sie beim Zuweisen von Zugriffsschlüsseln auf Eigenschaftenseiten daran, bei Verwendung "A" für Anwenden zu reservieren.

### <a name="menu-access-keys"></a>Menüzugriffsschlüssel

-   **Weisen Sie allen Menüelementen Zugriffsschlüssel zu.** Keine Ausnahmen.
-   **Weisen Sie für dynamische Menüelemente (z. B. zuletzt verwendete Dateien) Zugriffsschlüssel numerisch zu.**

    ![Screenshot von Menüelementen mit numerischen Zugriffsschlüsseln ](images/inter-keyboard-image17.png)

    In diesem Beispiel weist das Paint-Programm in Windows zuletzt verwendeten Dateien numerische Zugriffsschlüssel zu.

-   **Weisen Sie eindeutige Zugriffsschlüssel innerhalb einer Menüebene zu.** Sie können Zugriffsschlüssel auf verschiedenen Menüebenen wiederverwenden.
-   **Einfaches Aufschlüsseln von Zugriffsschlüsseln:**
    -   Wählen Sie für die am häufigsten verwendeten Menüelemente Zeichen am Anfang des ersten oder zweiten Worts der Bezeichnung aus, vorzugsweise das erste Zeichen.
    -   Wählen Sie für weniger häufig verwendete Menüelemente Buchstaben aus, die in der Bezeichnung ein charakteristischer Konsonant oder Vokal sind.

### <a name="dialog-box-access-keys"></a>Zugriffsschlüssel für Dialogfelder

-   **Weisen Sie nach Möglichkeit allen interaktiven Steuerelementen** oder deren Bezeichnungen eindeutige Zugriffsschlüssel zu. [Schreibgeschützte Textfelder sind](ctrl-text-boxes.md) interaktive Steuerelemente (da Benutzer scrollen und Text kopieren können), sodass sie von Zugriffsschlüsseln profitieren. **Weisen Sie keine Zugriffsschlüssel zu:**
    -   **Schaltflächen OK, Abbrechen und Schließen.** Eingabe und ESC werden für ihre Zugriffsschlüssel verwendet. Weisen Sie einem Steuerelement jedoch immer einen Zugriffsschlüssel zu, der OK oder Abbrechen bedeutet, aber eine andere Bezeichnung hat.

        ![Screenshot des Dialogfelds mit Schaltflächen "Ja" und "Nein" ](images/inter-keyboard-image18.png)

        In diesem Beispiel ist der Schaltfläche für den positiven Commit ein Zugriffsschlüssel zugewiesen.

    -   **Gruppenbezeichnungen.** Normalerweise werden den einzelnen Steuerelementen innerhalb einer Gruppe Zugriffsschlüssel zugewiesen, sodass die Gruppenbezeichnung keinen benötigt. Weisen Sie der Gruppenbezeichnung jedoch einen Zugriffsschlüssel zu, nicht den einzelnen Steuerelementen, wenn es zu einem Mangel an Zugriffsschlüsseln kommt.
    -   **Generische Hilfeschaltflächen,** auf die mit F1 zugegriffen wird.
    -   **Linkbezeichnungen.** Es gibt häufig zu viele Links, um eindeutige Zugriffsschlüssel zu zuweisen, und Link unterstriche blenden die Unterstriche der Zugriffsschlüssel aus. Lassen Sie benutzer stattdessen mit der TAB-TASTE auf Links zugreifen.
    -   **Registerkartennamen.** Tabstopps werden mit STRG+TAB und STRG+UMSCHALT+TAB zyklen.
    -   **Schaltflächen mit der Bezeichnung "..." durchsuchen.** Diesen können keine Zugriffsschlüssel eindeutig zugewiesen werden.
    -   **Nicht bezeichnete Steuerelemente, z.** B. Drehsteuerelemente, grafische Befehlsschaltflächen und nicht bezeichnete Steuerelemente für die progressive Offenlegung.
    -   **Nicht beschriftete statischer Text** oder Bezeichnungen für Steuerelemente, die nicht interaktiv sind, z. B. Statusleisten.

-   **Weisen Sie zuerst Zugriffsschlüssel für commit-Schaltflächen zu, um sicherzustellen, dass sie über die Standardschlüsselzuweisungen verfügen.** Wenn es keine Standardschlüsselzuweisung gibt, verwenden Sie den ersten Buchstaben des ersten Worts. Beispielsweise sollte der Zugriffsschlüssel für die Schaltflächen Ja und Nein commit immer "Y" und "N" sein, unabhängig von den anderen Steuerelementen im Dialogfeld.
-   **Weisen Sie für negative Commitschaltflächen (mit Anderen als Abbrechen), die als "Don't" (Nicht) formuliert sind, den Zugriffsschlüssel dem "n" in "Don't" zu.** Wenn sie nicht als "Nicht" bezeichnet werden, verwenden Sie die Standardzugriffsschlüsselzuweisung, oder weisen Sie den ersten Buchstaben des ersten Worts zu. Auf diese Weise verfügen alle Don'ts und No es über einen konsistenten Zugriffsschlüssel.
-   **Um zugriffsschlüssel** leicht zu finden, weisen Sie die Zugriffsschlüssel einem Zeichen zu, das früh in der Bezeichnung angezeigt wird, idealerweise das erste Zeichen, auch wenn später in der Bezeichnung ein Schlüsselwort angezeigt wird.
-   **Weisen Sie mindestens 20 Zugriffsschlüssel zu,** sodass Sie über einige nicht zugewiesene Zeichen verfügen, um die Lokalisierung zu vereinfachen.
-   **Wenn es zu viele interaktive Steuerelemente gibt, um eindeutige** Zugriffsschlüssel zu zuweisen, können Sie nicht eindeutige Zugriffsschlüssel in den folgendem Fällen zuweisen:
    -   Andernfalls wäre es zu schwierig, zu den Steuerelementen zu navigieren.
    -   Die nicht eindeutigen Zugriffsschlüssel stehen nicht in Konflikt mit den Zugriffsschlüsseln häufig verwendeter Steuerelemente.
-   **Verwenden Sie keine Menüleisten in Dialogfeldern.** In diesem Fall ist es schwierig, eindeutige Zugriffsschlüssel zu zuweisen, da die Steuerelemente und Menüelemente des Dialogfelds dieselben Zeichen verwenden.

### <a name="shortcut-keys"></a>Tastenkombinationen

-   **Weisen Sie den am häufigsten verwendeten Befehlen Tastenkombinationen zu.** Selten verwendete Programme und Features benötigen keine Tastenkombinationen, da Benutzer stattdessen Zugriffsschlüssel verwenden können.
-   **Machen Sie keine Tastenkombination zur einzigen Möglichkeit, eine Aufgabe auszuführen.** Benutzer sollten auch in der Lage sein, die Maus oder die Tastatur mit TAB-TASTE, Pfeil und Zugriffstasten zu verwenden.
-   **Weisen Sie bekannten Tastenkombinationen keine anderen Bedeutungen zu.** Da sie auswendig sind, sind inkonsistente Bedeutungen für bekannte Verknüpfungen frustrierend und fehleranfällig.
-   **Versuchen Sie nicht, systemweite Programmtasten zu zuweisen.** Die Tastenkombinationen Ihres Programms haben nur dann Auswirkungen, wenn ihr Programm den Eingabefokus besitzt.
-   **Dokumentieren Sie alle Tastenkombinationen.** Dokumentverknüpfungen in Menüleistenelementen, QuickInfos für die Symbolleiste und ein einzelner Hilfeartikel, der alle verwendeten Tastenkombinationen dokumentiert. Auf diese Weise können Benutzer die Tastenkombinationszuweisungen erlernen, die sie nicht als Geheimnis verwenden sollten.

    -   **Ausnahme:** Tastenkombinationen werden nicht in Kontextmenüs angezeigt. Kontextmenüs zeigen die Tastenkombinationszuweisungen nicht an, da diese Menüs für Effizienz optimiert sind.

    ![Screenshot der QuickInfo für fett formatierten Tastenkombination ](images/inter-keyboard-image19.png)

    Die Tastenkombination ist in der QuickInfo dokumentiert.

-   **Wenn Ihr Programm viele Tastenkombinationen zu weist, können Sie die Zuweisungen anpassen.** Auf diese Weise können Benutzer in Konflikt stehende Tastenkombinationen neu zuweisen und von anderen Produkten migrieren. Die meisten Programme weisen nicht genügend Tastenkombinationen zu, um dieses Feature zu benötigen.

### <a name="choosing-shortcut-keys"></a>Auswählen von Tastenkombinationen

-   **Verwenden Sie für bekannte Tastenkombinationen die Standardzuweisungen.**
-   **Verwenden Sie für nicht standardmäßige Tastenzuweisungen die folgenden empfohlenen Tastenkombinationen für häufiger verwendete Befehle.** Diese Tastenkombinationen werden empfohlen, da sie nicht mit den bekannten Tastenkombinationen in Konflikt stehen und einfach zu drücken sind.
    -   STRG+G, J, K, L M, Q, R oder T
    -   STRG+beliebige Zahl
    -   F7, F8, F9 oder F12
    -   UMSCHALT+F2, F3, F4, F5, F7, F8, F9, F11 oder F12
    -   ALT+beliebiger Funktionsschlüssel außer F4
-   **Verwenden Sie die folgenden empfohlenen Tastenkombinationen für weniger häufig verwendete Befehle.** Diese Tastenkombinationen haben keine Konflikte, aber es ist schwieriger, häufig zwei Hände zu drücken.
    -   STRG+beliebige Funktionstaste außer F4 und F6
    -   STRG+UMSCHALT+beliebiger Buchstabe oder beliebige Zahl
-   **Machen Sie sich häufig verwendete Tastenkombinationen leicht zu merken:**
    -   Verwenden Sie Buchstaben anstelle von Zahlen oder Funktionsschlüsseln.
    -   Versuchen Sie, einen Buchstaben im ersten Wort oder einprägsamste Zeichen in den Schlüsselwörtern des Befehls zu verwenden.
-   **Verwenden Sie Funktionsschlüssel für Befehle, die eine geringe** Auswirkung haben, z. B. Befehle, die für das ausgewählte Objekt gelten. Beispielsweise benennt F2 das ausgewählte Element um.
-   **Verwenden Sie STRG-Tastenkombinationen für Befehle,** die einen großen Effekt haben, z. B. Befehle, die für ein gesamtes Dokument gelten. Strg+S speichert z. B. das aktuelle Dokument.
-   **Verwenden Sie UMSCHALT-Tastenkombinationen für Befehle, die die Aktionen der Standardtastenkombination erweitern oder ergänzen.** Die Tastenkombination ALT+TAB durchfing z. B. geöffnete primäre Fenster, während ALT+UMSCHALT+TAB in umgekehrter Reihenfolge zyklen. Auf ähnliche Weise zeigt F1 Hilfe an, während UMSCHALT+F1 kontextorientierte Hilfe anzeigt.
-   **Wenn Sie pfeiltasten verwenden, um ein Element zu verschieben oder seine Größe zu ändern, verwenden Sie STRG+Pfeiltasten, um eine präzisere Steuerung zu erhalten.**

### <a name="choosing-shortcut-keys-what-not-to-do"></a>Auswählen von Tastenkombinationen (was nicht zu tun ist)

-   **Unterscheiden Sie nicht zwischen schlüsseln Speicherorten.** Windows kann z. B. zwischen DER LINKEN UND DER RECHTEN [](glossary.md)UMSCHALTTASTE, ALT, STRG, [Windows-Logo](glossary.md)und Anwendungstasten sowie Tasten auf der numerischen Tastatur unterscheiden. Das Zuweisen von Verhalten nur zu einem Schlüsselspeicherort ist verwirrend und unerwartet.
-   **Verwenden Sie nicht die Windows-Logomodifizierertaste für Tastenkombinationen des Programms.** Die Windows-Logo-Taste ist für die Verwendung durch Windows reserviert. Auch wenn windows derzeit keine Kombination aus Windows-Logoschlüsseln verwendet, kann sie in der Zukunft sein.
-   **Verwenden Sie die Anwendungsschlüssel nicht als Tastenkombinationsmodifizierer.** Verwenden Sie stattdessen STRG, ALT und UMSCHALT.
-   **Verwenden Sie keine Tastenkombinationen, die von Windows für Tastenkombinationen für Programme verwendet werden.** Dies steht in Konflikt mit den Tastenkombinationen des Windows-Systems, wenn ihr Programm den Eingabefokus besitzt.
-   **Verwenden Sie keine Alt+alphanumerische Tastenkombinationen für Tastenkombinationen.** Solche Tastenkombinationen können mit Zugriffsschlüsseln in Konflikt stehen.
-   **Verwenden Sie nicht die folgenden Zeichen für Tastenkombinationen:** @ $ {} \[ \] \\  ~  \| ^ ' < >. Diese Zeichen erfordern unterschiedliche Tastenkombinationen in verschiedenen Sprachen oder sind lokal spezifisch.
-   **Vermeiden Sie** komplexe Tastenkombinationen, z. B. drei oder mehr Tasten (z. B. STRG+ALT+LEERZEICHEN) oder Tasten, die weit voneinander entfernt auf der Tastatur liegen (Beispiel: STRG+F5). Verwenden Sie einfache Tastenkombinationen für häufig verwendete Befehle.
-   **Verwenden Sie keine Tastenkombinationen von STRG+ALT,** da Windows diese Kombination in einigen Sprachversionen als ALTGR-Taste interpretiert, die alphanumerische Zeichen generiert.

### <a name="keyboard-and-mouse-combinations"></a>Tastenkombinationen und Mauskombinationen

-   Verwenden Sie für Links UMSCHALT+Klick, um in einem neuen Fenster zu navigieren, und drücken Sie STRG+Klick, um mithilfe einer neuen Registerkarte zu navigieren. Dieser Ansatz ist konsistent mit Windows Internet Explorer.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf die Tastatur:

-   Verwenden Sie die Bildschirmtastatur, um auf eine Tastaturdarstellung auf dem Bildschirm zu verweisen, die der Benutzer auf Eingabezeichen berührt.
-   Geben Sie Tastenkombinationen an, die mit der Modifizierertaste beginnen. Geben Sie die Modifizierertasten in der folgenden Reihenfolge an: Windows-Logo, Anwendung, STRG, ALT, UMSCHALT. Wenn der Numpad-Modifizierer verwendet wird, legen Sie diesen direkt vor dem Schlüssel ab, den er ändert.
-   Verwenden Sie nicht alle Großbuchstaben für Tastaturtasten. Befolgen Sie stattdessen die Groß-/Kleinschreibung, die von Standardtastaturen verwendet wird, oder klein, wenn die Taste nicht auf der Tastatur beschriftet ist.
    -   Verwenden Sie für alphabetische Tastenkombinationen einen Großbuchstaben.
    -   Schreibweise Nach oben, Bildlauf nach unten, Druckbildschirm und Bildlaufsperre aus.
    -   Schreibweise plus Vorzeichen, Minuszeichen, Bindestrich, Zeitraum und Komma.
    -   Verwenden Sie für Pfeiltasten den Pfeil nach links, den Pfeil nach rechts, den Pfeil nach oben und den Pfeil nach unten. Verwenden Sie keine grafischen Bezeichnungen für die Pfeiltasten.
    -   Verwenden Sie die Windows-Logo-TASTE und den Anwendungsschlüssel, um auf die Schlüssel zu verweisen, die mit Symbolen gekennzeichnet sind. Verwenden Sie keine grafischen Bezeichnungen für diese Schlüssel.

**Richtig:**

Leertaste, TAB, EINGABETASTE, SEITE NACH-OBEN, STRG+ALT+ENTF, ALT+W, STRG+PLUSZEICHEN

**Falsch:**

LEERTASTE, TAB, EINGABETASTE, PG UP, STRG+ALT+ENTF, ALT+W, STRG++

-   Geben Sie Schlüsselkombinationen mit einem Pluszeichen ohne Leerzeichen an.

**Richtig:**

STRG+A, UMSCHALT+F5

**Falsch:**

STRG+A, UMSCHALT+F5

-   Um eine Tastenkombination anzuzeigen, die Satzzeichen enthält, die die Verwendung der UMSCHALTTASTE erfordern, z. B. das Fragezeichen, fügen Sie der Kombination UMSCHALT HINZU, und geben Sie den Namen oder das Symbol des verschobenen Schlüssels an. Die Verwendung des Namens des nicht umschalteten Schlüssels, z. B. 4 anstelle von $, kann für Benutzer verwirrend oder sogar falsch sein. z. B. ? und/characters werden nicht immer auf jeder Tastatur umschaltet.

**Richtig:**

STRG+UMSCHALT+?, STRG+UMSCHALT+, \* STRG+UMSCHALT+KOMMA

**Falsch:**

STRG+UMSCHALT+/, STRG+?, STRG+UMSCHALT+8, STRG+.\*

-   Verwenden Sie zunächst den Schlüssel und mit dem Schlüsselnamen, falls dies zur Übersichtlichkeit erforderlich ist, z.B. die Taste F1. Verweisen Sie bei allen nachfolgenden Verweisen nur anhand ihres Namens auf die Taste, z.B. drücken Sie F1.
-   Weitere Informationen finden Sie insbesondere unter Zugriffsschlüssel und Tastenkombinationen in der Programmierung und in anderen technischen Dokumentationen. Verwenden Sie keine Zugriffstasten, mnemonic- oder Hot-Tasten. Überall verwenden Sie Tastenkombinationen, insbesondere in der Benutzerdokumentation.

Beim Verweisen auf die Interaktion:

-   Verwenden Sie beim Drücken und sofortigen Loslassen einer Taste drücken, nicht drücken, schlagen, drücken oder eingeben, um eine Aktion innerhalb des Programms auszulösen oder innerhalb eines Dokuments oder einer Benutzeroberfläche zu navigieren.
-   Verwenden Sie "type" und nicht "enter", um Benutzer an die Eingabe von Text zu leiten.
-   Verwenden Sie die Verwendung in Situationen, in der das Drücken verwirrend sein kann, z. B. wenn auf einen Schlüsseltyp verwiesen wird, z. B. die Pfeiltasten oder Funktionstasten. In solchen Fällen können Benutzer durch Drücken von dazu bringen, dass sie alle Tasten gleichzeitig drücken müssen.
-   Verwenden Sie halten, wenn Sie eine Taste drücken und halten, z. B. eine Modifizierertaste.
-   Verwenden Sie "press" nicht als Synonym für Klicks.

Beispiele:

-   Geben Sie Ihren Namen ein, und drücken Sie dann die EINGABETASTE.
-   Drücken Sie STRG+F, und geben Sie dann den Text ein, nach dem Sie suchen möchten.
-   Um die Datei zu speichern, drücken Sie Y.
-   Verwenden Sie die Pfeiltasten, um die Einfügemarke zu verschieben.

 

