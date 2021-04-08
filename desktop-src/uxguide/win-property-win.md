---
title: Eigenschaften Fenster
description: Das Eigenschaften Fenster ist der gemeinsame Name für die folgenden Typen von Benutzeroberflächen (User Interfaces, UIs), die zum Anzeigen und Ändern von Eigenschaften für ein Objekt oder eine Auflistung von Objekten in einem Dialogfeld verwendet werden. Eigenschaften Inspektor, der zum Anzeigen und Ändern von Eigenschaften für ein Objekt oder eine Sammlung von Objekten in einem Bereich verwendet wird. Dialogfeld "Optionen" zum Anzeigen und Ändern von Optionen für eine Anwendung.
ms.assetid: 18fc04da-9f84-4a44-9f3d-a9e29b121e7c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c255d638f236b4bc4a4f1a6c923eac24421cfe9d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103761214"
---
# <a name="property-windows"></a>Eigenschaften Fenster

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Das Eigenschaften Fenster ist der Sammelname für die folgenden Typen von Benutzeroberflächen (User Interfaces, UIs):

-   Eigenschaften Blatt: wird zum **anzeigen und Ändern von Eigenschaften für ein Objekt oder eine Sammlung von Objekten in einem Dialogfeld** verwendet.
-   Eigenschaften Inspektor: wird zum **anzeigen und Ändern von Eigenschaften für ein Objekt oder eine Sammlung von Objekten in einem** Bereich verwendet.
-   Optionen (Dialogfeld): dient zum **anzeigen und Ändern von Optionen für eine Anwendung**.

Eine Eigenschaft für ein Objekt ist eine der folgenden:

-   Eine Einstellung, die Benutzer ändern können (z. b. der Name einer Datei und das schreibgeschützte Attribut).
-   Ein Attribut eines Objekts, das Benutzer nicht direkt ändern können (z. b. Größe und Erstellungsdatum einer Datei).

Im Gegensatz zu Dialogfeldern (außer Options Dialogfeldern) und Assistenten unterstützen Eigenschaften Fenster in der Regel mehrere Aufgaben anstelle einer einzelnen Aufgabe.

Eigenschaften Fenster werden in der Regel in Seiten organisiert, auf die über Registerkarten zugegriffen wird. Eigenschaften Fenster sind häufig mit Registerkarten verknüpft (und umgekehrt), aber **Registerkarten sind für Eigenschaften Fenster nicht von Bedeutung**.

![Screenshot des Eigenschaften Blatts "Dokumenteigenschaften" ](images/win-property-win-image1.png)

Ein typisches Eigenschaften Blatt.

**Hinweis:** Richtlinien im Zusammenhang mit [Layout](vis-layout.md) und [Registerkarten](ctrl-tabs.md) werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Erfordert das Festlegen der Eigenschaften, dass Benutzer eine festgelegte, nicht triviale Abfolge von Schritten ausführen?** Wenn dies der Fall ist, verwenden Sie stattdessen einen [Assistenten](win-wizards.md) oder einen [Task Fluss](glossary.md) .
-   **Handelt es sich bei dem Inhalt ausschließlich um Anwendungs Optionen?** Wenn dies der Fall ist, verwenden Sie das Dialogfeld Optionen.
-   **Handelt es sich bei dem Inhalt ausschließlich um die Attribute einer Anwendung?** Wenn dies der Fall ist, verwenden Sie das [Feld Info](glossary.md).
-   **Handelt es sich bei dem Inhalt hauptsächlich um die Eigenschaften eines Objekts (seine Einstellungen oder Attribute)?** Wenn nicht, verwenden Sie ein Standard [Dialogfeld](win-dialog-box.md) oder ein [Dialogfeld im Register](glossary.md)Kartenformat.
-   Werden Benutzer **wahrscheinlich häufig oder über einen längeren Zeitraum Eigenschaften anzeigen oder ändern?** Wenn dies der Fall ist, verwenden Sie einen Eigenschaften Inspektor. Verwenden Sie andernfalls ein Eigenschaften Blatt.
-   Können Benutzer die **Eigenschaften für mehrere unterschiedliche Objekte gleichzeitig anzeigen oder ändern?** Wenn dies der Fall ist, verwenden Sie einen Eigenschaften Inspektor. Verwenden Sie andernfalls ein Eigenschaften Blatt.

**Eigenschaften Blätter und Eigenschaften Inspektoren sind nicht exklusiv.** Sie können die am häufigsten verwendeten Eigenschaften in einer Eigenschaften Analyse und die gesamte Gruppe auf dem Eigenschaften Blatt anzeigen.

## <a name="design-concepts"></a>Entwurfskonzepte

**Eigenschaften Fenster werden oft zu einer ungeraden Palette von technologischen Einstellungen auf niedriger Ebene.** Zu häufig sind diese Eigenschaften in Registerkarten unterteilt, aber darüber hinaus sind Sie nicht für bestimmte Aufgaben oder Benutzer vorgesehen. Wenn Benutzer mit einer Aufgabe in einem Eigenschaften Fenster konfrontiert werden, wissen Sie daher oft nicht, was zu tun ist.

Führen Sie die folgenden Schritte aus, um sicherzustellen, dass ihre Eigenschaften Fenster nützlich und verwendbar sind:

-   Stellen Sie sicher, dass die Eigenschaften erforderlich sind.
-   Präsentieren von Eigenschaften in Bezug auf die Benutzer Ziele, nicht auf die Technologie.
-   Stellen Sie die Eigenschaften auf der rechten Ebene dar.
-   Entwurfs Seiten für bestimmte Aufgaben.
-   Entwurfs Seiten für bestimmte Benutzer, insbesondere für eingeschränkte Benutzer (nicht-Administratoren).
-   Organisieren Sie die Eigenschaften Seiten effizient.

**Wenn Sie nur eine Aktion ausführen...**

Präsentieren von Eigenschaften in Bezug auf die Benutzer Ziele, nicht auf die Technologie. Geben Sie an, dass Sie die Eigenschaft erläutern und warum Sie für einen Freund hilfreich ist. Wie würden Sie es erläutern? Welche Sprache sollten Sie verwenden? Dies ist die Sprache, die in den Eigenschaften Seiten verwendet werden soll.

## <a name="usage-patterns"></a>Verwendungsmuster

Eigenschaften Fenster verfügen über mehrere Verwendungs Muster.

-   Eigenschaften Blätter. Eigenschaften für ein einzelnes Objekt werden in einem nicht modalem Dialogfeld angezeigt.
-   Eigenschaften Blätter mit mehreren Objekten. Eigenschaften für mehrere Objekte werden in einem nicht modalem Dialogfeld angezeigt.
-   Eigenschaften Blätter für effektive Einstellungen. Die effektiven Eigenschaften für ein einzelnes Objekt werden in einem nicht modalem Dialogfeld angezeigt.
-   Dialogfelder für Optionen. Die Eigenschaften einer Anwendung werden in einem modalen Dialogfeld angezeigt.
-   Eigenschaften Inspektoren. Eigenschaften für die aktuelle Auswahl (ein einzelnes Objekt oder eine Gruppe von Objekten) werden in einem nicht modalem Fensterbereich oder in einem nicht angedockten Fenster angezeigt.

Alle Eigenschaften Fenster Muster außer Eigenschaften Inspektoren verwenden einen verzögerten Commit, was bedeutet, dass Änderungen nur wirksam werden, wenn Benutzer auf OK oder übernehmen klicken. Eigenschaften Inspektoren verwenden einen sofortigen Commit (die Eigenschaften werden geändert, sobald Benutzer Änderungen vornehmen). Daher sind die Schaltflächen "OK", "Abbrechen" und "anwenden" nicht erforderlich.

## <a name="guidelines"></a>Richtlinien

### <a name="property-sheets"></a>Eigenschaftenblätter

-   **Anzeigen eines Eigenschaften Blatts, wenn Benutzer:**
    -   Wählen Sie den Befehl Eigenschaften für ein Objekt aus.
    -   Legen Sie den Eingabefokus auf ein Objekt fest, und drücken Sie ALT + EINGABETASTE.

**Eigenschaften Blätter mit mehreren Objekten**

-   **Zeigt die allgemeinen Eigenschaften aller ausgewählten Objekte an.** Wenn sich die Eigenschaftswerte unterscheiden, können Sie die Steuerelemente anzeigen, die diesen Werten zugeordnet sind. (Informationen zum Verwenden von Werten mit gemischtem Status finden Sie in den entsprechenden Steuerungs Richtlinien.)
-   Wenn das ausgewählte Objekt eine Auflistung von mehreren diskreten Objekten ist (z. b. ein Datei Ordner), werden **die Eigenschaften des einzelnen gruppierten Objekts anstelle eines Eigenschaften Blatts mit mehreren Objekten für die diskreten Objekte angezeigt.**

### <a name="options-dialog-boxes"></a>Optionen (Dialogfelder)

-   **Trennen Sie Optionen nicht von der Anpassung.** Das heißt, Sie verfügen nicht über einen Befehl "Optionen" und einen "anpassen"-Befehl. Benutzer sind häufig von dieser Trennung verwirrt. Greifen Sie stattdessen auf die Anpassung über Optionen zu.

### <a name="property-pages"></a>Eigenschaftenseiten

-   **Befolgen Sie diese Richtlinien für die Seiten Reihenfolge:**
    -   Legen Sie die Seite Allgemein oder die entsprechende auf die erste Seite.
    -   Legen Sie die Seite "Erweitert" oder die entsprechende auf der letzten Seite ab.
    -   Für die restlichen Seiten:
        -   Organisieren Sie Sie in Gruppen verwandter Seiten.
        -   Ordnen Sie die Gruppen nach der Wahrscheinlichkeit ihrer Nutzung.
        -   Ordnen Sie die Seiten innerhalb jeder Gruppe entweder nach ihren Beziehungen oder nach der Wahrscheinlichkeit ihrer Verwendung.
        -   Sie sollten nicht so viele Seiten haben, dass Sie in alphabetischer Reihenfolge angezeigt werden müssen.
-   **Machen Sie die Seiten kohärent, indem Sie alle Eigenschaften auf jeder Seite mit einem einzelnen, spezifischen, aufgabenbasierten Zweck verknüpfen.**
-   **Wenn Speicherplatz zulässt, erläutern Sie den Zweck des Eigenschaften Fensters am oberen Rand der Seite, wenn die Ziel Benutzer nicht offensichtlich sind.** Wenn die Seite verwendet wird, um nur eine einzelne Aufgabe auszuführen, **formulieren Sie den Text als eine klare Anweisung zum Ausführen dieser Aufgabe**. Verwenden Sie vollständige Sätze, die mit einem bestimmten Zeitraum enden.

    ![Screenshot des Eigenschaften Blatts "Firewalleigenschaften" ](images/win-property-win-image2.png)

    In diesem Beispiel wird der Zweck der Microsoft Windows-Firewall oben auf der Seite Allgemein erläutert.

-   **Verwenden Sie konsistente Steuerelement Namen und-Speicherorte, um den Seiten übergreifenden Inhalt konsistent zu gestalten.** Wenn z. b. mehrere Seiten namens Felder haben, versuchen Sie, Sie am gleichen Speicherort auf der Seite zu platzieren und konsistente Bezeichnungen zu verwenden. Ein ähnlicher Inhalt sollte nicht von Seite zu Seite springen.
-   **Platzieren Sie dieselbe Eigenschaft in der gesamten Anwendung auf derselben Seite.** Legen Sie z. b. auf der Registerkarte Allgemein für einen Objekttyp und auf der Registerkarte Erweitert für einen anderen Typ keine Ablauf Eigenschaft ab.
-   **Wenn Benutzer wahrscheinlich mit der zuletzt angezeigten Seite beginnen, legen Sie die Seite auf der Registerkarte dauerhaft ab, und wählen Sie Sie standardmäßig aus.** Sorgen Sie dafür, dass die Einstellungen für das Fenster pro Eigenschaft dauerhaft gespeichert werden. Wählen Sie andernfalls standardmäßig die erste Seite aus.
-   **Nehmen Sie nicht die Einstellungen auf einer Seite vor, die von den Einstellungen auf anderen Seiten abhängig sind.** Legen Sie stattdessen die abhängigen Einstellungen auf einer einzelnen Seite ab. Wenn Sie eine Einstellung auf einer Seite ändern, sollten die Einstellungen auf anderen Seiten niemals automatisch geändert werden.
    -   **Ausnahme:** Wenn sich die abhängigen Einstellungen in zwei unterschiedlichen Eigenschaften Fenstern befinden, verwenden Sie statische Text Beschriftungen, um diese Beziehung an beiden Speicherorten zu erläutern.
-   **Scrollen Sie nicht auf Eigenschaften Seiten.** Sowohl Registerkarten als auch Scrollleisten werden verwendet, um den effektiven Bereich eines Fensters zu vergrößern, aber es sollte ein Mechanismus ausreichen. Anstatt Scrollleisten zu verwenden, machen Sie die Eigenschaften Seiten größer, und legen Sie die Seiten auf effiziente Weise fest.

**Erste Seiten**

-   Legen Sie für Objekteigenschaften **den Namen des Objekts auf der ersten Seite ab.**
-   Wenn Sie den Objekten (optional) [Symbole](vis-icons.md) zuordnen, **zeigen Sie das entsprechende Symbol in der oberen linken Ecke** der ersten Seite an.

**Allgemeine Seiten**

-   **Vermeiden Sie allgemeine Seiten.** Sie benötigen keine Seite "Allgemein". Nur eine allgemeine Seite verwenden, wenn:
    -   Die Eigenschaften gelten für mehrere Aufgaben und sind für die meisten Benutzer von Bedeutung. Legen Sie auf der Seite Allgemein keine spezialisierten oder erweiterten Eigenschaften auf, aber Sie können auf der Seite Allgemein über eine Befehls Schaltfläche auf Sie zugreifen.
    -   Die Eigenschaften passen nicht zu einer spezifischeren Kategorie. Wenn dies der Fall ist, verwenden Sie stattdessen den Namen für die Seite.

**Erweiterte Seiten**

-   **Vermeiden Sie erweiterte Seiten.** Erweiterte Seite nur verwenden, wenn:
    -   Die Eigenschaften gelten für ungewöhnliche Aufgaben und sind hauptsächlich für fortgeschrittene Benutzer von Bedeutung.
    -   Die Eigenschaften passen nicht zu einer spezifischeren Kategorie. Wenn dies der Fall ist, verwenden Sie stattdessen den Namen für die Seite.
-   **Keine Eigenschaften, die ausschließlich auf technologischen Measures basieren, werden nicht aufgerufen.** Beispielsweise kann eine Drucker Heften-Option eine erweiterte Drucker Funktion sein, aber Sie ist für alle Benutzer von Bedeutung, sodass Sie sich nicht auf einer erweiterten Seite befinden sollte.

### <a name="owned-property-windows"></a>Besitzende Eigenschaften Fenster

-   **Sie sollten nicht mehr als ein Eigenschafts Fenster im Besitz eines Eigenschaften Fensters anzeigen.** Wenn Sie mehr als eins anzeigen, ist die Bedeutung der Schaltflächen OK und Abbrechen schwer zu verstehen. Sie können andere Typen von hilfdialogfeldern (z. b. Objekt-Picker) nach Bedarf anzeigen.

    **Falsch:**

    ![Screenshot der drei eigenen Eigenschaften Fenster ](images/win-property-win-image3.png)

    In diesem Beispiel umfasst das Dialogfeld "Besitzer Optionen" drei Ebenen von Eigenschafts Fenstern. Folglich sind die Bedeutungen von "OK" und "Abbrechen" verwirrend.

-   Stellen Sie für Eigenschaften Fenster, die ein verzögertes Commit-Modell verwenden, sicher, dass **die Benutzer Änderungen, die in einem eigenen Eigenschaften Fenster vorgenommen wurden, abbrechen können, indem Sie im Fenster Besitzer**
-   Wenn ein eigenes Eigenschaften Fenster einen sofortigen Commit erfordert, **Geben Sie an, dass die Änderungen durch Umbenennen der Schaltfläche Abbrechen im Fenster Besitzer geändert wurden, um den Vorgang zu schließen.** Setzen Sie die Schaltfläche zurück, um abbrechen, wenn der Benutzer auf übernehmen klickt.

    ![Screenshot des Eigenschaften Fensters mit "OK" und "Schließen" ](images/win-property-win-image4.png)

    In diesem Beispiel können Änderungen an benutzerdefinierten Wörterbüchern und Grammatik Einstellungen nicht abgebrochen werden. Sie können Benutzern dieses Feedback geben, indem Sie Abbrechen ändern, um den Vorgang zu schließen.

**Andere Fenster im Besitz**

-   Wenn ein eigenes Fenster verwendet wird, um eine hilfsaufgabe auszuführen, **benennen Sie die Schaltfläche Abbrechen nicht um.** Die vorangehenden Richtlinien gelten nur für eigene Eigenschaften Fenster, nicht für Dialogfelder, die zum Ausführen von Hilfsaufgaben verwendet werden.

    ![Screenshot des Besitzer Fensters und der Datenträger Bereinigung ](images/win-property-win-image5.png)

    In diesem Beispiel ist die Datenträger Bereinigung eine hilfsanweise, sodass die vorherigen Richtlinien nicht zutreffen. Beispielsweise sollte die Schaltfläche Abbrechen im Fenster Besitzer nicht in schließen geändert werden.

-   Wenn das eigene Fenster verwendet wird, um eine hilfsaufgabe auszuführen, **Schließen Sie das Eigenschaften Fenster des Besitzers nicht, wenn auf die Befehls Schaltfläche geklickt wird.** Dabei geht es um Disorienting und geht davon aus, dass der Benutzer das Eigenschaften Fenster nur dann durchführen muss, wenn dieser Befehl ausgeführt wird.

    **Falsch:**

    ![Screenshot des Dialog Felds "Optionen" ](images/win-property-win-image6.png)

    Wenn Sie in diesem Beispiel auf **Dokument schützen** klicken, wird das Dialogfeld Optionen nicht ordnungsgemäß geschlossen.

### <a name="tabs"></a>Registerkarten

-   **Verwenden Sie präzise Registerkarten Bezeichnungen.** Verwenden Sie ein oder zwei Wörter, die den Inhalt der Seite eindeutig beschreiben. Längere Bezeichnungen führen zu einer ineffizienten Verwendung des Bildschirm Raums, insbesondere dann, wenn die Bezeichnungen lokalisiert sind.
-   **Verwenden Sie bestimmte, aussagekräftige Registerkarten Bezeichnungen.** Vermeiden Sie generische Registerkarten Bezeichnungen, die auf eine beliebige Registerkarte (z. b. Allgemein, erweitert oder Einstellungen) angewendet werden können.
-   **Horizontale Registerkarten verwenden, wenn:**
    -   Das Eigenschaften Fenster enthält sieben oder weniger Registerkarten (einschließlich Erweiterungen von Drittanbietern).
    -   **Alle Registerkarten passen in eine Zeile, auch wenn die Benutzeroberfläche lokalisiert ist.**
    -   Sie verwenden horizontale Registerkarten für die anderen Eigenschaften Fenster in der Anwendung.
-   **Vertikale Registerkarten verwenden, wenn:**

    -   Das Eigenschaften Fenster verfügt über acht oder mehr Registerkarten (einschließlich Erweiterungen von Drittanbietern).
    -   **Die Verwendung von horizontalen Registerkarten erfordert mehr als eine Zeile.**
    -   Sie verwenden vertikale Registerkarten für die anderen Eigenschaften Fenster in der Anwendung.

    ![Screenshot des Eigenschaften Fensters mit vertikalen Registerkarten ](images/win-property-win-image7.png)

    In diesem Beispiel werden vertikale Registerkarten verwendet, um acht oder mehr Registerkarten zu unterstützen.

-   **Verwenden Sie für Eigenschaften Inspektoren, um Speicherplatz zu sparen, eine Dropdown Liste anstelle von Registerkarten**, insbesondere dann, wenn die aktuelle Registerkarte selten vom Benutzer geändert wird.
-   **Wenn eine Registerkarte nicht auf den aktuellen Kontext angewendet wird und Benutzer dies nicht erwarten, entfernen Sie die Registerkarte.** Dies vereinfacht die Benutzeroberfläche, und Benutzer werden Sie nicht übersehen.

    **Falsch:**

    ![Screenshot der Registerkarte für Abbild Speicherorte ](images/win-property-win-image8.png)

    In diesem Beispiel ist die Registerkarte Dateispeicher Orte falsch deaktiviert, wenn Microsoft Word 2003 als e-Mail-Editor verwendet wird. Die Seite sollte entfernt werden, da Benutzer nicht erwarten, Dateispeicher Orte in diesem Kontext anzuzeigen oder zu ändern.

-   **Wenn eine Registerkarte nicht für den aktuellen Kontext gilt und die Benutzer möglicherweise Folgendes erwarten:**

    -   **Zeigen Sie die Registerkarte an.**
    -   **Deaktivieren Sie die Steuerelemente auf der Seite.**
    -   **Schließt Text ein, der erklärt, warum die Steuerelemente deaktiviert sind.**

    Deaktivieren Sie die Registerkarte nicht, da dies nicht selbsterklärend ist und die Untersuchung untersagt. Außerdem würden Benutzer, die nach einer bestimmten Eigenschaft suchen, gezwungen sein, auf allen anderen Registerkarten zu suchen.

    ![Screenshot der Abbild-Steuerelemente ](images/win-property-win-image9.png)

    In diesem Beispiel aus Word 2003 gilt keine der Ansichtsoptionen beim Lesen des Layouts. Benutzer erwarten jedoch möglicherweise, dass Sie auf Grundlage der Registerkarten Bezeichnung angewendet werden, sodass die Seite angezeigt wird, aber die Optionen deaktiviert sind.

-   **Weisen Sie den Wechsel von Registerkarten keine Auswirkungen zu.** Das Ändern der aktuellen Registerkarte darf keine Nebeneffekte haben, Einstellungen anwenden oder zu einer Fehlermeldung führen.
-   **Schachteln Sie keine Registerkarten, oder kombinieren Sie keine horizontalen Registerkarten mit vertikalen** Reduzieren Sie stattdessen die Anzahl der Registerkarten, verwenden Sie nur vertikale Registerkarten, oder verwenden Sie ein anderes Steuerelement, z. b. eine Dropdown Liste.
-   **Verwenden Sie keine Registerkarten, wenn ein Eigenschaften Fenster nur eine einzige Registerkarte hat und nicht erweiterbar ist.** Verwenden Sie stattdessen ein reguläres Dialogfeld mit OK, Abbrechen und einer optionalen Schaltfläche anwenden. Erweiterbare Eigenschaften Fenster (die von Drittanbietern erweitert werden können) müssen immer Registerkarten verwenden.
-   **Fügen Sie Symbole nicht auf Registerkarten ein.** Symbole fügen in der Regel unnötige visuelle Übersichtlichkeit hinzu, verbrauchen Bildschirmfläche und verbessern das Benutzer Verständnis häufig nicht. Fügen Sie nur Symbole hinzu, die das Verständnis unterstützen, z. b. Standardsymbole.

    **Falsch:**

    ![Screenshot von Registerkarten Bezeichnungen mit Symbolen ](images/win-property-win-image10.png)

    In diesem Beispiel fügen die Grafiken unnötige visuelle Übersichtlichkeit hinzu und führen wenig aus, um das Benutzer Verständnis zu verbessern.

-   **Verwenden Sie keine Produktlogos für Registerkarten Grafiken.** Registerkarten sind nicht zum Branding.
-   **Scrollen Sie nicht in horizontalen Registerkarten.** Horizontales Scrollen ist nicht leicht erkennbar. Sie können jedoch auf vertikalen Registerkarten scrollen.

    **Falsch:**

    ![Screenshot der abgeschnittene horizontalen Registerkarten Bezeichnung ](images/win-property-win-image11.png)

    In diesem Beispiel werden auf den horizontalen Registerkarten ein Rollup ausgeführt.

### <a name="command-buttons"></a>Befehls Schaltflächen

-   **Platzieren Sie Befehls Schaltflächen, die für alle Eigenschaften Seiten am unteren Rand des Eigenschaften Fensters gelten.** Richten Sie die Schaltflächen rechtsbündig aus, und verwenden Sie diese Reihenfolge (von links nach rechts): OK, Abbrechen und anwenden.
-   **Platzieren Sie Befehls Schaltflächen, die nur auf einzelne Eigenschaften Seiten direkt auf der Eigenschaften Seite angewendet werden.**

### <a name="commit-buttons"></a>Commit-Schaltflächen

**OK-Schaltflächen**

-   **Für Besitzer Eigenschaften Fenster bedeutet die Schaltfläche OK, dass die ausstehenden Änderungen (seit dem Öffnen des Fensters oder das letzte anwenden) angewendet werden, und das Fenster wird geschlossen.**
-   **Bei besitzenden Eigenschaften Fenstern bedeutet die Schaltfläche OK, die Änderungen beizubehalten, das Fenster zu schließen und die Änderungen zu übernehmen, wenn die Änderungen des Besitzer Fensters angewendet werden.**
-   **Benennen Sie die Schaltfläche OK nicht um.** Im Gegensatz zu anderen Dialogfeldern werden Eigenschaften Fenster nicht verwendet, um eine bestimmte Aufgabe auszuführen. Wenn es sinnvoll ist, die Schaltfläche "OK" umzubenennen (z. b. zum Drucken), ist das Fenster kein Eigenschaften Fenster.
-   **Weisen Sie keinen Zugriffsschlüssel zu.**

**Schaltflächen Abbrechen**

-   **Mit der Schaltfläche Abbrechen können Sie alle ausstehenden Änderungen verwerfen (seit dem Öffnen des Fensters oder der letzten Anwendung) und das Fenster schließen.**
-   **Wenn alle ausstehenden Änderungen nicht abgebrochen werden können, benennen Sie die Schaltfläche Abbrechen in close um.** Durch Klicken auf Abbrechen müssen alle ausstehenden Änderungen verworfen werden.
-   **Wenn das besitzende Eigenschaften Fenster einen sofortigen Commit erfordert, benennen Sie die Schaltfläche Abbrechen im Fenster Besitzer um, um anzuzeigen, dass für die Änderungen ein Commit ausgeführt wurde.**
-   **Weisen Sie keinen Zugriffsschlüssel zu.**

**Schaltflächen anwenden**

-   **Die Schaltfläche anwenden bedeutet, dass die Schaltfläche übernehmen die ausstehenden Änderungen anwendet (seit dem Öffnen oder letzten Anwenden des Fensters vorgenommen), das Fenster aber geöffnet lassen.** Auf diese Weise können Benutzer die Änderungen auswerten, bevor Sie das Eigenschaften Blatt schließen.
-   **Verwenden Sie für Eigenschafts Blätter im Besitz von nicht.** Wenn Sie die Schaltfläche übernehmen auf einem eigenen Eigenschaften Blatt verwenden, ist die Bedeutung der Commit-Schaltflächen auf dem Eigenschaften Blatt "Besitzer" schwer zu verstehen.
-   **Geben Sie nur dann eine Apply-Schaltfläche an, wenn das Eigenschaften Blatt über Einstellungen (mindestens eine) mit Effekten verfügt, die Benutzer auf sinnvolle Weise auswerten können.** Normalerweise werden Schaltflächen anwenden verwendet, wenn Einstellungen sichtbare Änderungen vornehmen. Benutzer sollten in der Lage sein, eine Änderung anzuwenden, die Änderung zu evaluieren und auf der Grundlage dieser Auswertung weitere Änderungen vorzunehmen. Wenn dies nicht der Fall ist, entfernen Sie die Schaltfläche anwenden, anstatt Sie zu deaktivieren.

    **Falsch:**

    ![Screenshot der Systemeigenschaften mit der Schaltfläche "anwenden" ](images/win-property-win-image12.png)

    In diesem Beispiel hat keine der Systemeigenschaften einen visuellen Effekt, sodass die Schaltfläche anwenden keinen Wert hat und entfernt werden sollte.

-   **Legen Sie alle Einstellungen fest, die Benutzer möglicherweise auf Besitzer Seiten anwenden möchten.** Verwenden Sie die Schaltflächen anwenden nicht für eigene Eigenschaften Blätter, da dies verwirrend ist.
-   **Verwenden Sie die Schaltflächen anwenden nur für Eigenschaften Blätter, nicht für Dialogfelder für Optionen.**
-   **Aktivieren Sie die Schaltfläche Anwenden nur, wenn ausstehende Änderungen vorhanden sind**. Andernfalls deaktivieren Sie Sie.
-   **Weisen Sie als Zugriffsschlüssel "A" zu.**

**Schließen von Schaltflächen**

-   **Wenn alle ausstehenden Änderungen nicht abgebrochen werden können, benennen Sie die Schaltfläche Abbrechen in close um.** Durch Klicken auf Abbrechen müssen alle ausstehenden Änderungen verworfen werden.
-   **Vergewissern Sie sich nicht, dass Benutzer Ihre Änderungen verwerfen.**
    -   **Ausnahme:** Wenn das Eigenschaften Fenster Einstellungen enthält, für die ein erheblicher Aufwand erforderlich ist, und der Benutzer Änderungen vorgenommen hat, können Sie eine [Bestätigung](mess-confirm.md) anzeigen, wenn der Benutzer auf der Titelleiste auf die Schaltfläche Schließen klickt. Der Grund hierfür ist, dass einige Benutzer versehentlich davon ausgehen, dass die Schaltfläche Schließen auf der Titelleiste dieselbe Auswirkung hat wie die Schaltfläche OK.
-   **Mit Ausnahme der Bestätigungsmeldung müssen Sie sicherstellen, dass die Schaltfläche Schließen auf der Titelleiste dieselbe Auswirkung wie abbrechen oder schließen hat.**

### <a name="page-contents"></a>Seiten Inhalt

-   **Stellen Sie sicher, dass die Eigenschaften erforderlich sind.** Überladen Sie Ihre Seiten nicht mit unnötigen Eigenschaften, um zu vermeiden, dass Sie harte Entwurfsentscheidungen treffen.
-   **Präsentieren von Eigenschaften in Bezug auf die Benutzer Ziele, nicht auf die Technologie.** Nur weil eine Eigenschaft eine bestimmte Technologie konfiguriert, bedeutet das nicht, dass Sie die Eigenschaft in Bezug auf diese Technologie darstellen müssen.
    -   Wenn Sie Einstellungen in Bezug auf die Technologie darstellen müssen (möglicherweise, weil Ihre Benutzer den Namen der Technologie erkennen), sollten Sie eine kurze Beschreibung der Vorteile dieser Einstellung angeben.
-   **Stellen Sie die Eigenschaften auf der rechten Ebene dar.** Sie müssen auf einer Eigenschaften Seite keine einzelnen Einstellungen auf niedriger Ebene präsentieren. Stellen Sie daher die Eigenschaften auf einer Ebene dar, die für die Benutzer sinnvoll ist.
-   **Entwerfen von Eigenschaften Seiten für bestimmte Aufgaben.** Bestimmen Sie die Aufgaben, die Benutzer ausführen werden, und stellen Sie sicher, dass ein eindeutiger Pfad vorhanden ist, um diese Aufgaben auszuführen.
-   **Organisieren Sie Eigenschaften Seiten effizient** , indem Sie die Anzahl der Registerkarten verringern, die Entscheidung, was auf einer Seite basiert, basierend auf der logischen Gruppierung und Kohärenz treffen und die Darstellung der Seite vereinfachen.

<!-- -->

-   **Wenn eine Option dringend empfohlen wird, sollten Sie "(empfohlen)" der Bezeichnung hinzufügen.**
-   **Geben Sie die Befehls Schaltfläche Standardwerte wiederherstellen für eine Eigenschaften Seite oder das gesamte Eigenschaften Fenster an, wenn:**

    -   Ihre Benutzer sind wahrscheinlich auf die Einstellungen komplex und schwer zu verstehen.
    -   Falsche Einstellungen können zu einer Unterbrechung der Funktionalität führen, aber die Standardeinstellungen stellen die Funktionalität wieder her.
    -   Es ist einfacher, die Benutzer zu starten, wenn das Objekt falsch konfiguriert ist.

    ![Screenshot der Registerkarte mit Schaltfläche "Standard wiederherstellen" ](images/win-property-win-image13.png)

    In diesem Beispiel sind die Windows-Firewall-Einstellungen komplex und können zu einer unterbrochenen Funktionalität führen. Wenn ein Problem vorliegt, ist es für Benutzer häufig einfacher, zu beginnen, indem Sie auf Standardwerte wiederherstellen klicken.

-   Bestätigen Sie den Befehl "Standard wiederherstellen", wenn der Effekt nicht offensichtlich ist oder die Einstellungen komplex sind. Geben Sie die Bestätigung mithilfe von [Ellipsen](ctrl-command-buttons.md)an.
-   **Wenn dies der Fall ist, zeigen Sie eine Vorschau der Ergebnisse einer Einstellung an.**

    ![Screenshot der Maus Eigenschaften-Zeiger Beispiele ](images/win-property-win-image14.png)

    In diesem Beispiel wird auf der Seite eine Vorschau der Zeiger Schemas angezeigt. Wenn Sie auf "anwenden" klicken, wird auch eine Vorschau angezeigt, eine Vorschau auf der Seite ist für Benutzer effizienter.

    ![Screenshot der Vorschau der Ergebnisse der Schriftart Einstellungen ](images/win-property-win-image15.png)

    In diesem Beispiel zeigt das Vorschaufeld die Ergebnisse der Schriftart Einstellungen an. Dieses Beispiel zeigt, dass Sie Vorschau Einstellungen anzeigen können, die nicht grafisch sind.

### <a name="help"></a>Hilfe

-   Wenn Sie Benutzerunterstützung bereitstellen, **sollten Sie die folgenden Optionen verwenden** (in Ihrer bevorzugten Reihenfolge aufgelistet):
    -   Teilen Sie den interaktiven Steuerelementen selbsterklärende Bezeichnungen mit. Benutzer sind eher mit der Wahrscheinlichkeit vertraut, dass Sie die Bezeichnungen für interaktive Steuerelemente lesen als bei anderen Text.
    -   Stellen Sie mithilfe statischer Text Bezeichnungen Kontext gesteuerte Erläuterungen bereit.
    -   Geben Sie einen bestimmten [Link](ctrl-links.md) zu einem relevanten Hilfethema an.
-   **Suchen Sie Links unten auf jeder Seite nach Hilfe Links.** Wenn eine Seite über mehrere unterschiedliche Gruppen von Einstellungen mit einem Hilfethema (z. b. innerhalb von Gruppen Feldern) verfügt, finden Sie den Hilfelink unten in der Gruppe.
-   **Verwenden Sie keine allgemeinen oder ungenauen Hilfe Themen Links oder allgemeine Hilfe Schaltflächen.** Benutzer ignorieren häufig die generische Hilfe.

Weitere Informationen und Beispiele finden Sie in der [Hilfe](winenv-help.md).

### <a name="standard-users-and-protected-administrators"></a>Standard Benutzer und geschützte Administratoren

**Viele Einstellungen erfordern Administratorrechte, damit Sie geändert werden können.** Wenn ein Prozess Administratorrechte erfordert, erfordert Windows und höher, dass [Standard Benutzer](glossary.md) und [geschützte Administratoren](glossary.md) Ihre Berechtigungen explizit erhöhen. Dadurch wird verhindert, dass bösartiger Code mit Administratorrechten ausgeführt wird.

Weitere Informationen und Beispiele finden Sie unter [Benutzerkontensteuerung](winenv-uac.md).

### <a name="default-values"></a>Standardwerte

-   **Die Einstellungen innerhalb eines Eigenschaften Fensters müssen den aktuellen Status der Anwendung, des Objekts oder der Sammlung von Objekten widerspiegeln.** Andernfalls wäre es irreführend, was zu unerwünschten Ergebnissen führen könnte. Wenn die Einstellungen z. b. die Empfehlungen, aber nicht den aktuellen Status widerspiegeln, können Benutzer auf Abbrechen klicken, anstatt Änderungen vorzunehmen, und denken Sie daran, dass keine Änderungen erforderlich sind.
-   **Wählen Sie den sichersten (um den Verlust von Daten oder den System Zugriff zu verhindern) und den sichersten Anfangszustand.** Nehmen Sie an, dass die meisten Benutzer die Einstellungen nicht ändern.
-   **Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie den anfänglichen Status aus, der höchstwahrscheinlich oder praktisch ist.**

## <a name="text"></a>Text

### <a name="commands"></a>Befehle

-   Verwenden Sie zum Anzeigen der Programmoptionen "Optionen".
-   Um das Eigenschaften Fenster eines Objekts anzuzeigen, verwenden Sie "Properties".
-   Verwenden Sie "[personalisieren](glossary.md)", um eine Zusammenfassung der häufig verwendeten Programm Anpassungs Einstellungen anzuzeigen.
-   Verwenden Sie nicht "Einstellungen" oder "Einstellungen".
-   Verwenden Sie für diese Befehle keine [Ellipsen](ctrl-command-buttons.md) .

### <a name="property-sheet-titles"></a>Eigenschaften Blatt Titel

-   Verwenden Sie für ein einzelnes Objekt " \[ Eigenschaften von Objektnamen \] ".
    -   Wenn das Objekt keinen Namen hat, verwenden Sie den Typnamen des Objekts. (Z. b. Benutzerkonto Eigenschaften.)
-   Verwenden Sie für mehrere Objekte " \[ erster Objektname \] ,... Eigenschaften. "
    -   Wenn die Objekte keine Namen haben, verwenden Sie den Typnamen des Objekts. (Z. b. Eigenschaften von Benutzerkonten.)
    -   Wenn die Objekte unterschiedliche Typen aufweisen, verwenden Sie "Auswahl Eigenschaften".
-   Verwenden Sie die groß [-](glossary.md)/Kleinschreibung.
-   Verwenden Sie keine Interpunktion am Ende.
-   Verwenden Sie keine Bindestriche, wie z \[ . b. "Objektname \] -Eigenschaften".

### <a name="property-inspector-titles"></a>Titel der Eigenschaften Inspektor

-   Verwenden Sie "Properties".
-   Verwenden Sie die Groß-/Kleinschreibung.
-   Verwenden Sie keine Interpunktion am Ende.

### <a name="options-dialog-box-titles"></a>Titel des Dialog Felds "Optionen"

-   Verwenden Sie "Optionen".
-   Verwenden Sie die Groß-/Kleinschreibung.
-   Verwenden Sie keine Interpunktion am Ende.

### <a name="property-page-tab-names"></a>Registerkarten Namen der Eigenschaften Seite

-   **Verwenden Sie präzise Registerkarten Bezeichnungen.** Verwenden Sie ein oder zwei Wörter, die den Inhalt der Seite eindeutig beschreiben. Die Verwendung längerer Registerkarten Namen führt zu einer ineffizienten Verwendung des Bildschirm Raums, insbesondere dann, wenn die Registerkarten Namen lokalisiert sind.
-   **Verwenden Sie bestimmte, aussagekräftige Registerkarten Bezeichnungen.** Vermeiden Sie generische Registerkarten Bezeichnungen, die auf eine beliebige Registerkarte (z. b. Allgemein, erweitert oder Einstellungen) angewendet werden können.
-   Schreiben Sie die Bezeichnung als ein-oder zwei-Wort-Ausdruck, und verwenden Sie keine endinterpunktions Zeichen.
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Weisen Sie keinen eindeutigen [Zugriffsschlüssel](glossary.md)zu.

### <a name="property-page-text"></a>Text der Eigenschaften Seite

-   Vermeiden Sie große Textblöcke.
-   Geben Sie ausreichend Platz für den Text ein, um 30 Prozent zu erweitern, wenn er lokalisiert wird.
-   Verwenden Sie keinen Text, der als Befehl in den Eigenschaften Fenstern formuliert ist. Da Benutzer die Einstellungen möglicherweise einfach anzeigen möchten, möchten Sie Sie nicht zum Ändern der Einstellungen auffordern.
-   Verwenden Sie die Groß-und Kleinschreibung im Satz Stil.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Eigenschaften Fenster:

-   Informationen zum Programmieren und zur anderen technischen Dokumentation finden Sie in den Dialogfeldern Eigenschaften Blätter und Optionen als Eigenschaften Blätter. Verwenden Sie in jedem anderen Dialogfeld, insbesondere in der Benutzerdokumentation.
-   Verwenden Sie den genauen Titeltext, einschließlich der Groß-/Kleinschreibung.
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie öffnen und schließen.
-   Formatieren Sie den Titel nach Möglichkeit mithilfe von fettem Text. Andernfalls sollten Sie den Titel nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beim Verweisen auf Eigenschaften Seiten:

-   Informationen zu den Eigenschaften Seiten finden Sie unter Programmieren und andere technische Dokumentation. Verwenden Sie die Tab-Taste, insbesondere in der Benutzerdokumentation.
-   Verwenden Sie den genauen Titeltext, einschließlich der Groß-/Kleinschreibung.
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie klicken Sie, um auf eine Registerkarte zu verweisen.
-   Formatieren Sie den Namen, wenn möglich, mit fett formatiertem Text. Andernfalls sollten Sie den Namen nur dann in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

 

 