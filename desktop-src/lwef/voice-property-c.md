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
# <a name="voice-property-command-object"></a><span data-ttu-id="6c6c4-103">Voice-Eigenschaft (Command-Objekt)</span><span class="sxs-lookup"><span data-stu-id="6c6c4-103">Voice Property (Command Object)</span></span>

<span data-ttu-id="6c6c4-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="6c6c4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6c6c4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c6c4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6c6c4-106">Gibt den Text zurück, der zur Erkennung an die Sprach-Engine-Grammatik übergeben wird, um diesen [**Befehl**](/windows/desktop/lwef/the-command-object) für das Zeichen abzugleichen, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-106">Returns or sets the text that is passed to the speech engine grammar (for recognition) for matching this [**Command**](/windows/desktop/lwef/the-command-object) for the character.</span></span>

</dd> <dt>

<span data-ttu-id="6c6c4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="6c6c4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6c6c4-108">*agent\***. Zeichen ("**_CharacterID_*_"). Befehle ("_*_Name_*_")._ \*  \[  =  *Sprachzeichenfolge*\]</span><span class="sxs-lookup"><span data-stu-id="6c6c4-108">*agent\***.Characters ("**_CharacterID_*_").Commands ("_*_name_*_").Voice_\* \[ = *string*\]</span></span>



| <span data-ttu-id="6c6c4-109">Teil</span><span class="sxs-lookup"><span data-stu-id="6c6c4-109">Part</span></span>     | <span data-ttu-id="6c6c4-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c6c4-110">Description</span></span>                                                                                                                                       |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6c4-111">*string*</span><span class="sxs-lookup"><span data-stu-id="6c6c4-111">*string*</span></span> | <span data-ttu-id="6c6c4-112">Ein Zeichenfolgenausdruck, der den Wörtern oder Ausdrücken entspricht, die von der Sprach-Engine zum Erkennen dieses [**Befehls**](/windows/desktop/lwef/the-command-object)verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-112">A string expression corresponding to the words or phrase to be used by the speech engine for recognizing this [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c6c4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c6c4-113">Remarks</span></span>

<span data-ttu-id="6c6c4-114">Wenn Sie diesen Parameter nicht angeben, wird das [**VoiceCaption-Objekt**](voicecaption-property.md) für Ihr [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) nicht im Fenster "Sprachbefehle" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-114">If you do not supply this parameter, the [**VoiceCaption**](voicecaption-property.md) for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object will not appear in the Voice Commands Window.</span></span> <span data-ttu-id="6c6c4-115">Wenn Sie [](voice-property.md) einen Voice-Parameter, aber keine VoiceCaption (oder [**Beschriftung)**](https://www.bing.com/search?q=**Caption**)angeben, wird der Befehl nicht im Fenster "Sprachbefehle" angezeigt, aber er ist sprachfähig, wenn die Clientanwendung eingabeaktiv wird. </span><span class="sxs-lookup"><span data-stu-id="6c6c4-115">If you specify a [**Voice**](voice-property.md) parameter but not a **VoiceCaption** (or [**Caption**](https://www.bing.com/search?q=**Caption**)), the command will not appear in the Voice Commands Window, but it will be voice-accessible when the client application becomes input-active.</span></span>

<span data-ttu-id="6c6c4-116">Der Zeichenfolgenausdruck kann eckige Klammern \[ \] () enthalten, um optionale Wörter und vertikale Balkenzeichen ( \| ) anzugeben, um alternative Zeichenfolgen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-116">Your string expression can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="6c6c4-117">Alternative Müssen in Klammern eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-117">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="6c6c4-118">Beispielsweise weist "(hello \[ there \] \| hi)" die Sprach-Engine an, "hello", "hello there" oder "hi" für den Befehl zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-118">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="6c6c4-119">Denken Sie daran, geeignete Leerzeichen zwischen dem Text in Klammern oder Klammern und dem Text einzuschließen, der nicht in Klammern oder Klammern gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-119">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span>

<span data-ttu-id="6c6c4-120">Sie können den \* Sternoperator ( ) verwenden, um null oder mehr Instanzen der in der Gruppe enthaltenen Wörter anzugeben, oder den Plusoperator (+), um eine oder mehrere Instanzen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-120">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="6c6c4-121">Die folgenden Ergebnisse führen beispielsweise zu einer Grammatik, die "try this", "please try this", "please please try this" mit unbegrenzten Iterationen von "please" unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6c6c4-121">For example, the following results in a grammar that supports "try this", "please try this", "please please try this", with unlimited iterations of "please":</span></span>


```
   "please* try this"
```



<span data-ttu-id="6c6c4-122">Das folgende Grammatikformat schließt "try this" aus, da der Operator + mindestens eine Instanz von "please" definiert:</span><span class="sxs-lookup"><span data-stu-id="6c6c4-122">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>


```
   "please+ try this"
```



<span data-ttu-id="6c6c4-123">Die Wiederholungsoperatoren folgen normalen Rangfolgeregeln und gelten für das unmittelbar vorangehende Textelement.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-123">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="6c6c4-124">Die folgende Grammatik führt beispielsweise zu "New York" und "New York York", aber nicht zu "New York New York":</span><span class="sxs-lookup"><span data-stu-id="6c6c4-124">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>


```
   "New York+"
```



<span data-ttu-id="6c6c4-125">Daher sollten Sie diese Operatoren in der Regel mit den Gruppierungszeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-125">Therefore, you typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="6c6c4-126">Die folgende Grammatik enthält beispielsweise sowohl "New York" als auch "New York New York":</span><span class="sxs-lookup"><span data-stu-id="6c6c4-126">For example, the following grammar includes both "New York" and "New York New York":</span></span>


```
   "(New York)+"
```



<span data-ttu-id="6c6c4-127">Wiederholungsoperatoren sind nützlich, wenn Sie eine Grammatik erstellen möchten, die eine wiederholte Sequenz enthält, z. B. eine Telefonnummer oder die Angabe einer Liste von Elementen.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-127">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items.</span></span>


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



<span data-ttu-id="6c6c4-128">Obwohl die Operatoren auch mit dem optionalen Gruppierungszeichen in eckigen Klammern verwendet werden können, kann dies die Effizienz der Verarbeitung der Grammatik durch den -Agent beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-128">Although the operators can also be used with the optional square-brackets grouping character, doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="6c6c4-129">Sie können auch eine Auslassungspunkte (...) verwenden, um die *Worterkennung* zu unterstützen, d. h., die Spracherkennungs-Engine soll Wörter ignorieren, die an dieser Position im Ausdruck gesprochen werden (manchmal auch als *"Garbage* Words" bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="6c6c4-129">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="6c6c4-130">Daher erkennt die Sprach-Engine nur bestimmte Wörter in der Zeichenfolge, unabhängig davon, ob sie mit angrenzenden Wörtern oder Ausdrücken gesprochen werden.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-130">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="6c6c4-131">Wenn Sie diese Eigenschaft beispielsweise auf " \[ ... \] check mail \[ ... \] ", die Spracherkennungs-Engine stimmt mit Ausdrücken wie "please check mail" oder "check mail please" mit diesem Befehl überein.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-131">For example, if you set this property to "\[...\] check mail \[...\]", the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="6c6c4-132">Ellipsen können an einer beliebigen Stelle innerhalb einer Zeichenfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-132">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="6c6c4-133">Seien Sie jedoch vorsichtig mit dieser Technik, da sie das Potenzial unerwünschter Übereinstimmungen erhöhen kann.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-133">However, be careful using this technique as it may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="6c6c4-134">Wenn Sie die Wortgrammatik für Ihren Befehl definieren, schließen Sie mindestens ein erforderliches Wort ein. Vermeiden Sie also, nur optionale Wörter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-134">When defining the word grammar for your command, include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="6c6c4-135">Stellen Sie außerdem sicher, dass das Wort nur aussprechbare Wörter und Buchstaben enthält.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-135">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="6c6c4-136">Bei Zahlen ist es besser, das Wort zu schreiben, anstatt eine mehrdeutige Darstellung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-136">For numbers, it is better to spell out the word rather than using an ambiguous representation.</span></span> <span data-ttu-id="6c6c4-137">"345" ist beispielsweise keine gute Grammatikform.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-137">For example, "345" is not a good grammar form.</span></span> <span data-ttu-id="6c6c4-138">Verwenden Sie auf ähnliche Weise anstelle von "IEEE" "I triple E".</span><span class="sxs-lookup"><span data-stu-id="6c6c4-138">Similarly, instead of "IEEE", use "I triple E".</span></span> <span data-ttu-id="6c6c4-139">Achten Sie außerdem darauf, alle Interpunktionszeichen oder Symbole auszulassen.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-139">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="6c6c4-140">Verwenden Sie beispielsweise anstelle von \# "1 $10 pizza!" die "Zehn-Dollar-Pizza Nummer 1".</span><span class="sxs-lookup"><span data-stu-id="6c6c4-140">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="6c6c4-141">Das Einschließen nicht aussprechbarer Zeichen oder Symbole für einen Befehl kann dazu führen, dass die Sprach-Engine die Grammatik für alle Befehle nicht kompiliert.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-141">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="6c6c4-142">Machen Sie schließlich Ihren Sprachparameter so unterschiedlich wie möglich von anderen von Ihnen definierten Sprachbefehlen.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-142">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="6c6c4-143">Je größer die Ähnlichkeit zwischen der Sprachgrammatik für Befehle ist, desto wahrscheinlicher wird die Sprach-Engine einen Erkennungsfehler machen.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-143">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="6c6c4-144">Sie können auch die Zuverlässigkeitsbewertungen verwenden, um besser zwischen zwei Befehlen zu unterscheiden, die eine ähnliche oder ähnlich klingende Sprachgrammatik aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-144">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="6c6c4-145">Sie können Grammatikwörter in form von *\\ "Textaussprechung"* einschließen, wobei *Text* der angezeigte Text und *Aussprache* Text ist, der die Aussprache verdeutlicht.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-145">You can include in your grammar words in the form of "*text\\pronunciation*", where *text* is the text displayed and *pronunciation* is text that clarifies the pronunciation.</span></span> <span data-ttu-id="6c6c4-146">Beispielsweise würde die Grammatik "1st \\ first" erkannt werden, wenn der Benutzer "first" sagt, aber das [**Command-Ereignis**](/windows/desktop/lwef/the-command-object) gibt den Text "1st \\ first" zurück.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-146">For example, the grammar, "1st\\first", would be recognized when the user says "first", but the [**Command**](/windows/desktop/lwef/the-command-object) event will return the text, "1st\\first".</span></span> <span data-ttu-id="6c6c4-147">Sie können auch IPA (Internationales phonetisches Alphabet) verwenden, um eine Aussprache anzugeben, indem Sie die Aussprache mit einem Nummernzeichen ("") beginnen \# und dann den Text einschließen, der die IPA-Aussprache darstellt.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-147">You can also use IPA (International Phonetic Alphabet) to specify a pronunciation by beginning the pronunciation with a pound sign character ("\#"), then include the text representing the IPA pronunciation.</span></span>

<span data-ttu-id="6c6c4-148">Bei japanischen Spracherkennungs-Engines können Sie grammatik in der Form *"kana \\ kanji"* definieren, um die alternative Aussprache zu reduzieren und die Genauigkeit zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-148">For Japanese speech recognition engines, you can define grammar in the form "*kana\\kanji*", reducing the alternative pronunciations and increasing the accuracy.</span></span> <span data-ttu-id="6c6c4-149">(Die Reihenfolge wird aus Gründen der Abwärtskompatibilität umgekehrt.) Dies ist besonders wichtig für die Aussprache von Eigennamen in Kanji.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-149">(The ordering is reversed for backward compatibility.) This is particularly important for the pronunciation of proper names in Kanji.</span></span> <span data-ttu-id="6c6c4-150">Sie können Kanji jedoch einfach ohne kana übergeben. In diesem Fall sollte die Engine auf alle zulässigen Aussprachen für das Kanji lauschen.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-150">However, you can just pass in Kanji without the Kana, in which case the engine should listen for all acceptable pronunciations for the Kanji.</span></span> <span data-ttu-id="6c6c4-151">Sie können auch nur Kana übergeben.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-151">You can also pass in just Kana.</span></span>

<span data-ttu-id="6c6c4-152">Beachten Sie auch, dass für Sprachen wie Japanisch, Chinesisch und Thailändisch, die keine Leerzeichen zum Festlegen von Wortumbrüchen verwenden, ein Unicode-Leerzeichen mit einer Breite von null (0x200B) einfügen, um logische Wortumbrüche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-152">Also note that for languages such as Japanese, Chinese, and Thai, that do not use space characters to designate word breaks, insert a Unicode zero-width space character (0x200B) to indicate logical word breaks.</span></span>

<span data-ttu-id="6c6c4-153">Mit Ausnahme von Fehlern bei der Verwendung der Gruppierungs- oder Wiederholungsformatierungszeichen meldet der -Agent keine Fehler in Ihrer Grammatik, es sei denn, die Engine selbst meldet den Fehler.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-153">Except for errors using the grouping or repetition formatting characters, Agent will not report errors in your grammar, unless the engine itself reports the error.</span></span> <span data-ttu-id="6c6c4-154">Wenn Sie Text in Ihrer Grammatik übergeben, der von der Engine nicht kompiliert werden kann, die Engine jedoch nicht behandelt und als Fehler zurückgegeben wird, kann der -Agent den Fehler nicht melden.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-154">If you pass text in your grammar that the engine fails to compile, but the engine does not handle and return as an error, Agent cannot report the error.</span></span> <span data-ttu-id="6c6c4-155">Daher muss die Clientanwendung die Grammatik für die [**Voice-Eigenschaft**](voice-property.md) sorgfältig definieren.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-155">Therefore, the client application must be carefully define grammar for the [**Voice**](voice-property.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="6c6c4-156">Die verfügbaren Grammatikfeatures hängen möglicherweise von der Spracherkennungs-Engine ab.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-156">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="6c6c4-157">Möglicherweise sollten Sie beim Anbieter der Engine nachsehen, welche Grammatikoptionen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-157">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="6c6c4-158">Verwenden Sie [**SRModeID,**](srmodeid-property.md) um eine bestimmte Engine zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-158">Use the [**SRModeID**](srmodeid-property.md) to use a specific engine.</span></span>

 

<span data-ttu-id="6c6c4-159">Der Vorgang dieser Eigenschaft hängt vom Zustand der Spracherkennungseigenschaft des Servers ab.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-159">The operation of this property depends on the state of the server's speech recognition property.</span></span> <span data-ttu-id="6c6c4-160">Wenn die Spracherkennung beispielsweise deaktiviert oder nicht installiert ist, hat diese Eigenschaft keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="6c6c4-160">For example, if speech recognition is disabled or not installed, this property has no effect.</span></span>

 

 
