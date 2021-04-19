---
title: Iagentcommand setvoice
description: Iagentcommand setvoice
ms.assetid: bee06616-26bf-4e1e-89da-6765dd77fb02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36bed7e86cb93824fc26c770c1d01336077fda39
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338657"
---
# <a name="iagentcommandsetvoice"></a>Iagentcommand:: setvoice

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

Legt die [**Voice**](voice-property.md) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszvoice*
</dt> <dd>

Ein BSTR, der den Text für die [**Voice**](voice-property.md) -Eigenschaft eines [**Befehls**](/windows/desktop/lwef/the-command-object)angibt.

</dd> </dl>

Für einen [**Befehl**](/windows/desktop/lwef/the-command-object) muss die [**sprach**](voice-property.md) Eigenschaft und die [**aktivierte**](enabled-property.md) Eigenschaft auf sprach Zugriff festgelegt sein. Außerdem muss die [**voicecaption**](voicecaption-property.md) -Eigenschaft im **Fenster "Sprachbefehle**" angezeigt werden. (Aus Gründen der Abwärtskompatibilität wird die [**Beschriftungs**](caption-property.md) Einstellung verwendet, wenn keine **voicecaption** vorhanden ist.)

Der von Ihnen bereitgestellte BSTR-Ausdruck kann eckige Klammer Zeichen ( \[ \] ) enthalten, um optionale Wörter und vertikale Balken Zeichen ( \| ) anzugeben, um alternative Zeichen folgen anzugeben. Alternativen müssen in Klammern eingeschlossen werden. Beispiel: "(Hello \[ there \] \| HI)" weist die Sprach-Engine an, "Hello", "Hello There" oder "Hi" für den Befehl zu akzeptieren. Denken Sie daran, die entsprechenden Leerzeichen zwischen dem Text in Klammern oder Klammern und dem Text, der sich nicht in Klammern oder Klammern befindet, einzufügen.

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

Obwohl die Operatoren auch mit den eckigen Klammern (einem optionalen Gruppierungs Zeichen) verwendet werden können, kann dadurch die Effizienz der Agentverarbeitung der Grammatik verringert werden.

Sie können auch ein Auslassungs Zeichen (...) verwenden, um die Erkennung von Wörtern zu unterstützen, d. h., das sprach Erkennungs Modul soll Wörter ignorieren, die an dieser Position in dem Ausdruck *gesprochen werden (* manchmal als " *Garbage* Words" bezeichnet) Daher erkennt die Sprach-Engine nur bestimmte Wörter in der Zeichenfolge, unabhängig davon, wann Sie mit benachbarten Wörtern oder Ausdrücken gesprochen werden. Wenn Sie diese Eigenschaft beispielsweise auf " \[ ... \] e-Mail-Überprüfung \[ ... \] "die Spracherkennungs-Engine entspricht den Ausdrücken wie" Bitte überprüfen Sie die e-Mail "oder" Mail überprüfen "auf diesen Befehl. Ellipsen können überall innerhalb einer Zeichenfolge verwendet werden. Seien Sie jedoch vorsichtig, wenn Sie diese Technik verwenden, da Spracheinstellungen mit Ellipsen möglicherweise das Potenzial unerwünschter Übereinstimmungen erhöhen.

Wenn Sie die Wörter und die Grammatik für den Befehl definieren, stellen Sie immer sicher, dass Sie mindestens ein Wort einschließen, das erforderlich ist. Dies bedeutet, dass nur optionale Wörter bereitgestellt werden. Stellen Sie außerdem sicher, dass das Wort nur sprechbare Wörter und Buchstaben enthält. Bei Zahlen ist es besser, das Wort anstelle der numerischen Darstellung zu buchstabieren. Lassen Sie außerdem alle Interpunktions Zeichen oder Symbole aus. Verwenden Sie beispielsweise anstelle von "The \# $1 10 Pizza!" die Zahl 1 10 Dollar Pizza. Das einschließen nicht-sprechbarer Zeichen oder Symbole für einen Befehl kann dazu führen, dass die Sprach-Engine die Grammatik für alle Befehle nicht kompiliert. Legen Sie schließlich ihren Voice-Parameter so eindeutig wie möglich von anderen Sprachbefehlen, die Sie definieren. Umso größer die Ähnlichkeit zwischen der Sprachgrammatik für Befehle, desto wahrscheinlicher wird die Sprach-Engine einen Erkennungs Fehler. Sie können auch die Vertrauens Ergebnisse verwenden, um zwischen zwei Befehlen besser zu unterscheiden, die eine ähnliche oder ähnlich klingende Sprachgrammatik aufweisen können.

Wenn Sie die [**Voice**](voice-property.md) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object) festlegen, werden die Sprachdienste des-Agents automatisch aktiviert, sodass der Abhör Schlüssel und der lauschtip verfügbar sind Die sprach Erkennungs-Engine wird jedoch nicht geladen.

> [!Note]  
> Welche Grammatik Features verfügbar sind, hängt möglicherweise von der Spracherkennungs-Engine ab. Möglicherweise möchten Sie sich an den Hersteller der Engine wenden, um zu ermitteln, welche Grammatik Optionen unterstützt werden. Verwenden Sie [**iagentcharakteriex:: srmodeid**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) , um eine Engine anzugeben.

 

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommand:: getvoice**](iagentcommand--getvoice.md), [**iagentcommand:: setCaption**](iagentcommand--setcaption.md), [**iagentcommand:: SetEnabled**](iagentcommand--setenabled.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)


 

 