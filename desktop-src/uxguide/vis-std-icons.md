---
title: Standardsymbole
description: Standard Symbole sind die Symbole "Fehler", "Warnung", "Information" und "Fragezeichen", die Teil von Windows sind.
ms.assetid: 63b5c31d-5094-4299-b44b-35b2452ce706
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 69085f4c527db8431b5e33f0dba4668d43d1c669
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351058"
---
# <a name="standard-icons"></a>Standardsymbole

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Standard Symbole sind die Symbole "Fehler", "Warnung", "Information" und "Fragezeichen", die Teil von Windows sind.

![Screenshot von vier Standardsymbolen ](images/vis-std-icons-image1.png)

Die Symbole Standardfehler, Warnung, Information und Fragezeichen.

Die Standardsymbole haben folgende Bedeutungen:

-   **Fehler Symbol.** Die Benutzeroberfläche zeigt einen Fehler oder ein Problem an, der aufgetreten ist.
-   **Warnsymbol.** Die Benutzeroberfläche stellt eine Bedingung dar, die in der Zukunft ein Problem verursachen kann.
-   **Informationssymbol.** Die Benutzeroberfläche stellt nützliche Informationen dar.
-   **Symbol für Fragezeichen.** Die Benutzeroberfläche gibt einen Einstiegspunkt für die Hilfe an.

Die Standardsymbole sind bemerkenswert, da Sie in viele Windows-Anwendungs Programmierschnittstellen (APIs) integriert sind, z. b. [Aufgaben Dialogfelder](win-dialog-box.md), Meldungs [Felder](glossary.md), [Luftballons](ctrl-balloons.md)und [Benachrichtigungen](mess-notif.md). Sie werden auch häufig für direkte [Nachrichten](glossary.md) und [Status leisten](ctrl-status-bars.md)verwendet.

**Hinweis:** Die Richtlinien im Zusammenhang mit [Symbolen](vis-icons.md) werden in einem separaten Artikel dargestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

Es gibt mehrere Faktoren bei der Auswahl des geeigneten Standard Symbols, das teilweise erläutert, warum Sie so oft falsch verwendet werden. Die häufigsten Fehler sind:

-   Verwenden eines Warn Symbols für kleinere Fehler. Warnungen sind keine "weich"-Fehler.
-   Verwenden Sie ein Standard Symbol, wenn es besser ist, überhaupt kein Symbol zu verwenden. Nicht jede Nachricht benötigt ein Symbol.
-   Warnen von Benutzern durch die Gewährung von Warnungen für kleinere Probleme oder das präsentieren von Routine Fragen als Warnungen. Dadurch werden Programme anfällig für Gefährdungen und werden von wirklich wichtigen Problemen entfernt.

Im restlichen Teil dieses Abschnitts wird erläutert, wie Sie Standardsymbole vorstellen, um diese häufigen Fehler zu vermeiden.

### <a name="message-type-vs-severity"></a>Nachrichtentyp im Vergleich zu Schweregrad

Wählen Sie Standardsymbole basierend auf dem Nachrichtentyp und nicht mit dem Schweregrad des zugrunde liegenden Problems aus. Die Nachrichten Typen lauten wie folgt:

-   **Zeit.** Ein Fehler oder ein Problem, der aufgetreten ist.
-   **Davor.** Eine Bedingung, die in der Zukunft ein Problem verursachen kann.
-   **Informationen.** Nützliche Informationen.

Folglich kann eine Fehlermeldung ein Fehler Symbol, aber nie ein Warnsymbol annehmen. Verwenden Sie Warn Symbole nicht als Möglichkeit zum "weichen" von geringfügigen Fehlern. Trotz des schwere Grads des schwere Grads ist die "falsche Schriftart Größe" ein Fehler, während "mit diesem Vorgang wird das Haus beim Auslösen" festgelegt wird.

### <a name="determining-the-appropriate-message-type"></a>Bestimmen des geeigneten Nachrichten Typs

Einige Probleme können je nach Betonung und Formulierung als Fehler, Warnung oder Informationen angezeigt werden. Nehmen Sie beispielsweise an, eine Webseite kann ein nicht signiertes ActiveX-Steuerelement nicht auf Grundlage der aktuellen Windows Internet Explorer-Konfiguration laden:

-   **Zeit.** "Auf dieser Seite kann kein nicht signiertes ActiveX-Steuerelement geladen werden." (Als vorhandenes Problem formuliert.)
-   **Davor.** "Diese Seite verhält sich möglicherweise nicht wie erwartet, da Windows Internet Explorer nicht zum Laden von nicht signierten ActiveX-Steuerelementen konfiguriert ist." oder "Diese Seite darf ein nicht signiertes ActiveX-Steuerelement installieren? Wenn Sie dies aus nicht vertrauenswürdigen Quellen machen, kann dies Ihren Computer beeinträchtigen. " (Beide werden als Bedingungen formuliert, die möglicherweise zukünftige Probleme verursachen.)
-   **Informationen.** "Sie haben Windows Internet Explorer so konfiguriert, dass nicht signierte ActiveX-Steuerelemente blockiert werden." (Als eine-Anweisung formuliert.)

**Um den richtigen Nachrichtentyp zu bestimmen, konzentrieren Sie sich auf den wichtigsten Aspekt des Problems, das Benutzer kennen oder reagieren müssen.** Wenn ein Problem darin besteht, dass der Benutzer nicht mehr fortfahren kann, wird es normalerweise als Fehler angezeigt. Wenn der Benutzer fortfahren kann, handelt es sich um eine Warnung. Erstellen Sie die [Haupt Anweisung](text-ui.md) oder einen anderen entsprechenden Text basierend auf diesem Fokus, und wählen Sie dann ein Symbol (Standard oder anderweitig), das mit dem Text übereinstimmt. Der Hauptanweisungs Text und die Symbole sollten immer mit dem Text identisch sein

### <a name="severity"></a>severity

Der Schweregrad ist bei der Auswahl der Symbole "Fehler", "Warnung" und "Information" nicht zu berücksichtigen, aber der **Schweregrad ist ein Faktor für die Bestimmung, ob überhaupt ein Standard Symbol verwendet werden soll.**

Symbole funktionieren am besten, wenn Sie für die visuelle Kommunikation verwendet werden. (Beachten Sie, dass diese visuelle Kommunikation aus Gründen der Barrierefreiheit immer mit einer anderen Form, wie z. b. Text oder Sound, redundant sein muss.) Benutzer sollten in der Lage sein, die Art der Informationen und die Folgen ihrer Reaktion auf einen Blick zu erkennen. Daher müssen wir kritische Fehler und Warnungen von ihren normalen Gegenstücken unterscheiden. Kritische Fehler und Warnungen haben folgende Merkmale:

-   Sie beinhalten mögliche Verluste von einem oder mehreren der folgenden:
    -   Ein wertvolles Asset, z. b. Datenverlust oder finanzieller Verlust.
    -   System Zugriff oder-Integrität.
    -   Datenschutz oder Kontrolle über vertrauliche Informationen.
    -   Benutzer Zeit (eine beträchtliche Menge, z. b. 30 Sekunden oder mehr).
-   Sie haben unerwartete oder unbeabsichtigte Konsequenzen.
-   Sie benötigen jetzt eine korrekte Behandlung, da Fehler nicht einfach behoben werden können und sogar nicht mehr rückgängig gemacht werden können.

Um nicht kritische Fehler und Warnungen von kritischen Fehlern zu unterscheiden, werden nicht kritische Nachrichten normalerweise ohne ein Symbol angezeigt. Auf diese Weise werden wichtige Nachrichten berücksichtigt, kritische und nicht kritische Nachrichten werden visuell unterschieden, und Sie sind mit dem [Windows-Ton](text-style-tone.md)konsistent.

Nicht jede Nachricht benötigt ein Symbol. Symbole sind keine Möglichkeit, Nachrichten zu ergänzen.

Im folgenden finden Sie ein gutes Beispiel für eine kritische Warnung, da Sie den zuvor definierten Merkmalen entspricht.

![Screenshot einer Warnung zum Sichern von Daten ](images/vis-std-icons-image2.png)

In diesem Beispiel warnt eine kritische Warnung die Benutzer über den möglichen Verlust von Datenverlusten.

Das nächste Beispiel ist jedoch nicht wichtig, da es wahrscheinlich beabsichtigt ist und seine Ergebnisse leicht rückgängig gemacht werden.

**Falsch:**

![Screenshot einer irreführenden Verwendung eines Warn Symbols ](images/vis-std-icons-image3.png)

In diesem Beispiel ist diese [Bestätigung](mess-confirm.md) nicht wichtig, da Sie wahrscheinlich absichtlich und leicht rückgängig gemacht wird.

In einer typischen Benutzeroberfläche stehen die meisten Fehler in Beziehung zu Benutzereingabe Fehlern. Die meisten Benutzereingabe Fehler sind nicht wichtig, da Sie leicht korrigiert werden können, bevor Sie fortfahren. Außerdem ist das Zeichnen von zu viel Aufmerksamkeit auf kleinere Benutzerfehler mit dem Windows-Ton zu tun. Folglich werden kleinere Benutzereingabe Fehler normalerweise ohne Fehler Symbol angezeigt. Um Ihre nicht kritische Art zu verstärken, bezeichnen wir diese als Probleme bei der Benutzereingabe.

![Screenshot, der Benutzer über die richtige Eingabe informiert ](images/vis-std-icons-image4.png)

In diesem Beispiel ist dieses geringfügige Benutzereingabe Problem nicht wichtig, sodass es kein Symbol benötigt, wenn es in einem Dialogfeld angezeigt wird.

### <a name="avoid-overwarning"></a>Vermeiden von überschreinungs Warnungen

In Windows-Programmen wird eine übermäßige Warnung angezeigt. Das typische Windows-Programm weist scheinbar überall Warn Symbole auf, und es wird eine Warnung bezüglich Dingen angezeigt, die wenig Bedeutung haben In einigen Programmen wird fast jede Frage als Warnung angezeigt. Durch die übermäßige Warnung wird die Verwendung eines Programms wie eine gefährliche Aktivität vereinfacht, und es wird von wirklich wichtigen Problemen entfernt.

Das einzige Potenzial für einen Datenverlust allein reicht nicht aus, um ein Warnsymbol aufzurufen. Außerdem sollten unerwünschte Ergebnisse unerwartet oder unbeabsichtigt und nicht leicht korrigiert werden. Andernfalls könnte fast jede falsch beantwortete Frage so interpretiert werden, dass Sie zu einem Datenverlust führt und ein Warnsymbol verdient.

So konzentrieren Sie Warn Symbole auf wirklich kritische Probleme:

-   Stellen Sie sicher, dass das Problem eine erhöhte Benutzer Aufmerksamkeit erfordert. [Routine Bestätigungen](mess-confirm.md) und-Fragen sollten keine Warn Symbole aufweisen.
-   Verhalten sich Benutzer wahrscheinlich aufgrund des Warn Symbols anders? Werden Benutzer die Entscheidung wahrscheinlich genauer in Erwägung ziehen?

**Falsch:**

![Screenshot des Warn Symbols, das unnötig verwendet wird ](images/vis-std-icons-image5.png)

In diesem Beispiel können Benutzer diese Frage aufgrund des Warn Symbols unterschiedlich beantworten?

-   Gibt es einige bedeutende Maßnahmen oder Entscheidungen, die getroffen werden müssen? Warnungen ohne Aktionen machen es einfach, dass die Benutzer in der Meinung sind

**Falsch:**

![Screenshot des Warn Symbols, das mit Erinnerung verwendet wird ](images/vis-std-icons-image6.png)

Warum ist diese Benachrichtigung eine Warnung? Was sollten Benutzer tun (neben Sorge)?

### <a name="context"></a>Kontext

Der Kontext ist auch bei der Verwendung von Standardsymbolen von bedacht, da der Kontext selbst Informationen kommuniziert. Dies gilt insbesondere in folgenden Fällen:

-   Während Dialogfelder (einschließlich Aufgaben Dialogfeldern und Meldungs Feldern) und Benachrichtigungen keine Symbole für nicht schwerwiegende Fehler benötigen, werden bei direkten Fehlern immer Fehler Symbole benötigt. Andernfalls wäre ein solches nicht modales Feedback zu leicht zu übersehen.
-   Direkte Warnungen benötigen immer Warn Symbole, um Sie von regulären Text zu unterscheiden.
-   Dialog Felder, Benachrichtigungen und Luftballons benötigen keine Informations Symbole, da Sie eindeutig Informationen darstellen. Im Gegensatz dazu benötigen Banner 16x16 Pixel Informationen oder andere Symbole, da dieses nicht modale Feedback zu leicht zu übersehen wäre.

Da der Kontext ein bedeutender Faktor bei der Verwendung von Symbolen ist, werden die Standard-Symbol Richtlinien in diesem Artikel in Bezug auf ihren Kontext angegeben.

### <a name="evaluating-standard-icon-appropriateness"></a>Auswerten der Standard Symbol-Eignung

Wenn Sie den Benutzeroberflächen Text auswerten, lesen Sie auch alle Standardsymbole. Lesen Sie die Fehler Symbole als "Fehler!", Warn Symbole als "Warnung, seien Sie hier!" und Informations Symbole als "Aufmerksamkeit!". Fahren Sie dann mit dem verbleibenden Kontext fort, z. b. die Haupt Anweisung, den Inhalts Bereich und die Commit-Schaltflächen. Stellen Sie sicher, dass die Bedeutung und der Ton der einzelnen Standardsymbole mit der Bedeutung und dem Farbton des Kontexts übereinstimmen. Wenn dies nicht der Fall ist, haben Sie ein Problem festgestellt.

**Wenn Sie nur eine Aktion ausführen...**

Stellen Sie sicher, dass die Bedeutung und der Ton der einzelnen Standardsymbole mit der Bedeutung und dem Farbton des Kontexts übereinstimmen. Wenn Sie nicht identisch sind, ändern oder entfernen Sie das Symbol.

## <a name="guidelines"></a>Richtlinien

**Hinweis:** Für die folgenden Richtlinien bedeutet "direkt" auf jeder normalen Fenster Oberfläche, z. b. innerhalb des Inhalts Bereichs eines Assistenten, eines Eigenschaften Blatts oder einer System Steuerungselement-Seite.

### <a name="general"></a>Allgemein

-   Wählen Sie Standardsymbole basierend auf dem Nachrichtentyp und nicht mit dem Schweregrad des zugrunde liegenden Problems aus:
    -   **Zeit.** Ein Fehler oder ein Problem, der aufgetreten ist.
    -   **Davor.** Eine Bedingung, die in der Zukunft ein Problem verursachen kann.
    -   **Informationen.** Nützliche Informationen.
-   Wenn ein Problem verschiedene Nachrichten Typen überschreitet, konzentrieren Sie sich auf den wichtigsten Aspekt, auf den Benutzer reagieren müssen.
-   Symbole müssen immer mit der Main-Anweisung oder einem anderen entsprechenden Text übereinstimmen.

**Richtig:**

![Screenshot des mit Fehlertext verwendeten Fehler Symbols ](images/vis-std-icons-image7.png)

**Falsch:**

![Screenshot des mit Fehlertext verwendeten Warn Symbols ](images/vis-std-icons-image8.png)

Im falschen Beispiel stimmt das Standard Warnsymbol nicht mit der Main-Anweisung (die einen Fehler ergibt) ab.

### <a name="icon-size"></a>Symbolgröße

-   **Wählen Sie die Standard Symbolgröße basierend auf dem Kontext aus:**
  



    | Kontext                         | Verwendung                                                                                        |
    |--------------------------|-----------------------------------------------------------------------------------------|
    | Dialogfelder<br/>  | 32 x 32 Pixel für Inhalts Bereichs Symbole verwenden; 16x16 Pixel für Fußnote-Bereichs Symbole.<br/> |
    | Direkt<br/>      | 32 x 32 Pixel für Fehlerseiten verwenden; 16 x 16 Pixel Symbole für alle anderen.<br/>           |
    | Benachrichtigungen<br/> | Verwenden Sie 16x16 Pixel-Symbole.<br/>                                                       |
    | Ballons<br/>      | Verwenden Sie 16x16 Pixel-Symbole.<br/>                                                       |
    | Mitzubringen<br/>       | Verwenden Sie 16x16 Pixel-Symbole.<br/>                                                       |



 

### <a name="error-icons"></a>Fehler Symbole

-   **Verwenden Sie Fehler Symbole nur dann, wenn ein Fehler oder ein Problem aufgetreten ist:**



    | Kontext                           | Verwendung                                                                                                                                                                                                                                             |
    |----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Dialogfelder<br/>    | Nur bei kritischen Fehlern verwendet werden. (verwenden Sie keine Standardsymbole für nicht kritische Fehler.) <br/> ![Screenshot, der das mit der Fehlermeldung verwendete Fehler Symbol anzeigt ](images/vis-std-icons-image9.png)<br/>                                              |
    | Direkte Fehler<br/> | Verwenden Sie für alle Fehler. <br/> ![Screenshot des Fehler Symbols, das mit einer Fehlermeldung verwendet wird.](images/vis-std-icons-image10.png)<br/>                                                                                                           |
    | Benachrichtigungen<br/>   | Nur bei kritischen Fehlern verwendet werden. (bei [Aktions Fehlern](https://msdn.microsoft.com/library/windows/desktop/aa511497.aspx).) <br/> ![Screenshot, der ein Fehler Symbol anzeigt, das mit einer Benachrichtigungs Fehlermeldung verwendet wird.](images/vis-std-icons-image11.png)<br/> |
    | Ballons<br/>        | Verwenden Sie nicht. Ballons sollten nicht für kritische Fehler verwendet werden, und Sie benötigen keine Fehler Symbole für nicht kritische Fehler.<br/>                                                                                                               |
    | Mitzubringen<br/>         | Verwenden Sie nicht. Banner sollten nicht für Fehler verwendet werden.<br/>                                                                                                                                                                                  |



 

-   Im Allgemeinen sind Fehler Symbole für nicht kritische Probleme bei der Benutzereingabe nicht erforderlich. Symbole werden jedoch für direkte Fehler benötigt, da dieses kontextbezogene Feedback zu leicht zu übersehen wäre.
-   **Verwenden Sie für Aufgaben Dialogfelder keine Fehler Fußnote-Symbole.** Fehler Symbole müssen nur im Inhalts Bereich angezeigt werden.

### <a name="warning-icons"></a>Warn Symbole

-   **Verwenden Sie Warn Symbole nur dann, wenn eine Bedingung in der Zukunft ein Problem verursachen kann:**



    | Kontext                             |  Verwendung                                                                                                                                                                                      |
    |------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Dialogfelder<br/>      | Verwenden Sie für alle Warnungen. <br/> ![Bildschirm Abbildung der Änderung der Dateinamenerweiterung ](images/vis-std-icons-image12.png)<br/>                                                   |
    | Direkte Warnungen<br/> | Verwenden Sie, um den Text als Warnung zu identifizieren. <br/> ![Screenshot der Warnung, dass nicht genügend freier Speicherplatz verfügbar ist ](images/vis-std-icons-image13.png)<br/>                                    |
    | Benachrichtigungen<br/>     | Verwenden Sie für alle Warnungen. (für [nicht kritische Systemereignisse](glossary.md).) <br/> ![Screenshot der Warn Benachrichtigung mit geringer Akkukapazität ](images/vis-std-icons-image14.png)<br/> |
    | Ballons<br/>          | Verwenden Sie dies für [spezielle Bedingungen](ctrl-balloons.md). <br/> ![Screenshot der Sprechblasen Warnung bei der FESTSTELL Sperre ](images/vis-std-icons-image15.png)<br/>                           |
    | Mitzubringen<br/>           | Verwenden Sie, um auf das Banner aufmerksam zu machen. <br/> ![Screenshot des Banners mit der Warnung "Fehlendes TPM" ](images/vis-std-icons-image16.png)<br/>                                    |



 

-   **Verwenden Sie keine Warn Symbole, um nicht schwerwiegende Fehler zu "weichen".** Fehler sind keine Warnungen wenden Sie stattdessen die Fehler Symbol Richtlinien an.
-   **Verwenden Sie für Frage Dialogfelder Warnungs Symbole nur für Fragen mit erheblichen Konsequenzen.** Verwenden Sie keine Warn Symbole für Routine Fragen.

**Richtig:**

![Bildschirm Abbildung Warnung zum Verhindern der Systemwiederherstellung ](images/vis-std-icons-image17.png)

**Falsch:**

![Screenshot der Warnung über fehlende Erinnerungen ](images/vis-std-icons-image18.png)

Im falschen Beispiel wird ein Warnsymbol fälschlicherweise für eine Routine Frage verwendet.

-   **Für Aufgaben Dialogfelder können Sie das Symbol für die fußnotiz "Warnung" verwenden, um Benutzer über riskante Konsequenzen zu benachrichtigen.** Verwenden Sie jedoch ein Warnsymbol entweder im Inhalts Bereich oder im fußnotiz Bereich, aber nicht in beiden.

![Screenshot der Warnung einer potenziell unsicheren Datei ](images/vis-std-icons-image19.png)

In diesem Beispiel wird ein gelbes Sicherheitsschild in einer fußnotiz verwendet.

### <a name="information-icons"></a>Informations Symbole

-   **Verwenden Sie Informations Symbole nur, wenn der Kontext nicht offensichtlich Informationen darstellt:**



    | Kontext                         | Verwendung                                                                                                                                                  |
    |--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
    | Dialogfelder<br/>  | Verwenden Sie nicht.<br/>                                                                                                                             |
    | Direkt<br/>      | Verwenden Sie nicht. Verwenden Sie stattdessen entweder einfachen statischen Text oder ein Banner.<br/>                                                                           |
    | Benachrichtigungen<br/> | Verwenden Sie nicht.<br/>                                                                                                                             |
    | Ballons<br/>      | Verwenden Sie nicht.<br/>                                                                                                                             |
    | Mitzubringen<br/>       | Verwenden Sie, um auf das Banner aufmerksam zu machen. <br/> ![Screenshot des Banners mit Einstellungs Informationen ](images/vis-std-icons-image20.png)<br/> |



 

-   Informations Symbole werden in Dialogfeldern, Benachrichtigungen und Luftballons nicht benötigt, da Ihr Kontext ausreichend kommuniziert, dass Sie Benutzern Informationen bereitstellen.
-   **Verwenden Sie für Aufgaben Dialogfelder keine Info-Fußnote-Symbole.** Fußnoten sind ausreichend sichtbar, und es wird nicht gesagt, dass Sie Informationen sind.

### <a name="question-mark-icons"></a>Fragezeichen Symbole

-   **Verwenden Sie das Fragezeichen-Symbol nur für Hilfe Einstiegspunkte.** Weitere Informationen finden Sie in den Richtlinien für den [Einstiegspunkt der Hilfe](winenv-help.md) .
-   **Verwenden Sie das Fragezeichen Symbol nicht, um Fragen zu stellen.** Verwenden Sie das Fragezeichen-Symbol nur für Hilfe Einstiegspunkte. Es ist nicht erforderlich, mit dem Fragezeichen-Symbol Fragen zu stellen. es ist trotzdem ausreichend, eine Haupt Anweisung als Frage zu präsentieren.
-   **Ersetzen Sie Fragezeichen Symbole nicht routinemäßig durch Warnungs Symbole.** Ersetzen Sie ein Fragezeichen Symbol nur dann durch ein Warnsymbol, wenn die Frage bedeutende Konsequenzen hat. Andernfalls verwenden Sie kein Symbol.

 

