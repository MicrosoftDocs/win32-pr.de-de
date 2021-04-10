---
title: Befehlsverknüpfungen
description: Mit Befehls Verknüpfungen wählen Benutzer eine einzelne Antwort auf eine Haupt Anweisung aus, und auf diese Weise fahren Sie mit dem nächsten Schritt in einer Aufgabe fort.
ms.assetid: a77819b1-9a32-4468-94fb-3f73a469fb81
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 29031b4456950db6ceff30d75b354dece92c5897
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103761289"
---
# <a name="command-links"></a>Befehlsverknüpfungen

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mit Befehls Verknüpfungen wählen Benutzer eine einzelne Antwort auf eine Haupt Anweisung aus, und auf diese Weise fahren Sie mit dem nächsten Schritt in einer Aufgabe fort.

Befehls Verknüpfungen verfügen über eine saubere, einfache Darstellung, die beschreibende Bezeichnungen zulässt. Sie werden entweder mit einem Standardpfeil oder einem benutzerdefinierten Symbol und einer optionalen Zusatzerklärung angezeigt.

![Screenshot eines typischen Befehls Link Dialogfelds ](images/ctrl-command-links-image1.png)

Ein typischer Satz von Befehls Verknüpfungen.

Befehls Verknüpfungen ähneln options [Feldern insofern,](ctrl-radio-buttons.md) als Sie verwendet werden, um aus einem Satz von sich gegenseitig ausschließenden, zusammenhängenden Optionen auszuwählen. Wie Options Felder werden Befehls Verknüpfungen immer in den Sätzen, nie einzeln, angezeigt. In der Darstellung weisen Befehls Verknüpfungen das vereinfachte Aussehen ähnlich wie reguläre [Verknüpfungen](ctrl-links.md)auf, ohne einen Frame oder einen anderen [starken Klick zu](glossary.md)bieten. Befehls Verknüpfungen sind auch mit [Befehls](ctrl-command-buttons.md)Schaltflächen vergleichbar, da Sie als Standard Befehls Schaltfläche dienen können und Ihnen eine Zugriffstaste zugewiesen werden kann. Wenn Sie auf die Schaltflächen " [Commit](glossary.md)" klicken, schließen Sie entweder das Fenster (für Dialogfelder), oder fahren Sie mit der nächsten Seite fort (für Assistenten und Seiten Flüsse).

> [!Note]  
> Richtlinien, die sich auf [Links](ctrl-links.md) und [Layout](vis-layout.md) beziehen, werden in separaten Artikeln dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Gibt es die Optionen, die auf die Haupt Anweisung Antworten und mit dem Hauptzweck des Fensters oder der Seite verknüpft sind?** Müssen Benutzer darauf reagieren, um etwas anderes zu tun, als einfach nur zu einer anderen Seite zu navigieren? Andernfalls verwenden Sie ein anderes Steuerelement, z. b. Befehls Schaltflächen oder Links. Befehls Verknüpfungen sind bei sekundären oder optionalen Optionen oder reinen Navigationsmöglichkeiten nicht geeignet.

    ![Screenshot eines Personalisier enden System Steuerungs Elements ](images/ctrl-command-links-image2.png)

    Das Element der Personalisierungs-Systemsteuerung sieht so aus, als ob es Befehls Verknüpfungen verwendet, die Optionen sind reguläre Verknüpfungen, da diese [Hub-Seite](winenv-ctrl-panels.md) für reine Navigation vorgesehen ist.

-   **Wird das Steuerelement verwendet, um eine Antwort aus einem Satz von sich gegenseitig ausschließenden Antworten auszuwählen?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Verwenden Sie Befehls Schaltflächen oder Links, damit Benutzer einzelne Befehle auswählen können.
-   **Wird in Dialogfeldern das Fenster durch Klicken auf das Steuerelement geschlossen?** Wenn dies nicht der Wert ist, verwenden Sie ein Steuerelement, für das das Schließen des Fensters nicht erforderlich ist, z.b. Options Felder, Befehls Schaltflächen oder Links

    **Falsch:**

    ![Screenshot des Dialog Felds "Firewalleinstellungen im Registerkarten Format" ](images/ctrl-command-links-image3.png)

    Befehls Verknüpfungen können nicht in Eigenschaften Fenstern oder Dialogfeldern mit Registerkarten verwendet werden, da das Fenster durch Klicken auf das Steuerelement geschlossen wird

-   **Wenn Sie Assistenten und Seiten Flüsse ausführen, klicken Sie ohne Verpflichtung auf zur nächsten Seite.** Verwenden Sie keine Befehls Verknüpfungen zum Ausführen eines Commit für eine Aufgabe. Verwenden Sie stattdessen Commit-Schaltflächen. Da Befehls Verknüpfungen wie Links Aussehen und Benutzer innerhalb eines Seiten Flusses Verknüpfungen mit der Navigation verknüpfen, sind Verknüpfungen für [Commit-Seiten](glossary.md) nicht geeignet, da Benutzer immer in der Lage sein sollten, die Sicherung durchzuführen.
-   **Gibt es für Assistenten und Seiten Flüsse andere Seiten, die Befehls Verknüpfungen verwenden?** Wenn dies der Fall ist und alle anderen Faktoren gleich sind, werden Befehls Verknüpfungen für die Konsistenz zwischen den Seiten bevorzugt.
-   **Ist die Anzahl der Antworten zwischen zwei und fünf?** Es darf nie ein einziger Befehls Link vorhanden sein. Da es sich bei den Befehls Verknüpfungen um große Steuerelemente handelt und der verwendete Bildschirmbereich proportional zur Anzahl der Optionen ist, sollten Sie die Anzahl der Antworten auf höchstens fünf Zeichen beschränken. Verwenden Sie für sechs oder mehr Optionen Options Felder, reguläre Links oder eine [Listenansicht](ctrl-list-views.md)mit einfacher Auswahl.

    ![Screenshot des Dialog Felds mit der Liste der Befehle ](images/ctrl-command-links-image4.png)

    In diesem Beispiel verwendet die Funktion "AutoPlay" in Microsoft Windows eine Listenansicht.

-   **Ist eine Kombination aus Options Feldern und der Schaltfläche "Commit" eine bessere Wahl?** Options Felder sind eine bessere Wahl, wenn Folgendes zutrifft:
    -   **Es gibt eine starke Standardoption, die die meisten Benutzer auswählen können.** Es ist weniger wahrscheinlich, dass Benutzer eine Standard Options Schaltfläche ändern, als dies ein Standard Befehls Link ist, insbesondere in einem Assistenten, bei dem die Benutzer daran gewöhnt sind, die entsprechenden Standardwerte zu akzeptieren. Auf der anderen Seite sind Befehls Verknüpfungen eine bessere Wahl, wenn Sie Benutzer auffordern möchten, eine explizite Auswahl zu treffen.
    -   **Benutzer müssen mit den Optionen interagieren (möglicherweise, um weitere Informationen anzuzeigen), bevor Sie eine Entscheidung treffen.** Wenn Sie z. b. ein Optionsfeld auswählen, wird möglicherweise eine Beschreibung der Option angezeigt.

        ![Screenshot des Dialog Felds mit Options Feldern ](images/ctrl-command-links-image5.png)

        In diesem Beispiel wird durch Auswählen eines Options Felds eine Beschreibung der Option angezeigt.

    -   **Auf der Seite sind sekundäre oder zugehörige Optionen vorhanden.** Befehls Verknüpfungen neigen dazu, die Seite zu dominieren, sodass alles leicht übersehen wird. Außerdem ist es nicht möglich, sekundäre Optionen auszuwählen, sobald auf einen Befehls Link geklickt wurde.

        **Falsch:**

        ![Screenshot des Dialog Felds mit gemischten Steuerelementen ](images/ctrl-command-links-image6.png)

        In diesem Beispiel gibt es zwei verschiedene Möglichkeiten, auf die Haupt Anweisung zu reagieren. Ein Befehls Link wurde nicht für die erste Antwort verwendet, da es schwierig wäre, sekundäre Optionen auszuwählen.

        **Richtig:**

        ![Screenshot des Dialog Felds mit denselben Steuerelementen ](images/ctrl-command-links-image7.png)

        In diesem Beispiel werden die Antworten durch Options Felder klarer, während Benutzer gleichzeitig sekundäre Optionen auswählen können.

-   **Wäre eine Gruppe von Commit-Schaltflächen für Dialogfelder eine bessere Wahl?** Befehls Verknüpfungen funktionieren besser, wenn die Optionen längere, ausführlichere Antworten und zusätzliche Erläuterungen erfordern, aber eine Gruppe von Commit-Schaltflächen ist eine bessere Wahl, wenn es einige einfache Optionen gibt.

    **Falsch:**

    ![Screenshot des Dialog Felds mit "Speichern" und "nicht speichern" ](images/ctrl-command-links-image8.png)

    Wenn Sie in diesem Beispiel Befehls Verknüpfungen für einfache Befehle verwenden, wird das Dialogfeld unnötig kompliziert.

    **Richtig:**

    ![Screenshot mit einem Dialogfeld mit den Schaltflächen "Speichern", "nicht speichern" und "Abbrechen".](images/ctrl-command-links-image9.png)

    In diesem Beispiel wird die Verwendung einfacher Commit-Schaltflächen direkt zum Punkt angezeigt.

    Selbsterklärende Befehls Verknüpfungen sind jedoch immer besser geeignet, wenn Text verwendet wird, um Commit-Schaltflächen zu erläutern.

    **Falsch:**

    ![Screenshot des Dialog Felds mit unnötigem Text ](images/ctrl-command-links-image10.png)

    In diesem Beispiel wird Text verwendet, um die Commit-Schaltflächen zu erläutern.

    **Richtig:**

    ![Screenshot von Bezeichnungen, die keinen Text mehr benötigen ](images/ctrl-command-links-image11.png)

    In diesem Beispiel sind die Befehls Verknüpfungen selbsterklärend.

> [!Note]  
> Für Befehls Verknüpfungen ist Windows Vista oder höher erforderlich, sodass Sie sich nicht für frühere Versionen von Windows eignen. Sie können reguläre Verknüpfungen als Ersatz verwenden.

 

![Screenshot der regulären Verknüpfungen mit Symbolen und Text ](images/ctrl-command-links-image12.png)

In diesem Beispiel werden reguläre Verknüpfungen mit einem Symbol und eine ergänzende Erklärung als Ersatz für Befehls Verknüpfungen in Windows XP verwendet.

## <a name="design-concepts"></a>Entwurfskonzepte

Nur weil Befehls Verknüpfungen es Ihnen ermöglichen, aussagekräftigere Bezeichnungen zu verwenden, bedeutet dies nicht, dass Sie dies tun sollten. Betrachten Sie das folgenden Beispiel:

**Falsch:**

![Screenshot des Dialog Felds mit zu viel Text ](images/ctrl-command-links-image13.png)

Dieses Dialogfeld ist äußerst übermittelt.

In diesem Dialogfeld wird eine einfache Frage gestellt, und es wird unnötigerweise mit dem Text des Befehls Links erschwert. Benutzer möchten nicht den gesamten Text für solche einfachen Fragen lesen.

Wir können dieses Dialogfeld vereinfachen, indem Sie drei Befehls Link Richtlinien anwenden:

-   **Verwenden Sie keine ergänzende Erklärung, bei der es sich um eine verfassen Anpassung des Befehls Links handelt.** Verwenden Sie eine ergänzende Erläuterung nur dann, wenn Sie keinen Befehls Link selbsterklärend erstellen können. Das Bereitstellen einer ergänzenden Erklärung für einen Befehls Link bedeutet nicht, dass Sie Sie für alle Befehle bereitstellen müssen.
-   **Wählen Sie das sicherste (um den Verlust von Daten oder den System Zugriff zu verhindern) und die sicherste Antwort als Standard aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequeme Antwort aus.
-   **Geben Sie eine explizite Schaltfläche Abbrechen an.** Verwenden Sie für diesen Zweck keinen Befehls Link.

Durch die Anwendung dieser Richtlinien können wir die unnötigen ergänzenden Erklärungen beseitigen, die standardmäßige Antwort auf den Standardwert festlegen und eine explizite Schaltfläche "Abbrechen" bereitstellen.

**Besserer**

![Screenshot des Dialog Felds mit Befehlen und Bezeichnungen ](images/ctrl-command-links-image14.png)

Eine verbesserte Version mit einfacheren Befehls Verknüpfungen.

Obwohl es zutrifft, dass diese Version nicht explizit erklärt, dass das Speichern als Verlust gezählt wird, ändern sich nur wenige Benutzer ihre Entscheidung anhand dieser Informationen, sodass dies ein guter Kompromiss ist.

Dieses Dialogfeld kann sogar noch besser erstellt werden, indem Sie analysieren, ob Befehls Verknüpfungen sogar das richtige Steuerelement sind, das in diesem Fall verwendet werden soll. Commit-Schaltflächen sind tatsächlich eine bessere Wahl, da längere, ausführlichere Antworten nicht benötigt werden.

**Best**

![Screenshot des Dialog Felds mit Commit-Schaltflächen ](images/ctrl-command-links-image15.png)

Die richtige Version verwendet Commit-Schaltflächen, um direkt zum Punkt zu gelangen.

Befehls Verknüpfungen haben viele Vorteile, aber wenn Sie unklugerweise verwendet werden, führen Sie zu einer über-Kommunikation. Verwenden Sie für Dialogfelder zunächst die Option Commit-Schaltflächen, und verwenden Sie nur die Befehls Verknüpfungen, wenn Commit-Schaltflächen den Auftrag nicht gut ausführen

**Bei entsprechender Verwendung sollten Befehls Verknüpfungen Ihre Benutzeroberfläche vereinfachen und verdeutlichen.** Wenn die Ergebnisse das Gegenteil sind, nehmen Sie einen Schritt zurück, überprüfen Sie die Alternativen, und konzentrieren Sie sich auf das, was Sie wirklich benötigen, um zu kommunizieren.

**Wenn Sie nur eine Aktion ausführen...** Verwenden Sie keine Befehls Verknüpfungen, um die Kommunikation zu überschreiten. Befehls Verknüpfungen sollten die Kommunikation vereinfachen und verdeutlichen und Sie nicht komplizierter machen.

## <a name="usage-patterns"></a>Verwendungsmuster

Befehls Verknüpfungen weisen mehrere Verwendungs Muster auf:



|                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Seiten Antworten** Befehls Verknüpfungen werden verwendet, um auf die Haupt Anweisung zu Antworten und zur nächsten Seite zu gelangen.    | mit diesem Muster ersetzen die Befehls Verknüpfungen die Schaltfläche "weiter", aber es gibt noch eine Schaltfläche "Abbrechen".<br/>Seiten Antworten impliziert keine Verpflichtung. Da Befehls Verknüpfungen wie Links Aussehen und Benutzer innerhalb eines Seiten Flusses Verknüpfungen mit der Navigation verknüpfen, sind Verknüpfungen für Commit-Seiten nicht geeignet. Benutzer sollten immer in der Lage sein, Sie zu sichern. <br/> ![Screenshot, der das Dialogfeld "Verbindung mit dem Internet herstellen" mit den Befehls Verknüpfungen "drahtlos", "Breitband (PPPoE)" und "Einwähl" anzeigt.](images/ctrl-command-links-image16.png)<br/>In diesem Beispiel werden Befehls Verknüpfungen verwendet, um beschreibende Antworten auf die main-Anweisung zu geben. Obwohl Options Felder hier verwendet werden können, ermöglichen Befehls Verknüpfungen Benutzern, mit einem einzigen Mausklick zu antworten.<br/> |
| **Dialog Feld Antworten** Befehls Verknüpfungen werden verwendet, um auf die Haupt Anweisung zu Antworten und das Dialogfeld zu schließen.  | bei diesem Muster ersetzen die Befehls Verknüpfungen die Commit-Schaltflächen (z. b. OK), aber es gibt immer noch eine Schaltfläche "Abbrechen".<br/>Anders als bei Seiten Flüssen gibt es keine Möglichkeit, eine auf einem Dialogfeld basierende Antwort zu sichern, sobald Sie erstellt wurde. Folglich implizieren Dialogfeld-Befehls Verknüpfungen die Zusage. <br/> ![Screenshot des Dialog Felds mit Befehls Verknüpfungen ](images/ctrl-command-links-image17.png)<br/>In diesem Beispiel werden Befehls Verknüpfungen verwendet, um beschreibende Antworten auf die main-Anweisung zu geben. Die Options Felder können hier verwendet werden. mit den Befehls Verknüpfungen können Benutzer jedoch mit einem einzigen Mausklick auswählen.<br/>                                                   |
| **Ausführliche Antworten** Eine Seite oder Dialogfeld Antwort, die ausführliche Informationen enthält.                          | Gelegentlich benötigen Benutzer ausführlichere Informationen, um Ihre Antwort auszuwählen. <br/> ![Screenshot des Dialog Felds "Datei kopieren" und Miniaturansichten ](images/ctrl-command-links-image18.png)<br/> In diesem Beispiel werden ausführliche Befehls Verknüpfungen verwendet, damit Benutzer fundierte Entscheidungen treffen können. Die Miniaturansichten und Dateidetails helfen Benutzern bei der Entscheidung.<br/>                                                                                                                                                                                                                                                                                                         |



 

## <a name="guidelines"></a>Richtlinien

### <a name="interaction"></a>Interaktion

-   **Zeigen Sie einen ausgelasteten Zeiger an, wenn das Ergebnis des Klickens auf einen Befehls Link nicht sofort ist.** Ohne Feedback können Benutzer davon ausgehen, dass das Klicken nicht durchgeführt wurde, und dann erneut auf klicken.

### <a name="presentation"></a>Präsentation

-   **Befehls Verknüpfungen sollten immer in einem Satz von zwei oder mehr vorhanden sein.** Logisch, es gibt keinen Grund, eine Frage zu stellen, die nur eine Antwort hat.

    **Falsch:**

    ![Screenshot des Dialog Felds mit einem Befehls Link ](images/ctrl-command-links-image19.png)

    In diesem Beispiel sieht das Dialogfeld so aus, als würde dem Benutzer eine Auswahl angeboten, aber es gibt nur eine Anweisung. Dies sollte stattdessen ein Informations Dialogfeld sein.

-   **Präsentieren Sie zuerst die am häufigsten verwendeten Befehls Verknüpfungen.** Die resultierende Reihenfolge sollte ungefähr der Wahrscheinlichkeit der Verwendung, aber auch eines logischen Flows entsprechen.
    -   **Ausnahme:** Befehls Verknüpfungen, die zu allen Aufgaben führen, sollten zuerst platziert werden.
-   **Geben Sie eine explizite Schaltfläche Abbrechen an.** Verwenden Sie für diesen Zweck keinen Befehls Link. Häufig bemerken Benutzer, dass Sie keine Aufgabe ausführen möchten. Wenn Sie einen Befehls Link zum Abbrechen verwenden, müssen Benutzer alle Befehls Verknüpfungen sorgfältig lesen, um zu bestimmen, welches der Abbruch bedeutet. Durch eine explizite Schaltfläche "Abbrechen" können Benutzer eine Aufgabe effizient abbrechen.

    **Falsch:**

    ![Screenshot des Dialog Felds mit dem Link "nicht beenden" ](images/ctrl-command-links-image20.png)

    In diesem Beispiel sollte das Befehls Link nicht beenden eine Schaltfläche "Abbrechen" lauten.

-   **Wenn die Bereitstellung einer expliziten Schaltfläche Abbrechen einen einzelnen Befehls Link verlässt, geben Sie einen Befehls Link zum Abbrechen und eine Schaltfläche Abbrechen an.** Dadurch wird deutlich, dass Benutzer eine Auswahl treffen. Formulieren Sie diesen Befehls Link in Bezug darauf, wie er sich von der ersten Antwort unterscheidet, anstelle von "Abbrechen" oder einer Abweichung.

    ![Screenshot von zwei Links und einer Schaltfläche "Abbrechen" ](images/ctrl-command-links-image21.png)

    In diesem Beispiel gibt der zweite Befehls Link an, dass der Benutzer eine Auswahl hat, aber nur den Vorgang abbrechen. Es wird jedoch in Bezug auf die Unterschiede zwischen dem ersten Befehls Link formuliert.

-   **Verwenden Sie Close anstelle von Cancel, wenn Sie die Umgebung nicht in ihren vorherigen Zustand zurücksetzen können, ohne Nebeneffekte zu hinterlassen.**
-   **Nicht deaktivierte Befehls Verknüpfungen anzeigen.** Wenn ein Befehls Link nicht auf den aktuellen Kontext angewendet wird, entfernen Sie ihn stattdessen. Wenn das Entfernen aller nicht angewendenden Befehls Verknüpfungen einen einzelnen Befehls Link verlässt, entfernen Sie entweder das Fenster oder die Seite, oder zeigen Sie eine [Bestätigung](mess-confirm.md) an, wenn eine explizite Zustimmung des Benutzers erforderlich ist.

### <a name="icons"></a>Symbole

-   **Für alle Befehls Verknüpfungen ist ein Symbol erforderlich.** Die Symbole helfen Benutzern, Befehls Verknüpfungen von regulären Verknüpfungen und Benutzeroberflächen Text zu unterscheiden.
-   **Verwenden Sie das Pfeilsymbol nur für Befehls Verknüpfungen.** Reguläre Verknüpfungen sollten das Pfeilsymbol nur verwenden, wenn Sie als Ersatz für Befehls Verknüpfungen in Windows XP verwendet werden.
-   **Verwenden Sie das Sicherheitsschild Symbol, um anzugeben, dass eine Antwort eine sofortige Erhöhung erfordert.** Weitere Richtlinien zur Verwendung des Sicherheitsschild Symbols finden Sie unter [Benutzerkontensteuerung](winenv-uac.md).
-   **Verwenden Sie benutzerdefinierte Symbole nur, wenn Sie Benutzer bei der visuellen Identifizierung und Unterscheidung der Optionen unterstützen.** Verwenden Sie benutzerdefinierte Symbole nicht, wenn Sie nicht sofort erkennbar oder aussagekräftig sind.

    **Falsch:**

    ![Screenshot von zwei Befehls Verknüpfungen mit benutzerdefinierten Symbolen ](images/ctrl-command-links-image22.png)

    In diesem Beispiel sind die benutzerdefinierten Symbole nicht sofort erkennbar.

-   **Verwenden Sie für benutzerdefinierte Symbole 16x16-oder 32 x 32 Pixel-Symbole.** Verwenden Sie die größeren Symbole, wenn ausreichend Speicherplatz vorhanden ist, und profitieren Sie von der größeren Größe. Wenn Sie sicherheitstokenüberlagerungen benötigen, verwenden Sie Symbole mit 32 x 32 oder 48 Pixel.

    ![Screenshot von drei Befehls Verknüpfungen mit Symbolen ](images/ctrl-command-links-image23.png)

    In diesem Beispiel werden benutzerdefinierte 32 x 32 Pixel-Symbole verwendet.

    ![Screenshot von zwei Befehls Verknüpfungen mit größeren Symbolen ](images/ctrl-command-links-image24.png)

    In diesem Beispiel werden benutzerdefinierte 48 Pixel-Symbole mit einem Sicherheitsschild Overlay verwendet.

-   **Vermeiden Sie die Mischung von benutzerdefinierten Symbolen mit dem Standardpfeil Symbol in einem Fenster oder einer Seite.** Wenn Sie ein benutzerdefiniertes Symbol auf einer Oberfläche verwenden, versuchen Sie, alle benutzerdefinierten Symbole zu verwenden. Bevorzugen Sie jedoch das Standardpfeil Symbol für bedeutungslose benutzerdefinierte Symbole.

### <a name="default-values"></a>Standardwerte

-   **Wählen Sie das sicherste (um den Verlust von Daten oder den System Zugriff zu verhindern) und die sicherste Antwort als Standard aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequeme Antwort aus.
-   **Wenn dies praktikabel ist, sollten Sie die erste Antwort als Standardoption festlegen,** da Benutzer häufig davon ausgehen, dass diese Reihenfolge nicht logisch ist.
-   **Machen Sie für Dialogfelder keine destruktive Aktion als Standard Befehls Link,** es sei denn, es gibt eine einfache Möglichkeit, die Aktion rückgängig zu machen.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstände

![Screenshot der Größenanpassung und des Abstands des Befehls Links ](images/ctrl-command-links-image25.png)

## <a name="labels"></a>Bezeichnungen

> [!Note]  
> Da Befehls Verknüpfungen Antworten auf eine Haupt Anweisung sind, sollten Sie vor dem Bestimmen der Antworten eine [gute Haupt Anweisung](text-ui.md) erstellen.

 

**Befehls Link Bezeichnungen**

-   **Wählen Sie eine präzise Bezeichnung aus, die die Funktionsweise des Befehls Links eindeutig kommuniziert und unterscheidet.** Es sollte selbsterklärend sein und der Haupt Anweisung entsprechen. Konzentrieren Sie die Bezeichnungen auf die Unterschiede zwischen den Antworten. Benutzer müssen nicht ermitteln, was der Befehls Link wirklich bedeutet, oder wie er sich von anderen Befehls Verknüpfungen unterscheidet.

    **Falsch:**

    ![Screenshot eines redundanten Befehls Links ](images/ctrl-command-links-image26.png)

    Worin besteht der Unterschied zwischen den zweiten und dritten Antworten in diesem Beispiel? Sind Sie nicht glücklich, dass es eine Schaltfläche zum Abbrechen gibt?

-   **Fokus-Befehls Link Bezeichnungen, die Benutzern helfen, die richtige Entscheidung zu treffen.** Lassen Sie Details aus, die sich nicht auf die Auswahl auswirken. Die Bezeichnungen müssen keine umfassende Spezifikation dafür sein, was passiert.
-   **Start Befehl Verknüpfungen mit einem Verb.** Verwenden Sie die Option "Click" jedoch nicht, da die Bezeichnung über die Funktionsweise des Befehls Links und nicht über die Funktionsweise kommunizieren soll.
    -   **Ausnahme:** Wenn alle Befehls Verknüpfungen mit demselben Verb oder Ausdruck beginnen, entfernen Sie das redundante Verb oder den Ausdruck.
-   Verwenden Sie im Allgemeinen den **positiven** Ausdruck (stellen Sie eine Auswahl, um etwas zu tun). Ein negativer Ausdruck (bei der Auswahl, dass nichts zu tun ist) ist akzeptabel, wenn die Bezeichnungen leichter zu verstehen sind.
-   **Verwenden Sie parallele Ausdrücke und einzeilige Bezeichnungen.** Lange Bezeichnungen verhindern das Lesen und sollten nicht notwendig sein. Außerdem ist es in der Dokumentation einfacher, in mittelgroßen Bezeichnungen zu verweisen.
-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
-   **Verwenden Sie keine endpunktierungen, es sei denn, die Bezeichnung ist eine Frage.**
-   **Weisen Sie einen eindeutigen Zugriffsschlüssel zu.** Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   **Verwenden Sie keine Ellipsen.** Ellipsen bedeutet, dass möglicherweise weitere Informationen erforderlich sind, um die Aktion auszuführen. Ordnungsgemäß verwendete Befehls Verknüpfungen benötigen keine Ellipsen, da Sie unmittelbare Auswirkungen haben.
-   **Wenn eine Antwort dringend empfohlen wird, fügen Sie "(empfohlen)" der Bezeichnung hinzu.** Stellen Sie sicher, dass Sie der Bezeichnung und nicht der ergänzenden Erläuterung hinzufügen.
-   **Wenn eine Antwort nur für fortgeschrittene Benutzer vorgesehen ist, sollten Sie der Bezeichnung "(Advanced)" hinzufügen.** Stellen Sie sicher, dass Sie der Bezeichnung und nicht der ergänzenden Erläuterung hinzufügen.

**Tipp:** Sie können Befehls Verknüpfungen auswerten, indem Sie festgelegt haben, dass ein Freund die Haupt Anweisung angegeben hat, und dass Sie mit den Befehls Verknüpfungen geantwortet haben. Wenn die Antwort mit den Befehls Verknüpfungen unnatürlich oder umständlich wäre, überarbeiten Sie die Befehls Verknüpfungen und möglicherweise die Haupt Anweisung.

**Ergänzende Erläuterungen**

-   Wenn für einen Befehls Link eine weitere Erläuterung erforderlich ist, sollten Sie **eine zusätzliche Erläuterung angeben**. Ergänzende Erläuterungen beschreiben, warum Benutzer möglicherweise eine Antwort auswählen oder was geschieht, wenn eine Antwort ausgewählt wird.

    ![Screenshot von Text, in dem die Ergebnisse der Option beschrieben werden ](images/ctrl-command-links-image27.png)

    In diesem Beispiel werden die Auswirkungen der-Option in der ergänzenden Erläuterung beschrieben.

-   **Verwenden Sie keine ergänzende Erklärung, die für den Befehls Link "Verfassen Anpassung" ist.** Verwenden Sie eine ergänzende Erläuterung nur dann, wenn Sie keinen Befehls Link selbsterklärend erstellen können. Das Bereitstellen einer ergänzenden Erklärung für einen Befehls Link bedeutet nicht, dass Sie Sie für alle bereitstellen müssen.
-   **Konzentrieren Sie sich auf ergänzende Erklärungen, um Benutzern zu helfen, die richtige Entscheidung zu treffen.** Lassen Sie Details aus, die sich nicht auf die Auswahl auswirken. Die ergänzenden Erklärungen müssen keine umfassende Spezifikation dafür sein, was passiert.
-   **Verwenden Sie parallele Ausdrücke und höchstens drei Textzeilen.** Lange ergänzende Erklärungen verhindern das Lesen und sollten nicht notwendig sein.
-   **Verwenden Sie vollständige Sätze und endinterpunktions Zeichen.**

**Befehls Verknüpfungs Gruppen Bezeichnungen**

-   **Verwenden Sie keine Gruppen Bezeichnungen.** Die Haupt Anweisungen fungieren als Gruppen Bezeichnung für Befehls Verknüpfungen.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Befehls Verknüpfungen:

-   Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-und Kleinschreibung, aber nicht den Unterstrich des Zugriffsschlüssels.
-   Wenn die Bezeichnung einen Objektnamen enthält, lassen Sie entweder den Objektnamen aus, oder verwenden Sie Platzhalter Text.
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie klicken.
-   Formatieren Sie nach Möglichkeit die Bezeichnung mit fettem Text. Andernfalls sollten Sie die Bezeichnung nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

**Beispiele:** Um das Bild zu kopieren, klicken Sie auf **Kopieren und ersetzen**.

Klicken Sie auf **Netzwerkadapter zurücksetzen**. (Einen Befehls Link mit der Bezeichnung "Netzwerkadapter- *Adapter Name* zurücksetzen".)

 

