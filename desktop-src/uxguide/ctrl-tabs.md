---
title: Registerkarten
description: Registerkarten bieten eine Möglichkeit, verwandte Informationen auf separaten beschrifteten Seiten darzustellen.
ms.assetid: d90228ce-aa95-4359-be8e-ea2014d71ae6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d6922865abcaa060cc2e4b13e4768d57bcd17aa8
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524474"
---
# <a name="tabs"></a>Registerkarten

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Registerkarten bieten eine Möglichkeit, verwandte Informationen auf separaten beschrifteten Seiten darzustellen.

![Screenshot von fünf Registerkarten ](images/ctrl-tabs-image1.png)

Ein typischer Satz von Registerkarten.

Registerkarten sind in der Regel Eigenschaftenfenstern zugeordnet (und umgekehrt), aber Registerkarten können in jedem Fenstertyp verwendet werden.

Registerkartensteuerelemente stellen die Ordner im Registerkartenbett dar, die zum Organisieren von Informationen in Denkschränken verwendet werden, die häufig im USA gefunden werden. (Ordner werden nicht weltweit verwendet.)

> [!Note]  
> Richtlinien im Zusammenhang mit [Layout,](vis-layout.md) [Registerkartenmenüs,](cmd-menus.md) [Dialogfeldern](win-dialog-box.md)und [Eigenschaftenfenstern](win-property-win.md) werden in separaten Artikeln dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Können die Steuerelemente problemlos auf eine einzelne Seite mit angemessener Größe passen?** Verwenden Sie in diesem Falle eine einzelne Seite.
-   **Gibt es nur eine Registerkarte?** Verwenden Sie in diesem Falle eine einzelne Seite.
-   **Sind die Registerkarten auf offensichtliche Weise miteinander verknüpft?** Falls nicht, sollten Sie die Informationen in separate Fenster verwandter Informationen aufteilen.
-   **Sind Einstellungen auf verschiedenen Seiten vollständig unabhängig, wenn sie für Einstellungen verwendet werden?** Wirkt sich das Ändern einer Einstellung auf einer Seite auf Einstellungen auf anderen Seiten aus? Wenn sie nicht unabhängig sind, verwenden Sie stattdessen Aufgabenseiten oder einen [Assistenten.](win-wizards.md)
-   **Sind die Registerkarten größtenteils miteinander verbunden, oder gibt es eine hierarchische Beziehung?** Erwägen Sie bei hierarchischer Darstellung die Verwendung von progressiver Offenlegung oder [untergeordneten Dialogfeldern,](win-dialog-box.md) um verwandte Informationen anzuzeigen.
-   **Werden die Registerkarten zum Anzeigen von Schritten innerhalb einer Aufgabe verwendet?** Sie können "Registerkarten" verwenden, um Schritte innerhalb einer Aufgabe nur anzuzeigen, wenn sie wie Schritte angezeigt werden, und es gibt eine offensichtliche alternative Möglichkeit, zum Textschritt zu gelangen, z. B. die Schaltfläche Weiter. Wenn die Schritte erforderlich sind, verwenden Sie andernfalls Seiten in einem Seitenflow oder [assistenten](win-wizards.md). Wenn die Schritte optional sind, zeigen Sie die optionalen Schritte stattdessen in modalen [Dialogfeldern an.](win-dialog-box.md)
-   **Sind die Registerkarten unterschiedliche Ansichten derselben Daten?** Wenn dies der Fall ist, sollten Sie eine [geteilte Schaltfläche](ctrl-command-buttons.md) oder [Dropdownliste](/windows/desktop/uxguide/ctrl-drop) verwenden, um Ansichten zu ändern. Registerkarten können zwar effektiv zum Ändern von Ansichten verwendet werden, aber die Alternativen sind einfacher.

## <a name="usage-patterns"></a>Verwendungsmuster

Registerkarten weisen mehrere Verwendungsmuster auf:



|  Verwendung                                                                                                                                                                                                 |    Beispiel                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Dynamische Fensteroberfläche**<br/> Wie Scrollleisten können Registerkarten verwendet werden, um die Fensteroberfläche zu vergrößern, um verwandte Informationen anzuzeigen.<br/>                                                    | Bei diesem Muster ähnelt die Verwendung von Registerkarten konzeptionell dem linearen Platzieren aller Informationen auf den Registerkarten auf einer einzelnen scrollbaren Oberfläche mit den Registerkartenbezeichnungen als Überschriften. <br/> ![Screenshot von fünf Registerkarten ](images/ctrl-tabs-image1.png)<br/> In diesem Beispiel vergrößern Registerkarten effektiv die Fensteroberfläche.<br/>                          |
| **Mehrere Ansichten**<br/> Wie geteilte Schaltflächen oder Dropdownlisten können Registerkarten verwendet werden, um verschiedene Ansichten derselben oder verwandter Informationen anzuzeigen. <br/>                                           | ![Screenshot der Registerkarten "Entwurf", "Teilen" und "Vorschau" ](images/ctrl-tabs-image2.png)<br/> In diesem Beispiel ändern Registerkarten ansichten innerhalb eines Dokuments.<br/>                                                                                                                                                                                                         |
| **Mehrere Dokumente**<br/> Wie mehrere Fenster können Registerkarten verwendet werden, um verschiedene Dokumente in einem einzigen Fenster anzuzeigen. <br/>                                                                   | ![Screenshot von drei Registerkarten für verschiedene Dokumente ](images/ctrl-tabs-image3.png)<br/> ![Abbildung der Registerkarten für verschiedene Monate ](images/ctrl-tabs-image4.png)<br/> In diesen Beispielen zeigen Registerkarten verschiedene Dokumente innerhalb eines einzelnen Anwendungsfensters an.<br/>                                                                                       |
| **Exklusive Optionen**<br/> Wie Optionsfelder können Registerkarten verwendet werden, um mehrere exklusive Optionen darzustellen. In diesem Muster wird nur die ausgewählte Registerkarte angewendet, und alle anderen Registerkarten werden ignoriert. <br/> | ![Screenshot der Registerkarten "Speicherort", "Daten" und "Meldungen" ](images/ctrl-tabs-image5.png)<br/> In diesem Beispiel werden Registerkarten (fälschlicherweise) als Ersatz für Optionsfelder verwendet.<br/> **Dieses Muster wird nicht empfohlen,** da es ein nicht standardmäßiges Verhalten verwendet. Die Registerkarten verhalten sich wie eine Einstellung anstelle einer reinen Möglichkeit, innerhalb des Fensters zu navigieren. <br/> |



 

**Wenn Sie nur eine Sache tun...**

Stellen Sie sicher, dass die Informationen auf den Registerkarten verknüpft sind, die Einstellungen auf verschiedenen Seiten jedoch unabhängig sind. Die letzte ausgewählte Registerkarte sollte keine besondere Bedeutung haben.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie horizontale Registerkarten, wenn:**
    -   Das Fenster verfügt über sieben oder weniger Registerkarten.
    -   **Alle Registerkarten passen in eine Zeile, auch wenn die Benutzeroberfläche lokalisiert ist.**
-   **Verwenden Sie vertikale Registerkarten, wenn:**
    -   Das Eigenschaftenfenster verfügt über acht oder mehr Registerkarten.
    -   **Die Verwendung horizontaler Registerkarten würde mehr als eine Zeile erfordern.**

        ![Screenshot des Eigenschaftenfensters mit elf Optionen ](images/ctrl-tabs-image6.png)

        In diesem Beispiel sind auf vertikalen Registerkarten acht oder mehr Registerkarten möglich.

-   **Schachteln Sie registerkarten nicht, oder kombinieren Sie horizontale Registerkarten nicht mit vertikalen Registerkarten.** Reduzieren Sie stattdessen die Anzahl der Registerkarten, verwenden Sie nur vertikale Registerkarten, oder verwenden Sie ein anderes Steuerelement, z. B. eine Dropdownliste.
-   **Scrollen Sie nicht auf horizontalen Registerkarten.** Horizontales Scrollen ist nicht sofort erkennbar. Sie können jedoch auf vertikalen Registerkarten scrollen.

    **Falsch:**

    ![Screenshot der abgeschnittenen horizontalen Registerkartenbezeichnung ](images/ctrl-tabs-image7.png)

    In diesem Beispiel werden die horizontalen Registerkarten gescrollt.

-   Legen Sie für Registerkarten in einem fenster- oder bereichsveränderbaren Fenster oder Bereich bei Bedarf eine Bildlaufleiste auf der Seite und nicht im Fenster oder Bereich ein. Die Registerkarten sollten immer sichtbar sein und nicht aus der Ansicht scrollen.

    ![Screenshot der vertikalen Registerkartenseite mit Scrollleiste ](images/ctrl-tabs-image8.png)

    In diesem Beispiel verfügt die Registerkarte über die Scrollleiste, nicht über den Bereich.

-   **Stellen Sie sicher, dass die Registerkarten wie Registerkarten und nicht wie ein anderer Steuerelementtyp aussehen.**

    **Falsch:**

    ![Screenshot des Fensters mit Schaltflächen für Registerkarten ](images/ctrl-tabs-image9.png)

    In diesem Beispiel sehen diese Registerkarten wie Befehlsschaltflächen aus.

### <a name="interaction"></a>Interaktion

-   **Wenn Steuerelemente nur auf eine Seite angewendet werden, platzieren Sie sie innerhalb des Rahmens der Registerkartenseite.**
-   **Wenn Steuerelemente auf das gesamte Fenster angewendet werden, platzieren Sie sie außerhalb der Registerkartenseite.**
-   **Weisen Sie änderungenden Registerkarten keine Effekte zu.** Auf Registerkarten muss in beliebiger Reihenfolge zugegriffen werden können. Das Ändern der aktuellen Registerkarte sollte niemals Nebeneffekte haben, Einstellungen anwenden oder zu einer Fehlermeldung führen.
-   **Weisen Sie der letzten ausgewählten Registerkarte keine besondere Bedeutung zu.** Die Registerkartenauswahl ist für die Navigation vorgesehen, bei der die letzte Registerkartenauswahl des Benutzers keine Einstellung ist.
-   **Machen Sie die Einstellungen auf einer Seite nicht von den Einstellungen auf anderen Seiten abhängig.** Legen Sie alle abhängigen Einstellungen stattdessen auf derselben Seite ab.
-   **Wenn Benutzer wahrscheinlich mit der letzten angezeigten Registerkarte beginnen, machen Sie die Registerkarte persistent, und wählen Sie sie standardmäßig aus.** Sorgen Sie dafür, dass die Einstellungen pro Fenster und pro Benutzer beibehalten werden. Wählen Sie andernfalls standardmäßig die erste Seite aus.

### <a name="icons"></a>Symbole

-   **Setzen Sie keine Symbole auf Registerkarten.** Symbole bringen in der Regel unnötige visuelle Übersichtlichkeit mit sich, verbrauchen Platz auf dem Bildschirm und verbessern das Benutzerverständnis häufig nicht. Fügen Sie nur Symbole hinzu, die beim Verständnis helfen, z. B. Standardsymbole.

    **Falsch:**

    ![Screenshot des Fensters mit Symbolen auf Registerkarten ](images/ctrl-tabs-image10.png)

    In diesem Beispiel fügen die Symbole die visuelle Übersichtlichkeit hinzu und verbessern das Benutzerverständnis nur wenig.

    **Ausnahme:** Sie können klar erkennbare Symbole verwenden, wenn möglicherweise nicht genügend Platz zum Anzeigen aussagekräftiger Bezeichnungen verfügbar ist:

    **Richtig:**

    ![Screenshot von Registerkarten mit Symbolen und verkürzten Bezeichnungen ](images/ctrl-tabs-image11.png)

    In diesem Beispiel ist das Fenster so schmal, dass Symbole die Registerkarten besser kommunizieren als die Bezeichnungen.

-   **Verwenden Sie keine Produktlogos für Tabstoppgrafiken.** Registerkarten sind nicht für das Branding [von .](exper-branding.md)

### <a name="dynamic-window-surface-pattern"></a>Dynamisches Fensteroberflächenmuster

-   **Verwenden Sie keine Scrollleisten auf Registerkartenseiten.** Tabstopps funktionieren ähnlich wie Scrollleisten, um den effektiven Bereich eines Fensters zu erhöhen. Ein Mechanismus sollte ausreichend sein.
-   **Verwenden Sie präzise Registerkartenbezeichnungen.** Verwenden Sie ein oder zwei Wörter, die den Inhalt der Seite eindeutig beschreiben. Längere Bezeichnungen verbrauchen Bildschirmspeicherplatz, insbesondere wenn die Bezeichnungen lokalisiert sind.
-   **Verwenden Sie spezifische, aussagekräftige Registerkartenbezeichnungen.** Vermeiden Sie generische Registerkartenbezeichnungen, die auf alle Registerkarten angewendet werden können, z. B. Allgemein, Erweitert oder Einstellungen.
-   **Wenn eine Registerkarte nicht für den aktuellen Kontext gilt und Benutzer dies nicht erwarten, entfernen Sie sie.** Dadurch wird die Benutzeroberfläche vereinfacht, und Benutzer werden sie nicht übersehen.

    **Falsch:**

    ![Screenshot des Optionsfensters mit abgeblendeten Registerkartennamen ](images/ctrl-tabs-image12.png)

    In diesem Beispiel ist die Registerkarte Dateiadressen falsch deaktiviert, wenn Microsoft Word als E-Mail-Editor verwendet wird. Anstatt diese Registerkarte zu deaktivieren, sollte sie entfernt werden, da Benutzer nicht erwarten würden, dateistandorte in diesem Kontext ein- oder zu ändern.

-   **Wenn eine Registerkarte nicht für den aktuellen Kontext gilt und Benutzer dies möglicherweise erwarten:**

    -   Zeigt die Registerkarte an.
    -   Deaktivieren Sie die Steuerelemente auf der Seite.
    -   Fügen Sie Text ein, der erklärt, warum die Steuerelemente deaktiviert sind.

    Deaktivieren Sie die Registerkarte nicht, da dies nicht selbsterklärend ist und das Erkunden verhindert. Benutzer, die nach einem bestimmten Wert suchen, werden gezwungen, auf allen anderen Registerkarten zu suchen.

    ![Screenshot des Fensters mit abgeblendet angezeigten Registerkartenoptionen ](images/ctrl-tabs-image13.png)

    In diesem Beispiel gilt keine der Ansichtsoptionen im Leselayout. Benutzer erwarten jedoch möglicherweise, dass sie basierend auf der Registerkartenbezeichnung angewendet werden, sodass die Seite angezeigt wird, die Optionen jedoch deaktiviert sind.

### <a name="multiple-views-and-documents-patterns"></a>Mehrere Ansichten und Dokumentmuster

-   **Verwenden Sie die Ansichts- oder Dokumentnamen auf Registerkartenbezeichnungen.**
-   **Vermeiden Sie übermäßig lange Registerkartennamen.** Verwenden Sie bei Bedarf entweder eine maximale Namensgröße, oder schneiden Sie die angezeigte Registerkartenbezeichnung mithilfe von Ellipsen ab. Längere Bezeichnungen verbrauchen Bildschirmspeicherplatz, insbesondere wenn die Bezeichnungen lokalisiert sind.
-   **Wenn eine Registerkarte nicht für den aktuellen Kontext gilt, entfernen Sie die Registerkarte.**

### <a name="exclusive-options-pattern"></a>Muster für exklusive Optionen

-   **Verwenden Sie dieses Muster nicht!** Verwenden Sie stattdessen Optionsfelder oder eine Dropdownliste.

    **Falsch:**

    ![Screenshot des Fensters mit zwei Registerkarten "Erstellen" ](images/ctrl-tabs-image14.png)

    In diesem Beispiel werden Registerkarten fälschlicherweise als Ersatz für Optionsfelder verwendet.

    **Richtig:**

    ![Screenshot des Fensters mit zwei Optionsfeldern ](images/ctrl-tabs-image15.png)

    In diesem Beispiel werden Optionsfelder stattdessen ordnungsgemäß verwendet.

## <a name="labels"></a>Bezeichnungen

-   Bezeichnungsregisterkarte basierend auf ihrem Muster. Verwenden Sie Nomen anstelle von Verben, ohne die Interpunktion zu beenden. Weitere Informationen finden Sie in den obigen Musterrichtlinien.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Weisen Sie keinen Zugriffsschlüssel zu. Der Zugriff auf Registerkarten ist über die Tastenkombinationen (STRG+TAB, STRG+UMSCHALT+TAB, STRG+PgUp, STRG+PgDN) möglich. Es gibt einen Mangel an guten Zugriffsschlüsseloptionen, sodass das Zuweisen von Zugriffsschlüsseln zu Registerkarten es einfacher macht, sie anderen Steuerelementen zu zuweisen.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Registerkarten:

-   Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Unterschrift, und schließen Sie die Wortregisterkarte ein.
-   Verwenden Sie click, um die Benutzerinteraktion zu beschreiben.
-   Formatieren Sie die Bezeichnung nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.
-   Da mehrere Verwendungsmöglichkeiten mehrdeutig sein können, insbesondere für eine weltweite Zielgruppe, verwenden Sie die Nomenregisterkarte allein, um nur auf ein Registerkarten-Steuerelement zu verweisen. Bei anderen Verwendungen sollten Sie die Bedeutung mit einem Deskriptor verdeutlichen: die TAB-TASTE, einen Tabstopp oder ein Tabstoppzeichen auf dem Lineal.

Beispiel: Klicken Sie **im Menü Extras** auf **Optionen** und dann auf **die Registerkarte** Ansicht.

