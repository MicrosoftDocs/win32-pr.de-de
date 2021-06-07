---
title: Links
description: Mit einem Link können Benutzer zu einer anderen Seite, einem anderen Fenster oder einem anderen Hilfethema navigieren. Eine Definition anzeigen; initiieren Sie einen Befehl. oder wählen Sie eine Option aus.
ms.assetid: a23748e4-b2dd-4b9f-9a7c-ff6533922c8c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 161313008612d04b5009942f82f662888d1ffd35
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524255"
---
# <a name="links"></a>Links

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Mit einem *Link* können Benutzer zu einer anderen Seite, einem anderen Fenster oder einem anderen Hilfethema navigieren. Eine Definition anzeigen; initiieren Sie einen Befehl. oder wählen Sie eine Option aus. Ein Link ist text oder eine Grafik, die angibt, dass darauf geklickt werden kann. Dies geschieht in der Regel durch Anzeige mit den Systemfarben für den besuchten oder nicht aufgerufenen [Link.](vis-color.md) Links werden in der Regel auch unterstrichen, aber dieser Ansatz ist oft unnötig und wird nicht bevorzugt, um visuelle Überladen zu reduzieren.

Wenn Benutzer mit dem Mauszeiger auf einen Link zeigen, wird der Linktext als unterstrichen angezeigt (falls dies noch nicht dere war), und die Zeigerform ändert sich in eine [Hand.](inter-mouse.md)

Ein Textlink ist das leichtste klickbare Steuerelement und wird häufig verwendet, um die visuelle Komplexität eines Entwurfs zu reduzieren.

> [!Note]  
> Richtlinien im Zusammenhang mit [Befehlslinks](ctrl-command-links.md) und [Layout](vis-layout.md) werden in separaten Artikeln vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Der Link, der zum Navigieren zu einer anderen Seite, zu einem anderen Fenster oder zu einem anderen Hilfethema verwendet wird. Eine Definition anzeigen; initiieren Sie einen Befehl. oder eine Option auswählen?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement.
-   **Wäre eine Befehlsschaltfläche eine bessere Wahl?** Verwenden Sie eine [Befehlsschaltfläche,](ctrl-command-buttons.md) wenn:
    -   Das Steuerelement initiiert eine sofortige Aktion, einschließlich der Anzeige eines Fensters, und dieser Befehl bezieht sich auf den Hauptzweck des Fensters.
    -   Ein Fenster wird angezeigt, um Eingaben zu erfassen oder Entscheidungen zu treffen, auch wenn für einen sekundären Befehl erforderlich ist.
    -   Die Bezeichnung ist kurz und besteht aus vier oder weniger Wörtern und vermeidet so die umständliche Darstellung langer Schaltflächen.
    -   Der Befehl ist nicht inline.
    -   Das Steuerelement wird in einer Gruppe anderer verwandter Befehlsschaltflächen angezeigt.
    -   Die Aktion ist destruktiv oder kann nicht rückgängig gemacht werden. Da Benutzer Links der Navigation zuordnen (und die Möglichkeit zum Back-Out) haben, sind Links nicht für Befehle geeignet, die erhebliche Folgen haben.
    -   Auf ähnliche Weise stellt der Befehl in einem [Assistenten](win-wizards.md) oder [Taskflow](glossary.md)die Verpflichtung dar. In solchen Fenstern deuten Befehlsschaltflächen auf Verpflichtung hin, während Links die Navigation zum nächsten Schritt empfehlen.

## <a name="design-concepts"></a>Entwurfskonzepte

**Erkennbarmachen von Links**

Links bieten keine [Angebote,](glossary.md)was bedeutet, dass **ihre visuellen Eigenschaften nicht vorschlagen, wie sie verwendet werden** und nur durch Erfahrung verstanden werden. Verknüpfungen ohne Unterstreichung und Linksystemfarben werden als normaler Text angezeigt. Die einzige Möglichkeit, ihr Verhalten zu ermitteln, ist ihre Darstellung, ihr Kontext oder die Positionierung des Zeigers darauf.

Überraschenderweise ist dieser Mangel an Erschwinglichkeit oft ein Beweggrund für die Verwendung von Links, da sie so einfach erscheinen und dadurch die visuelle Komplexität eines Entwurfs reduzieren. Links entfernen den visuell starken Frame, der von [Befehlsschaltflächen](ctrl-command-buttons.md) und Rahmen verwendet wird, die von anderen Steuerelementen verwendet werden. Während Sie beispielsweise Befehlsschaltflächen verwenden können, um primäre Befehle offensichtlich zu machen, können Sie Links für sekundäre Befehle auswählen, um sie zu deaktivieren.

Die Herausforderung besteht dann darin, genügend visuelle Hinweise zu erhalten, damit Benutzer die Links erkennen können. Die grundlegende Richtlinie besteht darin, dass **Benutzer Links nur durch visuelle Überprüfung erkennen können müssen, wenn sie nicht mit dem Mauszeiger auf ein Objekt zeigen oder darauf klicken müssen, um festzustellen, ob es sich um einen Link handelt.**

Benutzer können einen Link allein durch visuelle Überprüfung erkennen, wenn der Link die [Linksystemfarben](vis-color.md) und mindestens einen der folgenden visuellen Hinweise verwendet:

-   Unterstrichener Text.
-   Eine Grafik oder aufzählungszeichen, z. B. mit dem [Text mit Symbollinkmuster.](#usage-patterns)
-   Platzierung innerhalb einer Standardnavigations-, Options- oder Befehlsposition, z. B. im [Inhaltsbereich](glossary.md) eines Fensters oder in einer Navigationsleiste, Menüleiste, Symbolleiste oder Seitenfußzeile.

Benutzer können einen Link auch durch visuelle Überprüfung mit den folgenden visuellen Hinweisen erkennen, aber diese Hinweise reichen nicht allein aus:

-   Text, der klickt, z. B. ein Befehl, der mit einem imperativen Verb wie Anzeigen, Drucken, Kopieren oder Löschen beginnt.
-   Platzierung innerhalb eines Blocks mit normalem Text.

Natürlich können Benutzer einen Link immer durch Interaktion bestimmen, indem sie entweder mit dem Mauszeiger zeigen oder klicken. Wenn die Ermittlung eines Links für keine wichtigen Aufgaben erforderlich ist, können Sie diese Links deaktivieren.

![Screenshot von grauen Bezeichnungen auf schwarzem Hintergrund ](images/ctrl-links-image1.png)

In diesem Beispiel sind "Kontakt aufnehmen", "Nutzungsbedingungen", "Marken" und "Datenschutzbestimmungen" Links. Sie werden absichtlich de-emphasized, da sie für keine wichtigen Aufgaben erforderlich sind. Die einzigen Hinweise darauf, dass es sich um Links handelt, sind, dass sie mit dem Mauszeiger darauf zeigen und in einem Standardnavigationsbereich am unteren Rand des Fensters positioniert sind.

**Erstellen spezifischer, relevanter und vorhersagbarer Links**

Linktext sollte das Ergebnis des Klickens auf den Link angeben.

Bestimmte Links sind für Benutzer überzeugender als allgemeine Links. Verwenden Sie daher **Linkbezeichnungen, die spezifische beschreibende Informationen über das Ergebnis des Klickens auf den Link liefern.** Stellen Sie jedoch sicher, dass Ihr Linktext nicht so spezifisch ist, dass er irreführend ist, und raten Sie von der ordnungsgemäßen Verwendung ab.

Präzise Links werden wahrscheinlicher gelesen als ausführliche Links. **Vermeiden Sie unnötigen Text und details.** Linkbezeichnungen müssen nicht umfassend sein.

So werten Sie Ihren Linktext aus:

-   Stellen Sie sicher, dass der Linktext die Szenarien widerspiegelt, die der Link unterstützt.
-   Stellen Sie sicher, dass die Ergebnisse des Links vorhersagbar sind. Benutzer sollten sich nicht über die Ergebnisse wundern.

**Wenn Sie nur zwei Dinge tun...**

1. Machen Sie Links allein durch die visuelle Überprüfung sichtbar. Benutzer sollten nicht mit Ihrem Programm interagieren müssen, um Links zu finden.

2. Verwenden Sie Links, die spezifische beschreibende Informationen über das Ergebnis des Klickens auf den Link enthalten, und verwenden Sie dabei so viel Text wie nötig. Benutzer sollten in der Lage sein, das Ergebnis eines Links aus dem Linktext und dem optionalen Infotip genau [vorherzusagen.](ctrl-tooltips-and-infotips.md)

## <a name="usage-patterns"></a>Verwendungsmuster

Links weisen mehrere funktionale Muster auf:



|    Verwendung                  |    Beispiel   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Navigationslinks**<br/> Ein Link, der zum Navigieren zu einer anderen Seite oder zu einem anderen Fenster verwendet wird. <br/>                                                      | Wenn Sie auf den Link klicken, wird direkt zu einer anderen Seite navigiert, wie in einem Browserfenster oder Assistenten. oder zeigt ein neues Fenster an. Im Gegensatz zu Aufgabenlinks initiiert die Navigation keine Aufgabe, sondern navigiert einfach zu einer anderen Stelle oder fährt mit einer Aufgabe fort, die bereits ausgeführt wird. Die Navigation impliziert Sicherheit, da der Benutzer jederzeit zurückkehren kann.<br/> News-Überschriften<br/> In diesem Beispiel wird durch Klicken auf den Link zur Seite News-Überschriften navigiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Aufgabenlinks**<br/> Ein Link, der zum Initiieren eines neuen Befehls verwendet wird. <br/>                                                                        | Durch Klicken auf den Link wird entweder sofort ein Befehl ausgeführt, oder es wird ein Dialogfeld oder eine Seite angezeigt, um weitere Eingaben zu erfassen. Im Gegensatz zu Navigationslinks initiieren Tasklinks eine neue Aufgabe, anstatt mit einer vorhandenen Aufgabe fortzufahren. Aufgaben implizieren keine SicherheitUser können nicht mit einem Back-Befehl auf den vorherigen Zustand zurückgesetzt werden. Aufgabenlinks werden so aufgerufen, um Verwechslungen mit [Befehlslinks](ctrl-command-links.md)zu vermeiden. <br/> Anmelden<br/> In diesem Beispiel wird durch Klicken auf den Link ein Anmeldebefehl initiiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Hilfelinks**<br/> Ein Textlink zum Anzeigen eines Hilfethemas. <br/>                                                                     | Wenn Sie auf den Link klicken, wird ein Hilfeartikel in einem separaten Fenster angezeigt.<br/> Was ist ein sicheres Kennwort?<br/> In diesem Beispiel wird durch Klicken auf den Link ein Hilfefenster mit dem angegebenen Thema angezeigt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Definitionslinks**<br/> Ein Textlink, der verwendet wird, um eine Definition in einer Infotip anzuzeigen, wenn der Benutzer auf den Link klickt oder darauf zeigt. <br/> | Dieses Muster eignet sich zum Definieren von Begriffen, die Ihren Benutzern möglicherweise nicht bekannt sind, ohne den Bildschirm zu überladen.<br/> ![Screenshot der Infotip, die mit dem Mauszeigerzeiger angezeigt wird ](images/ctrl-links-image2.png)<br/> In diesem Beispiel wird die InfoTip-Definition angezeigt. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Menülinks**<br/> eine Reihe von Aufgabenlinks, die zum Erstellen eines Menüs verwendet werden. <br/>                                                                    | da der Kontext des Menüs einen Satz von Links angibt, wird der Text in der Regel nicht unterstrichen (mit Ausnahme des Mauszeigers) und verwendet möglicherweise nicht die Linksystemfarben.<br/> ![Screenshot einer Gruppe von Links ](images/ctrl-links-image3.png)<br/> In diesem Beispiel erstellt eine Gruppe von Links ein Menü.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Optionslinks**<br/> eine ausgewählte Option oder deren Platzhalter, wobei durch Klicken auf den Link ein Befehl aufgerufen wird, um diese Option zu ändern.<br/>       | Im Gegensatz zu regulären Textlinks ändert der Link seinen Text entsprechend der aktuell ausgewählten Option und wird immer mit der nicht überwachten Linkfarbe gezeichnet. <br/> ![Screenshot einer Regel im Outlook-Regel-Assistenten ](images/ctrl-links-image4.png)<br/> Das Beispiel auf der linken Seite zeigt eine Regel aus dem Microsoft Outlook-Regel-Assistenten mit Platzhalteroptionen. Nachdem Benutzer auf die Links geklickt und einige Optionen ausgewählt haben, aktualisiert das rechte Beispiel den Linktext, um die Ergebnisse zu zeigen.<br/> Die Verwendung von Optionslinks ist besonders geeignet, wenn die Optionen ein Variablenformat haben. <br/> ![Screenshot einer geänderten Regel im Regel-Assistenten ](images/ctrl-links-image5.png)<br/> Das Beispiel auf der rechten Seite zeigt, dass Outlook-Regeln ein Variablenformat haben. <br/> ![Screenshot der Änderung des Texts in die Dropdownliste ](images/ctrl-links-image6.png)<br/> Das Beispiel auf der linken Seite zeigt einen Optionslink. Sie wird bei Auswahl zu einer Dropdownliste, wie auf der rechten Seite dargestellt.<br/> |



 

Links verfügen auch über mehrere Präsentationsmuster:



|    Verwendung                                 |    Beispiel                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nur-Text-Links**<br/> besteht nur aus Text. <br/>                                      | diese Präsentation ist die flexibelste, da sie überall verwendet werden kann, einschließlich [inline.](glossary.md)<br/> ![Screenshot von blauem Linktext ](images/ctrl-links-image7.png)<br/> In diesem Beispiel identifiziert die Textfarbe eindeutig einen Inlinelink.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Text mit Symbollinks**<br/> Text mit einem vorangehenden Symbol, das seine Funktion angibt.<br/> | Da die Grafik einen zusätzlichen visuellen Hinweis auf einen Link bietet, ist es einfacher, als Link zu erkennen als ein nicht unterstrichener Nur-Text-Link. Dieses Muster verwendet in der Regel ein Symbol mit 16 x 16 Pixeln.<br/> ![Screenshot der Liste mit vier Links mit Symbolen ](images/ctrl-links-image8.png)<br/> in diesem Beispiel stellen die Symbole eine zusätzliche visuelle Angabe eines Links zur Verfügung.<br/> ![Screenshot des Wiedergabebefehls mit kleinem Dreieck ](images/ctrl-links-image9.png)<br/> In diesem Beispiel gibt das standardmäßige dreieckige Wiedergabesymbol an, dass dieser Text ein Befehl ist.<br/>                                                                                                                                     |
| **Links nur für Grafiken**<br/> besteht nur aus einer Grafik.<br/>                               | Wenn kein Textlink angezeigt wird, gibt es keine Linkfarbe oder -unterstreichung, um den Link anzugeben. Diese Links hängen entweder vom grafischen Design ab, um das Klicken zu empfehlen, oder vom Text in der Grafik, der eine Aktion vorschlägt, wenn Benutzer klicken. Nur grafische Links weisen manchmal einen Mouse-Over-Effekt auf, um den Link anzugeben. Dieser Ansatz hilft, ist aber nicht allein durch die visuelle Überprüfung erkennbar.<br/> ![Screenshot des Symbols mit Linkauswahl-Mauszeiger ](images/ctrl-links-image10.png)<br/> In diesem Beispiel ist der Link nicht allein durch die visuelle Überprüfung erkennbar.<br/> **Aufgrund ihrer potenziellen Erkennungs- und Lokalisierungsprobleme werden links auf Grafiken nicht als einzige Möglichkeit zum Ausführen einer Aufgabe empfohlen.** <br/> |



 

## <a name="guidelines"></a>Richtlinien

### <a name="interaction"></a>Interaktion

-   **Zeigen Sie einen Zeiger auf ausgelastet an, wenn das Ergebnis des Klickens auf einen Link nicht sofort angezeigt wird.** Ohne Feedback gehen Benutzer möglicherweise davon aus, dass der Klick nicht passiert ist, und klicken sie erneut.

### <a name="color"></a>Color

-   **Verwenden Sie das Design oder die Linksystemfarben für besuchten und nicht überwachten Links.** Die Bedeutung dieser Farben ist in allen Programmen konsistent. Wenn Benutzern diese Farben aus irgendeinem Grund nicht gefällt (z. B. aus Gründen der Barrierefreiheit), können sie sie selbst ändern.
-   **Verwenden Sie für Navigationslinks unterschiedliche Farben für besuchte und nicht überwachte Links.** Behalten Sie den Verlauf der besuchten Links nur für die Dauer der Programminstanz bei. Die besuchten Farben sind wichtig, um anzugeben, wo benutzer bereits waren, und verhindert, dass sie die gleichen Seiten unbeabsichtigt wiederholt erneut besuchen.
-   **Verwenden Sie für andere Arten von Links nicht die Farbe des besuchten Links.** Es gibt z. B. keinen ausreichenden Wert für die Identifizierung von "besuchten" Befehlen.
-   **Färben Sie keinen Text, der kein Link ist, da Benutzer davon ausgehen können, dass es sich um einen Link handelt.** Verwenden Sie fett oder grau, wenn Sie andernfalls farbigen Text verwenden würden.
-   **Ausnahme:** Sie können farbigen Text verwenden, wenn alle Links entweder unterstrichen oder innerhalb von Standardnavigations- oder Befehlspositionen platziert werden.

    **Falsch:**

    ![Screenshot der Power Plan-Nachricht mit blauem Text ](images/ctrl-links-image11.png)

    In diesem Beispiel wird blauer Text fälschlicherweise für Text verwendet, der kein Link ist.

-   **Verwenden Sie Hintergrundfarben, die mit den Linkfarben kontrastieren.** Die [Fenstersystemfarbe](vis-color.md) ist immer eine gute Wahl.

    **Falsch:**

    ![Screenshot von blauem Linktext auf blauem Hintergrund ](images/ctrl-links-image12.png)

    In diesem Beispiel bietet die Hintergrundfarbe einen schlechten Kontrast zur Linkfarbe.

### <a name="underlining"></a>Unterstreichung

-   **Stellen Sie für Links, die zum Ausführen einer primären Aufgabe erforderlich sind, visuelle Hinweise zur Verfügung, damit Benutzer Links allein durch visuelle Überprüfung erkennen können.** Zu diesen Hinweisen zählen Unter- oder Aufzählungszeichen sowie Standardlinkpositionen. Benutzer sollten nicht auf ein Objekt bewegen oder versuchen, darauf zu klicken, um zu ermitteln, ob es sich um einen Link handelt. Verwenden Sie unterstrichenen Text, wenn der Link im Kontext nicht offensichtlich ist.
-   **Unterstrichen Sie keinen Text, der kein Link ist, da Benutzer davon ausgehen können, dass es sich um einen Link handelt.** Verwenden Sie italisch, wenn Sie andernfalls unterstrichenen Text verwenden würden. Reservieren Sie das Untergliedern nur für Links.
-   **Drucken Sie beim Drucken keine Unterstreichungen oder Linkfarben.** Gedruckte Links haben keinen Wert und sind möglicherweise verwirrend.

### <a name="text-with-icon-links"></a>Text mit Symbollinks

-   **Verwenden Sie das Pfeilsymbol nur für Befehlslinks.** Reguläre Links sollten das Pfeilsymbol nur verwenden, wenn sie als Ersatz für Befehlslinks [in](ctrl-command-links.md) Windows XP verwendet werden.
-   **Platzieren Sie das Symbol links neben dem Text.** Das Symbol muss visuell in den Text führen.

**Richtig:**

![Screenshot des Symbols vor dem Text ](images/ctrl-links-image13.png)

**Falsch:**

![Screenshot des Symbols nach Text ](images/ctrl-links-image14.png)

Im falschen Beispiel führt das Symbol nicht in den Text.

-   **Ändern Sie das Ergebnis des Klickens auf das Symbol mit dem Klicken auf den Text.** Andernfalls wäre dies unerwartet und verwirrend.

### <a name="graphics-only-links"></a>Links nur für Grafiken

-   **Verwenden Sie keine Nur-Grafiken-Links.** Benutzer haben sie schwer als Links erkannt, und jeder Text in der Grafik (der verwendet wird, um ihre Aktion anzugeben, wenn darauf geklickt wird) führt zu einem Lokalisierungsproblem.

### <a name="navigation-links"></a>Navigationslinks

-   **Stellen Sie sicher, dass für Navigationslinks keine Verpflichtung erforderlich ist.** Benutzer sollten immer in der Lage sein, zum ursprünglichen Zustand zurückzukehren, entweder durch Verwendung von Zurück für die Ortsnavigation oder Abbrechen, um ein neues Fenster zu schließen.
-   **Link zu bestimmten Inhalten und nicht zu allgemeinem Inhalt.** Beispielsweise ist es besser, mit dem relevanten Abschnitt eines Dokuments zu verknüpfen, als mit dem Anfang zu verknüpfen.
-   **Verwenden Sie einen Link nur, wenn das verknüpfte Material relevant, hilfreich und nicht redundant ist.** Verwenden Sie in Navigationslinks nicht einfach so, wie Sie dies können.
-   Wenn ein Link zu einer externen Website navigiert, geben Sie die URL in den **Infotip ein,** damit Benutzer das Ziel des Links bestimmen können.
-   **Verknüpfen Sie nur das erste Vorkommen des Linktexts.** Redundante Links sind unnötig und können das Lesen von Text erschweren.

    **Richtig:**

    Der Ordner Bilder erleichtert das Freigeben Ihrer Bilder. Sie können die Aufgaben in Bilder verwenden, um Ihre Bilder per E-Mail zu senden oder sie an einem sicheren, privaten Ort im Web zu veröffentlichen. Sie können Ihre Bilder auch direkt aus dem Ordner Bilder drucken.

    **Falsch:**

    Der Ordner Bilder erleichtert das Freigeben Ihrer Bilder. Sie können die Aufgaben in Bilder verwenden, um Ihre Bilder per E-Mail zu senden oder sie an einem sicheren privaten Ort im Web zu veröffentlichen. Sie können Ihre Bilder auch direkt aus dem Ordner Bilder drucken.

    Im richtigen Beispiel wird nur das erste Vorkommen des relevanten Texts verknüpft.

    **Ausnahmen:**

    -   **Wenn eine Anweisung über einen Link verfügt, legen Sie den Link in die Anweisung ein.**

        Die Verwendung sicherer Kennwörter ist sehr wichtig. Weitere Informationen finden Sie unter Sichere Kennwörter.

        In diesem Beispiel befindet sich der Link in der -Anweisung anstelle des ersten Vorkommens.

    -   **Link zu späteren Vorkommen, wenn sie weit vom ersten entfernt sind.** Beispielsweise können Sie redundante Verknüpfungen in verschiedenen Abschnitten in einem Hilfethema erstellen.

### <a name="task-links"></a>Aufgabenlinks

-   **Verwenden Sie Aufgabenlinks für Befehle, die nicht destruktiv sind oder leicht umkehrbar sind.** Da Benutzer Links der Navigation zuordnen (und die Möglichkeit zum Back-Out) haben, sind Links nicht für Befehle geeignet, die erhebliche Folgen haben. Befehle, die ein Dialogfeld oder eine Bestätigung anzeigen, sind eine gute Wahl.

    **Richtig:**

    Start

    Beenden

    **Falsch:**

    Datei löschen

    Im falschen Beispiel ist der Befehl destruktiv.

### <a name="menu-links"></a>Menülinks

-   **Gruppieren sie verwandte Navigations- und Aufgabenlinks in Menüs.** Ein Menü verwandter Links, die sich in einer Standardnavigations- oder Befehlsposition befinden, erleichtert das Suchen und Verstehen der Links als bei getrennter Platzierung.
-   **Entfernen Sie für auswahlabhängige Menüs Menülinks, die nicht angewendet werden.** Deaktivieren Sie sie nicht. Auf diese Weise wird unübersichtlich, und Benutzer werden keine Links auslassen, für die eine Auswahl erforderlich ist.
-   **Deaktivieren Sie für auswahlunabhängige Menüs Menülinks, die nicht angewendet werden.** Entfernen Sie sie nicht. Dadurch werden die Menüs stabiler, und solche Links sind leichter zu finden.

    ![Screenshot des Dialogfelds mit abgeblendeter Menübefehl ](images/ctrl-links-image15.png)

    In diesem Beispiel von Windows Update wird ein Update ausgeführt, sodass der Befehl Nach Updates suchen deaktiviert und nicht entfernt wird.

### <a name="link-infotips"></a>Linkinfos

-   Wenn ein Link eine weitere Erläuterung erfordert, **geben Sie die Erklärung entweder in einer ergänzenden Erklärung in einem separaten Textsteuerelement oder in einem** [Infotip](ctrl-tooltips-and-infotips.md)an, aber nicht in beiden. Verwenden Sie vollständige Sätze und endende Interpunktion. Beides ist nicht erforderlich, wenn der Text identisch ist, und verwirrend, wenn der Text unterschiedlich ist.

    ![Screenshot des Links mit ergänzendem Text ](images/ctrl-links-image16.png)

    In diesem Beispiel enthält eine ergänzende Erläuterung weitere Informationen zum Link.

    ![Screenshot des Links mit Infotip ](images/ctrl-links-image17.png)

    In diesem Beispiel enthält ein Infotip weitere Informationen.

-   **Geben Sie keine Infoinfo an, die lediglich eine Neuformierung des Linktexts ist.**

    **Falsch:**

    ![Screenshot des Links mit redundanter Infotip ](images/ctrl-links-image18.png)

    In diesem Beispiel riskiert der Infotip Benutzer durch seine Wiederholungshäufigkeit zu verärgern.

## <a name="text"></a>Text

-   Weisen Sie keinen [Zugriffsschlüssel](glossary.md)zu. Der Zugriff auf Links erfolgt über die TAB-TASTE.
-   **Verwenden Sie Links, die spezifische beschreibende Informationen über das Ergebnis des Klickens auf den Link mit** so viel Text wie nötig liefern. Der Linktext sollte das Ergebnis des Klickens auf den Link angeben. **Benutzer sollten in der Lage sein, das Ergebnis eines Links aus dem Linktext und optionalen Infotips genau vorherzusagen.**

    **Falsch:**

    ![Screenshot eines Links zu einer Sicherheitshinweiswarnung ](images/ctrl-links-image19.png)

    In diesem Beispiel ist die Bezeichnung zu allgemein, obwohl der Link wichtig erscheint. Benutzer klicken eher auf einen spezifischeren Link.

-   Für Inlinelinks:
    -   Behalten Sie die Groß- und Interpunktion des Texts bei.
    -   Schließen Sie keine endende Interpunktion in den Link ein, es sei denn, der Text ist eine Frage.
    -   Verknüpfen Sie den relevantesten Teil des Texts, und wählen Sie Den Linktext aus, der groß genug ist, um einfach zu klicken.

        **Richtig:**

        Wechseln Sie zu einer Newsgroup.

        **Falsch:**

        Wechseln Sie zu einer Newsgroup.

        In diesen Beispielen ist "Go" nicht der relevanteste Teil des Texts und nicht groß genug, um ein gutes Klickziel zu erzielen, während "newsgroup" ist.

    -   **Vermeiden Sie es, zwei verschiedene Inlinelinks nebeneinander zu setzen.** Benutzer sind wahrscheinlich der Meinung, dass es sich um einen einzelnen Link handelt.

        **Falsch:**

        Weitere Informationen finden Sie unter UX-Richtlinien.

        In diesem Beispiel sind "UX" und "guidelines" zwei verschiedene Links.

-   Für unabhängige Links (nicht inline):
    -   Verwenden Sie [die Groß-/Großschreibung im Satzformat.](glossary.md)
    -   Verwenden Sie keine endende Interpunktion, es sei denn, der Link ist eine Frage.
    -   Verwenden Sie den gesamten Text als Link.
-   Verwenden Sie Links, die sich deutlich von den anderen Links auf dem Bildschirm unterscheiden. Benutzer sollten in der Lage sein, Linkziele genau vorherzusagen und zwischen diesen zu unterscheiden.

    **Falsch:**

    Suchen nach Antivirensoftware

    Abrufen von Antivirensoftware

    **Richtig:**

    Erfahren Sie, ob Antivirensoftware installiert ist.

    Installieren von Antivirensoftware

    Im falschen Beispiel ist der Unterschied zwischen den beiden Links unklar.

-   Fügen Sie dem Linktext nicht Click (Klicken) oder Click here (Klicken Sie hier) hinzu. Dies ist nicht erforderlich, da ein Link ein Klicken impliziert. Klicken Sie auch nur hier und hier, um beim Lesen durch eine Sprachausgabe keine Informationen über den Link zu übermitteln.

    **Falsch:**

    Klicken Sie hier, um eine Beschreibung zu finden.

    **Richtig:**

    BESCHREIBUNG

    In den falschen Beispielen ist "Klicken Sie hier" selbstverständlich und übermittelt keine Informationen über den Link.

**Navigationslinks**

-   **Starten Sie den Link mit einem Nomen, und beschreiben Sie deutlich, wohin das Klicken auf den Link erfolgen soll.** Verwenden Sie keine Interpunktion am Ende. Gelegentlich müssen Sie möglicherweise Navigationslinks mit einem Verb starten, aber verwenden Sie keine Verben, die die Navigation wiederholen, die bereits durch die Tatsache der Verknüpfung impliziert wird, z. B. Ansicht, Öffnen oder Gehe zu.
-   **Zeigen Sie einen Navigationslink als URL an, wenn er zu einer Webseite navigiert, und Sie erwarten, dass die Zielbenutzer die URL abrufen und in einen Browser eingeben.** Entwerfen Sie diese URLs nach Möglichkeit so, dass sie kurz und leicht zu merken sind.
-   **Wenn der Link eine URL zu einer Website enthält, die mit "www" beginnt, lassen Sie den https:// Protokollnamen weg, und verwenden Sie Kleinbuchstaben.**

    **Falsch:**

    https://www.microsoft.com

    `www.microsoft.com`

    **Richtig:**

    microsoft.com

    In den falschen Beispielen sind die "https://" und "www" selbstverständlich.

**Aufgabenlinks**

-   **Starten Sie den Link mit einem imperativen Verb, und beschreiben Sie eindeutig die Aufgabe, die der Link ausführt.** Verwenden Sie keine Interpunktion am Ende.
-   **Beenden Sie den Link mit einem Auslassungszeichen, wenn der Befehl zusätzliche Informationen (einschließlich einer Bestätigung) für den erfolgreichen Abschluss benötigt.** Verwenden Sie keine Auslassungszeichen, wenn der Task erfolgreich abgeschlossen wurde, um nur dann ein weiteres Fenster anzuzeigen, wenn zusätzliche Informationen zum Ausführen der Aufgabe erforderlich sind.

    Drucken...

    In diesem Beispiel wird der Druck... Über den Befehlslink wird ein Dialogfeld Drucken angezeigt, um weitere Informationen zu sammeln.

    Drucken

    Im Gegensatz dazu gibt in diesem Beispiel ein Befehlslink Drucken eine einzelne Kopie eines Dokuments ohne weitere Benutzerinteraktion auf dem Standarddrucker aus.

    **Die ordnungsgemäße Verwendung von Ellipsen ist wichtig, um anzugeben, dass Benutzer vor dem Ausführen der Aufgabe weitere Entscheidungen treffen oder die Aufgabe vollständig abbrechen können.** Die visuellen Hinweise, die von auslassungsbaren Ellipsen geboten werden, ermöglichen es Benutzern, Ihre Software ohne Sorge zu erkunden.

-   **Beenden Sie bei Bedarf einen Aufgabenlink mit "now", um ihn von einem Navigationslink zu unterscheiden.**

    Herunterladen von Dateien

    Dateien jetzt herunterladen

    In diesem Beispiel navigiert "Dateien herunterladen" zu einer Seite zum Herunterladen von Dateien, während "Dateien jetzt herunterladen" tatsächlich den Befehl ausführt.

**Hilfelinks**

Richtlinien und Beispiele finden Sie unter [Hilfe.](winenv-help.md)

**Linkinfos**

-   Verwenden Sie vollständige Sätze und endende Interpunktion.

Weitere Richtlinien und Beispiele finden Sie unter [QuickInfos und Infotips.](ctrl-tooltips-and-infotips.md)

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Links:

-   Verwenden Sie den genauen Linktext, einschließlich der Groß-/Großschreibung, aber schließen Sie die Auslassungszeichen nicht ein.
-   Um die Benutzerinteraktion zu beschreiben, klicken Sie auf .
-   Formatieren Sie den Linktext nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie den Linktext nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

Beispiel: Klicken Sie zum Starten der Überprüfung auf **Computer überprüfen.**

 

