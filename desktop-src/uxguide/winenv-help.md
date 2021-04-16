---
title: Hilfe
description: Verwenden Sie die Hilfe als sekundären Mechanismus, um die Benutzer beim Ausführen und besser verstehen von Aufgaben \ 8212 zu unterstützen. der primäre Mechanismus ist die Benutzeroberfläche. Wenden Sie diese Richtlinien an, damit der Inhalt wirklich hilfreich und leicht zu finden ist.
ms.assetid: 82ce076e-062b-4793-a1c0-ed96c0f2b284
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 907494e9a97ccaf51e4eba463c34e49854b14a81
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104562391"
---
# <a name="help"></a>Hilfe

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Verwenden Sie die Hilfe als sekundären Mechanismus, um Benutzer beim Ausführen und besseren Verständnis von Aufgaben zu unterstützen. Wenden Sie diese Richtlinien an, damit der Inhalt wirklich hilfreich und leicht zu finden ist.

Ein Hilfesystem besteht aus verschiedenen Arten von Inhalten, die Benutzern helfen sollen, wenn Sie eine Aufgabe nicht ausführen können, ein Konzept ausführlicher verstehen oder weitere technische Details benötigen, als auf der Benutzeroberfläche verfügbar sind.

In diesem Artikel wird als sekundäres Element für die Benutzeroberfläche unterstützt. Die Benutzeroberfläche ist primär, da Benutzer zuerst versuchen, ihre Probleme zu lösen. Sie werden das Hilfesystem nur dann lesen, wenn Sie Ihre Aufgabe nicht mit der Benutzeroberfläche ausführen können.

![Screenshot der Seite "Windows-Hilfe und Support" ](images/winenv-help-image1.png)

Die Windows-Hilfe-und Support-Startseite, die im Startmenü verfügbar ist.

**Hinweis:** Richtlinien im Zusammenhang mit [Stil und Ton](text-style-tone.md) werden in einem separaten Artikel dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Wie motiviert sind die Ziel Benutzer?** Umso wichtiger ist es, dass Sie die Funktionalität Ihres Programms ermitteln und zu fortgeschrittenen oder sogar fortgeschrittenen Benutzern der IT werden. umso besser ist es, dass Sie Antworten auf Ihre Fragen durch Beratungshilfe Themen untersuchen.
-   **Verwenden Sie die Hilfe, um eine fehlerhafte Benutzeroberfläche zu beheben?** Umso besser ist die Benutzeroberfläche, desto weniger Benutzer werden weitere Hilfe suchen. Wenn Ihr Programm eine sehr klare, hilfreiche primäre Benutzeroberfläche aufweist (z. b. für den Fachbereich freie Fehlermeldungen, gut geschriebene Assistenten und eindeutige Dialogfelder), benötigen Sie möglicherweise überhaupt kein sekundäres Hilfesystem.
-   **Ist Ihr Programm relativ einfach?** Wenn dies der Fall ist, sollten Sie ggf. alle notwendigen Unterstützungs Inhalte in ihre primären Oberflächen Oberflächen integrieren. Es ist wahrscheinlicher, dass Benutzer zusätzliche Hilfe in Programmen suchen, die komplexe Aufgaben ausführen.
-   **Richtet sich Ihre Anwendung an Entwickler, IT-Experten oder andere Softwareexperten?** Diese Benutzer erwarten in der Regel Referenz Hilfe für Programmiersprachen Konventionen und ausführliche konzeptionelle Hilfe zur Beherrschung von Features.

## <a name="design-concepts"></a>Entwurfskonzepte

Wenn Sie sich dazu entschließen, Hilfe in das Programm einzubeziehen, integrieren Sie es in ihren Gesamtentwurf. Die Hilfe Schnittstelle sollte einfach, effizient und relevant sein. Dadurch können Benutzer problemlos Hilfe erhalten und dann zu ihrer Aufgabe zurückkehren. Sehen Sie sich Ihr Hilfesystem im Hinblick auf die Benutzer Zeit an: minimieren Sie zunächst die Unterbrechung, indem Sie die Probleme im Programm lösen und diese Probleme lösen, indem Sie grundlegende Unterstützung direkt in die Benutzeroberfläche integrieren und klare und konsistente Einstiegspunkte in Ihre ausführlichere Hilfe erstellen.

Die Windows-Unterstützung wurde gemäß diesen Prinzipien entworfen. Im folgenden finden Sie einige der Entwurfs Änderungen an der Windows-Hilfe:

-   Besser auffinalisier Bare Einstiegspunkte zur Unterstützung der primären Benutzeroberfläche (insbesondere neue Hilfe Links von Benutzeroberflächen Oberflächen wie Dialogfeldern, Fehlermeldungen und Assistenten). Hilfe Links gelangen direkt zum entsprechenden Thema in der-Hilfe.
-   Ein Schaltflächen Symbol für Hilfe ist in der oberen rechten Ecke der meisten System Steuerungs-Hub-Seiten sowie in shellordnern verfügbar.
-   Benutzer können die neuesten Hilfe Inhalte von Windows Online Hilfe und Support erhalten, wenn Sie online sind.
-   Hilfe Themen sind nun Aufgaben basiert und nicht auf Features fokussiert, sodass Benutzer ihre Aufgaben schnell und effizient erledigen können.
-   Hilfe Themen basieren nun größtenteils auf bekannten Top-Benutzer Szenarien.
-   Hilfe Themen haben einen entspannteren und informellen [Ton](text-style-tone.md), der in realer Sprache verwendet wird.
-   Hilfe Themen sind für eine effektive Überprüfung konzipiert, da Benutzer den Word-Word-Word-Inhalt nur selten lesen.

### <a name="an-analogy-for-help"></a>Eine Analogie zur Hilfe

Um mehr über das Entwerfen Ihres Hilfesystems nachzudenken, betrachten Sie eine Analogie aus dem alltäglichen Leben. Sie sind in einer unbekannten Stadt verloren gegangen. Was ist zu tun? Viele würden wie folgt reagieren:

-   Orientierung erhalten; Suchen Sie nach-Marken, Straßen Zeichen (Namen und Zeiger auf Orte).
-   Suchen Sie nach Maps.
-   Stellen Sie schließlich als letztes Mittel eine Anleitung, oder wenden Sie sich an einen Freund.

Der Entwurf der "Schnittstelle" der Stadt wirkt sich auf Ihre Notwendigkeit aus. Gut bezeichnete Straßen, explizite Richtungen (Zeiger auf Krankenhäuser, Flughäfen, Museen, das Postbüro) und klare Kennzeichen, wie z. b. bedeutende geografische Features oder Gebäude, unterstützen Sie bei der Suche.

Sie werden als letztes Mittel um Hilfe gefragt. Es ist ein Hinweis darauf, dass die "Schnittstelle" der Stadt ausgefallen ist, weil sie unzureichend entworfen und verwirrend ist. Es ist wahrscheinlicher, dass Sie an einem Ort, der über eine bestimmte Bezeichnung verfügt und eine bestimmte Bezeichnung vorschlägt, nach Hilfe Fragen. Beispielsweise ist es wahrscheinlicher, dass Sie die Hilfe an einem Ort mit der Bezeichnung "Directions" oder "Information" anfordern, als eine allgemeine Stelle wie die Stadt Hall.

Wenn Sie Hilfe anfordern, sind Sie frustriert und möchten nur auf Ihr beabsichtigter Ziel gelangen. Wahrscheinlich sind Sie nicht in der Lage, eine Tour durch die Stadt zu machen oder den Verlauf kennenzulernen. Die Motivation hängt außerdem von der Wichtigkeit der Aufgabe ab. Wenn Sie versuchen, Ihren Hotel Raum zu finden, machen Sie alles, was Sie benötigt. Wenn Ihr Ziel jedoch darin besteht, eine Stelle der geringfügigen Wichtigkeit zu finden, werden Sie wahrscheinlich nur nach einem geringfügigen Aufwand darauf achten.

Alle diese Aspekte bei der Suche nach dem richtigen Raum entsprechen der Art und Weise, wie Benutzer in der Regel im virtuellen Bereich Ihres Programms suchen. Das Suchen von Hilfe über die primäre Benutzeroberfläche hinaus besteht darin, dass es sich um eine disarisierung handelt. machen Sie sich am besten mit einer gut entworfenen Benutzeroberfläche und intelligenten "Straßen signieren" vertraut, um die Benutzer auf die benötigten Antworten zu lenken.

### <a name="designing-ui-so-that-help-is-unnecessary"></a>Entwerfen der Benutzeroberfläche, sodass Hilfe unnötig ist

Versuchen Sie, die Hilfe zuerst zu überprüfen, indem Sie folgende Schritte durchführen:

-   Die einfache Ermittlung und Durchführung allgemeiner Aufgaben.
-   Eindeutige [Haupt Anweisungen](text-ui.md)werden bereitgestellt.
-   Bereitstellen klarer, präziser Steuerelement Bezeichnungen, die Ziel-und aufgabenorientiert sind.
-   Zusätzliche Anleitungen und Erläuterungen, sofern erforderlich.
-   Die Vorhersage von Problemen mithilfe von Steuerelementen, die auf gültige Optionen beschränkt sind, das Bereitstellen geeigneter Standardwerte, das Behandeln aller Eingabeformate und das verhindern von Fehlern
-   Schreiben von Fehlermeldungen, die eine klare Lösung oder Aktion für den Benutzer bereitstellen.
-   Vermeiden Sie verwirrende UI-Entwürfe, wie z. b. Aufgaben mit mangelendem Datenfluss oder die Verwendung von Steuerelementen, die aus Gründen der
-   Arbeiten mit Writern und Editoren früh im Entwicklungszeitraum, um einen qualitativ hochwertigen, konsistenten [UI-Text](text-ui.md) im gesamten Programm zu erstellen.

Benutzer sollten sich nicht an einem anderen Ort befinden, um herauszufinden, wie Sie Ihre Benutzeroberfläche verwenden. Fügen Sie wichtige Informationen direkt in die primäre Benutzeroberfläche ein, anstatt Benutzer aus Ihrem unmittelbaren Kontext und dem Hilfebereich zu zwingen. Wenn wichtige Informationen nur in einem Hilfethema vorhanden sind, besteht die Möglichkeit, dass Benutzer diese nicht sehen können. Informationen, die optional und ausführlichere Informationen sind, finden Sie unter Hilfe Links von der primären Benutzeroberfläche zum relevanten Hilfethema, um zusätzliche Unterstützung zu erhalten.

### <a name="considering-user-motivation"></a>Berücksichtigen der Benutzer Motivation

Bei den meisten Benutzern gehören Geschwindigkeit und Effizienz zu den wichtigsten Vorteilen guter Programme. Benutzer möchten Ihre Arbeit erledigen. Im Allgemeinen ist es nicht interessant, das Programm und die Technologie zu erlernen. Ihre Geduld wird nur dadurch erweitert, dass das Programm Ihre eigenen Interessen erfüllt und Probleme löst.

Entwerfen Sie Ihr Hilfesystem so, dass es der Motivation Ihrer Benutzer entspricht. Nehmen Sie beispielsweise an, dass ein Benutzer, der sich auf einen Kiosk in einem Museum gezogen hat. Wenn Sie nicht ermitteln kann, wie die Aufgabe schnell durchgeführt werden kann, ist Sie wahrscheinlich einfach nur auf dem neuesten Stand. Es ist unwahrscheinlich, dass Sie sich mit der Hilfe Zeit beschäftigen. Alternativ hat ein stark motivierter Benutzer eine höhere Toleranz für die Zeit, die für die Untersuchung des Hilfesystems für Antworten aufgewendet wird. Ein Geschäfts Benutzer, der z. b. die Bücher ausgleichen muss, ist wahrscheinlich bereit, Hilfe Inhalte zu lesen, um die neue Buchhaltungs Anwendung optimal zu nutzen.

### <a name="writing-content-for-scanning"></a>Schreiben von Inhalten zum Scannen

Schreiben Sie Hilfe Themen, in denen Sie wissen, dass Sie auf bestimmte Informationen überprüft werden, und nicht auf Word für Word. Schreiben Sie einen gewissen Wert, um schnell auf den Punkt zu gelangen und Informationen bereitzustellen, auf die Benutzer reagieren können.

-   Schreiben Sie "Gewusst-wie"-Themen, indem Sie nummerierte Schritte in einem konsistenten Format verwenden, damit die Benutzer erkennen, dass Sie Unterstützung bei der
-   Schreiben Sie Referenz Themen mit einfacher Überprüfung, und verwenden Sie Tabellen, z. b. zur Darstellung von Benutzeroberflächen Optionen oder Sprachsyntax.
-   Schreiben von konzeptionellen Themen, die logisch nach untergeordneten Überschriften angeordnet sind, sodass der Benutzer ganze Abschnitte mit geringerem Interesse überspringen kann.

Bei allen Hilfe Inhalten ist es einfacher, aufzurufene Listen zu scannen als Standard Absatz Blöcke von Text; Verwenden Sie Aufzählungs Listen jedoch nicht als Krümel für unorganisierte Materialien.

### <a name="creating-content-that-matters"></a>Erstellen von Inhalten, die wichtig sind

Da kein Hilfesystem jede Frage, die jeder Benutzer möglicherweise hat, vorhersehen kann, konzentrieren Sie sich auf den größten Teil des Inhalts auf die Beantwortung der wichtigsten Fragen in den wichtigsten Szenarien für Ihre Ziel Benutzer. Beispielsweise können das effektive suchen und das Einrichten von Netzwerkverbindungen (unter anderem Aufgaben) in hohem Maße gesucht werden. Konzentrieren Sie sich auch auf Aufgaben in ihren Top-Benutzer Szenarien, anstatt ein Feature oder eine Technologie für den eigenen Zweck zu dokumentieren.

**Tipp:** Technischer Support ist eine gute Quelle für Hilfe Inhalte. Helpdesks behalten häufig Datensätze häufig gestellter Fragen zu bestimmten Programmen oder Aufgaben bei, die von den Benutzern zu erledigen sind.

Es ist nicht erforderlich, Hilfe zu allen Features in der Benutzeroberfläche bereitzustellen. **Sehr häufig sind nicht hilfreiche Hilfe Ergebnisse bei der Erstellung von Hilfe für alles.** Wenn die Benutzeroberfläche gut entworfen wurde, sind die meisten dieser Hilfe Themen nicht sehr hilfreich. Sie werden lediglich die offensichtlichste wiedergeben.

Wenn es mehr als eine Möglichkeit gibt, eine Aufgabe auszuführen, können Sie in den meisten Fällen nur die gängigste Art dokumentieren, die von unerfahrenen Benutzern verwendet wird. Zu den Ausnahmen gehören Überlegungen zur Barrierefreiheit (z. b. das Dokumentieren von Tastatur Entsprechungen von Mausaktionen) und Platt Form Überlegungen (z. b. die Dokumentation für den Tablet-Formular Faktor oder für Serverumgebungen, in denen die Befehlszeile für die grafische Benutzeroberfläche verwendet werden kann).

Denken Sie daran, dass die Benutzer oft nicht die Probleme, die Sie in den gleichen Begriffen wie Sie auftreten, berücksichtigen. So kann es beispielsweise vorkommen, dass Benutzer sich als "Konto" vorstellen. Stellen Sie sicher, dass Sie Ihre Such-und Indizierungs Funktionalität entwerfen und dann wahrscheinlich Terminologie-und Synonyme für Terminologie berücksichtigen.

Zwischen der primären Benutzeroberfläche und dem Hilfesystem sollten die Begriffe jedoch sehr ähnlich sein, wenn Sie nicht identisch sind. Benutzer können verwirrt werden, wenn sich die Hilfesystem Sprache nicht ganz genau mit der Anzeige auf dem Bildschirm korreliert.

### <a name="writing-compelling-help-link-text"></a>Schreiben von ansprechenden Hilfelink

Wenn Sie über Ihre primäre Benutzeroberfläche eine Verknüpfung mit einem Hilfethema erstellen, achten Sie darauf, dass Sie einen ansprechenden Hilfelink schreiben. Clear und eine bestimmte Sprache sorgen für Vertrauen. Benutzer sind tendenziell der Meinung, dass generische Hilfe Links (eine Schaltfläche mit dem Wort "Help" oder "Weitere Informationen") nicht zu den richtigen Informationen führt, ohne dass eine beträchtliche Zeit investiert werden muss.

**Wenn Sie nur fünf Dinge tun...**

1.  Entwerfen Sie die Benutzeroberfläche, sodass Benutzer keine Hilfe benötigen.
2.  Helfen Sie, Ihre Hilfe zu nutzen, indem Sie den Inhalt auf die wichtigsten Fragen in den wichtigsten Szenarien für Ihre Ziel Benutzer konzentrieren.
3.  Präsentieren Sie den Hilfe Inhalt, sodass er leicht zu scannen ist.
4.  Beachten Sie, dass Sie keine Hilfe zu allen Features in der Benutzeroberfläche bereitstellen müssen.
5.  Machen Sie die Hilfe Einstiegspunkte auffindbar und aussagekräftigen.

## <a name="usage-patterns"></a>Verwendungsmuster

Verschiedene Arten von Inhalten dienen unterschiedlichen Zwecken.



|                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hilfe zur Vorgehensweise**<br/> enthält die Schritte zum Ausführen einer Aufgabe. <br/>                       | Die Verfahrenshilfe sollte sich auf "wie"-Informationen anstelle von "was" oder "Warum" konzentrieren. <br/> ![Screenshot der Hilfeseite zum Löschen von temporären Dateien ](images/winenv-help-image2.png)<br/> In diesem Beispiel wird in dem Hilfethema beschrieben, wie Sie eine Funktion des Hilfsprogramms für die Datenträger Bereinigung verwenden, und Sie können die nachfolgenden Schritte ausführen.<br/>                                              |
| **Konzeptionelle Hilfe**<br/> Stellt Hintergrundinformationen, Featureübersichten oder Prozesse bereit. <br/> | Die konzeptionelle Hilfe sollte über das hinausgehende Informationen bereitstellen, die zum Ausführen einer Aufgabe erforderlich sind. <br/> ![Screenshot der Hilfeseite "Desktop (Übersicht)" ](images/winenv-help-image3.png)<br/> In diesem Beispiel definiert das Hilfethema, was der Desktop ist, und bietet weitere Details darüber, was er enthält und warum Benutzer mit ihm interagieren.<br/>           |
| **Verweis Hilfe**<br/> dient als Online-Referenzbuch. <br/>                                | Sie können die Verweis Hilfe verwenden, um eine Programmiersprache oder Programmierschnittstellen zu dokumentieren. <br/> ![Screenshot der Hilfeseite "notational Conventions" ](images/winenv-help-image4.png)<br/> In diesem Beispiel werden in der Hilfe Themen typografische Konventionen für diese bestimmte Sprache oder Anwendung aufgelistet und die Informationen in einer leicht zu überprüfenden Tabelle bereitgestellt.<br/> |



 

## <a name="guidelines"></a>Richtlinien

### <a name="entry-points"></a>Einstiegspunkte

-   **Link zu bestimmten, relevanten Hilfe Themen.** Keine Verknüpfung mit der Startseite der Hilfe, dem Inhaltsverzeichnis, einer Liste von Suchergebnissen oder einer Seite, die nur mit anderen Seiten verknüpft ist. Vermeiden Sie das Verknüpfen mit Seiten, die als eine große Liste häufig gestellter Fragen strukturiert sind, da Benutzer gezwungen werden, nach der Datei zu suchen, die dem Link entspricht, auf den Sie geklickt haben Verknüpfen Sie nicht mit bestimmten Hilfe Themen, die für die vorliegende Aufgabe nicht relevant und hilfreich sind. Niemals mit leeren Seiten verknüpfen.
-   **Fügen Sie keine Hilfe Verknüpfungen für jedes Fenster oder jede Seite ein, um die Konsistenz zu gewährleisten.** Wenn Sie einen Hilfelink an einem Ort bereitstellen, bedeutet das nicht, dass Sie Sie überall bereitstellen müssen.
-   **Verwenden von Hilfe Verknüpfungen für Dialogfelder, Fehlermeldungen, Assistenten und Eigenschaften Blätter.** Wenn der Hilfelink für bestimmte Steuerelemente gilt, platzieren Sie ihn linksbündig. Wenn der Hilfelink auf das gesamte Fenster zutrifft, platzieren Sie ihn in der unteren linken Ecke des Fensters Inhalts Bereich.

    ![Screenshot des Eigenschaften Blatts mit dem Gruppenfeld ](images/winenv-help-image5.png)

    In diesem Beispiel bezieht sich der zweite Hilfelink auf eine Gruppe von Steuerelementen.

    ![Screenshot des Eigenschaften Blatts und Hilfelink ](images/winenv-help-image6.png)

    In diesem Beispiel wird der Hilfelink auf das gesamte Fenster angewendet.

-   **Verwenden Sie Hilfe Links anstelle von generischen Text verweisen, um immer technisch zu helfen.**

    **Richtig:**

    Wie kann ich Datenträger Fehler reparieren?

    **Falsch:**

    Weitere Informationen zum Reparieren von Datenträger Fehlern finden Sie unter Hilfe und Support.

-   **Verwenden Sie eine Hilfe Schaltfläche mit dem Hilfe Symbol für die Hub-Seiten der System Steuerungselemente.** Platzieren Sie ihn in der oberen rechten Ecke. Diese Schaltflächen verfügen nicht über eine Bezeichnung, aber Sie verfügen über eine QuickInfo, die die Hilfe liest.

    ![Screenshot des System Steuerungs Elements mit der Schaltfläche "Hilfe" ](images/winenv-help-image7.png)

    Ein System Steuerungselement mit einer Hilfe Schaltfläche.

-   **Die F1-Hilfe ist optional.** Benutzer haben sich daran gewöhnt, Hilfe Informationen zum unmittelbaren Kontext der Benutzeroberfläche auf dem Bildschirm zu finden, indem Sie die F1-Taste drücken, die als Hilfe zu Standard-Tastaturen bezeichnet wird. Sie können F1-Hilfe einschließen, wenn z. b. Verwendbarkeits Studien zeigen, dass die Benutzer das Auffinden erwarten, oder die Programm Benutzeroberfläche ist komplex genug, um von kontextbezogener Unterstützung profitieren zu können.
-   **Programme mit Menüleisten können über eine Menükategorie "Hilfe" verfügen.** Hilfe Menü Richtlinien finden Sie unter [Menüs](cmd-menus.md).

    ![Screenshot der Hilfe, auf die über die Menüleiste zugegriffen wird ](images/winenv-help-image8.png)

    In diesem Beispiel verfügt das Windows Paint-Zubehör über eine Menükategorie "Hilfe".

-   **Geben Sie für die Tastatureingabe Tabstopps für Hilfe Schaltflächen und Verknüpfungen an.**
-   Hilfe Schaltfläche und Verknüpfungs Verhalten sollten wie folgt lauten: der Hilfebereich wird geöffnet, und es wird ein dediziertes Hilfethema angezeigt. die Benutzeroberfläche, die den Bereich Hilfe aufgerufen hat, sollte offen bleiben, um die kontextbezogene Darstellung zu erhalten.
-   **Verwenden Sie nicht die folgenden veralteten Hilfe Einstiegspunkt-Stile: "Weitere Informationen" oder "Weitere Informationen zu..." Links, generische Hilfe Schaltflächen und kontextabhängige Hilfe Schaltflächen auf der Titelleiste.** Obwohl Sie in der Vergangenheit verwendet wurden, haben Benutzerfreundlichkeit festgestellt, dass Sie von den Benutzern tendenziell ignoriert werden. Verwenden Sie stattdessen Links zu bestimmten Hilfe Themen. Richtlinien zum Schreiben von guten Hilfe Links finden Sie unter [Hilfe Links](#text).

    **Falsch:**

    ![Screenshot des Dialog Felds mit dem Link "Weitere Informationen" ](images/winenv-help-image9.png)

    Verwenden Sie nicht "Weitere Informationen" oder "Weitere Informationen zu..." verweist.

    **Falsch:**

    ![Screenshot der Schaltfläche "Hilfe" neben Commit-Schaltflächen ](images/winenv-help-image10.png)

    Verwenden Sie keine generischen Hilfe Schaltflächen.

    **Falsch:**

    ![Screenshot des fragezeichensymbols in der Titelleiste ](images/winenv-help-image11.png)

    Verwenden Sie auf der Titelleiste keine kontextbezogenen Hilfe Schaltflächen.

### <a name="content"></a>Inhalt

-   **Erstellen Sie keinen offensichtlichen Inhalt.** Hilfe Themen, die wiederholen, was sich in der primären Benutzeroberfläche befindet, fügen keinen Wert hinzu
-   **Erstellen Sie keinen Inhalt, in dem der Benutzer nicht auf irgendeine Weise agieren kann.**
    -   **Ausnahme:** Einige konzeptionelle Inhalte liefern wichtige Hintergrundinformationen, ohne dass Sie notwendigerweise zu Benutzeraktionen führen.
-   **Vermeiden Sie vage Lösungen für Probleme.** Beispiel: "wenden Sie sich an den Systemadministrator, oder installieren Sie die Anwendung neu, um Benutzer zu beeinträchtigen.
    -   **Ausnahme:** Es wird empfohlen, sich an den Systemadministrator zu wenden, wenn dies die einzige praktische Lösung ist, und Systemadministratoren erwarten, dass Sie mit dem Problem kontaktiert werden.
-   **Vermeiden Sie Inhalte, die sehr unwahrscheinlich in Benutzer Szenarios behandelt werden.** Entwickeln Sie Ihre Haupt Hilfe Inhalte für das, was Sie als normale Verwendung erwarten. Beachten Sie wichtige Ausnahmen bei der erwarteten Verwendung, behandeln Sie diesen Inhalt jedoch mit niedrigerer Priorität.
-   **Sammeln Sie Feedback von Ihren Benutzern über die hilfreiche Hilfe Themen.** Ermöglicht es Benutzern, einzelne Themen zu bewerten. Führen Sie in Ihrer Dokumentation [Nutzbarkeits Studien](glossary.md) durch, um Probleme mit der Qualität und Auffindbarkeit von Inhalten zu ermitteln.
    -   **Tipp:** Benutzer Feedback ist auch eine hervorragend Möglichkeit, mehr aufgabenbasierte Inhalte zu generieren, die sich darauf konzentrieren, was Benutzer mit Ihrem Programm tatsächlich tun, und sich nicht um featurebasierte Inhalte, sondern lediglich eine Beschreibung der Technologie.
-   **Bietet mehrere Möglichkeiten, auf Ihre Inhalte zuzugreifen.** Ein Inhaltsverzeichnis, ein Index und ein [Such](ctrl-search-boxes.md) Mechanismus sind drei der gängigsten Methoden zum Verbessern der Auffindbarkeit.
-   **Wenn es mehr als eine Möglichkeit gibt, eine Aufgabe auszuführen, können Sie in den meisten Fällen nur die gängigste Art dokumentieren, die von unerfahrenen Benutzern verwendet wird.**

### <a name="icons"></a>Symbole

-   Verwenden Sie das Hilfe Symbol nur für Explorer-Fenster und die Hub-Seiten der System Steuerungselemente. Verwenden Sie das Hilfe Symbol nicht mit Hilfe Links.

**Richtig:**

![Screenshot des Fensters mit dem Fragezeichen-Symbol ](images/winenv-help-image12.png)

In diesem Beispiel verwendet ein Windows-Explorer-Fenster ein Hilfe Symbol, um den Zugriff auf die Hilfe zu ermöglichen.

**Falsch:**

![Screenshot des Fensters mit Hilfe Symbol im linken Bereich ](images/winenv-help-image13.png)

In diesem Beispiel wird das Hilfe Symbol unten links mit einem Hilfelink falsch verwendet.

## <a name="text"></a>Text

**Hilfe Links**

-   Stellen Sie spezifische Informationen zum Inhalt des Hilfe Themas bereit, und verwenden Sie so viel relevanten und präzisen Text wie erforderlich. Benutzer ignorieren häufig generische Hilfe Links. Stellen Sie sicher, dass die Ergebnisse der Verknüpfung vorhersagbar sind. Benutzer sollten nicht von den Ergebnissen überrascht sein.

    -   **Ausnahme:** Sie können "Weitere Informationen" verwenden, um Anweisungen zu ergänzen, die sich direkt in der Benutzeroberfläche befinden. Dies gilt insbesondere dann, wenn die Bereitstellung spezifischer Informationen im Hilfelink zu unnötigen Wiederholungen führt oder den Link weniger interessant macht.

    **Falsch:**

    Ein sicheres Kennwort hat mindestens sechs Großbuchstaben, Zahlen und Symbole. Was ist ein sicheres Kennwort?

    **Richtig:**

    Ein sicheres Kennwort hat mindestens sechs Großbuchstaben, Zahlen und Symbole. Weitere Informationen

    Im falschen Beispiel wird der Hilfelink wiederholt. Es wird eine Frage gestellt, die wirklich bereits beantwortet wurde.

-   Wenn möglich, verknüpfen Sie Text in Bezug auf die primäre Frage, die der Hilfe Inhalt beantwortet hat. Verwenden Sie nicht "Weitere Informationen zu", "Weitere Informationen zu" oder "Hilfe zu diesem" formulieren.

    **Falsch:**

    Weitere Informationen zum Hinzufügen von Ausnahmen

    **Richtig:**

    Welche Risiken besteht darin, Ausnahmen zuzulassen?

    Gewusst wie Ausnahmen hinzufügen?

    In den richtigen Beispielen wird der Link in Bezug auf die primäre Frage formuliert, die im Hilfethema beantwortet wird.

-   Wenn die relevantesten Informationen kurz zusammengefasst werden können, platzieren Sie die Zusammenfassung direkt in der Benutzeroberfläche, anstatt einen Hilfelink zu verwenden. Sie können jedoch einen Hilfelink verwenden, um zusätzliche Informationen bereitzustellen.

    **Falsch:**

    ![Screenshot des Links zu einem sicheren Kennwort? ](images/winenv-help-image14.png)

    **Richtig:**

    ![Screenshot des ergänzenden Texts zu kenn Wörtern ](images/winenv-help-image15.png)

    **Besserer**

    ![Screenshot von Text mit Link zu weiteren Informationen ](images/winenv-help-image16.png)

    Im richtigen Beispiel werden die Hilfe Informationen kurz zusammengefasst und die Wahrscheinlichkeit, dass Benutzer Sie lesen, deutlich verbessert. Das bessere Beispiel bietet einen Hilfelink, um weitere Informationen zu diesem komplexen Thema zu erhalten.

-   Hilfe Links zu Ausdrücken, um Unterstützung eindeutig anzugeben. Hilfe Links sollten nie ähnliche Aktions Verknüpfungen lesen.
-   Verwenden Sie den gesamten Hilfelink für den Linktext, nicht nur für die Schlüsselwörter.

    **Richtig:**

    Welche Risiken besteht darin, Ausnahmen zuzulassen?

    **Falsch:**

    Welche Risiken besteht darin, Ausnahmen zuzulassen?

    Im richtigen Beispiel wird der gesamte Hilfelink-Satz für den Linktext verwendet.

    -   **Ausnahme:** Hilfe Links zu externen Websites sollten einfach den Namen der Website oder der Seite als Link verwenden. Jeder Text, der den Namen der Site einführt, muss nicht in den Link selbst eingeschlossen werden.

-   Hilfe Links müssen nicht genau mit Hilfe Themenüberschriften übereinstimmen, aber es sollte eine starke und offensichtliche Verbindung zwischen den beiden vorhanden sein. Entwerfen Sie Verknüpfungen und Überschriften in Paaren aus diesem Grund.

    **Richtig:**

    Wie kann ich die Leistung dieses Features verbessern? (Linktext)

    Konfigurieren dieses Features für eine optimale Leistung (Themen Überschrift)

    **Falsch:**

    Wie kann ich die Leistung dieses Features verbessern? (Linktext)

    Umfassende Übersicht über dieses Feature (Themen Überschrift)

    Im falschen Beispiel unterscheidet sich die Überschrift des Hilfe Themas im Gültigkeitsbereich vom Hilfelink-Text und kann sich möglicherweise nicht mehr unterscheiden.

-   Wenn der Hilfe Inhalt online ist, legen Sie diesen im Linktext fest. Dadurch wird das Ergebnis der Verknüpfungen vorhersagbar.

    **Richtig:**

    Weitere Formate und Tools finden Sie auf der Microsoft-Website.

    **Falsch:**

    Wo finde ich weitere Formate und Tools?

-   Verwenden Sie vollständige Sätze.
-   Verwenden Sie keine endinterpunktions Zeichen, mit Ausnahme von Fragezeichen.
-   Verwenden Sie keine Ellipsen für Hilfe Links oder Befehle.

**Hilfe Inhalt**

-   Formatieren Sie Benutzeroberflächen Elemente mithilfe von Fetten, damit Sie leicht zu erkennen sind. Dies ist besonders nützlich für prozedurale Hilfe Themen, die es Benutzern ermöglichen, Prozeduren zu durchsuchen und relevante Benutzeroberflächen Elemente schnell anzuzeigen.
-   Formatieren von Beschriftungen mithilfe von kursiv Formatierung. Dies gilt für Tabellen, Grafiken, Screenshots und andere grafische Elemente, die von einer kurzen Erläuterung von Text profitieren.
-   Weitere Informationen finden Sie in der Hilfe. Verwenden Sie im Allgemeinen nicht den Begriff "Online Hilfe", es sei denn, Sie verweisen tatsächlich auf Inhalte auf Ihrer Website.

 

