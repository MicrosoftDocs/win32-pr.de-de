---
title: Voice-Eigenschaft (Commands-Objekt)
description: Voice-Eigenschaft
ms.assetid: 1feb5597-7971-4778-8221-2eb3a6e5e1ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0207fb4fb6f09d460496b6886354bc17738def17
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517270"
---
# <a name="voice-property-commands-object"></a>Voice-Eigenschaft (Commands-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Text zurück, der an die Sprach-Engine-Grammatik (für die Erkennung) übermittelt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("**_Merkmal-ID_*_"). Commands. Voice_- *  \[  =  *Zeichenfolge*\]



| Teil     | BESCHREIBUNG                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------|
| *string* | Ein Zeichen folgen Ausdruck, der den Wörtern oder dem Ausdruck entspricht, der von der Sprach-Engine zum erkennen dieses Befehls verwendet werden soll. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie diesen Parameter nicht angeben, wird die [**voicecaption**](voicecaption-property.md) für das [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Objekt nicht im Fenster "Sprachbefehle" angezeigt.

Der von Ihnen bereitgestellte Zeichen folgen Ausdruck kann eckige Klammer Zeichen ( \[ \] ) enthalten, um optionale Wörter und vertikale Balken Zeichen ( \| ) anzugeben, um alternative Zeichen folgen anzugeben. Alternativen müssen in Klammern eingeschlossen werden. Beispiel: "(Hello \[ there \] \| HI)" weist die Sprach-Engine an, "Hello", "Hello There" oder "Hi" für den Befehl zu akzeptieren. Denken Sie daran, die entsprechenden Leerzeichen zwischen dem Text in Klammern oder Klammern und dem Text, der sich nicht in Klammern oder Klammern befindet, einzufügen. Sie können den Stern ( \* )-Operator verwenden, um NULL oder mehr Instanzen der in der Gruppe enthaltenen Wörter anzugeben, oder den Plus (+)-Operator, um eine oder mehrere Instanzen anzugeben. Der folgende Code führt z. b. zu einer Grammatik, die "try this", "try this", "try do this", mit unbegrenzten Iterationen von "bitte" unterstützt:


```
   "please* try this"
```



Das folgende Grammatik Format schließt "try this" aus, da der +-Operator mindestens eine Instanz von "bitte" definiert:


```
   "please+ try this"
```



Die Wiederholungs Operatoren befolgen normale Rangfolge und gelten für das unmittelbar vorangehende Textelement. Die folgende Grammatik ergibt beispielsweise "New York" und "New York York", aber nicht "New York New York":


```
   "New York+"
```



Daher sollten Sie diese Operatoren in der Regel mit den Gruppierungs Zeichen verwenden. Die folgende Grammatik enthält z. b. "New York" und "New York New York":


```
   "(New York)+"
```



Wiederholungs Operatoren sind nützlich, wenn Sie eine Grammatik verfassen möchten, die eine wiederholte Sequenz, z. b. eine Telefonnummer oder eine Angabe einer Liste von Elementen, enthält.


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



Obwohl die Operatoren auch mit dem optionalen Gruppierungs Zeichen für eckige Klammern verwendet werden können, kann dadurch die Effizienz der Agentverarbeitung der Grammatik verringert werden.

Sie können auch ein Auslassungs Zeichen (...) verwenden, um die Erkennung von Wörtern zu unterstützen, d. h., das sprach Erkennungs Modul soll Wörter ignorieren, die an dieser Position in dem Ausdruck *gesprochen werden (* manchmal als " *Garbage* Words" bezeichnet) Daher erkennt die Sprach-Engine nur bestimmte Wörter in der Zeichenfolge, unabhängig davon, wann Sie mit benachbarten Wörtern oder Ausdrücken gesprochen werden. Wenn Sie diese Eigenschaft beispielsweise auf " \[ ... \] e-Mail-Überprüfung \[ ... \] ", die Spracherkennungs-Engine entspricht den Ausdrücken wie" Bitte überprüfen Sie e-Mail "oder" e-Mail überprüfen "auf diesen Befehl. Ellipsen können überall innerhalb einer Zeichenfolge verwendet werden. Seien Sie jedoch vorsichtig, wenn Sie diese Technik verwenden, da dadurch möglicherweise unerwünschte Übereinstimmungen entstehen.

Wenn Sie die Wort Grammatik für Ihren Befehl definieren, schließen Sie mindestens ein Wort ein, das erforderlich ist. Dies bedeutet, dass nur optionale Wörter bereitgestellt werden. Stellen Sie außerdem sicher, dass das Wort nur sprechbare Wörter und Buchstaben enthält. Bei Zahlen ist es besser, das Wort zu buchstabieren, anstatt eine mehrdeutige Darstellung zu verwenden. Beispielsweise ist "345" keine gute Grammatik Form. Verwenden Sie auf ähnliche Weise anstelle von "IEEE" "I Triple E". Lassen Sie außerdem alle Interpunktions Zeichen oder Symbole aus. Verwenden Sie beispielsweise anstelle von "The \# $1 10 Pizza!" die Zahl 1 10 Dollar Pizza. Das einschließen nicht-sprechbarer Zeichen oder Symbole für einen Befehl kann dazu führen, dass die Sprach-Engine die Grammatik für alle Befehle nicht kompiliert. Legen Sie schließlich ihren Voice-Parameter so eindeutig wie möglich von anderen Sprachbefehlen, die Sie definieren. Umso größer die Ähnlichkeit zwischen der Sprachgrammatik für Befehle, desto wahrscheinlicher wird die Sprach-Engine einen Erkennungs Fehler. Sie können auch die Vertrauens Ergebnisse verwenden, um zwischen zwei Befehlen besser zu unterscheiden, die eine ähnliche oder ähnlich klingende Sprachgrammatik aufweisen können.

Sie können in die Grammatik Wörter in Form von *Text \\ Aussprache* einschließen, wobei *Text* der angezeigte Text und die *Aussprache* Text ist, der die Aussprache verdeutlicht. So würde z. b. die Grammatik "1st \\ First" erkannt werden, wenn der Benutzer "First" sagt, aber das [**Befehls**](command-event.md) Ereignis gibt den Text "1st \\ First" zurück. Sie können auch IPA (Internationales Phonetisches Alphabet) verwenden, um eine Aussprache anzugeben, indem Sie die Aussprache mit einem Nummern Zeichen (" \# ") beginnen und dann den Text einschließen, der die IPA-Aussprache darstellt.

Bei japanischen sprach Erkennungs Modulen können Sie die Grammatik in der Form "*Kana \\ Kanji*" definieren, um die alternativen Ausdrücke zu verringern und die Genauigkeit zu erhöhen. (Die Reihenfolge wird aus Gründen der Abwärtskompatibilität umgekehrt.) Dies ist besonders wichtig für die Aussprache der richtigen Namen in Kanji. Sie können jedoch nur Kanji ohne den Kana übergeben. in diesem Fall sollte die Engine alle zulässigen Ausdrücke für das Kanji überwachen. Sie können auch nur Kana übergeben.

Beachten Sie außerdem, dass bei Sprachen wie Japanisch, Chinesisch und Thailändisch, die keine Leerzeichen zum Angeben von Wort Umbrüchen verwenden, ein Unicode-Leerzeichen (0x200b) mit einer Breite von NULL Zeichen eingefügt werden, um logische Wort Umbrüche anzugeben.

Mit Ausnahme von Fehlern bei Verwendung der Formatierungszeichen für die Gruppierung oder Wiederholung meldet der-Agent keine Fehler in der Grammatik, es sei denn, die Engine selbst meldet den Fehler. Wenn Sie Text in der Grammatik übergeben, dass die Engine nicht kompiliert werden kann, die Engine jedoch nicht verarbeitet und als Fehler zurückgibt, kann der-Agent den Fehler nicht melden. Daher muss die Client Anwendung die Grammatik für die **Voice** -Eigenschaft sorgfältig definieren.

> [!Note]  
> Welche Grammatik Features verfügbar sind, hängt möglicherweise von der Spracherkennungs-Engine ab. Möglicherweise möchten Sie sich an den Hersteller der Engine wenden, um zu ermitteln, welche Grammatik Optionen unterstützt werden. Verwenden Sie [**srmodeid**](srmodeid-property.md) , um ein bestimmtes Modul zu verwenden.

 

Der Vorgang dieser Eigenschaft hängt vom Status der sprach Erkennungs Eigenschaft des Servers ab. Wenn z. b. die Spracherkennung deaktiviert oder nicht installiert ist, hat diese Eigenschaft keine Auswirkung.

 

 
