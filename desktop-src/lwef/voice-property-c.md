---
title: Voice-Eigenschaft (Befehlsobjekt)
description: Erfahren Sie mehr über die Voice-Eigenschaft des Command-Objekts, die den Text für die Grammatik der Sprach-Engine zurückgibt oder legt, um diesen Befehl für das Zeichen zu finden.
ms.assetid: e393aa89-6fa7-4080-9faf-66faca83d561
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698b39bf2129ff30eae78a949cf6d694af3c356e4c994a1a192bc55ab29fa23c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245076"
---
# <a name="voice-property-command-object"></a>Voice-Eigenschaft (Befehlsobjekt)

\[Microsoft Agent ist ab Version Windows 7 veraltet und möglicherweise in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Text zurück, der an die Grammatik der Sprach-Engine (zur Erkennung) übergeben wird, um diesen [**Befehl**](/windows/desktop/lwef/the-command-object) für das Zeichen zu finden, oder legt diesen fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Befehle ("_*_name_*_"). Sprachzeichenfolge_ *  \[  =  \]



| Teil     | BESCHREIBUNG                                                                                                                                       |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Ein Zeichenfolgenausdruck, der den Wörtern oder Ausdrücken entspricht, die von der Sprach-Engine zum Erkennen dieses Befehls verwendet [**werden sollen.**](/windows/desktop/lwef/the-command-object) |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie diesen Parameter nicht angeben, wird [**die VoiceCaption**](voicecaption-property.md) für Ihr [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) nicht im Fenster Sprachbefehle angezeigt. Wenn Sie [](voice-property.md) einen Voice-Parameter, aber keine **VoiceCaption** (oder [**Caption)**](https://www.bing.com/search?q=**Caption**)angeben, wird der Befehl nicht im Fenster für Sprachbefehle angezeigt, aber er ist sprachgefehlt, wenn die Clientanwendung eingabeaktiv wird.

Der Zeichenfolgenausdruck kann eckige Klammern () enthalten, um optionale Wörter und vertikale Balkenzeichen ( ) anzugeben, \[ \] um alternative \| Zeichenfolgen anzugeben. Alternativen müssen in Klammern eingeschlossen werden. Beispielsweise weist "(hello there hi)" die Sprach-Engine \[ \] \| an, "hello", "hello there" oder "hi" für den Befehl zu akzeptieren. Denken Sie daran, die entsprechenden Leerzeichen zwischen dem Text in Klammern oder Klammern und dem Text, der nicht in Klammern oder Klammern enthalten ist, ein- und zu schließen.

Sie können den Sternoperator ( ) verwenden, um null oder mehr Instanzen der in der Gruppe enthaltenen Wörter anzugeben, oder den Plusoperator (+), um eine oder mehrere Instanzen \* anzugeben. Das folgende Beispiel führt zu einer Grammatik, die "try this", "please try this", "please try this" und "please try this" mit unbegrenzten Iterationen von "please" unterstützt:


```
   "please* try this"
```



Das folgende Grammatikformat schließt "try this" aus, da der +-Operator mindestens eine Instanz von "please" definiert:


```
   "please+ try this"
```



Die Wiederholungsoperatoren befolgen normale Rangfolgeregeln und gelten für das unmittelbar vorangehende Textelement. Die folgende Grammatik führt beispielsweise zu "New York" und "New York York", aber nicht zu "New York New York":


```
   "New York+"
```



Daher sollten Sie diese Operatoren in der Regel mit den Gruppierungszeichen verwenden. Die folgende Grammatik enthält beispielsweise sowohl "New York" als auch "New York New York":


```
   "(New York)+"
```



Wiederholungsoperatoren sind nützlich, wenn Sie eine Grammatik erstellen möchten, die eine wiederholte Sequenz enthält, z. B. eine Telefonnummer oder eine Spezifikation einer Liste von Elementen.


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



Obwohl die Operatoren auch mit dem optionalen Gruppierungszeichen in eckigen Klammern verwendet werden können, kann dies die Effizienz der Grammatikverarbeitung durch den -Agent verringern.

Sie können auch auslassungszeichen (...) verwenden, um die Worterkennung zu unterstützen, d. h., die Spracherkennungs-Engine soll Wörter ignorieren, die an dieser Position im Ausdruck (manchmal auch als Garbage *Words* bezeichnet) gesprochen werden. Daher erkennt die Sprach-Engine nur bestimmte Wörter in der Zeichenfolge, unabhängig davon, ob sie mit angrenzenden Wörtern oder Ausdrücken gesprochen wird. Wenn Sie diese Eigenschaft z. B. auf " \[ ... \] check mail \[ ... ", die Spracherkennungs-Engine gleicht Ausdrücke wie \] "Please check mail" oder "check mail please" mit diesem Befehl ab. Ellipsen können überall innerhalb einer Zeichenfolge verwendet werden. Seien Sie jedoch vorsichtig, wenn Sie diese Technik verwenden, da sie das Potenzial unerwünschter Übereinstimmungen erhöhen kann.

Wenn Sie die Wortgrammatik für Ihren Befehl definieren, schließen Sie mindestens ein Wort ein, das erforderlich ist. das heißt, geben Sie keine optionalen Wörter an. Stellen Sie außerdem sicher, dass das Wort nur aussetzbare Wörter und Buchstaben enthält. Für Zahlen ist es besser, das Wort zu sagen, anstatt eine mehrdeutige Darstellung zu verwenden. Beispielsweise ist "345" keine gute Grammatikform. Verwenden Sie auf ähnliche Weise anstelle von "IEEE" "I triple E". Sie sollten auch keine Interpunktion oder Symbole weglassen. Verwenden Sie z. B. anstelle von \# "1 $10 Pizza!" "the number one ten dollar pizza". Das Verwenden nicht aussprechbarer Zeichen oder Symbole für einen Befehl kann dazu führen, dass die Sprach-Engine die Grammatik für alle Befehle nicht kompiliert. Machen Sie schließlich Ihren Voice-Parameter so eindeutig wie möglich von anderen Sprachbefehlen, die Sie definieren. Je größer die Ähnlichkeit zwischen der Sprachgrammatik für Befehle ist, desto wahrscheinlicher wird die Sprach-Engine einen Erkennungsfehler machen. Sie können auch die Konfidenzergebnisse verwenden, um besser zwischen zwei Befehlen zu unterscheiden, die eine ähnliche oder ähnlich klingende Sprachgrammatik haben können.

Sie können ihre Grammatikwörter in Form von " Text  aussprache " enthalten,  wobei Text der angezeigte Text und Aussprache Text ist, der die Aussprache verdeutlicht.*\\* Beispielsweise würde die Grammatik "1st first" erkannt, wenn der Benutzer "first" sagt, aber das Command-Ereignis gibt den Text \\ "1st [](/windows/desktop/lwef/the-command-object) \\ first" zurück. Sie können auch IPA (International Phonetic Alphabet) verwenden, um eine Aussprache anzugeben, indem Sie die Aussprache mit einem Pfundzeichen ("") beginnen und dann den Text enthalten, der die \# IPA-Aussprache darstellt.

Für japanische Spracherkennungs-Engines können Sie grammatikalisch in der Form "*kana \\ kanji*" definieren, um die alternative Aussprache zu reduzieren und die Genauigkeit zu erhöhen. (Die Reihenfolge wird aus Gründen der Abwärtskompatibilität umgekehrt.) Dies ist besonders wichtig für die Aussprache von Eigennamen in Kanji. Sie können jedoch nur Kanji ohne Kana übergeben. In diesem Fall sollte die Engine auf alle akzeptablen Aussprachen für das Kanji lauschen. Sie können auch nur Kana übergeben.

Beachten Sie auch, dass Sie für Sprachen wie Japanisch, Chinesisch und Thailändisch, die keine Leerzeichen verwenden, um Wortumbrüche anzugeben, ein Unicode-Leerzeichen mit einer Breite von null (0x200B) einfügen, um logische Wortumbrüche anzugeben.

Mit Ausnahme von Fehlern, die die Gruppierungs- oder Wiederholungsformatierungszeichen verwenden, meldet der -Agent keine Fehler in der Grammatik, es sei denn, die Engine selbst meldet den Fehler. Wenn Sie Text in Der Grammatik übergeben, dass die Engine nicht kompiliert werden kann, die Engine jedoch nicht behandelt und als Fehler zurücksaget, kann der -Agent den Fehler nicht melden. Daher muss die Clientanwendung die Grammatik für die [**Voice-Eigenschaft sorgfältig**](voice-property.md) definieren.

> [!Note]  
> Die verfügbaren Grammatikfeatures hängen möglicherweise von der Spracherkennungs-Engine ab. Sie sollten sich an den Hersteller der Engine wenden, um zu ermitteln, welche Grammatikoptionen unterstützt werden. Verwenden Sie [**die SRModeID,**](srmodeid-property.md) um eine bestimmte Engine zu verwenden.

 

Der Vorgang dieser Eigenschaft hängt vom Zustand der Spracherkennungseigenschaft des Servers ab. Wenn die Spracherkennung beispielsweise deaktiviert oder nicht installiert ist, hat diese Eigenschaft keine Auswirkungen.

 

 
