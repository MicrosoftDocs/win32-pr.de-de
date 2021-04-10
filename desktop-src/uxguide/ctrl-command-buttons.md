---
title: Befehlsschaltflächen
description: Mit einer Befehls Schaltfläche initiieren Benutzer eine sofortige Aktion.
ms.assetid: 0e2ff31a-657b-4e4c-afee-2a6bd742f46c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 32c8c16cef275e1fefe44e579105515d3e61c497
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103761295"
---
# <a name="command-buttons"></a>Befehlsschaltflächen

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mit einer Befehls Schaltfläche initiieren Benutzer eine sofortige Aktion.

![Screenshot der Befehls Schaltfläche "OK" ](images/ctrl-command-buttons-image1.png)

Eine typische Befehls Schaltfläche.

Die Standard Befehls Schaltfläche wird aufgerufen, wenn Benutzer die EINGABETASTE drücken. Sie wird vom Entwickler zugewiesen, aber alle Befehls Schaltflächen werden zum Standard, wenn die Benutzer die Tab-Taste drücken.

> [!Note]  
> Richtlinien für das [Layout](vis-layout.md) werden in einem separaten Artikel dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Wird die Befehls Schaltfläche verwendet, um eine sofortige Aktion einzuleiten?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement.
-   **Wäre ein Link eine bessere Wahl?** Verwenden Sie einen Link, wenn:
    -   Die Aktion besteht darin, zu einer anderen Seite, einem Fenster oder einem Hilfethema zu navigieren. **Ausnahme**: die Assistenten Navigation verwendet die Befehls Schaltflächen zurück und weiter.
    -   Der Befehl ist in einen Textkörper eingebettet.
    -   Der Befehl ist in der Natur sekundär. Dies bedeutet, dass Sie sich nicht auf den primären Zweck des Fensters bezieht. In diesem Fall wäre entweder eine leichte Befehls Schaltfläche oder ein Link geeignet.
    -   Der Befehl ist Teil eines Menüs oder einer Gruppe verwandter Verknüpfungen.
    -   Die Bezeichnung ist lang und besteht aus fünf oder mehr Wörtern, sodass eine Befehls Schaltfläche ein unangenehmes Aussehen hat.
-   **Ist eine Kombination aus Options Feldern und generischen Befehls Schaltflächen eine bessere Wahl?** Häufig werden Options Felder in Verbindung mit generischen Befehls Schaltflächen (OK, Abbrechen) anstelle eines Satzes spezifischer Befehls Schaltflächen verwendet, wenn eine der folgenden Punkte zutrifft:
    -   Es sind fünf oder mehr mögliche Aktionen vorhanden.
    -   Benutzer müssen zusätzliche Informationen anzeigen, bevor Sie eine Entscheidung treffen.
    -   Benutzer müssen mit den Optionen interagieren (möglicherweise, um weitere Informationen anzuzeigen), bevor Sie eine Entscheidung treffen.
    -   Benutzer zeigen die Auswahl Optionen als Optionen anstelle verschiedener Befehle an.

        **Richtig:** ![ Screenshot: Dialogfeld, Options Felder und Text ](images/ctrl-command-buttons-image2.png)

        In diesem Beispiel werden Options Felder mit den Schaltflächen OK und Abbrechen kombiniert, um zusätzliche Informationen zu den Optionen bereitzustellen.

        **Falsch:** ![ Screenshot der Nachricht mit Befehls Schaltflächen ](images/ctrl-command-buttons-image3.png)

        In diesem Beispiel machen Befehls Schaltflächen allein es Benutzern schwierig, eine fundierte Entscheidung zu treffen.

## <a name="design-concepts"></a>Entwurfskonzepte

**Verwenden von Ellipsen**

Wenn Befehls Schaltflächen für sofortige Aktionen verwendet werden, sind möglicherweise weitere Informationen erforderlich, um die Aktion auszuführen. **Geben Sie einen Befehl an, der zusätzliche Informationen (einschließlich der Bestätigung) benötigt, indem Sie am Ende der Schaltflächen Bezeichnung eine Ellipse hinzufügen**.

![Screenshot der Druck Befehlsschaltfläche mit Ellipsen ](images/ctrl-command-buttons-image4.png)

In diesem Beispiel wird der Druck... Befehl zeigt ein Druck Dialogfeld an, um weitere Informationen zu sammeln.

![Screenshot der Druck Befehlsschaltfläche, ohne Ellipsen ](images/ctrl-command-buttons-image5.png)

Im Gegensatz dazu druckt der Befehl "Print" in diesem Beispiel eine einzelne Kopie eines Dokuments auf den Standarddrucker, ohne dass weitere Benutzerinteraktionen vorhanden sind.

Die **korrekte Verwendung von Ellipsen ist wichtig, um anzugeben, dass Benutzer vor der Durchführung der Aktion weitere Möglichkeiten treffen oder sogar die Aktion vollständig abbrechen können**. Der visuelle Hinweis, der von einem Ellipsen angeboten wird, ermöglicht es Benutzern, Ihre Software ohne Angst zu untersuchen.

**Dies bedeutet nicht, dass Sie immer dann eine Ellipse verwenden sollten, wenn eine Aktion ein anderes Fenster nur dann anzeigt** , wenn zusätzliche Informationen erforderlich sind, um die Aktion auszuführen. Folglich **nimmt jede Befehls Schaltfläche, deren implizites Verb den Wert "ein anderes Fenster anzeigen" ist, keine Ellipsen auf**, wie z. b. mit den Befehlen about, Advanced, Help (oder einem anderen Befehl, der mit einem Hilfethema verknüpft ist), Optionen, Eigenschaften oder Einstellungen.

Im Allgemeinen werden Ellipsen in Benutzeroberflächen verwendet, um die Vollständigkeit anzugeben. Befehle, die andere Fenster anzeigen, sind nicht unvollständig. Sie müssen ein anderes Fenster anzeigen, und zusätzliche Informationen sind nicht erforderlich, um die Aktion auszuführen. Bei diesem Ansatz wird die Bildschirm Übersichtlichkeit vermieden, wenn Ellipsen nur wenig Wert haben.

**Hinweis:** Wenn Sie bestimmen, ob für eine Befehls Schaltfläche ein Auslassungs Zeichen erforderlich ist, verwenden Sie nicht die Notwendigkeit, Berechtigungen als Faktor zu [erhöhen](winenv-uac.md) . Die Rechte Erweiterung ist nicht erforderlich, um einen Befehl auszuführen (sondern um die Berechtigung zu erteilen), und die Notwendigkeit, die Rechte zu erhöhen, wird durch das Sicherheitsschild angegeben.

**Wenn Sie nur eine Aktion ausführen...** Verwenden Sie eine präzise, selbsterklärende Bezeichnung, die die von der Befehls Schaltfläche ausgeführten Aktionen eindeutig beschreibt, und verwenden Sie ggf. eine Ellipse.

## <a name="usage-patterns"></a>Verwendungsmuster

Befehls Schaltflächen weisen mehrere Verwendungs Muster auf:



|                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Standard Befehls** Schaltflächen Sie können Standard Befehls Schaltflächen verwenden, um eine sofortige Aktion zu initiieren.<br/>                                                           | ![Screenshot der Standard Befehls Schaltfläche (grau) ](images/ctrl-command-buttons-image6.png)<br/> Eine Standard Befehls Schaltfläche.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Standard Befehls** Schaltflächen Die Standard Befehls Schaltfläche in einem Fenster gibt die Befehls Schaltfläche an, die aktiviert wird, wenn Benutzer die EINGABETASTE drücken.<br/>       | ![Screenshot der Standard Befehls Schaltfläche (blau) ](images/ctrl-command-buttons-image7.png)<br/> Eine Standard Befehls Schaltfläche.<br/> Alle Befehls Schaltflächen werden zum Standard, wenn die Benutzer mit der Tab-Taste. Wenn sich der Eingabefokus auf einem Steuerelement befindet, das keine Befehls Schaltfläche ist, wird die Befehls Schaltfläche mit dem Standard-Schaltflächen Attribut zum Standard. Nur eine Befehls Schaltfläche in einem Fenster kann die Standardeinstellung sein.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Leichte Befehls** Schaltflächen Eine Lightweight-Befehls Schaltfläche ähnelt einer Standard Befehls Schaltfläche, mit dem Unterschied, dass der Schaltflächen Rahmen nur beim Mauszeiger angezeigt wird. <br/> | ![Screenshot einer der beiden ausgewählten Druck Schaltflächen ](images/ctrl-command-buttons-image8.png)<br/> In diesem Beispiel hat der Befehl ein sehr schlankes aussehen (ähnlich wie ein [Link](ctrl-links.md)), bis der Benutzer mit dem Mauszeiger auf den Befehl zeigt. an diesem Punkt wird er mit einem Schaltflächen Rahmen gezeichnet.<br/> Sie können Lightweight-Befehls Schaltflächen in Situationen verwenden, in denen Sie eine Standard Befehls Schaltfläche verwenden würden, aber Sie sollten vermeiden, dass Sie immer den Schaltflächen Rahmen anzeigt. Lightweight-Befehls Schaltflächen eignen sich ideal für Befehle, die Sie unterstreichen möchten, und die Verwendung eines Links wäre nicht geeignet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Menü** Schaltflächen Verwenden Sie eine Menü Schaltfläche, wenn Sie ein Menü für einen kleinen Satz verwandter Befehle benötigen.<br/>                                                                 | ![Screenshot der Menü Schaltfläche "Format" und der zugehörigen Befehle ](images/ctrl-command-buttons-image9.png)<br/> Eine Menü Schaltfläche mit einem kleinen Satz verwandter Befehle.<br/> Verwenden Sie eine Menü Schaltfläche, wenn eine Menüleiste nicht erwünscht ist, z. b. in einem Dialogfeld, einer Symbolleiste oder einem anderen Fenster, das keine Menüleiste enthält. Ein einzelnes nach unten zeigendes Dreieck gibt an, dass durch Klicken auf die Schaltfläche ein Menü angezeigt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Trenn** Schaltflächen Verwenden Sie eine Trenn Schaltfläche, um einen Satz von Variationen eines Befehls zu konsolidieren, insbesondere, wenn einer der Befehle meistens verwendet wird.<br/>          | ![Screenshot der geöffneten Trenn Schaltfläche ohne Befehle ](images/ctrl-command-buttons-image10.png)<br/> eine reduzierte Trenn Schaltfläche.<br/> wie eine Menü Schaltfläche zeigt ein einzelnes nach unten zeigendes Dreieck an, dass durch Klicken auf den rechten Teil der Schaltfläche ein Menü angezeigt wird.<br/> ![Screenshot der geöffneten Trenn Schaltfläche mit Befehlen ](images/ctrl-command-buttons-image11.png)<br/> eine aufgeteilte Trenn Schaltfläche.<br/> in diesem Beispiel wird eine Trenn Schaltfläche verwendet, um sechs Variationen des geöffneten Befehls zu konsolidieren. der reguläre Öffnungs Befehl wird meistens verwendet, sodass Benutzer normalerweise nicht die anderen Befehle sehen müssen. die Verwendung einer unterteilten Schaltfläche spart eine beträchtliche Menge an Bildschirmfläche und bietet gleichzeitig leistungsstarke Optionen.<br/> anders als bei einer Menü Schaltfläche wird durch Klicken auf den linken Teil der Schaltfläche die Aktion direkt für die Bezeichnung ausgeführt. unterteilte Schaltflächen sind in Situationen wirksam, in denen die nächste Aktion mit einem bestimmten Tool wahrscheinlich mit der letzten Aktion identisch ist. in diesem Fall wird die Bezeichnung wie bei einer Farbauswahl in die letzte Aktion geändert:<br/> ![Screenshot der Trenn Schaltfläche "ausfüllen" ohne Befehle ](images/ctrl-command-buttons-image12.png)<br/> In diesem Beispiel wird die Bezeichnung in die letzte Aktion geändert.<br/> |
| **Schaltflächen Durchsuchen** Verwenden Sie die Schaltfläche Durchsuchen, um ein Dialogfeld anzuzeigen, mit dem Benutzer einen gültigen Wert auswählen können.<br/>                                                           | mithilfe von Schaltflächen zum Durchsuchen gestartete Dialogfelder können Benutzer Dateien, Ordner, Computer, Benutzer, Farben usw. auswählen. Sie werden in der Regel mit einem nicht eingeschränkten Steuerelement, z. b. einem Textfeld, kombiniert. Sie haben in der Regel die Bezeichnung "Browse", "Other" oder mehr und verfügen immer über ein Auslassungs Zeichen, um anzugeben, dass weitere Informationen erforderlich sind. <br/> ![Screenshot des Textfelds mit der Schaltfläche "Durchsuchen" ](images/ctrl-command-buttons-image13.png)<br/> ein Textfeld mit einer Schaltfläche zum Durchsuchen.<br/> für Windows mit vielen Schaltflächen zum Durchsuchen können Sie eine kurze Version verwenden:<br/> ![Screenshot der kurzen Schaltfläche zum Durchsuchen mit Ellipsen ](images/ctrl-command-buttons-image14.png)<br/> Eine kurze Schaltfläche zum Durchsuchen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Progressiv-Schalt** Flächen Verwenden Sie die Schaltfläche Progressive Offenlegung, um selten verwendete Optionen anzuzeigen oder auszublenden.<br/>                                            | das Ausblenden von selten verwendeten Optionen, bis Sie benötigt werden, wird als Progressive Offenlegung bezeichnet. doppelte Spitze Klammern werden verwendet, um die Progressive Offenlegung anzugeben, und Sie zeigen in der Richtung, in der die Offenlegung oder das Ausblenden stattfindet: <br/> ![Screenshot der Schaltfläche mit "More" und Pfeil nach rechts ](images/ctrl-command-buttons-image15.png)<br/> nach dem Klicken auf die Schaltfläche wird die Bezeichnung geändert, um anzugeben, dass der nächste Klick den umgekehrten Effekt hat:<br/> ![Screenshot der Schaltfläche mit "weniger" und Pfeil nach links ](images/ctrl-command-buttons-image16.png)<br/> Weitere Informationen und Beispiele finden Sie unter [Progressive Offenlegung](ctrl-progressive-disclosure-controls.md)von Steuerelementen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Richtungs** Schaltflächen Verwenden Sie eine direktionale Schaltfläche, um die Richtung anzugeben, in der eine Aktion stattfindet.<br/>                                               | in diesem Fall wird anstelle eines doppelten Chevron eine einzelne Spitze Klammer verwendet: <br/> ![Screenshot der nach-rechts-und nach-links-Taste ](images/ctrl-command-buttons-image17.png)<br/> Eine direktionale Schaltfläche gibt die Aktions Richtung an.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Zeigt einen ausgelasteten Zeiger an, wenn das Ergebnis des Klickens auf eine Befehls Schaltfläche nicht sofort ist** Ohne Feedback können Benutzer davon ausgehen, dass das Klicken nicht durchgeführt wurde, und dann erneut auf klicken.
-   Wenn dieselbe Befehls Schaltfläche in mehr als einem Fenster angezeigt wird, versuchen Sie, denselben Bezeichnungs **Text und denselben Zugriffsschlüssel zu verwenden, und suchen Sie ihn in den einzelnen Fenstern an ungefähr derselben Stelle.**
-   **Verwenden Sie für Befehls Schaltflächen mit Text Bezeichnungen eine minimale Schaltflächen breite und die standardmäßige Befehls Schaltfläche.** Weitere Informationen finden Sie unter [Empfohlene Größe und Abstände](#recommended-sizing-and-spacing).
-   Legen Sie für jedes Fenster die Befehls Schaltflächen auf **die gleiche Breite**. Wenn dies nicht praktikabel ist, begrenzen Sie die Anzahl der unterschiedlichen breiten für Befehls Schaltflächen mit Text Bezeichnungen auf zwei.
-   Wenn ein anderes Steuerelement mit einer Befehls Schaltfläche interagiert, z. b. ein Textfeld mit einer Schaltfläche zum Durchsuchen, bezeichnen Sie **die Beziehung, indem Sie die Befehls Schaltfläche an einem von drei Stellen**
    -   Rechts von und mit dem anderen Steuerelement am oberen Rand ausgerichtet.
    -   Unten und linksbündig mit dem anderen Steuerelement.
    -   Vertikaler zentriert zwischen Steuerelementen, die interagieren (z. b. Schaltflächen hinzufügen und entfernen zwischen zwei Listenfeldern für die Zusammenarbeit).
-   Wenn mehrere Befehls Schaltflächen mit dem gleichen Steuerelement interagiert, werden **Sie vertikal nach rechts von und oben mit dem anderen Steuerelement gestapelt, oder Sie können Sie nach linksbündig unter dem Steuerelement platzieren.**
-   Wenn Befehls Schaltflächen anderen Steuerelementen untergeordnet sind, **verwenden Sie die obige Platzierung, und deaktivieren Sie die untergeordnete Befehls Schaltfläche, bis das übergeordnete Steuer** Element
-   **Verwenden Sie keine schmalen, kurzen oder hohen Befehls Schaltflächen mit Text Bezeichnungen** , da Sie eher Unprofessional sehen. Versuchen Sie, mit der Standardbreite und-Höhe zu arbeiten.

**Richtig:** ![ Screenshot der Schaltfläche "Standardgröße OK" ](images/ctrl-command-buttons-image18.png)

In diesem Beispiel ist die Schaltflächen Größe Standard und Professional.

**Falsch:** ![ Screenshot der kurzen Schaltfläche "OK" ](images/ctrl-command-buttons-image19.png)

In diesem Beispiel ist die Schaltfläche zu klein.

**Falsch:** ![ Screenshot der großen, quadratischen Schaltfläche "OK" ](images/ctrl-command-buttons-image20.png)

In diesem Beispiel hat die Schaltfläche zu viel Platz um die Bezeichnung.

-   **Vermeiden Sie das Kombinieren von Text Bezeichnungen und Grafiken auf Befehls Schaltflächen** Das Kombinieren von Text und Grafiken fügt in der Regel unnötige visuelle Übersichtlichkeit hinzu und verbessert nicht das Verständnis des Benutzers. Kombinieren Sie Text und Grafiken nur dann, wenn die Grafik hilfreich ist, z. b. wenn es sich um ein Standard Symbol für den Befehl handelt, oder um Benutzer beim visualisieren der Ergebnisse des Befehls zu unterstützen. Andernfalls sollten Sie Text bevorzugen, aber entweder Text oder Grafiken verwenden.

**Richtig:** ![ Screenshot des Befehls "drehen" mit gekrümmtem Pfeil ](images/ctrl-command-buttons-image21.png)

In diesem Beispiel unterstützt die Pfeil Grafik Benutzer beim visualisieren der Ergebnisse des Befehls.

**Richtig:** ![ Screenshot der Adressleiste mit Symbolen und Text ](images/ctrl-command-buttons-image22.png)

In diesem Beispiel werden Standardsymbole mit Text kombiniert, um das Verständnis zu unterstützen.

**Falsch:** ![ Screenshot der Schaltfläche mit x-Symbol und Abbruch ](images/ctrl-command-buttons-image23.png)

In diesem Beispiel fügt die Cancel-Grafik nichts zum Text hinzu.

-   **Verwenden Sie keine Befehls Schaltflächen zum Festlegen des Zustands**. Verwenden Sie stattdessen Options Felder oder Kontrollkästchen. Befehls Schaltflächen dienen nur zum Initiieren von Aktionen.

### <a name="split-buttons"></a>Trenn Schaltflächen

-   **Stellen Sie den wahrscheinlichsten Befehl als Standardverhalten** dar. Wenn mehr als ein wahrscheinlichste Befehl vorhanden ist, wählen Sie einen aus, der keine zusätzlichen Informationen erfordert.
-   **Wenn der wahrscheinlichste Befehl die letzte Benutzer Auswahl ist, ändern Sie die Schaltflächen Bezeichnung in die letzte Auswahl.**
-   **Zeigen Sie den Standardbefehl mit fettem Text im Menü an**. Dies erleichtert es Benutzern, den Standardbefehl zu finden, insbesondere wenn der Standardbefehl dynamisch ist oder die unterteilte Schaltfläche anstelle einer Text Bezeichnung eine Grafik verwendet.

### <a name="default-values"></a>Standardwerte

-   Fügen Sie in jedem Dialogfeld eine Standard Befehls Schaltfläche ein. **Wählen Sie das sicherste (um den Verlust von Daten oder den System Zugriff zu vermeiden) und der sicherste Befehl als Standard** aus. Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie den wahrscheinlichsten oder den bequemen Befehl aus.
-   **Nehmen Sie keine destruktiven Aktionen als Standard Befehls Schaltfläche** vor, es sei denn, es gibt eine einfache Möglichkeit, den Befehl rückgängig

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstände

![Diagramm der Schaltflächen Dimensionen in Pixel und DLUs ](images/ctrl-command-buttons-image24.png)

Empfohlene Größe und Abstände für Befehls Schaltflächen.

## <a name="labels"></a>Bezeichnungen

-   Bezeichnung jeder Befehls Schaltfläche.
-   Wenn die Schaltfläche nur eine Grafik Bezeichnung hat, weisen Sie deren Name-Eigenschaft einer entsprechenden Text Bezeichnung zu. Dadurch können Hilfstechnologieprodukte, z. b. Bildschirm Sprachausgaben, Benutzern alternative Informationen zur Grafik bereitstellen.

    ![Screenshot der Schaltflächen "up", "Down" und "Copy" ](images/ctrl-command-buttons-image25.png)

    Dieses Beispiel zeigt Grafik Schaltflächen. Intern werden diese Schaltflächen als "Previous&quot;, &quot;Next&quot; und &quot;Copy&quot; bezeichnet.

-   Für kurze Schaltflächen zum Durchsuchen (mit der Bezeichnung &quot;...") sollte die interne Bezeichnung "Durchsuchen" lauten.
-   Weisen Sie einen eindeutigen [Zugriffsschlüssel](glossary.md)zu. Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).

    **Ausnahmen:**

    -   Weisen Sie den Schaltflächen "OK" und "Abbrechen" keine Zugriffsschlüssel zu, da "Enter" der Zugriffsschlüssel für die Standard Schaltfläche (normalerweise die Schaltfläche "OK") und ESC die Zugriffstaste für Abbrechen ist. Dadurch können die anderen Zugriffsschlüssel leichter zugewiesen werden.
    -   Weisen Sie den Schaltflächen für das Durchsuchen (mit der Bezeichnung "...") keine Zugriffstasten zu, da Sie nicht eindeutig zugewiesen werden können.

-   Bevorzugen spezifischer Bezeichnungen gegenüber generischen Bezeichnungen. Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen. Benutzer sind viel wahrscheinlicher, dass Befehlszeilen Bezeichnungen als statischer Text gelesen werden.

    -   **Ausnahme:** Benennen Sie die Schaltfläche Abbrechen nicht um, wenn die Bedeutung von Cancel eindeutig ist. Benutzer sollten nicht alle Schaltflächen lesen müssen, um zu bestimmen, welche Schaltfläche eine Aktion abbricht. Umbenennen Sie jedoch abbrechen, wenn unklar ist, welche Aktion abgebrochen wird, z. b. Wenn mehrere ausstehende Aktionen vorhanden sind.

    **Annehmbar:**

    ![Screenshot, der die Schaltflächen "OK" und "Abbrechen" anzeigt.](images/ctrl-command-buttons-image26.png)

    In diesem Beispiel sind "OK" und "Abbrechen" akzeptable, aber nicht spezifische Bezeichnungen.

    **Besserer**

    ![Screenshot der Schaltflächen zum Brennen von CD und Abbrechen ](images/ctrl-command-buttons-image27.png)

    In diesem Beispiel ist Burn CD spezifischer als OK.

    **Falsch:**

    ![Screenshot von Brennen von CD und nicht brennen von CD-Schaltflächen ](images/ctrl-command-buttons-image28.png)

    In diesem Beispiel sollte Abbrechen anstelle von CD nicht brennen verwendet werden.

-   Beginnen Sie Bezeichnungen mit einem imperativen Verb, und beschreiben Sie die Aktion, die von der Schaltfläche ausgeführt wird. Verwenden Sie keine Interpunktion am Ende.
    -   **Ausnahme:** Die folgenden Standard Bezeichnungen sind ohne Verben zulässig: "Erweitert", "zurück", "Details", "Weiterleiten", "kleiner", "mehr", "neu", "weiter", "Nein", "Optionen", "
-   Obwohl kurze Bezeichnungen bevorzugt werden, verwenden Sie genug Text, um den Befehl ausreichend zu erläutern. Verwenden Sie ein direktes Objekt (ein Substantiv nach dem Verb), wenn das Objekt aus dem Kontext nicht ersichtlich ist. Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen.

    **Annehmbar:**

    ![Screenshot der Schaltfläche mit "Bezeichnung hinzufügen" ](images/ctrl-command-buttons-image29.png)

    In diesem Beispiel ist eine kurze Bezeichnung akzeptabel, wenn ihre Bedeutung im Kontext leicht ersichtlich ist.

    **Besser:** (wenn "Add" nicht eindeutig ist)

    ![Screenshot der Schaltfläche mit der Bezeichnung "Elemente hinzufügen" ](images/ctrl-command-buttons-image30.png)

    In diesem Beispiel unterstützt das Hinzufügen eines Substantiv zum Verb das Verständnis der Benutzer.

    **Am besten:** (wenn Elemente hinzufügen oder hinzufügen nicht klar sind)

    ![Screenshot der Schaltfläche mit ausgewählten Elementen hinzufügen ](images/ctrl-command-buttons-image31.png)

    In diesem Beispiel ist die Bezeichnung selbsterklärend.

-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format. Dies eignet sich besser für Windows [Tone](text-style-tone.md)[und die](https://msdn.microsoft.com/library/windows/desktop/aa974175.aspx) Verwendung von kurzen Ausdrücken für Befehls Schaltflächen.
    -   **Ausnahme:** Bei älteren Anwendungen können Sie ggf. die Groß-/Kleinschreibung von Titeln verwenden, um das Mischen von groß [-](glossary.md) /Kleinschreibung
-   Verwenden Sie in Befehlszeilen Bezeichnungen nicht jetzt, da die Unmittelbarkeit des Befehls für die Gewährung übernommen werden kann.

    -   **Ausnahme:** Verwenden Sie bei Bedarf jetzt, um Befehle zu unterscheiden, die eine Aufgabe aus Befehlen starten, die eine Aufgabe sofort ausführen.

    ![Screenshot der Schaltfläche mit der Download Bezeichnung ](images/ctrl-command-buttons-image32.png)

    Wenn Sie in diesem Beispiel auf die Befehls Schaltfläche klicken, wird ein Fenster oder eine Seite angezeigt, das Benutzern das Herunterladen ermöglicht.

    ![Screenshot der Schaltfläche mit der Bezeichnung "jetzt herunterladen" ](images/ctrl-command-buttons-image33.png)

    In diesem Beispiel wird durch Klicken auf die Befehls Schaltfläche der Download durchführt.

    Nur ein Befehl in einem Aufgaben Fluss sollte mit "Now" gekennzeichnet werden. So sollte z. b. der Befehl " **jetzt herunterladen** " niemals von einem anderen Befehl " **jetzt herunterladen** " befolgt werden.

-   Verwenden Sie in Befehlszeilen Bezeichnungen nicht später, wenn dies eine Aktion impliziert, die nicht ausgeführt werden kann. Verwenden Sie z. b. nicht später installieren (im Gegensatz zur Installation jetzt), es sei denn, der Befehl wird zu einem späteren Zeitpunkt installiert. Verwenden Sie stattdessen entweder nicht installieren oder Abbrechen.

    **Falsch:**

    ![Screenshot von "jetzt neu starten" und später neu starten ](images/ctrl-command-buttons-image34.png)

    In diesem Beispiel bedeutet der Neustart später fälschlicherweise, dass der Befehl automatisch zu einem späteren Zeitpunkt neu gestartet wird.

-   Verwenden Sie die Schaltfläche Erweitert nur für Optionen, die für fortgeschrittene Benutzer relevant sind oder erweiterte Benutzerkenntnisse erfordern. Verwenden Sie keine Schaltfläche "Erweitert" für Features, die als technologisch erweitert betrachtet werden. Beispielsweise ist die hepling-Funktion eines Druckers keine erweiterte Option, aber sein Farb Verwaltungssystem ist.

    **Falsch:** (wenn die Optionen wirklich nicht fortgeschritten sind)

    ![Screenshot der Schaltfläche mit der erweiterten Bezeichnung ](images/ctrl-command-buttons-image35.png)

    In diesem Beispiel ist "Advanced" irreführend.

    **Richtig:**

    ![Screenshot der Schaltfläche mit der Bezeichnung "Weitere Optionen" ](images/ctrl-command-buttons-image36.png)

    In diesem Beispiel ist die Bezeichnung spezifischer und genauer.

-   Wählen Sie für Befehls Schaltflächen, die andere Fenster öffnen, eine Bezeichnung aus, die den Teil oder den gesamten Text der Titelleiste des sekundären Fensters verwendet. Beispielsweise wird durch die Befehls Schaltfläche Durchsuchen möglicherweise ein Dialogfeld mit der Bezeichnung nach Ordner suchen geöffnet. Die Verwendung der gleichen Terminologie in der gesamten Aufgabe trägt dazu bei, dass die Benutzer orientiert bleiben.
-   Wenn Sie eine Frage stellen, verwenden Sie Bezeichnungen, die der Frage entsprechen. Verwenden Sie OK/Abbrechen nicht, um Ja/Nein-Fragen zu beantworten.

    **Richtig:**

    ![Screenshot der Schaltflächen "Ja" und "Nein" ](images/ctrl-command-buttons-image37.png)

    In diesem Beispiel beantworten die Schaltflächen die Frage.

    **Falsch:**

    ![Screenshot der Schaltflächen "OK" und "Abbrechen" ](images/ctrl-command-buttons-image38.png)

    In diesem Beispiel beantworten die Schaltflächen die Frage nicht.

-   Beenden Sie die Bezeichnung mit einem Ellipsen, wenn der Befehl zusätzliche Informationen zur Ausführung erfordert.

    -   **Ausnahme:** Grafik Bezeichnungen nehmen keine Auslassungs Punkte auf.

    **Richtig:** (wenn ein Dialogfeld "Druckoptionen" angezeigt wird)

    ![Screenshot der Schaltfläche "Drucken" mit Ellipsen ](images/ctrl-command-buttons-image39.png)

    Wenn Sie in diesem Beispiel auf die Schaltfläche klicken, wird das Dialogfeld "Druckoptionen" angezeigt, das weitere Informationen vom Benutzer erfordert.

-   Verwenden Sie kein Auslassungs Zeichen, wenn die erfolgreiche Ausführung der Aktion lediglich ein anderes Fenster anzeigt. Die folgenden Befehle nehmen nie eine Ellipse auf: info, erweitert, Optionen, Eigenschaften, Hilfe.

    **Falsch:**

    ![Screenshot der Schaltfläche "Optionen" mit Ellipsen ](images/ctrl-command-buttons-image40.png)

    Wenn Sie in diesem Beispiel auf die Schaltfläche klicken, wird das Dialogfeld Optionen angezeigt, es sind jedoch keine weiteren Informationen vom Benutzer erforderlich.

-   Bei Mehrdeutigkeit (z. b. bei der Befehls Bezeichnung fehlt ein Verb), entscheiden Sie sich für die wahrscheinlichste Benutzeraktion. Wenn die Anzeige des Fensters eine gängige Aktion ist, verwenden Sie keine Auslassungs Punkte.

    **Richtig:**

    Weitere Farben...

    Versionsinformationen

    Im ersten Beispiel wählen Benutzer wahrscheinlich eine Farbe aus, sodass die Verwendung eines Ellipsen korrekt ist. Im zweiten Beispiel werden Benutzer wahrscheinlich die Versionsinformationen anzeigen, sodass Ellipsen unnötig sind.

-   Verwenden Sie für Schaltflächen zum Durchsuchen kurze Schaltflächen (mit der Bezeichnung "..."), wenn in einem Fenster mehr als zwei Schaltflächen zum Durchsuchen vorhanden sind. Verwenden Sie immer die kurze Version, wenn Sie eine Schaltfläche zum Durchsuchen in einem Raster anzeigen möchten.
-   Verwenden Sie für direktionale Schaltflächen eine einzelne Spitze Klammer, und legen Sie fest, wo die Aktion ausgeführt wird.

In der folgenden Tabelle werden einige allgemeine Befehlszeilen Bezeichnungen und deren Verwendung angezeigt.



|                             |                                                                                                              |                             |
|-----------------------------|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| **Schaltflächen Bezeichnung**<br/> | **Bedeutung**<br/>                                                                                       | **Zugriffsschüssel**<br/>   |
| **Zurück**<br/>         | Wechseln Sie in Assistenten und Aufgaben Flüsse zur vorherigen Seite.<br/>                                               | 'B'<br/>              |
| **Durchsuchen...**<br/>    | Zeigt ein Dialogfeld an, in dem nach einer Datei oder einem Objekt gesucht werden soll.<br/>                                                | "B" oder "r"<br/>       |
| **Optionen**<br/>      | Zeigen Sie die verfügbaren Optionen für Benutzer zum Anpassen eines Programms an.<br/>                                 | 'O'<br/>              |
| **Anhalten**<br/>        | In Bearbeitung befindliche Dialogfelder, hält die Aufgabe an.<br/>                                                       | Cker<br/>              |
| **Personalize**<br/>  | Passen Sie eine Kern Darstellung an, die für die persönliche Identifizierung des Benutzers mit einem Programm entscheidend ist.<br/> | Cker<br/>              |
| **Einstellungen**<br/>  | Verwenden Sie nicht. Verwenden Sie stattdessen Optionen.<br/>                                                                   | Nicht zutreffend<br/>  |
| **Eigenschaften**<br/>   | Zeigen Sie die Attribute und Einstellungen für ein Objekt an.<br/>                                                | "P" oder "r"<br/> |
| **Speichern**<br/>         | Speichern Sie eine Gruppe von Einstellungen, oder speichern Sie eine Datei oder ein Objekt unter Verwendung des aktuellen namens.<br/>                        | Hymnen<br/>              |
| **Speichern unter...**<br/>   | Speichert eine Datei oder ein Objekt mit einem angegebenen Namen.<br/>                                                     | Zweites "a"<br/>       |
| **Einstellungen**<br/>     | Verwenden Sie nicht. Verwenden Sie stattdessen Optionen.<br/>                                                                   | Nicht zutreffend<br/>  |
| **Problembehandlung**<br/> | Verwenden Sie nicht. Verwenden Sie stattdessen einen bestimmten Hilfelink.<br/>                                                      | Nicht zutreffend<br/>  |



 

Richtlinien zu den Bezeichnungen von Commit-Schaltflächen (OK, Abbrechen, Ja/Nein, schließen, beenden, anwenden, weiter, Fertigstellen, fertig) finden Sie unter [Benutzeroberflächen Text](text-ui.md).

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Befehls Schaltflächen:

-   Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-und Kleinschreibung, aber nicht den Unterstrich oder die Auslassungs Punkte des Zugriffsschlüssels Fügen Sie die Word-Schaltfläche nicht ein.
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie klicken.
-   Formatieren Sie nach Möglichkeit die Bezeichnung mit fettem Text. Andernfalls sollten Sie die Bezeichnung nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Klicken Sie auf **Drucken** , um das Dokument zu drucken.

 

