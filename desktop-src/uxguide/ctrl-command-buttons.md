---
title: Befehlsschaltflächen
description: Mit einer Befehlsschaltfläche initiieren Benutzer eine sofortige Aktion.
ms.assetid: 0e2ff31a-657b-4e4c-afee-2a6bd742f46c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 97b452964066ce061a71a74f547305ba7d9d5794
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524584"
---
# <a name="command-buttons"></a>Befehlsschaltflächen

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere aktuelle [Entwurfsanleitung wider.](/windows/uwp/design/)

Mit einer Befehlsschaltfläche initiieren Benutzer eine sofortige Aktion.

![Screenshot der Befehlsschaltfläche "OK" ](images/ctrl-command-buttons-image1.png)

Eine typische Befehlsschaltfläche.

Die Standardbefehlsschaltfläche wird aufgerufen, wenn Benutzer die EINGABETASTE drücken. Sie wird vom Entwickler zugewiesen, aber jede Befehlsschaltfläche wird zur Standardschaltfläche, wenn Benutzer darauf klicken.

> [!Note]  
> Richtlinien zum [Layout werden](vis-layout.md) in einem separaten Artikel vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Wird die Befehlsschaltfläche verwendet, um eine sofortige Aktion zu initiieren?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement.
-   **Wäre ein Link eine bessere Wahl?** Verwenden Sie einen Link, wenn:
    -   Die Aktion besteht im Navigieren zu einer anderen Seite, einem anderen Fenster oder einem anderen Hilfethema. **Ausnahme:** Die Navigation des Assistenten verwendet die Befehlsschaltflächen Zurück und Weiter.
    -   Der Befehl ist in einen Textkörper eingebettet.
    -   Der Befehl ist sekundär. Das heißt, es bezieht sich nicht auf den primären Zweck des Fensters. In diesem Fall wäre entweder eine einfache Befehlsschaltfläche oder ein Link geeignet.
    -   Der Befehl ist Teil eines Menüs oder einer Gruppe verwandter Links.
    -   Die Bezeichnung ist lang und besteht aus fünf oder mehr Wörtern, wodurch eine Befehlsschaltfläche umkehrlich angezeigt wird.
-   **Wäre eine Kombination aus Optionsfeldern und generischen Befehlsschaltflächen die bessere Wahl?** Häufig werden Optionsfelder in Verbindung mit generischen Befehlsschaltflächen (OK, Abbrechen) statt einer Reihe bestimmter Befehlsschaltflächen verwendet, wenn eine der folgenden Bedingungen zutrifft:
    -   Es gibt fünf oder mehr mögliche Aktionen.
    -   Benutzer müssen zusätzliche Informationen anzeigen, bevor sie eine Entscheidung treffen.
    -   Benutzer müssen mit den Optionen interagieren (um möglicherweise zusätzliche Informationen zu erhalten), bevor sie eine Entscheidung treffen.
    -   Benutzer zeigen die Optionen als Optionen anstelle verschiedener Befehle an.

        **Richtig:** ![ Screenshot des Dialogfelds, der Optionsfelder und des Texts ](images/ctrl-command-buttons-image2.png)

        In diesem Beispiel werden Optionsfelder mit den Schaltflächen OK und Abbrechen kombiniert, um zusätzliche Informationen zu den Optionen zu erhalten.

        **Falsch:** ![ Screenshot der Nachricht mit Befehlsschaltflächen ](images/ctrl-command-buttons-image3.png)

        In diesem Beispiel erschweren Befehlsschaltflächen allein benutzern das Treffen einer fundierten Entscheidung.

## <a name="design-concepts"></a>Entwurfskonzepte

**Verwenden von Ausellipsen**

Während Befehlsschaltflächen für sofortige Aktionen verwendet werden, sind möglicherweise weitere Informationen erforderlich, um die Aktion auszuführen. Geben Sie einen Befehl an, der zusätzliche Informationen (einschließlich Bestätigung) benötigt, indem Sie am Ende der Schaltflächenbezeichnung ein **Auslassungszeichen hinzufügen.**

![Screenshot der Druckbefehlsschaltfläche mit Ausellipsen ](images/ctrl-command-buttons-image4.png)

In diesem Beispiel wird die Druck-... -Befehl zeigt ein Dialogfeld Drucken an, um weitere Informationen zu sammeln.

![Screenshot der Druckbefehlsschaltfläche, keine Ausellipsen ](images/ctrl-command-buttons-image5.png)

Im Gegensatz dazu druckt der Befehl Drucken ohne weitere Benutzerinteraktion eine einzelne Kopie eines Dokuments auf dem Standarddrucker.

**Die ordnungsgemäße Verwendung von Ausellipsen** ist wichtig, um anzugeben, dass Benutzer vor dem Ausführen der Aktion weitere Entscheidungen treffen oder sogar die Aktion vollständig abbrechen können. Die visuellen Hinweise, die durch auslassungsbare Elemente geboten werden, ermöglichen es Benutzern, Ihre Software ohne Sorge zu untersuchen.

**Dies bedeutet nicht, dass Sie** immer dann eine Auslassungsellipse verwenden sollten, wenn eine Aktion nur dann ein anderes Fenster anzeigt, wenn zusätzliche Informationen zum Ausführen der Aktion erforderlich sind. Folglich nimmt jede Befehlsschaltfläche, deren implizites Verb "Anderes Fenster **anzeigen"** ist, keine Auslassungsellipse an, z. B. mit den Befehlen About, Advanced, Help (oder einem anderen Befehl, der mit einem Hilfethema verlinkt), Optionen, Eigenschaften oder Einstellungen.

Im Allgemeinen werden Ausellipsen in Benutzeroberflächen verwendet, um auf Vollständigkeit hindeuten zu können. Befehle, die andere Fenster anzeigen, sind nicht unvollständig, sie müssen ein anderes Fenster anzeigen, und es sind keine zusätzlichen Informationen erforderlich, um ihre Aktion auszuführen. Dieser Ansatz beseitigt unübersichtlichen Bildschirm in Situationen, in denen Ellipsen wenig Nutzen haben.

**Hinweis:** Wenn Sie bestimmen, ob für eine [Befehlsschaltfläche](winenv-uac.md) Auslassungsellipsen erforderlich sind, verwenden Sie nicht die Notwendigkeit, Berechtigungen als Faktor zu erhöhen. Erhöhte Rechte sind keine Informationen, die zum Ausführen eines Befehls erforderlich sind (sondern aus Berechtigungsgründen), und die Notwendigkeit einer Erhöhung wird mit dem Sicherheitsschutz angezeigt.

**Wenn Sie nur eine Sache tun...** Verwenden Sie eine präzise, spezifische, selbsterklärende Bezeichnung, die die Aktion, die die Befehlsschaltfläche ausführt, eindeutig beschreibt, und verwenden Sie gegebenenfalls auslassungszeichen.

## <a name="usage-patterns"></a>Verwendungsmuster

Befehlsschaltflächen haben mehrere Verwendungsmuster:



|     Verwendung                                                                                                                                                                    |    Beispiel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Standardbefehlsschaltflächen** Sie können Standardbefehlsschaltflächen verwenden, um eine sofortige Aktion zu initiieren.<br/>                                                           | ![Screenshot der Standardbefehlsschaltfläche (grau) ](images/ctrl-command-buttons-image6.png)<br/> Eine Standardbefehlsschaltfläche.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Standardbefehlsschaltflächen** Die Standardbefehlsschaltfläche in einem Fenster gibt die Befehlsschaltfläche an, die aktiviert wird, wenn Benutzer die EINGABETASTE drücken.<br/>       | ![Screenshot der Standardbefehlsschaltfläche (blau) ](images/ctrl-command-buttons-image7.png)<br/> Eine Standardbefehlsschaltfläche.<br/> Jede Befehlsschaltfläche wird zur Standardschaltfläche, wenn Benutzer darauf klicken. Wenn sich der Eingabefokus auf einem Steuerelement befindet, das keine Befehlsschaltfläche ist, wird die Befehlsschaltfläche mit dem Standardschaltfläche-Attribut zur Standardschaltfläche. Standardmäßig kann nur eine Befehlsschaltfläche in einem Fenster verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Einfache Befehlsschaltflächen** Eine einfache Befehlsschaltfläche ähnelt einer Standardbefehlsschaltfläche, mit der Ausnahme, dass ihr Schaltflächenrahmen nur beim Mauszeigerzeiger angezeigt wird. <br/> | ![Screenshot einer von zwei ausgewählten Druckschaltflächen ](images/ctrl-command-buttons-image8.png)<br/> In diesem Beispiel hat der Befehl eine sehr [](ctrl-links.md)einfache Darstellung (ähnlich einem Link), bis der Benutzer mit der Maustaste auf den Befehl zeigt, an dem er mit einem Schaltflächenrahmen gezeichnet wird.<br/> Sie können einfache Befehlsschaltflächen in Situationen verwenden, in denen Sie eine Standardbefehlsschaltfläche verwenden würden, aber vermeiden möchten, dass immer der Schaltflächenrahmen angezeigt wird. Einfache Befehlsschaltflächen eignen sich ideal für Befehle, die Sie unter- und verwenden möchten, und die Verwendung eines Links wäre nicht geeignet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Menüschaltflächen** Verwenden Sie eine Menüschaltfläche, wenn Sie ein Menü für eine kleine Gruppe verwandter Befehle benötigen.<br/>                                                                 | ![Screenshot der Menüschaltfläche "Format" und deren Befehle ](images/ctrl-command-buttons-image9.png)<br/> Eine Menüschaltfläche mit einem kleinen Satz verwandter Befehle.<br/> Verwenden Sie eine Menüschaltfläche, wenn eine Menüleiste nicht erwünscht ist, z. B. in einem Dialogfeld, einer Symbolleiste oder einem anderen Fenster ohne Menüleiste. Ein einzelnes nach unten zeigende Dreieck gibt an, dass durch Klicken auf die Schaltfläche ein Menü in der Dropdownliste angezeigt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Aufteilen von Schaltflächen** Verwenden Sie eine geteilte Schaltfläche, um eine Reihe von Variationen eines Befehls zu konsolidieren, insbesondere, wenn einer der Befehle in den meisten Jahren verwendet wird.<br/>          | ![Screenshot der geöffneten geteilten Schaltfläche ohne Befehle ](images/ctrl-command-buttons-image10.png)<br/> eine reduzierte Teilungsschaltfläche.<br/> Wie bei einer Menüschaltfläche gibt ein einzelnes nach unten zeigende Dreieck an, dass durch Klicken auf den äußersten rechten Teil der Schaltfläche ein Dropdownmenü angezeigt wird.<br/> ![Screenshot der geöffneten geteilten Schaltfläche mit Befehlen ](images/ctrl-command-buttons-image11.png)<br/> eine verworfene Teilungsschaltfläche.<br/> in diesem Beispiel wird eine geteilte Schaltfläche verwendet, um sechs Variationen des befehls open zu konsolidieren. Der reguläre Open-Befehl wird in den meisten Jahren verwendet, sodass Benutzer normalerweise die anderen Befehle nicht sehen müssen. Durch die Verwendung einer geteilten Schaltfläche wird viel Platz auf dem Bildschirm gespart, während gleichzeitig leistungsstarke Optionen zur Verfügung stehen.<br/> Im Gegensatz zu einer Menüschaltfläche führt das Klicken auf den linken Teil der Schaltfläche die Aktion direkt auf der Bezeichnung aus. Teilungsschaltflächen sind in Situationen wirksam, in denen die nächste Aktion mit einem bestimmten Tool wahrscheinlich mit der letzten Aktion identisch ist. In diesem Fall wird die Bezeichnung in die letzte Aktion geändert, wie bei einer Farbauswahl:<br/> ![Screenshot der Schaltfläche zum Aufteilen von Füllungen ohne Befehle ](images/ctrl-command-buttons-image12.png)<br/> In diesem Beispiel wird die Bezeichnung in die letzte Aktion geändert.<br/> |
| **Schaltflächen zum Durchsuchen** Verwenden Sie eine Schaltfläche zum Durchsuchen, um ein Dialogfeld anzuzeigen, mit dem Benutzer einen gültigen Wert auswählen können.<br/>                                                           | -Dialogfelder, die über eine Schaltfläche zum Durchsuchen gestartet werden, helfen Benutzern bei der Auswahl von Dateien, Ordnern, Computern, Benutzern, Farben und so weiter. sie werden in der Regel mit einem ierten Steuerelement kombiniert, z. B. einem Textfeld. Sie sind in der Regel als durchsuchen, andere oder mehr bezeichnet und weisen immer aus, dass weitere Informationen erforderlich sind. <br/> ![Screenshot des Textfelds mit Schaltfläche "Durchsuchen" ](images/ctrl-command-buttons-image13.png)<br/> Ein Textfeld mit einer Schaltfläche zum Durchsuchen.<br/> Für Fenster mit vielen Schaltflächen zum Durchsuchen können Sie eine Kurzversion verwenden:<br/> ![Screenshot der kurzen Schaltfläche zum Durchsuchen mit Ausellipsen ](images/ctrl-command-buttons-image14.png)<br/> Eine kurze Schaltfläche zum Durchsuchen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Schaltflächen für progressive Offenlegung** Verwenden Sie eine Progressive Disclosure-Schaltfläche, um selten verwendete Optionen ein- oder auszublenden.<br/>                                            | Das Ausblenden selten verwendeter Optionen, bis sie benötigt werden, wird als progressive Offenlegung bezeichnet. doppelte Chevrons werden verwendet, um die progressive Offenlegung anzugeben, und sie zeigen in die Richtung, in der das Ein- oder Ausblenden stattfinden wird: <br/> ![Screenshot der Schaltfläche mit "mehr" und Nach-rechts-Pfeilen ](images/ctrl-command-buttons-image15.png)<br/> Nachdem auf die Schaltfläche geklickt wurde, ändert sich die Bezeichnung, um anzugeben, dass der nächste Klick den entgegengesetzten Effekt hat:<br/> ![Screenshot der Schaltfläche mit "kleiner" und nach links weisenden Pfeilen ](images/ctrl-command-buttons-image16.png)<br/> Weitere Informationen und Beispiele finden Sie unter [Progressive Disclosure Controls](ctrl-progressive-disclosure-controls.md). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Richtungsschaltflächen** Verwenden Sie eine direktionale Schaltfläche, um die Richtung anzugeben, in der eine Aktion stattfindet.<br/>                                               | In diesem Fall wird anstelle eines doppelten Chevrons eine einzelne eckige Klammer verwendet: <br/> ![Screenshot der Nach-rechts- und nach-links-Schaltflächen ](images/ctrl-command-buttons-image17.png)<br/> Eine Richtungsschaltfläche gibt die Richtung der Aktion an.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Zeigen Sie einen zeiger auf ausgelastet an, wenn das Ergebnis des Klickens auf eine Befehlsschaltfläche nicht sofort angezeigt wird.** Ohne Feedback gehen Benutzer möglicherweise davon aus, dass der Klick nicht passiert ist, und klicken sie erneut.
-   Wenn dieselbe Befehlsschaltfläche in mehr als einem Fenster angezeigt wird, versuchen Sie, denselben Bezeichnungstext und Zugriffsschlüssel zu verwenden, und suchen Sie ihn in jedem Fenster an ungefähr derselben Stelle, wenn dies praktisch **ist.**
-   **Verwenden Sie für Befehlsschaltflächen mit Textbezeichnungen eine minimale Schaltflächenbreite und die Standardhöhe der Befehlsschaltfläche.** Weitere Informationen finden Sie unter [Empfohlene Größe und Abstand.](#recommended-sizing-and-spacing)
-   Ändern Sie für **jedes Fenster die Befehlsschaltflächen in der gleichen Breite.** Wenn dies nicht praktikabel ist, beschränken Sie die Anzahl der verschiedenen Breiten für Befehlsschaltflächen mit Textbezeichnungen auf zwei.
-   Wenn ein anderes Steuerelement mit einer Befehlsschaltfläche interoperiert, z. B. einem Textfeld mit einer Schaltfläche Durchsuchen, kennzeichnet die Beziehung, indem Sie die Befehlsschaltfläche an einer **von drei Stellen platzieren:**
    -   Rechts von und am oberen Ende des anderen Steuerelements ausgerichtet.
    -   Unten und linksbündig mit dem anderen Steuerelement.
    -   Vertikal zentriert zwischen Steuerelementen, die zusammenarbeiten (z. B. Schaltflächen Hinzufügen und Entfernen zwischen zwei interoperabilitätslistenfeldern).
-   Wenn mehrere Befehlsschaltflächen mit demselben Steuerelement zusammenarbeiten, stapeln Sie sie vertikal rechts von und oben ausgerichtet mit dem anderen Steuerelement, oder platzieren Sie sie horizontal linksbündig unter dem **Steuerelement.**
-   Wenn Befehlsschaltflächen anderen Steuerelementen untergeordnet sind, verwenden Sie die obige Platzierung, und deaktivieren Sie die untergeordnete Befehlsschaltfläche, **bis das übergeordnete Steuerelement ausgewählt ist.**
-   **Verwenden Sie keine schmalen, kurzen oder hohen** Befehlsschaltflächen mit Textbezeichnungen, da sie tendenziell unprofessionell aussehen. Versuchen Sie, mit den Standardbreiten und -höhen zu arbeiten.

**Richtig:** ![ Screenshot der Schaltfläche "OK" der Standardgröße ](images/ctrl-command-buttons-image18.png)

In diesem Beispiel ist die Schaltflächengröße standard und sieht professional aus.

**Falsch:** ![ Screenshot der kurzen SCHALTFLÄCHE "OK" ](images/ctrl-command-buttons-image19.png)

In diesem Beispiel ist die Schaltfläche zu klein.

**Falsch:** ![ Screenshot der großen, quadratischen OK-Schaltfläche ](images/ctrl-command-buttons-image20.png)

In diesem Beispiel hat die Schaltfläche zu viel Platz um die Bezeichnung.

-   **Vermeiden Sie die Kombination von Textbezeichnungen und Grafiken auf Befehlsschaltflächen.** Das Kombinieren von Text und Grafiken führt in der Regel zu unnötiger visueller Übersichtlichkeit und verbessert nicht das Verständnis des Benutzers. Erwägen Sie die Kombination von Text und Grafiken nur, wenn die Grafik das Verständnis unterstützt, z. B. wenn es sich um ein Standardsymbol für den Befehl handelt oder benutzer die Ergebnisse des Befehls visualisieren kann. Andernfalls bevorzugen Sie Text, aber verwenden Sie entweder Text oder Grafiken.

**Richtig:** ![ Screenshot des Befehls "Rotate" mit gekrümmten Pfeilen ](images/ctrl-command-buttons-image21.png)

In diesem Beispiel hilft die Pfeilgrafik Benutzern, die Ergebnisse des Befehls zu visualisieren.

**Richtig:** ![ Screenshot der Adressleiste mit Symbolen und Text ](images/ctrl-command-buttons-image22.png)

In diesem Beispiel werden Standardsymbole mit Text kombiniert, um das Verständnis zu helfen.

**Falsch:** ![ Screenshot der Schaltfläche mit x-Symbol und Abbrechen ](images/ctrl-command-buttons-image23.png)

In diesem Beispiel fügt die Abbrichtgrafik dem Text nichts hinzu.

-   **Verwenden Sie keine Befehlsschaltflächen zum Festlegen des Zustands**. Verwenden Sie stattdessen Optionsfelder oder Kontrollkästchen. Befehlsschaltflächen sind nur zum Initiieren von Aktionen.

### <a name="split-buttons"></a>Aufteilen von Schaltflächen

-   **Machen Sie den wahrscheinlichsten Befehl zum Standardverhalten.** Wenn es mehrere wahrscheinliche Befehle gibt, wählen Sie einen Befehl aus, für den keine zusätzlichen Informationen erforderlich sind.
-   **Wenn der wahrscheinlichste Befehl die letzte Benutzerauswahl ist, ändern Sie die Bezeichnung der Schaltfläche in die letzte Auswahl.**
-   **Zeigen Sie den Standardbefehl mit fett formatierten Text im Menü an.** Dadurch können Benutzer den Standardbefehl leichter finden, insbesondere wenn der Standardbefehl dynamisch ist oder die Teilungsschaltfläche eine Grafik anstelle einer Textbezeichnung verwendet.

### <a name="default-values"></a>Standardwerte

-   Fügen Sie in jedem Dialogfeld eine Standardbefehlsschaltfläche ein. **Wählen Sie den sichersten Befehl (um Datenverlust oder** Systemzugriff zu verhindern) und den sichersten Befehl als Standardbefehl aus. Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie den wahrscheinlichsten oder bequemsten Befehl aus.
-   **Machen Sie keine destruktive Aktion zur** Standardbefehlsschaltfläche, es sei denn, es gibt eine einfache Möglichkeit, den Befehl rückgängig zu machen.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstand

![Diagramm der Schaltflächendimensionen in Pixel und Stift ](images/ctrl-command-buttons-image24.png)

Empfohlene Größen- und Abstandstasten für Befehlsschaltflächen.

## <a name="labels"></a>Bezeichnungen

-   Beschriften Sie jede Befehlsschaltfläche.
-   Wenn die Schaltfläche nur über eine grafische Bezeichnung verfügt, weisen Sie deren Name-Eigenschaft einer entsprechenden Textbezeichnung zu. Auf diese Weise können Hilfstechnologieprodukte wie Sprachbildschirme Benutzern alternative Informationen über die Grafik bereitstellen.

    ![Screenshot der Schaltflächen "Nach oben", "Nach unten" und "Kopieren" ](images/ctrl-command-buttons-image25.png)

    Dieses Beispiel zeigt grafische Schaltflächen. Intern haben diese Schaltflächen die Bezeichnungen Zurück, Weiter und Kopieren.

-   Für kurze Schaltflächen zum Durchsuchen (mit der Bezeichnung "...") sollte die interne Bezeichnung Durchsuchen sein.
-   Weisen Sie einen [eindeutigen Zugriffsschlüssel zu.](glossary.md) Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).

    **Ausnahmen:**

    -   Weisen Sie den Schaltflächen OK und Abbrechen keine Zugriffsschlüssel zu, da die EINGABETASTE der Zugriffsschlüssel für die Standardschaltfläche (normalerweise die Schaltfläche OK) und ESC der Zugriffsschlüssel für Abbrechen ist. Dadurch wird die Zuweisung der anderen Zugriffsschlüssel vereinfacht.
    -   Weisen Sie kurzen Schaltflächen zum Durchsuchen (mit der Bezeichnung "...") keine Zugriffsschlüssel zu, da sie nicht eindeutig zugewiesen werden können.

-   Bevorzugen Sie bestimmte Bezeichnungen gegenüber generischen Bezeichnungen. Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen. Benutzer lesen die Bezeichnungen der Befehlsschaltfläche viel wahrscheinlicher als statischen Text.

    -   **Ausnahme:** Benennen Sie die Schaltfläche Abbrechen nicht um, wenn die Bedeutung des Abbrechens eindeutig ist. Benutzer sollten nicht alle Schaltflächen lesen müssen, um zu bestimmen, welche Schaltfläche eine Aktion abbricht. Benennen Sie abbrechen jedoch um, wenn unklar ist, welche Aktion abgebrochen wird, z. B. wenn mehrere Aktionen ausstehen.

    **Annehmbar:**

    ![Screenshot: Schaltflächen "OK" und "Abbrechen"](images/ctrl-command-buttons-image26.png)

    In diesem Beispiel sind OK und Abbrechen akzeptable, aber nicht angegebene Bezeichnungen.

    **Besser:**

    ![Screenshot der Schaltflächen "CD" und "Abbrechen" ](images/ctrl-command-buttons-image27.png)

    In diesem Beispiel ist CD-Burn spezifischer als OK.

    **Falsch:**

    ![Screenshot von "cd" und "cd"-Schaltflächen werden nicht glühen ](images/ctrl-command-buttons-image28.png)

    In diesem Beispiel sollte Cancel anstelle von Don't Burn CD verwendet werden.

-   Starten Sie Bezeichnungen mit einem imperativen Verb, und beschreiben Sie die Aktion, die die Schaltfläche ausführt. Verwenden Sie keine Interpunktion am Ende.
    -   **Ausnahme:** Die folgenden Standardbezeichnungen sind ohne Verben akzeptabel: Erweitert, Zurück, Details, Vorwärts, Weniger, Mehr, Neu, Weiter, Nein, OK, Optionen, Zurück, Eigenschaften, Einstellungen und Ja.
-   Obwohl kurze Bezeichnungen bevorzugt werden, verwenden Sie genügend Text, um den Befehl ausreichend zu erklären. Verwenden Sie ein direktes Objekt (ein Nomen nach dem Verb), wenn das Objekt nicht aus dem Kontext ersichtlich ist. Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen.

    **Annehmbar:**

    ![Screenshot der Schaltfläche mit Bezeichnung hinzufügen ](images/ctrl-command-buttons-image29.png)

    In diesem Beispiel ist eine Kurzbezeichnung akzeptabel, wenn ihre Bedeutung im Kontext leicht erkennbar ist.

    **Besser:** (wenn Hinzufügen nicht klar ist)

    ![Screenshot der Schaltfläche mit der Bezeichnung "Elemente hinzufügen" ](images/ctrl-command-buttons-image30.png)

    In diesem Beispiel unterstützt das Hinzufügen eines Nomens zum Verb das Verständnis der Benutzer.

    **Am besten:** (wenn Elemente hinzufügen oder hinzufügen nicht klar ist)

    ![Screenshot der Schaltfläche mit ausgewähltem Element hinzufügen ](images/ctrl-command-buttons-image31.png)

    In diesem Beispiel ist die Bezeichnung selbsterklärend.

-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md) Dies ist besser geeignet für [Windows-Ton](text-style-tone.md)[Windows-Ton](https://msdn.microsoft.com/library/windows/desktop/aa974175.aspx) und die Verwendung kurzer Ausdrücke für Befehlsschaltflächen.
    -   **Ausnahme:** Bei älteren Anwendungen können Sie bei Bedarf die [Groß-/Formatvorlagen](glossary.md) verwenden, um das Mischen von Groß-/Formatvorlagen zu vermeiden.
-   Verwenden Sie jetzt nicht in Befehlsschaltfläche-Bezeichnungen, da die Unmittelbarkeit des Befehls selbstverständlich ist.

    -   **Ausnahme:** Verwenden Sie bei Bedarf jetzt , um Befehle, die eine Aufgabe starten, von Befehlen zu unterscheiden, die eine Aufgabe sofort ausführen.

    ![Screenshot der Schaltfläche mit Downloadbezeichnung ](images/ctrl-command-buttons-image32.png)

    In diesem Beispiel wird durch Klicken auf die Befehlsschaltfläche ein Fenster oder eine Seite geöffnet, auf der Benutzer herunterladen können.

    ![Screenshot der Schaltfläche mit der Bezeichnung "Jetzt herunterladen" ](images/ctrl-command-buttons-image33.png)

    In diesem Beispiel wird durch Klicken auf die Befehlsschaltfläche der Download ausgeführt.

    Nur ein Befehl in einem Taskfluss sollte jetzt mit bezeichnet werden. Beispielsweise sollte auf den **Befehl Jetzt** herunterladen nie ein weiterer Befehl Jetzt herunterladen **folgen.**

-   Verwenden Sie später nicht in Befehlsschaltfläche-Bezeichnungen, wenn dies eine Aktion impliziert, die nicht ausgeführt wird. Verwenden Sie beispielsweise Nicht später installieren (im Gegensatz zu Jetzt installieren), es sei denn, dieser Befehl wird zu einem späteren Zeitpunkt installiert. Verwenden Sie stattdessen entweder Nicht installieren oder Abbrechen.

    **Falsch:**

    ![Screenshot von "Jetzt neu starten" und "Später neu starten" ](images/ctrl-command-buttons-image34.png)

    In diesem Beispiel impliziert Restart Later fälschlicherweise, dass der Befehl zu einem späteren Zeitpunkt automatisch neu gestartet wird.

-   Verwenden Sie die Schaltfläche Erweitert nur für Optionen, die für fortgeschrittene Benutzer relevant sind oder erweiterte Benutzerkenntnisse erfordern. Verwenden Sie keine Schaltfläche Erweitert für Features, die als technisch fortgeschritten angesehen werden. Beispielsweise ist das Heftfeature eines Druckers keine erweiterte Option, aber das Farbverwaltungssystem ist dies.

    **Falsch:** (wenn die Optionen tatsächlich nicht erweitert sind)

    ![Screenshot der Schaltfläche mit erweiterter Bezeichnung ](images/ctrl-command-buttons-image35.png)

    In diesem Beispiel ist Erweitert irreführend.

    **Richtig:**

    ![Screenshot der Schaltfläche mit einer Bezeichnung für weitere Optionen ](images/ctrl-command-buttons-image36.png)

    In diesem Beispiel ist die Bezeichnung spezifischer und genauer.

-   Wählen Sie für Befehlsschaltflächen, die andere Fenster öffnen, eine Bezeichnung aus, die den Titelleistentext des sekundären Fensters teilweise oder ganz verwendet. Beispielsweise kann eine Befehlsschaltfläche mit der Bezeichnung Durchsuchen ein Dialogfeld mit dem Titel Nach Ordner suchen öffnen. Die Verwendung der gleichen Terminologie in der gesamten Aufgabe trägt dazu bei, benutzerorientiert zu bleiben.
-   Wenn Sie eine Frage stellen, verwenden Sie Bezeichnungen, die mit der Frage übereinstimmen. Verwenden Sie nicht OK/Abbrechen, um Ja/Nein-Fragen zu beantworten.

    **Richtig:**

    ![Screenshot der Schaltflächen "Ja" und "Nein" ](images/ctrl-command-buttons-image37.png)

    In diesem Beispiel beantworten die Schaltflächen die Frage.

    **Falsch:**

    ![Screenshot der Schaltflächen "OK" und "Abbrechen" ](images/ctrl-command-buttons-image38.png)

    In diesem Beispiel beantworten die Schaltflächen die Frage nicht.

-   Beenden Sie die Bezeichnung mit einem Auslassungszeichen, wenn für den Befehl zusätzliche Informationen zum Ausführen erforderlich sind.

    -   **Ausnahme:** Grafische Bezeichnungen verwenden keine Auslassungszeichen.

    **Richtig:** (wenn ein Dialogfeld "Druckoptionen" angezeigt wird)

    ![Screenshot der Druckschaltfläche mit Ausellipsen ](images/ctrl-command-buttons-image39.png)

    In diesem Beispiel wird nach dem Klicken auf die Schaltfläche das Dialogfeld Druckoptionen angezeigt, und der Benutzer benötigt weitere Informationen.

-   Verwenden Sie keine Auslassungsellipse, wenn der erfolgreiche Abschluss der Aktion lediglich das Anzeigen eines anderen Fensters ist. Die folgenden Befehle nehmen nie aus: About, Advanced, Options, Properties, Help.

    **Falsch:**

    ![Screenshot der Optionsschaltfläche mit Ausellipsen ](images/ctrl-command-buttons-image40.png)

    In diesem Beispiel wird nach dem Klicken auf die Schaltfläche das Dialogfeld Optionen angezeigt. Weitere Informationen vom Benutzer sind jedoch nicht erforderlich.

-   Bei Mehrdeutigkeit (z. B. fehlt in der Befehlsbezeichnung ein Verb), entscheiden Sie basierend auf der wahrscheinlichsten Benutzeraktion. Wenn das einfache Anzeigen des Fensters eine gängige Aktion ist, verwenden Sie keine Auslassungsellipse.

    **Richtig:**

    Weitere Farben...

    Versionsinformationen

    Im ersten Beispiel wählen Benutzer wahrscheinlich eine Farbe aus, daher ist die Verwendung von Ausellipsen richtig. Im zweiten Beispiel werden Benutzer wahrscheinlich die Versionsinformationen anzeigen, wodurch Ellipsen nicht erforderlich sind.

-   Verwenden Sie für Schaltflächen zum Durchsuchen kurze Schaltflächen (mit der Bezeichnung "..."), wenn ein Fenster mehr als zwei Schaltflächen zum Durchsuchen enthält. Verwenden Sie immer die Kurzversion, wenn Sie eine Schaltfläche zum Durchsuchen in einem Raster anzeigen möchten.
-   Verwenden Sie für direktionale Schaltflächen eine einzelne eckige Klammer, und lassen Sie sie in die Richtung zeigen, in der die Aktion stattfindet.

In der folgenden Tabelle sind einige allgemeine Befehlsschaltflächenbezeichnungen und ihre Verwendung aufgeführt.



| Schaltflächenbezeichnung | Bedeutung              | Zugriffsschüssel   |
|-----------------------------|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| **Zurück**<br/>         | Wechseln Sie in Assistenten und Aufgabenflüssen zur vorherigen Seite.<br/>                                               | 'B'<br/>              |
| **Durchsuchen...**<br/>    | Zeigt ein Dialogfeld an, um nach einer Datei oder einem Objekt zu suchen.<br/>                                                | "B" oder "r"<br/>       |
| **Optionen**<br/>      | Zeigt die Optionen an, die Benutzern zum Anpassen eines Programms zur Verfügung stehen.<br/>                                 | 'O'<br/>              |
| **Anhalten**<br/>        | In Bearbeitung (Dialogfelder) wird die Aufgabe angehalten.<br/>                                                       | "P"<br/>              |
| **Personalize**<br/>  | Passen Sie eine Kernerfahrung an, die für die persönliche Identifikation des Benutzers mit einem Programm entscheidend ist.<br/> | "P"<br/>              |
| **Einstellungen**<br/>  | Nicht verwenden. Verwenden Sie stattdessen Optionen.<br/>                                                                   | Nicht zutreffend<br/>  |
| **Eigenschaften**<br/>   | Zeigt die Attribute und Einstellungen für ein Objekt an.<br/>                                                | "P" oder erstes "r"<br/> |
| **Speichern**<br/>         | Speichern Sie eine Gruppe von Einstellungen, oder speichern Sie eine Datei oder ein Objekt mit dem aktuellen Namen.<br/>                        | 'S'<br/>              |
| **Speichern unter...**<br/>   | Speichern Sie eine Datei oder ein Objekt mit einem angegebenen Namen.<br/>                                                     | Zweites "a"<br/>       |
| **Einstellungen**<br/>     | Nicht verwenden. Verwenden Sie stattdessen Optionen.<br/>                                                                   | Nicht zutreffend<br/>  |
| **Problembehandlung**<br/> | Nicht verwenden. Verwenden Sie stattdessen einen bestimmten Hilfelink.<br/>                                                      | Nicht zutreffend<br/>  |



 

Richtlinien zu Commit-Schaltflächenbezeichnungen (OK, Abbrechen, Ja/Nein, Schließen, Beenden, Anwenden, Weiter, Fertig) finden Sie unter [Benutzeroberfläche Text](text-ui.md).

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Befehlsschaltflächen:

-   Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Großschreibung, aber nicht den Zugriffsschlüsselunterstrich oder die Auslassungszeichen. Schließen Sie die Wortschaltfläche nicht ein.
-   Um die Benutzerinteraktion zu beschreiben, klicken Sie auf .
-   Formatieren Sie die Bezeichnung nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

Beispiel: Klicken Sie auf **Drucken,** um das Dokument zu drucken.

 

