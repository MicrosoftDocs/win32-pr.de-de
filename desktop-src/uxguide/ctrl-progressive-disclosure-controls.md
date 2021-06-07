---
title: Progressive Offenlegungskontrollen
description: Mit einem Progressive Disclosure-Steuerelement können Benutzer zusätzliche Informationen ein- oder ausblenden, einschließlich Daten, Optionen oder Befehlen.
ms.assetid: 0ca00c49-f897-49a6-926a-cc65f3155c6c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a40f4c2fadd75cbcb6711dec2c1361ce2f970088
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524544"
---
# <a name="progressive-disclosure-controls"></a>Progressive Offenlegungskontrollen

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere aktuelle [Entwurfsanleitung wider.](/windows/uwp/design/)

Mit einem Progressive Disclosure-Steuerelement können Benutzer zusätzliche Informationen ein- oder ausblenden, einschließlich Daten, Optionen oder Befehlen. Die progressive Offenlegung fördert die Einfachheit, indem sie sich auf das Wesentliche konzentriert und bei Bedarf zusätzliche Details preis gibt.

![Screenshot der progressiven Offenlegungssteuerelemente](images/progressive-disclosure-controls-image1.png)

Beispiele für progressive Offenlegungskontrollen.

> [!Note]  
> Richtlinien im Zusammenhang [mit Layout,](vis-layout.md) [Menüs](cmd-menus.md)und Symbolleisten werden in separaten Artikeln dargestellt. [](cmd-toolbars.md)

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Müssen Benutzer die Informationen in einigen, aber nicht in allen Szenarien oder in einigen, aber nicht immer sehen?** Wenn ja, vereinfacht die Anzeige der Informationen mithilfe der progressiven Offenlegung die Baselineerfahrung, ermöglicht benutzern jedoch den einfachen Zugriff auf die Informationen.

    ![Screenshot: Anzeige des Security Center-Status](images/progressive-disclosure-controls-image2.png)

    In diesem Beispiel zeigt Security Center den wichtigen Sicherheitsstatus an, verwendet aber die progressive Offenlegung, um Details bei Bedarf anzuzeigen.

-   **Wenn die Informationen standardmäßig angezeigt werden, werden Benutzer diese wahrscheinlich ausblenden?** Gibt es Szenarien, in denen Benutzer mehr Speicherplatz benötigen? Sind Benutzer ausreichend motiviert, die Benutzeroberfläche anzupassen? Falls nicht, zeigen Sie die Informationen ohne progressive Offenlegung an.

    **Falsch:**

    ![Screenshot der standardmäßig angezeigten Datenauswahl ](images/progressive-disclosure-controls-image3.png)

    In diesem Beispiel sind Benutzer nicht dazu bewegt, die Informationen auszublenden.

-   **Sind die zusätzlichen Informationen erweitert, erheblich, komplex oder stehen im Zusammenhang mit einem unabhängigen Subtask?** Falls ja, sollten Sie die Informationen [](ctrl-command-buttons.md) in einem [](ctrl-command-links.md) separaten Fenster mithilfe von Befehlsschaltflächen oder Links anzeigen, anstatt ein progressives Offenlegungssteuersystem zu verwenden. (Zusätzliche Informationen werden erweitert, wenn sie für fortgeschrittene Benutzer vorgesehen sind. Es ist komplex, wenn andere Informationen schwer zu lesen oder zu verlegen sind.)

    ![Screenshot: Möchten Sie diese Datei ausführen? ](images/progressive-disclosure-controls-image4.png)

    In diesem Beispiel sind Informationen zum Namen und Herausgeber der Software in erster Linie für fortgeschrittene Benutzer sinnvoll, sodass Links zu separaten Fenstern verwendet werden.

-   **Handelt es sich bei den zusätzlichen Informationen um ein Satz- oder Satzfragment, das beschreibt, was ein Element macht oder wie es verwendet werden kann?** Falls ja, sollten Sie eine [QuickInfo oder infotip](ctrl-tooltips-and-infotips.md) verwenden.
-   **Sind die zusätzlichen Informationen mit der aktuellen Aufgabe verknüpft, aber unabhängig von den aktuell angezeigten Informationen?** Wenn dies der Meinung ist, [sollten Sie stattdessen Registerkarten](ctrl-tabs.md) verwenden. Reduzierbare Listen sind jedoch häufig Registerkarten vorzuziehen, da sie flexibler und skalierbarer sind.
-   **Werden die zusätzlichen Informationen im Wesentlichen als Datenfilter angezeigt oder verborgen?** Wenn dies der Fall ist, [](ctrl-check-boxes.md) sollten Sie [stattdessen eine Dropdownliste oder](/windows/desktop/uxguide/ctrl-drop) Kontrollkästchen verwenden, um den Filter auf die gesamte Liste anzuwenden.

## <a name="design-concepts"></a>Entwurfskonzepte

Die ziele der progressiven Offenlegung sind:

-   **Vereinfachen Sie eine Benutzeroberfläche,** indem Sie sich auf das Wesentliche konzentrieren, aber bei Bedarf zusätzliche Details anzeigen.
-   **Vereinfachen Sie die Darstellung einer Benutzeroberfläche,** indem Sie die Übersichtlichkeit reduzieren.

Beide Ziele können mithilfe von progressiven Offenlegungssteuerelementen erreicht werden, bei denen Benutzer klicken, um weitere Details zu sehen. Sie können jedoch das zweite Ziel erreichen, die Darstellung zu vereinfachen, ohne explizite Steuerungen für die progressive Offenlegung zu verwenden, indem Sie:

-   **Kontextbezogene Details werden nur im Kontext angezeigt.** Beispielsweise können Sie kontextbezogene Befehle oder Symbolleisten automatisch anzeigen, wenn sie für das ausgewählte Objekt oder den ausgewählten Modus relevant sind.
-   **Verringern der Gewichtung von Benutzeroberflächen für sekundäre Benutzeroberflächen** ["Affordances" sind](glossary.md) visuelle Eigenschaften, die vorschlagen, wie Objekte verwendet werden. Der Trend besteht in der Benutzeroberfläche, mit der Benutzer interagieren können, aber dass alle diese Benutzeroberflächen zum "Klicken auf mich!" gezeichnet werden. führt zu viel visueller Übersichtlichkeit. Für die sekundäre Benutzeroberfläche ist es oft besser, kleine Verfingungen zu verwenden und die vollständigen Auswirkungen auf den Mauszeiger zu erzielen.

    ![Screenshot der Sternsymbole, die zum Bewerten von Fotos verwendet werden ](images/progressive-disclosure-controls-image5.png)

    In diesem Beispiel ist das Feld Bewertung interaktiv, wird jedoch erst angezeigt, wenn der Mauszeiger darauf zeigt.

-   **Die Folgeschritte werden erst angezeigt, nachdem die Voraussetzungen erfüllt sind.** Dieser Ansatz wird am besten für vertraute Aufgaben verwendet, bei denen Benutzer die ersten Schritte sicher ausführen können.

    ![Screenshot der Textfelder für Benutzername und Kennwort ](images/progressive-disclosure-controls-image6.png)

    In diesem Beispiel werden auf der Seite Benutzername und Kennwort zunächst nur die Felder Benutzername und optionales Kennwort angezeigt. Die Bestätigungs- und Hinweisfelder werden angezeigt, nachdem der Benutzer ein Kennwort eingegeben hat.

Die progressive Offenlegung ist zwar eine hervorragende Möglichkeit zur Vereinfachung von Beschriftungen, aber sie birgt die folgenden Risiken:

-   **Fehlende Aufholbarkeit.** Benutzer gehen möglicherweise davon aus, dass sie nicht vorhanden sind, wenn sie etwas nicht sehen können. Benutzer können nicht darauf klicken oder darauf klicken, wenn sie nicht sehen, was sie suchen. Es besteht immer die Möglichkeit, dass Benutzer nicht auf Weitere Optionen klicken.
-   **Fehlende Stabilität.** Die progressive Offenlegung sollte erwartet oder zumindest natürlich sein. Wenn Steuerelemente unerwartet angezeigt und nicht mehr angezeigt werden, kann sich die resultierende Benutzeroberfläche instabil verhalten.

### <a name="progressive-disclosure-controls"></a>Progressive Offenlegungskontrollen

Progressive Offenlegungssteuerelemente werden in der Regel ohne direkte Bezeichnungen angezeigt, die ihr Verhalten beschreiben, sodass Benutzer die folgenden Schritte allein anhand der visuellen Darstellung des Steuerelements tun können müssen:

-   Erkennen Sie, dass das Steuerelement eine progressive Offenlegung ermöglicht.
-   Bestimmen Sie, ob der aktuelle Zustand erweitert oder reduziert ist.
-   Bestimmen Sie, ob zusätzliche Informationen, Optionen oder Befehle erforderlich sind, um die Aufgabe auszuführen.
-   Bestimmen Sie bei Wunsch, wie der ursprüngliche Zustand wiederhergestellt werden soll.

Benutzer können die oben genannten Informationen zwar durch Testversion und Fehler bestimmen, aber Sie sollten versuchen, solche Experimente unnötig zu machen.

Progressive Offenlegungssteuerelemente weisen relativ [schwache](glossary.md)Vorgabe auf, was bedeutet, dass ihre visuellen Eigenschaften vorschlagen, wie sie verwendet werden, obwohl sie schwach sind. In der folgenden Tabelle wird die Darstellung der gängigen Steuerelemente für die progressive Offenlegung verglichen:



| Control | Zweck  | Darstellung | Glyphen gibt an |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| **Chevrons**<br/> ![Screenshot der Chevrons links/rechts und nach oben/unten ](images/progressive-disclosure-controls-image7.png)<br/>                 | **Alle anzeigen:** Blendet die verbleibenden Elemente in vollständig oder teilweise ausgeblendeten Inhalten ein oder aus. Elemente werden entweder direkt (mit einem einzelnen Chevron) oder in einem Popupmenü (mit einem doppeln Chevron) angezeigt.<br/> | Chevrons zeigen in die Richtung, in der die Aktion auftritt.<br/>                                                        | Zukünftiger Status<br/>        |
| **Pfeile**<br/> ![Screenshot der Pfeile nach links/rechts und nach oben/unten ](images/progressive-disclosure-controls-image8.png)<br/>                     | **Optionen anzeigen:** Ein Popupbefehlsmenü anzeigen.<br/>                                                                                                                                                    | Pfeile zeigen in die Richtung, in der die Aktion erfolgt.<br/>                                                          | Zukünftiger Status<br/>        |
| **Plus- und Minussteuerelemente**<br/> ![Screenshot von zwei kleinen Plus- und Minusschaltflächen ](images/progressive-disclosure-controls-image9.png)<br/> | **Erweitern von Containern:** Erweitern oder reduzieren Sie Containerinhalte an Ort und Stelle, wenn Sie durch eine Hierarchie navigieren.<br/>                                                                                        | Plus- und Minuszeichen zeigen nicht, aber die Aktion erfolgt immer rechts.<br/>                                    | Zukünftiger Status<br/>        |
| **Drehen von Dreiecken**<br/> ![Screenshot von zwei kleinen Dreiecken ](images/progressive-disclosure-controls-image10.png)<br/>                  | **Details anzeigen:** Anzeigen oder Ausblenden zusätzlicher Informationen für ein einzelnes Element. Sie werden auch zum Erweitern von Containern verwendet.<br/>                                                                  | Drehende Dreiecke ähneln drehbaren Hebeln, sodass sie in die Richtung zeigen, in der die Aktion aufgetreten ist.<br/> | Vorhandener Zustand<br/>       |



 

**Wenn Sie nur eine Sache tun...**

Benutzer sollten in der Lage sein, das Verhalten einer progressiven Offenlegungssteuerung ordnungsgemäß vorherzusagen, indem sie nur eine Überprüfung durchführen. Um dies zu erreichen, wählen Sie die entsprechenden Verwendungsmuster aus, und wenden Sie deren Darstellung, Position und Verhalten konsistent an.

## <a name="usage-patterns"></a>Verwendungsmuster

Progressive Offenlegungskontrollen haben mehrere Verwendungsmuster. Einige davon sind in gängige Steuerelemente integriert.

### <a name="chevrons"></a>Chevrons

Chevrons blenden die verbleibenden Elemente in vollständig oder teilweise ausgeblendeten Inhalten ein oder aus. Normalerweise werden die Elemente an Ort und Stelle angezeigt, können aber auch in einem Popupmenü angezeigt werden. Wenn es bereits verwendet wird, bleibt das Element erweitert, bis es vom Benutzer reduziert wird.

Chevrons werden auf folgende Weise verwendet:



|      Verwendung                                                                                                                                                          |    Beispiel                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **In-place UI**<br/> das zugeordnete -Objekt erhält den Eingabefokus, und das einzelne Chevron wird mit der Raumleiste aktiviert.<br/>                       | ![Screenshot der Anzeige des Security Center-Status ](images/progressive-disclosure-controls-image11.png)<br/> In diesen Beispielen werden die einzelnen Chevrons rechts neben dem zugeordneten Steuerelement positioniert.<br/>                                                                            |
| **Befehlsschaltflächen mit externen Bezeichnungen**<br/> Die Befehlsschaltfläche erhält den Eingabefokus, und das einzelne Chevron wird mit der Leerzeichenleiste aktiviert.<br/> | ![Screenshot des Chevrons mit der Bezeichnung "Weitere Optionen" ](images/progressive-disclosure-controls-image12.png)<br/> In diesem Beispiel wird die einzelne Chevronschaltfläche beschriftet und links neben der Bezeichnung positioniert. Bei diesem Muster wäre die Schaltfläche ohne ihre Bezeichnung schwer zu verstehen.<br/> |
| **Befehlsschaltflächen mit internen Bezeichnungen**<br/> Die Befehlsschaltfläche erhält den Eingabefokus und wird mit der Leerzeichenleiste aktiviert.<br/>                    | ![Screenshot der Befehlsschaltflächen "mehr" und "weniger" ](images/progressive-disclosure-controls-image13.png)<br/> In diesen Beispielen ist für reguläre Befehlsschaltflächen das doppelte Chevron positioniert, um ihre Bedeutung zu vorschlagen.<br/>                                                                          |



 

### <a name="arrows"></a>Pfeile

Pfeile zeigen ein Popupbefehlsmenü an. Das Element bleibt erweitert, bis der Benutzer eine Auswahl trifft oder auf eine beliebige Stelle klickt.

Wenn die Pfeilschaltfläche ein unabhängiges Steuerelement ist, erhält sie den Eingabefokus und wird mit der Leerzeichenleiste aktiviert. Wenn die Pfeilschaltfläche über ein übergeordnetes Steuerelement verfügt, erhält das übergeordnete Element den Eingabefokus, und der Pfeil wird wie beim Dropdownlisten-Steuerelement mit ALT+NACH-UNTEN-TASTE und ALT+NACH-OBEN-TASTE aktiviert.

Pfeile werden auf folgende Weise verwendet:



|    Verwendung                                                                                   |    Beispiel                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Separate Schaltflächen**<br/> Der Pfeil befindet sich in einem separaten Schaltflächen-Steuerelement.<br/> | ![Screenshot der Pfeile rechts von Steuerelementen ](images/progressive-disclosure-controls-image14.png)<br/> In diesen Beispielen weisen separate Pfeilschaltflächen, die rechts positioniert sind, auf ein Befehlsmenü hin.<br/>               |
| **Befehlsschaltflächen**<br/> Der Pfeil ist Teil einer Befehlsschaltfläche.<br/>      | ![Screenshot der Bezeichnung und des Pfeils auf der Befehlsschaltfläche ](images/progressive-disclosure-controls-image15.png)<br/> In diesen Beispielen sind die Pfeile für Menüschaltflächen und geteilte Schaltflächen rechts neben dem Text positioniert.<br/> |



 

### <a name="plus-and-minus-controls"></a>Plus- und Minussteuerelemente

Plus- und Minussteuerelemente werden erweitert oder reduziert, um containerinhalt beim Navigieren durch eine Hierarchie anzuzeigen. Das Element bleibt erweitert, bis es vom Benutzer reduziert wird. Obwohl diese wie Schaltflächen aussehen, ist ihr Verhalten direkt.

Das zugeordnete -Objekt empfängt den Eingabefokus. Das Pluszeichen wird mit der NACH-RECHTS-TASTE und das Minuszeichen mit der NACH-LINKS-TASTE aktiviert.

Plus- und Minussteuerelemente werden auf folgende Weise verwendet:



|       Verwendung                                                                                         |       Beispiel                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Reduzierbare Strukturen**<br/> eine Hierarchie mit mehreren Ebenen, um Containerinhalte anzuzeigen.<br/> | ![Screenshot, der eine Windows-Explorer Ordnerstruktur mit ausgewählter Option "Verhalten" zeigt.](images/progressive-disclosure-controls-image16.png)<br/> In diesem Beispiel werden die Plus- und Minussteuerelemente links vom zugeordneten Container positioniert.<br/>       |
| **Reduzierbare Listen**<br/> eine Hierarchie mit zwei Ebenen, um Containerinhalte anzuzeigen.<br/>   | ![Screenshot der liste erweitert, um zwei Ebenen anzuzeigen ](images/progressive-disclosure-controls-image17.png)<br/> In diesem Beispiel werden die Plus- und Minussteuerelemente links vom zugeordneten Listenheader positioniert.<br/> |



 

### <a name="rotating-triangles"></a>Drehen von Dreiecken

Durch drehende Dreiecke werden zusätzliche Informationen für ein einzelnes Element angezeigt oder ausblendet. Sie werden auch zum Erweitern von Containern verwendet. Das Element bleibt erweitert, bis es vom Benutzer reduziert wird.

Das zugeordnete -Objekt empfängt den Eingabefokus. Das reduzierte (nach rechts zeigende) Dreieck wird mit der nach rechts weisenden Pfeiltaste und das erweiterte (nach unten zeigende) Dreieck mit der nach links weisenden Pfeiltaste aktiviert.

Rotierende Dreiecke werden auf folgende Weise verwendet:



|     Verwendung                                                                                                       |    Beispiel                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Reduzierbare Strukturen**<br/> eine Hierarchie mit mehreren Ebenen, um Containerinhalte anzuzeigen.<br/>             | ![Screenshot der Ordnerstruktur im Windows-Explorer ](images/progressive-disclosure-controls-image18.png)<br/> In diesem Beispiel werden die drehenden Dreiecke links vom zugeordneten Container positioniert.<br/>       |
| **Reduzierbare Listen**<br/> eine Hierarchie mit zwei Ebenen, um zusätzliche Informationen an Ort und Stelle zu zeigen.<br/> | ![Screenshot der Liste mit zusätzlichen Daten ](images/progressive-disclosure-controls-image19.png)<br/> In diesem Beispiel werden die drehenden Dreiecke links von ihren zugeordneten Listenelementen positioniert.<br/> |



 

### <a name="preview-arrows"></a>Vorschaupfeile

Wie Chevrons werden zusätzliche Informationen angezeigt oder ausgeblendet. Das Element bleibt erweitert, bis es vom Benutzer reduziert wird. Im Gegensatz zu Chevrons verfügen die Glyphen über eine grafische Darstellung der Aktion, in der Regel mit einem Pfeil, der angibt, was passiert.

![Screenshot von pfeilförmigen Glyphen, die diagonal zeigen ](images/progressive-disclosure-controls-image20.png)

In diesen Beispielen von Microsoft Windows Media Player weisen die Glyphen Pfeile auf, die die aktionsschnelle Aktion vorschlagen.

Vorschaupfeile sind am besten für Situationen reserviert, in denen ein Standard-Chevron das Verhalten des Steuerelements nicht angemessen kommuniziert, z. B. wenn die Offenlegung komplex ist oder es mehrere Arten der Offenlegung gibt.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Wählen Sie das Muster für die progressive Offenlegung basierend auf seiner Verwendung aus.** Eine Beschreibung der einzelnen Verwendungsmuster finden Sie in der vorherigen Tabelle.
-   **Verwenden Sie keine Links für progressive Offenlegungssteuerungen.** Verwenden Sie nur die progressiven Offenlegungssteuerelemente, die im Abschnitt Verwendungsmuster dargestellt sind. Verwenden Sie jedoch Links, um zu Den [Hilfethemen zu navigieren.](winenv-help.md)

    **Richtig:**

    ![Screenshot des Chevrons mit der Bezeichnung "Mixer anzeigen" ](images/progressive-disclosure-controls-image21.png)

    **Falsch:**

    ![Screenshot des Linktexts "Mixer anzeigen" ](images/progressive-disclosure-controls-image22.png)

    Im falschen Beispiel wird ein Link verwendet, um weitere Optionen zu zeigen. Diese Verwendung wäre richtig, wenn der Link zu einer anderen Seite oder zu einem anderen Dialogfeld navigiert oder ein Hilfethema angezeigt würde.

### <a name="interaction"></a>Interaktion

-   **Verwenden Sie für Chevrons und Pfeile, die nicht direkt beschriftet sind, QuickInfos, um ihre Verwendung zu beschreiben.**

    ![Screenshot der QuickInfo "Erweitern des Abfrage-Generators" ](images/progressive-disclosure-controls-image23.png)

    In diesem Beispiel gibt die QuickInfo den Effekt eines nicht bezeichneten Chevron-Steuerelements an.

-   **Wenn ein Benutzer ein** Element erweitert oder reduziert, lassen Sie den Zustand beibehalten, damit er beim nächsten Anzeigen des Fensters wirksam wird, es sei denn, Benutzer bevorzugen wahrscheinlich, im Standardzustand zu beginnen. Sorgen Sie dafür, dass der Zustand pro Fenster und pro Benutzer beibehalten wird.
-   **Stellen Sie sicher, dass alle erweiterten Inhalte reduziert werden können und umgekehrt, und dass der umgekehrte Vorgang offensichtlich ist.** Dies fördert die Erkundung und verringert die Frust. Die beste Möglichkeit, den umgekehrten Vorgang offensichtlich zu machen, besteht im Behalten des Steuerelements an derselben festen Position. Wenn Sie das Steuerelement verschieben müssen, behalten Sie es an der gleichen relativen Position innerhalb eines visuell eindeutigen Bereichs bei.

    **Falsch:**

    ![Screenshot der Schaltfläche "Ersetzen" mit Chevron ](images/progressive-disclosure-controls-image24.png)

    ![Screenshot der Schaltfläche "Ersetzen" ohne Chevron ](images/progressive-disclosure-controls-image25.png)

    In diesem Beispiel wird durch Klicken auf die Schaltfläche Ersetzen durch das Chevron das **Textfeld Ersetzen durch** angezeigt. Sobald dies erfolgt ist, wird der Replace-Expander zum Replace-Befehl, sodass es keine Möglichkeit gibt, den ursprünglichen Zustand wiederherzustellen.

-   **Verwenden Sie nur die Zugriffsschlüssel, die für das Muster für die progressive** Offenlegung geeignet sind, wie im Abschnitt Verwendungsmuster aufgeführt. Verwenden Sie die EINGABETASTE nicht, um die progressive Offenlegung zu aktivieren.

### <a name="presentation"></a>Präsentation

-   **Verwenden Sie dreieckige Pfeilspitzen nicht für einen anderen Zweck als die progressive Offenlegung.**

    **Falsch:**

    ![Screenshot der Bezeichnung mit nach rechts zeigenden Dreieck ](images/progressive-disclosure-controls-image26.png)

    Obwohl dieses Beispiel kein progressives Offenlegungsmuster ist, deutet die Verwendung eines Pfeils hier darauf hin, dass Befehle in einem Popupfenster angezeigt werden.

    **Richtig:**

    ![Screenshot der Bezeichnung mit einem Aufzählungszeichen links vom Text ](images/progressive-disclosure-controls-image27.png)

    In diesem Beispiel wird stattdessen ein Aufzählungszeichen ordnungsgemäß verwendet.

-   **Entfernen (nicht deaktivieren) progressiver Offenlegungssteuerelemente, die im aktuellen Kontext nicht gelten.** Progressive Offenlegungskontrollen sollten immer ihre Zusage erfüllen. Entfernen Sie sie daher, wenn keine weitere Informationen zu geben sind.

    **Falsch:**

    ![Screenshot eines abgeblendet dargestellten Steuerelements "Weitere Optionen" ](images/progressive-disclosure-controls-image28.png)

    In diesem Beispiel ist ein nicht angewendetes progressives Offenlegungssteuersystem falsch deaktiviert.

### <a name="chevrons"></a>Chevrons

-   **Verwenden Sie einzelne Chevrons, um sie ein- oder auszublenden. Verwenden Sie doppelte Chevrons, um sie mithilfe eines Popupmenüs ein- oder auszublenden.** Sie sollten jedoch immer doppelte Chevrons für Befehlsschaltflächen mit internen Bezeichnungen verwenden.

    **Richtig:**

    ![Screenshot des Steuerelements "Mehr Optionen" für ein Chevron ](images/progressive-disclosure-controls-image29.png)

    **Falsch:**

    ![Screenshot des Doppel-Chevron-Steuerelements mit mehr Optionen ](images/progressive-disclosure-controls-image30.png)

    Im falschen Beispiel wird ein doppeltes Chevron für die schrittweise Veröffentlichung verwendet.

    **Richtig:**

    ![Screenshot der Doppel-Chevron-Befehlsschaltfläche "Mehr" ](images/progressive-disclosure-controls-image31.png)

    In diesem Beispiel wird ein doppeltes Chevron für die ortsinterne progressive Offenlegung verwendet, da es sich um eine Befehlsschaltfläche mit einer internen Bezeichnung handelt.

-   **Stellen Sie eine visuelle Beziehung zwischen dem Chevron und dem zugeordneten Steuerelement zur Verfügung.** Da direkt platzierte Chevrons rechts neben ihrer zugeordneten Benutzeroberfläche platziert und rechtsbündig ausgerichtet sind, kann ein relativer Abstand zwischen einem Chevron und dem zugehörigen Steuerelement liegen.

    **Richtig:**

    ![Screenshot der gegestuften Schattierung hinter Steuerelementen ](images/progressive-disclosure-controls-image32.png)

    In diesem Beispiel gibt es eine klare Beziehung zwischen dem in-place-Chevron und der zugehörigen Benutzeroberfläche.

    **Falsch:**

    ![Screenshot von Vollbildhintergrund für Steuerelemente ](images/progressive-disclosure-controls-image33.png)

    In diesem Beispiel gibt es keine klare visuelle Beziehung zwischen dem in-place-Chevron und der zugehörigen Benutzeroberfläche, sodass es im Raum unverankert zu sein scheint.

### <a name="arrows"></a>Pfeile

-   **Verwenden Sie keine Pfeilgrafiken, die mit Back, Forward, Go oder Play verwechselt werden könnten.** Verwenden Sie einfache dreieckige Pfeilspitzen (Pfeile ohne Stamm) auf neutralen Hintergründen.

    **Richtig:**

    ![Screenshot von zwei kleinen schwarzen Dreiecken ](images/progressive-disclosure-controls-image34.png)

    Diese Pfeile sind eindeutig progressive Offenlegungssteuerelemente.

    **Falsch (für progressive Offenlegung):**

    ![Screenshot von zwei kleinen grünen Pfeilen ](images/progressive-disclosure-controls-image35.png)

    Diese Pfeile sehen nicht wie progressive Offenlegungssteuerelemente aus.

    **Falsch (für Zurück, Vorwärts):**

    ![Screenshot von zwei Schaltflächen mit schwarzen Dreiecken ](images/progressive-disclosure-controls-image36.png)

    Diese Pfeile sehen wie progressive Offenlegungssteuerelemente aus, aber nicht.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstand

![Screenshot der empfohlenen Größen- und Abstandsgröße ](images/progressive-disclosure-controls-image37.png)

Empfohlene Größen- und Abstandsangaben für progressive Offenlegungssteuerungen.

## <a name="labels"></a>Bezeichnungen

-   Für Chevrons auf einer Befehlsschaltfläche mit einer externen Bezeichnung:
    -   Weisen Sie einen [eindeutigen Zugriffsschlüssel zu.](glossary.md) Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
    -   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)
    -   Schreiben Sie die Bezeichnung als Ausdruck, und verwenden Sie keine endende Interpunktion.
    -   Schreiben Sie die Bezeichnung so, dass sie die Auswirkung des Klickens auf die Schaltfläche beschreibt und die Bezeichnung ändert, wenn sich der Zustand ändert.
    -   Wenn auf der Oberfläche immer einige Optionen, Befehle oder Details angezeigt werden, verwenden Sie die folgenden Bezeichnungspaare:
        -   **Mehr/Weniger Optionen.** Verwenden Sie für Optionen oder eine Mischung aus Optionen, Befehlen und Details.
        -   **Mehr/Weniger Befehle.** Verwenden Sie nur für Befehle.
        -   **Mehr/weniger Details.** Verwenden Sie nur für Informationen.
        -   **Mehr/weniger <object name> .** Verwenden Sie für andere Objekttypen, z. B. Ordner.
    -   Andernfalls:
        -   **Optionen zum Ein-/Ausblenden.** Verwenden Sie für Optionen oder eine Mischung aus Optionen, Befehlen und Details.
        -   **Befehle ein-/ausblenden.** Verwenden Sie nur für Befehle.
        -   **Details ein-/ausblenden.** Verwenden Sie nur für Informationen.
        -   **Ein-/Ausblenden <object name> von .** Verwenden Sie für andere Objekttypen, z. B. Ordner.
-   Befolgen Sie für Chevrons auf einer Befehlsschaltfläche mit einer internen Bezeichnung die [Standardrichtlinien für Befehlsschaltfläche.](ctrl-command-buttons.md)

## <a name="documentation"></a>Dokumentation

Beim Verweis auf progressive Offenlegungssteuerelemente:

-   Wenn das Steuerelement über eine feste Bezeichnung verfügt, verweisen Sie nur über seine Bezeichnung auf das Steuerelement. versuchen Sie nicht, das Steuerelement zu beschreiben. Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Weißzeichen, aber schließen Sie den Unterstrich der Zugriffsschlüssel nicht ein.
-   Wenn das Steuerelement keine Bezeichnung hat oder nicht fixiert ist, verweisen Sie auf das Steuerelement nach seinem Typ: Chevron, Pfeil, Dreieck oder Plus-/Minusschaltfläche. Beschreiben Sie bei Bedarf auch die Position des Steuerelements. Wenn das Steuerelement dynamisch angezeigt [](glossary.md) wird, z. B. das Seitenbereich-Steuerelement, starten Sie den Verweis, indem Sie beschreiben, wie das Steuerelement angezeigt wird.

    **Beispiel:** Um die Dateien in einem Ordner anzuzeigen, verschieben Sie den Zeiger auf den Anfang des Ordnernamens, und klicken Sie dann auf das Dreieck neben dem Ordner.

-   Verweisen Sie nicht auf das Steuerelement als Schaltfläche, es sei denn, sie stehen im Gegensatz zu anderen progressiven Offenlegungssteuerelementen, bei denen es sich nicht um Schaltflächen handelt.
-   Verwenden Sie click, um die Benutzerinteraktion zu beschreiben. Verwenden Sie aus Gründen der Übersichtlichkeit klick... , um zu erweitern oder zu reduzieren.
-   Formatieren Sie die Bezeichnung nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiele:

-   (Für ein Chevron) Klicken Sie auf Details , um die Dateigröße **zu bestimmen.**
-   (Für einen Pfeil) Klicken Sie auf den Pfeil neben dem Feld Suchen, um alle **Optionen** zu sehen.
-   (Für Plus/Minus) Klicken Sie zum Anzeigen des Bilds auf **Bilder**.

