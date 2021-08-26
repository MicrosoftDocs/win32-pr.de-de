---
title: Standardsymbole
description: Standardsymbole sind fehler-, warnungs-, informations- und fragezeichensymbole, die Teil Windows sind.
ms.assetid: 63b5c31d-5094-4299-b44b-35b2452ce706
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 74f5b70fb218606eb5f87cbad247c1c75a100f9c5e0f675bb6c075e559fd1a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936384"
---
# <a name="standard-icons"></a>Standardsymbole

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Standardsymbole sind fehler-, warnungs-, informations- und fragezeichensymbole, die Teil Windows sind.

![Screenshot von vier Standardsymbolen ](images/vis-std-icons-image1.png)

Die Standardsymbole für Fehler, Warnungen, Informationen und Fragezeichen.

Die Standardsymbole haben folgende Bedeutungen:

-   **Fehlersymbol.** Die Benutzeroberfläche zeigt einen Fehler oder ein aufgetretenes Problem an.
-   **Warnsymbol.** Die Benutzeroberfläche stellt eine Bedingung dar, die in Zukunft ein Problem verursachen kann.
-   **Informationssymbol.** Die Benutzeroberfläche stellt nützliche Informationen dar.
-   **Fragezeichensymbol.** Die Benutzeroberfläche gibt einen Hilfeeinstiegspunkt an.

Die Standardsymbole sind von Belang, da sie in viele Windows APIs (Application Programming Interfaces) integriert sind, z. B. [Aufgabendialoge,](win-dialog-box.md) [Meldungsfelder,](glossary.md) [Sprechblasen](ctrl-balloons.md)und [Benachrichtigungen.](mess-notif.md) Sie werden auch häufig für [lokale Nachrichten](glossary.md) und [Statusleisten](ctrl-status-bars.md)verwendet.

**Hinweis:** Richtlinien im Zusammenhang mit [Symbolen](vis-icons.md) werden in einem separaten Artikel vorgestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

Bei der Auswahl des geeigneten Standardsymbols gibt es mehrere Faktoren, die teilweise erklären, warum sie so oft falsch verwendet werden. Die häufigsten Fehler sind:

-   Verwenden eines Warnsymbols für kleinere Fehler. Warnungen sind keine "aufweichten" Fehler.
-   Verwenden eines Standardsymbols, wenn es besser ist, überhaupt kein Symbol zu verwenden. Nicht jede Nachricht benötigt ein Symbol.
-   Alarmierende Benutzer, indem Sie Warnungen für kleinere Probleme geben oder routinemäßige Fragen als Warnungen darstellen. Auf diese Weise erscheinen Programme anfällig für Gefährdungen und ziehen sich von wirklich signifikanten Problemen ab.

Im weiteren Verlauf dieses Abschnitts wird erläutert, wie Sie standardsymbole betrachten, um diese häufigen Fehler zu vermeiden.

### <a name="message-type-vs-severity"></a>Nachrichtentyp und Schweregrad

Wählen Sie Standardsymbole basierend auf dem Nachrichtentyp und nicht auf dem Schweregrad des zugrunde liegenden Problems aus. Die Nachrichtentypen sind:

-   **Fehler.** Ein Aufgetretener Fehler oder ein Aufgetretenes Problem.
-   **Warnung.** Eine Bedingung, die in Zukunft ein Problem verursachen kann.
-   **Informationen.** Nützliche Informationen.

Folglich kann eine Fehlermeldung ein Fehlersymbol, aber nie ein Warnsymbol annehmen. Verwenden Sie warnungssymbole nicht als Möglichkeit, kleinere Fehler zu "entschärfen". Trotz des Unterschieds im Schweregrad ist "Falscher Schriftgrad" ein Fehler, während "Wenn Sie mit diesem Vorgang fortfahren, wird Ihr Haus in Brand gesetzt" eine Warnung ist.

### <a name="determining-the-appropriate-message-type"></a>Bestimmen des geeigneten Nachrichtentyps

Einige Probleme können je nach Schwerpunkt und Ausdruck als Fehler, Warnung oder Information dargestellt werden. Angenommen, eine Webseite kann basierend auf der aktuellen Windows Internet Explorer Konfiguration keine nicht signierten ActiveX-Steuerelement laden:

-   **Fehler.** "Diese Seite kann kein steuerelement ohne Vorzeichen ActiveX laden." (Wird als vorhandenes Problem bezeichnet.)
-   **Warnung.** "Diese Seite verhält sich möglicherweise nicht wie erwartet, da Windows Internet Explorer nicht so konfiguriert ist, dass nicht signierte ActiveX-Steuerelemente geladen werden." oder "Zulassen, dass diese Seite ein nicht signiertes ActiveX-Steuerelement installiert? Wenn Sie dies aus nicht vertrauenswürdigen Quellen tun, kann dies ihrem Computer schaden." (Beide werden als Bedingungen bezeichnet, die zukünftige Probleme verursachen können.)
-   **Informationen.** "Sie haben Windows Internet Explorer so konfiguriert, dass nicht signierte ActiveX-Steuerelemente blockiert werden." (Als Faktenhinweis formuliert.)

**Um den geeigneten Nachrichtentyp zu bestimmen, konzentrieren Sie sich auf den wichtigsten Aspekt des Problems, den Benutzer kennen müssen oder auf den sie reagieren müssen.** Wenn ein Problem den Benutzer daran hindert, fortzufahren, wird es in der Regel als Fehler angezeigt. Wenn der Benutzer fortfahren kann, handelt es sich um eine Warnung. Erstellen Sie die [Hauptanweisung](text-ui.md) oder einen anderen entsprechenden Text basierend auf diesem Fokus, und wählen Sie dann ein Symbol (Standard oder anderweitig) aus, das dem Text entspricht. Der Hauptanweisungstext und die Symbole sollten immer übereinstimmen.

### <a name="severity"></a>Schweregrad

Obwohl der Schweregrad bei der Auswahl der Symbole für Fehler, Warnungen und Informationen keine Rolle spielt, ist der Schweregrad ein Faktor bei der **Bestimmung, ob überhaupt ein Standardsymbol verwendet werden soll.**

Symbole funktionieren am besten, wenn sie für die visuelle Kommunikation verwendet werden. (Beachten Sie, dass diese visuelle Kommunikation aus Gründen der Barrierefreiheit immer mit einem anderen Formular wie Text oder Sound redundant sein muss.) Benutzer sollten in der Lage sein, auf einen Blick die Art der Informationen und die Folgen ihrer Antwort zu erkennen, daher müssen wir kritische Fehler und Warnungen von ihren gewöhnlichen Entsprechungen unterscheiden. Kritische Fehler und Warnungen weisen folgende Merkmale auf:

-   Sie umfassen den möglichen Verlust einer oder mehrerer der folgenden Punkte:
    -   Eine wertvolle Ressource, z. B. Datenverlust oder finanzieller Verlust.
    -   Systemzugriff oder -integrität.
    -   Datenschutz oder Kontrolle über vertrauliche Informationen.
    -   Die Zeit des Benutzers (eine beträchtliche Menge, z. B. 30 Sekunden oder mehr).
-   Sie haben unerwartete oder unbeabsichtigte Folgen.
-   Sie erfordern jetzt eine korrekte Behandlung, da Fehler nicht einfach behoben werden können und sogar nicht rückgängig gemacht werden können.

Um nicht kritische Fehler und Warnungen von kritischen Fehlern zu unterscheiden, werden nicht kritische Meldungen in der Regel ohne Symbol angezeigt. Dadurch wird die Aufmerksamkeit auf kritische Nachrichten lenken, kritische und nicht kritische Meldungen visuell eindeutig und mit dem [Windows Tonfall](text-style-tone.md)konsistent.

Nicht jede Nachricht benötigt ein Symbol. Symbole sind keine Möglichkeit, Nachrichten zu verzieren.

Das folgende Beispiel ist ein gutes Beispiel für eine kritische Warnung, da sie die zuvor definierten Merkmale erfüllt.

![Screenshot einer Warnung zum Sichern von Daten ](images/vis-std-icons-image2.png)

In diesem Beispiel werden Benutzer mit einer kritischen Warnung vor einem möglichen nicht rückgängig gemachten Datenverlust gewarnt.

Das nächste Beispiel ist jedoch nicht entscheidend, da es wahrscheinlich beabsichtigt ist und seine Ergebnisse leicht rückgängig zu machen sind.

**Falsch:**

![Screenshot einer irreführenden Verwendung eines Warnsymbols ](images/vis-std-icons-image3.png)

In diesem Beispiel ist diese [Bestätigung](mess-confirm.md) nicht wichtig, da sie wahrscheinlich beabsichtigt und leicht rückgängig zu machen ist.

In einer typischen Benutzeroberfläche beziehen sich die meisten Fehler auf Benutzereingabefehler. Die meisten Benutzereingabefehler sind nicht wichtig, da sie leicht korrigiert werden können, und Benutzer müssen sie korrigieren, bevor sie fortfahren. Außerdem steht es im Gegensatz zum Windows Tonfall, zu viel Aufmerksamkeit auf kleinere Benutzerfehler zu lenken. Daher werden kleinere Benutzereingabefehler in der Regel ohne Fehlersymbol angezeigt. Um ihre nicht kritische Natur zu verstärken, bezeichnen wir diese als Benutzereingabeprobleme.

![Screenshot, der Benutzer über die richtige Eingabe informiert ](images/vis-std-icons-image4.png)

In diesem Beispiel ist dieses kleinere Benutzereingabeproblem nicht kritisch, sodass es kein Symbol benötigt, wenn es in einem Dialogfeld angezeigt wird.

### <a name="avoid-overwarning"></a>Vermeiden von Überwarnungen

Wir haben Windows Programme überwarnt. Das typische Windows Programms verfügt scheinbar überall über Warnsymbole, warnungen zu Dingen, die nur eine geringe Bedeutung haben. In einigen Programmen wird fast jede Frage als Warnung dargestellt. Eine Überhärtung bewirkt, dass die Verwendung eines Programms sich wie eine gefährliche Aktivität anfühlt und von wirklich signifikanten Problemen abweicht.

Das reine Risiko eines Datenverlusts allein reicht nicht aus, um ein Warnsymbol aufzurufen. Darüber hinaus sollten unerwünschte Ergebnisse unerwartet oder unbeabsichtigt sein und nicht einfach korrigiert werden. Andernfalls könnten fast alle falsch beantworteten Fragen so beantwortet werden, dass datenverluste irgendeiner Art entstehen und ein Warnsymbol angezeigt wird.

So konzentrieren Sie Warnsymbole auf wirklich kritische Probleme:

-   Stellen Sie sicher, dass das Problem erhöhte Aufmerksamkeit des Benutzers erforderlich macht. [Routinemäßige Bestätigungen](mess-confirm.md) und Fragen sollten keine Warnsymbole enthalten.
-   Verhalten sich Benutzer aufgrund des Warnsymbols wahrscheinlich anders? Ziehen Benutzer die Entscheidung wahrscheinlich sorgfältiger in Betracht?

**Falsch:**

![Screenshot des unnötig verwendeten Warnsymbols ](images/vis-std-icons-image5.png)

Gibt es in diesem Beispiel die Wahrscheinlichkeit, dass Benutzer diese Frage aufgrund des Warnsymbols unterschiedlich beantworten?

-   Gibt es einige wichtige Maßnahmen oder Entscheidungen zu treffen? Warnungen ohne Aktionen sorgen nur dafür, dass Benutzer paranoid sind.

**Falsch:**

![Screenshot des Mit Erinnerung verwendeten Warnsymbols ](images/vis-std-icons-image6.png)

Warum ist diese Benachrichtigung eine Warnung? Was sollen Benutzer tun (neben der Sorge)?

### <a name="context"></a>Kontext

Der Kontext ist auch ein Aspekt bei der Verwendung von Standardsymbolen, da der Kontext selbst Informationen kommuniziert. Dies gilt insbesondere in folgenden Fällen:

-   Während Dialogfelder (einschließlich Aufgabendialoge und Meldungsfelder) und Benachrichtigungen keine Symbole für nicht kritische Fehler benötigen, benötigen direkt auftretende Fehler immer Fehlersymbole. Andernfalls wäre ein solches nicht modales Feedback zu leicht zu übersehen.
-   Für warnungsbasierte Warnungen sind immer Warnsymbole erforderlich, um sie von regulärem Text zu unterscheiden.
-   Dialogfelder, Benachrichtigungen und Sprechblasen benötigen keine Informationssymbole, da sie informationen eindeutig darstellen. Im Gegensatz dazu benötigen Banner 16 x 16 Pixel Informationen oder andere Symbole, da ein solches nicht modales Feedback zu leicht zu übersehen wäre.

Da der Kontext ein wichtiger Faktor bei der Symbolverwendung ist, werden die Standardsymbolrichtlinien in diesem Artikel hinsichtlich ihres Kontexts angegeben.

### <a name="evaluating-standard-icon-appropriateness"></a>Auswerten der Standardsymbol-Eignung

Lesen Sie beim Auswerten des Benutzeroberflächentexts auch alle Standardsymbole. Lesen Sie Fehlersymbole als "Fehler!", Warnsymbole als "Warnung, seien Sie hier sehr vorsichtig!" und Informationssymbole als "Aufmerksamkeit!". Lesen Sie dann weiterhin den verbleibenden Kontext, z. B. die Hauptanweisung, den Inhaltsbereich und die Commitschaltflächen. Stellen Sie sicher, dass die Bedeutung und der Ton jedes Standardsymbols mit der Bedeutung und dem Ton des Kontexts übereinstimmen. Wenn dies nicht dere ist, haben Sie ein Problem gefunden.

**Wenn Sie nur eine Sache durchführen...**

Stellen Sie sicher, dass die Bedeutung und der Ton jedes Standardsymbols mit der Bedeutung und dem Ton des Kontexts übereinstimmen. Wenn sie nicht übereinstimmen, ändern oder entfernen Sie das Symbol.

## <a name="guidelines"></a>Richtlinien

**Hinweis:** Für die folgenden Richtlinien bedeutet "in-place" auf jeder normalen Fensteroberfläche, z. B. innerhalb des Inhaltsbereichs eines Assistenten, eines Eigenschaftenblatts oder einer Elementseite der Systemsteuerung.

### <a name="general"></a>Allgemein

-   Wählen Sie Standardsymbole basierend auf ihrem Nachrichtentyp aus, nicht auf dem Schweregrad des zugrunde liegenden Problems:
    -   **Fehler.** Ein Aufgetretener Fehler oder ein Aufgetretenes Problem.
    -   **Warnung.** Eine Bedingung, die in Zukunft ein Problem verursachen kann.
    -   **Informationen.** Nützliche Informationen.
-   Wenn ein Problem verschiedene Nachrichtentypen betrifft, konzentrieren Sie sich auf den wichtigsten Aspekt, auf den Benutzer reagieren müssen.
-   Symbole müssen immer mit der Hauptanweisung oder einem anderen entsprechenden Text übereinstimmen.

**Richtig:**

![Screenshot des Mit Fehlertexts verwendeten Fehlersymbols ](images/vis-std-icons-image7.png)

**Falsch:**

![Screenshot des Mit Fehlertexts verwendeten Warnsymbols ](images/vis-std-icons-image8.png)

Im falschen Beispiel stimmt das Standardwarnungssymbol nicht mit der Hauptanweisung überein (was einen Fehler ergibt).

### <a name="icon-size"></a>Symbolgröße

-   **Wählen Sie die Standardsymbolgröße basierend auf dem Kontext aus:**
  



    | Kontext                         | Verwendung                                                                                        |
    |--------------------------|-----------------------------------------------------------------------------------------|
    | Dialogfelder<br/>  | Verwenden Sie 32 x 32 Pixel für Inhaltsbereichssymbole. 16 x 16 Pixel für Fußnotenbereichssymbole.<br/> |
    | Direkt<br/>      | Verwenden Sie 32 x 32 Pixel für Fehlerseiten. Symbole mit 16 x 16 Pixeln für alle anderen.<br/>           |
    | Benachrichtigungen<br/> | Verwenden Sie Symbole mit 16 x 16 Pixeln.<br/>                                                       |
    | Ballons<br/>      | Verwenden Sie Symbole mit 16 x 16 Pixeln.<br/>                                                       |
    | Banner<br/>       | Verwenden Sie Symbole mit 16 x 16 Pixeln.<br/>                                                       |



 

### <a name="error-icons"></a>Fehlersymbole

-   **Verwenden Sie Fehlersymbole nur, wenn ein Fehler oder ein Problem aufgetreten ist:**



    | Kontext                           | Verwendung                                                                                                                                                                                                                                             |
    |----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Dialogfelder<br/>    | Nur für kritische Fehler verwenden. (Verwenden Sie keine Standardsymbole für nicht kritische Fehler.) <br/> ![Screenshot des mit der Fehlermeldung verwendeten Fehlersymbols ](images/vis-std-icons-image9.png)<br/>                                              |
    | Fehler an Ort und Stelle<br/> | Verwenden Sie für alle Fehler. <br/> ![Screenshot des Mit einer Fehlermeldung verwendeten Fehlersymbols.](images/vis-std-icons-image10.png)<br/>                                                                                                           |
    | Benachrichtigungen<br/>   | Nur für kritische Fehler verwenden. (für [Aktionsfehler](https://msdn.microsoft.com/library/windows/desktop/aa511497.aspx).) <br/> ![Screenshot: Fehlersymbol, das mit einer Benachrichtigungsfehlermeldung verwendet wird](images/vis-std-icons-image11.png)<br/> |
    | Ballons<br/>        | Nicht verwenden. Balloons sollten nicht für kritische Fehler verwendet werden, und sie benötigen keine Fehlersymbole für nicht kritische Fehler.<br/>                                                                                                               |
    | Banner<br/>         | Nicht verwenden. Banner sollten nicht für Fehler verwendet werden.<br/>                                                                                                                                                                                  |



 

-   Im Allgemeinen sind Fehlersymbole für nicht kritische Benutzereingabeprobleme nicht erforderlich. Allerdings sind Symbole für direkt auftretende Fehler erforderlich, da ein solches kontextbezogenes Feedback andernfalls zu leicht zu übersehen wäre.
-   **Verwenden Sie für Aufgabendialoge keine Fehlernotesymbole.** Fehlersymbole dürfen nur im Inhaltsbereich angezeigt werden.

### <a name="warning-icons"></a>Warnsymbole

-   **Verwenden Sie Warnsymbole nur, wenn eine Bedingung in Zukunft zu einem Problem führen kann:**



    | Kontext                             |  Verwendung                                                                                                                                                                                      |
    |------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Dialogfelder<br/>      | Verwenden Sie für alle Warnungen. <br/> ![Screenshotwarnung vor Änderung der Dateinamenerweiterung ](images/vis-std-icons-image12.png)<br/>                                                   |
    | Warnungen an Ort und Stelle<br/> | Verwenden Sie , um den Text als Warnung zu identifizieren. <br/> ![Screenshot der Warnung vor nicht genügend freiem Speicherplatz ](images/vis-std-icons-image13.png)<br/>                                    |
    | Benachrichtigungen<br/>     | Verwenden Sie für alle Warnungen. (für [nicht kritische Systemereignisse.)](glossary.md) <br/> ![Screenshot der Warnungsbenachrichtigung mit geringem Akkustand ](images/vis-std-icons-image14.png)<br/> |
    | Ballons<br/>          | Verwenden Sie für [besondere Bedingungen.](ctrl-balloons.md) <br/> ![Screenshot: Sprechblasenwarnung vor Sperre von Obergrenzen ](images/vis-std-icons-image15.png)<br/>                           |
    | Banner<br/>           | Verwenden Sie , um die Aufmerksamkeit auf das Banner zu lenken. <br/> ![Screenshot des Banners mit Warnung vor fehlendem TPM ](images/vis-std-icons-image16.png)<br/>                                    |



 

-   **Verwenden Sie keine Warnsymbole, um nicht kritische Fehler zu "entschärfen".** Fehler sind keine Warnungen. Wenden Sie stattdessen die Richtlinien für Fehlersymbole an.
-   **Verwenden Sie für Fragedialoge Warnsymbole nur für Fragen mit erheblichen Konsequenzen.** Verwenden Sie keine Warnsymbole für Routinefragen.

**Richtig:**

![Screenshotwarnung zum Beenden der Systemwiederherstellung ](images/vis-std-icons-image17.png)

**Falsch:**

![Screenshot der Warnung zum Verwerfen von Erinnerungen ](images/vis-std-icons-image18.png)

Im falschen Beispiel wird ein Warnsymbol fälschlicherweise für eine Routinefrage verwendet.

-   **Für Aufgabendialoge können Sie ein Warnsymbol für Fußnoten verwenden, um Benutzer vor riskanten Folgen zu warnen.** Verwenden Sie jedoch entweder im Inhaltsbereich oder im Fußnotenbereich ein Warnsymbol, aber nicht beides.

![Screenshotwarnung einer potenziell unsicheren Datei ](images/vis-std-icons-image19.png)

In diesem Beispiel wird ein gelber Sicherheitsschild in einer Fußnote verwendet.

### <a name="information-icons"></a>Informationssymbole

-   **Verwenden Sie Informationssymbole nur, wenn der Kontext offensichtlich keine Informationen darstellt:**



    | Kontext                         | Verwendung                                                                                                                                                  |
    |--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
    | Dialogfelder<br/>  | Nicht verwenden.<br/>                                                                                                                             |
    | Direkt<br/>      | Nicht verwenden. Verwenden Sie stattdessen entweder einfachen statischen Text oder ein Banner.<br/>                                                                           |
    | Benachrichtigungen<br/> | Nicht verwenden.<br/>                                                                                                                             |
    | Ballons<br/>      | Nicht verwenden.<br/>                                                                                                                             |
    | Banner<br/>       | verwenden Sie , um die Aufmerksamkeit auf das Banner zu lenken. <br/> ![Screenshot des Banners mit Einstellungsinformationen ](images/vis-std-icons-image20.png)<br/> |



 

-   Informationssymbole werden in Dialogfeldern, Benachrichtigungen und Sprechblasen nicht benötigt, da ihr Kontext ausreichend kommuniziert, dass sie Benutzern Informationen bereitstellen.
-   **Verwenden Sie für Aufgabendialoge keine Informationsnotesymbole.** Fußnoten sind ausreichend sichtbar, und es versteht sich von selbst, dass es sich um Informationen handelt.

### <a name="question-mark-icons"></a>Fragezeichensymbole

-   **Verwenden Sie das Fragezeichensymbol nur für Hilfeeinstiegspunkte.** Weitere Informationen finden Sie in den Richtlinien [für Hilfeeinstiegspunkte.](winenv-help.md)
-   **Verwenden Sie nicht das Fragezeichensymbol, um Fragen zu stellen.** Verwenden Sie auch hier das Fragezeichensymbol nur für Hilfeeinstiegspunkte. Es ist nicht erforderlich, Fragen mithilfe des Fragezeichensymbols zu stellen. Es reicht trotzdem aus, eine Hauptanweisung als Frage darzustellen.
-   **Ersetzen Sie Fragezeichensymbole nicht routinemäßig durch Warnsymbole.** Ersetzen Sie ein Fragezeichensymbol nur dann durch ein Warnsymbol, wenn die Frage erhebliche Konsequenzen hat. Verwenden Sie andernfalls kein Symbol.

 

