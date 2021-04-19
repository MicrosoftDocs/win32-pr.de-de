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
# <a name="iagentcommandsetvoice"></a><span data-ttu-id="4eff2-103">Iagentcommand:: setvoice</span><span class="sxs-lookup"><span data-stu-id="4eff2-103">IAgentCommand::SetVoice</span></span>

<span data-ttu-id="4eff2-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="4eff2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

<span data-ttu-id="4eff2-105">Legt die [**Voice**](voice-property.md) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)fest.</span><span class="sxs-lookup"><span data-stu-id="4eff2-105">Sets the [**Voice**](voice-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="4eff2-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4eff2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4eff2-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszvoice*</span><span class="sxs-lookup"><span data-stu-id="4eff2-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="4eff2-108">Ein BSTR, der den Text für die [**Voice**](voice-property.md) -Eigenschaft eines [**Befehls**](/windows/desktop/lwef/the-command-object)angibt.</span><span class="sxs-lookup"><span data-stu-id="4eff2-108">A BSTR that specifies the text for the [**Voice**](voice-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="4eff2-109">Für einen [**Befehl**](/windows/desktop/lwef/the-command-object) muss die [**sprach**](voice-property.md) Eigenschaft und die [**aktivierte**](enabled-property.md) Eigenschaft auf sprach Zugriff festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="4eff2-109">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Voice**](voice-property.md) property and [**Enabled**](enabled-property.md) property set to be voice-accessible.</span></span> <span data-ttu-id="4eff2-110">Außerdem muss die [**voicecaption**](voicecaption-property.md) -Eigenschaft im **Fenster "Sprachbefehle**" angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4eff2-110">It also must have its [**VoiceCaption**](voicecaption-property.md) property set to appear in the **Voice Commands Window**.</span></span> <span data-ttu-id="4eff2-111">(Aus Gründen der Abwärtskompatibilität wird die [**Beschriftungs**](caption-property.md) Einstellung verwendet, wenn keine **voicecaption** vorhanden ist.)</span><span class="sxs-lookup"><span data-stu-id="4eff2-111">(For backward compatibility, if there is no **VoiceCaption**, the [**Caption**](caption-property.md) setting is used.)</span></span>

<span data-ttu-id="4eff2-112">Der von Ihnen bereitgestellte BSTR-Ausdruck kann eckige Klammer Zeichen ( \[ \] ) enthalten, um optionale Wörter und vertikale Balken Zeichen ( \| ) anzugeben, um alternative Zeichen folgen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4eff2-112">The BSTR expression you supply can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="4eff2-113">Alternativen müssen in Klammern eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="4eff2-113">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="4eff2-114">Beispiel: "(Hello \[ there \] \| HI)" weist die Sprach-Engine an, "Hello", "Hello There" oder "Hi" für den Befehl zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="4eff2-114">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="4eff2-115">Denken Sie daran, die entsprechenden Leerzeichen zwischen dem Text in Klammern oder Klammern und dem Text, der sich nicht in Klammern oder Klammern befindet, einzufügen.</span><span class="sxs-lookup"><span data-stu-id="4eff2-115">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span>

<span data-ttu-id="4eff2-116">Sie können den Stern ( \* )-Operator verwenden, um NULL oder mehr Instanzen der in der Gruppe enthaltenen Wörter anzugeben, oder den Plus (+)-Operator, um eine oder mehrere Instanzen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4eff2-116">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="4eff2-117">Der folgende Code führt beispielsweise zu einer Grammatik, die "try this", "try this" und "try this" (Bitte probieren Sie dies) mit unbegrenzten Iterationen "bitte" unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4eff2-117">For example, the following results in a grammar that supports "try this", "please try this", and "please please try this", with unlimited iterations of "please":</span></span>

``` syntax
   "please* try this"
```

<span data-ttu-id="4eff2-118">Das folgende Grammatik Format schließt "try this" aus, da der +-Operator mindestens eine Instanz von "bitte" definiert:</span><span class="sxs-lookup"><span data-stu-id="4eff2-118">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>

``` syntax
   "please+ try this"
```

<span data-ttu-id="4eff2-119">Die Wiederholungs Operatoren befolgen normale Rangfolge und gelten für das unmittelbar vorangehende Textelement.</span><span class="sxs-lookup"><span data-stu-id="4eff2-119">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="4eff2-120">Die folgende Grammatik ergibt beispielsweise "New York" und "New York York", aber nicht "New York New York":</span><span class="sxs-lookup"><span data-stu-id="4eff2-120">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>

``` syntax
   "New York+"
```

<span data-ttu-id="4eff2-121">Daher sollten Sie diese Operatoren in der Regel mit den Gruppierungs Zeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4eff2-121">Therefore, you will typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="4eff2-122">Die folgende Grammatik enthält z. b. "New York" und "New York New York":</span><span class="sxs-lookup"><span data-stu-id="4eff2-122">For example, the following grammar includes both "New York" and "New York New York":</span></span>

``` syntax
   "(New York)+"
```

<span data-ttu-id="4eff2-123">Wiederholungs Operatoren sind nützlich, wenn Sie eine Grammatik verfassen möchten, die eine wiederholte Sequenz, z. b. eine Telefonnummer oder eine Angabe einer Liste von Elementen, umfasst:</span><span class="sxs-lookup"><span data-stu-id="4eff2-123">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items:</span></span>

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

<span data-ttu-id="4eff2-124">Obwohl die Operatoren auch mit den eckigen Klammern (einem optionalen Gruppierungs Zeichen) verwendet werden können, kann dadurch die Effizienz der Agentverarbeitung der Grammatik verringert werden.</span><span class="sxs-lookup"><span data-stu-id="4eff2-124">Although the operators can also be used with the square brackets (an optional grouping character), doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="4eff2-125">Sie können auch ein Auslassungs Zeichen (...) verwenden, um die Erkennung von Wörtern zu unterstützen, d. h., das sprach Erkennungs Modul soll Wörter ignorieren, die an dieser Position in dem Ausdruck *gesprochen werden (* manchmal als " *Garbage* Words" bezeichnet)</span><span class="sxs-lookup"><span data-stu-id="4eff2-125">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="4eff2-126">Daher erkennt die Sprach-Engine nur bestimmte Wörter in der Zeichenfolge, unabhängig davon, wann Sie mit benachbarten Wörtern oder Ausdrücken gesprochen werden.</span><span class="sxs-lookup"><span data-stu-id="4eff2-126">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="4eff2-127">Wenn Sie diese Eigenschaft beispielsweise auf " \[ ... \] e-Mail-Überprüfung \[ ... \] "die Spracherkennungs-Engine entspricht den Ausdrücken wie" Bitte überprüfen Sie die e-Mail "oder" Mail überprüfen "auf diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="4eff2-127">For example, if you set this property to "\[...\] check mail \[...\]" the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="4eff2-128">Ellipsen können überall innerhalb einer Zeichenfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4eff2-128">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="4eff2-129">Seien Sie jedoch vorsichtig, wenn Sie diese Technik verwenden, da Spracheinstellungen mit Ellipsen möglicherweise das Potenzial unerwünschter Übereinstimmungen erhöhen.</span><span class="sxs-lookup"><span data-stu-id="4eff2-129">However, be careful using this technique, because voice settings with ellipses may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="4eff2-130">Wenn Sie die Wörter und die Grammatik für den Befehl definieren, stellen Sie immer sicher, dass Sie mindestens ein Wort einschließen, das erforderlich ist. Dies bedeutet, dass nur optionale Wörter bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4eff2-130">When defining the words and grammar for your command, always make sure that you include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="4eff2-131">Stellen Sie außerdem sicher, dass das Wort nur sprechbare Wörter und Buchstaben enthält.</span><span class="sxs-lookup"><span data-stu-id="4eff2-131">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="4eff2-132">Bei Zahlen ist es besser, das Wort anstelle der numerischen Darstellung zu buchstabieren.</span><span class="sxs-lookup"><span data-stu-id="4eff2-132">For numbers, it is better to spell out the word rather than using the numeric representation.</span></span> <span data-ttu-id="4eff2-133">Lassen Sie außerdem alle Interpunktions Zeichen oder Symbole aus.</span><span class="sxs-lookup"><span data-stu-id="4eff2-133">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="4eff2-134">Verwenden Sie beispielsweise anstelle von "The \# $1 10 Pizza!" die Zahl 1 10 Dollar Pizza.</span><span class="sxs-lookup"><span data-stu-id="4eff2-134">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="4eff2-135">Das einschließen nicht-sprechbarer Zeichen oder Symbole für einen Befehl kann dazu führen, dass die Sprach-Engine die Grammatik für alle Befehle nicht kompiliert.</span><span class="sxs-lookup"><span data-stu-id="4eff2-135">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="4eff2-136">Legen Sie schließlich ihren Voice-Parameter so eindeutig wie möglich von anderen Sprachbefehlen, die Sie definieren.</span><span class="sxs-lookup"><span data-stu-id="4eff2-136">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="4eff2-137">Umso größer die Ähnlichkeit zwischen der Sprachgrammatik für Befehle, desto wahrscheinlicher wird die Sprach-Engine einen Erkennungs Fehler.</span><span class="sxs-lookup"><span data-stu-id="4eff2-137">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="4eff2-138">Sie können auch die Vertrauens Ergebnisse verwenden, um zwischen zwei Befehlen besser zu unterscheiden, die eine ähnliche oder ähnlich klingende Sprachgrammatik aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="4eff2-138">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="4eff2-139">Wenn Sie die [**Voice**](voice-property.md) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object) festlegen, werden die Sprachdienste des-Agents automatisch aktiviert, sodass der Abhör Schlüssel und der lauschtip verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="4eff2-139">Setting the [**Voice**](voice-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object) automatically enables Agent's speech services, making the Listening key and Listening Tip available.</span></span> <span data-ttu-id="4eff2-140">Die sprach Erkennungs-Engine wird jedoch nicht geladen.</span><span class="sxs-lookup"><span data-stu-id="4eff2-140">However, it does not load the speech recognition engine.</span></span>

> [!Note]  
> <span data-ttu-id="4eff2-141">Welche Grammatik Features verfügbar sind, hängt möglicherweise von der Spracherkennungs-Engine ab.</span><span class="sxs-lookup"><span data-stu-id="4eff2-141">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="4eff2-142">Möglicherweise möchten Sie sich an den Hersteller der Engine wenden, um zu ermitteln, welche Grammatik Optionen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4eff2-142">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="4eff2-143">Verwenden Sie [**iagentcharakteriex:: srmodeid**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) , um eine Engine anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4eff2-143">Use [**IAgentCharacterEx::SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) to specify an engine.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="4eff2-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4eff2-144">See Also</span></span>

<span data-ttu-id="4eff2-145">[**Iagentcommand:: getvoice**](iagentcommand--getvoice.md), [**iagentcommand:: setCaption**](iagentcommand--setcaption.md), [**iagentcommand:: SetEnabled**](iagentcommand--setenabled.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="4eff2-145">[**IAgentCommand::GetVoice**](iagentcommand--getvoice.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 