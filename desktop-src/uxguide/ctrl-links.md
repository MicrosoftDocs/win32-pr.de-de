---
title: Links
description: Mit einem Link können Benutzer zu einer anderen Seite, einem anderen Fenster oder einem anderen Hilfethema navigieren. eine Definition anzeigen; Initiieren eines Befehls; oder wählen Sie eine Option aus.
ms.assetid: a23748e4-b2dd-4b9f-9a7c-ff6533922c8c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 985e266428a57bae88cf30090bff97f45787faa1a116993958086547339d465c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118040099"
---
# <a name="links"></a>Links

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Mit einem *Link* können Benutzer zu einer anderen Seite, einem anderen Fenster oder einem anderen Hilfethema navigieren. eine Definition anzeigen; Initiieren eines Befehls; oder wählen Sie eine Option aus. Ein Link ist text oder eine Grafik, die angibt, dass darauf geklickt werden kann, in der Regel durch Anzeige der besuchten oder nicht überwachten [Linksystemfarben](vis-color.md). Traditionell werden Links ebenfalls unterstrichen, aber dieser Ansatz ist oft unnötig und wird nicht bevorzugt, um die visuelle Übersichtlichkeit zu reduzieren.

Wenn Benutzer auf einen Link zeigen, wird der Linktext als unterstrichen angezeigt (sofern noch nicht vorhanden), und die Zeigerform ändert sich in eine [Hand.](inter-mouse.md)

Ein Textlink ist das klickbare Steuerelement mit der geringsten Gewichtung und wird häufig verwendet, um die visuelle Komplexität eines Entwurfs zu reduzieren.

> [!Note]  
> Richtlinien im Zusammenhang [mit Befehlslinks](ctrl-command-links.md) [und Layout](vis-layout.md) werden in separaten Artikeln vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Der Link, der zum Navigieren zu einer anderen Seite, einem anderen Fenster oder einem anderen Hilfethema verwendet wird. eine Definition anzeigen; Initiieren eines Befehls; oder wählen Sie eine Option aus?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement.
-   **Wäre eine Befehlsschaltfläche die bessere Wahl?** Verwenden Sie eine [Befehlsschaltfläche,](ctrl-command-buttons.md) wenn:
    -   Das -Steuerelement initiiert eine sofortige Aktion, einschließlich der Anzeige eines Fensters, und dieser Befehl bezieht sich auf den primären Zweck des Fensters.
    -   Ein Fenster wird angezeigt, um Eingaben zu erfassen oder Auswahlmöglichkeiten zu treffen, auch wenn es sich um einen sekundären Befehl handelt.
    -   Die Bezeichnung ist kurz und besteht aus vier oder weniger Wörtern, wodurch das ums andere Aussehen langer Schaltflächen vermieden wird.
    -   Der Befehl ist nicht inline.
    -   Das Steuerelement wird in einer Gruppe anderer verwandter Befehlsschaltflächen angezeigt.
    -   Die Aktion ist destruktiv oder kann nicht rückgängig gemacht werden. Da Benutzer Links der Navigation (und der Möglichkeit zum Back-Out) zuordnen, sind Links für Befehle mit erheblichen Folgen nicht geeignet.
    -   Auf ähnliche Weise stellt der Befehl in [einem Assistenten](win-wizards.md) oder [Taskfluss](glossary.md)eine Verpflichtung dar. In solchen Fenstern schlagen Befehlsschaltflächen eine Verpflichtung vor, während Links empfehlen, zum nächsten Schritt zu navigieren.

## <a name="design-concepts"></a>Entwurfskonzepte

**Erkennbar machen von Links**

Für Links [fehlt derEnthaltung.](glossary.md)Dies bedeutet, dass ihre visuellen Eigenschaften nicht vorschlagen, wie sie verwendet werden und nur durch Erfahrung verstanden werden.  Links ohne Unterstreichung und Linksystemfarben werden als normaler Text angezeigt. die einzige Möglichkeit, ihr Verhalten zu ermitteln, ist die Darstellung, der Kontext oder die Positionierung des Zeigers darüber.

Überraschenderweise ist dieses Fehlen des Bietetes oft eine Motivation für die Verwendung von Links, da sie so einfach erscheinen, wodurch die visuelle Komplexität eines Entwurfs reduziert wird. Links beseitigen den visuell starken Rahmen, der von [Befehlsschaltflächen und](ctrl-command-buttons.md) Rahmen verwendet wird, die von anderen Steuerelementen verwendet werden. Während Sie beispielsweise Befehlsschaltflächen verwenden können, um primäre Befehle offensichtlich zu machen, können Sie Links für sekundäre Befehle auswählen, um sie zu heben.

Die Herausforderung besteht dann darin, genügend visuelle Hinweise zu erhalten, damit Benutzer die Links erkennen können. Die grundlegende Richtlinie ist, dass Benutzer Links allein durch visuelle Überprüfung erkennen können müssen. Sie müssen nicht auf ein Objekt bewegen oder darauf klicken, um zu ermitteln, ob es sich um einen Link **handelt.**

Benutzer können einen Link allein durch visuelle [](vis-color.md) Überprüfung erkennen, wenn der Link die Farben des Linksystems und mindestens einen der folgenden visuellen Hinweise verwendet:

-   Unterstrichener Text.
-   Eine Grafik oder ein Aufzählungszeichen, z. B. mit dem [Text mit Symbollinkmuster.](#usage-patterns)
-   Platzierung innerhalb eines Standardnavigations-, Options- [](glossary.md) oder Befehlsspeicherorts, z. B. des Inhaltsbereichs eines Fensters, oder in einer Navigationsleiste, Menüleiste, Symbolleiste oder Seitenfußzeile.

Benutzer können einen Link auch durch visuelle Überprüfung mit den folgenden visuellen Hinweisen erkennen, aber diese Hinweise reichen selbst nicht aus:

-   Text, der ein Klicken vorschlägt, z. B. ein Befehl, der mit einem imperativen Verb wie Show, Print, Copy oder Delete beginnt.
-   Platzierung innerhalb eines Blocks mit normalem Text.

Natürlich können Benutzer einen Link immer durch Interaktion bestimmen, indem sie mit dem Hovern oder Klicken darauf klicken. Wenn die Ermittlung eines Links für wichtige Aufgaben nicht erforderlich ist, können Sie diese Links heben.

![Screenshot grauer Bezeichnungen auf schwarzem Hintergrund ](images/ctrl-links-image1.png)

In diesem Beispiel sind "Kontakt mit uns", "Nutzungsbedingungen", "Marken" und "Datenschutzbestimmungen" Links. Sie werden absichtlich nicht hervorgehoben, da sie für keine wichtigen Aufgaben erforderlich sind. Die einzigen Hinweise darauf, dass es sich um Links handelt, sind, dass sie einen Mauszeiger beim Zeigen haben und in einem Standardnavigationsbereich am unteren Rand des Fensters positioniert sind.

**Machen von Links spezifisch, relevant und vorhersagbar**

Der Linktext sollte das Ergebnis des Klickens auf den Link angeben.

Bestimmte Links sind für Benutzer überzeugender als allgemeine Links. Verwenden Sie daher Linkbezeichnungen, die spezifische beschreibende Informationen zum Ergebnis des Klickens auf **den Link enthalten.** Stellen Sie jedoch sicher, dass Ihr Linktext nicht so spezifisch ist, dass er irreführend ist und von der richtigen Verwendung abraten wird.

Es ist wahrscheinlicher, dass präzise Links gelesen werden als ausführliche Links. **Vermeiden Sie unnötigen Text und unnötige Details.** Linkbezeichnungen müssen nicht umfassend sein.

So werten Sie den Linktext aus:

-   Stellen Sie sicher, dass der Linktext die vom Link unterstützten Szenarien widerspiegelt.
-   Stellen Sie sicher, dass die Ergebnisse des Links vorhersagbar sind. Benutzer sollten von den Ergebnissen nicht überraschend sein.

**Wenn Sie nur zwei Dinge tun...**

1. Machen Sie Links allein durch visuelle Überprüfung erkennbar. Benutzer sollten nicht mit Ihrem Programm interagieren müssen, um Links zu finden.

2. Verwenden Sie Links, die spezifische beschreibende Informationen zum Ergebnis des Klickens auf den Link mit so viel Text wie nötig enthalten. Benutzer sollten in der Lage sein, das Ergebnis eines Links aus dem Linktext und dem optionalen Infotip [genau vorherzusagen.](ctrl-tooltips-and-infotips.md)

## <a name="usage-patterns"></a>Verwendungsmuster

Links haben mehrere Funktionsmuster:



|    Verwendung                  |    Beispiel   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Navigationslinks**<br/> Ein Link, der zum Navigieren zu einer anderen Seite oder einem anderen Fenster verwendet wird. <br/>                                                      | Durch Klicken auf den Link wird direkt zu einer anderen Seite navigiert, wie in einem Browserfenster oder Assistenten. oder zeigt ein neues Fenster an. Im Gegensatz zu Aufgabenlinks initiiert die Navigation keine Aufgabe, sondern navigiert einfach zu einer anderen Stelle oder geht mit einer aufgabe fort, die bereits in Bearbeitung ist. Die Navigation impliziert Sicherheit, da der Benutzer immer zurückkommen kann.<br/> News-Überschriften<br/> In diesem Beispiel wird durch Klicken auf den Link zur Seite News-Überschriften navigiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Aufgabenlinks**<br/> Ein Link, der zum Initiieren eines neuen Befehls verwendet wird. <br/>                                                                        | Durch Klicken auf den Link wird entweder sofort ein Befehl ausgeführt oder ein Dialogfeld oder eine Seite angezeigt, um weitere Eingaben zu sammeln. Im Gegensatz zu Navigationslinks initiieren Aufgabenlinks eine neue Aufgabe, anstatt mit einer vorhandenen Aufgabe fortzuführen. Aufgaben implizieren nicht, dass SafetyUsers nicht mit einem Back-Befehl in den vorherigen Zustand zurückverwenden können. Tasklinks werden aufgerufen, um Verwechslungen mit [Befehlslinks zu vermeiden.](ctrl-command-links.md) <br/> Anmelden<br/> In diesem Beispiel wird durch Klicken auf den Link ein Anmeldebefehl initiiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Hilfelinks**<br/> Ein Textlink zum Anzeigen eines Hilfethemas. <br/>                                                                     | Wenn Sie auf den Link klicken, wird ein Hilfeartikel in einem separaten Fenster angezeigt.<br/> Was ist ein starkes Kennwort?<br/> In diesem Beispiel wird durch Klicken auf den Link ein Hilfefenster mit dem angegebenen Thema angezeigt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Definitionslinks**<br/> Ein Textlink, der verwendet wird, um eine Definition in einer Infotip anzuzeigen, wenn der Benutzer auf den Link klickt oder darauf zeigt. <br/> | dieses Muster ist nützlich, um Begriffe zu definieren, die Ihren Benutzern möglicherweise nicht bekannt sind, ohne den Bildschirm unübersichtlich zu machen.<br/> ![Screenshot der Infotips, die mit dem Mauszeigerzeiger angezeigt werden ](images/ctrl-links-image2.png)<br/> In diesem Beispiel wird die Infotip-Definition angezeigt. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Menülinks**<br/> eine Reihe von Aufgabenlinks, die zum Erstellen eines Menüs verwendet werden. <br/>                                                                    | Da der Kontext des Menüs eine Reihe von Links angibt, wird der Text in der Regel nicht unterstrichen (mit Ausnahme des Hoverns) und verwendet möglicherweise nicht die Farben des Linksystems.<br/> ![Screenshot einer Reihe von Links ](images/ctrl-links-image3.png)<br/> In diesem Beispiel wird mit einer Reihe von Links ein Menü erstellt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Optionslinks**<br/> eine ausgewählte Option oder deren Platzhalter, bei der durch Klicken auf den Link ein Befehl aufgerufen wird, um diese Option zu ändern.<br/>       | Im Gegensatz zu regulären Textlinks ändert der Link seinen Text, um die aktuell ausgewählte Option widerzuspiegeln, und wird immer mit der Farbe des nicht überwachten Links gezeichnet. <br/> ![Screenshot einer Regel im Outlook-Regel-Assistenten ](images/ctrl-links-image4.png)<br/> Das Beispiel auf der linken Seite zeigt eine Regel aus dem Microsoft Outlook-Regel-Assistenten mit Platzhalteroptionen. Nachdem Benutzer auf die Links geklickt und einige Optionen ausgewählt haben, aktualisiert das rechte Beispiel den Linktext, um die Ergebnisse anzuzeigen.<br/> Die Verwendung von Optionslinks ist besonders geeignet, wenn die Optionen ein Variable-Format aufweisen. <br/> ![Screenshot einer geänderten Regel im Regel-Assistenten ](images/ctrl-links-image5.png)<br/> Das Beispiel auf der rechten Seite zeigt, dass Outlook-Regeln ein Variablenformat aufweisen. <br/> ![Screenshot der Textänderungen in der Dropdownliste ](images/ctrl-links-image6.png)<br/> Das Beispiel auf der linken Seite zeigt einen Optionslink. Wenn diese Option ausgewählt ist, wird sie zu einer Dropdownliste, wie auf der rechten Seite dargestellt.<br/> |



 

Links verfügen auch über mehrere Darstellungsmuster:



|    Verwendung                                 |    Beispiel                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nur-Text-Links**<br/> bestehen nur aus Text. <br/>                                      | Diese Präsentation ist die flexibelste, da sie überall verwendet werden kann, einschließlich [inline.](glossary.md)<br/> ![Screenshot des Blaulinktexts ](images/ctrl-links-image7.png)<br/> In diesem Beispiel identifiziert die Textfarbe einen Inlinelink eindeutig.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Text mit Symbollinks**<br/> Text mit einem vorangehenden Symbol, das seine Funktion angibt.<br/> | Da die Grafik einen zusätzlichen visuellen Hinweis auf einen Link bietet, ist es einfacher, als Link zu erkennen, als ein Nur-Text-Link, der nicht unterstrichen ist. Dieses Muster verwendet in der Regel ein 16 x 16 Pixel großes Symbol.<br/> ![Screenshot der Liste mit vier Links mit Symbolen ](images/ctrl-links-image8.png)<br/> In diesem Beispiel stellen die Symbole einen zusätzlichen visuellen Hinweis auf einen Link bereit.<br/> ![Screenshot des Wiedergabebefehls mit kleinem Dreieck ](images/ctrl-links-image9.png)<br/> In diesem Beispiel gibt das standardmäßige dreieckige Play-Symbol an, dass es sich bei diesem Text um einen Befehl handelt.<br/>                                                                                                                                     |
| **Links nur für Grafiken**<br/> bestehen nur aus einer Grafik.<br/>                               | Wenn kein Textlink vorhanden ist, gibt es keine Linkfarbe oder -unterstreichung, um den Link anzugeben. Diese Links hängen entweder vom grafischen Design ab, auf das geklickt werden soll, oder von Text in der Grafik, der eine Aktion vorschlägt, wenn Benutzer klicken. Grafische Links haben manchmal einen Mauszeigerovereffekt, um den Link anzugeben. Dieser Ansatz hilft, ist jedoch nicht allein durch die visuelle Überprüfung erkennbar.<br/> ![Screenshot des Symbols mit Linkauswahl-Mauszeiger ](images/ctrl-links-image10.png)<br/> In diesem Beispiel ist der Link nicht allein durch die visuelle Überprüfung erkennbar.<br/> **Aufgrund ihrer potenziellen Erkennungs- und Lokalisierungsprobleme werden nur Grafiklinks nicht als einzige Möglichkeit zum Ausführen einer Aufgabe empfohlen.** <br/> |



 

## <a name="guidelines"></a>Richtlinien

### <a name="interaction"></a>Interaktion

-   **Zeigt einen ausgelasteten Zeiger an, wenn das Ergebnis des Klickens auf einen Link nicht sofort erfolgt.** Ohne Feedback gehen Benutzer möglicherweise davon aus, dass der Klick nicht erfolgt ist, und klicken erneut.

### <a name="color"></a>Color

-   **Verwenden Sie die Design- oder Linksystemfarben für besuchte und nicht aufgerufene Links.** Die Bedeutung dieser Farben ist in allen Programmen konsistent. Wenn Benutzern diese Farben aus irgendeinem Grund nicht gefallen (z. B. aus Gründen der Barrierefreiheit), können sie sie selbst ändern.
-   **Verwenden Sie für Navigationslinks unterschiedliche Farben für besuchte und nicht aufgerufene Links.** Behalten Sie den Verlauf der besuchten Links nur für die Dauer der Programminstanz bei. Die besuchten Farben sind wichtig, um anzugeben, wo sich Benutzer bereits befinden, sodass sie dieselben Seiten nicht versehentlich wiederholt erneut aufrufen können.
-   **Verwenden Sie für andere Arten von Links nicht die Farbe des besuchten Links.** Die Identifizierung von "besuchten" Befehlen ist beispielsweise nicht ausreichend.
-   **Verwenden Sie keine Farbe für Text, der kein Link ist, da Benutzer davon ausgehen können, dass es sich um einen Link handelt.** Verwenden Sie fett oder grau, wo Sie andernfalls farbigen Text verwenden würden.
-   **Ausnahme:** Sie können farbigen Text verwenden, wenn alle Links entweder unterstrichen oder innerhalb der Standardnavigations- oder Befehlsspeicherorte platziert werden.

    **Falsch:**

    ![Screenshot der Energiesparmeldung mit blauem Text ](images/ctrl-links-image11.png)

    In diesem Beispiel wird blauer Text fälschlicherweise für Text verwendet, der kein Link ist.

-   **Verwenden Sie Hintergrundfarben, die im Gegensatz zu den Linkfarben stehen.** Die [Fenstersystemfarbe](vis-color.md) ist immer eine gute Wahl.

    **Falsch:**

    ![Screenshot des Blaulinktexts auf blauem Hintergrund ](images/ctrl-links-image12.png)

    In diesem Beispiel bietet die Hintergrundfarbe einen schlechten Kontrast zur Linkfarbe.

### <a name="underlining"></a>Unterstreichung

-   **Stellen Sie für Links, die zum Ausführen einer primären Aufgabe erforderlich sind, visuelle Hinweise bereit, damit Benutzer Links allein durch visuelle Überprüfung erkennen können.** Zu diesen Hinweisen gehören Unterstriche, Grafiken oder Aufzählungszeichen sowie Standardlinkpositionen. Benutzer sollten nicht mit dem Mauszeiger auf ein Objekt zeigen oder versuchen, darauf zu klicken, um festzustellen, ob es sich um einen Link handelt. Verwenden Sie unterstrichenen Text, wenn der Link im Kontext nicht offensichtlich ist.
-   **Unterstrichen Sie keinen Text, der kein Link ist, da Benutzer davon ausgehen können, dass es sich um einen Link handelt.** Verwenden Sie Kursivschrift, wenn Sie andernfalls unterstrichenen Text verwenden würden. Reservieren Sie underlining nur für Links.
-   **Geben Sie beim Drucken keine Unterstreichungen oder Linkfarben aus.** Gedruckte Links haben keinen Wert und sind möglicherweise verwirrend.

### <a name="text-with-icon-links"></a>Text mit Symbollinks

-   **Verwenden Sie das Pfeilsymbol nur für Befehlslinks.** Reguläre Links sollten nur dann das Pfeilsymbol verwenden, wenn sie als Ersatz für [Befehlslinks](ctrl-command-links.md) in Windows XP verwendet werden.
-   **Platzieren Sie das Symbol links neben dem Text.** Das Symbol muss visuell in den Text führen.

**Richtig:**

![Screenshot des Symbols vor dem Text ](images/ctrl-links-image13.png)

**Falsch:**

![Screenshot des Symbols nach Text ](images/ctrl-links-image14.png)

Im falschen Beispiel führt das Symbol nicht in den Text.

-   **Das Ergebnis des Klickens auf das Symbol entspricht dem Klicken auf den Text.** Andernfalls wäre dies unerwartet und verwirrend.

### <a name="graphics-only-links"></a>Links nur für Grafiken

-   **Verwenden Sie keine reinen Grafiklinks.** Benutzer haben sie schwer als Links zu erkennen, und jeder Text in der Grafik (der verwendet wird, um ihre Aktion anzugeben, wenn darauf geklickt wird), führt zu einem Lokalisierungsproblem.

### <a name="navigation-links"></a>Navigationslinks

-   **Stellen Sie sicher, dass für Navigationslinks keine Verpflichtung erforderlich ist.** Benutzer sollten immer in der Lage sein, zum ursprünglichen Zustand zurückzukehren, indem sie entweder Zurück für die Ortsnavigation oder Abbrechen verwenden, um ein neues Fenster zu schließen.
-   **Link zu bestimmten Inhalten und nicht zu allgemeinen Inhalten.** Beispielsweise ist es besser, einen Link zum relevanten Abschnitt eines Dokuments zu erstellen, als eine Verknüpfung mit dem Anfang zu erstellen.
-   **Verwenden Sie einen Link nur, wenn das verknüpfte Material relevant, hilfreich und nicht redundant ist.** Verwenden Sie sie in Navigationslinks nicht nur, weil Sie dies tun können.
-   **Wenn ein Link zu einer externen Website navigiert, legen Sie die URL in die Infotip ein,** damit Benutzer das Ziel des Links bestimmen können.
-   **Verknüpfen Sie nur das erste Vorkommen des Linktexts.** Redundante Links sind unnötig und können das Lesen von Text erschweren.

    **Richtig:**

    Der Ordner Bilder erleichtert die Freigabe Ihrer Bilder. Sie können die Aufgaben in Bilder verwenden, um Ihre Bilder per E-Mail zu senden oder sie an einem sicheren privaten Ort im Web zu veröffentlichen. Sie können Ihre Bilder auch direkt aus dem Ordner Bilder drucken.

    **Falsch:**

    Der Ordner Bilder erleichtert die Freigabe Ihrer Bilder. Sie können die Aufgaben in Bilder verwenden, um Ihre Bilder per E-Mail zu senden oder sie an einem sicheren privaten Ort im Web zu veröffentlichen. Sie können Ihre Bilder auch direkt aus dem Ordner Bilder drucken.

    Im richtigen Beispiel wird nur das erste Vorkommen des relevanten Texts verknüpft.

    **Ausnahmen:**

    -   **Wenn eine Anweisung über einen Link verfügt, legen Sie den Link in die Anweisung ein.**

        Die Verwendung sicherer Kennwörter ist sehr wichtig. Weitere Informationen finden Sie unter Sichere Kennwörter.

        In diesem Beispiel befindet sich der Link in der -Anweisung anstelle des ersten Vorkommens.

    -   **Link zu späteren Vorkommen, wenn sie weit vom ersten entfernt sind.** Beispielsweise können Sie redundante Verknüpfungen in verschiedenen Abschnitten in einem Hilfethema erstellen.

### <a name="task-links"></a>Aufgabenlinks

-   **Verwenden Sie Aufgabenlinks für Befehle, die nicht destruktiv sind oder leicht umkehrbar sind.** Da Benutzer Links der Navigation zuordnen (und die Möglichkeit zum Back-Out) haben, sind Links nicht für Befehle geeignet, die erhebliche Folgen haben. Befehle, die ein Dialogfeld oder eine Bestätigung anzeigen, sind eine gute Wahl.

    **Richtig:**

    Starten

    Beenden

    **Falsch:**

    Datei löschen

    Im falschen Beispiel ist der Befehl destruktiv.

### <a name="menu-links"></a>Menülinks

-   **Gruppieren sie verwandte Navigations- und Aufgabenlinks in Menüs.** Ein Menü verwandter Links, die sich in einer Standardnavigations- oder Befehlsposition befinden, erleichtert das Suchen und Verstehen der Links als bei getrennter Platzierung.
-   **Entfernen Sie für auswahlabhängige Menüs Menülinks, die nicht angewendet werden.** Deaktivieren Sie sie nicht. Auf diese Weise wird unübersichtlich, und Benutzer werden keine Links auslassen, für die eine Auswahl erforderlich ist.
-   **Deaktivieren Sie für auswahlunabhängige Menüs Menülinks, die nicht angewendet werden.** Entfernen Sie sie nicht. Auf diese Weise werden die Menüs stabiler, und solche Links sind leichter zu finden.

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
-   **Verwenden Sie Links, die spezifische beschreibende Informationen über das Ergebnis des Klickens auf den Link enthalten,** und verwenden Sie dabei so viel Text wie nötig. Der Linktext sollte das Ergebnis des Klickens auf den Link angeben. **Benutzer sollten in der Lage sein, das Ergebnis eines Links aus dem Linktext und optionalen Infotips genau vorherzusagen.**

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

        In diesen Beispielen ist "Go" nicht der relevanteste Teil des Texts und nicht groß genug, um ein gutes Klickziel zu erstellen, während "newsgroup" ist.

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

-   Fügen Sie dem Linktext nicht Click (Klicken) oder Click here (Klicken Sie hier) hinzu. Dies ist nicht erforderlich, da ein Link ein Klicken impliziert. Klicken Sie nur hier und hier, um beim Lesen durch eine Sprachausgabe keine Informationen über den Link zu übermitteln.

    **Falsch:**

    Klicken Sie hier, um eine Beschreibung zu finden.

    **Richtig:**

    BESCHREIBUNG

    In den falschen Beispielen ist "Klicken Sie hier" selbstverständlich und übermittelt keine Informationen über den Link.

**Navigationslinks**

-   **Starten Sie den Link mit einem Nomen, und beschreiben Sie deutlich, wohin das Klicken auf den Link gehen soll.** Verwenden Sie keine Interpunktion am Ende. Gelegentlich müssen Sie möglicherweise Navigationslinks mit einem Verb starten, aber verwenden Sie keine Verben, die die Navigation wiederholen, die bereits durch die Tatsache der Verknüpfung impliziert wird, z. B. Ansicht, Öffnen oder Gehe zu.
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

 

