---
title: Registerkarten
description: Registerkarten bieten eine Möglichkeit, verwandte Informationen auf separaten bezeichneten Seiten zu präsentieren.
ms.assetid: d90228ce-aa95-4359-be8e-ea2014d71ae6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 167b74bab228398eb0334452a5eacd359578d5bfc01efecb52ccafbcd90d376d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819025"
---
# <a name="tabs"></a>Registerkarten

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Registerkarten bieten eine Möglichkeit, verwandte Informationen auf separaten bezeichneten Seiten zu präsentieren.

![Screenshot von fünf Registerkarten ](images/ctrl-tabs-image1.png)

Ein typischer Satz von Registerkarten.

Registerkarten sind in der Regel Eigenschaftenfenstern (und umgekehrt) zugeordnet, aber Registerkarten können in jedem Fenstertyp verwendet werden.

Registerkartensteuerelemente stellen die Ordner im Registerkartenbett dar, die zum Organisieren von Informationen in Denkschränken verwendet werden, die häufig in der USA. (Ordner "Ordner" werden nicht weltweit verwendet.)

> [!Note]  
> Richtlinien im Zusammenhang mit [Layout,Registerkartenmenüs,](cmd-menus.md) [Dialogfeldern](win-dialog-box.md)und [Eigenschaftenfenstern](win-property-win.md) werden in separaten Artikeln dargestellt. [](vis-layout.md)

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Können die Steuerelemente auf eine einzelne Seite mit einer angemessenen Größe passen?** Wenn ja, verwenden Sie eine einzelne Seite.
-   **Gibt es nur eine Registerkarte?** Wenn ja, verwenden Sie eine einzelne Seite.
-   **Sind die Registerkarten auf offensichtliche Weise miteinander verknüpft?** Falls nicht, sollten Sie die Informationen in separate Fenster verwandter Informationen aufteilen.
-   **Sind Einstellungen auf verschiedenen Seiten vollständig unabhängig, wenn sie für Einstellungen verwendet werden?** Wirkt sich das Ändern einer Einstellung auf einer Seite auf einstellungen auf anderen Seiten aus? Wenn sie nicht unabhängig sind, verwenden Sie stattdessen Aufgabenseiten [oder einen](win-wizards.md) Assistenten.
-   **Sind die Registerkarten größtenteils Miteinander verknüpft, oder gibt es eine hierarchische Beziehung?** Wenn dies hierarchisch ist, sollten Sie die Verwendung von progressiven Offenlegungs- oder [untergeordneten Dialogfeldern](win-dialog-box.md) in Betracht ziehen, um verwandte Informationen anzuzeigen.
-   **Werden die Registerkarten verwendet, um Schritte innerhalb einer Aufgabe anzuzeigen?** Sie können "Registerkarten" verwenden, um Schritte innerhalb einer Aufgabe nur anzuzeigen, wenn sie wie Schritte aussehen, und es gibt eine offensichtliche alternative Möglichkeit, zum Textschritt zu kommen, z. B. eine Schaltfläche Weiter. Wenn die Schritte erforderlich sind, verwenden Sie andernfalls Seiten in einem Seitenfluss oder [einem Assistenten.](win-wizards.md) Wenn die Schritte optional sind, zeigen Sie stattdessen die optionalen Schritte mithilfe [modaler Dialogfelder](win-dialog-box.md) an.
-   **Sind die Registerkarten unterschiedliche Ansichten der gleichen Daten?** Wenn dies der Fall ist, sollten Sie eine geteilte [Schaltfläche](ctrl-command-buttons.md) oder [Dropdownliste verwenden,](/windows/desktop/uxguide/ctrl-drop) um Ansichten zu ändern. Registerkarten können zwar effektiv zum Ändern von Ansichten verwendet werden, die Alternativen sind jedoch schlanker.

## <a name="usage-patterns"></a>Verwendungsmuster

Registerkarten haben mehrere Verwendungsmuster:



|  Verwendung                                                                                                                                                                                                 |    Beispiel                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Dynamische Fensteroberfläche**<br/> Wie Bildlaufleisten können Registerkarten verwendet werden, um die Fensteroberfläche so zu erhöhen, dass verwandte Informationen angezeigt werden.<br/>                                                    | Bei diesem Muster ähnelt die Verwendung von Registerkarten konzeptionell dem linearen Platzieren aller Informationen auf den Registerkarten auf einer einzelnen bildlaufbaren Oberfläche mit den Registerkartenbezeichnungen als Überschriften. <br/> ![Screenshot von fünf Registerkarten ](images/ctrl-tabs-image1.png)<br/> In diesem Beispiel erhöhen Registerkarten effektiv die Fensteroberfläche.<br/>                          |
| **Mehrere Ansichten**<br/> Wie geteilte Schaltflächen oder Dropdownlisten können Registerkarten verwendet werden, um verschiedene Ansichten derselben oder verwandter Informationen zu zeigen. <br/>                                           | ![Screenshot der Registerkarten "Entwurf", "Teilen" und "Vorschau" ](images/ctrl-tabs-image2.png)<br/> In diesem Beispiel ändern Registerkarten ansichten innerhalb eines Dokuments.<br/>                                                                                                                                                                                                         |
| **Mehrere Dokumente**<br/> Wie mehrere Fenster können Registerkarten verwendet werden, um verschiedene Dokumente in einem einzelnen Fenster anzuzeigen. <br/>                                                                   | ![Screenshot von drei Registerkarten für verschiedene Dokumente ](images/ctrl-tabs-image3.png)<br/> ![Abbildung der Registerkarten für verschiedene Monate ](images/ctrl-tabs-image4.png)<br/> In diesen Beispielen zeigen Registerkarten verschiedene Dokumente innerhalb eines einzelnen Anwendungsfensters an.<br/>                                                                                       |
| **Exklusive Optionen**<br/> Wie Optionsfelder können Registerkarten verwendet werden, um mehrere exklusive Optionen zu präsentieren. in diesem Muster wird nur die ausgewählte Registerkarte angewendet, und alle anderen Registerkarten werden ignoriert. <br/> | ![Screenshot der Registerkarten "Speicherort", "Daten" und "Meldungen" ](images/ctrl-tabs-image5.png)<br/> In diesem Beispiel werden Registerkarten (falsch) als Ersatz für Optionsfelder verwendet.<br/> **Dieses Muster wird nicht empfohlen,** da es ein nicht standardmäßiges Verhalten verwendet. Die Registerkarten verhalten sich wie eine Einstellung und nicht als eine möglichkeit, innerhalb des Fensters zu navigieren. <br/> |



 

**Wenn Sie nur eins tun...**

Stellen Sie sicher, dass die Informationen auf den Registerkarten verknüpft sind, aber die Einstellungen auf verschiedenen Seiten sind unabhängig. Die letzte ausgewählte Registerkarte sollte keine besondere Bedeutung haben.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie horizontale Registerkarten, wenn:**
    -   Das Fenster verfügt über sieben oder weniger Registerkarten.
    -   **Alle Registerkarten passen in eine Zeile, auch wenn die Benutzeroberfläche lokalisiert ist.**
-   **Verwenden Sie vertikale Registerkarten, wenn:**
    -   Das Eigenschaftenfenster verfügt über acht oder mehr Registerkarten.
    -   **Die Verwendung horizontaler Registerkarten würde mehr als eine Zeile erfordern.**

        ![Screenshot des Eigenschaftenfensters mit elf Optionen ](images/ctrl-tabs-image6.png)

        In diesem Beispiel können vertikale Registerkarten acht oder mehr Registerkarten aufnehmen.

-   **Schachteln Sie keine Registerkarten, und kombinieren Sie keine horizontalen Registerkarten mit vertikalen Registerkarten.** Reduzieren Sie stattdessen die Anzahl der Registerkarten, verwenden Sie nur vertikale Registerkarten, oder verwenden Sie ein anderes Steuerelement, z. B. eine Dropdownliste.
-   **Scrollen Sie nicht auf horizontalen Registerkarten.** Horizontales Scrollen ist nicht leicht erkennbar. Sie können jedoch vertikale Registerkarten scrollen.

    **Falsch:**

    ![Screenshot der abgeschnittenen horizontalen Registerkartenbezeichnung ](images/ctrl-tabs-image7.png)

    In diesem Beispiel werden die horizontalen Registerkarten gescrollt.

-   Legen Sie für Registerkarten in einem Fenster oder Bereich, in dem die Größe geändert werden kann, bei Bedarf eine Bildlaufleiste auf der Seite und nicht im Fenster oder Bereich ab. Die Registerkarten sollten immer sichtbar sein und nicht aus der Ansicht heraus scrollen.

    ![Screenshot der vertikalen Registerkartenseite mit Bildlaufleiste ](images/ctrl-tabs-image8.png)

    In diesem Beispiel enthält die Registerkarte die Bildlaufleiste, nicht den Bereich.

-   **Stellen Sie sicher, dass die Registerkarten wie Registerkarten und nicht wie andere Steuerelementtypen aussehen.**

    **Falsch:**

    ![Screenshot des Fensters mit Schaltflächen für Registerkarten ](images/ctrl-tabs-image9.png)

    In diesem Beispiel sehen diese Registerkarten wie Befehlsschaltflächen aus.

### <a name="interaction"></a>Interaktion

-   **Wenn Steuerelemente nur auf eine Seite angewendet werden, platzieren Sie sie innerhalb des Rahmens der Registerkartenseite.**
-   **Wenn Steuerelemente auf das gesamte Fenster angewendet werden, platzieren Sie sie außerhalb der Registerkartenseite.**
-   **Weisen Sie sich ändernden Registerkarten keine Auswirkungen zu.** Auf Registerkarten muss in beliebiger Reihenfolge zugegriffen werden können. Das Ändern der aktuellen Registerkarte sollte niemals Nebeneffekte haben, Einstellungen anwenden oder zu einer Fehlermeldung führen.
-   **Weisen Sie der zuletzt ausgewählten Registerkarte keine besondere Bedeutung zu.** Die Registerkartenauswahl ist für die Navigation der letzten Registerkartenauswahl des Benutzers keine Einstellung.
-   **Machen Sie die Einstellungen auf einer Seite nicht von den Einstellungen auf anderen Seiten abhängig.** Legen Sie stattdessen alle abhängigen Einstellungen auf derselben Seite ab.
-   **Wenn Benutzer wahrscheinlich mit der letzten angezeigten Registerkarte beginnen, lassen Sie die Registerkarte beibehalten, und wählen Sie sie standardmäßig aus.** Sorgen Sie dafür, dass die Einstellungen pro Fenster und pro Benutzer beibehalten werden. Wählen Sie andernfalls standardmäßig die erste Seite aus.

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

    In diesem Beispiel ist die Registerkarte Dateiadressen falsch deaktiviert, Microsoft Word als E-Mail-Editor verwendet wird. Anstatt diese Registerkarte zu deaktivieren, sollte sie entfernt werden, da Benutzer in diesem Kontext nicht erwarten würden, Dateipositionen ein- oder zu ändern.

-   **Wenn eine Registerkarte nicht für den aktuellen Kontext gilt und Benutzer dies möglicherweise erwarten:**

    -   Zeigt die Registerkarte an.
    -   Deaktivieren Sie die Steuerelemente auf der Seite.
    -   Fügen Sie Text ein, der erklärt, warum die Steuerelemente deaktiviert sind.

    Deaktivieren Sie die Registerkarte nicht, da dies nicht selbsterklärend ist und das Erkunden verhindert. Benutzer, die nach einem bestimmten Wert suchen, werden gezwungen, auf allen anderen Registerkarten zu suchen.

    ![Screenshot des Fensters mit abgeblendet angezeigten Registerkartenoptionen ](images/ctrl-tabs-image13.png)

    In diesem Beispiel gilt keine der Ansichtsoptionen im Leselayout. Benutzer erwarten jedoch möglicherweise, dass sie basierend auf der Registerkartenbezeichnung angewendet werden, sodass die Seite angezeigt wird, die Optionen jedoch deaktiviert sind.

### <a name="multiple-views-and-documents-patterns"></a>Mehrere Ansichten und Dokumentmuster

-   **Verwenden Sie die Ansichts- oder Dokumentnamen auf Registerkartenbezeichnungen.**
-   **Vermeiden Sie übermäßig lange Registerkartennamen.** Verwenden Sie bei Bedarf entweder eine maximale Namensgröße, oder schneiden Sie die angezeigte Registerkartenbezeichnung mithilfe von Ausellipsen ab. Längere Bezeichnungen verbrauchen Bildschirmspeicherplatz, insbesondere wenn die Bezeichnungen lokalisiert sind.
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
-   Um die Benutzerinteraktion zu beschreiben, klicken Sie auf .
-   Formatieren Sie die Bezeichnung nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.
-   Da mehrere Verwendungen mehrdeutig sein können, insbesondere für eine weltweite Zielgruppe, verwenden Sie die Nomenregisterkarte allein, um nur auf ein Registerkarten-Steuerelement zu verweisen. Bei anderen Verwendungen sollten Sie die Bedeutung mit einem Deskriptor verdeutlichen: die TAB-TASTE, einen Tabstopp oder ein Tabstoppzeichen auf dem Lineal.

Beispiel: Klicken Sie **im Menü Extras** auf **Optionen** und dann auf **die Registerkarte** Ansicht.

