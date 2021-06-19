---
title: Voice-Eigenschaft (Command-Objekt)
description: Erfahren Sie mehr über die Voice-Eigenschaft des Command-Objekts, das den Text für die Sprach-Engine-Grammatik zurückgibt oder festlegt, um diesen Befehl für das Zeichen zu finden.
ms.assetid: e393aa89-6fa7-4080-9faf-66faca83d561
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee7981de076fb3c7d8f796a8cc7d1177f96495c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396145"
---
# <a name="voice-property-command-object"></a>Voice-Eigenschaft (Command-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Text zurück, der zur Erkennung an die Sprach-Engine-Grammatik übergeben wird, um diesen [**Befehl**](/windows/desktop/lwef/the-command-object) für das Zeichen abzugleichen, oder legt diesen fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Befehle ("_*_Name_*_")._ *  \[  =  *Sprachzeichenfolge*\]



| Teil     | Beschreibung                                                                                                                                       |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Ein Zeichenfolgenausdruck, der den Wörtern oder Ausdrücken entspricht, die von der Sprach-Engine zum Erkennen dieses [**Befehls**](/windows/desktop/lwef/the-command-object)verwendet werden sollen. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie diesen Parameter nicht angeben, wird das [**VoiceCaption-Objekt**](voicecaption-property.md) für Ihr [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) nicht im Fenster "Sprachbefehle" angezeigt. Wenn Sie [](voice-property.md) einen Voice-Parameter, aber keine VoiceCaption (oder [**Beschriftung)**](https://www.bing.com/search?q=**Caption**)angeben, wird der Befehl nicht im Fenster "Sprachbefehle" angezeigt, aber er ist sprachfähig, wenn die Clientanwendung eingabeaktiv wird. 

Der Zeichenfolgenausdruck kann eckige Klammern \[ \] () enthalten, um optionale Wörter und vertikale Balkenzeichen ( \| ) anzugeben, um alternative Zeichenfolgen anzugeben. Alternative Müssen in Klammern eingeschlossen werden. Beispielsweise weist "(hello \[ there \] \| hi)" die Sprach-Engine an, "hello", "hello there" oder "hi" für den Befehl zu akzeptieren. Denken Sie daran, geeignete Leerzeichen zwischen dem Text in Klammern oder Klammern und dem Text einzuschließen, der nicht in Klammern oder Klammern gesetzt ist.

Sie können den \* Sternoperator ( ) verwenden, um null oder mehr Instanzen der in der Gruppe enthaltenen Wörter anzugeben, oder den Plusoperator (+), um eine oder mehrere Instanzen anzugeben. Die folgenden Ergebnisse führen beispielsweise zu einer Grammatik, die "try this", "please try this", "please please try this" mit unbegrenzten Iterationen von "please" unterstützt:


```
   "please* try this"
```



Das folgende Grammatikformat schließt "try this" aus, da der Operator + mindestens eine Instanz von "please" definiert:


```
   "please+ try this"
```



Die Wiederholungsoperatoren folgen normalen Rangfolgeregeln und gelten für das unmittelbar vorangehende Textelement. Die folgende Grammatik führt beispielsweise zu "New York" und "New York York", aber nicht zu "New York New York":


```
   "New York+"
```



Daher sollten Sie diese Operatoren in der Regel mit den Gruppierungszeichen verwenden. Die folgende Grammatik enthält beispielsweise sowohl "New York" als auch "New York New York":


```
   "(New York)+"
```



Wiederholungsoperatoren sind nützlich, wenn Sie eine Grammatik erstellen möchten, die eine wiederholte Sequenz enthält, z. B. eine Telefonnummer oder die Angabe einer Liste von Elementen.


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



Obwohl die Operatoren auch mit dem optionalen Gruppierungszeichen in eckigen Klammern verwendet werden können, kann dies die Effizienz der Verarbeitung der Grammatik durch den -Agent beeinträchtigen.

Sie können auch eine Auslassungspunkte (...) verwenden, um die *Worterkennung* zu unterstützen, d. h., die Spracherkennungs-Engine soll Wörter ignorieren, die an dieser Position im Ausdruck gesprochen werden (manchmal auch als *"Garbage* Words" bezeichnet). Daher erkennt die Sprach-Engine nur bestimmte Wörter in der Zeichenfolge, unabhängig davon, ob sie mit angrenzenden Wörtern oder Ausdrücken gesprochen werden. Wenn Sie diese Eigenschaft beispielsweise auf " \[ ... \] check mail \[ ... \] ", die Spracherkennungs-Engine stimmt mit Ausdrücken wie "please check mail" oder "check mail please" mit diesem Befehl überein. Ellipsen können an einer beliebigen Stelle innerhalb einer Zeichenfolge verwendet werden. Seien Sie jedoch vorsichtig mit dieser Technik, da sie das Potenzial unerwünschter Übereinstimmungen erhöhen kann.

Wenn Sie die Wortgrammatik für Ihren Befehl definieren, schließen Sie mindestens ein erforderliches Wort ein. Vermeiden Sie also, nur optionale Wörter zu verwenden. Stellen Sie außerdem sicher, dass das Wort nur aussprechbare Wörter und Buchstaben enthält. Bei Zahlen ist es besser, das Wort zu schreiben, anstatt eine mehrdeutige Darstellung zu verwenden. "345" ist beispielsweise keine gute Grammatikform. Verwenden Sie auf ähnliche Weise anstelle von "IEEE" "I triple E". Achten Sie außerdem darauf, alle Interpunktionszeichen oder Symbole auszulassen. Verwenden Sie beispielsweise anstelle von \# "1 $10 pizza!" die "Zehn-Dollar-Pizza Nummer 1". Das Einschließen nicht aussprechbarer Zeichen oder Symbole für einen Befehl kann dazu führen, dass die Sprach-Engine die Grammatik für alle Befehle nicht kompiliert. Machen Sie schließlich Ihren Sprachparameter so unterschiedlich wie möglich von anderen von Ihnen definierten Sprachbefehlen. Je größer die Ähnlichkeit zwischen der Sprachgrammatik für Befehle ist, desto wahrscheinlicher wird die Sprach-Engine einen Erkennungsfehler machen. Sie können auch die Zuverlässigkeitsbewertungen verwenden, um besser zwischen zwei Befehlen zu unterscheiden, die eine ähnliche oder ähnlich klingende Sprachgrammatik aufweisen können.

Sie können Grammatikwörter in form von *\\ "Textaussprechung"* einschließen, wobei *Text* der angezeigte Text und *Aussprache* Text ist, der die Aussprache verdeutlicht. Beispielsweise würde die Grammatik "1st \\ first" erkannt werden, wenn der Benutzer "first" sagt, aber das [**Command-Ereignis**](/windows/desktop/lwef/the-command-object) gibt den Text "1st \\ first" zurück. Sie können auch IPA (Internationales phonetisches Alphabet) verwenden, um eine Aussprache anzugeben, indem Sie die Aussprache mit einem Nummernzeichen ("") beginnen \# und dann den Text einschließen, der die IPA-Aussprache darstellt.

Bei japanischen Spracherkennungs-Engines können Sie grammatik in der Form *"kana \\ kanji"* definieren, um die alternative Aussprache zu reduzieren und die Genauigkeit zu erhöhen. (Die Reihenfolge wird aus Gründen der Abwärtskompatibilität umgekehrt.) Dies ist besonders wichtig für die Aussprache von Eigennamen in Kanji. Sie können Kanji jedoch einfach ohne kana übergeben. In diesem Fall sollte die Engine auf alle zulässigen Aussprachen für das Kanji lauschen. Sie können auch nur Kana übergeben.

Beachten Sie auch, dass für Sprachen wie Japanisch, Chinesisch und Thailändisch, die keine Leerzeichen zum Festlegen von Wortumbrüchen verwenden, ein Unicode-Leerzeichen mit einer Breite von null (0x200B) einfügen, um logische Wortumbrüche anzugeben.

Mit Ausnahme von Fehlern bei der Verwendung der Gruppierungs- oder Wiederholungsformatierungszeichen meldet der -Agent keine Fehler in Ihrer Grammatik, es sei denn, die Engine selbst meldet den Fehler. Wenn Sie Text in Ihrer Grammatik übergeben, der von der Engine nicht kompiliert werden kann, die Engine jedoch nicht behandelt und als Fehler zurückgegeben wird, kann der -Agent den Fehler nicht melden. Daher muss die Clientanwendung die Grammatik für die [**Voice-Eigenschaft**](voice-property.md) sorgfältig definieren.

> [!Note]  
> Die verfügbaren Grammatikfeatures hängen möglicherweise von der Spracherkennungs-Engine ab. Möglicherweise sollten Sie beim Anbieter der Engine nachsehen, welche Grammatikoptionen unterstützt werden. Verwenden Sie [**SRModeID,**](srmodeid-property.md) um eine bestimmte Engine zu verwenden.

 

Der Vorgang dieser Eigenschaft hängt vom Zustand der Spracherkennungseigenschaft des Servers ab. Wenn die Spracherkennung beispielsweise deaktiviert oder nicht installiert ist, hat diese Eigenschaft keine Auswirkungen.

 

 
