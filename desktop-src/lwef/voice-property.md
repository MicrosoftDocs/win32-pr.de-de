---
title: Voice-Eigenschaft (Commands-Objekt)
description: Erfahren Sie mehr über die Voice-Eigenschaft des Commands-Objekts, die den Text zurückgibt oder legt, der an die Sprach-Engine-Grammatik (zur Erkennung) übergeben wird.
ms.assetid: 1feb5597-7971-4778-8221-2eb3a6e5e1ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af651532894537f58d35f860b781d3be42bfacf89b9be01d7caa26aa40102ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715810"
---
# <a name="voice-property-commands-object"></a>Voice-Eigenschaft (Commands-Objekt)

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Text zurück, der an die Sprach-Engine-Grammatik (zur Erkennung) übergeben wird, oder legt diesen fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Commands.Voice-Zeichenfolge_ *  \[  =  \]



| Teil     | Beschreibung                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------|
| *string* | Ein Zeichenfolgenausdruck, der den Wörtern oder Ausdrücken entspricht, die von der Sprach-Engine für die Erkennung dieses Befehls verwendet werden sollen. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie diesen Parameter nicht angeben, wird [**die VoiceCaption**](voicecaption-property.md) für Ihr [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) nicht im Fenster Sprachbefehle angezeigt.

Der von Ihnen angegebenen Zeichenfolgenausdruck kann eckige Klammern () enthalten, um optionale Wörter und vertikale Balkenzeichen ( ) anzugeben, \[ \] um alternative \| Zeichenfolgen anzugeben. Alternative müssen in Klammern eingeschlossen werden. Beispielsweise weist "(hello there hi)" die Sprach-Engine \[ \] \| an, "hello", "hello there" oder "hi" für den Befehl zu akzeptieren. Denken Sie daran, geeignete Leerzeichen zwischen dem Text in Klammern oder Klammern und dem Text, der nicht in Klammern oder Klammern enthalten ist, ein- und aus. Sie können den Sternoperator ( ) verwenden, um null oder mehr Instanzen der in der Gruppe enthaltenen Wörter anzugeben, oder den Plusoperator (+), um eine oder \* mehrere -Instanzen anzugeben. Das folgende Beispiel führt zu einer Grammatik, die "try this", "please try this", "please try this" und "please try this" mit unbegrenzten Iterationen von "please" unterstützt:


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

Sie können auch eine Auslassungszeichen (...) verwenden, um die Worterkennung zu unterstützen, d. h., die Spracherkennungs-Engine soll Wörter ignorieren, die an dieser Position im Ausdruck gesprochen werden (manchmal auch als Garbage *Words* bezeichnet).  Daher erkennt die Sprach-Engine nur bestimmte Wörter in der Zeichenfolge, unabhängig davon, ob sie mit angrenzenden Wörtern oder Ausdrücken gesprochen wird. Wenn Sie diese Eigenschaft z. B. auf " \[ ... \] check mail \[ ... ", die Spracherkennungs-Engine gleicht Ausdrücke wie \] "Please check mail" oder "check mail please" mit diesem Befehl ab. Ellipsen können überall innerhalb einer Zeichenfolge verwendet werden. Seien Sie jedoch vorsichtig, wenn Sie dieses Verfahren verwenden, da dies das Potenzial unerwünschter Übereinstimmungen erhöhen kann.

Wenn Sie die Wortgrammatik für Ihren Befehl definieren, schließen Sie mindestens ein Wort ein, das erforderlich ist. das heißt, geben Sie keine optionalen Wörter an. Stellen Sie außerdem sicher, dass das Wort nur aussetzbare Wörter und Buchstaben enthält. Bei Zahlen ist es besser, das Wort zu sagen, anstatt eine mehrdeutige Darstellung zu verwenden. Beispielsweise ist "345" keine gute Grammatikform. Verwenden Sie auf ähnliche Weise anstelle von "IEEE" "I triple E". Sie sollten auch keine Interpunktion oder Symbole weglassen. Verwenden Sie z. B. anstelle von \# "1 $10 Pizza!" "the number one ten dollar pizza". Das Verwenden nicht aussprechbarer Zeichen oder Symbole für einen Befehl kann dazu führen, dass die Sprach-Engine die Grammatik für alle Befehle nicht kompiliert. Machen Sie schließlich Ihren Voice-Parameter so eindeutig wie möglich von anderen Sprachbefehlen, die Sie definieren. Je größer die Ähnlichkeit zwischen der Sprachgrammatik für Befehle ist, desto wahrscheinlicher wird die Sprach-Engine einen Erkennungsfehler machen. Sie können auch die Konfidenzergebnisse verwenden, um besser zwischen zwei Befehlen zu unterscheiden, die eine ähnliche oder ähnlich klingende Sprachgrammatik haben können.

Sie können ihre Grammatikwörter in Form von " Text  aussprache " enthalten,  wobei Text der angezeigte Text und Aussprache Text ist, der die Aussprache verdeutlicht.*\\* Beispielsweise würde die Grammatik "1st first" erkannt, wenn der Benutzer "first" sagt, aber das Command-Ereignis gibt den Text \\ "1st [](command-event.md) \\ first" zurück. Sie können auch IPA (International Phonetic Alphabet) verwenden, um eine Aussprache anzugeben, indem Sie die Aussprache mit einem Pfundzeichen ("") beginnen und dann den Text enthalten, der die \# IPA-Aussprache darstellt.

Für japanische Spracherkennungs-Engines können Sie grammatikalisch in der Form "*kana \\ kanji*" definieren, um die alternative Aussprache zu reduzieren und die Genauigkeit zu erhöhen. (Die Reihenfolge wird aus Gründen der Abwärtskompatibilität umgekehrt.) Dies ist besonders wichtig für die Aussprache der richtigen Namen in Kanji. Sie können jedoch nur Kanji ohne Kana übergeben. In diesem Fall sollte die Engine auf alle akzeptablen Aussprachen für das Kanji lauschen. Sie können auch nur Kana übergeben.

Beachten Sie auch, dass Sie für Sprachen wie Japanisch, Chinesisch und Thailändisch, die keine Leerzeichen verwenden, um Wortumbrüche anzugeben, ein Unicode-Leerzeichen mit einer Breite von null (0x200B) einfügen, um logische Wortumbrüche anzugeben.

Mit Ausnahme von Fehlern, die die Gruppierungs- oder Wiederholungsformatierungszeichen verwenden, meldet der -Agent keine Fehler in der Grammatik, es sei denn, die Engine selbst meldet den Fehler. Wenn Sie Text in der Grammatik übergeben, dass die Engine nicht kompiliert werden kann, die Engine jedoch nicht behandelt und als Fehler zurücksaget, kann der -Agent den Fehler nicht melden. Daher muss die Clientanwendung die Grammatik für die **Voice-Eigenschaft sorgfältig** definieren.

> [!Note]  
> Die verfügbaren Grammatikfeatures hängen möglicherweise von der Spracherkennungs-Engine ab. Sie sollten sich an den Hersteller der Engine wenden, um zu ermitteln, welche Grammatikoptionen unterstützt werden. Verwenden Sie [**die SRModeID,**](srmodeid-property.md) um eine bestimmte Engine zu verwenden.

 

Der Vorgang dieser Eigenschaft hängt vom Zustand der Spracherkennungseigenschaft des Servers ab. Wenn die Spracherkennung beispielsweise deaktiviert oder nicht installiert ist, hat diese Eigenschaft keine Auswirkungen.

 

 
