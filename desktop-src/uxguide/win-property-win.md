---
title: Eigenschaften-Windows
description: Das Eigenschaftenfenster ist der gemeinsame Name für die folgenden Typen von Benutzeroberflächen (User Interfaces, UIs), die zum Anzeigen und Ändern von Eigenschaften für ein Objekt oder eine Auflistung von Objekten in einem Dialogfeld verwendet werden. Eigenschafteninspektor zum Anzeigen und Ändern von Eigenschaften für ein Objekt oder eine Auflistung von Objekten in einem Bereich. Dialogfeld "Optionen", das zum Anzeigen und Ändern von Optionen für eine Anwendung verwendet wird.
ms.assetid: 18fc04da-9f84-4a44-9f3d-a9e29b121e7c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 73260459c1dc22ee488233f3c7edebe25203a811a430870fdd4e68e1c2e153ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594385"
---
# <a name="property-windows"></a>Eigenschaften-Windows

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Das Eigenschaftenfenster ist der gemeinsame Name für die folgenden Arten von Benutzeroberflächen (User Interfaces, UIs):

-   Eigenschaftenblatt: Dient zum **Anzeigen und Ändern von Eigenschaften für ein Objekt oder eine Auflistung von Objekten in einem Dialogfeld.**
-   Eigenschafteninspektor: Dient zum **Anzeigen und Ändern von Eigenschaften für ein Objekt oder eine Auflistung von Objekten in einem Bereich.**
-   Dialogfeld "Optionen": Dient zum **Anzeigen und Ändern von Optionen für eine Anwendung.**

Eine Eigenschaft für ein -Objekt ist eine der folgenden:

-   Eine Einstellung, die Benutzer ändern können (z. B. den Namen einer Datei und das schreibgeschützte Attribut).
-   Ein Attribut eines Objekts, das Benutzer nicht direkt ändern können (z. B. Größe und Erstellungsdatum einer Datei).

Im Gegensatz zu Dialogfeldern (mit Ausnahme von Optionsdialogfeldern) und Assistenten unterstützen Eigenschaftenfenster in der Regel mehrere Aufgaben anstelle einer einzelnen Aufgabe.

Eigenschaftenfenster sind in der Regel in Seiten organisiert, auf die über Registerkarten zugegriffen wird. Eigenschaftenfenster werden häufig Registerkarten zugeordnet (und umgekehrt), aber **Registerkarten sind für Eigenschaftenfenster nicht wichtig.**

![Screenshot des Eigenschaftenblatts für Dokumenteigenschaften ](images/win-property-win-image1.png)

Ein typisches Eigenschaftenblatt.

**Hinweis:** Richtlinien im Zusammenhang mit [Layout](vis-layout.md) und [Registerkarten](ctrl-tabs.md) werden in separaten Artikeln vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Erfordert das Festlegen der Eigenschaften, dass Benutzer eine feste, nicht triviale Abfolge von Schritten ausführen?** Verwenden Sie in diesem Falle stattdessen einen [Assistenten](win-wizards.md) oder [Einen Taskflow.](glossary.md)
-   **Handelt es sich bei dem Inhalt ausschließlich um die Optionen einer Anwendung?** Verwenden Sie in diesem Falle ein Optionsdialogfeld.
-   **Handelt es sich bei dem Inhalt ausschließlich um die Attribute einer Anwendung?** Wenn ja, verwenden Sie das [Feld "About".](glossary.md)
-   **Handelt es sich bei dem Inhalt hauptsächlich um die Eigenschaften eines Objekts (einstellungen oder Attribute)?** Falls nicht, verwenden Sie ein [Standarddialogfeld](win-dialog-box.md) oder ein [Dialogfeld im Registerkartenbett.](glossary.md)
-   Können Benutzer **Eigenschaften häufig oder über einen längeren Zeitraum anzeigen oder ändern?** Verwenden Sie in diesem Falle einen Eigenschafteninspektor. Verwenden Sie andernfalls ein Eigenschaftenblatt.
-   Sind Benutzer **wahrscheinlich gleichzeitig in der Lage, Eigenschaften für mehrere verschiedene Objekte anzuzeigen oder zu ändern?** Verwenden Sie in diesem Falle einen Eigenschafteninspektor. Verwenden Sie andernfalls ein Eigenschaftenblatt.

**Eigenschaftenblätter und Eigenschafteninspektoren sind nicht exklusiv.** Sie können die eigenschaften, auf die am häufigsten zugegriffen wird, in einem Eigenschafteninspektor und den vollständigen Satz im Eigenschaftenblatt anzeigen.

## <a name="design-concepts"></a>Entwurfskonzepte

**Eigenschaftenfenster werden häufig zu einem Boden für eine ungerade Auswahl von low-level, technologiebasierten Einstellungen.** Zu oft sind diese Eigenschaften in Registerkarten organisiert, aber darüber hinaus nicht für bestimmte Aufgaben oder Benutzer konzipiert. Wenn Benutzer mit einer Aufgabe in einem Eigenschaftenfenster konfrontiert werden, wissen sie daher häufig nicht, was zu tun ist.

Führen Sie die folgenden Schritte aus, um sicherzustellen, dass Ihre Eigenschaftenfenster nützlich und verwendbar sind:

-   Stellen Sie sicher, dass die Eigenschaften erforderlich sind.
-   Stellen Sie Eigenschaften im Hinblick auf Benutzerziele dar, nicht auf Technologie.
-   Zeigen Sie Eigenschaften auf der richtigen Ebene an.
-   Entwurfsseiten für bestimmte Aufgaben.
-   Entwurfsseiten für bestimmte Benutzer, insbesondere eingeschränkte Benutzer (Nichtadministratoren).
-   Organisieren Sie die Eigenschaftenseiten effizient.

**Wenn Sie nur eine Sache durchführen...**

Stellen Sie Eigenschaften im Hinblick auf Benutzerziele dar, nicht auf Technologie. Geben Sie an, dass Sie die Eigenschaft erklären und warum sie für einen Freund nützlich ist. Wie würden Sie dies erklären? Welche Sprache würden Sie verwenden? Dies ist die Sprache, die auf Ihren Eigenschaftenseiten verwendet werden soll.

## <a name="usage-patterns"></a>Verwendungsmuster

Eigenschaftenfenster weisen mehrere Verwendungsmuster auf.

-   Eigenschaftenblätter. Eigenschaften für ein einzelnes Objekt werden in einem moduslosen Dialogfeld angezeigt.
-   Eigenschaftenblätter mit mehreren Objekten. Eigenschaften für mehrere Objekte werden in einem moduslosen Dialogfeld angezeigt.
-   Eigenschaftenblätter für effektive Einstellungen. Die effektiven Eigenschaften für ein einzelnes Objekt werden in einem moduslosen Dialogfeld angezeigt.
-   Dialogfelder "Optionen". Eigenschaften für eine Anwendung werden in einem modalen Dialogfeld angezeigt.
-   Eigenschafteninspektoren. Eigenschaften für die aktuelle Auswahl (ein einzelnes Objekt oder eine Gruppe von Objekten) werden in einem moduslosen Fensterbereich oder abgedockten Fenster angezeigt.

Alle Eigenschaftenfenstermuster mit Ausnahme von Eigenschafteninspektoren verwenden einen verzögerten Commit, was bedeutet, dass Änderungen nur wirksam werden, wenn Benutzer auf OK oder Übernehmen klicken. Eigenschafteninspektoren verwenden einen sofortigen Commit (Eigenschaften werden geändert, sobald Benutzer Änderungen vornehmen), sodass die Schaltflächen OK, Abbrechen und Übernehmen nicht erforderlich sind.

## <a name="guidelines"></a>Richtlinien

### <a name="property-sheets"></a>Eigenschaftenblätter

-   **Anzeigen eines Eigenschaftenblatts, wenn Benutzer:**
    -   Wählen Sie den Befehl Eigenschaften für ein Objekt aus.
    -   Legen Sie den Eingabefokus auf ein Objekt fest, und drücken Sie ALT+EINGABETASTE.

**Eigenschaftenblätter mit mehreren Objekten**

-   **Zeigen Sie die allgemeinen Eigenschaften aller ausgewählten Objekte an.** Wenn sich die Eigenschaftswerte unterscheiden, zeigen Sie die diesen Werten zugeordneten Steuerelemente in einem gemischten Zustand an. (Informationen zur Verwendung von Werten mit gemischten Zuständen finden Sie in den jeweiligen Steuerelementrichtlinien.)
-   Wenn das ausgewählte Objekt eine Auflistung mehrerer diskreter Objekte (z. B. ein Dateiordner) ist, **zeigen Sie die Eigenschaften des einzelnen gruppierten Objekts anstelle eines Eigenschaftenblatts mit mehreren Objekten für die diskreten Objekte an.**

### <a name="options-dialog-boxes"></a>Dialogfelder "Optionen"

-   **Trennen Sie Die Optionen nicht von der Anpassung.** Das heißt, sie verfügen nicht über einen Options- und einen Customize-Befehl. Benutzer werden häufig durch diese Trennung verwechselt. Greifen Sie stattdessen über Optionen auf die Anpassung zu.

### <a name="property-pages"></a>Eigenschaftenseiten

-   **Befolgen Sie die folgenden Richtlinien für die Seitenreihenfolge:**
    -   Machen Sie die Seite Allgemein oder deren Entsprechung zur ersten Seite.
    -   Machen Sie die Seite Erweitert oder deren Entsprechung zur letzten Seite.
    -   Für die verbleibenden Seiten:
        -   Organisieren Sie sie in Gruppen verwandter Seiten.
        -   Ordnen Sie die Gruppen nach der Wahrscheinlichkeit ihrer Nutzung an.
        -   Ordnen Sie die Seiten innerhalb jeder Gruppe entweder nach ihren Beziehungen oder nach der Wahrscheinlichkeit ihrer Verwendung an.
        -   Sie sollten nicht so viele Seiten haben, dass sie in alphabetischer Reihenfolge angezeigt werden müssen.
-   **Machen Sie Seiten zusammenhängend, indem Sie alle Eigenschaften auf jeder Seite mit einem einzelnen, spezifischen, aufgabenbasierten Zweck in Beziehung setzen.**
-   **Wenn Speicherplatz zulässt, erläutern Sie den Zweck des Eigenschaftenfensters am oberen Rand der Seite, wenn es für Ihre Zielbenutzer nicht offensichtlich ist.** Wenn die Seite nur zum Ausführen einer einzelnen Aufgabe verwendet wird, **formulieren Sie den Text als klare Anweisung zum Ausführen dieser Aufgabe.** Verwenden Sie vollständige Sätze, die mit einem Punkt enden.

    ![Screenshot des Eigenschaftenblatts der Firewall ](images/win-property-win-image2.png)

    In diesem Beispiel wird der Zweck von Microsoft Windows Firewall oben auf der Seite Allgemein erläutert.

-   **Machen Sie ähnliche Inhalte seitenübergreifend konsistent, indem Sie konsistente Steuerelementnamen und Speicherorte verwenden.** Wenn z. B. mehrere Seiten Namensfelder enthalten, versuchen Sie, sie an derselben Stelle auf der Seite zu platzieren und konsistente Bezeichnungen zu verwenden. Ähnliche Inhalte sollten nicht von Seite zu Seite springen.
-   **Platzieren Sie die gleiche Eigenschaft in der gesamten Anwendung auf derselben Seite.** Legen Sie beispielsweise keine Expiration-Eigenschaft auf der Registerkarte Allgemein für einen Objekttyp und auf der Registerkarte Erweitert für einen anderen Typ ab.
-   **Wenn Benutzer wahrscheinlich mit der letzten angezeigten Seite beginnen, lassen Sie die Registerkarte der Seite persistent, und wählen Sie sie standardmäßig aus.** Sorgen Sie dafür, dass die Einstellungen pro Eigenschaftsfenster pro Benutzer beibehalten werden. Wählen Sie andernfalls standardmäßig die erste Seite aus.
-   **Machen Sie die Einstellungen auf einer Seite nicht von den Einstellungen auf anderen Seiten abhängig.** Legen Sie die abhängigen Einstellungen stattdessen auf einer einzelnen Seite ab. Wenn Sie eine Einstellung auf einer Seite ändern, sollten die Einstellungen auf anderen Seiten niemals automatisch geändert werden.
    -   **Ausnahme:** Wenn sich die abhängigen Einstellungen in zwei verschiedenen Eigenschaftenfenstern befinden, verwenden Sie statische Textbeschriftungen, um diese Beziehung an beiden Stellen zu erklären.
-   **Scrollen Sie keine Eigenschaftenseiten.** Sowohl Registerkarten als auch Scrollleisten werden verwendet, um den effektiven Bereich eines Fensters zu erhöhen, aber ein Mechanismus sollte ausreichen. Anstatt Scrollleisten zu verwenden, vergrößern Sie die Eigenschaftenseiten, und legen Sie die Seiten effizient auf.

**Erste Seiten**

-   Legen Sie für Objekteigenschaften **den Namen des Objekts auf der ersten Seite fest.**
-   Wenn Sie Ihren Objekten (optional) [Symbole](vis-icons.md) zuordnen, **zeigen Sie das entsprechende Symbol in der oberen linken Ecke** der ersten Seite an.

**Allgemeine Seiten**

-   **Vermeiden Sie allgemeine Seiten.** Sie müssen keine Seite Allgemein haben. Verwenden Sie eine Seite Allgemein nur, wenn:
    -   Die Eigenschaften gelten für mehrere Aufgaben und sind für die meisten Benutzer von Bedeutung. Legen Sie keine spezialisierten oder erweiterten Eigenschaften auf einer Seite Allgemein ab, aber Sie können sie über eine Befehlsschaltfläche auf der Seite Allgemein zugänglich machen.
    -   Die Eigenschaften passen nicht zu einer spezifischeren Kategorie. Verwenden Sie in diesem Falle diesen Namen stattdessen für die Seite.

**Erweiterte Seiten**

-   **Vermeiden Sie Erweiterte Seiten.** Verwenden Sie eine Seite Erweitert nur, wenn:
    -   Die Eigenschaften gelten für ungewöhnliche Aufgaben und sind in erster Linie für fortgeschrittene Benutzer von Bedeutung.
    -   Die Eigenschaften passen nicht zu einer spezifischeren Kategorie. Verwenden Sie in diesem Falle diesen Namen stattdessen für die Seite.
-   **Rufen Sie eigenschaften nicht erweitert auf, die ausschließlich auf technologischen Measures basieren.** Beispielsweise kann eine Druckerstärkungsoption ein erweitertes Druckerfeature sein, aber sie ist für alle Benutzer sinnvoll, sodass sie sich nicht auf einer Erweitert-Seite befinden sollte.

### <a name="owned-property-windows"></a>Eigenschaftenfenster im Besitz

-   **Zeigen Sie nicht mehr als ein eigenschafteneigenes Eigenschaftenfenster in einem Eigenschaftenfenster an.** Das Anzeigen mehrerer Schaltflächen erschwert die Bedeutung der Schaltflächen OK und Abbrechen. Sie können bei Bedarf andere Arten von hilfsunterstunterstausgeberlichen Dialogfeldern (z. B. Objektauswahl) anzeigen.

    **Falsch:**

    ![Screenshot von drei eigenen Eigenschaftenfenstern ](images/win-property-win-image3.png)

    In diesem Beispiel weist das Dialogfeld Besitzeroptionen drei Ebenen von Eigenschaftenfenstern auf. Daher sind die Bedeutungen von OK und Abbrechen verwirrend.

-   Stellen Sie bei Eigenschaftenfenstern, die ein verzögertes Commitmodell verwenden, **sicher, dass Benutzer Änderungen in einem eigenschafteneigenen Fenster abbrechen können, indem Sie im Besitzerfenster auf Abbrechen klicken.**
-   Wenn für ein eigenschafteneigenes Fenster ein sofortiger Commit erforderlich ist, **geben Sie an, dass für Änderungen ein Commit ausgeführt wurde, indem Sie die Schaltfläche Abbrechen im Besitzerfenster in Schließen umbenennen.** Setzen Sie die Schaltfläche wieder auf Abbrechen zurück, wenn der Benutzer auf Übernehmen klickt.

    ![Screenshot des Eigenschaftenfensters mit "OK" und "Schließen" ](images/win-property-win-image4.png)

    In diesem Beispiel können Änderungen an benutzerdefinierten Wörterbüchern und Grammatikeinstellungen nicht abgebrochen werden. Sie können Benutzern dieses Feedback geben, indem Sie Abbrechen in Schließen ändern.

**Andere im Besitz befindliche Fenster**

-   Wenn ein eigenes Fenster zum Ausführen einer Hilfsaufgabe verwendet wird, **benennen Sie die Schaltfläche Abbrechen nicht um.** Die obigen Richtlinien gelten nur für eigenschafteneigene Fenster, nicht für Dialogfelder, die zum Ausführen zusätzlicher Aufgaben verwendet werden.

    ![Screenshot des Besitzerfensters und der Datenträgerbereinigung ](images/win-property-win-image5.png)

    In diesem Beispiel ist die Datenträgerbereinigung eine Hilfsaufgabe, daher gelten die vorherigen Richtlinien nicht. Beispielsweise sollte die Schaltfläche Abbrechen im Besitzerfenster nicht in Schließen geändert werden.

-   Wenn das eigene Fenster zum Ausführen einer Hilfsaufgabe verwendet wird, **schließen Sie das Besitzereigenschaftenfenster nicht, wenn auf die Befehlsschaltfläche geklickt wird.** Dies ist desorientierend und geht davon aus, dass der einzige Grund, aus dem der Benutzer das Eigenschaftenfenster angezeigt hat, die Ausführung dieses Befehls war.

    **Falsch:**

    ![Screenshot des Dialogfelds "Optionen" ](images/win-property-win-image6.png)

    Wenn Sie in diesem Beispiel auf **Dokument schützen** klicken, wird das Dialogfeld Optionen fälschlicherweise geschlossen.

### <a name="tabs"></a>Registerkarten

-   **Verwenden Sie präzise Registerkartenbezeichnungen.** Verwenden Sie ein oder zwei Wörter, die den Inhalt der Seite eindeutig beschreiben. Längere Bezeichnungen führen zu einer ineffizienten Verwendung des Bildschirmbereichs, insbesondere wenn die Bezeichnungen lokalisiert werden.
-   **Verwenden Sie bestimmte, aussagekräftige Registerkartenbezeichnungen.** Vermeiden Sie generische Registerkartenbezeichnungen, die auf alle Registerkarten angewendet werden können, z. B. Allgemein, Erweitert oder Einstellungen.
-   **Verwenden Sie horizontale Registerkarten, wenn:**
    -   Das Eigenschaftenfenster verfügt über sieben oder weniger Registerkarten (einschließlich erweiterungen von Drittanbietern).
    -   **Alle Registerkarten passen in eine Zeile, auch wenn die Benutzeroberfläche lokalisiert ist.**
    -   Sie verwenden horizontale Registerkarten in den anderen Eigenschaftenfenstern in Ihrer Anwendung.
-   **Verwenden Sie vertikale Registerkarten, wenn:**

    -   Das Eigenschaftenfenster verfügt über acht oder mehr Registerkarten (einschließlich erweiterungen von Drittanbietern).
    -   **Die Verwendung horizontaler Registerkarten würde mehr als eine Zeile erfordern.**
    -   Sie verwenden vertikale Registerkarten in den anderen Eigenschaftenfenstern in Ihrer Anwendung.

    ![Screenshot des Eigenschaftenfensters mit vertikalen Registerkarten ](images/win-property-win-image7.png)

    In diesem Beispiel werden vertikale Registerkarten verwendet, um acht oder mehr Registerkarten aufzunehmen.

-   **Um Platz zu sparen, sollten Sie für Eigenschafteninspektoren die Verwendung einer Dropdownliste anstelle von Registerkarten in Betracht ziehen,** insbesondere dann, wenn die aktuelle Registerkarte nur selten vom Benutzer geändert wird.
-   **Wenn eine Registerkarte nicht für den aktuellen Kontext gilt und Benutzer dies nicht erwarten, entfernen Sie die Registerkarte.** Dadurch wird die Benutzeroberfläche vereinfacht, und Benutzer werden sie nicht übersehen.

    **Falsch:**

    ![Screenshot der Registerkarte "Abgeblendete Dateispeicherorte" ](images/win-property-win-image8.png)

    In diesem Beispiel ist die Registerkarte Dateispeicherorte falsch deaktiviert, wenn Microsoft Word 2003 als E-Mail-Editor verwendet wird. Die Seite sollte entfernt werden, da Benutzer nicht erwarten würden, Dateispeicherorte in diesem Kontext anzuzeigen oder zu ändern.

-   **Wenn eine Registerkarte nicht für den aktuellen Kontext gilt und Benutzer dies möglicherweise erwarten:**

    -   **Zeigen Sie die Registerkarte an.**
    -   **Deaktivieren Sie die Steuerelemente auf der Seite.**
    -   **Fügen Sie Text ein, in dem erläutert wird, warum die Steuerelemente deaktiviert sind.**

    Deaktivieren Sie die Registerkarte nicht, da dies nicht selbsterklärend ist und das Erkunden verhindert. Darüber hinaus werden Benutzer, die nach einer bestimmten Eigenschaft suchen, gezwungen, auf allen anderen Registerkarten zu suchen.

    ![Screenshot von abgeblendeten Ansichtssteuerelementen ](images/win-property-win-image9.png)

    In diesem Beispiel aus Word 2003 gilt keine der Ansichtsoptionen im Leselayout. Benutzer erwarten jedoch möglicherweise, dass sie basierend auf der Registerkartenbezeichnung angewendet werden, sodass die Seite angezeigt wird, die Optionen jedoch deaktiviert sind.

-   **Weisen Sie änderungenden Registerkarten keine Effekte zu.** Das Ändern der aktuellen Registerkarte sollte niemals Nebeneffekte haben, Einstellungen anwenden oder zu einer Fehlermeldung führen.
-   **Schachteln Sie registerkarten nicht, oder kombinieren Sie horizontale Registerkarten nicht mit vertikalen Registerkarten.** Reduzieren Sie stattdessen die Anzahl der Registerkarten, verwenden Sie nur vertikale Registerkarten, oder verwenden Sie ein anderes Steuerelement, z. B. eine Dropdownliste.
-   **Verwenden Sie keine Registerkarten, wenn ein Eigenschaftenfenster nur über eine einzige Registerkarte verfügt und nicht erweiterbar ist.** Verwenden Sie stattdessen ein reguläres Dialogfeld mit OK, Abbrechen und einer optionalen Schaltfläche Anwenden. Erweiterbare Eigenschaftenfenster (die von Drittanbietern erweitert werden können) müssen immer Registerkarten verwenden.
-   **Legen Sie keine Symbole auf Registerkarten ab.** Symbole fügen in der Regel unnötige visuelle Überordnung hinzu, nutzen Bildschirmraum und verbessern häufig nicht das Benutzerverständnis. Fügen Sie nur Symbole hinzu, die das Verständnis unterstützen, z. B. Standardsymbole.

    **Falsch:**

    ![Screenshot von Registerkartenbezeichnungen mit Symbolen ](images/win-property-win-image10.png)

    In diesem Beispiel fügen die Grafiken unnötige visuelle Überordnung hinzu und tragen nur wenig zur Verbesserung des Benutzerverständnisses bei.

-   **Verwenden Sie keine Produktlogos für Registerkartengrafiken.** Registerkarten dienen nicht zum Branding.
-   **Scrollen Sie nicht auf horizontalen Registerkarten.** Horizontales Scrollen ist nicht leicht erkennbar. Sie können jedoch vertikale Registerkarten scrollen.

    **Falsch:**

    ![Screenshot der abgeschnittenen horizontalen Registerkartenbezeichnung ](images/win-property-win-image11.png)

    In diesem Beispiel werden die horizontalen Registerkarten gescrollt.

### <a name="command-buttons"></a>Befehlsschaltflächen

-   **Platzieren Sie Befehlsschaltflächen, die für alle Eigenschaftenseiten gelten, am unteren Rand des Eigenschaftenfensters.** Richten Sie die Schaltflächen rechts aus, und verwenden Sie diese Reihenfolge (von links nach rechts): OK, Abbrechen und Anwenden.
-   **Platzieren Sie Befehlsschaltflächen, die nur für einzelne Eigenschaftenseiten gelten, direkt auf der Eigenschaftenseite.**

### <a name="commit-buttons"></a>Commitschaltflächen

**OK-Schaltflächen**

-   **Bei Besitzereigenschaftsfenstern bedeutet die Schaltfläche OK, dass die ausstehenden Änderungen (seit dem Öffnen des Fensters oder des letzten Anwendens) angewendet und das Fenster geschlossen werden.**
-   **Bei Eigenschaftenfenstern im Besitz bedeutet die Schaltfläche OK, die Änderungen zu behalten, das Fenster zu schließen und die Änderungen anzuwenden, wenn die Änderungen des Besitzerfensters angewendet werden.**
-   **Benennen Sie die Schaltfläche OK nicht um.** Im Gegensatz zu anderen Dialogfeldern werden Eigenschaftenfenster nicht verwendet, um eine bestimmte Aufgabe auszuführen. Wenn es sinnvoll ist, die Schaltfläche OK umzubenennen (z. B. in Drucken), ist das Fenster kein Eigenschaftenfenster.
-   **Weisen Sie keinen Zugriffsschlüssel zu.**

**Schaltflächen "Abbrechen"**

-   **Die Schaltfläche Abbrechen bedeutet, dass alle ausstehenden Änderungen verworfen (seit dem Öffnen des Fensters oder dem letzten Anwenden) und das Fenster geschlossen werden.**
-   **Wenn alle ausstehenden Änderungen nicht abgebrochen werden können, benennen Sie die Schaltfläche Abbrechen in Schließen um.** Wenn Sie auf Abbrechen klicken, müssen alle ausstehenden Änderungen abgebrochen werden.
-   **Wenn für das Eigenschaftenfenster im Besitz ein sofortiger Commit erforderlich ist, benennen Sie die Schaltfläche Abbrechen im Besitzerfenster in Schließen um, um anzuzeigen, dass für die Änderungen ein Commit vorgenommen wurde.**
-   **Weisen Sie keinen Zugriffsschlüssel zu.**

**Schaltflächen anwenden**

-   **Für Besitzer-Eigenschaftenblätter bedeutet die Schaltfläche Übernehmen, dass die ausstehenden Änderungen (seit dem Öffnen des Fensters oder des letzten Anwendens) angewendet werden, aber das Fenster geöffnet lassen.** Auf diese Weise können Benutzer die Änderungen auswerten, bevor sie das Eigenschaftenblatt schließen.
-   **Verwenden Sie für Eigenschaftenblätter im Besitz nicht.** Die Verwendung einer Schaltfläche Anwenden auf einem Eigenschaftenblatt im Besitz macht die Bedeutung der Commitschaltflächen auf dem Eigenschaftenblatt des Besitzers schwer zu verstehen.
-   **Geben Sie nur dann eine Schaltfläche Anwenden an, wenn das Eigenschaftenblatt Über Einstellungen (mindestens eine) mit Effekten verfügt, die Benutzer sinnvoll auswerten können.** In der Regel werden Schaltflächen anwenden verwendet, wenn Einstellungen sichtbare Änderungen vornehmen. Benutzer sollten in der Lage sein, eine Änderung anzuwenden, die Änderung zu bewerten und weitere Änderungen basierend auf dieser Auswertung vorzunehmen. Wenn nicht, entfernen Sie die Schaltfläche Anwenden, anstatt sie zu deaktivieren.

    **Falsch:**

    ![Screenshot der Systemeigenschaften mit der Schaltfläche "Anwenden" ](images/win-property-win-image12.png)

    In diesem Beispiel hat keine der Systemeigenschaften einen visuellen Effekt, daher hat die Schaltfläche Anwenden keinen Wert und sollte entfernt werden.

-   **Platzieren Sie alle Einstellungen, die Benutzer möglicherweise anwenden möchten, auf Besitzerseiten.** Verwenden Sie keine Schaltflächen anwenden auf eigenschafteneigenen Eigenschaftenblättern, da dies verwirrend ist.
-   **Verwenden Sie Schaltflächen nur mit Eigenschaftenblättern anwenden, nicht mit Optionsdialogfeldern.**
-   **Aktivieren Sie die Schaltfläche Anwenden nur, wenn Änderungen ausstehen.** Andernfalls deaktivieren Sie es.
-   **Weisen Sie "A" als Zugriffsschlüssel zu.**

**Schaltflächen schließen**

-   **Wenn alle ausstehenden Änderungen nicht abgebrochen werden können, benennen Sie die Schaltfläche Abbrechen in Schließen um.** Wenn Sie auf Abbrechen klicken, müssen alle ausstehenden Änderungen abgebrochen werden.
-   **Bestätigen Sie nicht, ob Benutzer ihre Änderungen verwerfen.**
    -   **Ausnahme:** Wenn das Eigenschaftenfenster Einstellungen enthält, die einen erheblichen Aufwand erfordern, [](mess-confirm.md) und der Benutzer Änderungen vorgenommen hat, können Sie eine Bestätigung anzeigen, wenn der Benutzer auf der Titelleiste auf die Schaltfläche Schließen klickt. Der Grund dafür ist, dass einige Benutzer fälschlicherweise davon ausgehen, dass die Schaltfläche Schließen auf der Titelleiste die gleiche Wirkung wie die Schaltfläche OK hat.
-   **Stellen Sie mit Ausnahme der Bestätigungsmeldung sicher, dass die Schaltfläche Schließen auf der Titelleiste die gleiche Auswirkung wie Abbrechen oder Schließen hat.**

### <a name="page-contents"></a>Seiteninhalt

-   **Stellen Sie sicher, dass die Eigenschaften erforderlich sind.** Überladen Sie Ihre Seiten nicht mit unnötigen Eigenschaften, nur um schwierige Entwurfsentscheidungen zu vermeiden.
-   **Präsentieren Sie Eigenschaften in Bezug auf Benutzerziele, nicht auf Technologie.** Nur weil eine Eigenschaft eine bestimmte Technologie konfiguriert, bedeutet dies nicht, dass Sie die Eigenschaft in Bezug auf diese Technologie präsentieren müssen.
    -   Wenn Sie Einstellungen in Bezug auf die Technologie angeben müssen (möglicherweise weil Ihre Benutzer den Namen der Technologie erkennen), geben Sie eine kurze Beschreibung an, wie der Benutzer von dieser Einstellung profitiert.
-   **Präsentieren Sie Eigenschaften auf der rechten Ebene.** Sie müssen keine einzelnen Einstellungen auf niedriger Ebene auf einer Eigenschaftenseite anzeigen, daher müssen Sie die Eigenschaften auf einer Ebene präsentieren, die für Ihre Benutzer sinnvoll ist.
-   **Entwerfen Sie Eigenschaftenseiten für bestimmte Aufgaben.** Bestimmen Sie die Aufgaben, die Benutzer ausführen, und stellen Sie sicher, dass es einen eindeutigen Pfad zum Ausführen dieser Aufgaben gibt.
-   **Organisieren Sie Eigenschaftenseiten** effizient, indem Sie die Anzahl der Registerkarten reduzieren, entscheiden, was auf einer Seite basierend auf logischer Gruppierung und -unterführung passiert, und vereinfachen Sie die Darstellung der Seite.

<!-- -->

-   **Wenn eine Option dringend empfohlen wird, sollten Sie der Bezeichnung "(recommended)" hinzufügen.**
-   **Geben Sie die Befehlsschaltfläche Standardwerte wiederherstellen für eine Eigenschaftenseite oder das gesamte Eigenschaftenfenster an, wenn:**

    -   Ihre Benutzer werden die Einstellungen wahrscheinlich als komplex und schwer verständlich betrachten.
    -   Falsche Einstellungen können zu Funktionsausfällen führen, aber die Standardwerte können die Funktionalität wiederherstellen.
    -   Es ist einfacher für Benutzer, von vorn zu beginnen, wenn das Objekt falsch konfiguriert ist.

    ![Screenshot der Registerkarte mit Schaltfläche "Standardwerte wiederherstellen" ](images/win-property-win-image13.png)

    In diesem Beispiel sind die Windows Firewalleinstellungen komplex und können zu funktionsbrechenden Funktionen führen. Wenn ein Problem vor liegt, ist es für Benutzer oft einfacher, von vorn zu beginnen, indem sie auf Standardwerte wiederherstellen klicken.

-   Bestätigen Sie den Befehl Standardwerte wiederherstellen, wenn die Auswirkungen nicht offensichtlich sind oder die Einstellungen komplex sind. Geben Sie die Bestätigung mithilfe [von Ausellipsen an.](ctrl-command-buttons.md)
-   **Zeigen Sie gegebenenfalls eine Vorschau der Ergebnisse einer Einstellung an.**

    ![Screenshot der Zeigerbeispiele für Mauseigenschaften ](images/win-property-win-image14.png)

    In diesem Beispiel zeigt die Seite eine Vorschau der Zeigerschemas an. Wenn Sie auf Übernehmen klicken, wird auch eine Vorschau angezeigt, aber eine Vorschau auf der Seite ist für Benutzer effizienter.

    ![Screenshot der Vorschau der Ergebnisse der Schriftarteinstellungen ](images/win-property-win-image15.png)

    In diesem Beispiel werden im Feld Vorschau die Ergebnisse der Schriftarteinstellungen angezeigt. Dieses Beispiel zeigt, dass Sie eine Vorschau von Einstellungen anzeigen können, die nicht grafisch sind.

### <a name="help"></a>Hilfe

-   Wenn Sie Benutzerunterstützung bereitstellen, **sollten Sie die folgenden Optionen** verwenden (in ihrer Bevorzugten Reihenfolge aufgeführt):
    -   Geben Sie interaktiven Steuerelementen selbsterklärende Bezeichnungen. Benutzer lesen die Bezeichnungen wahrscheinlicher auf interaktiven Steuerelementen als jeder andere Text.
    -   Geben Sie Kontexterklärungen mit statischen Textbezeichnungen an.
    -   Geben Sie einen [bestimmten Link](ctrl-links.md) zu einem relevanten Hilfethema an.
-   **Suchen Sie unten auf jeder Seite nach Hilfelinks.** Wenn eine Seite über mehrere unterschiedliche Gruppen von Einstellungen verfügt, die über ein Hilfethema verfügen (z. B. in Gruppenfeldern), suchen Sie den Link Hilfe am unteren Rand der Gruppe.
-   **Verwenden Sie keine allgemeinen oder ungenauen Links zu Hilfethema oder generische Hilfeschaltflächen.** Benutzer ignorieren häufig die generische Hilfe.

Weitere Informationen und Beispiele finden Sie unter [Hilfe.](winenv-help.md)

### <a name="standard-users-and-protected-administrators"></a>Standardbenutzer und geschützte Administratoren

**Viele Einstellungen erfordern Administratorrechte, um sich zu ändern.** Wenn ein Prozess Administratorrechte erfordert, müssen Windows [](glossary.md) Standardbenutzer und [geschützte](glossary.md) Administratoren ihre Berechtigungen explizit erhöhen. Dadurch wird verhindert, dass schädlicher Code mit Administratorrechten ausgeführt wird.

Weitere Informationen und Beispiele finden Sie unter [Benutzerkontensteuerung.](winenv-uac.md)

### <a name="default-values"></a>Standardwerte

-   **Die Einstellungen in einem Eigenschaftenfenster müssen den aktuellen Zustand der Anwendung, des Objekts oder der Auflistung von Objekten widerspiegeln.** Andernfalls wäre dies irreführend und führt möglicherweise zu unerwünschten Ergebnissen. Wenn die Einstellungen z. B. die Empfehlungen, aber nicht den aktuellen Status widerspiegeln, können Benutzer auf Abbrechen klicken, anstatt Änderungen vorzunehmen, da sie denken, dass keine Änderungen erforderlich sind.
-   **Wählen Sie den sichersten (um Datenverlust oder Systemzugriff zu verhindern) und den sichersten Anfangszustand aus.** Angenommen, die meisten Benutzer ändern die Einstellungen nicht.
-   **Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie den Anfangszustand aus, der wahrscheinlich oder praktisch ist.**

## <a name="text"></a>Text

### <a name="commands"></a>Befehle

-   Verwenden Sie "Optionen", um Programmoptionen anzuzeigen.
-   Verwenden Sie "Eigenschaften", um das Eigenschaftenfenster eines Objekts anzuzeigen.
-   Um eine Zusammenfassung der häufig verwendeten Programmanpassungseinstellungen anzuzeigen, verwenden Sie["Personalisieren".](glossary.md)
-   Verwenden Sie nicht "Einstellungen" oder "Preferences".
-   Verwenden Sie für diese Befehle keine [Ellipsen.](ctrl-command-buttons.md)

### <a name="property-sheet-titles"></a>Titel von Eigenschaftenblättern

-   Verwenden Sie für ein einzelnes Objekt \[ "Objektname-Eigenschaften". \]
    -   Wenn das Objekt keinen Namen hat, verwenden Sie den Typnamen des Objekts. (Beispiel: Benutzerkontoeigenschaften.)
-   Verwenden Sie für mehrere Objekte " \[ first object name , \] ... Eigenschaften."
    -   Wenn die Objekte keine Namen haben, verwenden Sie den Typnamen der Objekte. (Beispiel: Benutzerkonteneigenschaften.)
    -   Wenn die Objekte unterschiedliche Typen aufweisen, verwenden Sie "Auswahleigenschaften".
-   Verwenden Sie [die Groß-/Großschreibung im Titelformat.](glossary.md)
-   Verwenden Sie keine Interpunktion am Ende.
-   Verwenden Sie keine Bindestriche, z. B. \[ "Objektname \] – Eigenschaften".

### <a name="property-inspector-titles"></a>Titel des Eigenschafteninspektors

-   Verwenden Sie "Eigenschaften".
-   Verwenden Sie die Groß-/Großschreibung im Titelstil.
-   Verwenden Sie keine Interpunktion am Ende.

### <a name="options-dialog-box-titles"></a>Titel des Dialogfelds "Optionen"

-   Verwenden Sie "Optionen".
-   Verwenden Sie die Groß-/Großschreibung im Titelstil.
-   Verwenden Sie keine Interpunktion am Ende.

### <a name="property-page-tab-names"></a>Namen der Registerkarten der Eigenschaftenseite

-   **Verwenden Sie präzise Registerkartenbezeichnungen.** Verwenden Sie ein oder zwei Wörter, die den Inhalt der Seite eindeutig beschreiben. Die Verwendung längerer Registerkartennamen führt zu einer ineffizienten Verwendung des Bildschirmbereichs, insbesondere dann, wenn die Registerkartennamen lokalisiert werden.
-   **Verwenden Sie bestimmte, aussagekräftige Registerkartenbezeichnungen.** Vermeiden Sie generische Registerkartenbezeichnungen, die für alle Registerkarten wie Allgemein, Erweitert oder Einstellungen gelten können.
-   Schreiben Sie die Bezeichnung als 1- oder 2-Wort-Ausdruck, und verwenden Sie keine endende Interpunktion.
-   Verwenden Sie [die Groß-/Großschreibung im Satzformat.](glossary.md)
-   Weisen Sie keinen eindeutigen [Zugriffsschlüssel](glossary.md)zu.

### <a name="property-page-text"></a>Text der Eigenschaftenseite

-   Vermeiden Sie große Textblöcke.
-   Geben Sie genügend Platz für den Text an, um 30 Prozent zu erweitern, wenn er lokalisiert wird.
-   Verwenden Sie keinen Text, der als Befehl in Eigenschaftenfenstern formuliert ist. Da Benutzer möglicherweise einfach Einstellungen anzeigen möchten, möchten Sie sie nicht auffordern, Einstellungen zu ändern.
-   Verwenden Sie die Groß- und Endpunktion im Satzformat.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Eigenschaftenfenster:

-   In der Programmierung und anderen technischen Dokumentationen finden Sie eigenschaftenblätter und Optionsdialogfelder als Eigenschaftenblätter. Verwenden Sie überall sonst das Dialogfeld, insbesondere in der Benutzerdokumentation.
-   Verwenden Sie den genauen Titeltext, einschließlich der Groß-/Großschreibung.
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie öffnen und schließen.
-   Formatieren Sie den Titel nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie den Titel nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

Beim Verweisen auf Eigenschaftenseiten:

-   Verweisen Sie in der Programmierung und anderen technischen Dokumentationen auf Eigenschaftenseiten als Eigenschaftenseiten. Verwenden Sie überall die Registerkarte , insbesondere in der Benutzerdokumentation.
-   Verwenden Sie den genauen Titeltext, einschließlich der Groß-/Großschreibung.
-   Verwenden Sie zum Beschreiben der Benutzerinteraktion Click, um auf eine Registerkarte zu verweisen.
-   Formatieren Sie den Namen nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie den Namen nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

 

 