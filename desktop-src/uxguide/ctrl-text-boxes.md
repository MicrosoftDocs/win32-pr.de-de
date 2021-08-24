---
title: Textfelder
description: Mit einem Textfeld können Benutzer text- oder numerische Werte anzeigen, eingeben oder bearbeiten.
ms.assetid: fb8ed262-1451-496d-a3f4-a29af39763bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 63418b3f72691e5ac23638291b9ec8aa83bc78d2f89815e093f5a04850a3d9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819425"
---
# <a name="text-boxes"></a>Textfelder

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Mit einem Textfeld können Benutzer text- oder numerische Werte anzeigen, eingeben oder bearbeiten.

![Screenshot eines typischen Textfelds und einer Bezeichnung ](images/ctrl-text-boxes-image1.png)

Ein typisches Textfeld.

> [!Note]  
> Richtlinien im Zusammenhang [mit Layout,](vis-layout.md) [Schriftarten](vis-fonts.md)und [Balloons](ctrl-balloons.md) werden in separaten Artikeln vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Ist es praktisch, alle gültigen Werte effizient aufzählen?** Wenn dies [](ctrl-list-boxes.md)der Fall ist, sollten Sie stattdessen eine Einzelauswahlliste, eine Listenansicht, [](ctrl-list-views.md)eine Dropdownliste, [](/windows/desktop/uxguide/ctrl-drop)eine bearbeitbare Dropdownliste oder einen [Schieberegler](ctrl-sliders.md) verwenden.
-   **Sind die gültigen Daten vollständig untrainiert? Oder sind die gültigen Daten nur durch das Format (eingeschränkte Länge oder Zeichentypen) eingeschränkt?** Wenn ja, verwenden Sie ein Textfeld.
-   **Stellt der Wert einen Datentyp dar, der über ein spezielles allgemeines Steuerelement verfügt?** Beispiele hierfür sind Datum, Uhrzeit oder IPv4- oder IPv6-Adresse. Verwenden Sie in diesem Beispiel das entsprechende Steuerelement, z. B. ein Datumssteuerfeld anstelle eines Textfelds.
-   Wenn die Daten numerisch sind:
    -   **Betrachten Benutzer die Einstellung als relative Menge?** Wenn ja, verwenden Sie einen Schieberegler.
    -   **Wäre es für Benutzer hilfreich, sofort Feedback zur Auswirkung von Einstellungsänderungen zu erhalten?** Wenn ja, verwenden Sie einen Schieberegler, möglicherweise zusammen mit einem Textfeld. Beispielsweise können Benutzer mithilfe eines Schiebereglers problemlos eine Farbe auswählen, da sie sofort die Auswirkungen von Änderungen an Farbton-, Sättigungs- oder Helligkeitswerten sehen können.

## <a name="design-concepts"></a>Entwurfskonzepte

Obwohl Textfelder den Vorteil haben, dass sie sehr flexibel sind, haben sie den Nachteil, dass sie minimale Einschränkungen haben. Die einzigen Einschränkungen für ein bearbeitbares Textfeld sind:

-   Sie können optional die maximale Anzahl von Zeichen festlegen.
-   Optional können Sie die Eingabe auf numerische Zeichen (0 9) beschränken.
-   Wenn Sie ein Drehungssteuer [steuerelement verwenden,](ctrl-spin-controls.md)können Sie die Auswahl der Drehungssteuerung auf gültige Werte beschränken.

Abgesehen von ihrer Länge und dem optionalen Vorhandensein eines Drehungssteuerfelds weisen Textfelder keine visuellen Hinweise auf, die die gültigen Werte oder ihr Format vorschlagen. Dies bedeutet, dass Sie sich auf Bezeichnungen verlassen, um diese Informationen für Benutzer zu übermitteln. Wenn Benutzer ungültigen Text eingeben, müssen Sie den Fehler mit einer Fehlermeldung behandeln.

Als allgemeine Regel sollten **Sie das am stärksten eingeschränkte Steuerelement verwenden, das Sie verwenden können.** Verwenden Sie als letztes Mittel ungeniert Steuerelemente wie Textfelder. Beachten Sie bei der Berücksichtigung von Einschränkungen jedoch die Anforderungen globaler Benutzer. Beispielsweise wird ein Steuerelement, das auf die USA-Postleitzahlen beschränkt ist, nicht globalisiert, aber ein nicht eingeschränktes Textfeld, das ein beliebiges Postleitzahlformat akzeptiert, ist .

## <a name="usage-patterns"></a>Verwendungsmuster

Ein Textfeld ist ein flexibles Steuerelement mit mehreren möglichen Verwendungsmöglichkeiten.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Dateneingabe</strong><br/> Ein einzeilenbasiertes, nicht trainiertes Textfeld, das zum Eingeben oder Bearbeiten kurzer Zeichenfolgen verwendet wird.<br/></td>
<td><img src="images/ctrl-text-boxes-image2.png" alt="Screen shot of a text box with Display name label " /><br/> Ein einzeilenbasiertes, nicht trainiertes Textfeld.<br/></td>
</tr>
<tr class="even">
<td><strong>Formatierte Dateneingabe</strong><br/> Ein Satz kurzer, einzeiler Textfelder mit fester Größe, die zum Eingeben von Daten in einem bestimmten Format verwendet werden. <br/></td>
<td><img src="images/ctrl-text-boxes-image3.png" alt="Screen shot of a Product key text box " /><br/> Ein Textfeld, das für formatierte Dateneingaben verwendet wird.<br/>
<blockquote>
[!Note]<br />
Das <a href="glossary.md">Feature zum automatischen</a> Beenden stellt den Eingabefokus automatisch von einem Textfeld auf das nächste. Ein Nachteil dieses Ansatzes ist, dass die Daten nicht als einzelne Einheit kopiert oder kopiert werden können.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>Unterstützte Dateneingabe</strong><br/> Ein einzeilenbasiertes, nicht trainiertes Textfeld, das zum Eingeben oder Bearbeiten von Zeichenfolgen verwendet wird, kombiniert mit einer Befehlsschaltfläche, mit der Benutzer gültige Werte auswählen können.<br/></td>
<td><img src="images/ctrl-text-boxes-image4.png" alt="Screen shot of text box with Browse button" /><br/> In diesem Beispiel hilft der Befehl Durchsuchen Benutzern bei der Auswahl gültiger Werte.<br/></td>
</tr>
<tr class="even">
<td><strong>Texteingabe</strong><br/> Ein mehrzeilenbasiertes, nicht übergreifendes Textfeld, das zum Eingeben oder Bearbeiten langer Zeichenfolgen verwendet wird. <br/></td>
<td><img src="images/ctrl-text-boxes-image5.png" alt="Screen shot of an Address text box " /><br/> Ein mehrzeilenbasiertes, nicht übergreifendes Textfeld.<br/></td>
</tr>
<tr class="odd">
<td><strong>Numerische Eingabe</strong><br/> Ein einzeigen, nur numerisches Textfeld, das zum Eingeben oder Bearbeiten von Zahlen verwendet wird, mit einem <a href="ctrl-spin-controls.md">optionalen</a> Drehungssteuerfeld, um mausbasierte Eingaben zu ermöglichen. <br/></td>
<td><img src="images/ctrl-text-boxes-image6.png" alt="Screen shot of a text box for entering a wait time " /><br/> Ein Textfeld, das für numerische Eingaben verwendet wird.<br/> Die Kombination aus einem Textfeld und dem zugehörigen Drehsteuerfeld wird als <a href="ctrl-spin-controls.md">Drehfeld bezeichnet.</a><br/></td>
</tr>
<tr class="even">
<td><strong>Kennwort- und PIN-Eingabe</strong><br/> Ein einzeilenbasiertes, nicht trainiertes Textfeld, das zum sicheren Eingeben von Kennwörtern und PINs verwendet wird.<br/></td>
<td><img src="images/ctrl-text-boxes-image7.png" alt="Screen shot of a Password text box " /><br/> Ein Textfeld zum Eingeben von Kennwörtern.<br/></td>
</tr>
<tr class="odd">
<td><strong>Datenausgabe</strong><br/> Ein einzeilenbasiertes, schreibgeschütztes Textfeld, das immer ohne Rahmen angezeigt wird und zum Anzeigen kurzer Zeichenfolgen verwendet wird. <br/></td>
<td>Im Gegensatz zu statischem Text können daten, die mithilfe eines Textfelds angezeigt werden, gescrollt (nützlich, wenn die Daten breiter als das Steuerelement sind), ausgewählt und kopiert werden.<br/> <img src="images/ctrl-text-boxes-image8.png" alt="Screen shot of a text box showing path to a folder " /><br/> Ein einzeilenbasiertes, schreibgeschütztes Textfeld, das zum Anzeigen von Daten verwendet wird.<br/></td>
</tr>
<tr class="even">
<td><strong>Textausgabe</strong><br/> Ein mehrzeilenbasiertes, schreibgeschütztes Textfeld, das zum Anzeigen langer Zeichenfolgen verwendet wird. <br/></td>
<td><img src="images/ctrl-text-boxes-image9.png" alt="Screen shot of a Privacy information text box " /><br/> Ein schreibgeschütztes Textfeld, das zum Anzeigen von Daten verwendet wird.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Deaktivieren Sie beim Deaktivieren eines Textfelds auch alle zugeordneten Bezeichnungen, Anweisungsbezeichnungen, Drehsteuerelemente und Befehlsschaltflächen.**
-   **Verwenden Sie die automatische Vervollstehung, um Benutzern die Eingabe von** Daten zu ermöglichen, die wahrscheinlich wiederholt verwendet werden. Beispiele hierfür sind Benutzernamen, Adressen und Dateinamen. Verwenden Sie jedoch nicht die automatische Vervollstität für Textfelder, die vertrauliche Informationen wie Kennwörter, PINs, Kreditkartennummern oder medizinische Informationen enthalten können.
-   **Lassen Sie Benutzer nicht unnötig scrollen.** Wenn Sie erwarten, dass die Daten größer als das Textfeld sind, und Sie das Textfeld problemlos vergrößern können, ohne das Layout zu schädlich zu machen, sollten Sie die Größe des Felds so anpassen, dass kein Bildlauf mehr notwendig ist.

    **Falsch:**

    ![Screenshot eines Textfelds für einen Computernamen ](images/ctrl-text-boxes-image10.png)

    In diesem Beispiel sollte das Textfeld wesentlich länger für die Verarbeitung seiner Daten verwendet werden.

-   Scrollleisten:
    -   **Legen Sie keine horizontalen Bildlaufleisten in mehrzeilenbasierten Textfeldern ab.** Verwenden Sie stattdessen vertikales Scrollen und Zeilenumbruch.
    -   **Setzen Sie keine Bildlaufleisten in einzeilenbasierte Textfelder.**
-   **Für numerische Eingaben können Sie ein Drehungssteuerfeld verwenden.** Verwenden Sie für Texteingaben stattdessen eine Dropdownliste oder eine bearbeitbare Dropdownliste.
-   **Verwenden Sie das Feature für automatisches Beenden nur für formatierte Dateneingaben.** Die automatische Fokusverschiebung kann Benutzer versischen.

### <a name="editable-text-boxes"></a>Bearbeitbare Textfelder

-   **Schränken Sie die Länge des Eingabetexts ein, wenn sie dies können.** Wenn die gültige Eingabe beispielsweise eine Zahl zwischen 0 und 999 ist, verwenden Sie ein numerisches Textfeld, das auf drei Zeichen beschränkt ist. Alle Teile von Textfeldern, die formatierte Dateneingaben verwenden, müssen eine kurze feste Länge haben.
-   **Seien Sie flexibel mit Datenformaten.** Wenn Benutzer wahrscheinlich Text mit einer Vielzahl von Formaten eingeben, versuchen Sie, alle gängigsten Formate zu verarbeiten. Beispielsweise können viele Namen, Zahlen und Bezeichner mit optionalen Leerzeichen und Interpunktion eingegeben werden, und die Groß-/Zu-/Abzeichen spielt häufig keine Rolle.
-   Wenn Sie die wahrscheinlichen Formate nicht verarbeiten können, fordern Sie ein bestimmtes Format mithilfe der formatierten Dateneingabe an, oder geben Sie die gültigen Formate in der Bezeichnung an.

    **Annehmbar:**

    ![Screenshot eines Textfelds für numerische Eingaben ](images/ctrl-text-boxes-image11.png)

    In diesem Beispiel erfordert ein Textfeld Eingaben in einem bestimmten Format.

    **Besser:**

    ![Screenshot des Formatierens des Textfelds für die Dateneingabe ](images/ctrl-text-boxes-image12.png)

    In diesem Beispiel wird das formatierte Dateneingabemuster verwendet, um ein bestimmtes Format zu erfordern.

    **Beste:**

    ![Screenshot eines uneingeschränkten Textfelds ](images/ctrl-text-boxes-image13.png)

    In diesem Beispiel verarbeitet ein Textfeld alle wahrscheinlichen Formate.

-   Berücksichtigen Sie die Formatflexibilität bei der Auswahl der maximalen Eingabelänge. Eine gültige Kreditkartennummer kann z. B. bis zu 19 Zeichen verwenden, sodass es schwierig wäre, Zahlen mit den längeren Formaten einzugeben, wenn die Länge auf einen kürzeren Wert beschränkt wird.
-   **Verwenden Sie nicht das formatierte Dateneingabemuster, wenn Benutzer mit größerer Wahrscheinlichkeit lange, komplexe Daten einfügen.** Reservieren Sie stattdessen das formatierte Dateneingabemuster für Situationen, in denen Benutzer die Daten eher eingeben.

    ![Screenshot eines Textfelds mit Bezeichnung: ipv6-Adresse ](images/ctrl-text-boxes-image14.png)

    In diesem Beispiel wird das formatierte Dateneingabemuster nicht verwendet, sodass Benutzer IPv6-Adressen einfügen können.

-   **Wenn Benutzer wahrscheinlich den gesamten Wert erneut eingeben, wählen Sie den gesamten Text im Eingabefokus aus.** Wenn Benutzer eher bearbeiten, platzieren Sie das Caretzeichen am Ende des Texts.

    ![Screenshot eines Kennworttextfelds ](images/ctrl-text-boxes-image15.png)

    In diesem Beispiel ersetzen Benutzer eher als bearbeiten, sodass der gesamte Wert im Eingabefokus ausgewählt wird.

    ![Screenshot eines Textfelds zum Eingeben von Schlüsselwörtern ](images/ctrl-text-boxes-image16.png)

    In diesem Beispiel fügen Benutzer wahrscheinlich Schlüsselwörter hinzu, als den Text zu ersetzen, sodass das Caretzeichen am Ende des Texts platziert wird.

-   **Verwenden Sie immer ein mehrzeiliges Textfeld, wenn Zeilenzeilenzeichen gültige Eingaben sind.**
-   **Wenn das Textfeld für eine Datei oder einen Pfad vorgesehen ist, geben Sie immer die Schaltfläche Durchsuchen an.**

### <a name="numeric-text-boxes"></a>Numerische Textfelder

-   **Wählen Sie die bequemste Einheit aus, und bezeichnen Sie die Einheiten.** Erwägen Sie beispielsweise die Verwendung von Millilitern anstelle von Litern (oder umgekehrt), Prozentsätzen anstelle direkter Werte (oder umgekehrt) usw.

    **Richtig:**

    ![Screenshot des Textfelds mit Litern als Einheit ](images/ctrl-text-boxes-image17.png)

    In diesem Beispiel ist die Einheit bezeichnet, erfordert jedoch, dass Benutzer Dezimalzahlen eingeben.

    **Besser:**

    ![Screenshot des Textfelds mit Millilitern als Einheit ](images/ctrl-text-boxes-image18.png)

    In diesem Beispiel verwendet das Textfeld eine praktischere Einheit.

-   **Verwenden Sie immer dann ein Drehsteuerelement, wenn es hilfreich ist.** Manchmal sind Drehsteuerelemente jedoch nicht praktikabel, z. B. wenn Benutzer viele große Zahlen eingeben müssen. Verwenden von Drehsteuerelementen in den:
    -   Die Eingabe ist wahrscheinlich eine kleine Zahl, in der Regel unter 100.
    -   Benutzer nehmen wahrscheinlich eine kleine Änderung an einer vorhandenen Zahl vor.
    -   Benutzer verwenden wahrscheinlich eher die Maus als die Tastatur.
-   **Richten Sie numerischen Text immer dann rechts aus, wenn:**

    -   Es gibt mehrere numerische Textfelder.
    -   Die Textfelder sind vertikal ausgerichtet.
    -   Benutzer werden die Werte wahrscheinlich hinzufügen oder vergleichen.

    **Richtig:**

    ![Screenshot der Ausgabentextfelder (Hotel usw.) ](images/ctrl-text-boxes-image19.png)

    In diesem Beispiel wird der numerische Text rechtsbündig ausgerichtet, um das Vergleichen von Werten zu vereinfachen.

    **Falsch:**

    ![Screenshot von Textfeldern für RGB-Werte ](images/ctrl-text-boxes-image20.png)

    In diesem Beispiel ist der numerische Text falsch linksbündig ausgerichtet.

-   **Richten Sie monetäre Werte immer rechts aus.**
-   **Weisen Sie bestimmten numerischen Werten keine besonderen Bedeutungen zu,** auch wenn diese speziellen Bedeutungen intern von Ihrer Anwendung verwendet werden. Verwenden Sie stattdessen Kontrollkästchen oder Optionsfelder für eine explizite Benutzerauswahl.

    **Falsch:**

    ![Screenshot der Bezeichnung: Verwenden Von -1 zum Deaktivieren der Zwischenspeicherung ](images/ctrl-text-boxes-image21.png)

    In diesem Beispiel hat der Wert -1 eine besondere Bedeutung.

    **Richtig:**

    ![Screenshot der Kontrollkästchenbezeichnung: Zwischenspeichern ](images/ctrl-text-boxes-image22.png)

    In diesem Beispiel wird die Option durch ein Kontrollkästchen explizit.

### <a name="password-and-pin-input"></a>Kennwort- und PIN-Eingabe

-   **Verwenden Sie immer das allgemeine Kennwortsteuerelement, anstatt ein eigenes zu erstellen.** Kennwörter und PINs erfordern eine besondere Behandlung, um sicher behandelt zu werden.

Weitere Richtlinien und Beispiele finden Sie unter [Balloons](ctrl-balloons.md).

### <a name="textual-output"></a>Textausgabe

-   **Erwägen Sie die Verwendung der Systemfarbe "Weißer Hintergrund" für großen, mehrzeiligen schreibgeschützten Text.** Ein weißer Hintergrund erleichtert das Lesen des Texts. Viele Text auf einem grauen Hintergrund raten vom Lesen ab.

Weitere Informationen zu Hintergrundfarben finden Sie unter [Schriftarten.](vis-fonts.md)

### <a name="data-output"></a>Datenausgabe

-   **Verwenden Sie keinen Rahmen für einzeilige, schreibgeschützte Textfelder.** Der Rahmen ist ein visueller Hinweis darauf, dass der Text bearbeitet werden kann.
-   **Deaktivieren Sie keine einzeiligen, schreibgeschützten Textfelder.** Dadurch wird verhindert, dass Benutzer den Text auswählen und in die Zwischenablage kopieren. Außerdem wird verhindert, dass Benutzer einen Bildlauf für die Daten durchführen, wenn sie die Größe ihrer Grenzen überschreiten.
-   **Legen Sie keine Tabstopps für einzeiliges, schreibgeschütztes Textfeld fest, es sei denn, der Benutzer muss wahrscheinlich scrollen oder den Text kopieren.**

## <a name="input-validation-and-error-handling"></a>Eingabeüberprüfung und Fehlerbehandlung

Da Textfelder in der Regel nicht darauf beschränkt sind, nur gültige Eingaben zu akzeptieren, müssen Sie möglicherweise die Eingabe überprüfen und Probleme behandeln. Überprüfen Sie die verschiedenen Arten von Eingabeproblemen wie folgt:

-   Wenn der Benutzer ein ungültiges Zeichen eingibt, ignorieren Sie das Zeichen, und zeigen Sie eine [Eingabeproblemsprechblase](ctrl-balloons.md) an, in der die gültigen Zeichen erläutert werden.

    ![Screenshot des Textfelds "Product Key"](images/ctrl-text-boxes-image23.png)

    In diesem Beispiel meldet eine Sprechblase ein falsches Eingabezeichen.

-   Wenn die Eingabedaten einen ungültigen Wert oder ein ungültiges Format aufweisen, zeigen Sie eine Eingabeproblemsprechblase an, wenn das Textfeld den Eingabefokus verliert.
-   Wenn die Eingabedaten mit anderen Steuerelementen im Fenster inkonsistent sind, geben Sie eine Fehlermeldung aus, wenn die gesamte Eingabe abgeschlossen ist, z. B. wenn Benutzer für ein modales Dialogfeld auf OK klicken.

**Löschen Sie ungültige Eingabedaten nur, wenn Benutzer Fehler nicht einfach beheben können.** Auf diese Weise können Benutzer Fehler korrigieren, ohne von vorn anfangen zu müssen. Beispielsweise sollten Sie falsche Kennwörter und PINs löschen, da Benutzer sie nicht einfach korrigieren können.

Weitere Richtlinien und Beispiele finden Sie unter [Fehlermeldungen](mess-error.md) und [Balloons.](ctrl-balloons.md)

## <a name="prompts"></a>Eingabeaufforderungen

Eine Eingabeaufforderung ist eine Bezeichnung oder eine kurze Anweisung, die als Standardwert in einem Textfeld platziert wird. Im Gegensatz zu statischem Text werden Eingabeaufforderungen nicht mehr auf dem Bildschirm angezeigt, sobald Benutzer etwas in das Textfeld eingeben oder den Eingabefokus erhalten.

![Screenshot des Eingabeaufforderungstextfelds mit Bezeichnung: Search ](images/ctrl-text-boxes-image24.png)

Eine typische Eingabeaufforderung.

Verwenden Sie eine Eingabeaufforderung, wenn:

-   Der Bildschirmbereich ist so premium, dass die Verwendung einer Bezeichnung oder Anweisung unerwünscht ist, z. B. auf einer Symbolleiste.
-   Die Eingabeaufforderung dient in erster Linie dazu, den Zweck des Textfelds auf kompakte Weise zu identifizieren. Es dürfen keine entscheidenden Informationen sein, die der Benutzer bei der Verwendung des Textfelds sehen muss.

Verwenden Sie keine Eingabeaufforderungen, um Benutzer nur anweisen, etwas einzugeben oder auf Schaltflächen zu klicken. Schreiben Sie z. B. keinen Eingabeaufforderungstext mit dem Text Geben Sie einen Dateinamen ein, und klicken Sie dann auf Senden.

Bei Verwendung von Eingabeaufforderungen:

-   Zeichnen Sie den Eingabeaufforderungstext in italischem Grau und den tatsächlichen Eingabetext in normalem Schwarz. Der Eingabeaufforderungstext darf nicht mit echtem Text verwechselt werden.
-   Halten Sie den Eingabeaufforderungstext kurz. Sie können Fragmente anstelle von vollständigen Sätzen verwenden.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Verwenden Sie keine endende Interpunktion oder Auslassungszeichen.
-   Der Eingabeaufforderungstext sollte nicht bearbeitbar sein und nicht mehr angezeigt werden, sobald Benutzer in das Textfeld klicken oder in das Textfeld klicken.
    -   **Ausnahme:** Wenn das Textfeld den Standardeingabefokus besitzt, wird die Eingabeaufforderung angezeigt, und sie wird ausgeblendet, sobald der Benutzer mit der Eingabe beginnt.
-   Der Eingabeaufforderungstext wird wiederhergestellt, wenn das Textfeld noch leer ist, wenn der Eingabefokus verloren geht.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstand

![Abbildung von ein- und zweizeilenbasierten Textfeldern ](images/ctrl-text-boxes-image25.png)

Empfohlene Größe und Abstand für Textfelder.

Die Breite eines Textfelds ist ein visueller Hinweis auf die erwartete Eingabegröße. Beim Anpassen der Größe von Textfeldern:

-   **Wählen Sie eine Breite aus, die für die längsten gültigen Daten geeignet ist.** In den meisten Fällen sollten Benutzer nicht die längste Zeichenfolge scrollen müssen, die sie eingeben oder anzeigen.
-   **Schließen Sie zusätzliche 30 Prozent** (bis zu 200 Prozent für kürzeren Text) für text (aber keine Zahlen) ein, die lokalisiert werden.
-   **Wenn die erwartete Eingabe keine bestimmte Größe hat, wählen Sie eine Breite aus, die mit den anderen Textfeldern oder Steuerelementen im Fenster konsistent ist.**
-   **Größe mehrzeilenübergreifender Textfelder, um eine ganzzahlige Anzahl von Textzeilen anzuzeigen.**

## <a name="labels"></a>Bezeichnungen

### <a name="text-box-labels"></a>Textfeldbezeichnungen

-   Alle Textfelder benötigen Bezeichnungen. Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, der mit einem Doppelpunkt endet und [statischen Text verwendet.](glossary.md)

    **Ausnahmen:**

    -   Textfelder mit Eingabeaufforderungen, in denen der Speicherplatz auf Premium-Ebene liegt.
    -   Bei der Bezeichnung sollte eine Gruppe von Textfeldern, die für **die formatierte** Dateneingabe verwendet werden, als einzelnes Textfeld behandelt werden.
    -   Wenn ein Textfeld einem Optionsfeld oder Kontrollkästchen untergeordnet ist und durch die Bezeichnung eingeführt wird, die mit einem Doppelpunkt endet, legen Sie keine zusätzliche Bezeichnung in das Textfeld ein.
    -   **Lassen Sie Steuerelementbezeichnungen weg, die die Hauptanweisung neu erstellen.** In diesem Fall übernimmt die main-Anweisung den Doppelpunkt (es sei denn, es ist eine Frage) und den Zugriffsschlüssel.

        **Annehmbar:**

        ![Screenshot des Textfelds mit erneuter Bezeichnung](images/ctrl-text-boxes-image26.png)

        In diesem Beispiel ist die Textfeldbezeichnung nur eine Neuformung der Main-Anweisung.

        **Besser:**

        ![Screenshot des Textfelds mit ausschließlicher Hauptanweisung ](images/ctrl-text-boxes-image27.png)

        In diesem Beispiel wird die redundante Bezeichnung entfernt, sodass die main-Anweisung den Doppelpunkt und den Zugriffsschlüssel übernimmt.

-   Weisen Sie einen eindeutigen Zugriffsschlüssel zu. Richtlinien für die Zuweisung von Zugriffsschlüsseln finden Sie unter [Tastatur](inter-keyboard.md).
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Positionieren Sie die Bezeichnung entweder links vom Textfeld oder über dem Textfeld, und richten Sie die Bezeichnung am linken Rand des Textfelds aus. Wenn sich die Bezeichnung links befindet, richten Sie den Bezeichnungstext vertikal am Textfeldtext aus.

    **Richtig:**

    ![Screenshot der linksbündig ausgerichteten Bezeichnung über dem Textfeld ](images/ctrl-text-boxes-image28.png)

    ![Screenshot der textbündigen Bezeichnung links vom Textfeld ](images/ctrl-text-boxes-image29.png)

    In diesen Beispielen wird die Bezeichnung oben am linken Rand des Textfelds ausgerichtet, und die Bezeichnung links wird am Text im Textfeld ausgerichtet.

    **Falsch:**

    ![Screenshot der textbündigen Bezeichnung über dem Textfeld ](images/ctrl-text-boxes-image30.png)

    ![Screenshot der oben ausgerichteten Bezeichnung links vom Textfeld ](images/ctrl-text-boxes-image31.png)

    In diesen falschen Beispielen wird die Bezeichnung oben am Text im Textfeld ausgerichtet, und die Bezeichnung links wird am oberen Ende des Textfelds ausgerichtet.

-   Sie können Einheiten (z. B. Sekunden oder Verbindungen) in Klammern nach der Bezeichnung angeben.
-   Wenn ein Textfeld eine beliebig kleine maximale Anzahl von Zeichen akzeptiert, können Sie die maximale Eingabe in der Bezeichnung eingeben. Die Breite des Textfelds sollte auch die maximale Größe vorschlagen.

    ![Screenshot des Textfelds "Kennwort" ](images/ctrl-text-boxes-image32.png)

    In diesem Beispiel gibt die Bezeichnung die maximale Anzahl von Zeichen an.

-   Machen Sie den Inhalt des Textfelds (oder seiner Einheitenbezeichnung) nicht als Teil eines Satzes, da dies nicht lokalisierbar ist.
-   Wenn das Textfeld zum Eingeben mehrerer Elemente verwendet werden kann, machen Sie deutlich, wie die Elemente in der Bezeichnung getrennt werden.

    ![Screenshot von bezeichnungstrennten Namen mit Semikolon ](images/ctrl-text-boxes-image33.png)

    In diesem Beispiel wird das Elementtrennzeichen in der Bezeichnung angegeben.

-   Richtlinien zum Angeben der erforderlichen Eingabe finden Sie unter Erforderliche Eingabe in [Dialogfeldern.](win-dialog-box.md)

### <a name="instruction-labels"></a>Anweisungsbezeichnungen

-   Wenn Sie Anweisungstext zu einem Textfeld hinzufügen müssen, fügen Sie ihn über der Bezeichnung hinzu. Verwenden Sie vollständige Sätze mit endender Interpunktion.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Zusätzliche Informationen, die hilfreich, aber nicht erforderlich sind, sollten kurz gehalten werden. Platzieren Sie diese Informationen entweder in Klammern zwischen der Bezeichnung und dem Doppelpunkt oder ohne Klammern unterhalb des Textfelds.

    ![Screenshot der hinzugefügten Informationen im Textfeld ](images/ctrl-text-boxes-image34.png)

    In diesem Beispiel werden zusätzliche Informationen unterhalb des Textfelds platziert.

### <a name="prompt-labels"></a>Eingabeaufforderungsbezeichnungen

-   Halten Sie den Eingabeaufforderungstext kurz. Sie können Fragmente anstelle von vollständigen Sätzen verwenden.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Verwenden Sie keine endenden Interpunktionen oder Auslassungszeichen.
-   Wenn die Eingabeaufforderung Benutzer zur Eingabe von Informationen anfing, auf die eine Schaltfläche neben dem Textfeld reagiert, platzieren Sie einfach die Schaltfläche neben dem Textfeld. Verwenden Sie nicht die Eingabeaufforderung, um Benutzer zum Klicken auf die Schaltfläche zu bewegen (schreiben Sie z. B. keinen Eingabeaufforderungstext mit dem Text Drag a file (Datei ziehen), und klicken Sie dann auf Send (Senden).

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Textfelder:

-   Verwenden Sie type, um auf Benutzerinteraktionen zu verweisen, für die Eingaben oder Eintippen erforderlich sind. Verwenden Sie andernfalls die Eingabetaste, wenn Benutzer Informationen auf andere Weise in das Textfeld eingeben können, z. B. indem Sie den Wert aus einer Liste auswählen oder die Schaltfläche Durchsuchen verwenden.
-   Verwenden Sie select, um auf einen Eintrag in einem schreibgeschützten Textfeld zu verweisen.
-   Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Unterschrift, und schließen Sie das Wortfeld ein. Schließen Sie den Unterstrich oder Doppelpunkt des Zugriffsschlüssels nicht ein. Verweisen Sie nicht auf ein Textfeld als Textfeld oder Feld.
-   Formatieren Sie die Bezeichnung nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

    Beispiel: Geben Sie Ihr Kennwort in das Feld **Kennwort** ein, und klicken Sie dann **auf OK.**

-   Wenn das Textfeld ein bestimmtes Format erfordert, dokumentieren Sie nur das am häufigsten verwendete zulässige Format. Ermöglichen Sie es Benutzern, alle anderen Formate selbst zu entdecken. Sie möchten flexibel mit Datenformaten arbeiten, dies sollte jedoch nicht zu einer komplexen Dokumentation führen.

    **Richtig:**

    Geben Sie die Seriennummer des Teils im Format 1234-56-7890 ein.

    **Falsch:**

    Geben Sie die Seriennummer des Teils in einem der folgenden Formate ein:

    1234567890

    1234-56-7890

    1234 56 7890

