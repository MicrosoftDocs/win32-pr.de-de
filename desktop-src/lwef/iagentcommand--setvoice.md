---
title: IAgentCommand SetVoice
description: IAgentCommand SetVoice
ms.assetid: bee06616-26bf-4e1e-89da-6765dd77fb02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45af753dea18e9fda7b613e3b800ac886d949eb6494fd969cd8b7ceb488dfc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477240"
---
# <a name="iagentcommandsetvoice"></a>IAgentCommand::SetVoice

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

Legt die [**Voice-Eigenschaft**](voice-property.md) für einen [**Befehl**](/windows/desktop/lwef/the-command-object)fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

Ein BSTR, der den Text für die [**Voice-Eigenschaft**](voice-property.md) eines [**Befehls**](/windows/desktop/lwef/the-command-object)angibt.

</dd> </dl>

Für einen [**Befehl**](/windows/desktop/lwef/the-command-object) müssen die [**Voice-Eigenschaft**](voice-property.md) und die [**Enabled-Eigenschaft**](enabled-property.md) so festgelegt sein, dass die Stimme zugänglich ist. Außerdem muss die [**VoiceCaption-Eigenschaft**](voicecaption-property.md) so festgelegt sein, dass sie im **Fenster "Sprachbefehle"** angezeigt wird. (Aus Gründen der Abwärtskompatibilität wird die [**Einstellung Caption**](caption-property.md) verwendet, wenn keine **VoiceCaption** vorhanden ist.)

Der von Ihnen angegebenen BSTR-Ausdruck kann eckige Klammern \[ \] () enthalten, um optionale Wörter und vertikale Balkenzeichen ( \| ) anzugeben, um alternative Zeichenfolgen anzugeben. Alternative Müssen in Klammern eingeschlossen werden. Beispielsweise weist "(hello \[ there \] \| hi)" die Sprach-Engine an, "hello", "hello there" oder "hi" für den Befehl zu akzeptieren. Denken Sie daran, geeignete Leerzeichen zwischen dem Text in Klammern oder Klammern und dem Text, der sich nicht in Klammern oder Klammern bezieht, einzuschließen.

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

Obwohl die Operatoren auch mit den eckigen Klammern (einem optionalen Gruppierungszeichen) verwendet werden können, kann dies die Effizienz der Verarbeitung der Grammatik durch den -Agent verringern.

Sie können auch auslassungspunkte (...) verwenden, um die *Worterkennung* zu unterstützen, d. h., die Spracherkennungs-Engine soll Wörter ignorieren, die an dieser Position im Ausdruck gesprochen werden (manchmal auch als *Garbage* Words bezeichnet). Daher erkennt die Sprach-Engine nur bestimmte Wörter in der Zeichenfolge, unabhängig davon, ob sie mit angrenzenden Wörtern oder Ausdrücken gesprochen werden. Wenn Sie diese Eigenschaft z. B. auf " \[ ... \] check mail \[ ... \] " Die Spracherkennungs-Engine stimmt mit Ausdrücken wie "please check mail" oder "check mail please" mit diesem Befehl überein. Ellipsen können an einer beliebigen Stelle innerhalb einer Zeichenfolge verwendet werden. Seien Sie jedoch vorsichtig mit dieser Technik, da Spracheinstellungen mit Ellipsen das Potenzial unerwünschter Übereinstimmungen erhöhen können.

Stellen Sie beim Definieren der Wörter und Grammatik für Ihren Befehl immer sicher, dass Sie mindestens ein erforderliches Wort einschließen. Vermeiden Sie also, nur optionale Wörter zu verwenden. Stellen Sie außerdem sicher, dass das Wort nur aussprechbare Wörter und Buchstaben enthält. Bei Zahlen ist es besser, das Wort zu schreiben, anstatt die numerische Darstellung zu verwenden. Achten Sie außerdem darauf, alle Interpunktionszeichen oder Symbole auszulassen. Verwenden Sie beispielsweise anstelle von \# "1 $10 pizza!" die "Zehn-Dollar-Pizza Nummer 1". Das Einschließen nicht aussprechbarer Zeichen oder Symbole für einen Befehl kann dazu führen, dass die Sprach-Engine die Grammatik für alle Befehle nicht kompiliert. Machen Sie schließlich Ihren Sprachparameter so unterschiedlich wie möglich von anderen von Ihnen definierten Sprachbefehlen. Je größer die Ähnlichkeit zwischen der Sprachgrammatik für Befehle ist, desto wahrscheinlicher wird die Sprach-Engine einen Erkennungsfehler machen. Sie können auch die Zuverlässigkeitsbewertungen verwenden, um besser zwischen zwei Befehlen zu unterscheiden, die eine ähnliche oder ähnlich klingende Sprachgrammatik aufweisen können.

Wenn Sie die [**Voice-Eigenschaft**](voice-property.md) für einen [**Befehl**](/windows/desktop/lwef/the-command-object) festlegen, werden die Sprachdienste des -Agents automatisch aktiviert, sodass die Überwachungsschlüssel und der Lauschende Tipp verfügbar sind. Die Spracherkennungs-Engine wird jedoch nicht geladen.

> [!Note]  
> Die verfügbaren Grammatikfeatures hängen möglicherweise von der Spracherkennungs-Engine ab. Möglicherweise sollten Sie beim Anbieter der Engine nachsehen, welche Grammatikoptionen unterstützt werden. Verwenden Sie [**IAgentCharacterEx::SRModeID,**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) um eine Engine anzugeben.

 

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommand::GetVoice**](iagentcommand--getvoice.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 