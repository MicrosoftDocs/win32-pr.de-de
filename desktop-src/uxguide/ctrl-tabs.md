---
title: Registerkarten
description: Registerkarten bieten eine Möglichkeit, Verwandte Informationen auf separaten beschrifteten Seiten darzustellen.
ms.assetid: d90228ce-aa95-4359-be8e-ea2014d71ae6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b2649862885e55bdfe10fdca7f34b7618d976a38
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104558661"
---
# <a name="tabs"></a>Registerkarten

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Registerkarten bieten eine Möglichkeit, Verwandte Informationen auf separaten beschrifteten Seiten darzustellen.

![Screenshot von fünf Registerkarten ](images/ctrl-tabs-image1.png)

Eine typische Gruppe von Registerkarten.

Registerkarten sind in der Regel mit Eigenschaften Fenstern (und umgekehrt) verknüpft, aber Tabstopps können in beliebigen Fenstertypen verwendet werden.

Registerkarten-Steuerelemente stellen die Manila-Ordner im Registerkarten Format dar, die zum Organisieren von Informationen in den in der USA allgemein gefundenen Ordner (Die Manila-Ordner werden nicht weltweit verwendet.)

> [!Note]  
> Richtlinien im Zusammenhang mit [Layout](vis-layout.md), [Registerkarten Menüs](cmd-menus.md), [Dialogfeldern](win-dialog-box.md)und [Eigenschaften Fenstern](win-property-win.md) werden in separaten Artikeln dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Können die Steuerelemente bequem in eine einzelne, eine Seite mit einer Größenanpassung passen?** Wenn dies der Fall ist, verwenden Sie eine einzelne Seite.
-   **Gibt es nur eine Registerkarte?** Wenn dies der Fall ist, verwenden Sie eine einzelne Seite.
-   **Sind die Registerkarten auf eine offensichtliche Weise miteinander verknüpft?** Falls nicht, sollten Sie die Informationen in getrennte Fenster mit verwandten Informationen aufteilen.
-   **Wenn die Einstellungen für Einstellungen verwendet werden, sind die Einstellungen auf unterschiedlichen Seiten vollständig unabhängig?** Wirkt sich die Änderung einer Einstellung auf einer Seite auf die Einstellungen auf anderen Seiten aus? Wenn Sie nicht unabhängig sind, verwenden Sie stattdessen Aufgabenseiten oder einen [Assistenten](win-wizards.md) .
-   **Handelt es sich bei den Registerkarten meistens um Peers, oder gibt es eine hierarchische Beziehung?** Wenn Sie hierarchisch verwenden, sollten Sie die Verwendung progressiver Offenlegung oder untergeordneter [Dialogfelder](win-dialog-box.md) in Erwägung gezogen haben
-   **Werden die Registerkarten zum Anzeigen von Schritten innerhalb einer Aufgabe verwendet?** Sie können "Registerkarten" verwenden, um Schritte innerhalb einer Aufgabe nur anzuzeigen, wenn Sie in Form von Schritten angezeigt werden, und es gibt eine offensichtliche Alternative Methode, um zum Text Schritt zu gelangen, z. b. eine Schaltfläche "weiter". Andernfalls sollten Sie, wenn die Schritte erforderlich sind, Seiten in einem Seiten Fluss oder einem [Assistenten](win-wizards.md)verwenden. Wenn die Schritte optional sind, zeigen Sie die optionalen Schritte stattdessen mithilfe von modalen [Dialogfeldern](win-dialog-box.md) an.
-   **Handelt es sich bei den Registerkarten um unterschiedliche Ansichten derselben Daten?** Wenn dies der Fall ist, sollten Sie eine unter [teilte Schaltfläche](ctrl-command-buttons.md) oder [Dropdown Liste](/windows/desktop/uxguide/ctrl-drop) verwenden, um Ansichten zu ändern. Obwohl Registerkarten für das Ändern von Ansichten effektiv verwendet werden können, sind die alternativen einfacher.

## <a name="usage-patterns"></a>Verwendungsmuster

Registerkarten weisen mehrere Verwendungs Muster auf:



|                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Dynamische Fenster Oberfläche**<br/> wie Scrollleisten können auch Registerkarten verwendet werden, um die Fenster Oberfläche zu vergrößern und damit verwandte Informationen anzuzeigen.<br/>                                                    | Bei diesem Muster ist die Verwendung von Registerkarten konzeptionell ähnlich, wenn alle Informationen auf den Registerkarten linear auf einer einzelnen scrollbaren Oberfläche platziert werden, wobei die Registerkarten Bezeichnungen als Überschriften angezeigt werden. <br/> ![Screenshot von fünf Registerkarten ](images/ctrl-tabs-image1.png)<br/> In diesem Beispiel vergrößern Registerkarten effektiv die Fenster Oberfläche.<br/>                          |
| **Mehrere Ansichten**<br/> wie z. b. unterteilte Schaltflächen oder Dropdown Listen können Registerkarten verwendet werden, um unterschiedliche Ansichten derselben oder verwandter Informationen anzuzeigen. <br/>                                           | ![Screenshot der Registerkarten "Entwurf", "teilen" und "Vorschau" ](images/ctrl-tabs-image2.png)<br/> In diesem Beispiel ändern Registerkarten Ansichten innerhalb eines Dokuments.<br/>                                                                                                                                                                                                         |
| **Mehrere Dokumente**<br/> wie bei mehreren Fenstern können auch Registerkarten verwendet werden, um unterschiedliche Dokumente in einem einzelnen Fenster anzuzeigen. <br/>                                                                   | ![Screenshot von drei Registerkarten für verschiedene Dokumente ](images/ctrl-tabs-image3.png)<br/> ![Abbildung von Registerkarten für verschiedene Monate ](images/ctrl-tabs-image4.png)<br/> In diesen Beispielen zeigen Registerkarten verschiedene Dokumente in einem einzelnen Anwendungsfenster an.<br/>                                                                                       |
| **Exklusive Optionen**<br/> wie Options Felder können auch Registerkarten verwendet werden, um mehrere exklusive Optionen zu präsentieren. in diesem Muster wird nur die ausgewählte Registerkarte angewendet, und alle anderen Registerkarten werden ignoriert. <br/> | ![Screenshot der Registerkarten "Standort", "Daten" und "Meldungen" ](images/ctrl-tabs-image5.png)<br/> In diesem Beispiel werden Registerkarten (falsch) als Ersatz für options Felder verwendet.<br/> **Dieses Muster wird nicht empfohlen** , da es ein nicht standardmäßiges Verhalten verwendet. Die Registerkarten Verhalten sich als Einstellung, anstatt Sie im Fenster zu navigieren. <br/> |



 

**Wenn Sie nur eine Aktion ausführen...**

Stellen Sie sicher, dass die Informationen auf den Registerkarten verwandt sind, aber die Einstellungen auf unterschiedlichen Seiten sind unabhängig voneinander. Die letzte ausgewählte Registerkarte sollte keine besondere Bedeutung haben.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Horizontale Registerkarten verwenden, wenn:**
    -   Das Fenster enthält sieben oder weniger Registerkarten.
    -   **Alle Registerkarten passen in eine Zeile, auch wenn die Benutzeroberfläche lokalisiert ist.**
-   **Vertikale Registerkarten verwenden, wenn:**
    -   Das Eigenschaften Fenster verfügt über acht oder mehr Registerkarten.
    -   **Die Verwendung von horizontalen Registerkarten erfordert mehr als eine Zeile.**

        ![Screenshot des Eigenschaften Fensters mit elf Optionen ](images/ctrl-tabs-image6.png)

        In diesem Beispiel werden bei vertikalen Registerkarten acht oder mehr Registerkarten angezeigt.

-   **Schachteln Sie keine Registerkarten, oder kombinieren Sie keine horizontalen Registerkarten mit vertikalen** Reduzieren Sie stattdessen die Anzahl der Registerkarten, verwenden Sie nur vertikale Registerkarten, oder verwenden Sie ein anderes Steuerelement, z. b. eine Dropdown Liste.
-   **Scrollen Sie nicht in horizontalen Registerkarten.** Horizontales Scrollen ist nicht leicht erkennbar. Sie können jedoch auf vertikalen Registerkarten scrollen.

    **Falsch:**

    ![Screenshot der abgeschnittene horizontalen Registerkarten Bezeichnung ](images/ctrl-tabs-image7.png)

    In diesem Beispiel werden auf den horizontalen Registerkarten ein Rollup ausgeführt.

-   Bei Registerkarten in einem Fenster oder Bereich, das in der Größe geändert werden kann, sollten Sie bei Bedarf eine Bild Lauf Leiste auf der Seite, nicht auf das Fenster oder den Bereich platzieren. Die Registerkarten sollten immer sichtbar sein und keinen Bildlauf außerhalb der Ansicht durchführen.

    ![Screenshot der vertikalen Registerkarte mit der Scrollleiste ](images/ctrl-tabs-image8.png)

    In diesem Beispiel verfügt die Registerkarte über die Scrollleiste, nicht über den Bereich.

-   **Stellen Sie sicher, dass die Registerkarten wie Registerkarten und keine andere Art von Steuerelement aussehen.**

    **Falsch:**

    ![Screenshot des Fensters mit Schaltflächen für Registerkarten ](images/ctrl-tabs-image9.png)

    In diesem Beispiel sehen diese Registerkarten wie Befehls Schaltflächen aus.

### <a name="interaction"></a>Interaktion

-   **Wenn Steuerelemente nur auf eine Seite angewendet werden, platzieren Sie diese innerhalb des Rahmens der Seite im Register Format.**
-   **Wenn Steuerelemente auf das gesamte Fenster angewendet werden, platzieren Sie diese außerhalb der Seite im Register Format.**
-   **Weisen Sie den Wechsel von Registerkarten keine Auswirkungen zu.** Registerkarten müssen in beliebiger Reihenfolge zugänglich sein. Das Ändern der aktuellen Registerkarte darf keine Nebeneffekte haben, Einstellungen anwenden oder zu einer Fehlermeldung führen.
-   **Weisen Sie der zuletzt ausgewählten Registerkarte keine besondere Bedeutung zu.** Registerkarten Auswahl dient zur Navigation: die letzte Registerkarten Auswahl des Benutzers ist keine Einstellung.
-   **Nehmen Sie die Einstellungen auf einer Seite nicht abhängig von den Einstellungen auf anderen Seiten vor.** Legen Sie stattdessen alle abhängigen Einstellungen auf derselben Seite ab.
-   **Wenn Benutzer wahrscheinlich mit der zuletzt angezeigten Registerkarte beginnen, legen Sie die Registerkarte persistent, und wählen Sie Sie standardmäßig aus.** Sorgen Sie dafür, dass die Einstellungen pro Fenster und Benutzer bezogen bleiben. Wählen Sie andernfalls standardmäßig die erste Seite aus.

### <a name="icons"></a>Symbole

-   **Fügen Sie Symbole nicht auf Registerkarten ein.** Symbole fügen in der Regel unnötige visuelle Übersichtlichkeit hinzu, verbrauchen Bildschirmfläche und verbessern das Benutzer Verständnis häufig nicht. Fügen Sie nur Symbole hinzu, die das Verständnis unterstützen, z. b. Standardsymbole.

    **Falsch:**

    ![Screenshot des Fensters mit Symbolen auf Registerkarten ](images/ctrl-tabs-image10.png)

    In diesem Beispiel fügen die Symbole visuelle Übersichtlichkeit hinzu und führen wenig aus, um das Benutzer Verständnis zu verbessern.

    **Ausnahme:** Sie können klar erkennbare Symbole verwenden, wenn möglicherweise nicht genügend Speicherplatz vorhanden ist, um aussagekräftige Bezeichnungen anzuzeigen:

    **Richtig:**

    ![Screenshot von Registerkarten mit Symbolen und abkürzte Bezeichnungen ](images/ctrl-tabs-image11.png)

    In diesem Beispiel ist das Fenster so schmal, dass Symbole die Registerkarten besser kommunizieren als die Bezeichnungen.

-   **Verwenden Sie keine Produktlogos für Registerkarten Grafiken.** Registerkarten sind nicht zum [Branding](exper-branding.md).

### <a name="dynamic-window-surface-pattern"></a>Dynamisches Fenster Oberflächenmuster

-   **Verwenden Sie keine Scrollleisten auf Registerkarten Seiten.** Registerkarten funktionieren ähnlich wie Bild Lauf leisten, um den effektiven Bereich eines Fensters zu vergrößern. Ein Mechanismus sollte ausreichen.
-   **Verwenden Sie präzise Registerkarten Bezeichnungen.** Verwenden Sie ein oder zwei Wörter, die den Inhalt der Seite eindeutig beschreiben. Längere Bezeichnungen belegen Bildschirmfläche, insbesondere dann, wenn die Bezeichnungen lokalisiert sind.
-   **Verwenden Sie bestimmte, aussagekräftige Registerkarten Bezeichnungen.** Vermeiden Sie generische Registerkarten Bezeichnungen, die auf eine beliebige Registerkarte (z. b. Allgemein, erweitert oder Einstellungen) angewendet werden können.
-   **Wenn eine Registerkarte nicht auf den aktuellen Kontext angewendet wird und Benutzer dies nicht erwarten, entfernen Sie Sie.** Dadurch wird die Benutzeroberfläche vereinfacht, und Benutzer werden Sie nicht übersehen.

    **Falsch:**

    ![Screenshot des Fensters "Optionen" mit der Registerkarte "Abbild" ](images/ctrl-tabs-image12.png)

    In diesem Beispiel ist die Registerkarte Dateispeicher Orte falsch deaktiviert, wenn Microsoft Word als e-Mail-Editor verwendet wird. Anstatt diese Registerkarte zu deaktivieren, sollte Sie entfernt werden, da Benutzer nicht erwarten, Dateispeicher Orte in diesem Kontext anzuzeigen oder zu ändern.

-   **Wenn eine Registerkarte nicht für den aktuellen Kontext gilt und die Benutzer möglicherweise Folgendes erwarten:**

    -   Zeigen Sie die Registerkarte an.
    -   Deaktivieren Sie die Steuerelemente auf der Seite.
    -   Schließt Text ein, der erklärt, warum die Steuerelemente deaktiviert sind.

    Deaktivieren Sie die Registerkarte nicht, da dies nicht selbsterklärend ist und die Untersuchung untersagt. Benutzer, die nach einem bestimmten Wert suchen, müssten alle anderen Registerkarten überprüfen.

    ![Screenshot des Fensters mit der Anzeige Registerkarten Optionen ](images/ctrl-tabs-image13.png)

    In diesem Beispiel gilt keine der Ansichtsoptionen beim Lesen des Layouts. Benutzer erwarten jedoch möglicherweise, dass Sie auf Grundlage der Registerkarten Bezeichnung angewendet werden, sodass die Seite angezeigt wird, aber die Optionen deaktiviert sind.

### <a name="multiple-views-and-documents-patterns"></a>Mehrere Ansichten und Dokument Muster

-   **Verwenden Sie die Ansichts-oder Dokumentnamen für Registerkarten Bezeichnungen.**
-   **Vermeiden Sie übermäßig lange Registerkarten Namen.** Verwenden Sie bei Bedarf entweder eine maximale namens Größe, oder kürzen Sie die angezeigte Registerkarten Bezeichnung mithilfe von Ellipsen. Längere Bezeichnungen belegen Bildschirmfläche, insbesondere dann, wenn die Bezeichnungen lokalisiert sind.
-   **Wenn eine Registerkarte nicht auf den aktuellen Kontext angewendet wird, entfernen Sie die Registerkarte.**

### <a name="exclusive-options-pattern"></a>Muster für exklusive Optionen

-   **Verwenden Sie dieses Muster nicht.** Verwenden Sie stattdessen Options Felder oder eine Dropdown Liste.

    **Falsch:**

    ![Screenshot des Fensters mit zwei ' Create '-Registerkarten ](images/ctrl-tabs-image14.png)

    In diesem Beispiel werden Registerkarten fälschlicherweise als Ersatz für options Felder verwendet.

    **Richtig:**

    ![Screenshot des Fensters mit zwei Options Feldern ](images/ctrl-tabs-image15.png)

    In diesem Beispiel werden stattdessen die Options Felder ordnungsgemäß verwendet.

## <a name="labels"></a>Bezeichnungen

-   Bezeichnungs Registerkarten auf der Grundlage ihres Musters. Verwenden Sie Nomen anstelle von Verben ohne das Beenden der Interpunktions Zeichen. Weitere Informationen finden Sie in den vorhergehenden Muster Richtlinien.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Weisen Sie keinen Zugriffsschlüssel zu. Sie können über die Tastenkombinationen auf Tabstopps zugreifen (STRG + TAB, STRG + UMSCHALT + TAB, STRG + PgUp, STRG + PgDn). Es gibt einen Mangel an guten Zugriffs Schlüsseln, sodass das Zuweisen von Zugriffs Schlüsseln zu Registerkarten die Zuweisung zu anderen Steuerelementen erleichtert.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Registerkarten:

-   Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-und Kleinschreibung, und schließen Sie die Registerkarte Word
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie klicken.
-   Formatieren Sie nach Möglichkeit die Bezeichnung mit fettem Text. Andernfalls sollten Sie die Bezeichnung nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.
-   Da mehrere Verwendungen mehrdeutig sein können, insbesondere für eine weltweite Zielgruppe, verwenden Sie die Registerkarte Substantiv, um nur auf ein Registerkarten-Steuerelement zu verweisen. Für andere Verwendungszwecke sollten Sie die Bedeutung mit einem Deskriptor verdeutlichen: die Tab-Taste, eine Tabstopp Taste oder eine Registerkarten Markierung für das Lineal.

Beispiel: Klicken Sie **im Menü Extras** auf **Optionen**, und klicken Sie dann auf die Registerkarte **Ansicht** .

