---
title: Listenfelder
description: Mit einem Listenfeld können Benutzer aus einer Gruppe von Werten auswählen, die in einer Liste angezeigt werden, die immer sichtbar ist.
ms.assetid: 620e9ff9-b367-446b-9e97-9c9d6d14f4bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0f1fe5a0c804e1c0b5b2636b4c7747caa9fb1049
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986903"
---
# <a name="list-boxes"></a>Listenfelder

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Mit einem Listenfeld können Benutzer aus einer Gruppe von Werten auswählen, die in einer Liste angezeigt werden, die immer sichtbar ist. Mit einem Listenfeld mit nur einer Auswahl wählen Benutzer ein Element aus einer Liste von sich gegenseitig ausschließenden Werten aus. Mit einem Listenfeld mit mehrfacher Auswahl wählen Benutzer 0 (null) oder mehr Elemente aus einer Liste von Werten aus.

![Screenshot des Listenfelds mit nur einer Auswahl ](images/ctrl-list-boxes-image1.png)

Ein typisches Listenfeld mit nur einer Auswahl.

> [!Note]  
> Richtlinien im Zusammenhang mit [Layout-](vis-layout.md) und [Listenansichten](ctrl-list-views.md) werden in separaten Artikeln vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Enthält die Liste Daten anstelle von Programmoptionen?** In beiden Fällen ist ein Listenfeld unabhängig von der Anzahl der Elemente eine geeignete Wahl. Im Gegensatz dazu eignen sich [Optionsfelder](ctrl-radio-buttons.md) oder [Kontrollkästchen](ctrl-check-boxes.md) nur für eine kleine Anzahl von Programmoptionen.
-   **Müssen Benutzer Sichten ändern, gruppieren, nach Spalten sortieren oder Spaltenbreite und -reihenfolge ändern?** Verwenden Sie in diesem Falle stattdessen eine [Listenansicht.](ctrl-list-views.md)
-   **Muss das Steuerelement eine Ziehquelle oder ein Ablageziel sein?** Verwenden Sie in diesem Falle stattdessen eine Listenansicht.
-   **Müssen die Listenelemente in die Zwischenablage kopiert oder aus der Zwischenablage eingefügt werden?** Verwenden Sie in diesem Falle stattdessen eine Listenansicht.

**Einzelauswahllisten**

-   **Wird das Steuerelement verwendet, um eine Option aus einer Liste von sich gegenseitig ausschließenden Werten auszuwählen?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Um mehrere Optionen auszuwählen, verwenden Sie stattdessen eine Standard-Mehrfachauswahlliste, eine Kontrollkästchenliste, einen Listen-Generator oder eine Liste hinzufügen/entfernen.
-   **Gibt es eine Standardoption, die für die meisten Benutzer in den meisten Situationen empfohlen wird?** Ist es viel wichtiger, die ausgewählte Option zu sehen, als die Alternativen zu sehen? Wenn dies der Fall ist, sollten Sie eine [Dropdownliste](/windows/desktop/uxguide/ctrl-drop) verwenden, wenn Sie die Benutzer nicht dazu ermutigen möchten, Änderungen vorzunehmen, indem Sie die Alternativen ausblenden.

![Screenshot der höchsten Qualität als Standardschaltfläche ](images/ctrl-list-boxes-image2.png)

In diesem Beispiel ist die höchste Farbqualität für die meisten Benutzer die beste Wahl, sodass eine Dropdownliste eine gute Wahl ist, um die Alternativen herunterzuspielen.

-   **Erfordert die Liste eine konstante Interaktion?** Verwenden Sie in diesem Falle eine Einzelauswahlliste, um die Interaktion zu vereinfachen.

![Screenshot der Liste der Optionen wie Nur-Text ](images/ctrl-list-boxes-image3.png)

In diesem Beispiel ändern Benutzer ständig das ausgewählte Element in der Liste Elemente anzeigen, um die Vordergrund- und Hintergrundfarben festzulegen. Die Verwendung einer Dropdownliste wäre in diesem Fall sehr mühsam.

-   **Sieht die Einstellung wie eine relative Menge aus? Würden Benutzer von sofortigem Feedback** zu den Auswirkungen von Einstellungsänderungen profitieren? In diesem Falle sollten Sie stattdessen einen [Schieberegler](ctrl-sliders.md) verwenden.
-   **Gibt es eine erhebliche hierarchische Beziehung zwischen den Listenelementen?** Verwenden Sie in [](ctrl-tree-views.md) diesem Falle stattdessen ein Strukturansichtssteuerelement.
-   **Ist der Bildschirmspeicherplatz premium?** Wenn dies der Fall ist, verwenden Sie stattdessen eine Dropdownliste, da der verwendete Bildschirmbereich fest und unabhängig von der Anzahl der Listenelemente ist.

**Standard-Mehrfachauswahllisten und Kontrollkästchenlisten**

-   **Ist die Mehrfachauswahl für die Aufgabe wichtig oder wird sie häufig verwendet?** Verwenden Sie in diesem Falle eine Kontrollkästchenliste, um die Mehrfachauswahl offensichtlich zu machen, insbesondere dann, wenn Ihre Zielbenutzer nicht erweitert sind. Vielen Benutzern wird nicht bewusst sein, dass eine Standard-Mehrfachauswahlliste die Mehrfachauswahl unterstützt. Verwenden Sie eine Standardmäßige Mehrfachauswahlliste, wenn die Kontrollkästchen zu viel Aufmerksamkeit auf die Mehrfachauswahl lenken oder zu einer zu großen Bildschirmübersicht führen würden.
-   **Ist die Stabilität der Mehrfachauswahl wichtig?** Verwenden Sie in diesem Falle eine Kontrollkästchenliste, einen Listen-Generator oder eine Liste hinzufügen/entfernen, da durch Klicken nur ein einzelnes Element gleichzeitig geändert wird. Bei einer Standard-Mehrfachauswahlliste ist es sehr einfach, alle Auswahlmöglichkeiten auch zufällig zu löschen.
-   **Wird das Steuerelement verwendet, um 0 (null) oder mehr Elemente aus einer Liste von Werten auszuwählen?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Verwenden Sie für die Auswahl eines Elements stattdessen eine Einzelauswahlliste.

**Vorschaulisten**

-   **Sind die Optionen mit Bildern einfacher auszuwählen als mit Text allein?** Verwenden Sie in diesem Falle eine Vorschauliste.

**Auflisten von Generatoren und Hinzufügen/Entfernen von Listen**

-   **Wird das Steuerelement verwendet, um 0 (null) oder mehr Elemente aus einer Liste von Werten auszuwählen?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Verwenden Sie für die Auswahl eines Elements stattdessen eine Einzelauswahlliste.
-   **Spielt die Reihenfolge der ausgewählten Elemente eine Rolle?** Wenn ja, unterstützen der Listen-Generator und das Hinzufügen/Entfernen von Listenmustern die Reihenfolge, die anderen Muster für die Mehrfachauswahl hingegen nicht.
-   **Ist es für Benutzer wichtig, eine Zusammenfassung aller ausgewählten Elemente anzuzeigen?** Wenn ja, zeigen der Listen-Generator und das Hinzufügen/Entfernen von Listenmustern nur die ausgewählten Elemente an, während die anderen Muster für die Mehrfachauswahl nicht angezeigt werden.
-   **Sind die möglichen Optionen uneingeschränkt?** Wenn ja, verwenden Sie eine Liste zum Hinzufügen/Entfernen, damit Benutzer Werte auswählen können, die derzeit nicht in der Liste enthalten sind.
-   **Ist für das Hinzufügen eines Werts zur Liste ein spezielles Dialogfeld zum Auswählen von Objekten erforderlich?** Verwenden Sie in diesem Falle eine Liste zum Hinzufügen/Entfernen, und zeigen Sie das Dialogfeld an, wenn Benutzer auf Hinzufügen klicken.
-   **Ist der Bildschirmspeicherplatz premium?** Wenn ja, verwenden Sie stattdessen eine Add-/Remove-Liste, da weniger Bildschirmbereich verwendet wird, da nicht immer der Satz von Optionen angezeigt wird.

Bei Listenfeldern **ist die Anzahl der Elemente in der Liste kein Faktor bei der Auswahl des Steuerelements,** da sie von Tausenden von Elementen bis hin zu eins für Einzelauswahllisten (und keine für Mehrfachauswahllisten) skaliert werden. Da Listenfelder für Daten verwendet werden können, ist die Anzahl der Elemente möglicherweise nicht im Voraus bekannt.

**Hinweis:** Manchmal wird ein Steuerelement, das wie ein Listenfeld aussieht, mithilfe einer Listenansicht implementiert und umgekehrt. Wenden Sie in solchen Fällen die Richtlinien basierend auf der Verwendung und nicht der Implementierung an.

## <a name="usage-patterns"></a>Verwendungsmuster

Listenfelder weisen mehrere Verwendungsmuster auf:




| Bezeichnung | Wert |
|--------|-------|
| <strong>Einzelauswahllisten</strong> Benutzern erlauben, jeweils ein Element auszuwählen. <br /> | <img src="images/ctrl-list-boxes-image4.png" alt="Screen shot of list box with one item selected " /><br /> In diesem Beispiel können Benutzer nur ein Anzeigeelement auswählen.<br /> | 
| <strong>Standardlisten für mehrfache Auswahl</strong> Benutzern das Auswählen einer beliebigen Anzahl von Elementen gestatten, einschließlich keines.<br /> | Standardlisten mit mehrfacher Auswahl weisen genau die gleiche Darstellung wie Einzelauswahllisten auf, sodass es keinen visuellen Hinweis darauf gibt, dass ein Listenfeld die Mehrfachauswahl unterstützt. Da Benutzer diese Fähigkeit ermitteln müssen, eignet sich dieses Listenmuster am besten für Aufgaben, bei denen die Mehrfachauswahl nicht wichtig ist und selten verwendet wird. <br /> Es gibt zwei verschiedene Modi für die Mehrfachauswahl: <a href="glossary.md">mehrere</a> und <a href="glossary.md">erweiterte</a>. <strong>Der erweiterte Auswahlmodus</strong> ist weitaus häufiger, wobei die Auswahl durch Ziehen oder mit UMSCHALT+KLICK und STRG+KLICK erweitert werden kann, um Gruppen zusammenhängender bzw. nicht benachbarter Werte auszuwählen. Wenn Sie im <strong>Mehrfachauswahlmodus</strong>auf ein element klicken, wird der Auswahlstatus unabhängig von der UMSCHALTTASTE und DER STRG-TASTE umgeschaltet. Aufgrund dieses ungewöhnlichen Verhaltens ist der Mehrfachauswahlmodus veraltet, und Sie sollten stattdessen Kontrollkästchenlisten verwenden.<br /><img src="images/ctrl-list-boxes-image5.png" alt="Screen shot of list box with several items selected " /><br /> In diesem Beispiel können Benutzer eine beliebige Anzahl von Elementen im Mehrfachauswahlmodus auswählen.<br /> | 
| <strong>Kontrollkästchenlisten</strong> Wie standard-Listenfelder mit mehrfacher Auswahl können Benutzer mit Kontrollkästchen eine beliebige Anzahl von Elementen auswählen, einschließlich keiner.<br /> | Im Gegensatz zu standardbasierten Mehrfachauswahllisten weisen die Kontrollkästchen eindeutig darauf hin, dass eine Mehrfachauswahl möglich ist. Verwenden Sie dieses Listenmuster für Aufgaben, bei denen die Mehrfachauswahl wichtig ist oder häufig verwendet wird. <br /><img src="images/ctrl-list-boxes-image6.png" alt="Screen shot of Toolbars check-box list " /><br /> In diesem Beispiel wählen Benutzer in der Regel mehrere Elemente aus, sodass eine Kontrollkästchenliste verwendet wird.<br /> Angesichts dieses eindeutigen Hinweises auf die Mehrfachauswahl können Sie davon ausgehen, dass Kontrollkästchenlisten standard-Mehrfachauswahllisten vorzuziehen sind. In der Praxis erfordern einige Aufgaben eine Mehrfachauswahl oder verwenden sie stark. die Verwendung einer Kontrollkästchenliste in solchen Fällen macht der Auswahl zu viel Aufmerksamkeit. Folglich <strong>sind standardbasierte Mehrfachauswahllisten weitaus häufiger.</strong><br /> | 
| <strong>Vorschaulisten</strong> Kann eine einzelne oder mehrfache Auswahl sein, aber sie zeigen eine Vorschau der Auswirkungen der Auswahl anstelle von Nur-Text an.<br /> | <img src="images/ctrl-list-boxes-image7.png" alt="Screen shot of Window Color options preview " /><br /> In diesem Beispiel zeigt eine Vorschau der einzelnen Optionen die Auswirkungen der Auswahl deutlich an, die effektiver als die Verwendung von Text allein ist.<br /> | 
| <strong>Auflisten von Generatoren</strong> Ermöglichen Sie Es Benutzern, eine Liste von Auswahlmöglichkeiten zu erstellen, indem Sie jeweils ein Element hinzufügen und optional die Listenreihenfolge festlegen.<br /> | Ein Listen-Generator besteht aus zwei Einzelauswahllisten: Die Liste auf der linken Seite ist ein fester Satz von Optionen, und die Liste auf der rechten Seite ist die Liste, die erstellt wird. Es gibt zwei Befehlsschaltflächen zwischen den Listen: <br /><ul><li>Eine Schaltfläche <strong>Hinzufügen,</strong> die die aktuell ausgewählte Option in die Liste verschiebt, die vor dem ausgewählten Element eingefügt wird. (Doppelklicken auf ein Optionselement hat die gleiche Auswirkung.)</li><li>Eine Schaltfläche <strong>Entfernen,</strong> die das ausgewählte Element aus der erstellten Liste entfernt und an die Optionsliste zurückgibt. (Doppelklicken auf ein Element in der erstellten Liste hat die gleiche Auswirkung.) Die integrierte Liste kann optional über die Befehle <strong>Nach oben</strong> und <strong>Nach unten</strong> verfügen, um die Listenelemente zu bestellen.</li></ul><img src="images/ctrl-list-boxes-image8.png" alt="Screen shot of Toolbar buttons list builder " /><br /> In diesem Beispiel wird ein Listen-Generator verwendet, um eine Symbolleiste zu erstellen, indem Elemente aus einer Reihe verfügbarer Optionen ausgewählt und deren Reihenfolge festgelegt wird.<br /> | 
| <strong>Hinzufügen/Entfernen von Listen</strong> Ermöglichen Sie Es Benutzern, eine Liste von Auswahlmöglichkeiten zu erstellen, indem Sie mindestens ein Element gleichzeitig hinzufügen und optional die Listenreihenfolge festlegen (z. B. Listen-Generatoren).<br /> | Im Gegensatz zu einem Listen-Generator wird durch Klicken auf <strong>Hinzufügen</strong> ein Dialogfeld angezeigt, in dem Elemente ausgewählt werden, die der Liste hinzugefügt werden sollen. Die Verwendung eines separaten Dialogfelds ermöglicht eine erhebliche Flexibilität bei der Auswahl von Elementen, die Sie mit einer spezialisierten Objektauswahl oder sogar mit einem allgemeinen Dialogfeld auswählen können. Im Vergleich zum Listen-Generator ist diese Variante kompakter, erfordert jedoch etwas mehr Aufwand zum Hinzufügen von Elementen. <br /><img src="images/ctrl-list-boxes-image9.png" alt="Screen shot of Menu contents list " /><br /> In diesem Beispiel können Benutzer Einem Menü Tools hinzufügen oder daraus entfernen sowie die Reihenfolge festlegen.<br /> Der Listen-Generator und das Hinzufügen/Entfernen von Listenmustern sind zwar erheblich größer als die anderen Listen mit mehrfacher Auswahl, bieten jedoch zwei einzigartige Vorteile:<br /><ul><li>Benutzer haben die Kontrolle über die Listenreihenfolge, sowohl beim Erstellen der Liste als auch nachher.</li><li>Benutzer können eine Zusammenfassung der ausgewählten Elemente überprüfen. Dies kann ein erheblicher Vorteil sein, wenn die Anzahl der Auswahlmöglichkeiten groß ist.</li></ul>Ihre Nachteile sind, dass sie viel mehr Bildschirmfläche benötigen und beim Erstellen einer großen Liste von Elementen von Grund auf schwer zu verwenden sind. Daher werden sie am besten verwendet, um kurze Listen zu erstellen oder listen zu ändern, die bereits vorhanden sind.<br /> | 




 

## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

-   **Sortieren Sie Listenelemente in einer logischen Reihenfolge,** z. B. gruppieren Sie verwandte Optionen, platzieren Sie die am häufigsten verwendeten Elemente an erster Stelle, oder verwenden Sie eine alphabetische Reihenfolge. Sortieren Sie Namen in alphabetischer Reihenfolge, Zahlen in numerischer Reihenfolge und Datumsangaben in chronologischer Reihenfolge. Listen mit 12 oder mehr Elementen sollten alphabetisch sortiert werden, um die Suche nach Elementen zu vereinfachen.

**Richtig:** ![ Screenshot der Ausrichtung (links, mitte, rechts) ](images/ctrl-list-boxes-image10.png)

In diesem Beispiel werden die Listenfeldelemente nach ihrer räumlichen Beziehung sortiert.

**Falsch:** ![ Screenshot der nicht organisierten Liste ](images/ctrl-list-boxes-image11.png)

In diesem Beispiel gibt es so viele Listenelemente, dass sie in alphabetischer Reihenfolge sortiert werden sollten.

**Richtig:** ![ Screenshot der alphabetischen Liste ](images/ctrl-list-boxes-image12.png)

In diesem Beispiel sind die Listenelemente einfacher zu finden, da sie in alphabetischer Reihenfolge sortiert sind. Das Element "Alle Windows Produkte" befindet sich jedoch unabhängig von der Sortierreihenfolge am Anfang der Liste.

-   **Platzieren Sie Optionen, die Alle oder Keine am Anfang der Liste darstellen,** unabhängig von der Sortierreihenfolge der verbleibenden Elemente.
-   **Schließen Sie Metaoptionen in Klammern ein.**

![Screenshot der Dropdownliste ohne Auswahl ](images/ctrl-list-boxes-image13.png)

In diesem Beispiel ist "(none)" eine Metaoption, da sie kein gültiger Wert für die Auswahl ist, sondern darauf hinweist, dass die Option selbst nicht verwendet wird.

-   **Verwenden Sie keine leeren Listenelemente, sondern Metaoptionen.** Benutzer wissen nicht, wie leere Elemente interpretiert werden, während die Bedeutung von Metaoptionen explizit ist.

**Falsch:** ![ Screenshot der Dropdownliste mit ausgewählter Option "Leer" ](images/ctrl-list-boxes-image14.png)

In diesem Beispiel ist die Bedeutung des leeren Elements unklar.

**Richtig:** ![ Screenshot der Dropdownliste ohne Auswahl ](images/ctrl-list-boxes-image13.png)

In diesem Beispiel wird stattdessen die Metaoption "(none)" verwendet.

### <a name="interaction"></a>Interaktion

-   **Erwägen Sie die Bereitstellung eines Doppelklickverhaltens.** Doppelklicken sollte die gleiche Auswirkung wie das Auswählen eines Elements und das Ausführen des Standardbefehls haben.
-   **Redundantes Doppelklickverhalten.** Es sollte immer eine Befehlsschaltfläche oder ein Kontextmenübefehl mit der gleichen Auswirkung vorhanden sein.
-   **Wenn Benutzer nichts mit den ausgewählten Elementen machen können, lassen Sie die Auswahl nicht zu.**

**Richtig:** ![ Screenshot der Liste der abgeschlossenen Assistentenänderungen ](images/ctrl-list-boxes-image15.png)

In diesem Listenfeld wird eine schreibgeschützte Liste von Änderungen angezeigt. es ist keine Auswahl erforderlich.

-   **Deaktivieren Sie beim Deaktivieren eines Listenfelds auch alle zugeordneten Bezeichnungen und Befehlsschaltflächen.**
-   **Verwenden Sie die Änderung des ausgewählten Elements in einem Listenfeld nicht für Folgendes:**
    -   Führen Sie Befehle aus.
    -   Zeigen Sie andere Fenster an, z. B. ein Dialogfeld, um weitere Eingaben zu erfassen.
    -   Dynamische Anzeige anderer Steuerelemente im Zusammenhang mit dem ausgewählten Steuerelement (Sprachausgaben können solche Ereignisse nicht erkennen). **Ausnahme:** Sie können statischen Text, der zum Beschreiben des ausgewählten Elements verwendet wird, dynamisch ändern.

**Akzeptabel:** ![ Screenshot der Details des ausgewählten Listenelements ](images/ctrl-list-boxes-image16.png)

In diesem Beispiel ändert das Ändern des ausgewählten Elements die Beschreibung.

-   **Vermeiden Sie horizontales Scrollen.** Mehrspaltige Listen basieren auf horizontalem Scrollen, was im Allgemeinen schwieriger zu verwenden ist als vertikales Scrollen. Listen mit mehreren Spalten, die horizontales Scrollen erfordern, können verwendet werden, wenn Sie über viele alphabetisch sortierte Elemente und ausreichend Bildschirmfläche für ein breit angeordnetes Steuerelement verfügen.

**Akzeptabel:** ![ Screenshot der Ordnerliste im Windows-Explorer ](images/ctrl-list-boxes-image17.png)

In diesem Beispiel werden mehrere Spalten verwendet, die horizontales Scrollen erfordern, da es viele Elemente und ausreichend verfügbaren Bildschirmbereich für ein breites Steuerelement gibt.

### <a name="multiple-selection-lists"></a>Mehrfachauswahllisten

-   **Erwägen Sie, die Anzahl der ausgewählten Elemente unterhalb der Liste anzuzeigen, insbesondere,** wenn Benutzer wahrscheinlich mehrere Elemente auswählen. Diese Informationen geben nicht nur nützliches Feedback, sondern geben auch deutlich an, dass das Listenfeld die Mehrfachauswahl unterstützt.

![Screenshot des Listenfelds mit vier ausgewählten Elementen ](images/ctrl-list-boxes-image5.png)

In diesem Beispiel wird die Anzahl der ausgewählten Elemente unterhalb der Liste angezeigt.

-   Sie können andere Auswahlmetriken bereitstellen, die möglicherweise aussagekräftiger sind, z. B. die für die Auswahl erforderlichen Ressourcen.

![Screenshot der Kontrollkästchenliste der Windows-Features ](images/ctrl-list-boxes-image18.png)

In diesem Beispiel ist der Speicherplatz, der für die Installation der Komponenten erforderlich ist, aussagekräftiger als die Anzahl der ausgewählten Elemente.

-   Wenn potenziell viele Listenelemente vorhanden sind und alle Elemente ausgewählt oder gelöscht werden, fügen Sie die Schaltflächen Alle auswählen und Alle befehle löschen hinzu.
-   Verwenden Sie für Standardmäßige Mehrfachauswahllisten nicht den Mehrfachauswahlmodus, da dieser Auswahlmodus veraltet ist. Verwenden Sie für ein entsprechendes Verhalten stattdessen eine Kontrollkästchenliste.

### <a name="default-values"></a>Standardwerte

-   **Wählen Sie standardmäßig die sicherste Option (um daten- oder systemzugriffsverlust zu verhindern) und die sicherste Option aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequemste Option aus.

**Ausnahme:** Wählen Sie keine Elemente aus, wenn das Steuerelement eine Eigenschaft in einem [gemischten Zustand](glossary.md)darstellt. Dies geschieht, wenn eine Eigenschaft für mehrere Objekte angezeigt wird, die nicht über die gleiche Einstellung verfügen.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größen- und Abstände

![Screenshot der Größen- und Abstände von Listenboxen ](images/ctrl-list-boxes-image19.png)

Empfohlene Größen- und Abstände für Listenfelder.

-   **Wählen Sie eine Listenfeldbreite aus, die für die längsten gültigen Daten geeignet ist.** Standardlistenfelder können nicht horizontal gescrollt werden, sodass Benutzer nur sehen können, was im Steuerelement sichtbar ist.
-   **Fügen Sie zusätzliche 30 Prozent** (bis zu 200 Prozent für kürzeren Text) für jeden Text (aber keine Zahlen) ein, der lokalisiert wird.
-   **Wählen Sie eine Listenfeldhöhe aus, die eine ganzzahligen Anzahl von Elementen anzeigt.** Vermeiden Sie das vertikale Abschneiden von Elementen.
-   **Wählen Sie eine Listenfeldhöhe aus, die unnötiges vertikales Scrollen überflüssig macht.** Listenfelder sollten zwischen 3 und 20 Elemente anzeigen, ohne scrollen zu müssen. Ziehen Sie in Betracht, ein Listenfeld etwas länger zu gestalten, wenn dadurch die vertikale Bildlaufleiste entfernt wird. Listen mit potenziell vielen Elementen sollten mindestens fünf Elemente anzeigen, um das Scrollen zu vereinfachen, indem mehr Elemente gleichzeitig angezeigt werden und die Position der Bildlaufleiste vereinfacht wird.
-   **Wenn Benutzer davon profitieren, das Listenfeld zu vergrößern, können Sie die Größe des Listenfelds und des übergeordneten Fensters ändern.** Auf diese Weise können Benutzer die Größe des Listenfelds nach Bedarf anpassen. In Listenfeldern mit größenveränderlicher Größe sollten jedoch nicht weniger als drei Elemente angezeigt werden.

## <a name="labels"></a>Bezeichnungen

**Steuerelementbezeichnungen**

-   Alle Listenfelder benötigen Bezeichnungen. Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz. verwenden Sie einen Doppelpunkt am Ende der Bezeichnung.

**Ausnahme:** Lassen Sie die Bezeichnung aus, wenn es sich lediglich um eine Neuanordnung der [Hauptanweisung](glossary.md)eines Dialogfelds handelt. In diesem Fall nimmt die Hauptanweisung den Doppelpunkt (sofern es sich nicht um eine Frage handelt) und den Zugriffsschlüssel.

**Akzeptabel:** ![ Screenshot der Liste mit redundanter Bezeichnung ](images/ctrl-list-boxes-image20.png)

In diesem Beispiel gibt die Listenfeldbezeichnung nur die Hauptanweisung an.

**Besser:** ![ Screenshot der Liste von ohne redundante Bezeichnung ](images/ctrl-list-boxes-image21.png)

In diesem Beispiel wird die redundante Bezeichnung entfernt, sodass die Main-Anweisung den Doppelpunkt und den Zugriffsschlüssel annimmt.

-   Wenn ein Listenfeld einem Optionsfeld oder Kontrollkästchen untergeordnet ist und durch die Bezeichnung dieses Steuerelements eingeführt wird, die mit einem Doppelpunkt endet, legen Sie keine zusätzliche Bezeichnung in das Listenfeld-Steuerelement ein.

![Screenshot der Schaltfläche und Liste mit derselben Bezeichnung ](images/ctrl-list-boxes-image22.png)

In diesem Beispiel ist das Listenfeld einem Optionsfeld untergeordnet und teilt seine Bezeichnung.

-   Weisen Sie einen eindeutigen [Zugriffsschlüssel zu.](glossary.md) Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie [die Groß-/Großschreibung im Satzformat.](glossary.md)
-   Positionieren Sie die Bezeichnung entweder links vom Steuerelement oder oberhalb des Steuerelements, und richten Sie die Bezeichnung am linken Rand des Steuerelements aus.
    -   Wenn sich die Bezeichnung auf der linken Seite befindet, richten Sie den Bezeichnungstext vertikal an der ersten Textzeile im Steuerelement aus.

**Richtig:** ![ Screenshot der Liste mit linksbündig ausgerichteter Bezeichnung über ](images/ctrl-list-boxes-image23.png)![ dem Screenshot der Liste mit nach links ausgerichteter Beschriftung ](images/ctrl-list-boxes-image24.png)

In diesen Beispielen wird die Bezeichnung oben am linken Rand des Listenfelds und die Bezeichnung links am Text im Listenfeld ausgerichtet.

**Falsch:** ![ Screenshot der Liste mit textbündiger Bezeichnung oberhalb ](images/ctrl-list-boxes-image25.png)![ des Screenshots der Liste mit der am oberen Rand ausgerichteten Bezeichnung auf der linken Seite ](images/ctrl-list-boxes-image26.png)

In diesen falschen Beispielen wird die Bezeichnung oben am Text im Listenfeld ausgerichtet, und die Bezeichnung links am oberen Rand des Listenfelds.

-   Verwenden Sie für Listenfelder mit mehrfacher Auswahl eine Bezeichnung, die eindeutig angibt, dass mehrere Auswahlmöglichkeiten möglich sind. Kontrollkästchenlistenbezeichnungen können weniger explizit sein.

**Richtig:** ![ Screenshot der Liste mit einer oder mehreren Bezeichnungen auswählen ](images/ctrl-list-boxes-image27.png)

In diesem Beispiel gibt die Bezeichnung deutlich an, dass eine Mehrfachauswahl möglich ist.

**Falsch:** ![ Screenshot des Listenfelds mit der Bezeichnung "Add-Ons" ](images/ctrl-list-boxes-image28.png)

In diesem Beispiel stellt die Bezeichnung keine offensichtlichen Informationen zur Mehrfachauswahl bereit.

**Am besten geeignet:** ![ Screenshot der Kontrollkästchenliste mit der Bezeichnung "Add-Ons" ](images/ctrl-list-boxes-image29.png)

In diesem Beispiel weisen die Kontrollkästchen deutlich darauf hin, dass mehrere Auswahlmöglichkeiten möglich sind, sodass die Bezeichnung nicht explizit sein muss.

-   Sie können Einheiten (Sekunden, Verbindungen usw.) in Klammern nach der Bezeichnung angeben.

**Optionstext**

-   Weisen Sie jeder Option einen eindeutigen Namen zu.
-   Verwenden Sie [großgeschriebene Sätze,](glossary.md)es sei denn, ein Element ist ein richtiges Nomen.
-   Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, und verwenden Sie keine Endpunktion.
-   Verwenden Sie parallele Ausdrücke, und versuchen Sie, die Länge für alle Optionen ungefähr gleich zu halten.

**Anweisungs- und Ergänzender Text**

-   Wenn Sie Anweisungstext zu einem Listenfeld hinzufügen müssen, fügen Sie es über der Bezeichnung hinzu. Verwenden Sie vollständige Sätze mit endender Interpunktion.
-   Verwenden Sie [die Groß-/Großschreibung im Satzformat.](glossary.md)
-   Zusätzliche Informationen, die hilfreich, aber nicht notwendig sind, sollten kurz gehalten werden. Platzieren Sie diesen Text entweder in Klammern zwischen der Bezeichnung und dem Doppelpunkt oder ohne Klammern unterhalb des Steuerelements.

![Screenshot der Kontrollkästchenliste und des beschreibenden Texts ](images/ctrl-list-boxes-image30.png)

In diesem Beispiel wird ergänzender Text unterhalb der Liste platziert.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Listenfelder:

-   Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Großschreibung, aber nicht den Unterstrich oder Doppelpunkt des Zugriffsschlüssels. Schließen Sie die Wortliste ein. Verweisen Sie nicht auf ein Listenfeld als Listenfeld oder Feld.
-   Verwenden Sie für Listenelemente den genauen Elementtext, einschließlich der Groß-/Großschreibung.
-   In der Programmierung und anderen technischen Dokumentationen werden Listenfelder als Listenfelder bezeichnet. Verwenden Sie überall sonst list.
-   Verwenden Sie select, um die Benutzerinteraktion zu beschreiben.
-   Formatieren Sie nach Möglichkeit die Bezeichnung und Listenelemente mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung und die Elemente nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

Beispiel: Wählen Sie in der Liste **Gehe zu was** die Option **Lesezeichen** aus.

