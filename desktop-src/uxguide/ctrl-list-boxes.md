---
title: Listenfelder
description: Mit einem Listenfeld können Benutzer aus einer Reihe von Werten auswählen, die in einer Liste angezeigt werden, die immer sichtbar ist.
ms.assetid: 620e9ff9-b367-446b-9e97-9c9d6d14f4bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 3db0bbb07ed6cea18b7d8fb29fd4e329840590d5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351109"
---
# <a name="list-boxes"></a>Listenfelder

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mit einem Listenfeld können Benutzer aus einer Reihe von Werten auswählen, die in einer Liste angezeigt werden, die immer sichtbar ist. Mit einem Listenfeld für die einfache Auswahl wählen Benutzer ein Element aus einer Liste von sich gegenseitig ausschließenden Werten aus. Mit einem Listenfeld Mehrfachauswahl wählen Benutzer NULL oder mehr Elemente aus einer Liste von Werten aus.

![Screenshot des Listen Felds für die einfache Auswahl ](images/ctrl-list-boxes-image1.png)

Ein typisches Listenfeld für die einfache Auswahl.

> [!Note]  
> Richtlinien, die sich auf [Layout](vis-layout.md) -und [Listenansichten](ctrl-list-views.md) beziehen, werden in separaten Artikeln dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Stellt die Liste Daten anstelle der Programmoptionen dar?** In jedem Fall ist ein Listenfeld unabhängig von der Anzahl der Elemente eine geeignete Wahl. Im Gegensatz dazu [](ctrl-radio-buttons.md) sind options [Felder oder Kontrollkästchen](ctrl-check-boxes.md) nur für eine kleine Anzahl von Programmoptionen geeignet.
-   **Müssen Benutzer Sichten ändern, gruppieren, nach Spalten sortieren oder Spaltenbreite und-Reihenfolge ändern?** Wenn dies der Fall ist, verwenden Sie stattdessen eine [Listenansicht](ctrl-list-views.md) .
-   **Muss das Steuerelement eine Zieh Quelle oder ein Ablage Ziel sein?** Wenn dies der Fall ist, verwenden Sie stattdessen eine Listenansicht.
-   **Müssen die Listenelemente in die Zwischenablage kopiert oder aus der Zwischenablage eingefügt werden?** Wenn dies der Fall ist, verwenden Sie stattdessen eine Listenansicht.

**Einfache Auswahllisten**

-   **Wird das Steuerelement verwendet, um eine Option aus einer Liste von sich gegenseitig ausschließenden Werten auszuwählen?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Wenn Sie mehrere Optionen auswählen möchten, verwenden Sie stattdessen eine standardmäßige Mehrfachauswahl Liste, eine Kontrollkästchen Liste, einen Listen-Generator oder eine Liste zum hinzufügen/entfernen.
-   **Gibt es eine Standardoption, die für die meisten Benutzer in den meisten Situationen empfohlen wird?** Sehen Sie, dass die ausgewählte Option weitaus wichtiger ist, als die Alternativen zu sehen? Wenn dies der Fall ist, sollten Sie eine [Dropdown Liste](/windows/desktop/uxguide/ctrl-drop) verwenden, wenn Sie nicht möchten, dass Benutzer Änderungen vornehmen, indem Sie die alternativen ausblenden.

![Screenshot der höchsten Qualität als Standard Schaltfläche ](images/ctrl-list-boxes-image2.png)

In diesem Beispiel ist die höchste Farbqualität die beste Wahl für die meisten Benutzer, sodass eine Dropdown Liste eine gute Wahl ist, um die alternativen herunter zugeben.

-   **Ist für die Liste eine Konstante Interaktion erforderlich?** Wenn dies der Fall ist, verwenden Sie eine einfache Auswahlliste, um die Interaktion zu vereinfachen.

![Screenshot der Liste der Optionen, z. b. nur-Text ](images/ctrl-list-boxes-image3.png)

In diesem Beispiel ändern Benutzer ständig das ausgewählte Element in der Liste Elemente anzeigen, um die Vordergrund-und Hintergrundfarben festzulegen. Die Verwendung einer Dropdown Liste ist in diesem Fall sehr mühsam.

-   **Erscheint die Einstellung wie eine relative Menge? Können die Benutzer sofort Feedback** zu den Auswirkungen der Einstellungsänderungen haben? Wenn dies der Fall ist, sollten Sie stattdessen einen [Schieberegler](ctrl-sliders.md) verwenden.
-   **Gibt es eine bedeutende hierarchische Beziehung zwischen den Listenelementen?** Verwenden Sie in diesem Fall stattdessen ein Struktur [Ansicht](ctrl-tree-views.md) -Steuerelement.
-   **Ist der Bildschirmbereich bei einem Premium-Tarif?** Wenn dies der Fall ist, verwenden Sie stattdessen eine Dropdown Liste, da der verwendete Bildschirmbereich fest und unabhängig von der Anzahl der Listenelemente ist.

**Standard Listen für Mehrfachauswahl und Kontrollkästchen**

-   **Ist die Mehrfachauswahl für den Task oder häufig verwendet?** Wenn dies der Fall ist, verwenden Sie eine Liste der Kontrollkästchen, um die Mehrfachauswahl zu verdeutlichen, insbesondere, wenn die Ziel Benutzer nicht erweitert sind Viele Benutzer bemerken nicht, dass eine standardmäßige Mehrfachauswahl Liste die Mehrfachauswahl unterstützt. Verwenden Sie eine standardmäßige Mehrfachauswahl Liste, wenn die Kontrollkästchen zu viel Aufmerksamkeit auf die Mehrfachauswahl zeichnen oder zu einer zu großen Bildschirm Übersichtlichkeit führen würden.
-   **Ist die Stabilität der Mehrfachauswahl wichtig?** Wenn dies der Fall ist, verwenden Sie eine Liste der Kontrollkästchen, Listen Generator oder Liste hinzufügen/entfernen, da Sie nur auf nur ein einzelnes Element klicken. Mit einer standardmäßigen Mehrfachauswahl Liste ist es sehr einfach, alle Auswahlmöglichkeiten zu löschen.
-   **Wird das Steuerelement verwendet, um 0 (null) oder mehr Elemente aus einer Liste von Werten auszuwählen?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Verwenden Sie zum Auswählen eines Elements stattdessen eine einfache Auswahlliste.

**Vorschau Listen**

-   **Können die Optionen leichter mit Bildern ausgewählt werden als nur mit Text?** Wenn dies der Fall ist, verwenden Sie eine Vorschau Liste.

**Auflisten von Generatoren und Hinzufügen/Entfernen von Listen**

-   **Wird das Steuerelement verwendet, um 0 (null) oder mehr Elemente aus einer Liste von Werten auszuwählen?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Verwenden Sie zum Auswählen eines Elements stattdessen eine einfache Auswahlliste.
-   **Ist die Reihenfolge der ausgewählten Elemente wichtig?** Wenn dies der Fall ist, unterstützen der Listen-Generator und das Hinzufügen/Entfernen von Listen Mustern die Reihenfolge, während die anderen Muster für Mehrfachauswahl nicht.
-   **Ist es wichtig für Benutzer, eine Zusammenfassung aller ausgewählten Elemente anzuzeigen?** Wenn dies der Fall ist, werden im Listen-Generator und in den Listen Mustern zum hinzufügen/entfernen nur die ausgewählten Elemente angezeigt, während die anderen Mehrfachauswahl Muster dies nicht tun.
-   **Sind die möglichen Auswahlmöglichkeiten nicht eingeschränkt?** Wenn dies der Fall ist, verwenden Sie eine Liste zum hinzufügen/entfernen, damit Benutzer Werte auswählen können, die sich derzeit nicht in der Liste
-   **Ist für das Hinzufügen eines Werts zur Liste ein spezielles Dialogfeld zum Auswählen von Objekten erforderlich?** Wenn ja, verwenden Sie eine Liste hinzufügen/entfernen, und zeigen Sie das Dialogfeld an, wenn Benutzer auf Hinzufügen klicken.
-   **Ist der Bildschirmbereich bei einem Premium-Tarif?** Wenn dies der Fall ist, verwenden Sie stattdessen eine Liste zum hinzufügen/entfernen, da Sie weniger Bildschirmbereich verwendet, da Sie nicht immer den Satz von Optionen anzeigt.

Bei Listenfeldern ist **die Anzahl der Elemente in der Liste kein Faktor bei der Auswahl des Steuer** Elements, da Sie von Tausenden von Elementen bis zu einer für einzelne Auswahllisten skaliert werden (und keine für Mehrfachauswahl Listen). Da Listenfelder für Daten verwendet werden können, wird die Anzahl der Elemente möglicherweise nicht im Voraus bekannt sein.

**Hinweis:** Manchmal wird ein Steuerelement, das wie ein Listenfeld aussieht, mithilfe einer Listenansicht und umgekehrt implementiert. Wenden Sie in solchen Fällen die Richtlinien auf Grundlage der Verwendung, nicht der Implementierung an.

## <a name="usage-patterns"></a>Verwendungsmuster

Listenfelder weisen mehrere Verwendungs Muster auf:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Einfache Auswahllisten</strong> Ermöglicht es Benutzern, jeweils ein Element auszuwählen. <br/></td>
<td><img src="images/ctrl-list-boxes-image4.png" alt="Screen shot of list box with one item selected " /><br/> In diesem Beispiel können Benutzer nur ein Anzeigeelement auswählen.<br/></td>
</tr>
<tr class="even">
<td><strong>Standard Listen für Mehrfachauswahl</strong> Ermöglicht Benutzern das Auswählen einer beliebigen Anzahl von Elementen, einschließlich "keine".<br/></td>
<td>Standard Listen mit Mehrfachauswahl weisen genau dieselbe Darstellung wie einfache Auswahllisten auf. es gibt also keinen visuellen Hinweis darauf, dass ein Listenfeld Mehrfachauswahl unterstützt. Da Benutzer diese Fähigkeit ermitteln müssen, wird dieses Listen Muster am besten für Aufgaben verwendet, bei denen die Mehrfachauswahl nicht wesentlich ist und nur selten verwendet wird. <br/> Es gibt zwei verschiedene Modi für Mehrfachauswahl: <a href="glossary.md">mehrfach</a> und <a href="glossary.md">erweitert</a>. Der <strong>Erweiterte Auswahlmodus</strong> ist weitaus häufiger, wo die Auswahl durchziehen oder mit Umschalt + Klick und Strg + Klick erweitert werden kann, um Gruppen von zusammenhängenden bzw. nicht angrenzenden Werten auszuwählen. Im <strong>Mehrfachauswahl Modus</strong>wird durch Klicken auf ein beliebiges Element der Auswahl Zustand unabhängig von der Umschalttaste und der STRG-Taste gewechselt. Bei diesem ungewöhnlichen Verhalten ist der Modus für Mehrfachauswahl veraltet, und Sie sollten stattdessen Kontrollkästchen-Listen verwenden.<br/> <img src="images/ctrl-list-boxes-image5.png" alt="Screen shot of list box with several items selected " /><br/> In diesem Beispiel können Benutzer mithilfe des Mehrfachauswahl Modus eine beliebige Anzahl von Elementen auswählen.<br/></td>
</tr>
<tr class="odd">
<td><strong>Kontrollkästchen Listen</strong> In den Listenfeldern Standard Mehrfachauswahl können Benutzer beliebig viele Elemente auswählen, z. b. keine.<br/></td>
<td>Im Gegensatz zu standardmäßigen Mehrfachauswahl Listen geben die Kontrollkästchen deutlich an, dass mehrere Auswahlmöglichkeiten möglich sind. Verwenden Sie dieses Listen Muster für Aufgaben, bei denen die Mehrfachauswahl wesentlich oder häufig verwendet wird. <br/> <img src="images/ctrl-list-boxes-image6.png" alt="Screen shot of Toolbars check-box list " /><br/> In diesem Beispiel wählen Benutzer in der Regel mehr als ein Element aus, sodass eine Kontrollkästchen Liste verwendet wird.<br/> Wenn Sie diese klare Angabe für Mehrfachauswahl feststellen, können Sie davon ausgehen, dass die Kontrollkästchen Listen den standardmäßigen Mehrfachauswahl Listen vorzuziehen sind. In der Praxis erfordern nur wenige Aufgaben eine Mehrfachauswahl oder eine hohe Verwendung. die Verwendung einer Liste der Kontrollkästchen in solchen Fällen zeichnet zu viel Aufmerksamkeit. Folglich <strong>sind standardmäßige Mehrfachauswahl Listen weitaus häufiger.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>Vorschau Listen</strong> Kann eine einzelne oder mehrere Auswahl sein, aber Sie zeigen eine Vorschau der Auswirkung der Auswahl anstelle von Text an.<br/></td>
<td><img src="images/ctrl-list-boxes-image7.png" alt="Screen shot of Window Color options preview " /><br/> In diesem Beispiel zeigt eine Vorschau der einzelnen Optionen die Auswirkung der Auswahl deutlich an, was effektiver ist als die Verwendung von Text alleine.<br/></td>
</tr>
<tr class="odd">
<td><strong>Auflisten</strong> von Generatoren Ermöglicht es Benutzern, eine Liste mit Auswahlmöglichkeiten zu erstellen, indem ein Element gleichzeitig hinzugefügt und optional die Listen Reihenfolge festgelegt wird.<br/></td>
<td>Ein Listen-Generator besteht aus zwei Einzel Auswahllisten: die Liste auf der linken Seite ist ein fester Satz von Optionen, und die Liste auf der rechten Seite ist die Liste, die erstellt wird. Zwischen den Listen stehen zwei Befehls Schaltflächen zur Verfügung: <br/>
<ul>
<li>Eine Schaltfläche zum <strong>Hinzufügen</strong> , mit der die aktuell ausgewählte Option in die Liste verschoben wird, die erstellt und vor dem ausgewählten Element eingefügt wird. (Doppelklicken auf ein Options Element hat denselben Effekt.)</li>
<li>Eine <strong>Entfernungs</strong> Schaltfläche, die das ausgewählte Element aus der erstellten Liste entfernt und an die Optionsliste zurückgibt. (Doppelklicken auf ein Element in der erstellten Liste hat denselben Effekt.) Die integrierte Liste kann optional die Befehle nach <strong>oben</strong> und nach <strong>unten</strong> verschieben, um die Listenelemente zu sortieren.</li>
</ul>
<img src="images/ctrl-list-boxes-image8.png" alt="Screen shot of Toolbar buttons list builder " /><br/> In diesem Beispiel wird ein Listen-Generator zum Erstellen einer Symbolleiste verwendet, indem Elemente aus einem Satz verfügbarer Optionen ausgewählt und deren Reihenfolge festgelegt wird.<br/></td>
</tr>
<tr class="even">
<td><strong>Listen hinzufügen/entfernen</strong> Ermöglicht es Benutzern, eine Liste mit Auswahlmöglichkeiten zu erstellen, indem ein oder mehrere Elemente gleichzeitig hinzugefügt werden und optional die Listen Reihenfolge (z. b. List Builder) festgelegt wird<br/></td>
<td>Wenn <strong>Sie auf Hinzufügen</strong> klicken, wird im Gegensatz zu einem Listen-Generator ein Dialogfeld angezeigt, in dem Sie Elemente auswählen können Die Verwendung eines separaten Dialog Felds ermöglicht erhebliche Flexibilität bei der Auswahl von Elementen. Sie können eine spezialisierte Objektauswahl oder sogar ein gängiges Dialogfeld verwenden. Im Vergleich zum Listen-Generator ist diese Variante kompakter, erfordert jedoch etwas mehr Aufwand, Elemente hinzuzufügen. <br/> <img src="images/ctrl-list-boxes-image9.png" alt="Screen shot of Menu contents list " /><br/> In diesem Beispiel können Benutzer Tools in einem Menü hinzufügen oder entfernen sowie die Reihenfolge festlegen.<br/> Die Listen-Generator-und Add/Remove-Listen Muster sind zwar erheblich schwerer als die anderen Mehrfachauswahl Listen, bieten jedoch zwei einzigartige Vorteile:<br/>
<ul>
<li>Benutzer haben die Kontrolle über die Listen Reihenfolge, und zwar sowohl bei der Erstellung der Liste als auch danach.</li>
<li>Benutzer können eine Zusammenfassung der ausgewählten Elemente überprüfen. Dies kann ein erheblicher Vorteil sein, wenn die Anzahl der Optionen sehr groß ist.</li>
</ul>
Ihre Nachteile sind, dass Sie viel mehr Bildschirmplatz benötigen und schwer zu verwenden sind, wenn eine große Liste von Elementen von Grund auf neu erstellt wird. Folglich werden Sie am besten dazu verwendet, kurze Listen zu erstellen oder Listen zu ändern, die bereits vorhanden sind.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

-   **Sortieren Sie Listenelemente in einer logischen Reihenfolge,** z. b. das Gruppieren verwandter Optionen, das Platzieren der am häufigsten verwendeten Elemente zuerst oder das Verwenden der alphabetischen Reihenfolge. Sortieren von Namen in alphabetischer Reihenfolge, Zahlen in numerischer Reihenfolge und Datumsangaben in chronologischer Reihenfolge. Listen mit 12 oder mehr Elementen sollten alphabetisch sortiert werden, damit Elemente leichter zu finden sind.

**Richtig:** ![ Screenshot der Ausrichtung (Links, zentriert, rechts) ](images/ctrl-list-boxes-image10.png)

In diesem Beispiel werden die Listenfeld Elemente nach ihrer räumlichen Beziehung sortiert.

**Falsch:** ![ Screenshot der nicht geordneten Liste ](images/ctrl-list-boxes-image11.png)

In diesem Beispiel gibt es so viele Listenelemente, dass Sie in alphabetischer Reihenfolge sortiert werden müssen.

**Richtig:** ![ Screenshot der alphabetisch sortierten Liste ](images/ctrl-list-boxes-image12.png)

In diesem Beispiel sind die Listenelemente leichter zu finden, da Sie in alphabetischer Reihenfolge sortiert sind. Das Element "alle Windows-Produkte" befindet sich jedoch unabhängig von der Sortierreihenfolge am Anfang der Liste.

-   **Platzieren Sie Optionen, die "All" oder "None" am Anfang der Liste darstellen**, unabhängig von der Sortierreihenfolge der restlichen Elemente.
-   **Umschließen von metaoptionen in Klammern.**

![Screenshot der Dropdown Liste ohne Auswahl ](images/ctrl-list-boxes-image13.png)

In diesem Beispiel ist "(None)" eine Meta-Option, da es sich nicht um einen gültigen Wert für die Auswahl handelt, sondern um die Angabe, dass die Option selbst nicht verwendet wird.

-   **Verwenden Sie stattdessen Meta-Options, wenn keine leeren Listenelemente vorhanden sind.** Benutzer wissen nicht, wie leere Elemente interpretiert werden, wohingegen die Bedeutung von metaoptionen explizit ist.

**Falsch:** ![ Screenshot der Dropdown Liste mit leerer Auswahl ](images/ctrl-list-boxes-image14.png)

In diesem Beispiel ist die Bedeutung des leeren Elements unklar.

**Richtig:** ![ Screenshot der Dropdown Liste ohne Auswahl ](images/ctrl-list-boxes-image13.png)

In diesem Beispiel wird stattdessen die Meta-Option "(None)" verwendet.

### <a name="interaction"></a>Interaktion

-   **Sie sollten das doppelte Klickverhalten bereitstellen.** Das Doppelklicken muss dieselbe Wirkung wie das Auswählen eines Elements und das Ausführen seines Standard Befehls haben.
-   **Doppelklick Verhalten redundant.** Es sollte immer eine Befehls Schaltfläche oder ein Kontextmenü Befehl vorhanden sein, der dieselbe Auswirkung hat.
-   **Wenn Benutzer mit den ausgewählten Elementen nichts tun können, dürfen Sie die Auswahl nicht zulassen.**

**Richtig:** ![ Screenshot der Liste der Assistenten Änderungen abgeschlossen ](images/ctrl-list-boxes-image15.png)

In diesem Listenfeld wird eine schreibgeschützte Liste von Änderungen angezeigt. Es ist keine Auswahl erforderlich.

-   **Wenn Sie ein Listenfeld deaktivieren, deaktivieren Sie auch alle zugeordneten Bezeichnungen und Befehls Schaltflächen.**
-   **Verwenden Sie die Änderung des ausgewählten Elements in einem Listenfeld nicht wie folgt:**
    -   Ausführen von Befehlen.
    -   Zeigen Sie andere Fenster an, z. b. ein Dialogfeld, um weitere Eingaben zu erfassen.
    -   Dynamische Anzeige anderer Steuerelemente, die mit dem ausgewählten Steuerelement verknüpft sind (Sprachausgabe können solche Ereignisse nicht erkennen). **Ausnahme:** Sie können den statischen Text, der zur Beschreibung des ausgewählten Elements verwendet wird, dynamisch ändern.

**Akzeptabel:** ![ Screenshot der Details des ausgewählten Listen Elements ](images/ctrl-list-boxes-image16.png)

In diesem Beispiel ändert sich die Beschreibung durch Ändern des ausgewählten Elements.

-   **Vermeiden Sie horizontales Scrollen.** Mehrspaltige Listen basieren auf dem horizontalen Scrollen, was im allgemeinen schwieriger zu verwenden ist als vertikaler Bildlauf. Mehrspaltige Listen, die einen horizontalen Bildlauf erfordern, können verwendet werden, wenn Sie viele alphabetisch sortierte Elemente und ausreichend Bildschirmfläche für ein breites Steuerelement haben.

**Akzeptabel:** ![ Screenshot der Liste der Ordner in Windows-Explorer ](images/ctrl-list-boxes-image17.png)

In diesem Beispiel werden mehrere Spalten verwendet, die einen horizontalen Bildlauf erfordern, da viele Elemente vorhanden sind und für ein breites Steuerelement ausreichend Speicherplatz verfügbar ist.

### <a name="multiple-selection-lists"></a>Mehrfachauswahl Listen

-   Es empfiehlt **sich, die Anzahl der ausgewählten Elemente unterhalb der Liste anzuzeigen** . Dies gilt insbesondere, wenn Benutzer wahrscheinlich mehrere Elemente auswählen. Diese Informationen bieten nicht nur nützliches Feedback, sondern auch deutlich, dass das Listenfeld Mehrfachauswahl unterstützt.

![Screenshot des Listen Felds mit vier ausgewählten Elementen ](images/ctrl-list-boxes-image5.png)

In diesem Beispiel wird die Anzahl der ausgewählten Elemente unterhalb der Liste angezeigt.

-   Sie können weitere auswahlmetriken angeben, die aussagekräftiger sein können, z. b. die für die Auswahl erforderlichen Ressourcen.

![Screenshot der Kontrollkästchen Liste der Windows-Features ](images/ctrl-list-boxes-image18.png)

In diesem Beispiel ist der Speicherplatz, der für die Installation der Komponenten erforderlich ist, aussagekräftiger als die Anzahl der ausgewählten Elemente.

-   Wenn potenziell viele Listenelemente vorhanden sind und Sie alle auswählen oder löschen, fügen Sie die Option Alles auswählen und alle Befehls Schaltflächen Löschen hinzu.
-   Verwenden Sie für Standard Listen mit Mehrfachauswahl nicht den Mehrfachauswahl Modus, da der Auswahlmodus veraltet ist. Verwenden Sie für ein entsprechendes Verhalten stattdessen eine Kontrollkästchen Liste.

### <a name="default-values"></a>Standardwerte

-   **Wählen Sie das sicherste (um Datenverlust oder System Zugriff zu vermeiden) und die sicherste Option standardmäßig aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequeme Option aus.

**Ausnahme:** Wählen Sie keine Elemente aus, wenn das Steuerelement eine Eigenschaft in einem [gemischten Zustand](glossary.md)darstellt. Dies ist der Fall, wenn eine Eigenschaft für mehrere Objekte angezeigt wird, die nicht die gleiche Einstellung aufweisen.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstände

![Screenshot der Listenfeld Größe und des Abstands ](images/ctrl-list-boxes-image19.png)

Empfohlene Größe und Abstände für Listenfelder.

-   **Wählen Sie eine Listenfeld Breite aus, die für die längsten gültigen Daten geeignet ist.** Standard Listenfelder können nicht horizontal gescrollt werden, sodass Benutzer nur sehen können, was im Steuerelement sichtbar ist.
-   **Fügen Sie zusätzliche 30 Prozent** (bis zu 200 Prozent für kürzerer Text) für Text (aber nicht zahlen) ein, der lokalisiert wird.
-   **Wählen Sie eine Listenfeld Höhe aus, die eine ganzzahlige Anzahl von Elementen anzeigt.** Vermeiden Sie das vertikale Abschneiden von Elementen.
-   **Wählen Sie eine Listenfeld Höhe aus, die unnötigen vertikalen Bildlauf eliminiert.** Listenfelder sollten zwischen 3 und 20 Elementen angezeigt werden, ohne dass ein Bildlauf erforderlich ist. Wenn Sie die vertikale Schiebe Leiste vermeiden, ist es sinnvoll, ein Listenfeld etwas länger zu gestalten. Listen mit potenziell vielen Elementen sollten mindestens fünf Elemente anzeigen, um den Bildlauf zu vereinfachen, indem mehr Elemente gleichzeitig angezeigt werden und die Bild Lauf Leiste leichter positioniert wird.
-   **Wenn die Benutzer das Listenfeld vergrößern, können Sie das Listenfeld und dessen übergeordnetes Fenster ändern.** Auf diese Weise können Benutzer die Größe des Listen Felds nach Bedarf anpassen. Allerdings sollten in der Größe in den Listenfeldern nicht weniger als drei Elemente angezeigt werden.

## <a name="labels"></a>Bezeichnungen

**Steuerelement Bezeichnungen**

-   Alle Listenfelder benötigen Bezeichnungen. Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz. Verwenden Sie einen Doppelpunkt am Ende der Bezeichnung.

**Ausnahme:** Lassen Sie die Bezeichnung aus, wenn es sich lediglich um eine erneute Anweisung der [Haupt Anweisung](glossary.md)eines Dialog Felds handelt. In diesem Fall nimmt die main-Anweisung den Doppelpunkt (es sei denn, es handelt sich um eine Frage) und den Zugriffsschlüssel.

**Akzeptabel:** ![ Screenshot der Liste mit redundanter Bezeichnung ](images/ctrl-list-boxes-image20.png)

In diesem Beispiel gibt die Listenfeld Bezeichnung nur die main-Anweisung erneut aus.

**Besser:** ![ Screenshot der Liste ohne redundante Bezeichnung ](images/ctrl-list-boxes-image21.png)

In diesem Beispiel wird die redundante Bezeichnung entfernt, sodass die Haupt Anweisung den Doppelpunkt und die Zugriffstaste übernimmt.

-   Wenn ein Listenfeld einem Optionsfeld oder Kontrollkästchen untergeordnet ist und die Bezeichnung des Steuer Elements mit einem Doppelpunkt endet, legen Sie keine zusätzliche Bezeichnung im Listenfeld-Steuerelement ab.

![Screenshot der Schaltfläche und Liste mit derselben Bezeichnung ](images/ctrl-list-boxes-image22.png)

In diesem Beispiel ist das Listenfeld einem Optionsfeld untergeordnet und gibt seine Bezeichnung frei.

-   Weisen Sie einen eindeutigen [Zugriffsschlüssel](glossary.md)zu. Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Positionieren Sie die Bezeichnung entweder links neben dem Steuerelement, und richten Sie die Bezeichnung am linken Rand des Steuer Elements aus.
    -   Wenn sich die Bezeichnung auf der linken Seite befindet, richten Sie den Beschriftungs Text vertikal mit der ersten Textzeile im Steuerelement aus.

**Richtig:** ![ Screenshot der Liste mit der linksbündig ausgerichteten Bezeichnung oberhalb ](images/ctrl-list-boxes-image23.png)![ der Bildschirm Abbildung der Liste mit einer Text ausgerichteten Bezeichnung nach links ](images/ctrl-list-boxes-image24.png)

In diesen Beispielen wird die Bezeichnung am oberen Rand am linken Rand des Listen Felds ausgerichtet, und die Bezeichnung auf der linken Seite richtet sich nach dem Text im Listenfeld.

**Falsch:** ![ Screenshot der Liste mit einer Text ausgerichteten Bezeichnung oberhalb ](images/ctrl-list-boxes-image25.png)![ des Screenshots der Liste mit der oben ausgerichteten Bezeichnung auf der linken Seite ](images/ctrl-list-boxes-image26.png)

In diesen falschen Beispielen wird die Bezeichnung im oberen Bereich mit dem Text im Listenfeld ausgerichtet, und die Bezeichnung auf der linken Seite richtet sich nach dem oberen Rand des Listen Felds.

-   Verwenden Sie für Listenfelder mit Mehrfachauswahl eine Bezeichnung, die eindeutig angibt, dass mehrere Auswahlmöglichkeiten möglich sind. Kontrollkästchen-Bezeichnungen können weniger explizit sein.

**Richtig:** ![ Screenshot der Liste mit mindestens einer Bezeichnung ](images/ctrl-list-boxes-image27.png)

In diesem Beispiel gibt die Bezeichnung eindeutig an, dass mehrere Auswahlmöglichkeiten möglich sind.

**Falsch:** ![ Screenshot des Listen Felds mit der Bezeichnung "Add-ons" ](images/ctrl-list-boxes-image28.png)

In diesem Beispiel stellt die Bezeichnung keine offensichtlichen Informationen zur Mehrfachauswahl zur Verfügung.

**Am besten:** ![ Screenshot der Liste der Kontrollkästchen mit der Bezeichnung "Add-ons" ](images/ctrl-list-boxes-image29.png)

In diesem Beispiel geben die Kontrollkästchen eindeutig an, dass eine Mehrfachauswahl möglich ist, sodass die Bezeichnung nicht explizit sein muss.

-   Sie können Einheiten (Sekunden, Verbindungen usw.) in Klammern hinter der Bezeichnung angeben.

**Options Text**

-   Weisen Sie jeder Option einen eindeutigen Namen zu.
-   Verwenden Sie die groß [-](glossary.md)/Kleinschreibung, es sei denn, ein Element ist ein richtiges Substantiv.
-   Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, und verwenden Sie keine endinterpunktions Zeichen.
-   Verwenden Sie parallele Ausdrücke, und versuchen Sie, die Länge für alle Optionen auf denselben Wert zu beschränken.

**Anweisungs-und ergänzender Text**

-   Wenn Sie Anweisungs Text zu einem Listenfeld hinzufügen müssen, fügen Sie ihn oberhalb der Bezeichnung hinzu. Verwenden Sie vollständige Sätze mit endinterpunktions Zeichen.
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Zusätzliche Informationen, die hilfreich, aber nicht erforderlich sind, sollten kurz gehalten werden. Platzieren Sie diesen Text entweder in Klammern zwischen der Bezeichnung und dem Doppelpunkt oder ohne Klammern unterhalb des Steuer Elements.

![Screenshot der Liste mit den Kontrollkästchen und beschreibender Text ](images/ctrl-list-boxes-image30.png)

In diesem Beispiel wird zusätzlicher Text unterhalb der Liste platziert.

## <a name="documentation"></a>Dokumentation

Beim Verweis auf Listenfelder:

-   Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-und Kleinschreibung, aber nicht den Unterstrich oder Doppelpunkt des Zugriffsschlüssels. Fügen Sie die Word-Liste ein. Verweisen Sie nicht auf ein Listenfeld als Listenfeld oder Feld.
-   Verwenden Sie für Listenelemente den exakten Element Text, einschließlich der Groß-/Kleinschreibung.
-   Informationen zum Programmieren und zur anderen technischen Dokumentation finden Sie Unterlisten Felder als Listenfelder. Verwenden Sie die Liste überall.
-   Verwenden Sie SELECT, um die Benutzerinteraktion zu beschreiben.
-   Formatieren Sie nach Möglichkeit die Bezeichnung und Listenelemente mithilfe von fettem Text. Andernfalls sollten Sie die Bezeichnung und die Elemente nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Wählen Sie in der Liste **Gehe zu** der Liste die Option **Lesezeichen** aus.

