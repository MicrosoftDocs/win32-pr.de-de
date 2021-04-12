---
title: Iagentcommands setvoice
description: Iagentcommands setvoice
ms.assetid: dfb3b58a-7f24-4366-8f04-93a9e956fdc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a8e29936dbca65ffded5f8a5e5ea5297b28362e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472861"
---
# <a name="iagentcommandssetvoice"></a>Iagentcommands:: setvoice

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // the Voice setting for Command collection
);
```

Legt die [**Voice**](voice-property.md) -Text-Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszvoice*
</dt> <dd>

Ein BSTR, der den Wert für die [**Voice**](voice-property.md) -Text-Eigenschaft einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angibt.

</dd> </dl>

Für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung muss die [**Voice**](voice-property.md) -Text-Eigenschaft auf sprach Zugriff festgelegt sein. Außerdem muss für die Eigenschaft [**voicecaption**](voicecaption-property.md) oder [**Caption**](caption-property.md) festgelegt sein, dass Sie im Fenster Sprachbefehle angezeigt wird und deren [**Visible**](visible-property.md) -Eigenschaft auf **true** festgelegt ist, damit Sie im Popupmenü des Zeichens angezeigt wird.

Der von Ihnen bereitgestellte BSTR-Ausdruck kann eckige Klammer Zeichen ( \[ \] ) enthalten, um optionale Wörter und vertikale Balken Zeichen ( \| ) anzugeben, um alternative Zeichen folgen anzugeben. Alternativen müssen in Klammern eingeschlossen werden. Beispiel: "(Hello \[ there \] \| HI)" weist die Sprach-Engine an, "Hello", "Hello There" oder "Hi" für den Befehl zu akzeptieren. Beachten Sie, dass Sie die entsprechenden Leerzeichen zwischen Wörtern einschließen, die Sie in eckige Klammern oder Klammern einschließen, sowie anderen Text. Denken Sie daran, die entsprechenden Leerzeichen zwischen dem Text in Klammern oder Klammern und dem Text, der sich nicht in Klammern oder Klammern befindet, einzufügen.

Sie können den Stern ( \* )-Operator verwenden, um NULL oder mehr Instanzen der in der Gruppe enthaltenen Wörter anzugeben, oder den Plus (+)-Operator, um eine oder mehrere Instanzen anzugeben. Der folgende Code führt beispielsweise zu einer Grammatik, die "try this", "try this" und "try this" (Bitte probieren Sie dies) mit unbegrenzten Iterationen "bitte" unterstützt:

``` syntax
   "please* try this"
```

Das folgende Grammatik Format schließt "try this" aus, da der +-Operator mindestens eine Instanz von "bitte" definiert:

``` syntax
   "please+ try this"
```

Die Wiederholungs Operatoren befolgen normale Rangfolge und gelten für das unmittelbar vorangehende Textelement. Die folgende Grammatik ergibt beispielsweise "New York" und "New York York", aber nicht "New York New York":

``` syntax
   "New York+"
```

Daher sollten Sie diese Operatoren in der Regel mit den Gruppierungs Zeichen verwenden. Die folgende Grammatik enthält z. b. "New York" und "New York New York":

``` syntax
   "(New York)+"
```

Wiederholungs Operatoren sind nützlich, wenn Sie eine Grammatik verfassen möchten, die eine wiederholte Sequenz, z. b. eine Telefonnummer oder eine Angabe einer Liste von Elementen, umfasst:

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

Obwohl die Operatoren auch mit eckigen Klammern (einem optionalen Gruppierungs Zeichen) verwendet werden können, kann dadurch die Effizienz der Agentverarbeitung der Grammatik verringert werden.

Sie können auch ein Auslassungs Zeichen (...) verwenden, um die Erkennung von Wörtern zu unterstützen, d. h., das sprach Erkennungs Modul soll Wörter ignorieren, die an dieser Position in dem Ausdruck *gesprochen werden (* manchmal als " *Garbage* Words" bezeichnet) Wenn Sie Ellipsen verwenden, erkennt die Sprach-Engine nur bestimmte Wörter in der Zeichenfolge, und zwar unabhängig davon, wann Sie mit benachbarten Wörtern oder Ausdrücken gesprochen werden. Wenn Sie diese Eigenschaft beispielsweise auf " \[ ... \] e-Mail-Überprüfung \[ ... \] "die Spracherkennungs-Engine entspricht den Ausdrücken wie" Bitte überprüfen Sie die e-Mail "oder" Mail überprüfen "auf diesen Befehl. Ellipsen können überall innerhalb einer Zeichenfolge verwendet werden. Seien Sie jedoch vorsichtig, wenn Sie diese Technik verwenden, da Spracheinstellungen mit Ellipsen möglicherweise das Potenzial unerwünschter Übereinstimmungen erhöhen.

Wenn Sie die Wörter und die Grammatik für den Befehl definieren, schließen Sie mindestens ein Wort ein, das erforderlich ist. Dies bedeutet, dass nur optionale Wörter bereitgestellt werden. Stellen Sie außerdem sicher, dass das Wort nur sprechbare Wörter und Buchstaben enthält. Bei Zahlen ist es besser, das Wort zu buchstabieren, anstatt eine mehrdeutige Darstellung zu verwenden. Beispielsweise ist "345" keine gute Grammatik Form. Verwenden Sie auf ähnliche Weise anstelle von "IEEE" "I Triple E". Lassen Sie außerdem alle Interpunktions Zeichen oder Symbole aus. Verwenden Sie beispielsweise anstelle von "The \# $1 10 Pizza!" die Zahl 1 10 Dollar Pizza. Das einschließen nicht-sprechbarer Zeichen oder Symbole für einen Befehl kann dazu führen, dass die Sprach-Engine die Grammatik für alle Befehle nicht kompiliert. Legen Sie schließlich ihren Voice-Parameter so eindeutig wie möglich von anderen Sprachbefehlen, die Sie definieren. Umso größer die Ähnlichkeit zwischen der Sprachgrammatik für Befehle, desto wahrscheinlicher wird die Sprach-Engine einen Erkennungs Fehler. Sie können auch die Vertrauens Ergebnisse verwenden, um zwischen zwei Befehlen besser zu unterscheiden, die eine ähnliche oder ähnlich klingende Sprachgrammatik aufweisen können.

Sie können in die Grammatik Wörter in Form von "*Text \\ Aussprache*" einschließen, wobei "Text" der Text ist, der angezeigt wird, und "Aussprache" Text ist, der die Aussprache verdeutlicht. So würde z. b. die Grammatik "1st \\ First" erkannt werden, wenn der Benutzer "First" sagt, aber das [**Befehls**](/windows/desktop/lwef/the-command-object) Ereignis gibt den Text "1st \\ First" zurück. Sie können auch IPA (Internationales Phonetisches Alphabet) verwenden, um eine Aussprache anzugeben, indem Sie die Aussprache mit einem Nummern Zeichen (" \# ") beginnen, dann den Text, der die IPA-Aussprache darstellt.

Bei japanischen sprach Erkennungs Modulen können Sie die Grammatik im Format "*Kana \\ Kanji*" definieren, um die alternativen Ausdrücke zu verringern und die Genauigkeit zu erhöhen. (Die Reihenfolge wird aus Gründen der Abwärtskompatibilität umgekehrt.) Dies ist besonders wichtig für die Aussprache der richtigen Namen in Kanji. Sie können jedoch einfach "Kanji" ohne Kana übergeben. in diesem Fall sollte die Engine auf alle zulässigen Ausdrücke für das Kanji lauschen. Sie können auch nur Kana übergeben.

Mit Ausnahme von Fehlern, die die Formatierungs-oder Wiederholungs Formatierungszeichen verwenden, meldet der Microsoft-Agent keine Fehler in der Grammatik, es sei denn, die Engine selbst meldet den Fehler. Wenn Sie Text in der Grammatik übergeben, dass die Engine nicht kompiliert werden kann, die Engine jedoch nicht verarbeitet und als Fehler zurückgibt, kann der-Agent den Fehler nicht melden. Daher muss die Client Anwendung vorsichtig sein, um die Grammatik für die [**Voice**](voice-property.md) -Eigenschaft zu definieren.

> [!Note]  
> Welche Grammatik Features verfügbar sind, hängt möglicherweise von der Spracherkennungs-Engine ab. Möglicherweise möchten Sie sich an den Hersteller der Engine wenden, um zu ermitteln, welche Grammatik Optionen unterstützt werden. Verwenden Sie [**srmodeid**](srmodeid-property.md) , um ein bestimmtes Modul zu verwenden.

 

Der Vorgang dieser Eigenschaft hängt vom Status des sprach Erkennungs Zustands des Microsoft-Agent-Servers ab. Wenn z. b. die Spracherkennung deaktiviert oder nicht installiert ist, hat diese Funktion keine unmittelbare Auswirkung. Wenn die Spracherkennung während einer Sitzung aktiviert ist, wird der Befehl jedoch zugänglich, wenn die Client Anwendung aktiv ist.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommands:: getvoice**](iagentcommands--getvoice.md), [**iagentcommands:: setCaption**](iagentcommands--setcaption.md), [**iagentcommands:: setVisible**](iagentcommands--setvisible.md)


 

 