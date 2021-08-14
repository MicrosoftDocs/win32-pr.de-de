---
title: Kombinationsfelder für Dropdownlisten
description: Mit einer Dropdownliste oder einem Kombinationsfeld treffen Benutzer eine Auswahl zwischen einer Liste von sich gegenseitig ausschließenden Werten.
ms.assetid: dbe88cf1-7946-4343-bc16-ce12be7ce205
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e74589da084a9f4c9f950336b3093452988052b57aba42e6a7a8f449f24a254f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966274"
---
# <a name="drop-down-lists--combo-boxes"></a>Dropdownlisten & Kombinationsfelder

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Mit einer Dropdownliste oder einem Kombinationsfeld treffen Benutzer eine Auswahl zwischen einer Liste von sich gegenseitig ausschließenden Werten. Benutzer können nur eine Option auswählen. Bei einer Standard-Dropdownliste sind Benutzer auf Die Auswahlmöglichkeiten in der Liste beschränkt, aber mit einem Kombinationsfeld können sie eine Auswahl eingeben, die nicht in der Liste enthalten ist.

![Screenshot des Kombinationsfelds "Erinnerungszeit" ](images/ctrl-drop-image1.png)

Ein typisches Kombinationsfeld.

Die folgenden Begriffe sind wichtig zu verstehen, wenn Sie diesen Artikel lesen:

-   Ein Standardlistenfeld ist ein Feld, das eine Liste mit mehreren Elementen enthält, wobei mehrere Elemente sichtbar sind.
-   Eine Dropdownliste ist eine Liste, in der das ausgewählte Element immer sichtbar ist, und die anderen bei Bedarf durch Klicken auf eine Dropdownschaltfläche sichtbar sind.
-   Ein Kombinationsfeld ist eine Kombination aus einem Standardlistenfeld oder einer Dropdownliste und einem bearbeitbaren [Textfeld,](ctrl-text-boxes.md)sodass Benutzer einen Wert eingeben können, der nicht in der Liste enthalten ist.
    -   Eine bearbeitbare Dropdownliste ist eine Kombination aus einer Dropdownliste und einem bearbeitbaren Textfeld.
    -   Ein bearbeitbares Listenfeld ist eine Kombination aus einem Standardlistenfeld und einem bearbeitbaren Textfeld.

> [!Note]  
> Richtlinien zum [Layout](vis-layout.md) werden in einem separaten Artikel vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Wird das Steuerelement verwendet, um eine Option aus einer Liste von sich gegenseitig ausschließenden Werten auszuwählen?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Um mehrere Optionen auszuwählen, verwenden Sie stattdessen eine [Standard-Mehrfachauswahlliste,](ctrl-list-boxes.md)eine Kontrollkästchenliste, einen Listen-Generator oder eine Liste hinzufügen/entfernen.
-   **Sind die Optionsbefehle?** Wenn ja, verwenden Sie stattdessen eine [Menüschaltfläche](ctrl-command-buttons.md) oder eine unterteilte Schaltfläche. Verwenden Sie Dropdownlisten und Kombinationsfelder für Objekte (Nomen) oder Attribute (Adjektive), aber nicht für Befehle (Verben).
-   **Enthält die Liste Daten anstelle von Programmoptionen?** In beiden Fällen ist eine Dropdownliste oder ein Kombinationsfeld eine geeignete Wahl. Im Gegensatz dazu sind [Optionsfelder](ctrl-radio-buttons.md) nur für eine kleine Anzahl von Programmoptionen geeignet.

**Dropdownlisten**

-   **Gibt es eine Standardoption, die für die meisten Benutzer in den meisten Situationen empfohlen wird?** Ist es viel wichtiger, die ausgewählte Option zu sehen, als die Alternativen zu sehen? Erwägen Sie die Verwendung einer Dropdownliste, wenn Sie Benutzer nicht dazu ermutigen möchten, Änderungen vorzunehmen, indem Sie die Alternativen ausblenden. Andernfalls sollten Sie Optionsfelder, eine Einzelauswahlliste oder ein bearbeitbares Listenfeld in Betracht ziehen, die den alternativen Optionen mehr Aufmerksamkeit verleihen.

    ![Screenshot der höchsten Qualität als Standardschaltfläche ](images/ctrl-drop-image2.png)

    In diesem Beispiel ist die höchste Farbqualität für die meisten Benutzer die beste Wahl, sodass eine Dropdownliste eine gute Wahl ist, um die Alternativen herunterzuspielen.

-   **Möchten Sie die Aufmerksamkeit auf die Option lenken?** In diesem Falle sollten Sie Optionsfelder, eine Liste mit nur einer Auswahl oder ein bearbeitbares Listenfeld in Betracht ziehen, die in der Regel mehr Aufmerksamkeit auf sich ziehen, indem Sie mehr Bildschirmfläche nutzen. Da Dropdownlisten kompakt sind, sind sie eine gute Wahl für Optionen, die Sie unterdimensionieren möchten.
-   **Ist der Bildschirmspeicherplatz premium?** Wenn dies der Fall ist, verwenden Sie eine Dropdownliste, da der verwendete Bildschirmbereich festgelegt ist und unabhängig von der Anzahl der Auswahlmöglichkeiten ist.
-   **Gibt es weitere Dropdownlisten im Fenster?** Wenn dies der Fall ist, sollten Sie eine Dropdownliste für Konsistenz verwenden.

**Bearbeitbare Dropdownlisten**

Zusätzlich zu den Prinzipien, die soeben für Dropdownlisten bereitgestellt wurden, gelten auch Folgendes:

-   **Sind die möglichen Optionen eingeschränkt?** Wenn dies der Fall ist, verwenden Sie stattdessen eine normale Dropdownliste. Kombinationsfelder dienen zur uneingeschränkten Eingabe, bei der Benutzer möglicherweise einen Wert eingeben müssen, der derzeit nicht in der Liste enthalten ist. Da die Eingabe uneingeschränkt ist, müssen Sie den Fehler mit einer Fehlermeldung behandeln, wenn Benutzer Text eingeben, der nicht gültig ist.
-   **Können Sie die wahrscheinlichsten Optionen im Voraus aufzählen?** Falls nicht, verwenden Sie stattdessen ein Textfeld.
-   **Wird die Dropdownliste verwendet, um vorherige Benutzereingaben aufzulisten?** Wenn Benutzer nicht die vollständige Liste der vorherigen Eingaben überprüfen müssen, verwenden Sie stattdessen ein Textfeld mit der Option für die automatische Vervollständigung.

    ![Screenshot des Dialogfelds "Ausführen" mit Dropdownliste ](images/ctrl-drop-image3.png)

    In diesem Beispiel müssen Benutzer möglicherweise ihre vorherigen Eingaben überprüfen, sodass eine bearbeitbare Dropdownliste eine gute Wahl ist.

    ![Screenshot von Outlook in Zeile und automatischer Vervollständigung ](images/ctrl-drop-image4.png)

    In diesem Beispiel ist ein Textfeld mit automatischer Vervollständigung eine gute Wahl.

-   **Benötigen Benutzer Unterstützung bei der Auswahl gültiger Werte?** Verwenden Sie in diesem Falle stattdessen ein Textfeld mit der [Schaltfläche Durchsuchen.](ctrl-command-buttons.md)

    ![Screenshot der Schaltfläche "Outlook to Line" und "Durchsuchen" ](images/ctrl-drop-image5.png)

    In diesem Beispiel können Benutzer auf "An" klicken, um gültige Werte auszuwählen.

-   **Ist es wichtig, Benutzer dazu zu ermutigen, die alternativen Optionen zu überprüfen oder Änderungen einzuladen?** Falls ja, sollten Sie stattdessen ein bearbeitbares Listenfeld verwenden. Mit einer bearbeitbaren Dropdownliste werden Benutzer die Alternativen erst kennen, wenn die Liste gelöscht wird.
-   **Müssen Benutzer schnell nach einem Element in einer großen Liste suchen?** (nur Win32) Verwenden Sie in diesem Falle ein Kombinationsfeld, da Benutzer ein Element auswählen können, indem sie seinen vollständigen Namen eingeben. Im Gegensatz dazu wählt die Win32-Dropdownliste Elemente aus, die nur auf dem letzten eingegebenen Zeichen basieren (daher würde die Eingabe von "Jun" in eine Liste von Monaten mit November und nicht mit Juni übereinstimmen). Verwenden Sie in diesem Fall auch dann ein Kombinationsfeld, wenn die möglichen Optionen eingeschränkt sind.

**Bearbeitbare Listenfelder**

-   **Sind die möglichen Optionen eingeschränkt?** Wenn dies der Fall ist, verwenden Sie stattdessen eine Einzelauswahlliste oder eine normale Dropdownliste. Kombinationsfelder sind für uneingeschränkte Eingaben vorgesehen, bei denen Benutzer möglicherweise einen Wert eingeben müssen, der derzeit nicht in der Liste enthalten ist. Da die Eingabe uneingeschränkt ist, müssen Sie den Fehler mit einer Fehlermeldung behandeln, wenn Benutzer ungültigen Text eingeben.
-   **Können Sie die wahrscheinlichsten Optionen im Voraus aufzählen?** Falls nicht, verwenden Sie stattdessen ein Textfeld.
-   **Ist es wichtig, Benutzer dazu zu ermutigen, die alternativen Optionen zu überprüfen oder Änderungen einzuladen?** Wenn dies nicht der Fall ist, ziehen Sie stattdessen eine bearbeitbare Dropdownliste in Betracht.
-   **Möchten Sie die Aufmerksamkeit auf die Option lenken?** Wenn dies nicht der Fall ist, ziehen Sie stattdessen eine bearbeitbare Dropdownliste in Betracht. Da Dropdownlisten kompakt sind, sind sie eine gute Wahl für Optionen, die Sie unterdimensionieren möchten.
-   **Ist der Bildschirmspeicherplatz premium?** Wenn dies der Fall ist, verwenden Sie eine bearbeitbare Dropdownliste, da der verwendete Bildschirmspeicherplatz unabhängig von der Anzahl der Auswahlmöglichkeiten festgelegt ist.

Bei Dropdownlisten **ist die Anzahl der Elemente in der Liste kein Faktor bei der Auswahl des Steuerelements,** da sie von Tausenden von Elementen bis hin zu eins skaliert werden. Bearbeitbare Dropdownlisten werden von Tausenden von Elementen auf keines herunterskaliert, da Benutzer einen Wert eingeben können, der nicht in der Liste enthalten ist. Da Dropdownlisten für Daten verwendet werden können, ist die Anzahl der Elemente möglicherweise nicht im Voraus bekannt und kann möglicherweise nicht garantiert werden. **Fügen Sie immer mindestens drei Elemente in bearbeitbare Listenfelder ein, um den zusätzlichen Bildschirmbereich zu rechtfertigen.**

## <a name="usage-patterns"></a>Verwendungsmuster

Dropdownlisten und Kombinationsfelder weisen mehrere Verwendungsmuster auf:



|   Verwendung     |    Beispiel   |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Dropdownliste** eine Standard-Dropdownliste mit einem festen Satz vordefinierter Werte. <br/>                                 | wenn es geschlossen ist, ist nur das ausgewählte Element sichtbar. Wenn Benutzer auf die Dropdownschaltfläche klicken, werden alle Optionen angezeigt. Um den Wert zu ändern, öffnen Benutzer die Liste und klicken auf einen anderen Wert.<br/> ![Screenshot der Dropdownliste, ausgeblendete Optionen ](images/ctrl-drop-image6.png)<br/> In diesem Beispiel befindet sich die Liste im normalen Zustand.<br/> ![Screenshot der Dropdownliste, angezeigte Optionen ](images/ctrl-drop-image7.png)<br/> In diesem Beispiel wurde die Liste gelöscht.<br/> |
| **Dropdownliste "Vorschau"** eine Dropdownliste, in der die Ergebnisse der Auswahl als Vorschau angezeigt werden, damit Benutzer diese auswählen können.<br/>             | ![Screenshot der Farb- und Textoptionen ](images/ctrl-drop-image8.png)<br/> In diesen Beispielen zeigen die Dropdownlisten eine Vorschau der Ergebnisse der Auswahl an.<br/>                                                                                                                                                                                                                                                                                                                                           |
| **Bearbeitbare Dropdownliste:** Ein Dropdown-Kombinationsfeld, mit dem Benutzer einen Wert eingeben können, der nicht in der Dropdownliste enthalten ist.<br/> | ![aa511458.dropdownlists27(en-us,msdn.10).png](images/ctrl-drop-image9.png)![Screenshot des bearbeitbaren Kombinationsfelds für den Schriftgrad ](images/ctrl-drop-image10.png)<br/> Beispiele für eine bearbeitbare Dropdownliste im Bearbeitungs- und Dropdownmodus.<br/> Verwenden Sie dieses Steuerelement, wenn Sie die Flexibilität eines Textfelds bereitstellen möchten, aber Benutzer unterstützen möchten, indem Sie eine praktische Liste der wahrscheinlichen Optionen bereitstellen.<br/>                                                                                                   |
| **Bearbeitbare Listenfelder** sind ein reguläres Kombinationsfeld, mit dem Benutzer einen Wert eingeben können, der nicht in der immer sichtbaren Liste enthalten ist. <br/> | ![Screenshot der Dropdownliste der Schriftartoptionen ](images/ctrl-drop-image11.png)<br/> In diesen Beispielen werden die bearbeitbaren Listenfelder immer angezeigt.<br/> Dieses Steuerelement ist eine bessere Wahl als die bearbeitbare Dropdownliste, wenn es wichtig ist, Benutzer dazu zu ermutigen, die alternativen Optionen zu überprüfen oder Änderungen einzuladen.<br/>                                                                                                                                                                      |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie nicht die Änderung einer Dropdownliste oder eines Kombinationsfelds in**:
    -   Führen Sie Befehle aus.
    -   Zeigen Sie andere Fenster an, z. B. ein Dialogfeld, um weitere Eingaben zu erfassen.
    -   Dynamische Anzeige anderer Steuerelemente im Zusammenhang mit dem ausgewählten Steuerelement ([Sprachausgaben](inter-accessibility.md) können solche Ereignisse nicht erkennen).

### <a name="presentation"></a>Präsentation

-   **Sortieren Sie Listenelemente in einer logischen Reihenfolge,** z. B. gruppieren Sie stark verwandte Optionen, platzieren Sie die häufigsten Optionen an erster Stelle, oder verwenden Sie die alphabetische Reihenfolge. Sortieren Sie Namen in alphabetischer Reihenfolge, Zahlen in numerischer Reihenfolge und Datumsangaben in chronologischer Reihenfolge. Listen mit 12 oder mehr Elementen sollten alphabetisch sortiert werden, um die Suche nach Elementen zu vereinfachen.

    **Richtig:** ![ Screenshot der logischen Dropdownliste ](images/ctrl-drop-image12.png)

    In diesem Beispiel werden die Listenelemente nach ihrer räumlichen Beziehung sortiert.

    **Falsch:** ![ Screenshot der nicht organisierten Dropdownliste ](images/ctrl-drop-image13.png)

    In diesem Beispiel gibt es so viele Listenelemente, dass sie in alphabetischer Reihenfolge sortiert werden müssen.

    **Richtig:** ![ Screenshot der alphabetischen Dropdownliste ](images/ctrl-drop-image14.png)

    In diesem Beispiel werden die Listenelemente in alphabetischer Reihenfolge sortiert, mit Ausnahme der Option, die alle Elemente darstellt.

-   **Platzieren Sie Optionen, die Alle oder Keine am Anfang der Liste darstellen, unabhängig von der Sortierreihenfolge der verbleibenden Elemente.**
-   **Schließen Sie Metaoptionen in Klammern ein.**

    ![Screenshot: Dropdownliste mit ausgewählter Option "(None)"](images/ctrl-drop-image15.png)

    In diesem Beispiel ist "(None)" eine Metaoption, da sie kein gültiger Wert für die Auswahl ist, sondern beschreibt, dass die Option selbst nicht verwendet wird.

-   **Wenn Sie eine Dropdownliste oder ein Kombinationsfeld deaktivieren, deaktivieren Sie auch alle zugeordneten Bezeichnungen und Befehlsschaltflächen.**

### <a name="drop-down-lists"></a>Dropdownlisten

-   Wenn eine einzelne Dropdownliste verwendet wird, um die Ansicht eines zugeordneten Steuerelements zu ändern, **ändern Sie die Ansicht sofort bei der Auswahl, anstatt eine separate Befehlsschaltfläche zu erfordern.** Verwenden Sie nur dann eine separate Befehlsschaltfläche, wenn das Rendern der Liste viel Zeit in Anspruch nimmt. Listenheader und [Menüschaltflächen](ctrl-command-buttons.md) sind jedoch die bevorzugten Steuerelemente für diesen Zweck.
-   **Verwenden Sie keine leeren Listenelemente,** **sondern Metaoptionen.** Benutzer wissen nicht, wie leere Elemente interpretiert werden, während die Bedeutung von Metaoptionen explizit ist.

    **Richtig:** ![ Screenshot der Dropdownliste ohne Auswahl ](images/ctrl-drop-image16.png)

    **Falsch:** ![ Screenshot der Dropdownliste mit ausgewählter Option "Leer" ](images/ctrl-drop-image17.png)

    Im falschen Beispiel ist die Bedeutung der leeren Option unklar.

### <a name="preview-drop-down-lists"></a>Dropdownlisten für die Vorschau

-   **Verwenden Sie Vorschauen in den Listenelementen, wenn es besser ist, mit Bildern anzuzeigen, als mithilfe von Text allein zu beschreiben.**

    ![Screenshot der Dropdownliste der Schriftarten in der Vorschau ](images/ctrl-drop-image18.png)

    In diesem Beispiel werden die Optionen in der Vorschau deutlich besser erläutert als text allein.

-   **Verwenden Sie keine unnötigen, nicht hilfreichen Symbole in Vorschauversionen.**

    **Falsch:** ![ Screenshot der Dropdownliste mit Bezeichnungen mit Symbolen ](images/ctrl-drop-image19.png)

    In diesem Beispiel sind die Vorschausymbole unnötig, da sie keine Informationen kommunizieren.

### <a name="combo-boxes"></a>Kombinationsfelder

-   **Begrenzen Sie die Länge des Eingabetexts nach Möglichkeit.** Wenn die gültige Eingabe beispielsweise eine Zahl zwischen 0 und 999 ist, verwenden Sie ein Kombinationsfeld, das auf drei Zeichen beschränkt ist.
-   **Wenn es viele mögliche Optionen gibt, konzentrieren Sie den Listeninhalt auf die wahrscheinlichsten Optionen.** Da Benutzer Werte eingeben können, die nicht in der Liste enthalten sind, müssen Kombinationsfelder nicht alle Auswahlmöglichkeiten auflisten, nur die wahrscheinlichen Auswahlmöglichkeiten oder ein repräsentatives Beispiel.

    ![Screenshot der Dropdownliste der Schriftgrade ](images/ctrl-drop-image10.png)

    In diesem Beispiel sind viele gültige Optionen nicht aufgeführt, z. B. 15 oder Schriftarten mit halber Größe wie 9,5.

### <a name="default-values"></a>Standardwerte

-   **Wählen Sie standardmäßig die sicherste Option (um daten- oder systemzugriffsverlust zu verhindern) und die sicherste Option aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequemste Option aus.
    -   **Ausnahme:** Zeigt einen leeren Standardwert an, wenn das Steuerelement eine Eigenschaft in einem [gemischten Zustand](glossary.md)darstellt. Dies geschieht, wenn eine Eigenschaft für mehrere Objekte angezeigt wird, die nicht die gleiche Einstellung aufweisen.

## <a name="prompts"></a>Eingabeaufforderungen

Eine Eingabeaufforderung ist eine Bezeichnung oder kurze Anweisung, die als Standardwert in einer bearbeitbaren Dropdownliste platziert wird. Im Gegensatz zu statischem Text werden Eingabeaufforderungen vom Bildschirm ausgeblendet, sobald Benutzer etwas in das Kombinationsfeld eingeben oder den Eingabefokus erhalten.

![Screenshot eines Suchfelds ](images/ctrl-drop-image20.png)

Eine typische Eingabeaufforderung.

Verwenden Sie eine Eingabeaufforderung, wenn:

-   Der Bildschirmbereich ist so premium, dass die Verwendung einer Bezeichnung oder Anweisung unerwünscht ist, z. B. auf einer Symbolleiste.
-   Die Eingabeaufforderung dient in erster Linie dazu, den Zweck der Liste auf kompakte Weise zu identifizieren. Es dürfen keine entscheidenden Informationen sein, die Benutzern bei der Verwendung des Kombinationsfelds angezeigt werden müssen.

Verwenden Sie keine Eingabeaufforderungen, um Benutzer nur anweisen, etwas aus der Liste auszuwählen oder auf Schaltflächen zu klicken. Eingabeaufforderungen wie Option auswählen oder Dateinamen eingeben und dann auf Senden sind nicht erforderlich.

Bei Verwendung von Eingabeaufforderungen:

-   Zeichnen Sie den Eingabeaufforderungstext in italischem Grau und den echten Text in normalem Schwarz. Der Eingabeaufforderungstext darf nicht mit echtem Text verwechselt werden.
-   Halten Sie den Eingabeaufforderungstext kurz. Sie können Fragmente anstelle von vollständigen Sätzen verwenden.
-   Verwenden Sie [die Groß-/Großschreibung im Satzformat.](glossary.md)
-   Verwenden Sie keine endende Interpunktion oder Auslassungszeichen.
-   Der Eingabeaufforderungstext sollte nicht bearbeitbar sein und nicht mehr angezeigt werden, sobald Benutzer in das Textfeld klicken oder die Registerkarte öffnen.
    -   **Ausnahme:** Die Eingabeaufforderung wird angezeigt, wenn das Textfeld den Standardeingabefokus besitzt und erst ausgeblendet wird, wenn der Benutzer mit der Eingabe beginnt.
-   Der Eingabeaufforderungstext wird wiederhergestellt, wenn das Textfeld noch leer ist, wenn der Eingabefokus verloren geht.

**Falsch:** ![ Screenshot von sechs bearbeitbaren Dropdownlisten](images/ctrl-drop-image21.png)

In diesem Beispiel ist der Bildschirmbereich nicht premium. Sobald eine bearbeitbare Dropdownliste ausgefüllt ist, ist es für Benutzer schwierig, sich zu merken, wofür sie sich eignet. und der Eingabeaufforderungstext kann bearbeitet und auf die gleiche Weise wie echter Text gezeichnet werden.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größen- und Abstände

![Screenshot der Dropdownliste und Spezifikationen ](images/ctrl-drop-image22.png)

Empfohlene Größen- und Abstände für Dropdownlisten und Kombinationsfelder.

-   **Wählen Sie eine Breite aus, die für die längsten gültigen Daten geeignet ist.** Dropdownlisten können nicht horizontal gescrollt werden, sodass Benutzer nur sehen können, was im Steuerelement sichtbar ist. (Beachten Sie jedoch, dass für Kombinationsfelder die AutoScroll-Funktionalität aktiviert sein kann.)
-   **Fügen Sie zusätzliche 30 Prozent** (bis zu 200 Prozent für kürzeren Text) für jeden Text (aber keine Zahlen) ein, der lokalisiert wird.
-   **Wählen Sie eine Listenlänge aus, die unnötiges vertikales Scrollen überflüssig macht.** Da Dropdownlisten bei Bedarf angezeigt werden, sollten ihre Listen bis zu 30 Elemente anzeigen. Bearbeitbare Listenfelder (die nicht über eine Dropdownschaltfläche verfügen) sollten zwischen 3 und 12 Elemente anzeigen.

## <a name="labels"></a>Bezeichnungen

**Steuerelementbezeichnungen**

-   Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, und beenden Sie sie mit einem Doppelpunkt. **Ausnahmen:**
    -   Bearbeitbare Dropdownlisten mit Eingabeaufforderungen, in denen sich der Speicherplatz im Premium-Bereich befindet.
    -   Wenn eine Dropdownliste oder ein Kombinationsfeld einem Optionsfeld oder Kontrollkästchen untergeordnet ist und durch die Bezeichnung eingeführt wird, die mit einem Doppelpunkt endet, legen Sie keine zusätzliche Bezeichnung auf dem Steuerelement ab.
-   Weisen Sie für jede Bezeichnung einen eindeutigen [Zugriffsschlüssel](glossary.md) zu. Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie [die Groß-/Großschreibung im Satzformat.](glossary.md)
-   Positionieren Sie die Bezeichnung entweder links vom Steuerelement oder oberhalb des Steuerelements, und richten Sie die Bezeichnung am linken Rand des Steuerelements aus. Wenn sich die Bezeichnung links befindet, richten Sie den Bezeichnungstext vertikal am Steuerelementtext aus.

    **Richtig:** ![ Screenshot der Ausrichtung von Dropdownlistenbezeichnungen ](images/ctrl-drop-image23.png)

    In diesem Beispiel ist die Bezeichnung ordnungsgemäß am Steuerelementtext ausgerichtet.

    **Falsch:** ![ Screenshot der falsch ausgerichteten Dropdownliste ](images/ctrl-drop-image24.png)

    In diesem Beispiel ist die Bezeichnung falsch am Steuerelementtext ausgerichtet.

-   Sie können Einheiten (Sekunden, Verbindungen und so weiter) in Klammern nach der Bezeichnung angeben.
-   Machen Sie den Inhalt der Dropdownliste oder des Kombinationsfelds (oder seiner Einheitenbezeichnung) nicht als Teil eines Satzes, da dies nicht lokalisierbar ist.

**Optionstext**

-   Weisen Sie jeder Option einen eindeutigen Namen zu.
-   Verwenden [Sie Die Groß-/Groß-/Formatvorlage,](glossary.md)es sei denn, ein Element ist ein richtiges Nomen.
-   Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, und verwenden Sie keine endende Interpunktion.
-   Verwenden Sie parallele Formulierungen, und versuchen Sie, die Länge für alle Optionen ungefähr gleich zu halten.

**Anweisungstext**

-   Wenn Sie Anweisungstext zu einer Dropdownliste oder einem Kombinationsfeld hinzufügen müssen, fügen Sie ihn über der Bezeichnung hinzu. Verwenden Sie vollständige Sätze mit endender Interpunktion.
-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)
-   Zusätzliche Informationen, die hilfreich, aber nicht erforderlich sind, sollten kurz gehalten werden. Platzieren Sie diese Informationen entweder in Klammern zwischen der Bezeichnung und dem Doppelpunkt oder ohne Klammern unterhalb des Steuerelements.

    ![Screenshot der Dropdownliste mit hinzugefügten Daten ](images/ctrl-drop-image25.png)

    Dieses Beispiel zeigt zusätzliche Informationen, die unterhalb des -Steuerelements platziert werden.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Dropdownlisten:

-   Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Groß-/Unterstriche, aber schließen Sie nicht den Unterstrich oder Doppelpunkt der Zugriffsschlüssel ein. fügen Sie entweder list oder box ein, unabhängig davon, was übersichtlicher ist.
-   Verwenden Sie für Listenoptionen den genauen Optionstext, einschließlich der Groß-/Groß-/Groß-/Unterform.
-   In der Programmierung und anderen technischen Dokumentationen finden Sie Dropdownlisten als Dropdownlisten. Verwenden Sie überall sonst entweder list oder box, unabhängig davon, was übersichtlicher ist.
-   Um die Benutzerinteraktion zu beschreiben, klicken Sie auf .
-   Formatieren Sie die Bezeichnungs- und Listenoptionen nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung und die Optionen nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Klicken Sie in **der Liste Schriftgrad** auf **Große Schriftarten.**

Beim Verweisen auf Kombinationsfelder:

-   Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Groß-/Unterstriche, aber schließen Sie den Unterstrich oder Doppelpunkt des Zugriffsschlüssels nicht ein. Fügen Sie das Wortfeld ein.
-   Verwenden Sie für Listenoptionen den genauen Optionstext, einschließlich der Groß-/Groß-/Groß-/Unterform.
-   In der Programmierung und anderen technischen Dokumentationen werden Kombinationsfelder als Kombinationsfelder bezeichnet. Verwenden Sie überall das Feld .
-   Verwenden Sie die EINGABETASTE, um die Benutzerinteraktion zu beschreiben.
-   Formatieren Sie die Bezeichnungs- und Listenoptionen nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung und die Optionen nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Geben Sie im **Feld Schriftart** die Schriftart ein, die Sie verwenden möchten.

 

