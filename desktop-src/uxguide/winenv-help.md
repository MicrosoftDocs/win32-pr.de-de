---
title: Hilfe
description: Verwenden Sie Hilfe als sekundären Mechanismus, um Benutzern zu helfen, Aufgaben \8212 auszuführen und besser zu verstehen. Der primäre Mechanismus ist die Benutzeroberfläche selbst. Wenden Sie diese Richtlinien an, damit der Inhalt wirklich hilfreich und leicht zu finden ist.
ms.assetid: 82ce076e-062b-4793-a1c0-ed96c0f2b284
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2a71abf4b90aeaf19f43997c5d8e98ad42f56d5daa86699ff8504ca5a3080bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935789"
---
# <a name="help"></a>Hilfe

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Verwenden Sie Hilfe als sekundären Mechanismus, um Benutzern zu helfen, Aufgaben auszuführen und besser zu verstehen. Der primäre Mechanismus ist die Benutzeroberfläche selbst. Wenden Sie diese Richtlinien an, damit der Inhalt wirklich hilfreich und leicht zu finden ist.

Ein Hilfesystem besteht aus verschiedenen Inhaltstypen, die Benutzern helfen sollen, wenn sie eine Aufgabe nicht abschließen können, ein Konzept ausführlicher verstehen möchten oder mehr technische Details benötigen, als auf der Benutzeroberfläche verfügbar sind.

In diesem Artikel wird Hilfe als sekundäre Benutzeroberfläche bezeichnet. Die Benutzeroberfläche ist primär, da Benutzer dort zum ersten Mal versuchen, ihre Probleme zu lösen. Sie wenden sich nur dann an das Hilfesystem, wenn sie ihre Aufgabe mit der Benutzeroberfläche nicht ausführen können.

![Screenshot der Windows-Hilfe- und -Supportseite ](images/winenv-help-image1.png)

Die Windows-Startseite für Hilfe und Support, die im Startmenü.

**Hinweis:** Richtlinien im Zusammenhang [mit Stil und Ton sind](text-style-tone.md) in einem separaten Artikel dargestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Wie motiviert sind Ihre Zielbenutzer?** Mit zunehmender Motivation sind sie dazu da, die Funktionalität Ihres Programms zu entdecken und fortgeschrittene oder sogar fortgeschrittene Benutzer zu werden, desto mehr sind sie bereit, antworten zu können, indem sie Hilfethemen lesen.
-   **Verwenden Sie die Hilfe, um eine fehlerhafte Benutzeroberfläche zu beheben?** Desto besser Ihre Benutzeroberfläche, desto weniger Benutzer werden zusätzliche Hilfe benötigen. Wenn Ihr Programm über eine sehr klare, hilfreiche primäre Benutzeroberfläche verfügt (z. B. jargonfreie Fehlermeldungen, gut geschriebene Assistenten und eindeutige Dialogfelder), benötigen Sie möglicherweise überhaupt kein sekundäres Hilfesystem.
-   **Ist Ihr Programm relativ einfach?** Falls ja, sollten Sie alle erforderlichen Unterstützungsinhalte in Ihre primären Benutzeroberflächenoberflächen integrieren. Benutzer suchen eher zusätzliche Hilfe in Programmen, die komplexe Aufgaben ausführen.
-   **Ist Ihre Anwendung für Entwickler, IT-Experten oder andere Softwareexperten vorgesehen?** Diese Benutzer erwarten in der Regel referenzbasierte Hilfe zu Programmiersprachenkonventionen und eine ausführliche konzeptionelle Hilfe zur Vererbung von Features.

## <a name="design-concepts"></a>Entwurfskonzepte

Wenn Sie die Hilfe in Ihr Programm integrieren möchten, integrieren Sie sie in Ihren gesamter Entwurf. Die Hilfeschnittstelle sollte einfach, effizient und relevant sein. Sie sollte es Benutzern ermöglichen, einfach Hilfe zu erhalten und dann zu ihrer Aufgabe zurückzukehren. Stellen Sie sich Ihr Hilfesystem in Bezug auf die Zeit der Benutzer vor: Minimieren Sie die Unterbrechung zunächst, indem Sie sich überlegen, wo probleme in Ihrem Programm auftreten. Lösen Sie diese Probleme dann, indem Sie grundlegende Unterstützung direkt in Ihre Benutzeroberfläche integrieren und klare und konsistente Einstiegspunkte in Ihre ausführlichere Hilfe erstellen.

Windows Unterstützung wurde gemäß diesen Prinzipien entworfen. Hier sind einige der Entwurfsänderungen an der Benutzeroberfläche Windows Hilfe:

-   Besser erkennbare Einstiegspunkte für Hilfe über die primäre Benutzeroberfläche (insbesondere neue Hilfelinks von Benutzeroberflächenoberflächen wie Dialogfeldern, Fehlermeldungen und Assistenten). Über Hilfelinks werden Sie direkt zum entsprechenden Thema in der Hilfe weiterverlässigt.
-   Ein Hilfeschaltflächensymbol ist in der oberen rechten Ecke der meisten hub Systemsteuerung seiten sowie shell-Ordner verfügbar.
-   Benutzer können auswählen, ob sie die neuesten Hilfeinhalte aus Windows Onlinehilfe und -support erhalten möchten, wenn sie online sind.
-   Hilfethemen sind jetzt aufgaben- und nicht featureorientiert, sodass Benutzer ihre Aufgaben schnell und effizient ausführen können.
-   Hilfethemen basieren jetzt größtenteils auf bekannten Szenarien mit den meisten Benutzer.
-   Hilfethemen haben einen lockereren und [lockereren Ton,](text-style-tone.md)der die reale Sprache verwendet.
-   Hilfethemen sind für effektive Überprüfungen konzipiert, da Benutzer den Inhalt nur selten wort für Wort lesen.

### <a name="an-analogy-for-help"></a>Eine Analogie für Hilfe

Um sich eingehender gedanken über das Entwerfen Ihres Hilfesystems zu machen, ziehen Sie eine Analogie zum alltäglichen Leben in Betracht. Sie gehen in einer unbekannten Stadt verloren. Was ist zu tun? Viele würden wie dies reagieren:

-   Get oriented; Suchen Sie nach Sehenswürdigkeiten, Straßenschildern (Namen und Zeiger auf Orte).
-   Suchen Sie nach Karten.
-   Fragen Sie schließlich als letztes Mittel nach einer Wegbeschreibung, oder rufen Sie einen Freund an.

Der Entwurf der "Schnittstelle" der Stadt wirkt sich auf Ihre Unterstützung aus. Gut beschriftete Straßen, explizite Wegbeschreibungen (Zeiger auf Krankenhaus, Gebiet, Gebiet und Post) und klare Sehenswürdigkeiten wie prominente geografische Merkmale oder Gebäude helfen Ihnen dabei, ihren Weg zu finden.

Als letztes Mittel bitten Sie um Hilfe. Dies ist ein Hinweis darauf, dass die "Schnittstelle" der Stadt fehlgeschlagen ist, da sie schlecht entworfen und verwirrend ist. Sie werden eher an einem Ort um Hilfe bitten, der über eine bestimmte Bezeichnung verfügt, die hilfreich ist. Beispielsweise fragen Sie eher an einem Ort mit der Bezeichnung "Directions" oder "Information" um Hilfe als an einem allgemeinen Ort wie dem City Hall, auch wenn ihnen in der City Hall nur von ungefähr jemand eine Wegbeschreibung geben könnte.

Wenn Sie um Hilfe bitten, sind Sie wahrscheinlich frustriert und möchten nur zu Ihrem vorgesehenen Ziel gelangen. Sie sind wahrscheinlich nicht in der Laune, zeitauf die Stadt zu erkunden oder mehr über ihre Geschichte zu erfahren. Darüber hinaus hängt Ihre Motivation von der Wichtigkeit der Aufgabe ab. Wenn Sie versuchen, Ihr Zimmer zu finden, werden Sie alles tun, was es benötigt. Wenn Ihr Ziel jedoch ist, einen Ort von geringfügiger Wichtigkeit zu finden, werden Sie wahrscheinlich nur nach einem geringen Aufwand aufgeben.

All diese Aspekte der Suche im realen Raum entsprechen der Art und Weise, wie Benutzer in der Regel ihren Weg im virtuellen Bereich Ihres Programms finden. Die Suche nach Hilfe über die primäre Benutzeroberfläche hinaus ist von Natur aus desordnend; Tun Sie Ihr Bestes, um eine solche Benutzeroberfläche durch eine gut entworfene Benutzeroberfläche und intelligente "Straßenschilder" zu entschärfen, um Benutzer auf die antworten zu lassen, die sie benötigen.

### <a name="designing-ui-so-that-help-is-unnecessary"></a>Entwerfen der Benutzeroberfläche, sodass Hilfe nicht erforderlich ist

Versuchen Sie, Hilfe von anfang an überflüssig zu machen, indem Sie:

-   Einfaches Aufarbeiten und Ausführen gängiger Aufgaben.
-   Bereitstellen eindeutiger [Hauptanweisungen.](text-ui.md)
-   Bereitstellen von klaren, präzisen Steuerelementbezeichnungen, die ziel- und aufgabenorientiert sind.
-   Bei Bedarf zusätzliche Anweisungen und Erläuterungen.
-   Antizipieren von vermeidbaren Problemen mithilfe von Steuerelementen, die auf gültige Auswahlmöglichkeiten beschränkt sind, Bereitstellen geeigneter Standardwerte, Behandeln aller Eingabeformate und Verhindern von Fehlern.
-   Schreiben von Fehlermeldungen, die eine klare Lösung oder Aktion für den Benutzer bereitstellen.
-   Vermeiden verwirrender Ui-Entwürfe, z. B. Aufgaben mit schlechtem Fluss oder Verwendung von Steuerelementen, die ohne ersichtlichen Grund deaktiviert sind.
-   Arbeiten sie frühzeitig im Entwicklungszyklus mit Writern und Editoren zusammen, um qualitativ hochwertigen, konsistenten Benutzeroberflächentext im [gesamten](text-ui.md) Programm zu erstellen.

Benutzer sollten nicht an eine andere Stelle wechseln müssen, um herauszufinden, wie Sie Ihre Benutzeroberfläche verwenden. Fügen Sie wichtige Informationen direkt in die primäre Benutzeroberfläche ein, anstatt Benutzer aus ihrem unmittelbaren Kontext heraus und in den Hilfebereich zu zwingen. Wenn wichtige Informationen nur in einem Hilfethema vorhanden sind, ist die Wahrscheinlichkeit gut, dass Benutzer sie nicht sehen. Informationen, die optional und erläuternder sind, finden Sie unter Hilfelinks von der primären Benutzeroberfläche zum relevanten Hilfethema, um zusätzliche Unterstützung zu erhalten.

### <a name="considering-user-motivation"></a>Berücksichtigen der Benutzermotivation

Für die meisten Benutzer gehören Geschwindigkeit und Effizienz zu den wichtigsten Vorteilen guter Programme. Benutzer möchten ihre Arbeit erledigen. Im Allgemeinen sind sie nicht daran interessiert, sich selbst über das Programm und die Technologie zu erfahren. Ihre Geduld wird nur dadurch erweitert, dass dieses Programm ihren eigenen Interessen dient und die jeweiligen Probleme löst.

Entwerfen Sie Ihr Hilfesystem so, dass es den Beweggründen Ihrer Benutzer passt. Stellen Sie sich z. B. einen Benutzer vor, der an einem Kiosk einen Kiosk gekauft hat. Wenn sie nicht herausfinden kann, wie sie die Aufgabe schnell ausführen kann, wird sie wahrscheinlich einfach auf die Arbeit gehen. Es ist unwahrscheinlich, dass sie Zeit mit der Verwendung der Hilfe verbringt. Alternativ dazu hat ein hoch motivierter Benutzer eine höhere Toleranz für die Zeit, die er damit verbracht hat, Ihr Hilfesystem nach Antworten zu recherchieren. Ein Geschäftsbenutzer, der z. B. die Bücher ausgleichen muss, ist wahrscheinlich bereit, Hilfeinhalte zu rate zu ziehen, um die neue Buchhaltungsanwendung am besten zu verwenden.

### <a name="writing-content-for-scanning"></a>Schreiben von Inhalt für die Überprüfung

Schreiben Sie Hilfethemen in dem Wissen, dass sie auf bestimmte Informationen überprüft werden, nicht auf Word-for-Word.) Schreiben Sie präzise, kommen Sie schnell auf den Punkt, und stellen Sie Informationen zur Verfügung, auf die Benutzer reagieren können.

-   Schreiben Sie "Schritt-für-Schritt"-Themen mit nummerierten Schritten in einem konsistenten Format, damit Benutzer erkennen können, dass sie prozedurale Unterstützung erhalten.
-   Schreiben Sie Referenzthemen mit Blick auf die Einfache Überprüfung, indem Sie Tabellen verwenden, um z. B. Ui-Optionen oder Sprachsyntax zu präsentieren.
-   Schreiben Sie konzeptionelle Themen, die logisch nach Unterüberungen organisiert sind, damit der Benutzer ganze Abschnitte überspringen kann, die weniger interessant sind.

In allen Hilfeinhalten ist es einfacher, Aufzählungen zu scannen als standardmäßige Absatzblöcke von Text; Verwenden Sie Aufzählungen jedoch mit Umsicht, nicht als Crutch für unorganisiertes Material.

### <a name="creating-content-that-matters"></a>Erstellen von Inhalten, die wichtig sind

Da kein Hilfesystem jede Frage, die jeder Benutzer haben könnte, vorhersehen kann, konzentrieren Sie sich den Großteil des Inhalts auf die Beantwortung der wichtigsten Fragen in den wichtigsten Szenarien für Ihre Zielbenutzer. Eine effektive Suche und die Einrichtung von Netzwerkkonnektivität (u.a. aufgaben) sind beispielsweise sehr gefragte Themen. Konzentrieren Sie sich auch auf Aufgaben in Ihren Top-Benutzerszenarien, anstatt ein Feature oder eine Technologie vollständig zu dokumentieren.

**Tipp:** Der technische Support ist eine gute Quelle für Hilfeinhalte. Helpdesks führen häufig Aufzeichnungen häufig gestellter Fragen zu bestimmten Programmen oder Aufgaben, die Benutzer versuchen (und fehlschlagen) zu erreichen.

Es ist nicht erforderlich, Für jedes Feature auf der Benutzeroberfläche Hilfe zu bieten. **Häufig ergibt sich eine nicht hilfreiche Hilfe aus dem Versuch, Hilfe für alles zu erstellen.** Wenn die Benutzeroberfläche gut entworfen ist, sind die meisten dieser Hilfethemen nicht sehr hilfreich. sie werden lediglich das Offensichtliche neu aufs neue worden sein.

Wenn es mehr als eine Möglichkeit gibt, eine Aufgabe auszuführen, können Sie in den meisten Fällen nur die gängigste Methode dokumentieren, die von unerfahrenen Benutzern verwendet wird. Ausnahmen hierfür sind Überlegungen zur Barrierefreiheit (z. B. Dokumentieren von Tastaturentsprechungen von Mausaktionen) und Überlegungen zur Plattform (z. B. für den Formfaktor des Tablets oder für Serverumgebungen, in denen die Befehlszeile die grafische Benutzeroberfläche ersetzen kann).

Denken Sie daran, dass benutzer sich die Probleme, auf die sie stoßen, häufig nicht in genau denselben Begriffen wie Sie denken. Beispielsweise kann es für Benutzer ungewöhnlich sein, sich selbst als "Konto" zu sehen. Achten Sie darauf, dass Sie Ihre Such- und Indizierungsfunktionen entwerfen, um wahrscheinliche Terminologievarianten und Synonyme zu berücksichtigen.

Zwischen der primären Benutzeroberfläche und dem Hilfesystem sollten die Begriffe jedoch sehr ähnlich sein, wenn sie nicht identisch sind. Benutzer können verwirrend sein, wenn die Hilfesystemsprache nicht sehr eng mit dem korreliert, was sie auf dem Bildschirm sehen.

### <a name="writing-compelling-help-link-text"></a>Schreiben von überzeugenden Hilfelinktexten

Wenn Sie über Ihre primäre Benutzeroberfläche einen Link zu einem Hilfethema erstellen, müssen Sie überzeugenden Text für den Hilfelink schreiben. Eine klare und spezifische Sprache gibt Vertrauen. Benutzer neigen dazu, zu glauben, dass generische Hilfelinks (eine Schaltfläche mit dem Wort "Hilfe" oder "Weitere Informationen") ohne einen erheblichen Zeitdruck nicht zu den richtigen Informationen führen.

**Wenn Sie nur fünf Dinge tun...**

1.  Entwerfen Sie Ihre Benutzeroberfläche so, dass Benutzer keine Hilfe benötigen.
2.  Machen Sie Ihre Hilfe hilfreich, indem Sie sich auf die wichtigsten Fragen in den wichtigsten Szenarien für Ihre Zielbenutzer konzentrieren.
3.  Stellen Sie den Hilfeinhalt vor, damit er leicht gescannt werden kann.
4.  Verstehen Sie, dass Sie nicht für jedes Feature auf der Benutzeroberfläche Hilfe bereitstellen müssen.
5.  Machen Sie die Einstiegspunkte der Hilfe erkennbar und überzeugend.

## <a name="usage-patterns"></a>Verwendungsmuster

Unterschiedliche Arten von Inhalten dienen unterschiedlichen Zwecken.



|    Inhaltstyp                                                                                                        |   Beispiel                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Prozedurale Hilfe**<br/> enthält die Schritte zum Ausführen einer Aufgabe. <br/>                       | Bei der prozeduralen Hilfe sollte der Fokus auf "Wie"-Informationen und nicht auf "Was" oder "Warum" stehen. <br/> ![Screenshot der Hilfeseite "Temporäre Dateien löschen" ](images/winenv-help-image2.png)<br/> In diesem Beispiel wird im Hilfethema beschrieben, wie sie ein Feature des Hilfsprogramms Datenträgerbereinigung verwenden und die schritte nacheinander ausführen.<br/>                                              |
| **Konzeptionelle Hilfe**<br/> stellt Hintergrundinformationen, Funktionsübersichten oder Prozesse zur Verfügung. <br/> | Konzeptionelle Hilfe sollte "Was"- oder "Warum"-Informationen darüber hinaus bereitstellen, die zum Abschließen einer Aufgabe erforderlich sind. <br/> ![Screenshot der Hilfeseite "Desktop (Übersicht)" ](images/winenv-help-image3.png)<br/> In diesem Beispiel definiert das Hilfethema, was der Desktop ist, und enthält zusätzliche Details darüber, was er enthält und warum Benutzer damit interagieren.<br/>           |
| **Referenzhilfe**<br/> dient als Onlinereferenzbuch. <br/>                                | Sie können die Referenzhilfe verwenden, um eine Programmiersprache oder Programmierschnittstellen zu dokumentieren. <br/> ![Screenshot der Hilfeseite "Notational conventions" (Notationale Konventionen) ](images/winenv-help-image4.png)<br/> In diesem Beispiel listet das Hilfethema typografische Konventionen auf, die für diese bestimmte Sprache oder Anwendung verwendet werden, und stellt die Informationen in einer einfach zu scannenden Tabelle zur Verfügung.<br/> |



 

## <a name="guidelines"></a>Richtlinien

### <a name="entry-points"></a>Einstiegspunkte

-   **Link zu bestimmten relevanten Hilfethemen.** Verknüpfen Sie nicht die Startseite der Hilfe, das Inhaltsverzeichnis, eine Liste mit Suchergebnissen oder eine Seite, die nur mit anderen Seiten verknüpft ist. Vermeiden Sie das Verknüpfen mit Seiten, die als eine große Liste häufig gestellter Fragen strukturiert sind, da benutzer dazu zwingt, nach der Seite zu suchen, die dem link entspricht, auf den sie geklickt haben. Verknüpfen Sie nicht mit bestimmten Hilfethemen, die für die jeweilige Aufgabe nicht relevant und hilfreich sind. Verlinken Sie niemals mit leeren Seiten.
-   **Stellen Sie aus Gründen der Konsistenz nicht in jedem Fenster oder jeder Seite Hilfelinks.** Das Bereitstellen eines Hilfelinks an einem Ort bedeutet nicht, dass Sie sie überall bereitstellen müssen.
-   **Verwenden Sie Hilfelinks für Dialogfelder, Fehlermeldungen, Assistenten und Eigenschaftenblätter.** Wenn der Hilfelink für bestimmte Steuerelemente gilt, platzieren Sie ihn unter diesen linksbündig. Wenn der Hilfelink für das gesamte Fenster gilt, platzieren Sie ihn in der unteren linken Ecke des Inhaltsbereichs des Fensters.

    ![Screenshot des Eigenschaftenblatts mit Gruppenfeld ](images/winenv-help-image5.png)

    In diesem Beispiel gilt der zweite Hilfelink für eine Gruppe von Steuerelementen.

    ![Screenshot des Eigenschaftenblatts und des Hilfelinks ](images/winenv-help-image6.png)

    In diesem Beispiel gilt der Link Hilfe für das gesamte Fenster.

-   **Verwenden Sie Hilfelinks anstelle generischer Textverweise, um Hilfe zu erhalten, wenn dies technisch möglich ist.**

    **Richtig:**

    Wie kann ich Datenträgerfehler reparieren?

    **Falsch:**

    Weitere Informationen zum Reparieren von Datenträgerfehlern finden Sie unter Hilfe und Support.

-   **Verwenden Sie eine Hilfeschaltfläche mit dem Hilfesymbol für die Hubseiten von Systemsteuerungselementen.** Platzieren Sie es in der oberen rechten Ecke. Diese Schaltflächen verfügen nicht über eine Bezeichnung, sondern über eine QuickInfo, die Hilfe liest.

    ![Screenshot des Systemsteuerungselements mit Der Hilfeschaltfläche ](images/winenv-help-image7.png)

    Ein Systemsteuerungselement mit einer Schaltfläche "Hilfe".

-   **Die F1-Hilfe ist optional.** Benutzer haben sich daran gewöhnt, Hilfeinformationen zu finden, die sich auf den unmittelbaren Kontext der Benutzeroberfläche auf dem Bildschirm bezieht, indem sie die F1-Taste drücken, die auf Standardtastaturen als Hilfe bezeichnet wird. Sie können die F1-Hilfe verwenden, wenn z. B. Benutzerfreundlichkeitsstudien zeigen, dass Ihre Benutzer es erwarten, oder ihre Programmbenutzeroberfläche komplex genug ist, um von kontextbezogener Unterstützung zu profitieren.
-   **Programme mit Menüleisten können eine Menükategorie Hilfe haben.** Hilfemenürichtlinien finden Sie unter [Menüs](cmd-menus.md).

    ![Screenshot der Hilfe, auf die über die Menüleiste zugegriffen wird ](images/winenv-help-image8.png)

    In diesem Beispiel verfügt das Windows Paint-Accessory über eine Menükategorie Hilfe.

-   **Geben Sie für die Tastaturzugriffseingabe Tabstopps für Hilfeschaltflächen und Links an.**
-   Das Verhalten der Schaltfläche "Hilfe" und des Links sollte wie folgt lauten: Der Hilfebereich wird geöffnet, und ein dediziertes Hilfethema wird angezeigt. Die Benutzeroberfläche, die den Hilfebereich aufgerufen hat, sollte geöffnet bleiben, um die kontextbezogene Benutzeroberfläche zu erhalten.
-   **Verwenden Sie nicht die folgenden veralteten Stile für Hilfeeinstiegspunkt: "Weitere Informationen" oder "Weitere Informationen..." Links, generische Hilfeschaltflächen und kontextsensible Hilfeschaltflächen auf der Titelleiste.** Obwohl sie in der Vergangenheit verwendet wurden, haben Benutzerfreundlichkeitsstudien festgestellt, dass Benutzer sie tendenziell ignorieren. Verwenden Sie stattdessen Links zu bestimmten Hilfethemen. Richtlinien zum Schreiben von guten Hilfelinks finden Sie unter [Hilfelinks.](#text)

    **Falsch:**

    ![Screenshot des Dialogfelds mit dem Link "Weitere Informationen" ](images/winenv-help-image9.png)

    Verwenden Sie nicht "Weitere Informationen" oder "Weitere Informationen..." Links.

    **Falsch:**

    ![Screenshot der Hilfeschaltfläche neben Commitschaltflächen ](images/winenv-help-image10.png)

    Verwenden Sie keine generischen Hilfeschaltflächen.

    **Falsch:**

    ![Screenshot des Fragezeichensymbols auf der Titelleiste ](images/winenv-help-image11.png)

    Verwenden Sie keine kontextspezifischen Hilfeschaltflächen auf der Titelleiste.

### <a name="content"></a>Content

-   **Erstellen Sie keine offensichtlichen Inhalte.** Hilfethemen, die wiederholen, was sich auf der primären Benutzeroberfläche befindet, bieten keinen Mehrwert.
-   **Erstellen Sie keine Inhalte, auf die der Benutzer nicht in irgendeiner Weise agieren kann.**
    -   **Ausnahme:** Einige konzeptionelle Inhalte liefern wichtige Hintergrundinformationen, ohne notwendigerweise zu Benutzeraktion führen zu müssen.
-   **Vermeiden Sie ungenaue Lösungen für Probleme.** Wenn Sie z. B. "Wenden Sie sich an Ihren Systemadministrator" oder "Anwendung neu installieren" verwenden, sind benutzer frustrierend.
    -   **Ausnahme:** Es empfiehlt sich, sich an den Systemadministrator zu wenden, wenn dies die einzige praktische Lösung ist, und Systemadministratoren erwarten, dass sie für das Problem kontaktiert werden.
-   **Vermeiden Sie Inhalte, die sehr unwahrscheinliche Benutzerszenarien adressieren.** Entwickeln Sie Ihre Haupthilfeinhalte für die normale Nutzung, die Sie erwarten. Beachten Sie wichtige Ausnahmen von der erwarteten Verwendung, behandeln Sie diesen Inhalt jedoch mit einer niedrigeren Priorität.
-   **Sammeln Sie Feedback von Ihren Benutzern darüber, wie hilfreich Ihre Hilfethemen sind.** Benutzern ermöglichen, einzelne Themen zu bewerten. Führen [Sie Benutzerfreundlichkeitsstudien](glossary.md) zu Ihrer Dokumentation durch, um Probleme im Zusammenhang mit der Qualität und Aufholbarkeit von Inhalten zu ermitteln.
    -   **Tipp:** Benutzerfeedback ist auch eine hervorragende Möglichkeit, mehr aufgabenbasierte Inhalte zu generieren, die sich auf das konzentrieren, was Benutzer tatsächlich mit Ihrem Programm machen, im Gegensatz zu featurebasierten Inhalten, die sich einfach auf eine Beschreibung der Technologie konzentrieren.
-   **Stellen Sie mehrere Möglichkeiten für den Zugriff auf Ihre Inhalte zur Verfügung.** Ein Inhaltsverzeichnis, ein Index [](ctrl-search-boxes.md) und ein Suchmechanismus sind drei der gängigsten Methoden zur Verbesserung der Aufsuchbarkeit.
-   **Wenn es mehr als eine Möglichkeit gibt, eine Aufgabe auszuführen, können Sie in den meisten Fällen nur die gängigste Methode dokumentieren, die von unerfahrenen Benutzern verwendet wird.**

### <a name="icons"></a>Symbole

-   Verwenden Sie das Hilfesymbol nur für Explorer-Fenster und die Hubseiten von Systemsteuerungselementen. Verwenden Sie nicht das Hilfesymbol mit Hilfelinks.

**Richtig:**

![Screenshot des Fensters mit Fragezeichensymbol ](images/winenv-help-image12.png)

In diesem Beispiel verwendet ein Windows-Explorer-Fenster ein Hilfesymbol, um Zugriff auf die Hilfe zu ermöglichen.

**Falsch:**

![Screenshot des Fensters mit Hilfesymbol im linken Bereich ](images/winenv-help-image13.png)

In diesem Beispiel wird das Hilfesymbol links unten fälschlicherweise mit einem Hilfelink verwendet.

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

    In den richtigen Beispielen wird der Link in Bezug auf die primäre Frage formuliert, die vom Hilfethema beantwortet wird.

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

    Im falschen Beispiel unterscheidet sich die Überschrift des Hilfethemas erheblich vom Bereich des Hilfelinktexts und kann unorientiert sein.

-   Wenn der Hilfeinhalt online ist, machen Sie dies im Linktext deutlich. Dies trägt dazu bei, das Ergebnis der Links vorhersagbar zu machen.

    **Richtig:**

    Weitere Formate und Tools finden Sie auf der Microsoft-Website.

    **Falsch:**

    Wo finde ich zusätzliche Formate und Tools?

-   Verwenden Sie vollständige Sätze.
-   Verwenden Sie mit Ausnahme von Fragezeichen keine endende Interpunktion.
-   Verwenden Sie keine Ausellipsen für Hilfelinks oder Befehle.

**Hilfeinhalt**

-   Formatieren Sie Benutzeroberflächenelemente fett, um sie leichter zu identifizieren. Dies ist besonders nützlich für Hilfethemen mit Prozeduren, die es Benutzern ermöglichen, Prozeduren zu durchsuchen und relevante Benutzeroberflächenelemente schnell anzuzeigen.
-   Formatieren von Untertiteln mithilfe von italisch. Dies gilt für Tabellen, Grafiken, Screenshots und andere grafische Elemente, die von einer kurzen Texterklärung profitieren.
-   Unter Hilfe finden Sie einfach Hilfe. Verwenden Sie im Allgemeinen nicht den Ausdruck Onlinehilfe, es sei denn, Sie verweisen tatsächlich auf Inhalte auf Ihrer Website.

 

