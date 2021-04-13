---
title: Warnmeldungen
description: Eine Warnmeldung ist ein modales Dialogfeld, eine direkte Nachricht, eine Benachrichtigung oder eine Sprechblase, die den Benutzer über eine Bedingung benachrichtigt, die möglicherweise in der Zukunft ein Problem verursacht.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d704890b2471e205b933e2995950716c269488e8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351088"
---
# <a name="warning-messages"></a>Warnmeldungen

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Eine Warnmeldung ist ein modales Dialogfeld, eine direkte Nachricht, eine Benachrichtigung oder eine Sprechblase, die den Benutzer über eine Bedingung benachrichtigt, die möglicherweise in der Zukunft ein Problem verursacht.

![Screenshot einer typischen Warnmeldung](images/mess-warn-image1.png)

Eine typische modale Warnmeldung.

Das wichtigste Merkmal von Warnungen besteht darin, dass Sie das Risiko eines Verlusts von einem oder mehreren der folgenden Punkte einschließen:

-   Ein wertvolles Asset, z. b. wichtige Finanzdaten oder andere Daten.
-   System Zugriff oder-Integrität.
-   Datenschutz oder Kontrolle über vertrauliche Informationen.
-   Benutzer Zeit (eine beträchtliche Menge, z. b. 30 Sekunden oder mehr).

Im Gegensatz dazu ist eine Bestätigung ein modales Dialogfeld, in dem Sie gefragt werden, ob der Benutzer eine Aktion fortsetzen möchte. Einige Typen von Warnungen werden als Bestätigungen dargestellt, und wenn dies der Fall ist, gelten die Bestätigungs Richtlinien ebenfalls.

**Hinweis:** Richtlinien, die sich auf [Dialogfelder](win-dialog-box.md), [Bestätigungen](mess-confirm.md), [Fehlermeldungen](mess-error.md)[Standardsymbole](vis-std-icons.md), [Benachrichtigungen](mess-notif.md)und das [Layout](vis-layout.md) beziehen, werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Wird der Benutzer über eine Bedingung benachrichtigt, die in der Zukunft möglicherweise ein Problem verursacht?** Andernfalls ist die Nachricht keine Warnung.
-   **Stellt die Benutzeroberfläche einen Fehler oder ein Problem dar, das bereits aufgetreten ist?** Wenn dies der Fall ist, verwenden Sie stattdessen eine Fehlermeldung.
-   **Werden Benutzer wahrscheinlich eine Aktion ausführen oder Ihr Verhalten als Ergebnis der Nachricht ändern?** Wenn dies nicht der Fall ist, wird die Unterbrechung des Benutzers durch die Bedingung nicht rechtfertigen, sodass die Warnung besser unterdrückt werden kann
-   **Ist die Bedingung das direkte Ergebnis einer vom Benutzer initiierten Aktion?** Wenn dies nicht der Fall ist, sollten Sie eine [nicht kritische Ereignis Benachrichtigung](mess-notif.md)verwenden.
-   **Handelt es sich bei der Bedingung um eine besondere Bedingung in einem Steuerelement?** Verwenden Sie in diesem Fall [stattdessen eine](ctrl-balloons.md) Sprechblase.
-   **Soll der Benutzer für Bestätigungen eine riskante Aktion ausführen?** Wenn dies der Fall ist, ist eine Warnung geeignet, wenn die Aktion bedeutende Konsequenzen hat oder nicht einfach rückgängig gemacht werden kann.
-   **Für andere Typen von Warnungen muss der Benutzer jetzt oder in naher Zukunft agieren?** Zeigen Sie keine Warnungen an, wenn Benutzer ohne unmittelbare Probleme weiterhin produktiv arbeiten können. Verschieben Sie die Warnung so lange, bis die Bedingung unmittelbarer und relevanter ist.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="avoid-overwarning"></a>Vermeiden von überschreinungs Warnungen

Wir haben in Microsoft Windows-Programmen Vorrang vor der Warnung. Das typische Windows-Programm weist scheinbar überall Warnungen auf, die mit einer geringen Bedeutung zu tun haben. In einigen Programmen wird fast jede Frage als Warnung angezeigt. Durch die übermäßige Warnung wird die Verwendung eines Programms wie eine gefährliche Aktivität vereinfacht, und es wird von wirklich wichtigen Problemen entfernt.

**Falsch:**

![Screenshot einer unnötigen Warnmeldung ](images/mess-warn-image2.png)

Durch die übermäßige Warnung wird Ihr Programm gefährlich, und es sieht so aus, als ob es von Anwälten entworfen wurde

Das einzige Potenzial für Datenverluste oder ein zukünftiges Problem allein ist nicht ausreichend, um eine Warnung aufzurufen. Außerdem sollten unerwünschte Ergebnisse unerwartet oder unbeabsichtigt sein und nicht einfach korrigiert werden. Andernfalls können fast alle Benutzerfehler so interpretiert werden, dass Datenverluste oder potenzielle Probleme auftreten und eine Warnung ausgegeben wird.

### <a name="characteristics-of-good-warnings"></a>Merkmale von guten Warnungen

Gute Warnungen:

-   **Risiken einbeziehen.** Gute Warnungen warnen Benutzer von etwas signifikanter.

**Falsch:**

![Screenshot von "möchten Sie den Vorgang beenden?" warning ](images/mess-warn-image3.png)

Na und? Diese Bestätigung setzt voraus, dass Benutzer Programme oft versehentlich beenden.

-   **Sie haben unmittelbare Relevanz.** Sie müssen sich nicht nur auf die Benutzer kümmern, sondern auch darauf achten. Benutzer sind in der Regel nicht an Problemen interessiert, die möglicherweise später auftreten, wenn Sie Ihre Arbeit jetzt erledigen können.

**Falsch:**

![Screenshot der Akku-Low-in-3-Stunden-Warnung ](images/mess-warn-image4.png)

In diesem Fall ist es besser, den Benutzer in drei Stunden zu warnen.

-   **Führt zu einer Aktion.** Es gibt etwas, das Benutzer als Ergebnis der Warnung verwenden oder beachten müssen. Möglicherweise müssen Sie jetzt oder in der unmittelbaren Zukunft eine Aktion durchführen. Möglicherweise wird eine Aufgabe als Ergebnis anders durchgeführt. Die Folge, dass die Warnung ignoriert wird, sollte klar sein. Warnungen ohne Aktionen machen es einfach, dass die Benutzer in der Meinung sind

**Falsch:**

![Screenshot der Warnung "Live Messenger wird ausgeführt" ](images/mess-warn-image5.png)

Warum ist diese Benachrichtigung eine Warnung? Was sollten Benutzer tun (neben Sorge)?

-   **Sind nicht offensichtlich.** Zeigen Sie keine Warnung an, um die offensichtliche Folge einer Aktion anzuzeigen. Nehmen Sie z. b. an, dass Benutzer die Konsequenzen der Nichtausführung einer Aufgabe verstehen.

**Falsch:**

![Screenshot von möchten Sie den Assistenten beenden? davor ](images/mess-warn-image6.png)

Wenn Sie einen unvollständigen Assistenten abbrechen, wird der Task nicht ausgeführt... Wer wusste?

-   **Tritt selten auf.** Konstante Warnungen werden schnell wirkungslos und lästig. Benutzer werden häufig stärker darauf ausgerichtet, die Warnung zu beseitigen, als das Problem zu beheben.

**Falsch:**

![Screenshot der Warnung "Viren Signaturen aktualisieren" ](images/mess-warn-image7.png)

Benutzer sind eher darauf ausgerichtet, die Warnung zu entfernen, als das zugrunde liegende Problem zu beheben.

Eine Nachricht, die nicht über diese Merkmale verfügt, ist möglicherweise trotzdem eine gute Nachricht, aber keine gute Warnung.

### <a name="determine-the-appropriate-message-type"></a>Bestimmen des geeigneten Nachrichten Typs

Einige Probleme können je nach Betonung und Formulierung als Fehler, Warnung oder Informationen angezeigt werden. Nehmen Sie beispielsweise an, eine Webseite kann ein nicht signiertes ActiveX-Steuerelement nicht auf Grundlage der aktuellen Windows Internet Explorer-Konfiguration laden:

-   **Zeit.** "Auf dieser Seite kann kein nicht signiertes ActiveX-Steuerelement geladen werden." (Als vorhandenes Problem formuliert.)
-   **Davor.** "Diese Seite verhält sich möglicherweise nicht wie erwartet, da Windows Internet Explorer nicht zum Laden von nicht signierten ActiveX-Steuerelementen konfiguriert ist." oder "Diese Seite darf ein nicht signiertes ActiveX-Steuerelement installieren? Wenn Sie dies aus nicht vertrauenswürdigen Quellen machen, kann dies Ihren Computer beeinträchtigen. " (Beide werden als Bedingungen formuliert, die möglicherweise zukünftige Probleme verursachen.)
-   **Informationen.** "Sie haben Windows Internet Explorer so konfiguriert, dass nicht signierte ActiveX-Steuerelemente blockiert werden." (Als eine-Anweisung formuliert.)

**Um den richtigen Nachrichtentyp zu bestimmen, konzentrieren Sie sich auf den wichtigsten Aspekt des Problems, das Benutzer kennen oder reagieren müssen.** Wenn ein Problem darin besteht, dass der Benutzer nicht mehr fortfahren kann, sollten Sie es in der Regel als Fehler darstellen. Wenn der Benutzer fortfahren kann, stellen Sie ihn als Warnung dar. Erstellen Sie die [Haupt Anweisung](text-ui.md) oder einen anderen entsprechenden Text basierend auf diesem Fokus, und wählen Sie dann ein Symbol ([Standard](vis-std-icons.md) oder anderweitig), das mit dem Text übereinstimmt. Der Hauptanweisungs Text und die Symbole sollten immer mit dem Text identisch sein

### <a name="be-specific"></a>Spezifisch

Warnungen sind überzeugender, wenn die folgenden Informationen spezifisch und klar sind:

-   Die Quelle der Warnung.
-   Die spezifische Bedingung und das potenzielle Problem.
-   Was der Benutzer damit tun sollte.
-   Was geschieht, wenn der Benutzer nichts tut.

**Falsch:**

![Screenshot der vagen Warnung mit erheblichem Risiko ](images/mess-warn-image8.png)

In diesem Beispiel ist das potenzielle Problem? Was soll der Benutzer tun, abgesehen davon, dass er nicht den Projektor über das Netzwerk verwendet? Ohne genauere Informationen kann der Vorgang nicht durchgeführt werden.

**Richtig:**

![Screenshot der Warnung zu Problemen und folgen ](images/mess-warn-image9.png)

In diesem Beispiel sind das Problem und die Konsequenzen eindeutig.

Manchmal gibt es ein legitimer potenzielles Problem, das die Benutzer über informiert, aber die Lösung und die Konsequenzen sind nicht bekannt. Anstatt eine vage Warnung anzugeben, sollten Sie die wahrscheinlichsten Informationen oder das gängigste Beispiel bereitstellen.

**Richtig:**

![Screenshot der Netzwerkfehler Warnung und-Lösungen ](images/mess-warn-image10.png)

In diesem Beispiel wird die Warnung durch Bereitstellen der wahrscheinlichsten Lösung festgestellt.

Verwenden Sie in solchen Fällen jedoch einen Wortlaut, der angibt, dass andere Möglichkeiten vorhanden sind. Andernfalls werden Benutzer möglicherweise Irre geführt.

**Falsch:**

![Screenshot der Warnung "Netzwerkkabel getrennt" ](images/mess-warn-image11.png)

**Richtig:**

![Screenshot des Kabels kann eine fehlende Warnung sein ](images/mess-warn-image12.png)

Im falschen Beispiel werden die Benutzer verwirrt, wenn das Kabel eindeutig angeschlossen ist.

**Wenn Sie nur zwei Dinge tun...**

1. Nicht überschreiben. Beschränken Sie Warnungen auf Bedingungen, die ein Risiko darstellen und sofort relevant, handlungsfähig, nicht offensichtlich und selten sind. Andernfalls entfernen Sie die Nachricht, oder formulieren Sie Sie neu.

2. Geben Sie spezielle, nützliche Informationen an.

## <a name="usage-patterns"></a>Verwendungsmuster

Warnungen weisen mehrere Verwendungs Muster auf:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Bewusstsein</strong><br/> Sorgen Sie dafür, dass der Benutzer eine Bedingung oder ein potenzielles Problem erkennt, aber der Benutzer muss möglicherweise noch nichts Unternehmen. <br/></td>
<td><img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br/> <img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br/> <img src="images/mess-warn-image15.png" alt="Screen shot of &#39;caps-lock-is-on&#39; warning " /><br/> <img src="images/mess-warn-image16.png" alt="Screen shot of &#39;TPM-not-found&#39; warning " /><br/> Beispiele für Warnungen zu Warnungen.<br/> Warnungen zu Warnungen haben folgende Präsentation: <br/>
<ul>
<li><strong>Main-Anweisung:</strong> Beschreiben Sie die Bedingung oder das potenzielle Problem.</li>
<li><strong>Ergänzende Anweisung:</strong> Erläutern Sie die Implikation und warum Sie wichtig ist.</li>
<li><strong>Commit-Schaltflächen:</strong> Ihrer.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Fehler Verhinderung</strong><br/> Machen Sie die Benutzer auf Informationen aufmerksam, die möglicherweise ein Problem verhindern, insbesondere bei Auswahlmöglichkeiten. <br/></td>
<td>Warnungen zur Fehler Verhinderung werden am besten mit einem direkten Warnsymbol und einem erklärenden Text dargestellt. <br/> <img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br/> <img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br/> Beispiele für Warnungen zur Fehler Verhinderung.<br/></td>
</tr>
<tr class="odd">
<td><strong>Bevorstehendes Problem</strong><br/> Der Benutzer muss jetzt etwas tun, um ein bevorstehendes Problem zu verhindern. <br/></td>
<td><img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br/> Ein Beispiel für eine Warnung zu einem bevorstehenden Problem.<br/> Bevorstehende Problem Warnungen haben folgende Präsentation: <br/>
<ul>
<li><strong>Main-Anweisung:</strong> Beschreiben Sie, was der Benutzer jetzt tun muss.</li>
<li><strong>Ergänzende Anweisung:</strong> Erläutern Sie die Bedingung und warum Sie wichtig ist.</li>
<li><strong>Commit-Schaltflächen:</strong> Eine Befehls Schaltfläche oder ein Befehls Link für jede Option oder OK, wenn die Aktion außerhalb des Dialog Felds erfolgt.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Bestätigung der riskanten Aktion</strong><br/> Vergewissern Sie sich, dass der Benutzer eine Aktion durchführen möchte, die ein gewisses Risiko aufweist und nicht einfach rückgängig gemacht werden kann. <br/></td>
<td><img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br/> Ein Beispiel für eine risikobehaftete Aktions Bestätigung.<br/> Riskante Aktions Bestätigungen haben die folgende Präsentation: <br/>
<ul>
<li><strong>Main-Anweisung:</strong> Stellen Sie eine Frage, um zu bestimmen, ob der Benutzer den Vorgang fortsetzen möchte.</li>
<li><strong>Ergänzende Anweisung:</strong> Erläutern Sie alle nicht offensichtlichen Gründe, warum der Benutzer möglicherweise nicht fortfahren möchte.</li>
<li><strong>Commit-Schaltflächen:</strong> Ja, Nein.</li>
</ul>
Richtlinien zu diesem Muster finden Sie unter <a href="mess-confirm.md">Bestätigungen</a>. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

-   **Wählen Sie die Präsentations Benutzeroberfläche basierend auf der Art der Informationen aus:**



|                               |                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **User interface (Benutzeroberfläche)**<br/> | **Beste Verwendung für**<br/>                                                                                                           |
| Modale Dialogfelder<br/> | Kritische Warnungen (einschließlich Bestätigungen), auf die Benutzer jetzt Antworten müssen.<br/>                                                 |
| Direkt<br/>           | Informationen, die möglicherweise ein Problem verhindern, insbesondere, wenn Benutzer Entscheidungen treffen.<br/>                                         |
| Mitzubringen<br/>            | Informationen, die möglicherweise ein Problem verhindern, insbesondere im Zusammenhang mit dem Abschließen einer Aufgabe.<br/>                                     |
| Benachrichtigungen<br/>      | Wichtige Ereignisse oder Status, die auf sichere Weise ignoriert werden können, zumindest vorübergehend.<br/>                                              |
| Ballons<br/>           | Ein-Steuerelement befindet sich in einem Zustand, der sich auf Eingaben auswirkt Dieser Status ist wahrscheinlich unbeabsichtigt, und der Benutzer hat möglicherweise keine Eingaben erkannt.<br/> |



 

-   **Für modale Dialogfelder:**
    -   **Verwenden Sie nach Bedarf Aufgaben Dialogfelder, um ein konsistentes Aussehen und Layout zu erzielen.** Aufgaben Dialogfelder erfordern Windows Vista oder höher, sodass Sie nicht für frühere Versionen von Windows geeignet sind.
    -   **Zeigt nur eine Warnmeldung pro Bedingung an.** Zeigen Sie z. b. eine einzelne Warnung an, die eine Bedingung vollständig erläutert, anstatt Sie jeweils einmal pro Nachricht zu beschreiben. Das Anzeigen einer Sequenz von Warn Dialogfeldern für eine einzelne Bedingung ist verwirrend und lästig.
    -   **Zeigen Sie eine Warnung nicht mehr als einmal pro Bedingung an.** Konstante Warnungen werden schnell wirkungslos und lästig. Benutzer werden häufig stärker darauf ausgerichtet, die Warnung zu beseitigen, als das Problem zu beheben. Wenn Sie für eine einzelne Bedingung wiederholt warnen müssen, verwenden Sie [Progressive Eskalation](mess-notif.md).
-   **Führen Sie keine Warnungen mit einem Soundeffekt oder einem Signal aus.** Dabei handelt es sich um jarringverfahren und unnötig.
    -   **Ausnahme:** Wenn der Benutzer sofort Antworten muss, können Sie einen Soundeffekt verwenden.

### <a name="icons"></a>Symbole

-   Platzieren Sie kein Warnsymbol in der Titelleiste eines Dialog Felds.
-   **Verwenden Sie ein Warnsymbol.** Ausnahmen:
    -   Wenn die Warnung für eine Funktion ist, die über ein Symbol verfügt, können Sie das Funktions Symbol mit einem Warn Überlagerungs Symbol verwenden.

        **Richtig:**

        ![Screenshot des sperrsymbols mit Warnsymbol Überlagerung ](images/mess-warn-image21.png)

        In diesem Beispiel enthält das Feature-Symbol eine Warn Überlagerung.

-   Legen Sie für modale Dialogfelder mit einer Warn fußnotiz das Warnsymbol in der fußnotiz anstelle des Inhalts Bereichs ab.

    **Richtig:**

    ![Screenshot des Warn Symbols im Dialogfeld "Fußnote" ](images/mess-warn-image22.png)

    In diesem Beispiel enthält die fußnotiz das Warnsymbol.

Weitere Richtlinien und Beispiele finden Sie unter [Standard Symbole](vis-std-icons.md).

### <a name="dont-show-this-message-again"></a>Diese Meldung nicht mehr anzeigen

-   **Wenn diese Option für ein Warn Dialogfeld erforderlich ist, überdenken Sie die Warnung und deren Häufigkeit.** Wenn Sie über alle Merkmale einer guten Warnung verfügt (was ein Risiko darstellt und sofort relevant, handlungsfähig, nicht offensichtlich und unregelmäßig ist), sollte es für Benutzer nicht sinnvoll sein, Sie zu unterdrücken.

Weitere Richtlinien finden Sie unter [Dialog Felder](win-dialog-box.md).

### <a name="progressive-disclosure"></a>Schrittweise Offenlegung

-   **Wenn Sie erweiterte Informationen in eine Warnmeldung einschließen müssen, können Sie diese mithilfe der Schaltflächen für die Progressive Offenlegung** anzeigen (z. b. "Details anzeigen"). Dies vereinfacht die Warnung für die typische Verwendung. Blenden Sie erforderliche Informationen nicht aus, da Benutzer Sie möglicherweise nicht finden.
-   **Verwenden Sie "Details anzeigen" nicht, es sei denn, es gibt wirklich weitere Details.** Geben Sie die vorhandenen Informationen nicht nur in einem anderen Format zurück.

Informationen zu Bezeichnungs Richtlinien finden Sie unter [Progressive Offenlegung](ctrl-progressive-disclosure-controls.md).

### <a name="default-values"></a>Standardwerte

-   **Wählen Sie die sicherste, am wenigsten zerstörerische oder sicherste Antwort als Standard aus.**

## <a name="text"></a>Text

### <a name="general"></a>Allgemein

-   **Entfernen Sie den redundanten Text.** Suchen Sie nach dem Titel, den Haupt Anweisungen, zusätzlichen Anweisungen, Inhalts Bereichen, Befehls Verknüpfungen und Commit-Schaltflächen. Im Allgemeinen sollten Sie voll Text in Anweisungen und interaktiven Steuerelementen belassen und Redundanz von den anderen Orten entfernen.
-   **Verwenden Sie nicht die Begriffe "Warnung" oder "Vorsicht" im Text.** Wenn das Warnsymbol [ordnungsgemäß verwendet](vis-std-icons.md)wird, kommuniziert das Warnsymbol ausreichend, dass Benutzer mit Vorsicht fortfahren müssen.

**Falsch:**

![Screenshot der unnötigen Verwendung von Warnung im Text ](images/mess-warn-image23.png)

In diesem Beispiel ist der Begriff "Warning" nicht erforderlich.

### <a name="titles"></a>Titel

-   **Verwenden Sie den Titel, um den Befehl oder das Feature zu identifizieren, von dem die Warnung stammt.** Ausnahmen:
    -   Wenn eine Warnung von vielen verschiedenen Befehlen angezeigt wird, sollten Sie stattdessen den Programmnamen verwenden.
    -   Wenn der Titel mit der Main-Anweisung redundant oder verwirrend wäre, sollten Sie stattdessen den Programmnamen verwenden.

**Falsch:**

![Screenshot des Dialogfeld Titels mit der Sicherheitswarnung ](images/mess-warn-image24.png)

In diesem Beispiel identifiziert "Sicherheitswarnung" nicht den Befehl oder das Feature, von dem die Warnung stammt.

-   **Verwenden Sie den Titel nicht, um zu erläutern, wie Sie im Dialog** Feld mit der Main-Anweisung vorgehen sollten.
-   Verwenden Sie die Groß-/Kleinschreibung im [Titel](glossary.md), ohne die Beendigung zu beenden

### <a name="main-instructions"></a>Haupt Anleitung

-   Die Haupt Anweisung für eine Warnung basiert auf dem Entwurfsmuster:



|                                      |                                                                      |
|--------------------------------------|----------------------------------------------------------------------|
| **Muster**<br/>               | **Main-Anweisung**<br/>                                      |
| Bewusstsein<br/>                 | Beschreiben Sie die Bedingung oder das potenzielle Problem.<br/>              |
| Bevorstehendes Problem<br/>          | Beschreiben Sie, was der Benutzer jetzt tun muss.<br/>                   |
| Bestätigung der riskanten Aktion<br/> | Stellen Sie eine Frage, um zu bestimmen, ob der Benutzer den Vorgang fortsetzen möchte.<br/> |



 

-   ![Screenshot einer Benachrichtigung mit geringem Akku ](images/mess-warn-image25.png)
-   In diesem Beispiel ist die Benachrichtigung bei geringer Akku Benachrichtigung eine Warnung, sodass die Bedingung in der Haupt Anweisung beschrieben wird.
-   ![Screenshot der Änderung der Akku sofortige Warnung ](images/mess-warn-image1.png)
-   In diesem Beispiel ist das Dialogfeld "geringe Akkukapazität" ein bevorstehendes Problem, daher wird in der Haupt Anweisung beschrieben, was der Benutzer jetzt tun muss.
-   **Bei der präzisen Verwendung wird nur ein einzelner, kompletter Satz verwendet.** Entfernen Sie die Haupt Anweisung zu den wesentlichen Informationen. Wenn Sie etwas anderes erläutern müssen, verwenden Sie eine ergänzende Anweisung.
-   **Verwenden Sie Wörter wie "Now" und "sofort", wenn der Benutzer sofort agieren muss.** Verwenden Sie diese Wörter nicht, wenn es keine Dringlichkeit gibt.
-   **Wenn Objekte beteiligt sind, geben Sie die vollständigen Namen an.**
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.

### <a name="supplemental-instructions"></a>Ergänzende Anweisungen

-   Die ergänzende Anweisung für eine Warnung basiert auf dem Entwurfsmuster:



|                                      |                                                                                    |
|--------------------------------------|------------------------------------------------------------------------------------|
| **Muster**<br/>               | **Ergänzende Anweisung**<br/>                                            |
| Bewusstsein<br/>                 | Erläutern Sie die Implikation und warum Sie wichtig ist.<br/>                        |
| Bevorstehendes Problem<br/>          | Erläutern Sie die Bedingung und warum Sie wichtig ist.<br/>                          |
| Bestätigung der riskanten Aktion<br/> | Erläutern Sie alle nicht offensichtlichen Gründe, warum der Benutzer möglicherweise nicht fortfahren möchte.<br/> |



 

-   **Wiederholen Sie die main-Anweisung nicht mit etwas anderen Formulierungen.** Lassen Sie stattdessen die ergänzende Anweisung Weg, wenn nicht mehr hinzugefügt werden muss.
-   Verwenden Sie vollständige Sätze, die Groß-/Kleinschreibung und die endinterpunktions Zeichen.

### <a name="commit-buttons"></a>Commit-Schaltflächen

-   Für Warn Dialogfelder basieren die Commit-Schaltflächen auf dem Entwurfsmuster:



|                                      |                                                                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **Muster**<br/>               | **Commit-Schaltflächen**<br/>                                                                                   |
| Bewusstsein<br/>                 | Fast richtig. Verwenden Sie "OK" nicht, da es ein mögliches Problem ist.<br/>                              |
| Bevorstehendes Problem<br/>          | Eine Befehls Schaltfläche oder ein Befehls Link für jede Option oder OK, wenn die Aktion außerhalb des Dialog Felds erfolgt.<br/> |
| Bestätigung der riskanten Aktion<br/> | Ja, Nein.<br/>                                                                                             |



 

-   **Falsch:**
-   ![Screenshot des Warn Dialogfelds mit der Schaltfläche "OK" ](images/mess-warn-image26.png)
-   Probleme sind nicht in Ordnung. verwenden Sie daher stattdessen close.

## <a name="documentation"></a>Dokumentation

Beim Verweis auf Warnungen:

-   Wenn in der Warnung eine Frage gestellt wird, finden Sie eine Warnung nach Ihrer Frage. Andernfalls verwenden Sie die main-Anweisung. Wenn die Frage oder die Haupt Anweisung lang oder ausführlich ist, fassen Sie sie zusammen.
-   Falls erforderlich, können Sie auf ein Warn Dialogfeld als Nachricht verweisen.
-   Formatieren Sie den Text nach Möglichkeit fett formatiert. Andernfalls sollten Sie den Text nur bei Bedarf in Anführungszeichen setzen, um Verwechslungen zu vermeiden.

Beispiel: Klicken Sie in der Meldung möchten **Sie die nicht sicheren Elemente anzeigen?** auf Ja.

 

