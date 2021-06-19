---
title: Voice-Eigenschaft (Commands-Objekt)
description: Erfahren Sie mehr über die Voice-Eigenschaft des Commands-Objekts, das den Text zurückgibt oder legt, der an die Sprach-Engine-Grammatik (zur Erkennung) übergeben wird.
ms.assetid: 1feb5597-7971-4778-8221-2eb3a6e5e1ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7403075d8ec0b2d16c66130fc9534edf4fc391df
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396155"
---
# <a name="voice-property-commands-object"></a><span data-ttu-id="b2088-103">Voice-Eigenschaft (Commands-Objekt)</span><span class="sxs-lookup"><span data-stu-id="b2088-103">Voice Property (Commands Object)</span></span>

<span data-ttu-id="b2088-104">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="b2088-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b2088-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b2088-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b2088-106">Gibt den Text zurück, der an die Sprach-Engine-Grammatik (zur Erkennung) übergeben wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="b2088-106">Returns or sets the text that is passed to the speech engine grammar (for recognition).</span></span>

</dd> <dt>

<span data-ttu-id="b2088-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="b2088-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b2088-108">*agent\***. Zeichen ("**_CharacterID_*_"). Commands.Voice-Zeichenfolge_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="b2088-108">*agent\***.Characters ("**_CharacterID_*_").Commands.Voice_\* \[ = *string*\]</span></span>



| <span data-ttu-id="b2088-109">Teil</span><span class="sxs-lookup"><span data-stu-id="b2088-109">Part</span></span>     | <span data-ttu-id="b2088-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2088-110">Description</span></span>                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2088-111">*string*</span><span class="sxs-lookup"><span data-stu-id="b2088-111">*string*</span></span> | <span data-ttu-id="b2088-112">Ein Zeichenfolgenausdruck, der den Wörtern oder Ausdrücken entspricht, die von der Sprach-Engine für die Erkennung dieses Befehls verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b2088-112">A string expression corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2088-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2088-113">Remarks</span></span>

<span data-ttu-id="b2088-114">Wenn Sie diesen Parameter nicht angeben, wird [**die VoiceCaption**](voicecaption-property.md) für Ihr [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) nicht im Fenster Sprachbefehle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2088-114">If you do not supply this parameter, the [**VoiceCaption**](voicecaption-property.md) for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object will not appear in the Voice Commands Window.</span></span>

<span data-ttu-id="b2088-115">Der von Ihnen angegebenen Zeichenfolgenausdruck kann eckige Klammern () enthalten, um optionale Wörter und vertikale Balkenzeichen ( ) anzugeben, \[ \] um alternative \| Zeichenfolgen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b2088-115">The string expression you supply can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="b2088-116">Alternative müssen in Klammern eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="b2088-116">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="b2088-117">Beispielsweise weist "(hello there hi)" die Sprach-Engine \[ \] \| an, "hello", "hello there" oder "hi" für den Befehl zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="b2088-117">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="b2088-118">Denken Sie daran, die entsprechenden Leerzeichen zwischen dem Text in Klammern oder Klammern und dem Text, der nicht in Klammern oder Klammern enthalten ist, ein- und zu schließen.</span><span class="sxs-lookup"><span data-stu-id="b2088-118">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span> <span data-ttu-id="b2088-119">Sie können den Sternoperator ( ) verwenden, um null oder mehr Instanzen der in der Gruppe enthaltenen Wörter anzugeben, oder den Plusoperator (+), um eine oder mehrere Instanzen \* anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b2088-119">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="b2088-120">Das folgende Beispiel führt zu einer Grammatik, die "try this", "please try this", "please try this" und "please try this" mit unbegrenzten Iterationen von "please" unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b2088-120">For example, the following results in a grammar that supports "try this", "please try this", "please please try this", with unlimited iterations of "please":</span></span>


```
   "please* try this"
```



<span data-ttu-id="b2088-121">Das folgende Grammatikformat schließt "try this" aus, da der +-Operator mindestens eine Instanz von "please" definiert:</span><span class="sxs-lookup"><span data-stu-id="b2088-121">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>


```
   "please+ try this"
```



<span data-ttu-id="b2088-122">Die Wiederholungsoperatoren befolgen normale Rangfolgeregeln und gelten für das unmittelbar vorangehende Textelement.</span><span class="sxs-lookup"><span data-stu-id="b2088-122">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="b2088-123">Die folgende Grammatik führt beispielsweise zu "New York" und "New York York", aber nicht zu "New York New York":</span><span class="sxs-lookup"><span data-stu-id="b2088-123">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>


```
   "New York+"
```



<span data-ttu-id="b2088-124">Daher sollten Sie diese Operatoren in der Regel mit den Gruppierungszeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2088-124">Therefore, you typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="b2088-125">Die folgende Grammatik enthält beispielsweise sowohl "New York" als auch "New York New York":</span><span class="sxs-lookup"><span data-stu-id="b2088-125">For example, the following grammar includes both "New York" and "New York New York":</span></span>


```
   "(New York)+"
```



<span data-ttu-id="b2088-126">Wiederholungsoperatoren sind nützlich, wenn Sie eine Grammatik erstellen möchten, die eine wiederholte Sequenz enthält, z. B. eine Telefonnummer oder eine Spezifikation einer Liste von Elementen.</span><span class="sxs-lookup"><span data-stu-id="b2088-126">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items.</span></span>


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



<span data-ttu-id="b2088-127">Obwohl die Operatoren auch mit dem optionalen Gruppierungszeichen in eckigen Klammern verwendet werden können, kann dies die Effizienz der Grammatikverarbeitung durch den -Agent verringern.</span><span class="sxs-lookup"><span data-stu-id="b2088-127">Although the operators can also be used with the optional square-brackets grouping character, doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="b2088-128">Sie können auch auslassungszeichen (...) verwenden, um die Worterkennung zu unterstützen, d. h., die Spracherkennungs-Engine soll Wörter ignorieren, die an dieser Position im Ausdruck (manchmal auch als Garbage *Words* bezeichnet) gesprochen werden.</span><span class="sxs-lookup"><span data-stu-id="b2088-128">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="b2088-129">Daher erkennt die Sprach-Engine nur bestimmte Wörter in der Zeichenfolge, unabhängig davon, ob sie mit angrenzenden Wörtern oder Ausdrücken gesprochen wird.</span><span class="sxs-lookup"><span data-stu-id="b2088-129">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="b2088-130">Wenn Sie diese Eigenschaft z. B. auf " \[ ... \] check mail \[ ... ", die Spracherkennungs-Engine gleicht Ausdrücke wie \] "Please check mail" oder "check mail please" mit diesem Befehl ab.</span><span class="sxs-lookup"><span data-stu-id="b2088-130">For example, if you set this property to "\[...\] check mail \[...\]", the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="b2088-131">Ellipsen können überall innerhalb einer Zeichenfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2088-131">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="b2088-132">Seien Sie jedoch vorsichtig, wenn Sie diese Technik verwenden, da sie das Potenzial unerwünschter Übereinstimmungen erhöhen kann.</span><span class="sxs-lookup"><span data-stu-id="b2088-132">However, be careful using this technique as it may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="b2088-133">Wenn Sie die Wortgrammatik für Ihren Befehl definieren, schließen Sie mindestens ein Wort ein, das erforderlich ist. das heißt, geben Sie keine optionalen Wörter an.</span><span class="sxs-lookup"><span data-stu-id="b2088-133">When defining the word grammar for your command, include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="b2088-134">Stellen Sie außerdem sicher, dass das Wort nur aussetzbare Wörter und Buchstaben enthält.</span><span class="sxs-lookup"><span data-stu-id="b2088-134">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="b2088-135">Bei Zahlen ist es besser, das Wort zu sagen, anstatt eine mehrdeutige Darstellung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2088-135">For numbers, it is better to spell out the word rather than using an ambiguous representation.</span></span> <span data-ttu-id="b2088-136">Beispielsweise ist "345" keine gute Grammatikform.</span><span class="sxs-lookup"><span data-stu-id="b2088-136">For example, "345" is not a good grammar form.</span></span> <span data-ttu-id="b2088-137">Verwenden Sie auf ähnliche Weise anstelle von "IEEE" "I triple E".</span><span class="sxs-lookup"><span data-stu-id="b2088-137">Similarly, instead of "IEEE", use "I triple E".</span></span> <span data-ttu-id="b2088-138">Sie sollten auch keine Interpunktion oder Symbole weglassen.</span><span class="sxs-lookup"><span data-stu-id="b2088-138">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="b2088-139">Verwenden Sie z. B. anstelle von \# "1 $10 Pizza!" "the number one ten dollar pizza".</span><span class="sxs-lookup"><span data-stu-id="b2088-139">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="b2088-140">Das Verwenden nicht aussprechbarer Zeichen oder Symbole für einen Befehl kann dazu führen, dass die Sprach-Engine die Grammatik für alle Befehle nicht kompiliert.</span><span class="sxs-lookup"><span data-stu-id="b2088-140">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="b2088-141">Machen Sie schließlich Ihren Voice-Parameter so eindeutig wie möglich von anderen Sprachbefehlen, die Sie definieren.</span><span class="sxs-lookup"><span data-stu-id="b2088-141">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="b2088-142">Je größer die Ähnlichkeit zwischen der Sprachgrammatik für Befehle ist, desto wahrscheinlicher wird die Sprach-Engine einen Erkennungsfehler machen.</span><span class="sxs-lookup"><span data-stu-id="b2088-142">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="b2088-143">Sie können auch die Konfidenzergebnisse verwenden, um besser zwischen zwei Befehlen zu unterscheiden, die eine ähnliche oder ähnlich klingende Sprachgrammatik haben können.</span><span class="sxs-lookup"><span data-stu-id="b2088-143">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="b2088-144">Sie können ihre Grammatikwörter in Form von " Text  aussprache " enthalten,  wobei Text der angezeigte Text und Aussprache Text ist, der die Aussprache verdeutlicht.*\\*</span><span class="sxs-lookup"><span data-stu-id="b2088-144">You can include in your grammar words in the form of "*text\\pronunciation*", where *text* is the text displayed and *pronunciation* is text that clarifies the pronunciation.</span></span> <span data-ttu-id="b2088-145">Beispielsweise würde die Grammatik "1st first" erkannt, wenn der Benutzer "first" sagt, aber das Command-Ereignis gibt den Text \\ "1st [](command-event.md) \\ first" zurück.</span><span class="sxs-lookup"><span data-stu-id="b2088-145">For example, the grammar, "1st\\first", would be recognized when the user says "first", but the [**Command**](command-event.md) event will return the text, "1st\\first".</span></span> <span data-ttu-id="b2088-146">Sie können auch IPA (International Phonetic Alphabet) verwenden, um eine Aussprache anzugeben, indem Sie die Aussprache mit einem Pfundzeichen ("") beginnen und dann den Text enthalten, der die \# IPA-Aussprache darstellt.</span><span class="sxs-lookup"><span data-stu-id="b2088-146">You can also use IPA (International Phonetic Alphabet) to specify a pronunciation by beginning the pronunciation with a pound sign character ("\#"), then include the text representing the IPA pronunciation.</span></span>

<span data-ttu-id="b2088-147">Für japanische Spracherkennungs-Engines können Sie grammatikalisch in der Form "*kana \\ kanji*" definieren, um die alternative Aussprache zu reduzieren und die Genauigkeit zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="b2088-147">For Japanese speech recognition engines, you can define grammar in the form "*kana\\kanji*", reducing the alternative pronunciations and increasing the accuracy.</span></span> <span data-ttu-id="b2088-148">(Die Reihenfolge wird aus Gründen der Abwärtskompatibilität umgekehrt.) Dies ist besonders wichtig für die Aussprache von Eigennamen in Kanji.</span><span class="sxs-lookup"><span data-stu-id="b2088-148">(The ordering is reversed for backward compatibility.) This is particularly important for the pronunciation of proper names in Kanji.</span></span> <span data-ttu-id="b2088-149">Sie können jedoch nur Kanji ohne Kana übergeben. In diesem Fall sollte die Engine auf alle akzeptablen Aussprachen für das Kanji lauschen.</span><span class="sxs-lookup"><span data-stu-id="b2088-149">However, you can just pass in Kanji without the Kana, in which case the engine should listen for all acceptable pronunciations for the Kanji.</span></span> <span data-ttu-id="b2088-150">Sie können auch nur Kana übergeben.</span><span class="sxs-lookup"><span data-stu-id="b2088-150">You can also pass in just Kana.</span></span>

<span data-ttu-id="b2088-151">Beachten Sie außerdem, dass Sie für Sprachen wie Japanisch, Chinesisch und Thailändisch, die keine Leerzeichen verwenden, um Wortumbrüche anzugeben, ein Unicode-Leerzeichen mit einer Breite von null (0x200B) einfügen, um logische Wortumbrüche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b2088-151">Also note that for languages such as Japanese, Chinese, and Thai, that do not use space characters to designate word breaks, insert a Unicode zero-width space character (0x200B) to indicate logical word breaks.</span></span>

<span data-ttu-id="b2088-152">Mit Ausnahme von Fehlern, die die Gruppierungs- oder Wiederholungsformatierungszeichen verwenden, meldet der -Agent keine Fehler in der Grammatik, es sei denn, die Engine selbst meldet den Fehler.</span><span class="sxs-lookup"><span data-stu-id="b2088-152">Except for errors using the grouping or repetition formatting characters, Agent will not report errors in your grammar, unless the engine itself reports the error.</span></span> <span data-ttu-id="b2088-153">Wenn Sie Text in Der Grammatik übergeben, dass die Engine nicht kompiliert werden kann, die Engine jedoch nicht behandelt und als Fehler zurücksaget, kann der -Agent den Fehler nicht melden.</span><span class="sxs-lookup"><span data-stu-id="b2088-153">If you pass text in your grammar that the engine fails to compile, but the engine does not handle and return as an error, Agent cannot report the error.</span></span> <span data-ttu-id="b2088-154">Daher muss die Clientanwendung die Grammatik für die **Voice-Eigenschaft sorgfältig** definieren.</span><span class="sxs-lookup"><span data-stu-id="b2088-154">Therefore, the client application must be carefully define grammar for the **Voice** property.</span></span>

> [!Note]  
> <span data-ttu-id="b2088-155">Die verfügbaren Grammatikfeatures hängen möglicherweise von der Spracherkennungs-Engine ab.</span><span class="sxs-lookup"><span data-stu-id="b2088-155">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="b2088-156">Sie sollten sich an den Hersteller der Engine wenden, um zu ermitteln, welche Grammatikoptionen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b2088-156">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="b2088-157">Verwenden Sie [**die SRModeID,**](srmodeid-property.md) um eine bestimmte Engine zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2088-157">Use the [**SRModeID**](srmodeid-property.md) to use a specific engine.</span></span>

 

<span data-ttu-id="b2088-158">Der Vorgang dieser Eigenschaft hängt vom Zustand der Spracherkennungseigenschaft des Servers ab.</span><span class="sxs-lookup"><span data-stu-id="b2088-158">The operation of this property depends on the state of the server's speech recognition property.</span></span> <span data-ttu-id="b2088-159">Wenn die Spracherkennung beispielsweise deaktiviert oder nicht installiert ist, hat diese Eigenschaft keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="b2088-159">For example, if speech recognition is disabled or not installed, this property has no effect.</span></span>

 

 
