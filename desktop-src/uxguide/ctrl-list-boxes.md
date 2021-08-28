---
title: Listenfelder
description: Mit einem Listenfeld können Benutzer aus einer Gruppe von Werten auswählen, die in einer Liste angezeigt werden, die immer sichtbar ist.
ms.assetid: 620e9ff9-b367-446b-9e97-9c9d6d14f4bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0476b53590cc6e8dcc691faf95be1a851889936e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481746"
---
# <a name="list-boxes"></a>Listenfelder

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

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
-   **Gibt es eine Standardoption, die für die meisten Benutzer in den meisten Situationen empfohlen wird?** Ist es viel wichtiger, die ausgewählte Option als die Alternativen zu sehen? Wenn dies der Fall ist, sollten Sie eine [Dropdownliste](/windows/desktop/uxguide/ctrl-drop) verwenden, wenn Sie die Benutzer nicht dazu auffordern möchten, Änderungen vorzunehmen, indem Sie die Alternativen ausblenden.

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
-   **Sind die möglichen Optionen uneingeschränkt?** Verwenden Sie in diesem Falle eine Liste zum Hinzufügen/Entfernen, damit Benutzer Werte auswählen können, die derzeit nicht in der Liste enthalten sind.
-   **Ist für das Hinzufügen eines Werts zur Liste ein spezielles Dialogfeld zum Auswählen von Objekten erforderlich?** Verwenden Sie in diesem Falle eine Liste zum Hinzufügen/Entfernen, und zeigen Sie das Dialogfeld an, wenn Benutzer auf Hinzufügen klicken.
-   **Ist der Bildschirmspeicherplatz premium?** Wenn ja, verwenden Sie stattdessen eine Add-/Remove-Liste, da weniger Bildschirmbereich verwendet wird, da nicht immer der Satz von Optionen angezeigt wird.

Bei Listenfeldern **ist die Anzahl der Elemente in der Liste kein Faktor bei der Auswahl des Steuerelements,** da sie von Tausenden von Elementen bis hin zu eins für Einzelauswahllisten (und keine für Mehrfachauswahllisten) skaliert werden. Da Listenfelder für Daten verwendet werden können, ist die Anzahl der Elemente möglicherweise nicht im Voraus bekannt.

**Hinweis:** Manchmal wird ein Steuerelement, das wie ein Listenfeld aussieht, mithilfe einer Listenansicht implementiert und umgekehrt. Wenden Sie in solchen Fällen die Richtlinien basierend auf der Verwendung und nicht der Implementierung an.

## <a name="usage-patterns"></a>Verwendungsmuster

Listenfelder weisen mehrere Verwendungsmuster auf:




| | | <strong>Einzelauswahllisten</strong> Benutzern erlauben, jeweils ein Element auszuwählen. <br /> | <img src="images/ctrl-list-boxes-image4.png" alt="Screen shot of list box with one item selected " /><br /> In diesem Beispiel können Benutzer nur ein Anzeigeelement auswählen.<br /> | | <strong>Standardlisten für mehrfache Auswahl</strong> Benutzern das Auswählen einer beliebigen Anzahl von Elementen gestatten, einschließlich keines.<br /> | Standard-Mehrfachauswahllisten weisen genau die gleiche Darstellung wie Einzelauswahllisten auf, sodass es keinen visuellen Hinweis gibt, dass ein Listenfeld die Mehrfachauswahl unterstützt. Da Benutzer diese Fähigkeit ermitteln müssen, wird dieses Listenmuster am besten für Aufgaben verwendet, bei denen die Mehrfachauswahl nicht wichtig ist und selten verwendet wird. <br /> Es gibt zwei verschiedene Modi für die Mehrfachauswahl: <a href="glossary.md">mehrere</a> und <a href="glossary.md">erweiterte</a>. <strong>Der erweiterte Auswahlmodus</strong> ist weitaus häufiger, wobei die Auswahl durch Ziehen oder mit UMSCHALT+KLICK und STRG+KLICK erweitert werden kann, um Gruppen zusammenhängender bzw. nicht benachbarter Werte auszuwählen. Wenn Sie im <strong>Mehrfachauswahlmodus</strong>auf ein element klicken, wird der Auswahlstatus unabhängig von der UMSCHALTTASTE und DER STRG-TASTE umgeschaltet. Aufgrund dieses ungewöhnlichen Verhaltens ist der Mehrfachauswahlmodus veraltet, und Sie sollten stattdessen Kontrollkästchenlisten verwenden.<br /><img src="images/ctrl-list-boxes-image5.png" alt="Screen shot of list box with several items selected " /><br /> In diesem Beispiel können Benutzer eine beliebige Anzahl von Elementen im Mehrfachauswahlmodus auswählen.<br /> | | <strong>Kontrollkästchenlisten</strong> Wie standardmäßige Mehrfachauswahllisten können Benutzer mit Kontrollkästchen eine beliebige Anzahl von Elementen auswählen, einschließlich keiner.<br /> | Im Gegensatz zu standardbasierten Mehrfachauswahllisten weisen die Kontrollkästchen eindeutig darauf hin, dass eine Mehrfachauswahl möglich ist. Verwenden Sie dieses Listenmuster für Aufgaben, bei denen die Mehrfachauswahl wichtig ist oder häufig verwendet wird. <br /><img src="images/ctrl-list-boxes-image6.png" alt="Screen shot of Toolbars check-box list " /><br /> In diesem Beispiel wählen Benutzer in der Regel mehrere Elemente aus, sodass eine Kontrollkästchenliste verwendet wird.<br /> Angesichts dieses eindeutigen Hinweises auf die Mehrfachauswahl können Sie davon ausgehen, dass Kontrollkästchenlisten standard-Mehrfachauswahllisten vorzuziehen sind. In der Praxis erfordern einige Aufgaben eine Mehrfachauswahl oder verwenden sie stark. Die Verwendung einer Kontrollkästchenliste in solchen Fällen macht der Auswahl zu viel Aufmerksamkeit. Folglich sind Standardlisten für <strong>die Mehrfachauswahl weitaus häufiger.</strong><br /> | | <strong>Vorschaulisten</strong> Kann eine einzelne oder mehrfache Auswahl sein, aber sie zeigen eine Vorschau der Auswirkungen der Auswahl anstelle von Nur-Text an.<br /> | <img src="images/ctrl-list-boxes-image7.png" alt="Screen shot of Window Color options preview " /><br /> In diesem Beispiel zeigt eine Vorschau der einzelnen Optionen die Auswirkungen der Auswahl deutlich an, die effektiver als die Verwendung von Text allein ist.<br /> | | <strong>Auflisten von Generatoren</strong> Ermöglichen Sie Es Benutzern, eine Liste von Auswahlmöglichkeiten zu erstellen, indem Sie jeweils ein Element hinzufügen und optional die Listenreihenfolge festlegen.<br /> | Ein Listen-Generator besteht aus zwei Einzelauswahllisten: Die Liste auf der linken Seite ist ein fester Satz von Optionen, und die Liste auf der rechten Seite ist die Liste, die erstellt wird. Es gibt zwei Befehlsschaltflächen zwischen den Listen: <br /><ul><li>Eine Schaltfläche <strong>Hinzufügen,</strong> die die aktuell ausgewählte Option in die Liste verschiebt, die vor dem ausgewählten Element eingefügt wird. (Doppelklicken auf ein Optionselement hat die gleiche Auswirkung.)</li><li>Eine <strong>Schaltfläche Entfernen,</strong> die das ausgewählte Element aus der erstellten Liste entfernt und an die Optionsliste zurückgibt. (Doppelklicken auf ein Element in der erstellten Liste hat die gleiche Auswirkung.) Die integrierte Liste kann optional über die <strong>Befehle Nach oben</strong> und Nach unten <strong>verfügen,</strong> um die Listenelemente zu bestellen.</li></ul><img src="images/ctrl-list-boxes-image8.png" alt="Screen shot of Toolbar buttons list builder " /><br /> In diesem Beispiel wird ein Listen-Generator verwendet, um eine Symbolleiste zu erstellen, indem Elemente aus einer Reihe verfügbarer Optionen ausgewählt und deren Reihenfolge festgelegt wird.<br /> | | <strong>Hinzufügen/Entfernen von Listen</strong> Ermöglichen Sie Es Benutzern, eine Liste von Auswahlmöglichkeiten zu erstellen, indem Sie ein oder mehrere Elemente gleichzeitig hinzufügen und optional die Listen reihenfolge festlegen (z. B. Listen-Generatoren).<br /> | Im Gegensatz zu einem Listen-Generator zeigt das Klicken <strong>auf</strong> Hinzufügen ein Dialogfeld an, in dem Elemente ausgewählt werden, die der Liste hinzugefügt werden. Die Verwendung eines separaten Dialogfelds ermöglicht eine erhebliche Flexibilität bei der Auswahl von Elementen, die Sie mit einer speziellen Objektauswahl oder sogar einem allgemeinen Dialog auswählen können. Im Vergleich zum Listen-Generator ist diese Variante kompakter, erfordert jedoch etwas mehr Aufwand, um Elemente hinzuzufügen. <br /><img src="images/ctrl-list-boxes-image9.png" alt="Screen shot of Menu contents list " /><br /> In diesem Beispiel können Benutzer Tools zu einem Menü hinzufügen oder daraus entfernen sowie die Reihenfolge festlegen.<br /> Der Listen-Generator und das Hinzufügen/Entfernen von Listenmustern sind zwar deutlich größer als die anderen Mehrfachauswahllisten, bieten jedoch zwei besondere Vorteile:<br /><ul><li>Benutzer haben die Kontrolle über die Reihenfolge der Listen, sowohl beim Erstellen der Liste als auch danach.</li><li>Benutzer können eine Zusammenfassung der ausgewählten Elemente überprüfen. Dies kann ein großer Vorteil sein, wenn die Anzahl der Auswahlmöglichkeiten groß ist.</li></ul>Ihre Nachteile sind, dass sie viel mehr Platz auf dem Bildschirm benötigen und schwierig zu verwenden sein können, wenn sie eine große Liste von Elementen von Grund auf neu erstellen. Daher werden sie am besten verwendet, um bereits vorhandene Kurzlisten zu erstellen oder Listen zu ändern.<br /> | 




 

## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

-   **Sortieren Sie Listenelemente in einer logischen Reihenfolge,** z. B. gruppieren sie verwandte Optionen, platzieren Sie die am häufigsten verwendeten Elemente an erster Stelle, oder verwenden Sie eine alphabetische Reihenfolge. Sortieren Sie Namen in alphabetischer Reihenfolge, Zahlen in numerischer Reihenfolge und Datumsangaben in chronologischer Reihenfolge. Listen mit 12 oder mehr Elementen sollten alphabetisch sortiert werden, damit Elemente leichter zu finden sind.

**Richtig:** ![ Screenshot der Ausrichtung (links, zentriert, rechts) ](images/ctrl-list-boxes-image10.png)

In diesem Beispiel werden die Listenfeldelemente nach ihrer räumlichen Beziehung sortiert.

**Falsch:** ![ Screenshot der nicht organisierten Liste ](images/ctrl-list-boxes-image11.png)

In diesem Beispiel gibt es so viele Listenelemente, dass sie in alphabetischer Reihenfolge sortiert werden sollten.

**Richtig:** ![ Screenshot der alphabetischen Liste ](images/ctrl-list-boxes-image12.png)

In diesem Beispiel sind die Listenelemente leichter zu finden, da sie in alphabetischer Reihenfolge sortiert sind. Das Element "Alle Windows" befindet sich jedoch am Anfang der Liste, unabhängig von der Sortierreihenfolge.

-   **Platzieren Sie Optionen, die All oder None** darstellen, am Anfang der Liste, unabhängig von der Sortierreihenfolge der verbleibenden Elemente.
-   **Schließen Sie Metaoptionen in Klammern ein.**

![Screenshot der Dropdownliste ohne Auswahl ](images/ctrl-list-boxes-image13.png)

In diesem Beispiel ist "(none)" eine Metaoption, da sie kein gültiger Wert für die Auswahl ist, sondern darauf hinweist, dass die Option selbst nicht verwendet wird.

-   **Verwenden Sie stattdessen Metaoptionen, wenn Sie keine leeren Listenelemente haben.** Benutzer wissen nicht, wie leere Elemente interpretiert werden, wohingegen die Bedeutung von Metaoptionen explizit ist.

**Falsch:** ![ Screenshot der Dropdownliste mit ausgewählter Option "Leer" ](images/ctrl-list-boxes-image14.png)

In diesem Beispiel ist die Bedeutung des leeren Elements unklar.

**Richtig:** ![ Screenshot der Dropdownliste ohne Auswahl ](images/ctrl-list-boxes-image13.png)

In diesem Beispiel wird stattdessen die Metaoption "(none)" verwendet.

### <a name="interaction"></a>Interaktion

-   **Erwägen Sie die Bereitstellung eines Doppelklickverhaltens.** Doppelklicken sollte die gleiche Wirkung wie das Auswählen eines Elements und das Ausführen des Standardbefehls haben.
-   **Machen Sie das Doppelklickverhalten redundant.** Es sollte immer eine Befehlsschaltfläche oder ein Kontextmenübefehl mit der gleichen Auswirkung geben.
-   **Wenn Benutzer die ausgewählten Elemente nicht verwenden können, lassen Sie die Auswahl nicht zu.**

**Richtig:** ![ Screenshot der Liste der abgeschlossenen Änderungen des Assistenten ](images/ctrl-list-boxes-image15.png)

In diesem Listenfeld wird eine schreibgeschützte Liste von Änderungen angezeigt. es ist keine Auswahl notwendig.

-   **Deaktivieren Sie beim Deaktivieren eines Listenfelds auch alle zugeordneten Bezeichnungen und Befehlsschaltflächen.**
-   **Verwenden Sie die Änderung des ausgewählten Elements in einem Listenfeld nicht für:**
    -   Führen Sie Befehle aus.
    -   Zeigen Sie andere Fenster an, z. B. ein Dialogfeld, um weitere Eingaben zu erfassen.
    -   Dynamisches Anzeigen anderer Steuerelemente im Zusammenhang mit dem ausgewählten Steuerelement (Sprachanzeigen können solche Ereignisse nicht erkennen). **Ausnahme:** Sie können statischen Text, der zum Beschreiben des ausgewählten Elements verwendet wird, dynamisch ändern.

**Akzeptabel:** ![ Screenshot der Details des ausgewählten Listenelements ](images/ctrl-list-boxes-image16.png)

In diesem Beispiel ändert das Ändern des ausgewählten Elements die Beschreibung.

-   **Vermeiden Sie horizontales Scrollen.** Mehrteilige Listen basieren auf horizontalem Scrollen, was im Allgemeinen schwieriger zu verwenden ist als vertikales Scrollen. Listen mit mehrerenColumns, die horizontales Scrollen erfordern, können verwendet werden, wenn Sie über viele alphabetisch sortierte Elemente und ausreichend Bildschirmfläche für ein breites Steuerelement verfügen.

**Akzeptabel:** ![ Screenshot der Liste der Ordner im Windows-Explorer ](images/ctrl-list-boxes-image17.png)

In diesem Beispiel werden mehrere Spalten verwendet, die horizontales Scrollen erfordern, da viele Elemente und viel verfügbarer Bildschirmbereich für ein breites Steuerelement vorhanden sind.

### <a name="multiple-selection-lists"></a>Mehrfachauswahllisten

-   **Erwägen Sie, die Anzahl der ausgewählten Elemente unterhalb der Liste anzuzeigen, insbesondere,** wenn Benutzer wahrscheinlich mehrere Elemente auswählen. Diese Informationen geben nicht nur nützliches Feedback, sondern zeigen auch deutlich an, dass das Listenfeld mehrfache Auswahl unterstützt.

![Screenshot des Listenfelds mit vier ausgewählten Elementen ](images/ctrl-list-boxes-image5.png)

In diesem Beispiel wird die Anzahl der ausgewählten Elemente unterhalb der Liste angezeigt.

-   Sie können andere Auswahlmetriken bereitstellen, die sinnvoller sein können, z. B. die ressourcen, die für die Auswahl erforderlich sind.

![Screenshot der Kontrollkästchenliste mit Windows-Features ](images/ctrl-list-boxes-image18.png)

In diesem Beispiel ist der speicherplatz, der zum Installieren der Komponenten erforderlich ist, aussagekräftiger als die Anzahl der ausgewählten Elemente.

-   Wenn potenziell viele Listenelemente verfügbar sind und sie wahrscheinlich alle auswählen oder löschen, fügen Sie Alle auswählen und Alle Löschen-Befehlsschaltflächen hinzu.
-   Verwenden Sie für Standardmäßige Mehrfachauswahllisten nicht den Mehrfachauswahlmodus, da dieser Auswahlmodus veraltet ist. Verwenden Sie für ein entsprechendes Verhalten stattdessen eine Kontrollkästchenliste.

### <a name="default-values"></a>Standardwerte

-   **Wählen Sie standardmäßig die sicherste Option (um Datenverlust oder Systemzugriff zu verhindern) und die sicherste Option aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequemste Option aus.

**Ausnahme:** Wählen Sie keine Elemente aus, wenn das [](glossary.md)Steuerelement eine Eigenschaft in einem gemischten Zustand darstellt. Dies geschieht, wenn eine Eigenschaft für mehrere Objekte angezeigt wird, die nicht die gleiche Einstellung haben.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstand

![Screenshot: Größen- und Abstandsgröße für Listenfeld ](images/ctrl-list-boxes-image19.png)

Empfohlene Größe und Abstand für Listenfelder.

-   **Wählen Sie eine Listenfeldbreite aus, die für die längsten gültigen Daten geeignet ist.** Standardlistenfelder können nicht horizontal gescrollt werden, sodass Benutzer nur sehen können, was im Steuerelement sichtbar ist.
-   **Schließen Sie zusätzliche 30 Prozent** (bis zu 200 Prozent für kürzeren Text) für text (aber keine Zahlen) ein, die lokalisiert werden.
-   **Wählen Sie eine Listenfeldhöhe aus, die eine ganzzahliger Anzahl von Elementen anzeigt.** Vermeiden Sie das vertikale Abschneiden von Elementen.
-   **Wählen Sie eine Listenfeldhöhe aus, die unnötiges vertikales Scrollen verhindert.** Listenfelder sollten zwischen 3 und 20 Elemente anzeigen, ohne dass ein Bildlauf notwendig ist. Erwägen Sie, ein Listenfeld etwas länger zu erstellen, wenn dadurch die vertikale Scrollleiste entfernt wird. Listen mit potenziell vielen Elementen sollten mindestens fünf Elemente anzeigen, um das Scrollen zu erleichtern, indem mehr Elemente gleichzeitig angezeigt werden und die Position der Scrollleiste vereinfacht wird.
-   **Wenn Benutzer davon profitieren, das Listenfeld zu vergrößern, können Sie die Größe des Listenfelds und des übergeordneten Fensters ändern.** Auf diese Weise können Benutzer die Größe des Listenfelds nach Bedarf anpassen. In Listenfeldern, die die Größe ändern können, sollten jedoch nicht weniger als drei Elemente angezeigt werden.

## <a name="labels"></a>Bezeichnungen

**Steuerelementbezeichnungen**

-   Alle Listenfelder benötigen Bezeichnungen. Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz. verwenden Sie einen Doppelpunkt am Ende der Bezeichnung.

**Ausnahme:** Lassen Sie die Bezeichnung weg, wenn es sich lediglich um eine Neubeschriftung der Hauptanweisung eines [Dialogfelds handelt.](glossary.md) In diesem Fall übernimmt die main-Anweisung den Doppelpunkt (es sei denn, es ist eine Frage) und den Zugriffsschlüssel.

**Akzeptabel:** ![ Screenshot der Liste mit redundanter Bezeichnung ](images/ctrl-list-boxes-image20.png)

In diesem Beispiel gibt die Bezeichnung des Listenfelds nur die Main-Anweisung wieder.

**Besser:** ![ Screenshot der Liste ohne redundante Bezeichnung ](images/ctrl-list-boxes-image21.png)

In diesem Beispiel wird die redundante Bezeichnung entfernt, sodass die main-Anweisung den Doppelpunkt und den Zugriffsschlüssel übernimmt.

-   Wenn ein Listenfeld einem Optionsfeld oder Kontrollkästchen untergeordnet ist und durch die Bezeichnung dieses Steuerelements eingeführt wird, die mit einem Doppelpunkt endet, legen Sie keine zusätzliche Bezeichnung im Listenfeld-Steuerelement ab.

![Screenshot von Schaltfläche und Liste mit der gleichen Bezeichnung ](images/ctrl-list-boxes-image22.png)

In diesem Beispiel ist das Listenfeld einem Optionsfeld untergeordnet und teilt seine Bezeichnung.

-   Weisen Sie einen [eindeutigen Zugriffsschlüssel zu.](glossary.md) Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)
-   Positionieren Sie die Bezeichnung entweder links vom Steuerelement oder über dem Steuerelement, und richten Sie die Bezeichnung am linken Rand des Steuerelements aus.
    -   Wenn sich die Bezeichnung links befindet, richten Sie den Bezeichnungstext vertikal an der ersten Textzeile im Steuerelement aus.

**Richtig:** ![ Screenshot der Liste mit linksbündiger Bezeichnung oberhalb des Screenshots der Liste ](images/ctrl-list-boxes-image23.png)![ mit textbündiger Bezeichnung auf der linken Seite ](images/ctrl-list-boxes-image24.png)

In diesen Beispielen wird die Bezeichnung oben am linken Rand des Listenfelds ausgerichtet, und die Bezeichnung auf der linken Seite wird am Text im Listenfeld ausgerichtet.

**Falsch:** ![ Screenshot der Liste mit textbündiger Bezeichnung oberhalb des Screenshots der Liste mit oben ](images/ctrl-list-boxes-image25.png)![ ausgerichteter Bezeichnung auf der linken Seite ](images/ctrl-list-boxes-image26.png)

In diesen falschen Beispielen wird die Bezeichnung oben am Text im Listenfeld ausgerichtet, und die Bezeichnung auf der linken Seite wird am oberen Ende des Listenfelds ausgerichtet.

-   Verwenden Sie für Listenfelder mit mehrfacher Auswahl eine Bezeichnung, die deutlich angibt, dass eine Mehrfachauswahl möglich ist. Kontrollkästchenlistenbezeichnungen können weniger explizit sein.

**Richtig:** ![ Screenshot der Liste mit auswahl einer oder mehrere Bezeichnungen ](images/ctrl-list-boxes-image27.png)

In diesem Beispiel gibt die Bezeichnung eindeutig an, dass eine Mehrfachauswahl möglich ist.

**Falsch:** ![ Screenshot des Listenfelds mit Add-On-Bezeichnung ](images/ctrl-list-boxes-image28.png)

In diesem Beispiel stellt die Bezeichnung keine offensichtlichen Informationen zur Mehrfachauswahl zur Verfügung.

**Am besten:** ![ Screenshot der Kontrollkästchenliste mit Add-On-Bezeichnung ](images/ctrl-list-boxes-image29.png)

In diesem Beispiel weisen die Kontrollkästchen eindeutig darauf hin, dass eine Mehrfachauswahl möglich ist, sodass die Bezeichnung nicht explizit sein muss.

-   Sie können Einheiten (Sekunden, Verbindungen und so weiter) in Klammern nach der Bezeichnung angeben.

**Optionstext**

-   Weisen Sie jeder Option einen eindeutigen Namen zu.
-   Verwenden [Sie Die Groß-/Groß-/Formatvorlage,](glossary.md)es sei denn, ein Element ist ein richtiges Nomen.
-   Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, und verwenden Sie keine endende Interpunktion.
-   Verwenden Sie parallele Formulierungen, und versuchen Sie, die Länge für alle Optionen ungefähr gleich zu halten.

**Anweisungstext und ergänzender Text**

-   Wenn Sie Anweisungstext zu einem Listenfeld hinzufügen müssen, fügen Sie ihn über der Bezeichnung hinzu. Verwenden Sie vollständige Sätze mit endender Interpunktion.
-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)
-   Zusätzliche Informationen, die hilfreich, aber nicht erforderlich sind, sollten kurz gehalten werden. Platzieren Sie diesen Text entweder in Klammern zwischen der Bezeichnung und dem Doppelpunkt oder ohne Klammern unterhalb des Steuerelements.

![Screenshot der Kontrollkästchenliste und beschreibender Text ](images/ctrl-list-boxes-image30.png)

In diesem Beispiel wird ergänzender Text unterhalb der Liste platziert.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Listenfelder:

-   Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Unterstriche, aber schließen Sie nicht den Unterstrich oder Doppelpunkt des Zugriffsschlüssels ein. Schließen Sie die Wortliste ein. Verweisen Sie nicht auf ein Listenfeld als Listenfeld oder Feld.
-   Verwenden Sie für Listenelemente den genauen Elementtext, einschließlich der Groß-/Groß-/Groß-//Unterform.
-   Verweisen Sie in der Programmierung und anderen technischen Dokumentationen auf Listenfelder als Listenfelder. Verwenden Sie überall sonst list.
-   Verwenden Sie select, um die Benutzerinteraktion zu beschreiben.
-   Formatieren Sie nach Möglichkeit die Bezeichnung und Listenelemente mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung und die Elemente nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Wählen Sie in **der Liste Zu was wechseln** die Option **Lesezeichen aus.**

