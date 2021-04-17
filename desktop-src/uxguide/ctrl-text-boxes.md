---
title: Text Felder
description: Mit einem Textfeld können Benutzer einen Text oder einen numerischen Wert anzeigen, eingeben oder bearbeiten.
ms.assetid: fb8ed262-1451-496d-a3f4-a29af39763bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2b5257e9772465f26815abb0f6ecbe0ff357ba4b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104530434"
---
# <a name="text-boxes"></a>Text Felder

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mit einem Textfeld können Benutzer einen Text oder einen numerischen Wert anzeigen, eingeben oder bearbeiten.

![Screenshot eines typischen Textfelds und einer Bezeichnung ](images/ctrl-text-boxes-image1.png)

Ein typisches Textfeld.

> [!Note]  
> Richtlinien im Zusammenhang mit [Layout](vis-layout.md), [Schriftarten](vis-fonts.md)und [Luftballons](ctrl-balloons.md) werden in separaten Artikeln dargestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Ist es praktikabel, alle gültigen Werte effizient aufzuzählen?** Wenn dies der Fall ist, sollten Sie stattdessen eine [Auswahlliste](ctrl-list-boxes.md), eine [Listenansicht](ctrl-list-views.md), eine [Dropdown Liste](/windows/desktop/uxguide/ctrl-drop), eine bearbeitbare Dropdown Liste oder einen [Schieberegler](ctrl-sliders.md) in Erwägung ziehen.
-   **Sind die gültigen Daten vollständig uneingeschränkt eingeschränkt? Oder ist die gültige Daten nur durch das Format eingeschränkt (eingeschränkte Länge oder Zeichen Typen)?** Wenn dies der Fall ist, verwenden Sie ein Textfeld.
-   **Stellt der Wert einen Datentyp dar, der über ein spezielles allgemeines Steuerelement verfügt?** Beispiele hierfür sind Datums-, Uhrzeit-oder IPv4-oder IPv6-Adressen. Wenn dies der Fall ist, verwenden Sie das entsprechende Steuerelement, z. b. ein Datums Steuerelement anstelle eines Textfelds.
-   Wenn die Daten numerisch sind:
    -   **Wird die Einstellung von Benutzern als relative Menge wahrgenommen?** Wenn ja, verwenden Sie einen Schieberegler.
    -   **Wäre es für Benutzer hilfreich, sofort Feedback zur Auswirkung von Einstellungsänderungen zu erhalten?** Wenn dies der Fall ist, verwenden Sie einen Schieberegler, möglicherweise zusammen mit einem Textfeld. Beispielsweise können Benutzer mithilfe eines Schiebereglers problemlos eine Farbe auswählen, da Sie sofort die Auswirkungen von Änderungen auf die Werte für Farbton, Sättigung und Helligkeit sehen können.

## <a name="design-concepts"></a>Entwurfskonzepte

Obwohl Textfelder den Vorteil haben, dass Sie sehr flexibel sind, haben Sie den Nachteil, dass Sie über minimale Einschränkungen verfügen. Für ein bearbeitbares Textfeld gelten die folgenden Einschränkungen:

-   Optional können Sie die maximale Anzahl von Zeichen festlegen.
-   Sie können die Eingabe optional nur auf numerische Zeichen (0 9) beschränken.
-   Wenn Sie ein [Drehfeld-Steuer](ctrl-spin-controls.md)Element verwenden, können Sie die Optionen für die Drehfeld Steuerung auf gültige Werte beschränken.

Abgesehen von der Länge und der optionalen Anwesenheit eines Spin-Steuer Elements haben Textfelder keine visuellen Hinweise, die die gültigen Werte oder deren Format vorschlagen. Dies bedeutet, dass Sie sich auf Bezeichnungen verlassen, um diese Informationen Benutzern zu vermitteln. Wenn Benutzer Text eingeben, der nicht gültig ist, müssen Sie den Fehler mit einer Fehlermeldung behandeln.

Als allgemeine Regel **sollten Sie die am meisten eingeschränkte Steuerung verwenden**. Verwenden Sie als letztes Mittel nicht eingeschränkte Steuerelemente wie Textfelder. Wenn Sie Einschränkungen in Erwägung ziehen, sollten Sie die Anforderungen von globalen Benutzern berücksichtigen. Beispielsweise ist ein Steuerelement, das auf die USA von Postleitzahlen beschränkt ist, nicht globalisiert, aber ein nicht eingeschränktes Textfeld, das beliebige Postleitzahl annimmt, ist.

## <a name="usage-patterns"></a>Verwendungsmuster

Ein Textfeld ist ein flexibles Steuerelement mit mehreren möglichen Verwendungsmöglichkeiten.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Dateneingabe</strong><br/> Ein einzeilige, nicht eingeschränktes Textfeld, das zum eingeben oder bearbeiten kurzer Zeichen folgen verwendet wird.<br/></td>
<td><img src="images/ctrl-text-boxes-image2.png" alt="Screen shot of a text box with Display name label " /><br/> Ein einzeilige, nicht eingeschränktes Textfeld.<br/></td>
</tr>
<tr class="even">
<td><strong>Formatierte Dateneingabe</strong><br/> Ein Satz kurzer, einzeilige Textfelder mit fester Größe, mit denen Daten in einem bestimmten Format eingegeben werden. <br/></td>
<td><img src="images/ctrl-text-boxes-image3.png" alt="Screen shot of a Product key text box " /><br/> Ein Textfeld, das für formatierte Dateneingaben verwendet wird.<br/>
<blockquote>
[!Note]<br />
Die Funktion zum <a href="glossary.md">automatischen Beenden</a> verschiebt den Eingabefokus automatisch von einem Textfeld auf das nächste. Ein Nachteil dieses Ansatzes besteht darin, dass die Daten nicht als einzelne Einheit kopiert oder eingefügt werden können.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>Unterstützte Dateneingabe</strong><br/> Ein einzeitiges, nicht eingeschränktes Textfeld zum eingeben oder Bearbeiten von Zeichen folgen in Kombination mit einer Befehls Schaltfläche, die Benutzern hilft, gültige Werte auszuwählen.<br/></td>
<td><img src="images/ctrl-text-boxes-image4.png" alt="Screen shot of text box with Browse button" /><br/> In diesem Beispiel hilft der Befehl "Durchsuchen" Benutzern dabei, gültige Werte auszuwählen.<br/></td>
</tr>
<tr class="even">
<td><strong>Texteingabe</strong><br/> Ein mehrzeilige, nicht eingeschränktes Textfeld, das verwendet wird, um lange Zeichen folgen einzugeben oder zu bearbeiten. <br/></td>
<td><img src="images/ctrl-text-boxes-image5.png" alt="Screen shot of an Address text box " /><br/> Ein mehrzeilige, nicht eingeschränktes Textfeld.<br/></td>
</tr>
<tr class="odd">
<td><strong>Numerische Eingabe</strong><br/> Ein einzeilige, numerisch formatierendes Textfeld zum eingeben oder Bearbeiten von Zahlen mit einem optionalen <a href="ctrl-spin-controls.md">Spin-Steuer</a> Element, um die Maus basierte Eingabe zu vereinfachen. <br/></td>
<td><img src="images/ctrl-text-boxes-image6.png" alt="Screen shot of a text box for entering a wait time " /><br/> Ein für numerische Eingaben verwendetes Textfeld.<br/> Die Kombination aus einem Textfeld und dem zugehörigen Drehfeld-Steuerelement wird als <a href="ctrl-spin-controls.md">Drehfeld</a>bezeichnet.<br/></td>
</tr>
<tr class="even">
<td><strong>Kennwort und PIN-Eingabe</strong><br/> Ein einzeilige, nicht eingeschränktes Textfeld, mit dem Kenn Wörter und Pins sicher eingegeben werden.<br/></td>
<td><img src="images/ctrl-text-boxes-image7.png" alt="Screen shot of a Password text box " /><br/> Ein Textfeld, mit dem Kenn Wörter eingegeben werden.<br/></td>
</tr>
<tr class="odd">
<td><strong>Datenausgabe</strong><br/> Ein einzeilige, Schreib geschütztes Textfeld, das immer ohne Rahmen angezeigt wird, um kurze Zeichen folgen anzuzeigen. <br/></td>
<td>Im Gegensatz zu statischem Text können mit einem Textfeld angezeigte Daten mittels Bildlauf (nützlich, wenn die Daten breiter als das Steuerelement sind), ausgewählt und kopiert werden.<br/> <img src="images/ctrl-text-boxes-image8.png" alt="Screen shot of a text box showing path to a folder " /><br/> Ein einzeilige, Schreib geschütztes Textfeld, das zum Anzeigen von Daten verwendet wird.<br/></td>
</tr>
<tr class="even">
<td><strong>Textausgabe</strong><br/> Ein mehrzeilige Schreib geschütztes Textfeld, in dem lange Zeichen folgen angezeigt werden. <br/></td>
<td><img src="images/ctrl-text-boxes-image9.png" alt="Screen shot of a Privacy information text box " /><br/> Ein Schreib geschütztes Textfeld, das zum Anzeigen von Daten verwendet wird.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Wenn Sie ein Textfeld deaktivieren, deaktivieren Sie auch alle zugeordneten Bezeichnungen, Anweisungs Bezeichnungen, Dreh Steuerelemente und Befehls Schaltflächen.**
-   **Verwenden Sie die automatische Vervollständigung, um Benutzern zu helfen, Daten einzugeben, die wahrscheinlich wiederholt verwendet werden**. Beispiele hierfür sind Benutzernamen, Adressen und Dateinamen. Verwenden Sie jedoch nicht die automatische Vervollständigung für Textfelder, die vertrauliche Informationen enthalten können, z. b. Kenn Wörter, Pins, Kreditkartennummern oder medizinische Informationen.
-   **Sorgen Sie dafür, dass Benutzer nicht unnötig scrollen.** Wenn Sie davon ausgehen, dass Daten größer als das Textfeld sind, und Sie das Textfeld problemlos vergrößern können, ohne dass das Layout beeinträchtigt wird, können Sie das Feld vergrößern, um einen Bildlauf zu vermeiden.

    **Falsch:**

    ![Screenshot des Textfelds "Computername" ](images/ctrl-text-boxes-image10.png)

    In diesem Beispiel sollte das Textfeld viel länger zum Verarbeiten der Daten erstellt werden.

-   Scrollleisten:
    -   **Fügen Sie keine horizontalen Schiebe leisten in mehrzeiligen Textfeldern ein.** Verwenden Sie stattdessen vertikales Scrollen und Zeilenumbrüchen.
    -   **Legen Sie keine Schiebe leisten in einzeiligen Textfeldern ab.**
-   **Für numerische Eingaben können Sie ein Drehfeld-Steuerelement verwenden.** Verwenden Sie für Texteingaben stattdessen eine Dropdown Liste oder eine bearbeitbare Dropdown Liste.
-   **Verwenden Sie die Funktion zum automatischen Beenden nicht mit Ausnahme der formatierten Dateneingabe.** Die automatische Verschiebung des Fokus kann die Benutzer überraschen.

### <a name="editable-text-boxes"></a>Bearbeitbare Textfelder

-   **Beschränken Sie die Länge des Eingabe Texts, wenn dies möglich ist.** Wenn die gültige Eingabe z. b. eine Zahl zwischen 0 und 999 ist, verwenden Sie ein numerisches Textfeld, das auf drei Zeichen begrenzt ist. Alle Teile von Textfeldern, in denen formatierte Dateneingaben verwendet werden, müssen eine kurze, festgelegte Länge aufweisen.
-   **Seien Sie flexibel mit Datenformaten.** Wenn Benutzer wahrscheinlich Text in einer Vielzahl von Formaten eingeben, versuchen Sie, alle häufigsten zu verarbeiten. Beispielsweise können viele Namen, Zahlen und Bezeichner mit optionalen Leerzeichen und Interpunktions Zeichen eingegeben werden, und die Groß-und Kleinschreibung ist oft unerheblich.
-   Wenn Sie die wahrscheinlichen Formate nicht verarbeiten können, benötigen Sie ein bestimmtes Format, indem Sie formatierte Dateneingaben verwenden, oder geben Sie die gültigen Formate in der Bezeichnung an.

    **Annehmbar:**

    ![Screenshot eines Textfelds für numerische Eingabe ](images/ctrl-text-boxes-image11.png)

    In diesem Beispiel erfordert ein Textfeld Eingaben in einem bestimmten Format.

    **Besserer**

    ![Screenshot des Eingabe Textfelds für formatierte Daten ](images/ctrl-text-boxes-image12.png)

    In diesem Beispiel wird das formatierte Dateneingabe Muster verwendet, um ein bestimmtes Format anzufordern.

    **Best**

    ![Screenshot eines nicht eingeschränkten Textfelds ](images/ctrl-text-boxes-image13.png)

    In diesem Beispiel werden in einem Textfeld alle wahrscheinlichen Formate behandelt.

-   Bei der Auswahl der maximalen Eingabe Länge sollten Sie die Formatflexibilität in Erwägung gezogen Eine gültige Kreditkartennummer kann z. b. bis zu 19 Zeichen lang sein. durch das Einschränken der Länge auf einen kürzeren Wert wird die Eingabe von Zahlen in den längeren Formaten erschwert.
-   **Verwenden Sie das Format für formatierte Dateneingaben nicht, wenn Benutzer mit höherer Wahrscheinlichkeit in lange, komplexe Daten eingefügt werden.** Reservieren Sie stattdessen das formatierte Dateneingabe Muster für Situationen, in denen Benutzer die Daten wahrscheinlicher eingeben.

    ![Screenshot eines Textfelds mit der Bezeichnung: IPv6-Adresse ](images/ctrl-text-boxes-image14.png)

    In diesem Beispiel wird das formatierte Dateneingabe Muster nicht verwendet, sodass Benutzer IPv6-Adressen einfügen können.

-   **Wenn Benutzer wahrscheinlicher werden, dass Sie den gesamten Wert erneut eingeben, wählen Sie den gesamten Text im Eingabefokus aus.** Wenn Benutzer die Wahrscheinlichkeit haben, dass Sie bearbeitet werden, platzieren Sie die Einfügemarke am Ende des Texts.

    ![Screenshot eines Kennwort-Textfelds ](images/ctrl-text-boxes-image15.png)

    In diesem Beispiel ist es wahrscheinlicher, dass Benutzer als "Edit" ersetzt werden, sodass der gesamte Wert im Eingabefokus ausgewählt wird.

    ![Screenshot eines Textfelds zum Eingeben von Schlüsselwörtern ](images/ctrl-text-boxes-image16.png)

    In diesem Beispiel ist es wahrscheinlicher, dass Benutzerschlüssel Wörter hinzufügen, als den Text zu ersetzen, sodass die Einfügemarke am Ende des Texts platziert wird.

-   **Verwenden Sie immer ein mehr zeitiges Textfeld, wenn neue Zeilenzeichen gültige Eingaben sind.**
-   **Wenn das Textfeld für eine Datei oder einen Pfad steht, stellen Sie immer eine Schaltfläche zum Durchsuchen bereit.**

### <a name="numeric-text-boxes"></a>Numerische Textfelder

-   **Wählen Sie die am einfachsten geeignete Einheit aus, und bezeichnen Sie die Einheiten.** Verwenden Sie z. b. die Verwendung von Millilitern anstelle von Litern (oder umgekehrt), Prozentsätzen anstelle direkter Werte (oder umgekehrt) usw.

    **Richtig:**

    ![Screenshot des Textfelds mit "Litern als Einheit" ](images/ctrl-text-boxes-image17.png)

    In diesem Beispiel wird die-Einheit als bezeichnet, erfordert jedoch, dass Benutzer Dezimalzahlen eingeben.

    **Besserer**

    ![Screenshot des Textfelds mit Millilitern als Einheit ](images/ctrl-text-boxes-image18.png)

    In diesem Beispiel verwendet das Textfeld eine komfortablere Einheit.

-   **Verwenden Sie ein Drehfeld-Steuerelement, wenn es hilfreich ist.** Manchmal sind Dreh Steuerelemente jedoch nicht praktikabel, z. b. Wenn Benutzer viele große Zahlen eingeben müssen. Dreh Steuerelemente verwenden, wenn:
    -   Die Eingabe ist wahrscheinlich eine kleine Zahl, in der Regel unter 100.
    -   Benutzer nehmen wahrscheinlich eine kleine Änderung an einer vorhandenen Zahl vor.
    -   Es ist wahrscheinlicher, dass Benutzer die Maus verwenden, als die Tastatur zu verwenden.
-   **Numerischen Text rechtsbündig ausrichten:**

    -   Es ist mehr als ein numerisches Textfeld vorhanden.
    -   Die Textfelder sind vertikal ausgerichtet.
    -   Benutzer können die Werte wahrscheinlich hinzufügen oder vergleichen.

    **Richtig:**

    ![Screenshot der Ausgaben Textfelder (Hotel usw.) ](images/ctrl-text-boxes-image19.png)

    In diesem Beispiel wird der numerische Text rechtsbündig ausgerichtet, um das Vergleichen von Werten zu erleichtern.

    **Falsch:**

    ![Screenshot von Textfeldern für RGB-Werte ](images/ctrl-text-boxes-image20.png)

    In diesem Beispiel ist der numerische Text falsch linksbündig ausgerichtet.

-   **Sie sollten Währungswerte immer rechtsbündig ausrichten.**
-   **Weisen Sie bestimmten numerischen Werten keine besondere Bedeutungen zu**, selbst wenn diese besondere Bedeutungen intern von Ihrer Anwendung verwendet werden. Verwenden Sie stattdessen Kontrollkästchen oder Options Felder für eine explizite Benutzer Auswahl.

    **Falsch:**

    ![Screenshot der Bezeichnung: Verwenden von "-1" zum Deaktivieren der Zwischenspeicherung ](images/ctrl-text-boxes-image21.png)

    In diesem Beispiel hat der Wert-1 eine besondere Bedeutung.

    **Richtig:**

    ![Screenshot der Kontrollkästchen Bezeichnung: Caching ](images/ctrl-text-boxes-image22.png)

    In diesem Beispiel wird die-Option durch ein Kontrollkästchen explizit.

### <a name="password-and-pin-input"></a>Kennwort und PIN-Eingabe

-   **Verwenden Sie immer das allgemeine Kennwort, anstatt ein eigenes Kennwort zu erstellen.** Kenn Wörter und Pins erfordern eine besondere Behandlung, damit Sie sicher verarbeitet werden.

Weitere Richtlinien und Beispiele finden Sie unter [Luftballons](ctrl-balloons.md).

### <a name="textual-output"></a>Textausgabe

-   **Verwenden Sie ggf. die Farbe des weißen hintergrundsystems für großen, mehrzeiligen schreibgeschützten Text.** Durch einen weißen Hintergrund wird der Text leichter lesbar. Viel Text in einem grauen Hintergrund verhindert das lesen.

Weitere Informationen zu Hintergrundfarben finden Sie unter [Schriftarten](vis-fonts.md).

### <a name="data-output"></a>Datenausgabe

-   **Verwenden Sie keinen Rahmen für einzeilige schreibgeschützte Textfelder.** Der Rahmen ist ein visueller Hinweis darauf, dass der Text bearbeitbar ist.
-   **Deaktivieren Sie nicht schreibgeschützte einzeilige Textfelder.** Dadurch wird verhindert, dass Benutzer den Text in die Zwischenablage auswählen und kopieren. Außerdem wird verhindert, dass Benutzer einen Bildlauf durchführen, wenn Sie die Größe ihrer Grenzen überschreiten.
-   **Legen Sie einen Tabstopp nicht in einem schreibgeschützten einzeiligen Textfeld fest, wenn der Benutzer wahrscheinlich keinen Bildlauf durchführen oder den Text kopieren muss.**

## <a name="input-validation-and-error-handling"></a>Eingabevalidierung und Fehlerbehandlung

Da Textfelder in der Regel nicht darauf beschränkt sind, nur gültige Eingaben zu akzeptieren, müssen Sie möglicherweise die Eingabe validieren und Probleme behandeln. Überprüfen Sie die verschiedenen Arten von Eingabe Problemen wie folgt:

-   Wenn der Benutzer ein ungültiges Zeichen eingibt, ignorieren Sie das Zeichen und zeigen eine [Eingabeproblem](ctrl-balloons.md) Sprechblase an, in der die gültigen Zeichen erläutert werden.

    ![Screenshot des Product Key Textfelds](images/ctrl-text-boxes-image23.png)

    In diesem Beispiel meldet eine Sprechblase ein falsches Eingabezeichen.

-   Wenn die Eingabedaten einen ungültigen Wert oder ein ungültiges Format aufweisen, zeigen Sie eine Sprechblase für Eingabe Probleme an, wenn das Textfeld den Eingabefokus verliert.
-   Wenn die Eingabedaten mit anderen Steuerelementen im Fenster inkonsistent sind, geben Sie eine Fehlermeldung an, wenn die gesamte Eingabe vollständig ist, z. b. Wenn Benutzer in einem modalen Dialogfeld auf OK klicken.

**Löschen Sie keine ungültigen Eingabedaten, es sei denn, die Benutzer können Fehler problemlos beheben.** Dies ermöglicht es Benutzern, Fehler zu beheben, ohne zu beginnen. Sie sollten z. b. falsche Kenn Wörter und Pins löschen, da Sie nicht auf einfache Weise korrigiert werden können.

Weitere Richtlinien und Beispiele finden Sie unter [Fehlermeldungen](mess-error.md) und [Luftballons](ctrl-balloons.md).

## <a name="prompts"></a>Eingabeaufforderungen

Eine Eingabeaufforderung ist eine Bezeichnung oder eine kurze Anweisung in einem Textfeld als Standardwert. Im Gegensatz zu statischem Text werden Aufforderungen auf dem Bildschirm ausgeblendet, sobald Benutzer etwas in das Textfeld eingeben oder den Eingabefokus erhalten.

![Screenshot des Eingabe Aufforderungs-Textfelds mit Bezeichnung: Suchen ](images/ctrl-text-boxes-image24.png)

Eine typische Eingabeaufforderung.

Verwenden Sie eine Eingabeaufforderung, wenn:

-   Der Bildschirmbereich ist so hoch, dass die Verwendung einer Bezeichnung oder Anweisung nicht erwünscht ist, z. b. auf einer Symbolleiste.
-   Bei der Eingabeaufforderung wird in erster Linie der Zweck des Textfelds auf kompakte Weise identifiziert. Dabei darf es sich nicht um wichtige Informationen handeln, die der Benutzer während der Verwendung des Textfelds sehen muss.

Verwenden Sie keine Aufforderungen, um Benutzer zur Eingabe von etwas oder zum Klicken auf Schaltflächen zu leiten. Schreiben Sie z. b. nicht den Text der Eingabeaufforderung, und klicken Sie dann auf senden.

Bei Verwendung von Eingabe Aufforderungen:

-   Zeichnen Sie den Eingabe Aufforderungs Text in kursiv grau und den eigentlichen Eingabetext in normaler schwarz. Der Eingabe Aufforderungs Text darf nicht mit echtem Text verwechselt werden.
-   Halten Sie den Text der Eingabeaufforderung kurz. Sie können Fragmente anstelle von vollständigen Sätzen verwenden.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Verwenden Sie keine endinterpunktions Zeichen oder Ellipsen.
-   Der Eingabe Aufforderungs Text sollte nicht bearbeitbar sein und sollte ausgeblendet werden, wenn Benutzer in das Textfeld oder die Tab-Taste klicken.
    -   **Ausnahme:** Wenn das Textfeld den Standardeingabe Fokus besitzt, wird die Eingabeaufforderung angezeigt, und Sie verschwindet, sobald der Benutzer mit der Eingabe beginnt.
-   Der Text der Eingabeaufforderung wird wieder hergestellt, wenn das Textfeld noch leer ist, wenn es den Eingabefokus verliert.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstände

![Abbildung von einzeiligen und zweizeiligen Textfeldern ](images/ctrl-text-boxes-image25.png)

Empfohlene Größe und Abstände für Textfelder.

Die Breite eines Textfelds ist ein visueller Hinweis auf die erwartete Eingabe Größe. Beim Anpassen von Textfeldern:

-   **Wählen Sie eine Breite aus, die für die längsten gültigen Daten geeignet ist.** In den meisten Fällen sollten Benutzer keinen Bildlauf der längsten wahrscheinlichen Zeichenfolge durchführen, die Sie eingeben oder anzeigen.
-   **Fügen Sie zusätzliche 30 Prozent** (bis zu 200 Prozent für kürzerer Text) für Text (aber nicht zahlen) ein, der lokalisiert wird.
-   **Wenn die erwartete Eingabe keine bestimmte Größe hat, wählen Sie eine Breite aus, die mit den anderen Textfeldern oder Steuerelementen im Fenster konsistent ist.**
-   **Größe für mehrzeilige Textfelder, um eine ganzzahlige Anzahl von Textzeilen anzuzeigen.**

## <a name="labels"></a>Bezeichnungen

### <a name="text-box-labels"></a>Text Feld Bezeichnungen

-   Alle Textfelder benötigen Bezeichnungen. Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, enden Sie mit einem Doppelpunkt, und verwenden Sie [statischen Text](glossary.md).

    **Ausnahmen:**

    -   Text Felder mit Eingabe Aufforderungen, die sich in einem Premium-Bereich befinden.
    -   Bei der Bezeichnung sollte eine Gruppe von Textfeldern, die für **formatierte Dateneingaben** verwendet werden, als einzelnes Textfeld behandelt werden.
    -   Wenn ein Textfeld einem Optionsfeld oder Kontrollkästchen untergeordnet ist und durch seine Bezeichnung mit einem Doppelpunkt vorangestellt wird, sollten Sie keine zusätzliche Bezeichnung für das Textfeld einfügen.
    -   **Lassen Sie Steuerelement Bezeichnungen aus, die die main-Anweisung wiedergeben.** In diesem Fall nimmt die main-Anweisung den Doppelpunkt (es sei denn, es handelt sich um eine Frage) und den Zugriffsschlüssel.

        **Annehmbar:**

        ![Screenshot des Textfelds mit wiederhollicher Bezeichnung](images/ctrl-text-boxes-image26.png)

        In diesem Beispiel ist die Textfeld-Bezeichnung lediglich eine erneute Anweisung der Main-Anweisung.

        **Besserer**

        ![Screenshot des Textfelds mit Haupt Anweisung ](images/ctrl-text-boxes-image27.png)

        In diesem Beispiel wird die redundante Bezeichnung entfernt, sodass die Haupt Anweisung den Doppelpunkt und die Zugriffstaste übernimmt.

-   Weisen Sie einen eindeutigen Zugriffsschlüssel zu. Richtlinien für die Zugriffsschlüssel Zuweisung finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Positionieren Sie die Bezeichnung entweder links neben dem Textfeld, und richten Sie die Bezeichnung am linken Rand des Textfelds aus. Wenn sich die Bezeichnung auf der linken Seite befindet, richten Sie den Beschriftungs Text vertikal mit dem Text Feld Text aus.

    **Richtig:**

    ![Screenshot der linksbündig ausgerichteten Bezeichnung oberhalb des Textfelds ](images/ctrl-text-boxes-image28.png)

    ![Screenshot der Text ausgerichteten Bezeichnung links vom Textfeld ](images/ctrl-text-boxes-image29.png)

    In diesen Beispielen richtet sich die Bezeichnung am oberen Rand am linken Rand des Textfelds, und die Bezeichnung auf der linken Seite richtet sich nach dem Text im Textfeld.

    **Falsch:**

    ![Screenshot der Text ausgerichteten Bezeichnung oberhalb des Textfelds ](images/ctrl-text-boxes-image30.png)

    ![Screenshot der oben ausgerichteten Bezeichnung links vom Textfeld ](images/ctrl-text-boxes-image31.png)

    In diesen falschen Beispielen richtet sich die Bezeichnung oben mit dem Text im Textfeld, und die Bezeichnung auf der linken Seite richtet sich nach dem oberen Rand des Textfelds.

-   Sie können Einheiten (z. b. Sekunden oder Verbindungen) in Klammern hinter der Bezeichnung angeben.
-   Wenn ein Textfeld eine beliebig kleine maximale Anzahl von Zeichen akzeptiert, können Sie die maximale Eingabe in der Bezeichnung angeben. Die Breite des Textfelds sollte außerdem die maximale Größe vorschlagen.

    ![Screenshot des Kennworts (Textfeld) ](images/ctrl-text-boxes-image32.png)

    In diesem Beispiel gibt die Bezeichnung die maximale Anzahl von Zeichen an.

-   Machen Sie den Inhalt des Textfelds (oder seiner Einheiten Bezeichnung) nicht Teil eines Satzes, da dies nicht lokalisierbar ist.
-   Wenn das Textfeld verwendet werden kann, um mehrere Elemente einzugeben, legen Sie fest, wie die Elemente in der Bezeichnung getrennt werden sollen.

    ![Screenshot der Bezeichnung von separaten Namen mit Semikolon ](images/ctrl-text-boxes-image33.png)

    In diesem Beispiel wird das Element Trennzeichen in der Bezeichnung angegeben.

-   Richtlinien zum Angeben der erforderlichen Eingabe finden Sie unter erforderliche Eingabe in [Dialog Feldern](win-dialog-box.md).

### <a name="instruction-labels"></a>Anweisungs Bezeichnungen

-   Wenn Sie Anweisungs Text über ein Textfeld hinzufügen müssen, fügen Sie ihn oberhalb der Bezeichnung hinzu. Verwenden Sie vollständige Sätze mit endinterpunktions Zeichen.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Zusätzliche Informationen, die hilfreich, aber nicht erforderlich sind, sollten kurz gehalten werden. Legen Sie diese Informationen entweder in Klammern zwischen der Bezeichnung und dem Doppelpunkt oder ohne Klammern unterhalb des Textfelds ab.

    ![Screenshot der hinzugefügten Informationen unten im Textfeld ](images/ctrl-text-boxes-image34.png)

    In diesem Beispiel werden unter dem Textfeld zusätzliche Informationen eingefügt.

### <a name="prompt-labels"></a>Bezeichnungen Aufforderungs Zeichen

-   Halten Sie den Text der Eingabeaufforderung kurz. Sie können Fragmente anstelle von vollständigen Sätzen verwenden.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Verwenden Sie keine endinterpunktions Zeichen oder Ellipsen.
-   Wenn die Eingabeaufforderung Benutzer zur Eingabe von Informationen auffordert, die durch eine Schaltfläche neben dem Textfeld bearbeitet werden, platzieren Sie einfach die Schaltfläche neben dem Textfeld. Verwenden Sie die Eingabeaufforderung nicht, um Benutzer zum Klicken auf die Schaltfläche zu leiten (schreiben Sie z. b. keinen Eingabe Aufforderungs Text, und klicken Sie dann auf Senden).

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Textfelder:

-   Verwenden Sie den Typ, um auf Benutzerinteraktionen zu verweisen, die eine Typisierung oder Einfügen erfordern. Andernfalls verwenden Sie die EINGABETASTE, wenn Benutzer mithilfe anderer Methoden Informationen in das Textfeld einfügen können, z. b. das Auswählen des Werts aus einer Liste oder das Verwenden einer Schaltfläche Durchsuchen.
-   Verwenden Sie SELECT, um auf einen Eintrag in einem schreibgeschützten Textfeld zu verweisen.
-   Verwenden Sie den genauen Bezeichnungs Text einschließlich der Groß-und Kleinschreibung, und schließen Sie das Textfeld ein. Fügen Sie den Unterstrich oder Doppelpunkt des Zugriffsschlüssels nicht ein. Verweisen Sie nicht auf ein Textfeld als Textfeld oder Feld.
-   Formatieren Sie nach Möglichkeit die Bezeichnung mit fettem Text. Andernfalls sollten Sie die Bezeichnung nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

    Beispiel: Geben Sie Ihr Kennwort in das Feld **Kennwort ein** , und klicken Sie dann auf **OK**.

-   Wenn für das Textfeld ein bestimmtes Format erforderlich ist, sollten Sie nur das am häufigsten verwendete akzeptable Format dokumentieren. Ermöglichen Sie Benutzern, beliebige andere Formate selbst zu erkennen. Sie möchten mit Datenformaten flexibel sein, aber dies sollte nicht zu einer komplexen Dokumentation führen.

    **Richtig:**

    Geben Sie die Seriennummer des Teils mit dem 1234-56-7890-Format ein.

    **Falsch:**

    Geben Sie die Seriennummer des Teils in einem der folgenden Formate ein:

    1234567890

    1234-56-7890

    1234 56 7890

