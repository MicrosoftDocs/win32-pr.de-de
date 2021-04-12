---
title: Kombinationsfelder für Dropdownlisten
description: Mit einer Dropdown Liste oder einem Kombinations Feld treffen Benutzer eine Auswahl in einer Liste von sich gegenseitig ausschließenden Werten.
ms.assetid: dbe88cf1-7946-4343-bc16-ce12be7ce205
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 646fb569cf3a7861d68d0eb885107ba12978c101
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218947"
---
# <a name="drop-down-lists--combo-boxes"></a>Dropdown Listen & Kombinations Feldern

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mit einer Dropdown Liste oder einem Kombinations Feld treffen Benutzer eine Auswahl in einer Liste von sich gegenseitig ausschließenden Werten. Benutzer können nur eine Option auswählen. Mit einer Standard-Dropdown Liste können Benutzer auf Auswahlmöglichkeiten in der Liste beschränken, aber mit einem Kombinations Feld können Sie eine Auswahl eingeben, die nicht in der Liste enthalten ist.

![Screenshot der Erinnerungszeit (Kombinations Feld) ](images/ctrl-drop-image1.png)

Ein typisches Kombinations Feld.

Die folgenden Begriffe sind wichtig zu verstehen, wenn Sie diesen Artikel lesen:

-   Ein Standard Listenfeld ist ein Feld, das eine Liste mehrerer Elemente enthält, bei der mehrere Elemente sichtbar sind.
-   Eine Dropdown Liste ist eine Liste, in der das ausgewählte Element immer sichtbar ist, und die anderen sind bei Bedarf sichtbar, indem Sie auf eine Dropdown-Schaltfläche klicken.
-   Ein Kombinations Feld ist eine Kombination aus einem Standard Listenfeld oder einer Dropdown Liste und einem bearbeitbaren [Textfeld](ctrl-text-boxes.md). Dadurch können Benutzer einen Wert eingeben, der nicht in der Liste enthalten ist.
    -   Eine bearbeitbare Dropdown Liste ist eine Kombination aus einer Dropdown Liste und einem bearbeitbaren Textfeld.
    -   Ein bearbeitbares Listenfeld ist eine Kombination aus einem Standard Listenfeld und einem bearbeitbaren Textfeld.

> [!Note]  
> Richtlinien für das [Layout](vis-layout.md) werden in einem separaten Artikel dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Wird das Steuerelement verwendet, um eine Option aus einer Liste von sich gegenseitig ausschließenden Werten auszuwählen?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Wenn Sie mehrere Optionen auswählen möchten, verwenden Sie stattdessen eine [standardmäßige Mehrfachauswahl Liste](ctrl-list-boxes.md), eine Kontrollkästchen Liste, einen Listen-Generator oder eine Liste zum hinzufügen/entfernen.
-   **Gibt es die Options Befehle?** Wenn dies der Fall ist, verwenden Sie stattdessen eine [Menü Schaltfläche](ctrl-command-buttons.md) oder eine Schaltfläche Verwenden Sie Dropdown Listen und Kombinations Felder für Objekte (Nomen) oder Attribute (Adjektive), aber keine Befehle (Verben).
-   **Stellt die Liste Daten anstelle der Programmoptionen dar?** In jedem Fall ist eine Dropdown Liste oder ein Kombinations Feld eine geeignete Wahl. Im Gegensatz dazu [sind Options](ctrl-radio-buttons.md) Felder nur für eine kleine Anzahl von Programmoptionen geeignet.

**Dropdownlisten**

-   **Gibt es eine Standardoption, die für die meisten Benutzer in den meisten Situationen empfohlen wird?** Sehen Sie, dass die ausgewählte Option weitaus wichtiger ist, als die Alternativen zu sehen? Verwenden Sie ggf. eine Dropdown Liste, wenn Sie nicht möchten, dass Benutzer Änderungen vornehmen, indem Sie die alternativen ausblenden. Wenn dies nicht der Grund ist, sollten Sie Options Felder, eine Auswahlliste oder ein bearbeitbares Listenfeld in Erwägung nehmen, die die Alternativen Optionen genauer machen.

    ![Screenshot der höchsten Qualität als Standard Schaltfläche ](images/ctrl-drop-image2.png)

    In diesem Beispiel ist die höchste Farbqualität die beste Wahl für die meisten Benutzer, sodass eine Dropdown Liste eine gute Wahl ist, um die alternativen herunter zugeben.

-   **Möchten Sie auf die Option aufmerksam machen?** Wenn dies der Fall ist, sollten Sie Options Felder, eine Auswahlliste oder ein bearbeitbares Listenfeld in Erwägung ziehen, die in der Regel mehr Aufmerksamkeit gewinnen, indem Sie mehr Bildschirmfläche einnehmen. Da Dropdown Listen kompakt sind, eignen Sie sich gut für Optionen, die Sie unterstreichen möchten.
-   **Ist der Bildschirmbereich bei einem Premium-Tarif?** Wenn dies der Fall ist, verwenden Sie eine Dropdown Liste, da der verwendete Bildschirmbereich fest und unabhängig von der Anzahl der Optionen ist.
-   **Gibt es andere Dropdown Listen im Fenster?** Wenn dies der Fall ist, sollten Sie in Erwägung ziehen, eine Dropdown Liste zu verwenden.

**Bearbeitbare Dropdown Listen**

Zusätzlich zu den Prinzipien, die nur für Dropdown Listen bereitgestellt werden, gilt Folgendes:

-   **Sind die möglichen Auswahlmöglichkeiten eingeschränkt?** Wenn dies der Fall ist, verwenden Sie stattdessen eine normale Dropdown Liste. Kombinations Felder sind für eine nicht eingeschränkte Eingabe, bei der Benutzer möglicherweise einen Wert eingeben müssen, der sich derzeit nicht in der Liste befinden. Da die Eingabe nicht eingeschränkt ist, müssen Sie den Fehler mit einer Fehlermeldung behandeln, wenn Benutzer Text eingeben, der nicht gültig ist.
-   **Können Sie die wahrscheinlichsten Auswahlmöglichkeiten im Voraus** auflisten? Wenn dies nicht der Wert ist, verwenden Sie stattdessen ein Textfeld.
-   **Wird die Dropdown Liste zum Auflisten vorheriger Benutzereingaben verwendet?** Wenn die Benutzer die vollständige Liste vorheriger Eingaben nicht überprüfen müssen, verwenden Sie stattdessen ein Textfeld mit der automatischen Vervollständigung-Option.

    ![Screenshot des Dialog Felds "ausführen" mit der Dropdown Liste ](images/ctrl-drop-image3.png)

    In diesem Beispiel müssen Benutzer möglicherweise Ihre vorherige Eingabe überprüfen, sodass eine bearbeitbare Dropdown Liste eine gute Wahl ist.

    ![Screenshot von Outlook zu Zeile und automatischer Vervollständigung ](images/ctrl-drop-image4.png)

    In diesem Beispiel ist ein Textfeld mit automatischer Vervollständigung eine gute Wahl.

-   **Benötigen Benutzer Unterstützung bei der Auswahl gültiger Werte?** Wenn dies der Fall ist, verwenden Sie stattdessen ein Textfeld mit der [Schaltfläche Durchsuchen](ctrl-command-buttons.md) .

    ![Screenshot der Schaltfläche "Zeilen-und Durchsuchen" in Outlook ](images/ctrl-drop-image5.png)

    In diesem Beispiel können Benutzer auf "to" klicken, um Ihnen bei der Auswahl gültiger Werte zu helfen.

-   **Ist es wichtig, den Benutzern zu empfehlen, die Alternativen Optionen zu überprüfen oder Änderungen einzuladen?** Wenn dies der Fall ist, sollten Sie stattdessen ein bearbeitbares Listenfeld verwenden. Wenn Benutzer eine bearbeitbare Dropdown Liste haben, werden Sie die alternativen erst beachten, wenn die Liste gelöscht wird.
-   **Müssen Benutzer schnell ein Element in einer großen Liste finden?** (Nur Win32) Wenn dies der Fall ist, verwenden Sie ein Kombinations Feld, da Benutzer ein Element auswählen können, indem Sie den vollständigen Namen eingeben. Im Gegensatz dazu wählt die Win32-Dropdown Liste nur Elemente aus, die nur durch das letzte typisierte Zeichen eingegeben werden. (die Eingabe von "Jun" in eine Liste von Monaten würde also November und nicht Juni entsprechen). Verwenden Sie in diesem Fall ein Kombinations Feld, auch wenn die möglichen Optionen eingeschränkt sind.

**Bearbeitbare Listenfelder**

-   **Sind die möglichen Auswahlmöglichkeiten eingeschränkt?** Wenn dies der Fall ist, verwenden Sie stattdessen eine einfache Auswahlliste oder eine normale Dropdown Liste. Kombinations Felder sind für eine nicht eingeschränkte Eingabe, bei der Benutzer möglicherweise einen Wert eingeben müssen, der sich derzeit nicht in der Liste befinden. Da die Eingabe nicht eingeschränkt ist, müssen Sie den Fehler mit einer Fehlermeldung behandeln, wenn Benutzer Text eingeben, der nicht gültig ist.
-   **Können Sie die wahrscheinlichsten Auswahlmöglichkeiten im Voraus auflisten?** Wenn dies nicht der Wert ist, verwenden Sie stattdessen ein Textfeld.
-   **Ist es wichtig, den Benutzern zu empfehlen, die Alternativen Optionen zu überprüfen oder Änderungen einzuladen?** Wenn dies nicht der Fall ist, sollten Sie stattdessen eine bearbeitbare Dropdown Liste verwenden.
-   **Möchten Sie auf die Option aufmerksam machen?** Wenn dies nicht der Fall ist, sollten Sie stattdessen eine bearbeitbare Dropdown Liste verwenden. Da Dropdown Listen kompakt sind, eignen Sie sich gut für Optionen, die Sie unterstreichen möchten.
-   **Ist der Bildschirmbereich bei einem Premium-Tarif?** Wenn dies der Fall ist, verwenden Sie eine bearbeitbare Dropdown Liste, da der verwendete Bildschirmbereich fest und unabhängig von der Anzahl der Optionen ist.

Für Dropdown Listen ist **die Anzahl der Elemente in der Liste kein Faktor bei der Auswahl des Steuer** Elements, da Sie von Tausenden von Elementen bis zu einer Skala skaliert werden. Bearbeitbare Dropdown Listen können von Tausenden von Elementen auf keine skaliert werden, da Benutzer einen Wert eingeben können, der nicht in der Liste enthalten ist. Da Dropdown Listen für Daten verwendet werden können, ist die Anzahl der Elemente möglicherweise nicht im Voraus bekannt und kann möglicherweise nicht garantiert werden. **Fügen Sie immer mindestens drei Elemente in bearbeitbare Listenfelder ein, um den zusätzlichen Bildschirmbereich zu rechtfertigen.**

## <a name="usage-patterns"></a>Verwendungsmuster

Dropdown Listen und Kombinations Felder weisen mehrere Verwendungs Muster auf:



|                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Dropdown Liste** eine Standard-Dropdown Liste mit einem festgelegten Satz von vordefinierten Werten. <br/>                                 | beim Schließen ist nur das ausgewählte Element sichtbar. Wenn Benutzer auf die Dropdown Schaltfläche klicken, werden alle Optionen sichtbar. um den Wert zu ändern, öffnen die Benutzer die Liste, und klicken Sie auf einen anderen Wert.<br/> ![Screenshot der Dropdown Liste, ausgeblendete Optionen ](images/ctrl-drop-image6.png)<br/> in diesem Beispiel befindet sich die Liste in Ihrem normalen Zustand.<br/> ![Screenshot der Dropdown Liste, angezeigte Optionen ](images/ctrl-drop-image7.png)<br/> In diesem Beispiel wurde die Liste gelöscht.<br/> |
| **Vorschau-Dropdown Liste** eine Dropdown Liste, in der die Ergebnisse der Auswahl in der Vorschau angezeigt werden, um Benutzern die Auswahl zu erleichtern.<br/>             | ![Screenshot der Farb-und Textoptionen ](images/ctrl-drop-image8.png)<br/> In diesen Beispielen wird in der Dropdown Liste eine Vorschau der Ergebnisse der Auswahl angezeigt.<br/>                                                                                                                                                                                                                                                                                                                                           |
| **Bearbeitbare Dropdown Liste** ein Dropdown-Kombinations Feld, das es Benutzern ermöglicht, einen Wert einzugeben, der nicht in der Dropdown Liste enthalten ist.<br/> | ![aa511458. dropdownlists27 (en-US, MSDN. 10). png](images/ctrl-drop-image9.png)![Screenshot des bearbeitbaren Kombinations Felds "Schriftart Größe" ](images/ctrl-drop-image10.png)<br/> Beispiele für eine bearbeitbare Dropdown Liste in den Modi "Bearbeiten" und "Dropdown".<br/> Verwenden Sie dieses Steuerelement, wenn Sie die Flexibilität eines Textfelds gewährleisten möchten, aber die Benutzer unterstützen möchten, indem Sie eine bequeme Liste der wahrscheinlichsten Optionen bereitstellen.<br/>                                                                                                   |
| **Bearbeitbare Listenfelder** ein reguläres Kombinations Feld, das es Benutzern ermöglicht, einen Wert einzugeben, der nicht in der Liste immer sichtbar ist. <br/> | ![Screenshot der Dropdown Liste mit Schriftart Optionen ](images/ctrl-drop-image11.png)<br/> In diesen Beispielen werden immer die bearbeitbaren Listenfelder angezeigt.<br/> Dieses Steuerelement ist besser geeignet als die bearbeitbare Dropdown Liste, wenn es wichtig ist, die Benutzer dazu aufzufordern, die Alternativen Optionen zu überprüfen oder Änderungen einzuladen.<br/>                                                                                                                                                                      |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie die Änderung einer Dropdown Liste oder eines Kombinations Felds nicht für** Folgendes:
    -   Ausführen von Befehlen.
    -   Zeigen Sie andere Fenster an, z. b. ein Dialogfeld, um weitere Eingaben zu erfassen.
    -   Dynamische Anzeige anderer Steuerelemente, die mit dem ausgewählten Steuerelement verknüpft[sind (sprach](inter-accessibility.md) Ausgabe können solche Ereignisse nicht erkennen).

### <a name="presentation"></a>Präsentation

-   **Sortieren Sie Listenelemente in einer logischen Reihenfolge**, z. b. das Gruppieren von stark verknüpften Optionen, das Platzieren der gängigsten Optionen zuerst oder das Verwenden von alphabetischer Reihen Sortieren von Namen in alphabetischer Reihenfolge, Zahlen in numerischer Reihenfolge und Datumsangaben in chronologischer Reihenfolge. Listen mit 12 oder mehr Elementen sollten alphabetisch sortiert werden, damit Elemente leichter zu finden sind.

    **Richtig:** ![ Screenshot der logischen Dropdown Liste ](images/ctrl-drop-image12.png)

    In diesem Beispiel werden die Listenelemente nach ihrer räumlichen Beziehung sortiert.

    **Falsch:** ![ Screenshot der nicht-Dropdown Liste ](images/ctrl-drop-image13.png)

    In diesem Beispiel gibt es so viele Listenelemente, dass Sie in alphabetischer Reihenfolge sortiert werden müssen.

    **Richtig:** ![ Screenshot der Dropdown Liste "alphabetisch" ](images/ctrl-drop-image14.png)

    In diesem Beispiel werden die Listenelemente in alphabetischer Reihenfolge sortiert, mit Ausnahme der Option, die alle Elemente darstellt.

-   **Platzieren Sie Optionen, die "All" oder "None" am Anfang der Liste darstellen, unabhängig von der Sortierreihenfolge der restlichen Elemente.**
-   **Umschließen von metaoptionen in Klammern.**

    ![Screenshot, der eine Dropdown Liste mit ausgewähltem "(None)" anzeigt.](images/ctrl-drop-image15.png)

    In diesem Beispiel ist "(None)" eine Meta-Option, da es sich nicht um einen gültigen Wert für die Auswahl handelt, sondern beschreibt, dass die Option selbst nicht verwendet wird.

-   **Deaktivieren Sie bei der Deaktivierung einer Dropdown Liste oder eines Kombinations Felds auch alle zugeordneten Bezeichnungen und Befehls Schaltflächen.**

### <a name="drop-down-lists"></a>Dropdownlisten

-   Wenn eine Dropdown Liste verwendet wird, um die Ansicht eines zugeordneten Steuer Elements zu ändern, **Ändern Sie die Ansicht sofort bei der Auswahl, anstatt eine separate Befehls Schaltfläche zu benötigen.** Verwenden Sie eine separate Befehls Schaltfläche nur dann, wenn die Liste sehr viel Zeit zum Rendering benötigt. Listen Header und [Menü](ctrl-command-buttons.md) Schaltflächen sind zu diesem Zweck jedoch die bevorzugten Steuerelemente.
-   **Verwenden Sie stattdessen Meta-Options**, wenn **keine leeren Listenelemente vorhanden sind** . Benutzer wissen nicht, wie leere Elemente interpretiert werden, wohingegen die Bedeutung von metaoptionen explizit ist.

    **Richtig:** ![ Screenshot der Dropdown Liste ohne Auswahl ](images/ctrl-drop-image16.png)

    **Falsch:** ![ Screenshot der Dropdown Liste mit leerer Auswahl ](images/ctrl-drop-image17.png)

    Im falschen Beispiel ist die Bedeutung der leeren Option unklar.

### <a name="preview-drop-down-lists"></a>Vorschau-Dropdown Listen

-   **Verwenden Sie Vorschauen in den Listenelementen, wenn es besser ist, mit Bildern zu zeigen, als die Verwendung von Text allein zu beschreiben.**

    ![Screenshot der Dropdown Liste der in der Vorschau angezeigten Schriftarten ](images/ctrl-drop-image18.png)

    In diesem Beispiel werden die Optionen in der Vorschau wesentlich besser als nur Text erläutert.

-   **Verwenden Sie in der Vorschau nicht unnötige, nicht hilfreiche Symbole**.

    **Falsch:** ![ Screenshot der Dropdown Liste mit den Bezeichnungen mit Symbolen ](images/ctrl-drop-image19.png)

    In diesem Beispiel sind die Vorschau Symbole unnötig, da Sie keine Informationen miteinander kommunizieren.

### <a name="combo-boxes"></a>Kombinations Felder

-   **Beschränken Sie die Länge des Eingabe Texts, wenn dies möglich ist.** Wenn die gültige Eingabe z. b. eine Zahl zwischen 0 und 999 ist, verwenden Sie ein Kombinations Feld, das auf drei Zeichen begrenzt ist.
-   **Wenn viele mögliche Optionen vorhanden sind, konzentrieren Sie sich auf den Listen Inhalt auf die wahrscheinlichste Option**. Da Benutzer Werte eingeben können, die nicht in der Liste enthalten sind, müssen Kombinations Felder nicht alle Optionen auflisten, sondern nur die wahrscheinliche Auswahl oder eine repräsentative Stichprobe.

    ![Screenshot der Dropdown Liste mit Schriftart Größen ](images/ctrl-drop-image10.png)

    In diesem Beispiel sind viele gültige Optionen nicht aufgeführt, z. b. 15 oder Schriftarten der Hälfte (z. b. 9,5).

### <a name="default-values"></a>Standardwerte

-   **Wählen Sie das sicherste (um Datenverlust oder System Zugriff zu vermeiden) und die sicherste Option standardmäßig aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequeme Option aus.
    -   **Ausnahme:** Zeigt einen leeren Standardwert an, wenn das Steuerelement eine Eigenschaft in einem [gemischten Zustand](glossary.md)darstellt. Dies ist der Fall, wenn eine Eigenschaft für mehrere Objekte angezeigt wird, die nicht die gleiche Einstellung aufweisen.

## <a name="prompts"></a>Eingabeaufforderungen

Eine Eingabeaufforderung ist eine Bezeichnung oder eine kurze Anweisung in einer bearbeitbaren Dropdown Liste als Standardwert. Im Gegensatz zu statischem Text werden Aufforderungen auf dem Bildschirm ausgeblendet, sobald Benutzer etwas in das Kombinations Feld eingeben oder den Eingabefokus erhalten.

![Screenshot eines Suchfeld ](images/ctrl-drop-image20.png)

Eine typische Eingabeaufforderung.

Verwenden Sie eine Eingabeaufforderung, wenn:

-   Der Bildschirmbereich ist so hoch, dass die Verwendung einer Bezeichnung oder Anweisung nicht erwünscht ist, z. b. auf einer Symbolleiste.
-   Bei der Eingabeaufforderung wird in erster Linie der Zweck der Liste auf kompakte Weise identifiziert. Es darf keine wichtigen Informationen sein, die Benutzer bei der Verwendung des Kombinations Felds anzeigen müssen.

Verwenden Sie keine Aufforderungen, um Benutzer anzuweisen, etwas aus der Liste auszuwählen oder auf Schaltflächen zu klicken. Beispielsweise sind Eingabe Aufforderungen wie SELECT an eine Option, oder geben Sie einen Dateinamen ein, und klicken Sie dann auf senden.

Bei Verwendung von Eingabe Aufforderungen:

-   Zeichnen Sie den Aufforderungs Text in kursiv grau und in normalem Text in normalem schwarz. Der Eingabe Aufforderungs Text darf nicht mit echtem Text verwechselt werden.
-   Halten Sie den Text der Eingabeaufforderung kurz. Sie können Fragmente anstelle von vollständigen Sätzen verwenden.
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Verwenden Sie keine endinterpunktions Zeichen oder Ellipsen.
-   Der Eingabe Aufforderungs Text sollte nicht bearbeitbar sein und sollte ausgeblendet werden, wenn Benutzer in das Textfeld oder in die Tab-Taste klicken.
    -   **Ausnahme:** Die Eingabeaufforderung wird angezeigt, wenn das Textfeld den Standardeingabe Fokus besitzt, und nur verschwindet, wenn der Benutzer mit der Eingabe beginnt.
-   Der Text der Eingabeaufforderung wird wieder hergestellt, wenn das Textfeld noch leer ist, wenn es den Eingabefokus verliert.

**Falsch:** ![ Screenshot von sechs bearbeitbaren Dropdown Listen](images/ctrl-drop-image21.png)

In diesem Beispiel befindet sich der Bildschirmbereich nicht im Premium-Modus. Nachdem eine bearbeitbare Dropdown Liste ausgefüllt wurde, ist es für Benutzer schwierig, zu merken, wofür Sie sich eignet. und der Eingabe Aufforderungs Text ist bearbeitbar und wird auf die gleiche Weise wie der echte Text gezeichnet.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstände

![Screenshot der Dropdown Liste und Spezifikationen ](images/ctrl-drop-image22.png)

Empfohlene Größe und Abstände für Dropdown Listen und Kombinations Felder.

-   **Wählen Sie eine Breite aus, die für die längsten gültigen Daten geeignet ist.** Dropdown Listen können nicht horizontal scrollt werden, sodass Benutzer nur sehen können, was im Steuerelement sichtbar ist. (Beachten Sie, dass für diese Kombinations Felder eine automatische Scrollfunktion aktiviert werden kann.)
-   **Fügen Sie zusätzliche 30 Prozent** (bis zu 200 Prozent für kürzerer Text) für Text (aber nicht zahlen) ein, der lokalisiert wird.
-   **Wählen Sie eine Listen Länge aus, die unnötige vertikale Bildläufe ausschließt.** Da Dropdown Listen bei Bedarf angezeigt werden, sollten in ihren Listen bis zu 30 Elemente angezeigt werden. Bearbeitbare Listenfelder (die nicht über eine Dropdown Schaltfläche verfügen) sollten zwischen 3 und 12 Elementen angezeigt werden.

## <a name="labels"></a>Bezeichnungen

**Steuerelement Bezeichnungen**

-   Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, und beenden Sie Sie mit einem Doppelpunkt. **Ausnahmen:**
    -   Bearbeitbare Dropdown Listen mit Eingabe Aufforderungen, die sich in der Premium-Speicherplatz Eingabe befinden.
    -   Wenn eine Dropdown Liste oder ein Kombinations Feld einem Optionsfeld oder einem Kontrollkästchen untergeordnet ist und von der Bezeichnung, die mit einem Doppelpunkt endet, eingeführt wurde, legen Sie keine zusätzliche Bezeichnung für das Steuerelement fest.
-   Weisen Sie einen eindeutigen [Zugriffsschlüssel](glossary.md) für jede Bezeichnung zu. Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Positionieren Sie die Bezeichnung entweder links neben dem Steuerelement, und richten Sie die Bezeichnung am linken Rand des Steuer Elements aus. Wenn sich die Bezeichnung auf der linken Seite befindet, richten Sie den Beschriftungs Text vertikal mit dem Steuerelement Text aus.

    **Richtig:** ![ Screenshot der Ausrichtungs Ausrichtung der Dropdown Liste ](images/ctrl-drop-image23.png)

    In diesem Beispiel ist die Bezeichnung ordnungsgemäß an den Steuerelement Text ausgerichtet.

    **Falsch:** ![ Screenshot der Dropdown Liste falsch ausgerichtet ](images/ctrl-drop-image24.png)

    In diesem Beispiel ist die Bezeichnung falsch am Steuerelement Text ausgerichtet.

-   Sie können Einheiten (Sekunden, Verbindungen usw.) in Klammern hinter der Bezeichnung angeben.
-   Legen Sie den Inhalt der Dropdown Liste oder des Kombinations Felds (oder der Bezeichnung der Einheiten) nicht als Teil eines Satzes fest, da dies nicht lokalisierbar ist.

**Options Text**

-   Weisen Sie jeder Option einen eindeutigen Namen zu.
-   Verwenden Sie die groß [-](glossary.md)/Kleinschreibung, es sei denn, ein Element ist ein richtiges Substantiv.
-   Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, und verwenden Sie keine endinterpunktions Zeichen.
-   Verwenden Sie parallele Ausdrücke, und versuchen Sie, die Länge für alle Optionen auf denselben Wert zu beschränken.

**Anweisungs Text**

-   Wenn Sie Anweisungs Text zu einer Dropdown Liste oder einem Kombinations Feld hinzufügen müssen, fügen Sie ihn oberhalb der Bezeichnung hinzu. Verwenden Sie vollständige Sätze mit endinterpunktions Zeichen.
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Zusätzliche Informationen, die hilfreich, aber nicht erforderlich sind, sollten kurz gehalten werden. Legen Sie diese Informationen entweder in Klammern zwischen der Bezeichnung und dem Doppelpunkt oder ohne Klammern unterhalb des Steuer Elements ab.

    ![Screenshot der Dropdown Liste mit hinzugefügten Daten ](images/ctrl-drop-image25.png)

    Dieses Beispiel zeigt zusätzliche Informationen, die unter dem-Steuerelement platziert werden.

## <a name="documentation"></a>Dokumentation

Wenn Sie sich auf Dropdown Listen beziehen:

-   Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-und Kleinschreibung, aber nicht den Unterstrich oder Doppelpunkt des Zugriffsschlüssels. Fügen Sie Listen oder Felder ein, je nachdem, welcher Wert klarer ist.
-   Verwenden Sie für Listen Optionen den exakten Options Text, einschließlich der Groß-/Kleinschreibung.
-   Informationen zur Programmierung und anderen technischen Dokumentationen finden Sie in den Dropdown Listen in den Dropdown Listen. Verwenden Sie in jedem anderen Fall entweder List oder Box, je nachdem, welcher Wert klarer ist.
-   Um die Benutzerinteraktion zu beschreiben, verwenden Sie klicken.
-   Formatieren Sie nach Möglichkeit die Beschriftungs-und Listen Optionen mithilfe von fettem Text. Andernfalls sollten Sie die Bezeichnung und die Optionen nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Klicken Sie in der Liste **Schrift** Grad auf **große Schriftarten**.

Beim Verweisen auf Kombinations Felder:

-   Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-und Kleinschreibung, aber nicht den Unterstrich oder Doppelpunkt des Zugriffsschlüssels. Fügen Sie das Textfeld ein.
-   Verwenden Sie für Listen Optionen den genauen Options Text einschließlich der Groß-/Kleinschreibung.
-   Informationen zum Programmieren und zur anderen technischen Dokumentation finden Sie in den Kombinations Feldern als Kombinations Felder. Verwenden Sie in allen anderen Feldern Box.
-   Verwenden Sie die EINGABETASTE, um Benutzerinteraktionen zu beschreiben.
-   Formatieren Sie nach Möglichkeit die Beschriftungs-und Listen Optionen mithilfe von fettem Text. Andernfalls sollten Sie die Bezeichnung und die Optionen nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Geben Sie im Feld **Schriftart** die Schriftart ein, die Sie verwenden möchten.

 

