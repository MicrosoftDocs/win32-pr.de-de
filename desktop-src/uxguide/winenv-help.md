---
title: Hilfe
description: Verwenden Sie Hilfe als sekundären Mechanismus, um Benutzern zu helfen, Aufgaben abzuschließen und besser zu verstehen \ 8212; der primäre Mechanismus ist die Benutzeroberfläche selbst. Wenden Sie diese Richtlinien an, um die Inhalte wirklich hilfreich und leicht zu finden.
ms.assetid: 82ce076e-062b-4793-a1c0-ed96c0f2b284
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: f9b1260128eb253a2d501a810923ae809c5f8187
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443242"
---
# <a name="help"></a>Hilfe

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Verwenden Sie Hilfe als sekundären Mechanismus, um Benutzern zu helfen, Aufgaben abzuschließen und besser zu verstehen, wobei der primäre Mechanismus die Benutzeroberfläche selbst ist. Wenden Sie diese Richtlinien an, um die Inhalte wirklich hilfreich und leicht zu finden.

Ein Hilfesystem besteht aus verschiedenen Arten von Inhalten, die Benutzern helfen sollen, wenn sie eine Aufgabe nicht ausführen können, ein Konzept ausführlicher verstehen oder mehr technische Details benötigen, als auf der Benutzeroberfläche verfügbar sind.

In diesem Artikel beziehen wir uns auf Hilfe als sekundär zur Benutzeroberfläche. Die Benutzeroberfläche ist primär, da benutzer hier zuerst versuchen, ihre Probleme zu lösen. Sie wenden sich nur dann an das Hilfesystem, wenn sie ihre Aufgabe nicht über die Benutzeroberfläche ausführen können.

![Screenshot der Windows-Hilfe- und -Supportseite ](images/winenv-help-image1.png)

Die Startseite für Windows-Hilfe und -Support, die über die Startmenü verfügbar ist.

**Hinweis:** Richtlinien im Zusammenhang mit [Stil und Tonfall](text-style-tone.md) werden in einem separaten Artikel vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Wie motiviert sind Ihre Zielbenutzer?** Je stärker sie die Funktionalität Ihres Programms entdecken und fortgeschrittene oder sogar fortgeschrittene Benutzer werden, desto mehr sind sie bereit, Antworten auf ihre Fragen zu recherchieren, indem sie Hilfethemen lesen.
-   **Verwenden Sie Hilfe, um eine fehlerhafte Benutzeroberfläche zu beheben?** Je besser Ihre Benutzeroberfläche ist, desto weniger Benutzer suchen zusätzliche Hilfe. Wenn Ihr Programm über eine sehr klare, hilfreiche primäre Benutzeroberfläche verfügt (z. B. jargonfreie Fehlermeldungen, gut geschriebene Assistenten und eindeutige Dialogfelder), benötigen Sie möglicherweise überhaupt kein sekundäres Hilfesystem.
-   **Ist Ihr Programm relativ einfach?** Falls ja, sollten Sie alle erforderlichen Unterstützungsinhalte in Ihre primären Benutzeroberflächen integrieren. Benutzer suchen eher zusätzliche Hilfe in Programmen, die komplexe Aufgaben ausführen.
-   **Ist Ihre Anwendung für Entwickler, IT-Experten oder andere Softwareexperten vorgesehen?** Diese Benutzer erwarten in der Regel Referenzhilfe für Programmiersprachenkonventionen und ausführliche konzeptionelle Hilfe zur Bemasterung von Features.

## <a name="design-concepts"></a>Entwurfskonzepte

Wenn Sie hilfe in Ihr Programm aufnehmen möchten, integrieren Sie es in Ihren Gesamtentwurf. Die Hilfeschnittstelle sollte einfach, effizient und relevant sein. Sie sollte es Benutzern ermöglichen, auf einfache Weise Hilfe zu erhalten und dann zu ihrer Aufgabe zurückzukehren. Stellen Sie sich Ihr Hilfesystem in Bezug auf die Zeit der Benutzer vor: Minimieren Sie zuerst die Unterbrechung, indem Sie vorhersehen, wo probleme in Ihrem Programm auftreten werden, und dann diese Probleme lösen, indem Sie grundlegende Unterstützung direkt in Ihre Benutzeroberfläche integrieren und klare und konsistente Einstiegspunkte in Ihre ausführlichere Hilfe erstellen.

Die Windows-Unterstützung wurde gemäß diesen Prinzipien entworfen. Hier sind einige der Entwurfsänderungen an der Benutzeroberfläche der Windows-Hilfe:

-   Weitere erkennbare Einstiegspunkte für die Hilfe von der primären Benutzeroberfläche (insbesondere neue Hilfelinks von Benutzeroberflächen wie Dialogfeldern, Fehlermeldungen und Assistenten). Hilfelinks führen Sie direkt zum entsprechenden Thema in der Hilfe.
-   Ein Symbol für die Hilfeschaltfläche ist in der oberen rechten Ecke der meisten Systemsteuerung Hubseiten sowie in Shellordnern verfügbar.
-   Benutzer können die aktuellsten Hilfeinhalte aus der Windows Online-Hilfe und dem -Support abrufen, wenn sie online sind.
-   Hilfethemen sind jetzt aufgabenbasiert und nicht featureorientiert, sodass Benutzer ihre Aufgaben schnell und effizient erledigen können.
-   Hilfethemen basieren jetzt größtenteils auf bekannten Szenarien mit den meisten Benutzern.
-   Hilfethemen weisen einen lockereren und [lockereren Ton auf,](text-style-tone.md)wobei die reale Sprache verwendet wird.
-   Hilfethemen sind für eine effektive Überprüfung konzipiert, da Benutzer den Inhalt nur selten wort für Wort lesen.

### <a name="an-analogy-for-help"></a>Eine Analogie zur Hilfe

Um ausführlicher über das Entwerfen Ihres Hilfesystems nachzudenken, sollten Sie eine Analogie aus dem täglichen Leben in Betracht ziehen. Sie gehen in einer unbekannten Stadt verloren. Was ist zu tun? Viele würden wie folgt reagieren:

-   Orientieren; Suchen Sie nach Sehenswürdigkeiten, Straßenzeichen (Namen und Zeiger auf Orte).
-   Suchen Sie nach Karten.
-   Fragen Sie abschließend als letzte Möglichkeit nach Wegbeschreibungen, oder rufen Sie einen Freund an.

Der Entwurf der "Schnittstelle" der Stadt wirkt sich auf Ihren Bedarf an Unterstützung aus. Gut beschriftete Straßen, explizite Wegbeschreibungen (Zeiger auf Krankenhause, Orte, Orte und Post) und klare Sehenswürdigkeiten wie prominente geografische Merkmale oder Gebäude helfen Ihnen dabei, ihren Weg zu finden.

Als letztes Mittel bitten Sie um Hilfe. Es ist ein Hinweis darauf, dass die "Schnittstelle" der Stadt fehlgeschlagen ist, da sie schlecht entworfen und verwirrend ist. Sie werden eher an einem Ort um Hilfe bitten, der über eine bestimmte Bezeichnung verfügt, die Hilfreichkeit andeutet. Beispielsweise bitten Sie eher an einem Ort mit den Bezeichnungen "Directions" oder "Information" um Hilfe als an einem allgemeinen Ort wie dem City Hall, auch wenn ihnen fast jeder im City Hall Anweisungen geben könnte.

Wenn Sie um Hilfe bitten, sind Sie wahrscheinlich frustriert und möchten nur zu Ihrem gewünschten Ziel gelangen. Sie sind wahrscheinlich nicht in der Stimmung, Zeit mit einer Tour durch die Stadt zu verbringen oder mehr über ihre Geschichte zu erfahren. Darüber hinaus hängt Ihre Motivation von der Wichtigkeit der Aufgabe ab. Wenn Sie versuchen, Ihr Zimmer zu finden, tun Sie alles, was sie benötigt. Wenn Ihr Ziel jedoch darin besteht, einen Ort mit geringfügiger Wichtigkeit zu finden, werden Sie wahrscheinlich nach einem geringen Aufwand einfach aufgeben.

All diese Aspekte der Suche im realen Raum entsprechen der Art und Weise, wie Benutzer sich in der Regel im virtuellen Bereich Ihres Programms befinden. Hilfe über die primäre Benutzeroberfläche hinaus zu suchen, ist von Natur aus destruktierend. Tun Sie Ihr Bestes, um eine solche Erfahrung zu verringern, indem Sie eine gut entworfene Benutzeroberfläche und intelligente "Straßenschilder" verwenden, um Benutzer auf die benötigten Antworten zu leiten.

### <a name="designing-ui-so-that-help-is-unnecessary"></a>Entwerfen der Benutzeroberfläche, sodass die Hilfe nicht erforderlich ist

Versuchen Sie, Hilfe von Anfang an unnötig zu machen, indem Sie Folgendes verwenden:

-   Einfaches Ermitteln und Ausführen gängiger Aufgaben.
-   Bereitstellen eindeutiger [Hauptanweisungen.](text-ui.md)
-   Bereitstellen von klaren, präzisen Steuerelementbezeichnungen, die ziel- und aufgabenorientiert sind.
-   Stellen Sie bei Bedarf zusätzliche Anweisungen und Erklärungen bereit.
-   Antiziping avoidable problems by using controls constrained to valid choices, providing suitable default values, handling all input formats, and preventing errors.
-   Schreiben von Fehlermeldungen, die eine klare Lösung oder Aktion für den Benutzer bereitstellen.
-   Vermeiden sie verwirrende Benutzeroberflächenentwürfe, z. B. Aufgaben mit schlechtem Flow oder die Verwendung von Steuerelementen, die aus keinem offensichtlichen Grund deaktiviert sind.
-   Arbeiten mit Writern und Editoren frühzeitig im Entwicklungszyklus, um qualitativ hochwertigen, konsistenten [Benutzeroberflächentext](text-ui.md) im gesamten Programm zu erstellen.

Benutzer sollten nicht an einen anderen Ort wechseln müssen, um herauszufinden, wie Sie Ihre Benutzeroberfläche verwenden. Fügen Sie wichtige Informationen direkt zur primären Benutzeroberfläche hinzu, anstatt Benutzer aus ihrem unmittelbaren Kontext und im Hilfebereich zu erzwingen. Wenn wichtige Informationen nur in einem Hilfethema vorhanden sind, besteht die Wahrscheinlichkeit, dass Benutzer sie nicht sehen. Informationen, die optional und erläuternder sind, finden Sie unter Hilfelinks von der primären Benutzeroberfläche zum entsprechenden Hilfethema.

### <a name="considering-user-motivation"></a>Berücksichtigen der Benutzermotivation

Für die meisten Benutzer gehören Geschwindigkeit und Effizienz zu den wichtigsten Vorteilen guter Programme. Benutzer möchten ihre Arbeit erledigen. Im Allgemeinen sind sie nicht daran interessiert, sich selbst über das Programm und die Technologie zu informieren. ihre Beeinträchtigung wird nur dadurch erweitert, dass dieses Programm ihren eigenen Interessen dient und probleme gelöst werden kann.

Entwerfen Sie Ihr Hilfesystem so, dass es der Motivation Ihrer Benutzer entspricht. Stellen Sie sich z. B. einen Benutzer vor, der sich an einem Kiosk in einem Kiosk befindet. Wenn sie nicht herausfinden kann, wie sie die Aufgabe schnell ausführen kann, wird sie wahrscheinlich einfach aufgeben und gehen. Es ist unwahrscheinlich, dass sie Zeit mit der Verwendung der Hilfe verbringen wird. Alternativ dazu hat ein hochmotivierter Benutzer eine höhere Toleranz für die Zeit, die für die Suche nach Antworten in Ihrem Hilfesystem aufgewendet wurde. Ein Geschäftsbenutzer, der z. B. die Bücher ausgleichen muss, ist wahrscheinlich bereit, Hilfeinhalte zu lesen, um diese neue Buchhaltungsanwendung optimal zu gestalten.

### <a name="writing-content-for-scanning"></a>Schreiben von Inhalten für die Überprüfung

Schreibhilfethemen, in denen sie wissen, dass sie auf bestimmte Informationen überprüft werden, nicht auf Wörter für Wörter lesen. Schreiben Sie präzise, gelangen Sie schnell auf den Punkt, und stellen Sie Informationen bereit, auf die Benutzer reagieren können.

-   Schreiben Sie Themen zur Vorgehensweise mit nummerierten Schritten in einem konsistenten Format, damit Benutzer erkennen, dass sie Prozedurunterstützung erhalten.
-   Schreiben Sie Referenzthemen mit Blick auf die einfache Überprüfung, indem Sie z. B. Tabellen verwenden, um Ui-Optionen oder Sprachsyntax darzustellen.
-   Schreiben Sie konzeptionelle Themen, die logisch nach Unterheadern organisiert sind, sodass der Benutzer ganze Abschnitte überspringen kann, die weniger interessant sind.

In allen Hilfeinhalten ist es einfacher, Aufzählungen zu überprüfen als standardmäßige Absatzblöcke von Text. Verwenden Sie Aufzählungszeichen jedoch mit Mäßigung, nicht als Krücke für unorganisiertes Material.

### <a name="creating-content-that-matters"></a>Erstellen von Inhalten, die wichtig sind

Da kein Hilfesystem jede Frage antizipieren kann, die jeder Benutzer möglicherweise hat, konzentrieren Sie sich den Großteil des Inhalts auf die Beantwortung der wichtigsten Fragen in den wichtigsten Szenarien für Ihre Zielbenutzer. Beispielsweise kann eine effektive Suche und das Einrichten der Netzwerkkonnektivität (neben anderen Aufgaben) sehr gefragte Themen sein. Konzentrieren Sie sich außerdem auf Aufgaben in Ihren Szenarien mit den wichtigsten Benutzern, anstatt ein Feature oder eine Technologie vollständig zu dokumentieren.

**Tipp:** Technischer Support ist eine gute Quelle für Hilfeinhalte. Helpdesks speichern häufig Datensätze mit häufig gestellten Fragen zu bestimmten Programmen oder Aufgaben, die Benutzer ausführen möchten (und die nicht erfolgreich sind).

Es ist nicht erforderlich, Hilfe für jedes Feature in der Benutzeroberfläche bereitzustellen. **Häufig führt die nicht hilfreiche Hilfe dazu, dass versucht wird, Hilfe für alles zu erstellen.** Wenn die Benutzeroberfläche gut entworfen ist, sind die meisten dieser Hilfethemen nicht sehr hilfreich. sie werden nur das Offensichtliche neu zugeben.

Wenn es mehrere Möglichkeiten gibt, eine Aufgabe auszuführen, können Sie in den meisten Fällen einfach die gängigste Methode dokumentieren, die von unerfahrenen Benutzern verwendet wird. Ausnahmen hierfür sind Überlegungen zur Barrierefreiheit (z. B. das Dokumentieren von Tastaturentsprechungen von Mausaktionen) und Plattformüberlegungen (z. B. das Dokumentieren des Tabletformfaktors oder für Serverumgebungen, in denen die Befehlszeile die grafische Benutzeroberfläche ersetzen kann).

Denken Sie daran, dass Benutzer häufig nicht genau so wie Sie an die Probleme denken, die auftreten. Beispielsweise kann es für Benutzer ungewöhnlich sein, sich selbst als "Konto" zu betrachten. Achten Sie darauf, ihre Such- und Indizierungsfunktionen zu entwerfen, um wahrscheinliche Terminologievarianten und Synonyme zu berücksichtigen.

Zwischen der primären Benutzeroberfläche und dem Hilfesystem sollten begriffe jedoch sehr ähnlich sein, wenn sie nicht identisch sind. Benutzer können verwechselt werden, wenn die Hilfesystemsprache nicht sehr eng mit dem korreliert, was auf dem Bildschirm angezeigt wird.

### <a name="writing-compelling-help-link-text"></a>Schreiben von überzeugenden Hilfelinktexten

Wenn Sie von Ihrer primären Benutzeroberfläche aus einen Link zu einem Hilfethema erstellen, müssen Sie überzeugenden Hilfelinktext schreiben. Eine klare und spezifische Sprache schafft Vertrauen. Benutzer sind tendenziell der Meinung, dass generische Hilfelinks (eine Schaltfläche mit dem Wort "Hilfe" oder "Weitere Informationen" dazu) ohne erhebliche Zeitaufwand nicht zu den richtigen Informationen führen.

**Wenn Sie nur fünf Dinge tun...**

1.  Entwerfen Sie Ihre Benutzeroberfläche so, dass Benutzer keine Hilfe benötigen.
2.  Machen Sie Ihre Hilfe hilfreich, indem Sie den Inhalt auf die wichtigsten Fragen in den wichtigsten Szenarien für Ihre Zielbenutzer konzentrieren.
3.  Zeigen Sie den Hilfeinhalt an, damit er leicht überprüft werden kann.
4.  Verstehen Sie, dass Sie nicht für jedes Feature auf der Benutzeroberfläche Hilfe bereitstellen müssen.
5.  Machen Sie die Einstiegspunkte der Hilfe erkennbar und überzeugend.

## <a name="usage-patterns"></a>Verwendungsmuster

Verschiedene Arten von Inhalten dienen unterschiedlichen Zwecken.



|    Inhaltstyp                                                                                                        |   Beispiel                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Prozedurale Hilfe**<br/> stellt die Schritte zum Ausführen einer Aufgabe bereit. <br/>                       | Die prozedurale Hilfe sollte sich auf "Wie"-Informationen und nicht auf "Was" oder "Warum" konzentrieren. <br/> ![Screenshot der Hilfeseite "Temporäre Dateien löschen" ](images/winenv-help-image2.png)<br/> In diesem Beispiel wird im Hilfethema beschrieben, wie Sie ein Feature des Hilfsprogramms für die Datenträgerbereinigung verwenden, indem Sie die Schritte nacheinander ausführen.<br/>                                              |
| **Konzeptionelle Hilfe**<br/> stellt Hintergrundinformationen, Featureübersichten oder Prozesse bereit. <br/> | Konzeptionelle Hilfe sollte darüber hinaus Informationen zu "Was" oder "Warum" bereitstellen, die für die Durchführung einer Aufgabe erforderlich sind. <br/> ![Screenshot der Hilfeseite "Desktop (Übersicht)" ](images/winenv-help-image3.png)<br/> In diesem Beispiel definiert das Hilfethema, was der Desktop ist, und bietet zusätzliche Details dazu, was er enthält und warum Benutzer damit interagieren.<br/>           |
| **Referenzhilfe**<br/> dient als Onlinereferenzbuch. <br/>                                | Sie können die Referenzhilfe verwenden, um eine Programmiersprache oder Programmierschnittstellen zu dokumentieren. <br/> ![Screenshot der Hilfeseite "Notational conventions" ](images/winenv-help-image4.png)<br/> In diesem Beispiel listet das Hilfethema typografische Konventionen auf, die für diese bestimmte Sprache oder Anwendung verwendet werden, und stellt die Informationen in einer einfach zu überprüfenden Tabelle bereit.<br/> |



 

## <a name="guidelines"></a>Richtlinien

### <a name="entry-points"></a>Einstiegspunkte

-   **Link zu bestimmten, relevanten Hilfethemen.** Verknüpfen Sie nicht mit der Hilfe-Startseite, dem Inhaltsverzeichnis, einer Liste von Suchergebnissen oder einer Seite, die nur mit anderen Seiten verknüpft ist. Vermeiden Sie das Verknüpfen mit Seiten, die als eine große Liste häufig gestellter Fragen strukturiert sind, da Benutzer dadurch gezwungen werden, nach der Seite zu suchen, die dem link entspricht, auf den sie geklickt haben. Verknüpfen Sie nicht mit bestimmten Hilfethemen, die für die jeweilige Aufgabe nicht relevant und hilfreich sind. Verknüpfen Sie niemals mit leeren Seiten.
-   **Stellen Sie aus Gründen der Konsistenz keine Hilfelinks in jedes Fenster oder jede Seite ein.** Wenn Sie einen Hilfelink an einem Ort bereitstellen, bedeutet dies nicht, dass Sie sie überall bereitstellen müssen.
-   **Verwenden Sie Hilfelinks für Dialogfelder, Fehlermeldungen, Assistenten und Eigenschaftenblätter.** Wenn der Hilfelink für bestimmte Steuerelemente gilt, platzieren Sie ihn linksbündig darunter. Wenn der Hilfelink für das gesamte Fenster gilt, platzieren Sie ihn in der unteren linken Ecke des Inhaltsbereichs des Fensters.

    ![Screenshot des Eigenschaftenblatts mit Gruppenfeld ](images/winenv-help-image5.png)

    In diesem Beispiel gilt der zweite Hilfelink für eine Gruppe von Steuerelementen.

    ![Screenshot des Eigenschaftenblatts und Hilfelinks ](images/winenv-help-image6.png)

    In diesem Beispiel gilt der Hilfelink für das gesamte Fenster.

-   **Verwenden Sie Nach möglichkeit Hilfelinks anstelle von generischen Textverweisen auf Help.**

    **Richtig:**

    Wie kann ich Datenträgerfehler reparieren?

    **Falsch:**

    Weitere Informationen zum Reparieren von Datenträgerfehlern finden Sie unter Hilfe und Support.

-   **Verwenden Sie eine Hilfeschaltfläche mit dem Hilfesymbol für die Hubseiten von Systemsteuerungselementen.** Platzieren Sie ihn in der oberen rechten Ecke. Diese Schaltflächen verfügen nicht über eine Bezeichnung, sondern über eine QuickInfo, die Hilfe liest.

    ![Screenshot des Systemsteuerungselements mit Hilfeschaltfläche ](images/winenv-help-image7.png)

    Ein Systemsteuerungselement mit einer Hilfeschaltfläche.

-   **Die F1-Hilfe ist optional.** Benutzer haben sich daran gewöhnt, Hilfeinformationen im Zusammenhang mit dem unmittelbaren Kontext der Benutzeroberfläche auf dem Bildschirm zu finden, indem sie die F1-Taste drücken, die auf Standardtastaturen als Hilfe bezeichnet wird. Sie können die F1-Hilfe einschließen, wenn z. B. Benutzerfreundlichkeitsstudien zeigen, dass Ihre Benutzer sie erwarten, oder ihre Programmoberfläche komplex genug ist, um von kontextabhängiger Unterstützung zu profitieren.
-   **Programme mit Menüleisten können über eine Menükategorie Hilfe verfügen.** Richtlinien für Hilfemenüs finden Sie unter [Menüs](cmd-menus.md).

    ![Screenshot der Hilfe, auf die über die Menüleiste zugegriffen wird ](images/winenv-help-image8.png)

    In diesem Beispiel verfügt das Windows Paint-Zubehör über eine Menükategorie Hilfe.

-   **Geben Sie für die Barrierefreiheit der Tastatur Tabstopps für Hilfeschaltflächen und Links an.**
-   Hilfeschaltfläche und Linkverhalten sollten wie folgt aussehen: Der Hilfebereich wird geöffnet, und es wird ein dediziertes Hilfethema angezeigt. Die Benutzeroberfläche, die den Hilfebereich aufgerufen hat, sollte geöffnet bleiben, um die Kontexterfahrung beizubehalten.
-   **Verwenden Sie nicht die folgenden veralteten Hilfeeinstiegspunktstile: "Weitere Informationen" oder "Weitere Informationen..." Links, generische Hilfeschaltflächen und kontextbezogene Hilfeschaltflächen auf der Titelleiste.** Obwohl sie in der Vergangenheit verwendet wurden, haben Benutzerfreundlichkeitsstudien festgestellt, dass Benutzer sie tendenziell ignorieren. Verwenden Sie stattdessen Links zu bestimmten Hilfethemen. Richtlinien zum Schreiben guter Hilfelinks finden Sie unter [Hilfelinks.](#text)

    **Falsch:**

    ![Screenshot des Dialogfelds mit dem Link "Weitere Informationen" ](images/winenv-help-image9.png)

    Verwenden Sie nicht "Weitere Informationen" oder "Weitere Informationen..." Links.

    **Falsch:**

    ![Screenshot der Hilfeschaltfläche neben Commitschaltflächen ](images/winenv-help-image10.png)

    Verwenden Sie keine generischen Hilfeschaltflächen.

    **Falsch:**

    ![Screenshot des Fragezeichensymbols auf der Titelleiste ](images/winenv-help-image11.png)

    Verwenden Sie keine kontextbezogenen Hilfeschaltflächen auf der Titelleiste.

### <a name="content"></a>Inhalt

-   **Erstellen Sie keine offensichtlichen Inhalte.** Hilfethemen, die wiederholen, was sich auf der primären Benutzeroberfläche befindet, haben keinen Mehrwert.
-   **Erstellen Sie keine Inhalte, auf die der Benutzer nicht reagieren kann.**
    -   **Ausnahme:** Einige konzeptionelle Inhalte liefern wichtige Hintergrundinformationen, ohne dass dies notwendigerweise zu Benutzeraktionen führt.
-   **Vermeiden Sie ungenaue Lösungen für Probleme.** "Wenden Sie sich beispielsweise an Ihren Systemadministrator", oder "Installieren Sie die Anwendung neu", um Benutzer zu frustrieren.
    -   **Ausnahme:** Es wird empfohlen, sich an den Systemadministrator zu wenden, wenn dies die einzige praktische Lösung ist, und systemadministratoren erwarten, dass sie für das Problem kontaktiert werden.
-   **Vermeiden Sie Inhalte, die sehr unwahrscheinliche Benutzerszenarien behandeln.** Entwickeln Sie Ihre wichtigsten Hilfeinhalte für das, was Sie als normaler Gebrauch erwarten. Beachten Sie wichtige Ausnahmen von der erwarteten Verwendung, behandeln Sie diesen Inhalt jedoch mit einer niedrigeren Priorität.
-   **Sammeln Sie Feedback von Ihren Benutzern, wie hilfreich Ihre Hilfethemen sind.** Benutzern das Bewerten einzelner Themen ermöglichen. Führen Sie [Usability-Studien](glossary.md) zu Ihrer Dokumentation durch, um Probleme im Zusammenhang mit der Qualität und Auffindbarkeit von Inhalten zu ermitteln.
    -   **Tipp:** Benutzerfeedback ist auch eine hervorragende Möglichkeit, mehr aufgabenbasierte Inhalte zu generieren, die sich darauf konzentrieren, was Benutzer tatsächlich mit Ihrem Programm tun, im Gegensatz zu featurebasierten Inhalten, die sich einfach auf eine Beschreibung der Technologie konzentrieren.
-   **Stellen Sie mehrere Möglichkeiten für den Zugriff auf Ihre Inhalte zur Verfügung.** Ein Inhaltsverzeichnis, ein Index [](ctrl-search-boxes.md) und ein Suchmechanismus sind drei der gängigsten Methoden zur Verbesserung der Aufsuchbarkeit.
-   **Wenn es mehr als eine Möglichkeit gibt, eine Aufgabe auszuführen, können Sie in den meisten Fällen nur die gängigste Methode dokumentieren, die von unerfahrenen Benutzern verwendet wird.**

### <a name="icons"></a>Symbole

-   Verwenden Sie das Hilfesymbol nur für Explorer-Fenster und die Hubseiten von Systemsteuerungselementen. Verwenden Sie nicht das Hilfesymbol mit Hilfelinks.

**Richtig:**

![Screenshot des Fensters mit Fragezeichensymbol ](images/winenv-help-image12.png)

In diesem Beispiel verwendet ein Windows-Explorer ein Hilfesymbol, um Zugriff auf die Hilfe zu ermöglichen.

**Falsch:**

![Screenshot des Fensters mit Hilfesymbol im linken Bereich ](images/winenv-help-image13.png)

In diesem Beispiel wird das Hilfesymbol links unten falsch mit einem Hilfelink verwendet.

## <a name="text"></a>Text

**Hilfelinks**

-   Geben Sie spezifische Informationen zum Inhalt des Hilfethemas an, indem Sie so viel relevanten, präzisen Text wie nötig verwenden. Benutzer ignorieren häufig generische Hilfelinks. Stellen Sie sicher, dass die Ergebnisse des Links vorhersagbar sind. Benutzer sollten nicht von den Ergebnissen überraschend sein.

    -   **Ausnahme:** Sie können "Weitere Informationen" verwenden, um Anweisungen zu ergänzen, die sich direkt auf der Benutzeroberfläche befinden. Dies gilt insbesondere, wenn die Angabe bestimmter Informationen im Hilfelink zu unnötiger Wiederholung führt oder den Link weniger überzeugend macht.

    **Falsch:**

    Ein starkes Kennwort enthält mindestens sechs Buchstaben, Zahlen und Symbole in gemischter Groß-/Kleinbuchstaben. Was ist ein starkes Kennwort?

    **Richtig:**

    Ein starkes Kennwort enthält mindestens sechs Buchstaben, Zahlen und Symbole in gemischter Groß-/Kleinbuchstaben. Weitere Informationen

    Im falschen Beispiel wiederholt sich der Link Hilfe. Sie stellt eine Frage, die tatsächlich bereits beantwortet wurde.

-   Geben Sie nach Möglichkeit Hilfelinktext in Bezug auf die primäre Frage ein, die vom Hilfeinhalt beantwortet wird. Verwenden Sie nicht den Ausdruck "Weitere Informationen", "Weitere Informationen" oder "Hilfe zu diesem Thema erhalten".

    **Falsch:**

    Weitere Informationen zum Hinzufügen von Ausnahmen

    **Richtig:**

    Welche Risiken bestehen beim Zulassen von Ausnahmen?

    Gewusst wie Ausnahmen hinzufügen?

    In den richtigen Beispielen wird der Link in Bezug auf die primäre Frage, die vom Hilfethema beantwortet wird, formuliert.

-   Wenn die relevantesten Informationen kurz zusammengefasst werden können, legen Sie die Zusammenfassung direkt auf der Benutzeroberfläche ab, anstatt einen Hilfelink zu verwenden. Sie können jedoch einen Hilfelink verwenden, um zusätzliche Informationen zur Verfügung zu stellen.

    **Falsch:**

    ![Screenshot des Links zu einem starken Kennwort? ](images/winenv-help-image14.png)

    **Richtig:**

    ![Screenshot mit ergänzendem Text zu Kennwörtern ](images/winenv-help-image15.png)

    **Besser:**

    ![Screenshot von Text mit Link zu mehr Informationen ](images/winenv-help-image16.png)

    Im richtigen Beispiel werden die Hilfeinformationen kurz zusammengefasst, was die Wahrscheinlichkeit, dass Benutzer sie lesen, stark verbessert. Das bessere Beispiel enthält einen Hilfelink, um weitere Informationen zu diesem komplexen Thema zu erhalten.

-   Hilfelinks zu Ausdrücken, um die Unterstützung eindeutig anzugeben. Hilfelinks sollten nie wie Aktionslinks aussehen.
-   Verwenden Sie den gesamten Hilfelink für den Linktext, nicht nur die Schlüsselwörter.

    **Richtig:**

    Welche Risiken bestehen beim Zulassen von Ausnahmen?

    **Falsch:**

    Welche Risiken bestehen beim Zulassen von Ausnahmen?

    Im richtigen Beispiel wird der gesamte Hilfelinksatz für den Linktext verwendet.

    -   **Ausnahme:** Hilfelinks zu externen Websites sollten einfach den Namen der Website oder Seite als Link verwenden. Text, der den Namen der Website einfing, muss nicht in den Link selbst aufgenommen werden.

-   Hilfelinks müssen nicht genau mit den Überschriften des Hilfethemas übereinstimmen, aber es sollte eine starke und offensichtliche Verbindung zwischen den beiden seiten geben. Entwerfen Sie aus diesem Grund Links und Überschriften paarweise.

    **Richtig:**

    Wie kann ich die Leistung dieses Features verbessern? (Linktext)

    Konfigurieren dieses Features für optimale Leistung (Themenüberschrift)

    **Falsch:**

    Wie kann ich die Leistung dieses Features verbessern? (Linktext)

    Vollständige Übersicht über dieses Feature (Themenüberschrift)

    Im falschen Beispiel unterscheidet sich die Überschrift des Hilfethemas erheblich vom Bereich des Hilfelinktexts und kann versiert sein.

-   Wenn der Hilfeinhalt online ist, machen Sie dies im Linktext deutlich. Dies trägt dazu bei, das Ergebnis der Links vorhersagbar zu machen.

    **Richtig:**

    Weitere Formate und Tools finden Sie auf der Microsoft-Website.

    **Falsch:**

    Wo finde ich zusätzliche Formate und Tools?

-   Verwenden Sie vollständige Sätze.
-   Verwenden Sie mit Ausnahme von Fragezeichen keine endende Interpunktion.
-   Verwenden Sie keine Ausellipsen für Hilfelinks oder Befehle.

**Hilfeinhalt**

-   Formatieren Sie Benutzeroberflächenelemente fett, um sie leicht zu identifizieren. Dies ist besonders nützlich für Hilfethemen mit Prozeduren, die es Benutzern ermöglichen, Prozeduren zu durchsuchen und relevante Benutzeroberflächenelemente schnell anzuzeigen.
-   Formatieren von Untertiteln mithilfe von italisch. Dies gilt für Tabellen, Grafiken, Screenshots und andere grafische Elemente, die von einer kurzen Texterklärung profitieren.
-   Unter Hilfe finden Sie einfach Hilfe. Verwenden Sie im Allgemeinen nicht den Ausdruck Onlinehilfe, es sei denn, Sie verweisen tatsächlich auf Inhalte auf Ihrer Website.

 

