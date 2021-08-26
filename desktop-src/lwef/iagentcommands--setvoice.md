---
title: IAgentCommands SetVoice
description: IAgentCommands SetVoice
ms.assetid: dfb3b58a-7f24-4366-8f04-93a9e956fdc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02fb124b51a3be1796258fdcb8ffa31d8b81b59636027f3d99497b27cd2bd00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961900"
---
# <a name="iagentcommandssetvoice"></a>IAgentCommands::SetVoice

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // the Voice setting for Command collection
);
```

Legt die [**Sprachtexteigenschaft**](voice-property.md) für einen [**Befehl**](/windows/desktop/lwef/the-command-object)fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

Ein BSTR, der den Wert für die [**Sprachtexteigenschaft**](voice-property.md) einer [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) angibt.

</dd> </dl>

Für [**eine Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) muss die [**Eigenschaft Sprachtext**](voice-property.md) festgelegt sein, damit die Stimme zugänglich ist. Außerdem muss die [**VoiceCaption-**](voicecaption-property.md) oder [**Caption-Eigenschaft**](caption-property.md) auf festgelegt sein, damit sie im Sprachbefehlsfenster angezeigt wird, und die [**Visible-Eigenschaft**](visible-property.md) muss auf **True** festgelegt sein, damit sie im Popupmenü des Zeichens angezeigt wird.

Der von Ihnen angegebenen BSTR-Ausdruck kann eckige Klammern \[ \] () enthalten, um optionale Wörter und vertikale Balkenzeichen ( \| ) anzugeben, um alternative Zeichenfolgen anzugeben. Alternative Müssen in Klammern eingeschlossen werden. Beispielsweise weist "(hello \[ there \] \| hi)" die Sprach-Engine an, "hello", "hello there" oder "hi" für den Befehl zu akzeptieren. Denken Sie daran, zwischen Wörtern, die Sie in Klammern oder Klammern einschließen, sowie anderen Texten geeignete Leerzeichen einzuschließen. Denken Sie daran, geeignete Leerzeichen zwischen dem Text in Klammern oder Klammern und dem Text, der sich nicht in Klammern oder Klammern bezieht, einzuschließen.

Sie können den \* Sternoperator ( ) verwenden, um null oder mehr Instanzen der in der Gruppe enthaltenen Wörter anzugeben, oder den Plusoperator (+), um eine oder mehrere Instanzen anzugeben. Das folgende Ergebnis führt beispielsweise zu einer Grammatik, die "try this", "please try this" und "please please try this" mit unbegrenzten Iterationen von "please" unterstützt:

``` syntax
   "please* try this"
```

Das folgende Grammatikformat schließt "try this" aus, da der Operator + mindestens eine Instanz von "please" definiert:

``` syntax
   "please+ try this"
```

Die Wiederholungsoperatoren folgen normalen Rangfolgeregeln und gelten für das unmittelbar vorangehende Textelement. Die folgende Grammatik führt beispielsweise zu "New York" und "New York York", aber nicht zu "New York New York":

``` syntax
   "New York+"
```

Daher sollten Sie diese Operatoren in der Regel mit den Gruppierungszeichen verwenden. Die folgende Grammatik enthält beispielsweise sowohl "New York" als auch "New York New York":

``` syntax
   "(New York)+"
```

Wiederholungsoperatoren sind nützlich, wenn Sie eine Grammatik erstellen möchten, die eine wiederholte Sequenz enthält, z. B. eine Telefonnummer oder eine Spezifikation einer Liste von Elementen:

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

Obwohl die Operatoren auch mit eckigen Klammern (einem optionalen Gruppierungszeichen) verwendet werden können, kann dies die Effizienz der Verarbeitung der Grammatik durch den -Agent verringern.

Sie können auch auslassungspunkte (...) verwenden, um die *Worterkennung* zu unterstützen, d. h., die Spracherkennungs-Engine soll Wörter ignorieren, die an dieser Position im Ausdruck gesprochen werden (manchmal auch als *Garbage* Words bezeichnet). Wenn Sie Ellipsen verwenden, erkennt die Sprach-Engine nur bestimmte Wörter in der Zeichenfolge, unabhängig davon, ob sie mit angrenzenden Wörtern oder Ausdrücken gesprochen werden. Wenn Sie diese Eigenschaft z. B. auf " \[ ... \] check mail \[ ... \] " Die Spracherkennungs-Engine stimmt mit Ausdrücken wie "please check mail" oder "check mail please" mit diesem Befehl überein. Ellipsen können an einer beliebigen Stelle innerhalb einer Zeichenfolge verwendet werden. Seien Sie jedoch vorsichtig, wenn Sie diese Technik verwenden, da Spracheinstellungen mit Ellipsen das Potenzial unerwünschter Übereinstimmungen erhöhen können.

Wenn Sie die Wörter und die Grammatik für Ihren Befehl definieren, schließen Sie mindestens ein erforderliches Wort ein. Vermeiden Sie also, nur optionale Wörter zu verwenden. Stellen Sie außerdem sicher, dass das Wort nur aussprechbare Wörter und Buchstaben enthält. Bei Zahlen ist es besser, das Wort zu schreiben, anstatt eine mehrdeutige Darstellung zu verwenden. "345" ist beispielsweise keine gute Grammatikform. Verwenden Sie auf ähnliche Weise anstelle von "IEEE" "I triple E". Achten Sie außerdem darauf, alle Interpunktionszeichen oder Symbole auszulassen. Verwenden Sie beispielsweise anstelle von \# "1 $10 pizza!" die "Zehn-Dollar-Pizza Nummer 1". Das Einschließen nicht aussprechbarer Zeichen oder Symbole für einen Befehl kann dazu führen, dass die Sprach-Engine die Grammatik für alle Befehle nicht kompiliert. Machen Sie schließlich Ihren Sprachparameter so unterschiedlich wie möglich von anderen von Ihnen definierten Sprachbefehlen. Je größer die Ähnlichkeit zwischen der Sprachgrammatik für Befehle ist, desto wahrscheinlicher wird die Sprach-Engine einen Erkennungsfehler machen. Sie können auch die Zuverlässigkeitsbewertungen verwenden, um besser zwischen zwei Befehlen zu unterscheiden, die eine ähnliche oder ähnlich klingende Sprachgrammatik aufweisen können.

Sie können Grammatikwörter in form von *\\ "Textaussprechung"* einschließen, wobei "text" der angezeigte Text und "Aussprache" Text ist, der die Aussprache verdeutlicht. Beispielsweise würde die Grammatik "1st \\ first" erkannt werden, wenn der Benutzer "first" sagt, aber das [**Command-Ereignis**](/windows/desktop/lwef/the-command-object) gibt den Text "1st \\ first" zurück. Sie können auch IPA (Internationales phonetisches Alphabet) verwenden, um eine Aussprache anzugeben, indem Sie die Aussprache mit einem Nummernzeichen ("") und \# dann mit dem Text beginnen, der die IPA-Aussprache darstellt.

Bei japanischen Spracherkennungs-Engines können Sie grammatik in der Form *"kana \\ kanji"* definieren, um die alternative Aussprache zu reduzieren und die Genauigkeit zu erhöhen. (Die Reihenfolge wird aus Gründen der Abwärtskompatibilität umgekehrt.) Dies ist besonders wichtig für die Aussprache von Eigennamen in Kanji. Sie können jedoch einfach "kanji" ohne kana übergeben. In diesem Fall sollte die Engine auf alle zulässigen Aussprachen für das Kanji lauschen. Sie können auch nur Kana übergeben.

Mit Ausnahme von Fehlern bei der Verwendung der Gruppierungs- oder Wiederholungsformatierungszeichen meldet der Microsoft-Agent keine Fehler in Ihrer Grammatik, es sei denn, die Engine selbst meldet den Fehler. Wenn Sie Text in Ihrer Grammatik übergeben, der von der Engine nicht kompiliert werden kann, die Engine jedoch nicht verarbeitet und als Fehler zurückgegeben wird, kann der -Agent den Fehler nicht melden. Daher muss die Clientanwendung sorgfältig die Grammatik für die [**Voice-Eigenschaft**](voice-property.md) definieren.

> [!Note]  
> Die verfügbaren Grammatikfeatures hängen möglicherweise von der Spracherkennungs-Engine ab. Möglicherweise sollten Sie beim Anbieter der Engine nachsehen, welche Grammatikoptionen unterstützt werden. Verwenden Sie [**SRModeID,**](srmodeid-property.md) um eine bestimmte Engine zu verwenden.

 

Der Vorgang dieser Eigenschaft hängt vom Status des Spracherkennungsstatus des Microsoft-Agent-Servers ab. Wenn die Spracherkennung beispielsweise deaktiviert oder nicht installiert ist, hat diese Funktion keine sofortige Auswirkung. Wenn die Spracherkennung während einer Sitzung aktiviert ist, ist der Befehl jedoch zugänglich, wenn die Clientanwendung eingabeaktiv ist.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommands::GetVoice,**](iagentcommands--getvoice.md) [**IAgentCommands::SetCaption,**](iagentcommands--setcaption.md) [**IAgentCommands::SetVisible**](iagentcommands--setvisible.md)


 

 