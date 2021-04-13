---
title: Progressive Offenlegungs Steuerelemente
description: Mit einem progressiven Steuerelement für die Offenlegung können Benutzer zusätzliche Informationen, einschließlich Daten, Optionen oder Befehle, anzeigen oder ausblenden.
ms.assetid: 0ca00c49-f897-49a6-926a-cc65f3155c6c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 22c74f60b3184f7fa7f7cdb2b4f2e9d9f64995ea
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351108"
---
# <a name="progressive-disclosure-controls"></a>Progressive Offenlegungs Steuerelemente

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mit einem progressiven Steuerelement für die Offenlegung können Benutzer zusätzliche Informationen, einschließlich Daten, Optionen oder Befehle, anzeigen oder ausblenden. Die Progressive Offenlegung fördert die Einfachheit, indem Sie sich auf die wesentlichen Punkte konzentriert, aber bei Bedarf weitere Details aufzeigt.

![Screenshot der progressiven Offenlegung von Steuerelementen](images/progressive-disclosure-controls-image1.png)

Beispiele für Progressive Offenlegung von Steuerelementen.

> [!Note]  
> Richtlinien im Zusammenhang mit [Layout](vis-layout.md), [Menüs](cmd-menus.md)und [Symbolleisten](cmd-toolbars.md) werden in separaten Artikeln dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Müssen die Benutzer die Informationen in einigen, aber nicht in allen Szenarios oder in einigen, aber nicht in allen Fällen sehen?** Wenn dies der Fall ist, wird durch die Anzeige der Informationen mithilfe progressiver Offenlegung die Baseline vereinfacht, aber Benutzer können problemlos auf die Informationen zugreifen.

    ![Screenshot, der die Security Center-Statusanzeige anzeigt](images/progressive-disclosure-controls-image2.png)

    In diesem Beispiel zeigt Security Center den wichtigen Sicherheitsstatus immer an, verwendet jedoch die Progressive Offenlegung, um Details bei Bedarf anzuzeigen.

-   **Wenn die Informationen standardmäßig angezeigt werden, können Benutzer diese wahrscheinlich ausblenden?** Gibt es Szenarios, in denen Benutzer mehr Speicherplatz benötigen? Sind Benutzer ausreichend motiviert, die Benutzeroberfläche (UI) anzupassen? Wenn nicht, zeigen Sie die Informationen ohne Progressive Offenlegung an.

    **Falsch:**

    ![Screenshot der standardmäßig angezeigten Datenauswahl ](images/progressive-disclosure-controls-image3.png)

    In diesem Beispiel werden die Benutzer nicht motiviert, die Informationen auszublenden.

-   **Sind die zusätzlichen Informationen erweitert, beträchtlich, komplex oder im Zusammenhang mit einer unabhängigen Unteraufgabe?** Wenn dies der Fall ist, sollten Sie die Informationen in einem separaten Fenster mithilfe von [Befehls](ctrl-command-buttons.md) Schaltflächen oder [Links](ctrl-command-links.md) anzeigen, anstatt ein progressives Offenlegung zu verwenden. (Zusätzliche Informationen sind erweitert, wenn Sie für fortgeschrittene Benutzer gedacht sind. Es ist komplex, wenn andere Informationen schwer lesbar oder zu gestalten sind.)

    ![Screenshot von möchten Sie diese Datei ausführen? ](images/progressive-disclosure-controls-image4.png)

    In diesem Beispiel sind Informationen zum Software Namen und-Herausgeber hauptsächlich für fortgeschrittene Benutzer von Bedeutung, sodass Links zu separaten Fenstern verwendet werden.

-   **Handelt es sich bei den zusätzlichen Informationen um einen Satz oder ein Satz Fragment, der beschreibt, was ein Element übernimmt oder wie es verwendet werden kann?** Wenn dies der Fall ist, sollten [Sie eine](ctrl-tooltips-and-infotips.md) QuickInfo oder einen InfoTipp verwenden
-   **Sind die zusätzlichen Informationen im Zusammenhang mit der aktuellen Aufgabe, aber unabhängig von den aktuell angezeigten Informationen?** Wenn dies der Fall ist, sollten Sie stattdessen [Registerkarten](ctrl-tabs.md) verwenden Allerdings sind redusible Listen häufig den Registerkarten vorzuziehen, da Sie flexibler und skalierbar sind.
-   **Werden die zusätzlichen Informationen im Wesentlichen als Daten Filter angezeigt oder ausgeblendet?** Wenn dies der Fall ist, sollten Sie stattdessen eine [Dropdown Liste](/windows/desktop/uxguide/ctrl-drop) oder [Kontrollkästchen](ctrl-check-boxes.md) verwenden, um den Filter auf die gesamte Liste anzuwenden.

## <a name="design-concepts"></a>Entwurfskonzepte

Die Ziele der progressiven Offenlegung lauten:

-   **Vereinfachen Sie die Benutzeroberfläche** , indem Sie sich auf das Wesentliche konzentrieren, aber bei Bedarf weitere Details anzeigen.
-   Vereinfachen Sie die Darstellung **einer Benutzeroberfläche** , indem Sie die Wahrnehmung der Übersichtlichkeit verringern.

Beide Ziele können mithilfe progressiver Offenlegung von Steuerelementen erreicht werden, auf die Benutzer klicken, um weitere Details anzuzeigen. Sie können jedoch das zweite Ziel der Vereinfachung der Darstellung erreichen, ohne die expliziten Steuerelemente der progressiven Offenlegung zu verwenden:

-   **Kontext Details werden nur im Kontext angezeigt.** Beispielsweise können Sie kontextabhängige Befehle oder Symbolleisten automatisch anzeigen, wenn Sie für das ausgewählte Objekt oder den ausgewählten Modus relevant sind.
-   **Verringern der Gewichtung der Kosten für die sekundäre Benutzeroberfläche.** Bei der Verwendung werden visuelle Eigenschaften empfohlen, [die die Verwendung](glossary.md) von Objekten vorschlagen. Der Trend besteht darin, die Benutzeroberfläche zu erstellen, mit der Benutzer direkt interagieren können, aber alle Benutzeroberflächen auf "klicken Sie" klicken. führt zu einer zu großen visuellen Übersichtlichkeit. Bei der sekundären Benutzeroberfläche ist es häufig besser, feine Kosten zu verwenden und die Maus über die vollständige Wirkung zu machen.

    ![Screenshot der Stern Symbole zum Bewerten von Fotos ](images/progressive-disclosure-controls-image5.png)

    In diesem Beispiel ist das Bewertungsfeld interaktiv, wird jedoch erst angezeigt, wenn Sie mit der Maus darauf zeigen.

-   **Es werden nur nachfolgenden Schritte angezeigt, nachdem die Voraussetzungen erfüllt sind.** Dieser Ansatz eignet sich am besten für vertraute Aufgaben, bei denen Benutzer die ersten Schritte zuverlässig durchführen können.

    ![Screenshot der Textfelder "Benutzername" und "Kennwort" ](images/progressive-disclosure-controls-image6.png)

    In diesem Beispiel werden zunächst auf der Seite Benutzername und Kennwort nur die Felder Benutzername und optionales Kennwort angezeigt. Die Bestätigungs-und Hinweis Felder werden angezeigt, nachdem der Benutzer ein Kennwort eingegeben hat.

Während die Progressive Offenlegung eine gute Möglichkeit zur Vereinfachung der Benutzeroberflächen ist, besteht die Gefahr:

-   **Fehlende Auffindbarkeit.** Benutzer können davon ausgehen, dass Sie, wenn Sie nichts sehen, nicht vorhanden ist. Benutzer können nicht darauf zeigen, dass Sie nicht angezeigt werden, oder klicken, wenn Sie nicht angezeigt werden. Es ist immer möglich, dass Benutzer auf Dinge wie weitere Optionen nicht klicken.
-   **Fehlende Stabilität.** Progressive Offenlegung sollte erwartungsgemäß erfolgen oder sich zumindest auf natürliche Weise Verhalten. Wenn Steuerelemente unerwartet angezeigt und ausgeblendet werden, kann sich die resultierende Benutzeroberfläche als instabil fühlen.

### <a name="progressive-disclosure-controls"></a>Progressive Offenlegungs Steuerelemente

Progressives Offenlegung von Steuerelementen wird normalerweise ohne direkte Bezeichnungen angezeigt, die ihr Verhalten beschreiben, sodass Benutzer in der Lage sein müssen, die folgenden Aktionen auf der Grundlage der visuellen Darstellung des Steuer Elements durchzuführen:

-   Erkennen, dass das Steuerelement Progressive Offenlegung bereitstellt.
-   Stellen Sie fest, ob der aktuelle Zustand erweitert oder reduziert ist.
-   Bestimmen Sie, ob zusätzliche Informationen, Optionen oder Befehle zum Ausführen der Aufgabe erforderlich sind.
-   Bestimmen Sie, wie Sie den ursprünglichen Zustand, falls gewünscht, wiederherstellen.

Benutzer können die oben genannten Tests nach Testversion und Fehler ermitteln, Sie sollten jedoch versuchen, derartige Experimente unnötig auszuführen.

Progressives Offenlegung von Steuerelementen haben eine ziemlich schwache Kosten, was [bedeutet, dass](glossary.md)Ihre visuellen Eigenschaften ihre Verwendung, obwohl schwach, vorschlagen. In der folgenden Tabelle wird die Darstellung der allgemeinen Steuerelemente für die Progressive Offenlegung verglichen:



|                                                                                                                                                          |                                                                                                                                                                                                             |                                                                                                                                |                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| **Steuerung**<br/>                                                                                                                                   | **Zweck**<br/>                                                                                                                                                                                      | **Darstellung**<br/>                                                                                                      | **Glyphe gibt an**<br/> |
| **Spitze Klammern**<br/> ![Screenshot von Links/Rechts und nach oben/unten Spitze Klammern ](images/progressive-disclosure-controls-image7.png)<br/>                 | **Alle anzeigen:** Ein-oder Ausblenden der restlichen Elemente in vollständig oder teilweise ausgeblendetem Inhalt. Elemente werden entweder direkt (mit einem einzelnen Chevron) oder in einem Popup Menü (mit einem doppelten Chevron) angezeigt.<br/> | Chevrons zeigen in der Richtung, in der die Aktion ausgeführt wird.<br/>                                                        | Zukünftiger Status<br/>        |
| **Pfeile**<br/> ![Screenshot von Links/Rechts und nach oben/nach-unten-Pfeilen ](images/progressive-disclosure-controls-image8.png)<br/>                     | **Optionen anzeigen:** Popup Befehlsmenü anzeigen.<br/>                                                                                                                                                    | Pfeilen zeigen in der Richtung an, in der die Aktion ausgeführt wird.<br/>                                                          | Zukünftiger Status<br/>        |
| **Plus-und minus Steuerelemente**<br/> ![Screenshot zweier kleiner Plus-und minus-Schaltflächen ](images/progressive-disclosure-controls-image9.png)<br/> | **Erweitern Sie Container:** Erweitern oder reduzieren Sie Container Inhalt direkt, wenn Sie durch eine Hierarchie navigieren.<br/>                                                                                        | Plus-und Minus Symbole zeigen nicht, aber die Aktion erfolgt immer auf der rechten Seite.<br/>                                    | Zukünftiger Status<br/>        |
| **Drehen von Dreiecken**<br/> ![Screenshot zweier kleiner Dreiecke ](images/progressive-disclosure-controls-image10.png)<br/>                  | **Details anzeigen:** Hiermit werden zusätzliche Informationen für ein einzelnes Element angezeigt oder ausgeblendet. Sie werden auch zum Erweitern von Containern verwendet.<br/>                                                                  | Das Drehen von Dreiecken ähnelt in gewisser Weise den rotierenden Hebern, sodass Sie in die Richtung zeigen, in der die Aktion aufgetreten ist<br/> | Vorhandener Zustand<br/>       |



 

**Wenn Sie nur eine Aktion ausführen...**

Benutzer sollten in der Lage sein, das Verhalten eines progressiven Offenlegung-Steuer Elements bei der Überprüfung allein zu prognostizieren. Um dies zu erreichen, wählen Sie die entsprechenden Verwendungs Muster aus, und wenden Sie Ihre Darstellung, den Speicherort und das Verhalten konsistent an.

## <a name="usage-patterns"></a>Verwendungsmuster

Progressive Offenlegung von Steuerelementen haben mehrere Verwendungs Muster. Einige von Ihnen sind in allgemeine Steuerelemente integriert.

### <a name="chevrons"></a>Spitze Klammern

Chevrons ein-oder Ausblenden der restlichen Elemente in vollständig oder teilweise ausgeblendetem Inhalt. Normalerweise werden die Elemente direkt angezeigt, aber Sie können auch in einem Popup Menü angezeigt werden. Wenn das Element vorhanden ist, bleibt es so lange erweitert, bis der Benutzer es reduziert.

Chevrons werden auf folgende Weise verwendet:



|                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Direkte Benutzeroberfläche**<br/> das zugeordnete-Objekt empfängt den Eingabefokus, und das einzelne Chevron wird mit der Leertaste aktiviert.<br/>                       | ![Screenshot der Security Center-Statusanzeige ](images/progressive-disclosure-controls-image11.png)<br/> In diesen Beispielen werden die direkten einzelnen Spitze Klammern rechts vom zugeordneten Steuerelement positioniert.<br/>                                                                            |
| **Befehls Schaltflächen mit externen Bezeichnungen**<br/> die Befehls Schaltfläche erhält den Eingabefokus, und das einzelne Chevron wird mit der Leertaste aktiviert.<br/> | ![Screenshot des chevroners mit der Bezeichnung "Weitere Optionen" ](images/progressive-disclosure-controls-image12.png)<br/> In diesem Beispiel wird die einzelne Chevron-Schaltfläche auf der linken Seite der Bezeichnung gekennzeichnet und positioniert. Bei diesem Muster wäre die Schaltfläche ohne Ihre Bezeichnung schwer zu verstehen.<br/> |
| **Befehls Schaltflächen mit internen Bezeichnungen**<br/> die Befehls Schaltfläche erhält den Eingabefokus und wird mit der Leertaste aktiviert.<br/>                    | ![Screenshot der Befehls Schaltflächen "mehr" und "weniger" ](images/progressive-disclosure-controls-image13.png)<br/> In diesen Beispielen haben reguläre Befehls Schaltflächen den doppelten Chevron positioniert, um ihre Bedeutung vorzuschlagen.<br/>                                                                          |



 

### <a name="arrows"></a>Pfeile

Pfeile zeigen ein Popup-Befehlsmenü an. Das Element bleibt erweitert, bis der Benutzer eine Auswahl trifft oder auf eine beliebige Stelle klickt.

Wenn die Pfeil Schaltfläche ein unabhängiges Steuerelement ist, erhält Sie den Eingabefokus und wird mit der Leerzeichen Leiste aktiviert. Wenn die Pfeil Schaltfläche über ein übergeordnetes Steuerelement verfügt, empfängt das übergeordnete Element den Eingabefokus, und der Pfeil wird mit alt + nach-unten und alt + nach-oben-Taste aktiviert, wie auch das Dropdown Listen-Steuerelement

Pfeile werden auf folgende Weise verwendet:



|                                                                                       |                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Separate Schaltflächen**<br/> der Pfeil befindet sich in einem separaten Schaltflächen-Steuerelement.<br/> | ![Screenshot der Pfeile auf der rechten Seite der Steuerelemente ](images/progressive-disclosure-controls-image14.png)<br/> In diesen Beispielen zeigen separate Pfeil Schaltflächen auf der rechten Seite ein Befehlsmenü an.<br/>               |
| **Befehls Schaltflächen**<br/> der Pfeil ist Teil einer Befehls Schaltfläche.<br/>      | ![Screenshot der Bezeichnung und des Pfeils auf der Befehls Schaltfläche ](images/progressive-disclosure-controls-image15.png)<br/> In diesen Beispielen haben Menü Schaltflächen und unterteilte Schaltflächen die Pfeile rechts neben dem Text.<br/> |



 

### <a name="plus-and-minus-controls"></a>Plus-und minus Steuerelemente

Plus-und minus Steuerelemente werden erweitert oder reduziert, um beim Navigieren durch eine Hierarchie Container Inhalt anzuzeigen. Das Element bleibt erweitert, bis der Benutzer es reduziert. Obwohl es sich dabei um Schaltflächen handelt, ist Ihr Verhalten direkt vorhanden.

Das zugeordnete-Objekt empfängt den Eingabefokus. Das Pluszeichen wird mit der nach-rechts-Taste und der Minus-Taste mit der nach-links-Taste aktiviert.

Plus-und minus Steuerelemente werden auf folgende Weise verwendet:



|                                                                                                |                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Redusible Trees**<br/> eine Hierarchie mit mehreren Ebenen zum Anzeigen von Container Inhalten.<br/> | ![Screenshot, der eine Windows Explorer-Ordnerstruktur mit ausgewähltem "Verhalten" anzeigt.](images/progressive-disclosure-controls-image16.png)<br/> In diesem Beispiel werden die Steuerelemente Plus und minus Links vom zugeordneten Container positioniert.<br/>       |
| **Redusible Listen**<br/> eine Hierarchie mit zwei Ebenen zum Anzeigen von Container Inhalten.<br/>   | ![Screenshot der Liste erweitert, um zwei Ebenen anzuzeigen ](images/progressive-disclosure-controls-image17.png)<br/> In diesem Beispiel werden die Steuerelemente Plus und minus links neben dem zugeordneten Listen Header positioniert.<br/> |



 

### <a name="rotating-triangles"></a>Drehen von Dreiecken

Beim Drehen von Dreiecken werden zusätzliche Informationen für ein einzelnes Element angezeigt oder ausgeblendet. Sie werden auch zum Erweitern von Containern verwendet. Das Element bleibt erweitert, bis der Benutzer es reduziert.

Das zugeordnete-Objekt empfängt den Eingabefokus. Das reduzierte (rechts zeigende) Dreieck wird mit der nach-rechts-Pfeiltaste und dem erweiterten (nach unten zeigenden) Dreieck mit der nach-links-Taste aktiviert.

Dreh Dreiecke werden auf folgende Weise verwendet:



|                                                                                                            |                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Redusible Trees**<br/> eine Hierarchie mit mehreren Ebenen zum Anzeigen von Container Inhalten.<br/>             | ![Screenshot der Ordnerstruktur von Windows-Explorer ](images/progressive-disclosure-controls-image18.png)<br/> In diesem Beispiel befinden sich die drehenden Dreiecke links vom zugeordneten Container.<br/>       |
| **Redusible Listen**<br/> eine Hierarchie mit zwei Ebenen, um zusätzliche Informationen anzuzeigen.<br/> | ![Screenshot der Liste mit zusätzlichen Daten ](images/progressive-disclosure-controls-image19.png)<br/> In diesem Beispiel werden die rotierenden Dreiecke links neben den zugehörigen Listenelementen positioniert.<br/> |



 

### <a name="preview-arrows"></a>Vorschau Pfeile

Wie Chevrons werden zusätzliche Informationen direkt angezeigt oder ausgeblendet. Das Element bleibt erweitert, bis der Benutzer es reduziert. Anders als Chevrons verfügen die Symbole über eine grafische Darstellung der Aktion, in der Regel mit einem Pfeil, der angibt, was passiert.

![Bildschirm Abbildung von Pfeilsymbolen, die diagonal zeigen ](images/progressive-disclosure-controls-image20.png)

In diesen Beispielen von Microsoft Windows Media Player haben die Symbole Pfeile, die die Aktion vorschlagen, die ausgeführt wird.

Vorschau Pfeile eignen sich am besten für Situationen, in denen ein Standardmäßiges Chevron das Verhalten des Steuer Elements nicht angemessen kommuniziert, z. b. wenn die Offenlegung Komplex ist oder mehrere Arten von Offenlegung vorhanden sind.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Wählen Sie basierend auf der Verwendung das Muster für die Progressive Offenlegung aus.** Eine Beschreibung der einzelnen Verwendungs Muster finden Sie in der vorherigen Tabelle.
-   **Verwenden Sie keine Verknüpfungen für progressiv-Offenlegung.** Verwenden Sie nur die im Abschnitt Verwendungs Muster dargestellten Steuerelemente für die Progressive Offenlegung. Verwenden Sie jedoch Links, um zu [Hilfe Themen](winenv-help.md)zu navigieren.

    **Richtig:**

    ![Screenshot des chevroners mit der Bezeichnung "Mixer anzeigen" ](images/progressive-disclosure-controls-image21.png)

    **Falsch:**

    ![Screenshot des linktexts "Mixer anzeigen" ](images/progressive-disclosure-controls-image22.png)

    Im falschen Beispiel wird ein Link verwendet, um weitere Optionen anzuzeigen. Diese Verwendung ist korrekt, wenn der Link zu einer anderen Seite oder einem anderen Dialogfeld navigiert oder ein Hilfethema angezeigt wird.

### <a name="interaction"></a>Interaktion

-   **Verwenden Sie Quick Infos für Spitze Klammern und Pfeile, die nicht direkt gekennzeichnet sind, um zu beschreiben, was Sie tun.**

    ![Screenshot der QuickInfo "Expand the Query Builder" ](images/progressive-disclosure-controls-image23.png)

    In diesem Beispiel gibt die QuickInfo die Auswirkung eines nicht gekennzeichneten Chevron-Steuer Elements an.

-   **Wenn ein Benutzer ein Element erweitert oder reduziert, legen Sie den Zustand dauerhaft fest, sodass er beim nächsten Anzeigen des Fensters wirksam** wird, es sei denn, die Benutzer werden wahrscheinlich den Standardzustand starten. Sorgen Sie dafür, dass der Zustand pro Fenster, pro Benutzer, beibehalten wird.
-   **Stellen Sie sicher, dass der gesamte erweiterte Inhalt reduziert werden kann und umgekehrt, und dass der umgekehrte Vorgang offensichtlich ist.** Dies fördert die Durchsuchung und reduziert die Frustration. Die beste Möglichkeit, den umgekehrten Vorgang offensichtlich zu machen, besteht darin, das Steuerelement am gleichen Speicherort zu halten. Wenn Sie das Steuerelement verschieben müssen, behalten Sie es am gleichen relativen Speicherort innerhalb eines visuell unterschiedlichen Bereichs bei.

    **Falsch:**

    ![Screenshot der Schaltfläche "Replace" durch Chevron ](images/progressive-disclosure-controls-image24.png)

    ![Screenshot der Schaltfläche "Replace" ohne Chevron ](images/progressive-disclosure-controls-image25.png)

    Wenn Sie in diesem Beispiel auf die Schaltfläche ersetzen mit dem Chevron klicken, wird das Textfeld **Ersetzen durch** angezeigt. Nachdem dies geschehen ist, wird der Replace-Expander zum Replace-Befehl, sodass es keine Möglichkeit gibt, den ursprünglichen Zustand wiederherzustellen.

-   **Verwenden Sie für das Muster für die Progressive Offenlegung nur die Zugriffsschlüssel**, die im Abschnitt Verwendungs Muster aufgeführt sind. Verwenden Sie die EINGABETASTE nicht zum Aktivieren der progressiven Veröffentlichung.

### <a name="presentation"></a>Präsentation

-   **Verwenden Sie keine dreieckigen Pfeilspitzen für einen anderen Zweck als Progressive Offenlegung.**

    **Falsch:**

    ![Screenshot der Bezeichnung mit dem nach rechts zeigenden Dreieck ](images/progressive-disclosure-controls-image26.png)

    Obwohl es sich bei diesem Beispiel nicht um ein progressives Offenlegungs Muster handelt, wird hier mit einem Pfeil darauf hingewiesen, dass Befehle in einem Popup Fenster angezeigt werden.

    **Richtig:**

    ![Screenshot der Bezeichnung mit der linken Seite des Texts ](images/progressive-disclosure-controls-image27.png)

    In diesem Beispiel wird stattdessen eine Aufzählungs Zeichen ordnungsgemäß verwendet.

-   **Entfernen Sie Progressive Offenlegungs Steuerelemente, die nicht im aktuellen Kontext angewendet werden (nicht deaktivieren).** Progressive Offenlegung von Steuerelementen sollten immer ihre Zusage erfüllen. entfernen Sie Sie also, wenn keine weiteren Informationen vorhanden sind.

    **Falsch:**

    ![Screenshot eines Abbild-Steuer Elements "Weitere Optionen" ](images/progressive-disclosure-controls-image28.png)

    In diesem Beispiel ist ein Steuerelement für die Progressive Offenlegung nicht ordnungsgemäß deaktiviert.

### <a name="chevrons"></a>Spitze Klammern

-   **Verwenden Sie einzelne Spitze Klammern zum Anzeigen oder ausblenden an Ort. Verwenden Sie doppelte Spitze Klammern zum Anzeigen oder ausblenden mithilfe eines Popup Menüs.** Sie sollten jedoch immer doppelte Spitze Klammern für Befehls Schaltflächen mit internen Bezeichnungen verwenden.

    **Richtig:**

    ![Screenshot eines Steuer Elements mit einem Steuerelement mit einem Chevron mehr Optionen ](images/progressive-disclosure-controls-image29.png)

    **Falsch:**

    ![Screenshot des Steuer Elements "Double-Chevron more options" ](images/progressive-disclosure-controls-image30.png)

    Im falschen Beispiel wird ein doppeltes Chevron für die direkte Progressive Offenlegung verwendet.

    **Richtig:**

    ![Screenshot der doppelten Chevron-Befehls Schaltfläche ](images/progressive-disclosure-controls-image31.png)

    In diesem Beispiel wird ein doppeltes Chevron für direkte Progressive Offenlegung verwendet, da es sich um eine Befehls Schaltfläche mit einer internen Bezeichnung handelt.

-   **Stellen Sie eine visuelle Beziehung zwischen dem Chevron und dem zugeordneten Steuerelement bereit.** Da direkte Spitze Klammern rechts von der zugehörigen Benutzeroberfläche platziert werden und rechtsbündig ausgerichtet sind, kann zwischen einem Chevron und dem zugeordneten Steuerelement ein gewisser Abstand bestehen.

    **Richtig:**

    ![Screenshot der gestaffelten Schattierung hinter Steuerelementen ](images/progressive-disclosure-controls-image32.png)

    In diesem Beispiel gibt es eine klare Beziehung zwischen dem direkten Chevron und der zugehörigen Benutzeroberfläche.

    **Falsch:**

    ![Screenshot des voll tonweißen Hintergrunds für Steuerelemente ](images/progressive-disclosure-controls-image33.png)

    In diesem Beispiel gibt es keine klare visuelle Beziehung zwischen dem direkten Chevron und der zugehörigen Benutzeroberfläche, daher scheint der Speicherplatz leer zu sein.

### <a name="arrows"></a>Pfeile

-   **Verwenden Sie keine Pfeil Grafiken, die mit Back, Forward, go oder Play verwechselt werden könnten.** Verwenden Sie einfache Dreiecks förmige Pfeilspitzen (Pfeile ohne Stämme) auf neutralen Hintergründen.

    **Richtig:**

    ![Screenshot zweier kleiner schwarzer Dreiecke ](images/progressive-disclosure-controls-image34.png)

    Diese Pfeile sind deutlich Progressive Offenlegung von Steuerelementen.

    **Falsch (bei progressiver Offenlegung):**

    ![Screenshot von zwei kleinen grünen Pfeilen ](images/progressive-disclosure-controls-image35.png)

    Diese Pfeile sehen nicht wie Progressive Offenlegung von Steuerelementen aus.

    **Falsch (für "Back&quot;, &quot;Forward"):**

    ![Screenshot von zwei Schaltflächen mit schwarzem Dreiecke ](images/progressive-disclosure-controls-image36.png)

    Diese Pfeile sehen wie Progressive Offenlegung von Steuerelementen aus, aber nicht.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstände

![Screenshot der empfohlenen Größe und des Abstands ](images/progressive-disclosure-controls-image37.png)

Empfohlene Größe und Abstände für Progressive Offenlegung von Steuerelementen.

## <a name="labels"></a>Bezeichnungen

-   Für Spitze Klammern auf einer Befehls Schaltfläche mit externer Bezeichnung:
    -   Weisen Sie einen eindeutigen [Zugriffsschlüssel](glossary.md)zu. Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
    -   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
    -   Schreiben Sie die Bezeichnung als Ausdruck, und verwenden Sie keine endpunktierungen.
    -   Schreiben Sie die Bezeichnung, sodass Sie die Auswirkung des Klicks auf die Schaltfläche beschreibt, und ändern Sie die Bezeichnung, wenn sich der Status ändert.
    -   Wenn die Oberfläche immer einige Optionen, Befehle oder Details anzeigt, verwenden Sie die folgenden Bezeichnungs Paare:
        -   **Mehr oder weniger Optionen.** Verwenden Sie für Optionen oder eine Mischung aus Optionen, Befehlen und Details.
        -   **Mehr oder weniger Befehle.** Nur für Befehle verwenden.
        -   **Mehr/weniger Details.** Wird nur für Informationen verwendet.
        -   **Mehr oder weniger <object name> .** Verwenden Sie für andere Objekttypen, z. b. Ordner.
    -   Andernfalls:
        -   **Optionen zum ein-/ausblenden.** Verwenden Sie für Optionen oder eine Mischung aus Optionen, Befehlen und Details.
        -   **Befehle anzeigen/ausblenden.** Nur für Befehle verwenden.
        -   **Details anzeigen/ausblenden.** Wird nur für Informationen verwendet.
        -   **Ein-/ausblenden <object name> .** Verwenden Sie für andere Objekttypen, z. b. Ordner.
-   Befolgen Sie für Spitze Klammern in einer Befehls Schaltfläche mit einer internen Bezeichnung die Standardrichtlinien für die [Befehls Schaltfläche](ctrl-command-buttons.md) .

## <a name="documentation"></a>Dokumentation

Beim Verweis auf Progressive Offenlegung von Steuerelementen:

-   Wenn das Steuerelement über eine Fixed-Bezeichnung verfügt, verweisen Sie auf das-Steuerelement nur über seine Bezeichnung. versuchen Sie nicht, das Steuerelement zu beschreiben. Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-und Kleinschreibung, aber nicht den Unterstrich des Zugriffsschlüssels.
-   Wenn das Steuerelement keine Bezeichnung aufweist oder es nicht korrigiert ist, verweisen Sie auf das Steuerelement, indem Sie den Typ Chevron, Pfeil, Dreieck oder plus/minus drücken. Beschreiben Sie ggf. auch die Position des Steuer Elements. Wenn das Steuerelement dynamisch angezeigt wird, z. b. das [Seiten Raum](glossary.md) Steuerelement, starten Sie den Verweis, indem Sie beschreiben, wie das Steuerelement angezeigt wird.

    **Beispiel:** Um die Dateien in einem Ordner anzuzeigen, verschieben Sie den Zeiger an den Anfang des Ordner namens, und klicken Sie dann auf das Dreieck neben dem Ordner.

-   Verweisen Sie nicht auf das-Steuerelement als Schaltfläche, es sei denn, Sie können mit anderen progressiven Offenlegung-Steuerelementen im Gegensatz zu
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie klicken. Verwenden Sie bei Bedarf den Klick... zum Erweitern oder reduzieren.
-   Formatieren Sie nach Möglichkeit die Bezeichnung mit fettem Text. Andernfalls sollten Sie die Bezeichnung nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiele:

-   (Für ein Chevron) Um die Dateigröße zu ermitteln, klicken Sie auf **Details**.
-   (Für einen Pfeil) Um alle Optionen anzuzeigen, klicken Sie auf den Pfeil neben dem **Suchfeld** .
-   (Für Plus/Minus) Klicken Sie auf **Bilder**, um das Bild anzuzeigen.

