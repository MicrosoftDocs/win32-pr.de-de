---
title: Links
description: Mit einem Link können Benutzer zu einer anderen Seite, einem anderen Fenster oder einem Hilfethema navigieren. Anzeigen einer Definition Initialisieren Sie einen Befehl. oder wählen Sie eine Option aus.
ms.assetid: a23748e4-b2dd-4b9f-9a7c-ff6533922c8c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 521f96146de535210d79814b375499ea34399179
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104558003"
---
# <a name="links"></a>Links

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mit einem *Link* können Benutzer zu einer anderen Seite, einem anderen Fenster oder einem Hilfethema navigieren. Anzeigen einer Definition Initialisieren Sie einen Befehl. oder wählen Sie eine Option aus. Ein Link ist Text oder eine Grafik, die darauf hinweist, dass darauf geklickt werden kann, in der Regel durch die Anzeige mithilfe der [Systemfarben](vis-color.md)"besuchte" oder "nicht besucht". Normalerweise werden auch Verknüpfungen unterstrichen, aber dieser Ansatz ist oft unnötig und ist nicht für die Verringerung der visuellen Übersichtlichkeit zu bevorzugen.

Wenn Benutzer auf einen Link zeigen, wird der Linktext wie unterstrichen angezeigt (falls er nicht bereits vorhanden ist), und die Form des Zeigers ändert sich in eine [Hand](inter-mouse.md).

Ein Textlink ist das leicht zu Gewichtungs Bare Steuerelement und wird häufig verwendet, um die visuelle Komplexität eines Entwurfs zu verringern.

> [!Note]  
> Richtlinien im Zusammenhang mit [Befehls Verknüpfungen](ctrl-command-links.md) und dem [Layout](vis-layout.md) werden in separaten Artikeln dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Der Link, der verwendet wird, um zu einer anderen Seite, einem anderen Fenster oder einem Hilfethema zu navigieren. Anzeigen einer Definition Initialisieren Sie einen Befehl. oder wählen Sie eine Option?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement.
-   **Wäre eine Befehls Schaltfläche eine bessere Wahl?** Verwenden Sie eine [Befehls Schaltfläche](ctrl-command-buttons.md) , wenn:
    -   Das-Steuerelement initiiert eine sofortige Aktion, einschließlich der Anzeige eines Fensters, und dieser Befehl bezieht sich auf den primären Zweck des Fensters.
    -   Ein Fenster wird angezeigt, um Eingaben zu erfassen oder auszuwählen, auch wenn für einen sekundären Befehl.
    -   Die Bezeichnung ist kurz und besteht aus vier oder weniger Wörtern. so wird das unschöne Aussehen von langen Schaltflächen vermieden.
    -   Der Befehl ist nicht Inline.
    -   Das-Steuerelement wird in einer Gruppe von anderen zugehörigen Befehls Schaltflächen angezeigt.
    -   Die Aktion ist destruktiv oder nicht rückgängig. Da Benutzer Verknüpfungen mit Navigation (und der Möglichkeit zum Zurücksetzen) verknüpfen, sind Links für Befehle mit erheblichen Konsequenzen nicht geeignet.
    -   Entsprechend stellt der Befehl in einem [Assistenten](win-wizards.md) oder [Task Ablauf](glossary.md)die Zusage dar. In solchen Fenstern empfehlen Befehls Schaltflächen die Zusage, während die Links die Navigation zum nächsten Schritt vorschlagen.

## <a name="design-concepts"></a>Entwurfskonzepte

**Erkennen von Verknüpfungen**

Links haben [keine Kosten](glossary.md)für die Verwendung, was bedeutet, **dass Ihre visuellen Eigenschaften nicht vorschlagen, wie Sie verwendet werden** und nur durch die Benutzeroberflächen verstanden werden. Links ohne Unterstreichung und linksystemfarben werden als normaler Text angezeigt. die einzige Möglichkeit, ihr Verhalten zu ermitteln, ist die Darstellung, der Kontext oder die Positionierung des Zeigers.

Vielleicht ist dieser Mangel an Aufforstung oft eine Motivation für die Verwendung von Verknüpfungen, da Sie so einfach erscheinen und dadurch die visuelle Komplexität eines Entwurfs reduziert werden. Links entfernen den visuell starken Frame, der von [Befehls](ctrl-command-buttons.md) Schaltflächen und von anderen Steuerelementen verwendeten Rahmen verwendet wird. Wenn Sie z. b. Befehls Schaltflächen verwenden, um primäre Befehle offensichtlich zu machen, können Sie Links für sekundäre Befehle auswählen, um Sie hervorzuheben.

Die Herausforderung besteht darin, genügend visuelle Hinweise beizubehalten, damit Benutzer die Verknüpfungen erkennen können. Die grundlegende Richtlinie besteht darin, **dass Benutzer in der Lage sein müssen, Links nur durch visuelle Überprüfung zu erkennen**

Benutzer können einen Link nur durch die visuelle Überprüfung erkennen, wenn der Link [Systemfarben](vis-color.md) und mindestens einen der folgenden visuellen Hinweise verwendet:

-   Unterstrichener Text.
-   Eine Grafik oder ein Aufzählungs Zeichen, z. b. mit dem [Text mit Symbol](#usage-patterns) Verknüpfungs Muster.
-   Platzierung innerhalb einer Standard Navigation,-Option oder-Befehls Position, z. b. der [Inhalts Bereich](glossary.md) eines Fensters oder einer Navigationsleiste, Menüleiste, Symbolleiste oder Seitenfuß.

Benutzer können auch einen Link anhand der visuellen Überprüfung mit den folgenden visuellen Hinweisen erkennen, aber diese Hinweise sind nicht selbst genug:

-   Text, der auf das Klicken klickt, z. b. ein Befehl, der mit einem imperativen Verb wie anzeigen, drucken, kopieren oder löschen beginnt.
-   Platzierung innerhalb eines Blocks von normalem Text.

Natürlich können Benutzer immer einen Link durch Interaktion ermitteln, indem Sie darauf zeigen oder klicken. Wenn die Ermittlung eines Links für wesentliche Aufgaben nicht erforderlich ist, können Sie diese Links hervorheben.

![Screenshot der grauen Bezeichnungen auf schwarzem Hintergrund ](images/ctrl-links-image1.png)

In diesem Beispiel sind Links zu den Nutzungsbedingungen, Marken und Datenschutzbestimmungen zu finden. Sie werden absichtlich von der hervorgehoben, da Sie für wichtige Aufgaben nicht erforderlich sind. Der einzige Hinweis darauf, dass Sie Verknüpfungen sind, besteht darin, dass Sie über einen Mauszeiger auf den Mauszeiger verfügen und sich am unteren Rand des Fensters in einem Standard Navigationsbereich befinden.

**Erstellen von Verknüpfungen speziell, relevant und vorhersagbar**

Der Linktext sollte das Ergebnis des Klickens auf den Link angeben.

Bestimmte Verknüpfungen sind für Benutzer wichtiger als allgemeine Links. verwenden Sie daher **Link Bezeichnungen, die bestimmte beschreibende Informationen über das Ergebnis des Klicks auf den Link** enthalten. Stellen Sie jedoch sicher, dass der Linktext nicht so spezifisch ist, dass er irreführend ist und die ordnungsgemäße Verwendung verhindert.

Präzisere Verknüpfungen sind eher als ausführliche Links lesbar. **Vermeiden Sie unnötige Text-und Detailinformationen.** Link Bezeichnungen müssen nicht umfassend sein.

So Werten Sie den Linktext aus:

-   Stellen Sie sicher, dass der Linktext die Szenarien widerspiegelt, die der Link unterstützt.
-   Stellen Sie sicher, dass die Ergebnisse der Verknüpfung vorhersagbar sind. Benutzer sollten nicht von den Ergebnissen überrascht werden.

**Wenn Sie nur zwei Dinge tun...**

1. Sorgen Sie dafür, dass Verknüpfungen von der visuellen Prüfung allein erkennbar sind Benutzer sollten nicht mit Ihrem Programm interagieren, um Links zu finden.

2. Verwenden Sie Links, die bestimmte beschreibende Informationen über das Ergebnis des Klicks auf den Link, und verwenden Sie so viel Text wie erforderlich. Benutzer sollten in der Lage sein, das Ergebnis einer Verknüpfung aus dem Linktext und dem optionalen [Infotipp](ctrl-tooltips-and-infotips.md)genau vorherzusagen.

## <a name="usage-patterns"></a>Verwendungsmuster

Links verfügen über mehrere funktionale Muster:



|                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Navigationslinks**<br/> Ein Link zum Navigieren zu einer anderen Seite oder einem anderen Fenster. <br/>                                                      | Wenn Sie auf den Link klicken, gelangen Sie zu einer anderen Seite, wie in einem Browserfenster oder Assistenten. oder zeigt ein neues Fenster an. Im Gegensatz zu Aufgaben Verknüpfungen initiiert die Navigation keine Aufgabe, sondern navigiert einfach zu einem anderen Ort oder geht mit einer bereits ausgeführten Aufgabe fort. Die Navigation impliziert Sicherheit, da der Benutzer jederzeit zurückkehren kann.<br/> Schlagzeilen<br/> Wenn Sie in diesem Beispiel auf den Link klicken, gelangen Sie zur Seite News-Schlagzeilen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Aufgaben Verknüpfungen**<br/> Ein Link, der verwendet wird, um einen neuen Befehl zu initiieren. <br/>                                                                        | Wenn Sie auf den Link klicken, wird entweder sofort ein Befehl oder ein Dialogfeld oder eine Seite angezeigt, um weitere Eingaben zu erfassen. Im Gegensatz zu Navigationslinks initiieren Aufgaben Verknüpfungen eine neue Aufgabe, anstatt eine vorhandene Aufgabe fortzusetzen. Tasks implizieren nicht, dass safetyusers mit einem zurück-Befehl nicht auf den vorherigen Zustand zurückgesetzt werden kann. Aufgaben Verknüpfungen werden so aufgerufen, um Verwechslungen mit [Befehls Verknüpfungen](ctrl-command-links.md)zu verhindern. <br/> Anmelden<br/> Wenn Sie in diesem Beispiel auf den Link klicken, wird ein Anmelde Befehl initiiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Hilfe Links**<br/> Ein Textlink, der verwendet wird, um ein Hilfethema anzuzeigen. <br/>                                                                     | Wenn Sie auf den Link klicken, wird ein Hilfeartikel in einem separaten Fenster angezeigt.<br/> Was ist ein sicheres Kennwort?<br/> Wenn Sie in diesem Beispiel auf den Link klicken, wird ein Hilfefenster mit dem angegebenen Thema angezeigt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Definitions Links**<br/> ein Textlink, der verwendet wird, um eine Definition in einem InfoTipp anzuzeigen, wenn der Benutzer auf den Link klickt oder darauf zeigt. <br/> | Dieses Muster eignet sich zum Definieren von Begriffen, die Ihren Benutzern möglicherweise nicht bekannt sind, ohne die Bildschirm Übersichtlichkeit hinzuzufügen.<br/> ![Screenshot des mit dem Mauszeiger angezeigten Infotipp ](images/ctrl-links-image2.png)<br/> In diesem Beispiel wird die Infotipp-Definition angezeigt. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Menü Verknüpfungen**<br/> eine Reihe von Aufgaben Verknüpfungen, die zum Erstellen eines Menüs verwendet werden. <br/>                                                                    | Da der Kontext des Menüs einen Satz von Links anzeigt, wird der Text in der Regel nicht unterstrichen (mit Ausnahme von Hover) und verwendet möglicherweise nicht die Farben des Link Systems.<br/> ![Screenshot eines Satzes von Links ](images/ctrl-links-image3.png)<br/> In diesem Beispiel erstellt ein Satz von Links ein Menü.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Options Verknüpfungen**<br/> eine ausgewählte Option oder Ihr Platzhalter, bei der auf den Link geklickt wird, um diese Option zu ändern.<br/>       | im Gegensatz zu regulären Text Verknüpfungen ändert der Link seinen Text so, dass er die aktuell ausgewählte Option widerspiegelt, und wird immer mit der nicht besuchten Linkfarbe gezeichnet. <br/> ![Screenshot einer Regel im Outlook-Regel-Assistenten ](images/ctrl-links-image4.png)<br/> im Beispiel auf der linken Seite wird eine Regel des Microsoft Outlook-Regel-Assistenten mit Platzhalter Optionen angezeigt. Nachdem Benutzer auf die Links klicken und einige Optionen ausgewählt haben, aktualisiert das Rechte Beispiel den Linktext, um die Ergebnisse anzuzeigen.<br/> die Verwendung von Options Verknüpfungen eignet sich besonders, wenn die Optionen ein Variablen Format aufweisen. <br/> ![Screenshot einer geänderten Regel im Regelerstellungs-Assistenten ](images/ctrl-links-image5.png)<br/> Das Beispiel auf der rechten Seite zeigt, dass Outlook-Regeln ein Variablen Format aufweisen. <br/> ![Screenshot der Textänderungen in der Dropdown Liste ](images/ctrl-links-image6.png)<br/> Das Beispiel auf der linken Seite zeigt einen Options Link. Dies wird zu einer Dropdown Liste, wenn Sie ausgewählt ist, wie auf der rechten Seite dargestellt.<br/> |



 

Links haben auch mehrere Präsentations Muster:



|                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nur-Text-Links**<br/> besteht nur aus Text. <br/>                                      | Diese Präsentation ist die flexibelste, da Sie überall, einschließlich [Inline](glossary.md), verwendet werden kann.<br/> ![Screenshot des blauen linktexts ](images/ctrl-links-image7.png)<br/> In diesem Beispiel identifiziert die Textfarbe einen Inline Link eindeutig.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Text mit Symbol Verknüpfungen**<br/> Text mit einem vorangehenden Symbol, das seine Funktion angibt.<br/> | Da die Grafik einen zusätzlichen visuellen Hinweis auf einen Link enthält, ist es einfacher, als Link zu erkennen, der nicht unterstrichen ist. Dieses Muster verwendet in der Regel ein 16x16-Pixel-Symbol.<br/> ![Screenshot der Liste mit vier Links mit Symbolen ](images/ctrl-links-image8.png)<br/> in diesem Beispiel stellen die Symbole einen zusätzlichen visuellen Hinweis auf einen Link dar.<br/> ![Screenshot des Wiedergabe Befehls mit kleinem Dreieck ](images/ctrl-links-image9.png)<br/> In diesem Beispiel gibt das Symbol für das standardmäßige dreieckige Spiel an, dass dieser Text ein-Befehl ist.<br/>                                                                                                                                     |
| **Links nur für Grafiken**<br/> besteht nur aus einer Grafik.<br/>                               | aufgrund des Mangels an Text Verknüpfungen gibt es keine Verknüpfungs Farbe oder einen Unterstrich, um den Link anzugeben. Diese Links hängen entweder von dem Grafik Entwurf ab, um zu klicken, oder Text innerhalb der Grafik, der eine Aktion vorschlägt, wenn Benutzer auf klicken. reine Grafik Links haben manchmal einen Mouseover-Effekt, um den Link anzugeben. Diese Vorgehensweise ist hilfreich, aber nicht allein durch die visuelle Überprüfung erkennbar.<br/> ![Screenshot des Symbols mit einem Link zum Auswählen von Maus Zeigern ](images/ctrl-links-image10.png)<br/> In diesem Beispiel ist der Link nicht allein durch die visuelle Überprüfung erkennbar.<br/> **Aufgrund der möglichen Erkennungs-und Lokalisierungs Probleme werden nur-Grafik-links als einzige Möglichkeit zum Ausführen einer Aufgabe empfohlen.** <br/> |



 

## <a name="guidelines"></a>Richtlinien

### <a name="interaction"></a>Interaktion

-   **Zeigen Sie einen ausgelasteten Zeiger an, wenn das Ergebnis des Klickens auf einen Link nicht sofort ist.** Ohne Feedback können Benutzer davon ausgehen, dass das Klicken nicht durchgeführt wurde, und dann erneut auf klicken.

### <a name="color"></a>Color

-   **Verwenden Sie das Design, oder verknüpfen Sie Systemfarben für besuchte und nicht besuchte Links.** Die Bedeutung dieser Farben ist in allen Programmen konsistent. Wenn Benutzer aus irgendeinem Grund diese Farben nicht mögen (z. b. aus Barrierefreiheits Gründen), können Sie Sie selbst ändern.
-   **Verwenden Sie für Navigations Verknüpfungen verschiedene Farben für besuchte und nicht besuchte Links.** Behalten Sie den Verlauf der besuchten Verknüpfungen nur für die Dauer der Programm Instanz bei. Die besuchte Farbe ist wichtig, um anzugeben, wo Benutzer bereits waren, sodass Sie nicht versehentlich die gleichen Seiten wiederholt besuchen.
-   **Verwenden Sie für andere Linktypen nicht die besuchte Linkfarbe.** Zum Identifizieren von "besuchten" Befehlen ist nicht ausreichend Wert vorhanden, z. b..
-   **Keinen Text, der kein Link ist, weil Benutzer möglicherweise davon ausgehen, dass es sich um einen Link handelt.** Verwenden Sie Fett oder einen grauen Farbton, in dem Sie andernfalls farbigen Text verwenden würden.
-   **Ausnahme**: Sie können farbigen Text verwenden, wenn alle Links entweder unterstrichen oder in standardmäßigen Navigations-oder Befehlspositionen abgelegt werden.

    **Falsch:**

    ![Screenshot der Energieplan Meldung mit blauem Text ](images/ctrl-links-image11.png)

    In diesem Beispiel wird blauer Text fälschlicherweise für Text verwendet, der kein Link ist.

-   **Verwenden Sie Hintergrundfarben im Gegensatz zu den Verknüpfungs Farben.** Die [Farbe des Fenstersystems](vis-color.md) ist immer eine gute Wahl.

    **Falsch:**

    ![Screenshot des blauen linktexts im blauen Hintergrund ](images/ctrl-links-image12.png)

    In diesem Beispiel stellt die Hintergrundfarbe einen schlechten Kontrast in Bezug auf die Linkfarbe dar.

### <a name="underlining"></a>Heben

-   **Stellen Sie für Links, die zum Ausführen einer primären Aufgabe erforderlich sind, visuelle Hinweise bereit, damit Benutzer Links nur durch die visuelle Überprüfung erkennen können.** Zu diesen Hinweisen zählen Unterstreichung, Grafiken oder Aufzählungs Zeichen und Standard-Verknüpfungs Positionen. Benutzer müssen nicht auf ein Objekt zeigen, oder Sie können darauf klicken, um zu ermitteln, ob es sich um einen Link handelt. Verwenden Sie unterstrichenen Text, wenn der Link aus seinem Kontext nicht ersichtlich ist.
-   **Unterstreichen Sie keinen Link, weil Benutzer möglicherweise davon ausgehen, dass es sich um einen Link handelt.** Verwenden Sie kursiv, wo Sie andernfalls unterstrichenen Text verwenden würden. Reservieren Sie nur auf Links.
-   **Beim Drucken sollten Sie keine Unterstriche oder Verknüpfungs Farben drucken.** Gedruckte Links haben keinen Wert und können potenziell verwirrend sein.

### <a name="text-with-icon-links"></a>Text mit Symbol Verknüpfungen

-   **Verwenden Sie das Pfeilsymbol nur für Befehls Verknüpfungen.** Reguläre Verknüpfungen sollten das Pfeilsymbol nur verwenden, wenn Sie als Ersatz für [Befehls Verknüpfungen](ctrl-command-links.md) in Windows XP verwendet werden.
-   **Platzieren Sie das Symbol links neben dem Text.** Das Symbol muss den Text visuell darstellen.

**Richtig:**

![Screenshot des Symbols für den vorangehenden Text ](images/ctrl-links-image13.png)

**Falsch:**

![Screenshot des Symbols nach Text ](images/ctrl-links-image14.png)

Im falschen Beispiel führt das Symbol nicht zu dem Text.

-   **Klicken Sie auf das Symbol, und klicken Sie auf den Text, um das Ergebnis zu klicken.** Andernfalls wäre es unerwartet und verwirrend.

### <a name="graphics-only-links"></a>Links nur für Grafiken

-   **Verwenden Sie keine reinen Grafik links.** Benutzer haben Sie als Links und Text in der Grafik (bei der Anzeige Ihrer Aktion, wenn Sie darauf geklickt haben) schwer zu erkennen. dadurch entsteht ein Lokalisierungs Problem.

### <a name="navigation-links"></a>Navigationslinks

-   **Stellen Sie sicher, dass für Navigationslinks keine Verpflichtung erforderlich ist** Benutzer sollten immer in der Lage sein, zum ursprünglichen Zustand zurückzukehren, indem Sie entweder für die direkte Navigation oder den Abbruch ein neues Fenster verwenden.
-   **Verknüpfung mit spezifischem Inhalt anstelle von allgemeinem Inhalt.** Beispielsweise ist es besser, mit dem relevanten Abschnitt eines Dokuments zu verknüpfen, als mit dem Anfang verknüpft werden zu können.
-   **Verwenden Sie einen Link nur, wenn das verknüpfte Material relevant, hilfreich und nicht redundant ist.** Verwenden Sie die Unterhaltung in Navigationslinks nicht nur, da dies möglich ist.
-   **Wenn ein Link zu einer externen Site navigiert, platzieren Sie die URL im Infotipp,** damit Benutzer das Ziel des Links ermitteln können.
-   **Verknüpfen Sie nur das erste Vorkommen des linktexts.** Redundante Verknüpfungen sind unnötig und können den Text schwer lesbar machen.

    **Richtig:**

    Der Ordner "Bilder" macht das Freigeben von Bildern leicht. Sie können die Aufgaben in Bildern verwenden, um Ihre Bilder per e-Mail zu senden oder an einem sicheren, privaten Speicherort im Web zu veröffentlichen. Sie können Ihre Bilder auch direkt aus dem Ordner "Bilder" Drucken.

    **Falsch:**

    Der Ordner "Bilder" macht das Freigeben von Bildern leicht. Sie können die Aufgaben in Bildern verwenden, um Ihre Bilder per e-Mail zu senden oder an einem sicheren, privaten Speicherort im Web zu veröffentlichen. Sie können Ihre Bilder auch direkt aus dem Ordner "Bilder" Drucken.

    Im richtigen Beispiel ist nur das erste Vorkommen des relevanten Texts verknüpft.

    **Ausnahmen:**

    -   **Wenn eine Anweisung über einen Link verfügt, platzieren Sie den Link in der Anweisung.**

        Die Verwendung von sicheren Kenn Wörtern ist äußerst wichtig. Weitere Informationen finden Sie unter Sichere Kennwörter.

        In diesem Beispiel befindet sich der Link in der Anweisung anstelle des ersten Vorkommens.

    -   **Link zu späteren vorkommen, wenn Sie weit vom ersten vorkommen.** Beispielsweise können Sie redundant in verschiedenen Abschnitten innerhalb eines Hilfe Themas verknüpfen.

### <a name="task-links"></a>Aufgaben Verknüpfungen

-   **Verwenden Sie Aufgaben Verknüpfungen für Befehle, die nicht destruktiv oder leicht umkehrbar sind.** Da Benutzer Verknüpfungen mit Navigation (und der Möglichkeit zum Zurücksetzen) verknüpfen, sind Links für Befehle mit erheblichen Konsequenzen nicht geeignet. Befehle, die ein Dialogfeld oder eine Bestätigung anzeigen, sind eine gute Wahl.

    **Richtig:**

    Start

    Stop

    **Falsch:**

    Datei löschen

    Im falschen Beispiel ist der Befehl destruktiv.

### <a name="menu-links"></a>Menü Verknüpfungen

-   **Gruppieren verwandter Navigations-und Aufgaben Verknüpfungen in Menüs.** Ein Menü mit verknüpften Links, das in einem Standard Navigations-oder Befehls Speicherort platziert wird, erleichtert das Auffinden und verstehen der Links, als wenn Sie getrennt platziert werden.
-   **Entfernen Sie Menü Verknüpfungen, die für Auswahl abhängige Menüs nicht zutreffen.** Deaktivieren Sie diese nicht. Dadurch entfällt die Übersichtlichkeit, und Benutzer verpassen keine Links, die eine Auswahl erfordern.
-   **Deaktivieren Sie für Auswahl unabhängige Menüs nicht geltende Menü Verknüpfungen.** Entfernen Sie Sie nicht. Auf diese Weise werden die Menüs stabiler und solche Verknüpfungen leichter zu finden.

    ![Screenshot des Dialog Felds mit dem Menübefehl "abgeblendet" ](images/ctrl-links-image15.png)

    In diesem Beispiel aus Windows Update wird ein Update ausgeführt, sodass der Befehl "nach Updates suchen" deaktiviert ist, anstatt entfernt zu werden.

### <a name="link-infotips"></a>Linkinfotipps

-   Wenn für einen Link Weitere Erläuterungen erforderlich sind, **Geben Sie die Erläuterung entweder in einer ergänzenden Erklärung in einem separaten Text Steuerelement oder in** einem [Infotipp](ctrl-tooltips-and-infotips.md)an, aber nicht in beiden. Verwenden Sie vollständige Sätze und endinterpunktions Zeichen. Beides ist nicht erforderlich, wenn der Text identisch ist, und verwirrend, wenn der Text anders ist.

    ![Screenshot des Links mit zusätzlichem Text ](images/ctrl-links-image16.png)

    In diesem Beispiel enthält eine ergänzende Erklärung Weitere Informationen zum Link.

    ![Screenshot des Links mit Infotipp ](images/ctrl-links-image17.png)

    In diesem Beispiel enthält ein Infotipp Weitere Informationen.

-   **Geben Sie keinen Infotipp an, der lediglich eine erneute Anweisung des linktexts ist.**

    **Falsch:**

    ![Screenshot des Links mit redundantem Infotipp ](images/ctrl-links-image18.png)

    In diesem Beispiel stellt der Infotipp eine Gefahr dar, dass Benutzer durch seine wiederholte Aktivität lästig werden.

## <a name="text"></a>Text

-   Weisen Sie keinen [Zugriffsschlüssel](glossary.md)zu. Auf Links wird mithilfe der Tab-Taste zugegriffen.
-   **Verwenden Sie Links, die bestimmte beschreibende Informationen über das Ergebnis des Klicks auf den Link**, und verwenden Sie so viel Text wie erforderlich. Der Linktext sollte das Ergebnis des Klickens auf den Link angeben. **Benutzer sollten in der Lage sein, das Ergebnis einer Verknüpfung aus dem Linktext und dem optionalen infotip genau vorherzusagen.**

    **Falsch:**

    ![Screenshot eines Sicherheitshinweis-Warnungs Links ](images/ctrl-links-image19.png)

    In diesem Beispiel ist die Bezeichnung zu allgemein, auch wenn der Link wichtig ist. Benutzer werden wahrscheinlich auf einen spezifischeren Link klicken.

-   Für Inline Verknüpfungen:
    -   Beibehalten der Groß-und Kleinschreibung des Texts.
    -   Fügen Sie keine Endpunktzeile in den Link ein, es sei denn, der Text ist eine Frage.
    -   Verknüpfen Sie den relevantesten Teil des Texts, und wählen Sie Linktext aus, der groß genug ist, um einfach zu klicken.

        **Richtig:**

        Wechseln Sie zu einer Newsgroup.

        **Falsch:**

        Wechseln Sie zu einer Newsgroup.

        In diesen Beispielen ist "Go" nicht der relevanteste Teil des Texts, und er ist nicht groß genug, um ein gutes Klick Ziel zu erreichen, während "Newsgroup" ist.

    -   **Vermeiden Sie, zwei unterschiedliche Inline Verknüpfungen nebeneinander zu platzieren.** Benutzer sind wahrscheinlich der Meinung, dass es sich um einen einzelnen Link handelt.

        **Falsch:**

        Weitere Informationen finden Sie unter Richtlinien für die Benutzerfreundlichkeit.

        In diesem Beispiel sind "UX" und "Richtlinien" zwei unterschiedliche Links.

-   Für unabhängige Verknüpfungen (nicht Inline):
    -   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
    -   Verwenden Sie keine endpunktierungen, es sei denn, der Link ist eine Frage.
    -   Verwenden Sie den gesamten Text als Link.
-   Verwenden Sie Links, die sich deutlich von den anderen Links auf dem Bildschirm unterscheiden. Benutzer sollten in der Lage sein, Verknüpfungs Ziele genau vorherzusagen und zu unterscheiden.

    **Falsch:**

    Antivirensoftware suchen

    Antivirussoftware

    **Richtig:**

    Informieren, ob Antivirussoftware installiert ist

    Installieren von Antivirensoftware

    Im falschen Beispiel ist der Unterschied zwischen den beiden Links unklar.

-   Fügen Sie den Link Text nicht hinzu, oder klicken Sie hier. Dies ist nicht erforderlich, da ein Link auf Klicken bedeutet. Klicken Sie hier, und übermitteln Sie hier allein keine Informationen über den Link, wenn Sie von einer Bildschirm Sprachausgabe gelesen werden.

    **Falsch:**

    Klicken Sie hier, um zu Beschreibungen.

    **Richtig:**

    BESCHREIBUNG

    In den falschen Beispielen lautet "hier klicken", ohne zu sagen, und es werden keine Informationen über den Link übermittelt.

**Navigationslinks**

-   **Starten Sie den Link mit einem Substantiv, und beschreiben Sie eindeutig, wo Sie auf den Link klicken.** Verwenden Sie keine Interpunktion am Ende. Gelegentlich müssen Sie möglicherweise Navigationslinks mit einem Verb starten, aber keine Verben verwenden, die die Navigation wiederholen, die bereits durch die Tatsache der Verknüpfung impliziert ist, wie z. b. "View", "Open" oder "Gehe zu".
-   **Einen Navigations Link als URL präsentieren, wenn er zu einer Webseite navigiert, und Sie erwarten, dass die Ziel Benutzer die URL zurückgeben und in einen Browser eingeben.** Wenn möglich, sollten Sie diese URLs so entwerfen, dass Sie kurz und leicht zu merken sind.
-   **Wenn der Link eine URL zu einer Website enthält, beginnend mit "www", lassen Sie den Namen des https://-Protokolls aus, und verwenden Sie Kleinbuchstaben.**

    **Falsch:**

    https://www.microsoft.com

    `www.microsoft.com`

    **Richtig:**

    microsoft.com

    In den falschen Beispielen sind "https://" und "www" ohne Aussage.

**Aufgaben Verknüpfungen**

-   **Starten Sie den Link mit einem imperativen Verb, und beschreiben Sie die Aufgabe, die der Link ausführt, eindeutig.** Verwenden Sie keine Interpunktion am Ende.
-   **Beenden Sie den Link mit einem Ellipsen, wenn der Befehl für einen erfolgreichen Abschluss zusätzliche Informationen (einschließlich einer Bestätigung) benötigt.** Verwenden Sie kein Auslassungs Zeichen, wenn beim erfolgreichen Abschluss der Aufgabe ein anderes Fenster nur angezeigt werden soll, wenn zusätzliche Informationen benötigt werden, um die Aufgabe auszuführen.

    Drucken...

    In diesem Beispiel wird der Druck... Befehls Link zeigt ein Druck Dialogfeld an, um weitere Informationen zu sammeln.

    Drucken

    Im Gegensatz dazu druckt ein Link zum Drucken eines Befehls eine einzelne Kopie eines Dokuments auf dem Standarddrucker, ohne dass weitere Benutzerinteraktionen vorhanden sind.

    Die **korrekte Verwendung von Ellipsen ist wichtig, um anzugeben, dass Benutzer vor dem Ausführen der Aufgabe weitere Optionen treffen oder die Aufgabe vollständig abbrechen können**. Der visuelle Hinweis, der von einem Ellipsen angeboten wird, ermöglicht es Benutzern, Ihre Software ohne Angst zu untersuchen.

-   **Beenden Sie ggf. eine Aufgaben Verknüpfung mit "Now", um Sie von einem Navigations Link zu unterscheiden.**

    Herunterladen von Dateien

    Dateien jetzt herunterladen

    In diesem Beispiel navigiert "Dateien herunterladen" zu einer Seite zum Herunterladen von Dateien, während der Befehl "Dateien jetzt herunterladen" tatsächlich den Befehl ausführt.

**Hilfe Links**

Richtlinien und Beispiele finden Sie in der [Hilfe](winenv-help.md).

**Linkinfotipps**

-   Verwenden Sie vollständige und endliche Satzzeichen.

Weitere Richtlinien und Beispiele finden Sie unter Quick [Infos und infotips](ctrl-tooltips-and-infotips.md).

## <a name="documentation"></a>Dokumentation

Beim Verweis auf Verknüpfungen:

-   Verwenden Sie den genauen Linktext, einschließlich der Groß-/Kleinschreibung, aber nicht die Auslassungs Punkte.
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie klicken.
-   Formatieren Sie den Linktext, wenn möglich, mit fett formatiertem Text. Andernfalls sollten Sie den Linktext nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Klicken Sie auf **Computer scannen**, um die Überprüfung zu starten.

 

