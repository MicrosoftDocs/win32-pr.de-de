---
title: Warnmeldungen
description: Eine Warnmeldung ist ein modales Dialogfeld, eine ortsbezogene Nachricht, eine Benachrichtigung oder eine Sprechblase, mit der der Benutzer über eine Bedingung benachrichtigt wird, die in Zukunft zu einem Problem führen kann.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 944c99b546df5fd313ee5bd656db58fafe991d01
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470287"
---
# <a name="warning-messages"></a>Warnmeldungen

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Eine Warnmeldung ist ein modales Dialogfeld, eine ortsbezogene Nachricht, eine Benachrichtigung oder eine Sprechblase, mit der der Benutzer über eine Bedingung benachrichtigt wird, die in Zukunft zu einem Problem führen kann.

![Screenshot einer typischen Warnmeldung](images/mess-warn-image1.png)

Eine typische modale Warnmeldung.

Das grundlegende Merkmal von Warnungen besteht darin, dass sie das Risiko mit sich bringen, eine oder mehrere der folgenden Punkte zu verlieren:

-   Eine wertvolle Ressource, z. B. wichtige Finanzdaten oder andere Daten.
-   Systemzugriff oder -integrität.
-   Datenschutz oder Kontrolle über vertrauliche Informationen.
-   Die Zeit des Benutzers (ein erheblicher Betrag, z. B. 30 Sekunden oder mehr).

Im Gegensatz dazu ist eine Bestätigung ein modales Dialogfeld, in dem gefragt wird, ob der Benutzer mit einer Aktion fortfahren möchte. Einige Arten von Warnungen werden als Bestätigungen angezeigt, und wenn ja, gelten auch die Bestätigungsrichtlinien.

**Hinweis:** Richtlinien im Zusammenhang mit [Dialogfeldern,](win-dialog-box.md) [Bestätigungen,](mess-confirm.md) [Fehlermeldungen](mess-error.md)[Standardsymbole,](vis-std-icons.md) [Benachrichtigungen](mess-notif.md)und [Layout](vis-layout.md) werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Wird der Benutzer über eine Bedingung benachrichtigt, die in Zukunft ein Problem verursachen kann?** Wenn nicht, ist die Nachricht keine Warnung.
-   **Stellt die Benutzeroberfläche einen Fehler oder ein Problem dar, das bereits aufgetreten ist?** Verwenden Sie in diesem Falle stattdessen eine Fehlermeldung.
-   **Führen Benutzer wahrscheinlich eine Aktion aus oder ändern ihr Verhalten als Ergebnis der Nachricht?** Wenn dies nicht der Lage ist, kann der Benutzer durch die Bedingung nicht unterbrochen werden. Daher ist es besser, die Warnung zu unterdrücken.
-   **Ist die Bedingung das direkte Ergebnis einer vom Benutzer initiierten Aktion?** Wenn dies nicht der Fall ist, sollten Sie eine [nicht kritische Ereignisbenachrichtigung](mess-notif.md)verwenden.
-   **Ist die Bedingung eine besondere Bedingung in einem Steuerelement?** Verwenden Sie in diesem Falle stattdessen einen [Balloon.](ctrl-balloons.md)
-   **Ist der Benutzer bereit, eine riskante Aktion auszuführen, um Bestätigungen zu erhalten?** In diesem Falle ist eine Warnung geeignet, wenn die Aktion erhebliche Folgen hat oder nicht einfach rückgängig zu werden ist.
-   **Muss der Benutzer für andere Arten von Warnungen jetzt oder in der unmittelbaren Zukunft handeln?** Zeigen Sie keine Warnungen an, wenn Benutzer weiterhin ohne sofortige Probleme produktiv arbeiten können. Verschieben Sie die Warnung, bis die Bedingung direkter und relevanter ist.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="avoid-overwarning"></a>Vermeiden von Überwarnungen

Wir haben uns in Microsoft Windows-Programmen überwarnt. Das typische Windows Programms enthält Warnungen, die scheinbar überall angezeigt werden, warnungen zu Dingen, die nur eine geringe Bedeutung haben. In einigen Programmen wird fast jede Frage als Warnung dargestellt. Eine Überhärtung bewirkt, dass die Verwendung eines Programms sich wie eine gefährliche Aktivität anfühlt und von wirklich signifikanten Problemen abweicht.

**Falsch:**

![Screenshot einer unnötigen Warnmeldung ](images/mess-warn-image2.png)

Überwarnungen machen Ihr Programm gefährlich und sehen so aus, als ob es von Dern entwickelt wurde.

Das reine Potenzial für Datenverlust oder ein zukünftiges Problem allein reicht nicht aus, um eine Warnung aufzurufen. Darüber hinaus sollten unerwünschte Ergebnisse unerwartet oder unbeabsichtigt sein und nicht einfach korrigiert werden. Andernfalls kann fast jeder Benutzerfehler behoben werden, um zu Datenverlust oder einem potenziellen Problem einer Art zu führen und eine Warnung auszulösen.

### <a name="characteristics-of-good-warnings"></a>Merkmale guter Warnungen

Gute Warnungen:

-   **Risiko einbeziehen.** Gute Warnungen warnen Benutzer vor etwas, das von Bedeutung ist.

**Falsch:**

![Screenshot von "Möchten Sie beenden?" warning ](images/mess-warn-image3.png)

Na und? Bei dieser Bestätigung wird davon ausgegangen, dass Benutzer Programme häufig aus Versehen beenden.

-   **Unmittelbar relevant.** Benutzer müssen sich nicht nur darum kümmern, sie müssen sich jetzt darum kümmern. Benutzer sind in der Regel nicht an Problemen interessiert, die sie möglicherweise später haben, solange sie ihre Arbeit jetzt erledigen können.

**Falsch:**

![Screenshot der Warnung "Akku–niedrig in drei Stunden" ](images/mess-warn-image4.png)

In diesem Fall ist es besser, den Benutzer in drei Stunden zu warnen.

-   **Führen Sie zu einer Aktion.** Es gibt etwas, das Benutzer als Ergebnis der Warnung tun oder beachten müssen. Möglicherweise müssen sie jetzt oder in der unmittelbaren Zukunft eine Aktion ergreifen. Möglicherweise führen sie daher eine Aufgabe anders aus. Die Folge des Ignorierens der Warnung sollte klar sein. Warnungen ohne Aktionen sorgen nur dafür, dass Benutzer paranoid sind.

**Falsch:**

![Screenshot der Warnung "Live Messenger wird ausgeführt" ](images/mess-warn-image5.png)

Warum ist diese Benachrichtigung eine Warnung? Was sollen Benutzer tun (neben der Sorge)?

-   **Dies ist nicht offensichtlich.** Zeigen Sie keine Warnung an, um die offensichtliche Folge einer Aktion anzugeben. Nehmen sie beispielsweise an, dass Benutzer die Konsequenzen verstehen, die sich ergeben, wenn eine Aufgabe nicht abgeschlossen wird.

**Falsch:**

![Screenshot: Möchten Sie den Assistenten beenden? Warnung ](images/mess-warn-image6.png)

Das Abbrechen eines unvollständigen Assistenten bedeutet, dass die Aufgabe nicht abgeschlossen wird... wer wusste?

-   **Tritt selten auf.** Konstante Warnungen werden schnell ineffektiv und ungern. Benutzer konzentrieren sich häufig eher darauf, die Warnung zu entfernen, als das Problem zu beheben.

**Falsch:**

![Screenshot der Warnung "Virussignaturen aktualisieren" ](images/mess-warn-image7.png)

Benutzer konzentrieren sich eher darauf, die Warnung zu entfernen, als das zugrunde liegende Problem zu beheben.

Eine Nachricht, die diese Merkmale nicht aufweist, ist möglicherweise dennoch eine gute Nachricht, keine gute Warnung.

### <a name="determine-the-appropriate-message-type"></a>Bestimmen des geeigneten Nachrichtentyps

Einige Probleme können je nach Schwerpunkt und Ausdruck als Fehler, Warnung oder Information dargestellt werden. Angenommen, eine Webseite kann ein steuerelement ohne Vorzeichen ActiveX basierend auf der aktuellen konfiguration Windows Internet Explorer nicht laden:

-   **Fehler.** "Diese Seite kann kein steuerelement ohne Vorzeichen ActiveX laden." (Wird als vorhandenes Problem bezeichnet.)
-   **Warnung.** "Diese Seite verhält sich möglicherweise nicht wie erwartet, da Windows Internet Explorer nicht zum Laden nicht signierter ActiveX-Steuerelemente konfiguriert ist." oder "Zulassen, dass diese Seite ein nicht signiertes ActiveX-Steuerelement installiert? Wenn Sie dies aus nicht vertrauenswürdigen Quellen tun, kann dies ihrem Computer schaden." (Beide werden als Bedingungen bezeichnet, die zukünftige Probleme verursachen können.)
-   **Informationen.** "Sie haben Windows Internet Explorer so konfiguriert, dass nicht signierte ActiveX-Steuerelemente blockiert werden." (Als Faktenhinweis formuliert.)

**Um den geeigneten Nachrichtentyp zu bestimmen, konzentrieren Sie sich auf den wichtigsten Aspekt des Problems, den Benutzer kennen müssen oder auf den sie reagieren müssen.** Wenn ein Problem den Benutzer daran hindert, fortzufahren, sollten Sie ihn in der Regel als Fehler darstellen. Wenn der Benutzer fortfahren kann, stellen Sie ihn als Warnung dar. Erstellen Sie die [Hauptanweisung](text-ui.md) oder einen anderen entsprechenden Text basierend auf diesem Fokus, und wählen Sie dann ein Symbol[(Standard](vis-std-icons.md) oder anderweitig) aus, das dem Text entspricht. Der Hauptanweisungstext und die Symbole sollten immer übereinstimmen.

### <a name="be-specific"></a>Spezifisch sein

Warnungen sind überzeugender, wenn die folgenden Informationen spezifisch und eindeutig sind:

-   Die Quelle der Warnung.
-   Die spezifische Bedingung und das potenzielle Problem.
-   Was der Benutzer tun sollte.
-   Was geschieht, wenn der Benutzer nichts tut?

**Falsch:**

![Screenshot der warnungsgefährdungsgefährdten Warnung vor erheblichem Risiko ](images/mess-warn-image8.png)

Was ist das potenzielle Problem in diesem Beispiel? Was soll der Benutzer tun, abgesehen davon, dass der Projektor nicht über das Netzwerk verwendet wird? Ohne spezifischere Informationen kann der Benutzer nicht fortfahren.

**Richtig:**

![Screenshot: Warnung vor Problem und Folgen ](images/mess-warn-image9.png)

In diesem Beispiel sind das Problem und die Konsequenzen klar.

Manchmal besteht ein legitimes potenzielles Problem, benutzer zu informieren, aber die Lösung und die Konsequenzen sind nicht sicher. Anstatt eine ungenaue Warnung zu geben, sollten Sie spezifisch sein, indem Sie die wahrscheinlichsten Informationen oder das gängigste Beispiel geben.

**Richtig:**

![Screenshot: Netzwerkfehlerwarnung und Lösungen ](images/mess-warn-image10.png)

In diesem Beispiel wird die Warnung spezifisch gemacht, indem die wahrscheinlichste Lösung zur Verfügung gestellt wird.

Verwenden Sie in solchen Fällen jedoch Formulierungen, die darauf hindeutet, dass es andere Möglichkeiten gibt. Andernfalls können Benutzer verfehlt werden.

**Falsch:**

![Screenshot der Netzwerkkabel-Entkabelungswarnung ](images/mess-warn-image11.png)

**Richtig:**

![Screenshot des Kabels ist möglicherweise nicht angeschlossen ](images/mess-warn-image12.png)

Im falschen Beispiel sind Benutzer verwirrend, wenn das Kabel eindeutig angeschlossen ist.

**Wenn Sie nur zwei Dinge tun...**

1. Nicht überwarnen. Beschränken Sie Warnungen auf Bedingungen, die risikenind und sofort relevant, umsetzbar, nicht offensichtlich und selten sind. Entfernen oder umformulieren Sie andernfalls die Nachricht.

2. Geben Sie spezifische, nützliche Informationen an.

## <a name="usage-patterns"></a>Verwendungsmuster

Warnungen haben mehrere Verwendungsmuster:




| | | <strong>Bewusstsein</strong><br /> Machen Sie den Benutzer auf eine Bedingung oder ein potenzielles Problem aufmerksam, aber der Benutzer muss jetzt möglicherweise nichts tun. <br /> | <img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br /><img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br /><img src="images/mess-warn-image15.png" alt="Screen shot of 'caps-lock-is-on' warning " /><br /><img src="images/mess-warn-image16.png" alt="Screen shot of 'TPM-not-found' warning " /><br /> Beispiele für Warnungen zu Bewusstsein.<br /> Warnungen zu Bewusstseinswarnungen haben die folgende Darstellung: <br /><ul><li><strong>Hauptanweisung:</strong> Beschreiben Sie die Bedingung oder das potenzielle Problem.</li><li><strong>Zusätzliche Anweisung:</strong> Erläutern Sie die Implikation und warum sie wichtig ist.</li><li><strong>Commitschaltflächen:</strong> Schließen.</li></ul> | | <strong>Fehlerschutz</strong><br /> Machen Sie den Benutzer auf Informationen aufmerksam, die ein Problem verhindern können, insbesondere wenn Sie Entscheidungen treffen. <br /> | Fehlerschutzwarnungen werden am besten mit einem symbol für eine warnungsbasierte Warnung und einem erläuternden Text angezeigt. <br /><img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br /><img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br /> Beispiele für Fehlerschutzwarnungen.<br /> | | <strong>Bevorstehendes Problem</strong><br /> Der Benutzer muss jetzt etwas tun, um ein bevorstehendes Problem zu verhindern. <br /> | <img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br /> Ein Beispiel für eine Warnung zu einem bevorstehenden Problem.<br /> Warnungen zu einem bevorstehenden Problem haben die folgende Darstellung: <br /><ul><li><strong>Hauptanweisung:</strong> Beschreiben Sie, was der Benutzer jetzt tun muss.</li><li><strong>Zusätzliche Anweisung:</strong> Erläutern Sie die Bedingung und deren Bedeutung.</li><li><strong>Commitschaltflächen:</strong> Eine Befehlsschaltfläche oder ein Befehlslink für jede Option oder OK, wenn die Aktion außerhalb des Dialogfelds erfolgt.</li></ul> | | <strong>Bestätigung riskanter Aktionen</strong><br /> Vergewissern Sie sich, dass der Benutzer mit einer Aktion fortfahren möchte, die ein gewisses Risiko auf sich hat und nicht einfach rückgängig gemacht werden kann. <br /> | <img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br /> Ein Beispiel für die Bestätigung riskanter Aktionen.<br /> Bestätigungen für riskante Aktionen haben die folgende Darstellung: <br /><ul><li><strong>Hauptanweisung:</strong> Stellen Sie eine Frage, um zu bestimmen, ob der Benutzer fortfahren möchte.</li><li><strong>Zusätzliche Anweisung:</strong> Erläutern Sie alle nicht offensichtlichen Gründe, warum der Benutzer möglicherweise nicht fortfahren möchte.</li><li><strong>Commitschaltflächen:</strong> Ja, Nein.</li></ul>Richtlinien zu diesem Muster finden Sie unter <a href="mess-confirm.md">Bestätigungen.</a> <br /> | 




 

## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

-   **Wählen Sie die Präsentationsbenutzeroberfläche basierend auf dem Informationstyp aus:**



| Benutzeroberfläche  | Am besten verwendet für |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Modale Dialogfelder<br/> | Kritische Warnungen (einschließlich Bestätigungen), auf die Benutzer jetzt reagieren müssen.<br/>                                                 |
| Direkt<br/>           | Informationen, die ein Problem verhindern könnten, insbesondere, wenn Benutzer Entscheidungen treffen.<br/>                                         |
| Banner<br/>            | Informationen, die ein Problem verhindern können, insbesondere im Zusammenhang mit dem Abschließen einer Aufgabe.<br/>                                     |
| Benachrichtigungen<br/>      | Wichtige Ereignisse oder Status, die zumindest vorübergehend ignoriert werden können.<br/>                                              |
| Ballons<br/>           | Ein Steuerelement befindet sich in einem Zustand, der die Eingabe beeinflusst. Dieser Zustand ist wahrscheinlich unbeabsichtigt, und der Benutzer erkennt möglicherweise nicht, dass die Eingabe betroffen ist.<br/> |



 

-   **Für modale Dialogfelder:**
    -   **Verwenden Sie Taskdialoge, wenn dies angemessen ist, um ein konsistentes Aussehen und Layout zu erzielen.** Taskdialogfelder erfordern Windows Vista oder höher, sodass sie nicht für frühere Versionen von Windows.
    -   **Zeigt nur eine Warnmeldung pro Bedingung an.** Zeigen Sie z. B. eine einzelne Warnung an, die eine Bedingung vollständig erklärt, anstatt sie nach und nach pro Nachricht zu beschreiben. Das Anzeigen einer Sequenz von Warndialogfeldern für eine einzelne Bedingung ist verwirrend und störend.
    -   **Zeigen Sie eine Warnung nicht mehr als einmal pro Bedingung an.** Konstante Warnungen werden schnell ineffektiv und lästig. Benutzer konzentrieren sich häufig eher darauf, die Warnung zu beheben, als das Problem zu beheben. Wenn Sie wiederholt bei einer einzelnen Bedingung warnen müssen, verwenden Sie [progressive Eskalation.](mess-notif.md)
-   **Warnungen werden nicht mit einem Soundeffekt oder Signalton begleitet.** Dies ist nicht erforderlich.
    -   **Ausnahme:** Wenn der Benutzer sofort reagieren muss, können Sie einen Soundeffekt verwenden.

### <a name="icons"></a>Symbole

-   Platzieren Sie kein Warnsymbol in der Titelleiste eines Dialogfelds.
-   **Verwenden Sie ein Warnsymbol.** Ausnahmen:
    -   Wenn die Warnung für ein Feature mit einem Symbol gilt, können Sie das Featuresymbol mit einer Warnüberlagerung verwenden.

        **Richtig:**

        ![Screenshot des Sperrsymbols mit Überlagerung des Warnsymbols ](images/mess-warn-image21.png)

        In diesem Beispiel verfügt das Featuresymbol über eine Warnüberlagerung.

-   Legen Sie für modale Dialogfelder mit einer Fußnote mit Einer Warnung das Warnsymbol in die Fußnote und nicht in den Inhaltsbereich.

    **Richtig:**

    ![Screenshot des Warnsymbols in der Fußnote des Dialogfelds ](images/mess-warn-image22.png)

    In diesem Beispiel verfügt die Fußnote über das Warnsymbol.

Weitere Richtlinien und Beispiele finden Sie unter [Standardsymbole.](vis-std-icons.md)

### <a name="dont-show-this-message-again"></a>Diese Meldung nicht mehr anzeigen

-   **Wenn für ein Warndialogfeld diese Option benötigt wird, sollten Sie die Warnung und deren Häufigkeit erneut überprüfen.** Wenn sie alle Merkmale einer guten Warnung aufweist (risikobezieht und sofort relevant, umsetzbar, nicht offensichtlich und selten ist), sollte es für Benutzer nicht sinnvoll sein, sie zu unterdrücken.

Weitere Richtlinien finden Sie unter [Dialogfelder](win-dialog-box.md).

### <a name="progressive-disclosure"></a>Schrittweise Offenlegung

-   Wenn Sie erweiterte Informationen in eine **Warnmeldung einschlussen müssen,** zeigen Sie sie mithilfe von Schaltflächen für die progressive Offenlegung an (z. B. "Details anzeigen"). Dadurch wird die Warnung für die typische Verwendung vereinfacht. Blenden Sie die benötigten Informationen nicht aus, da Benutzer sie möglicherweise nicht finden.
-   **Verwenden Sie nur dann "Details anzeigen", wenn es wirklich weitere Details gibt.** Erstellen Sie die vorhandenen Informationen nicht einfach in einem anderen Format.

Bezeichnungsrichtlinien finden Sie unter [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).

### <a name="default-values"></a>Standardwerte

-   **Wählen Sie die sicherste, am wenigsten destruktive oder sicherste Antwort als Standard aus.**

## <a name="text"></a>Text

### <a name="general"></a>Allgemein

-   **Entfernen Sie redundanten Text.** Suchen Sie in Titeln, Hauptanweisungen, ergänzenden Anweisungen, Inhaltbereichen, Befehlslinks und Commitschaltflächen. Lassen Sie im Allgemeinen vollständigen Text in Anweisungen und interaktiven Steuerelementen, und entfernen Sie alle Redundanzen von den anderen Stellen.
-   **Verwenden Sie nicht die Begriffe "Warnung" oder "Vorsicht" im Text.** Bei [ordnungsgemäßer Verwendung](vis-std-icons.md)gibt das Warnsymbol ausreichend an, dass Benutzer mit Vorsicht vorgehen müssen.

**Falsch:**

![Screenshot der unnötigen Verwendung von Warnungen im Text ](images/mess-warn-image23.png)

In diesem Beispiel ist der Begriff "Warnung" nicht erforderlich.

### <a name="titles"></a>Titel

-   **Verwenden Sie den Titel, um den Befehl oder das Feature zu identifizieren, von dem die Warnung stammt.** Ausnahmen:
    -   Wenn eine Warnung von vielen verschiedenen Befehlen angezeigt wird, sollten Sie stattdessen den Programmnamen verwenden.
    -   Wenn dieser Titel redundant oder verwirrend mit der Main-Anweisung wäre, verwenden Sie stattdessen den Programmnamen.

**Falsch:**

![Screenshot des Dialogfeldtitels "Sicherheitswarnung" ](images/mess-warn-image24.png)

In diesem Beispiel identifiziert "Sicherheitswarnung" nicht den Befehl oder das Feature, von dem die Warnung stammt.

-   **Verwenden Sie den Titel nicht, um zu erläutern,** was im Dialog zu tun ist, der der Zweck der Hauptanweisung ist.
-   Verwenden [Sie die Groß-/Groß-/Formatvorlage,](glossary.md)ohne die Interpunktion zu beenden.

### <a name="main-instructions"></a>Hauptanweisungen

-   Die Hauptanweisung für eine Warnung basiert auf ihrem Entwurfsmuster:



| Muster                        | Main-Anweisung                                               |
|--------------------------------------|----------------------------------------------------------------------|
| Bewusstsein<br/>                 | Beschreiben Sie die Bedingung oder das potenzielle Problem.<br/>              |
| Bevorstehendes Problem<br/>          | Beschreiben Sie, was der Benutzer jetzt tun muss.<br/>                   |
| Bestätigung riskanter Aktionen<br/> | Stellen Sie eine Frage, um zu bestimmen, ob der Benutzer fortfahren möchte.<br/> |



 

-   ![Screenshot einer Benachrichtigung mit wenig Akku ](images/mess-warn-image25.png)
-   In diesem Beispiel ist die Benachrichtigung über niedrige Akkukapazität eine Benachrichtigungswarnung, sodass die Hauptanweisung die Bedingung beschreibt.
-   ![Screenshot der sofortigen Warnung zum Ändern des Akkus ](images/mess-warn-image1.png)
-   In diesem Beispiel ist das Dialogfeld "Niedrige Akkukapazität" ein bevorstehendes Problem, sodass in der Hauptanweisung beschrieben wird, was der Benutzer jetzt tun muss.
-   **Seien Sie präzise, verwenden Sie nur einen einzelnen vollständigen Satz.** Entfernt die Hauptanweisung auf die grundlegenden Informationen. Wenn Sie mehr erklären müssen, verwenden Sie eine zusätzliche Anweisung.
-   **Verwenden Sie Wörter wie "jetzt" und "sofort", wenn der Benutzer sofort handeln muss.** Verwenden Sie diese Wörter nicht, wenn es keine Dringendkeit gibt.
-   **Seien Sie spezifisch, wenn Objekte beteiligt sind, geben Sie ihre vollständigen Namen an.**
-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)

### <a name="supplemental-instructions"></a>Zusätzliche Anweisungen

-   Die ergänzende Anweisung für eine Warnung basiert auf ihrem Entwurfsmuster:



| Muster            | Ergänzende Anweisung                                            |
|--------------------------------------|------------------------------------------------------------------------------------|
| Bewusstsein<br/>                 | Erläutern Sie die Implikation und warum sie wichtig ist.<br/>                        |
| Bevorstehendes Problem<br/>          | Erläutern Sie die Bedingung und deren Bedeutung.<br/>                          |
| Bestätigung riskanter Aktionen<br/> | Erläutern Sie alle nicht offensichtlichen Gründe, warum der Benutzer möglicherweise nicht fortfahren möchte.<br/> |



 

-   **Wiederholen Sie die Hauptanweisung nicht mit etwas anderen Formulierungen.** Lassen Sie stattdessen die zusätzliche Anweisung weg, wenn nicht mehr hinzugefügt werden muss.
-   Verwenden Sie vollständige Sätze, Groß- und Groß-/Endzeichen im Satzstil.

### <a name="commit-buttons"></a>Commitschaltflächen

-   Bei Warndialogfeldern basieren die Commitschaltflächen auf dem Entwurfsmuster:



| Muster               | Commitschaltflächen        |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Bewusstsein<br/>                 | Fast richtig. Verwenden Sie nicht OK, da dies darauf hindeutet, dass potenzielle Probleme in Ordnung sind.<br/>                              |
| Bevorstehendes Problem<br/>          | Eine Befehlsschaltfläche oder ein Befehlslink für jede Option oder OK, wenn die Aktion außerhalb des Dialogfelds erfolgt.<br/> |
| Bestätigung riskanter Aktionen<br/> | Ja, Nein.<br/>                                                                                             |



 

-   **Falsch:**
-   ![Screenshot des Dialogfelds "Warnung" mit der Schaltfläche "OK" ](images/mess-warn-image26.png)
-   Probleme sind nicht in Ordnung, verwenden Sie stattdessen Schließen.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Warnungen:

-   Wenn die Warnung eine Frage stellt, verweisen Sie auf eine Warnung durch ihre Frage. Verwenden Sie andernfalls die main-Anweisung. Wenn die Frage oder die Hauptanweisung lang oder ausführlich ist, fassen Sie sie zusammen.
-   Bei Bedarf können Sie auf ein Warnungsdialogfeld als Meldung verweisen.
-   Formatieren Sie den Text nach Möglichkeit fett. Andernfalls setzen Sie den Text nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Klicken Sie in der Meldung Möchten Sie **die unsicheren Elemente anzeigen?** auf Ja.

 

