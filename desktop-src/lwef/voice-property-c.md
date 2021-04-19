---
title: Voice-Eigenschaft (Befehls Objekt)
description: Voice-Eigenschaft
ms.assetid: e393aa89-6fa7-4080-9faf-66faca83d561
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a8f9003b5200882fc01ee37edb868a261c68c7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106342179"
---
# <a name="voice-property-command-object"></a><span data-ttu-id="b79e0-103">Voice-Eigenschaft (Befehls Objekt)</span><span class="sxs-lookup"><span data-stu-id="b79e0-103">Voice Property (Command Object)</span></span>

<span data-ttu-id="b79e0-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="b79e0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b79e0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b79e0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b79e0-106">Gibt den Text zurück, der an die Sprach-Engine-Grammatik (zur Erkennung) zum Abgleichen des [**Befehls**](/windows/desktop/lwef/the-command-object) für das Zeichen übergebenen wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="b79e0-106">Returns or sets the text that is passed to the speech engine grammar (for recognition) for matching this [**Command**](/windows/desktop/lwef/the-command-object) for the character.</span></span>

</dd> <dt>

<span data-ttu-id="b79e0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="b79e0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b79e0-108">\*Agent \***. Zeichen ("**_Merkmal-ID_*_"). Befehle ("_*_Name_\*_"). Sprach_ \*  \[  =  *Zeichenfolge*\]</span><span class="sxs-lookup"><span data-stu-id="b79e0-108">*agent\***.Characters ("**_CharacterID_*_").Commands ("_*_name_*_").Voice_\* \[ = *string*\]</span></span>



| <span data-ttu-id="b79e0-109">Teil</span><span class="sxs-lookup"><span data-stu-id="b79e0-109">Part</span></span>     | <span data-ttu-id="b79e0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b79e0-110">Description</span></span>                                                                                                                                       |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b79e0-111">*string*</span><span class="sxs-lookup"><span data-stu-id="b79e0-111">*string*</span></span> | <span data-ttu-id="b79e0-112">Ein Zeichen folgen Ausdruck, der den Wörtern oder dem Ausdruck entspricht, der von der Sprach-Engine zum erkennen dieses [**Befehls**](/windows/desktop/lwef/the-command-object)verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b79e0-112">A string expression corresponding to the words or phrase to be used by the speech engine for recognizing this [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b79e0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b79e0-113">Remarks</span></span>

<span data-ttu-id="b79e0-114">Wenn Sie diesen Parameter nicht angeben, wird die [**voicecaption**](voicecaption-property.md) für das [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Objekt nicht im Fenster "Sprachbefehle" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b79e0-114">If you do not supply this parameter, the [**VoiceCaption**](voicecaption-property.md) for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object will not appear in the Voice Commands Window.</span></span> <span data-ttu-id="b79e0-115">Wenn Sie einen [**sprach**](voice-property.md) Parameter angeben, aber keine **voicecaption** (oder [**Beschriftung**](https://www.bing.com/search?q=**Caption**)), wird der Befehl nicht im Fenster "Sprachbefehle" angezeigt, aber er kann auf die Spracheingabe zugreifen, wenn die Client Anwendung aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="b79e0-115">If you specify a [**Voice**](voice-property.md) parameter but not a **VoiceCaption** (or [**Caption**](https://www.bing.com/search?q=**Caption**)), the command will not appear in the Voice Commands Window, but it will be voice-accessible when the client application becomes input-active.</span></span>

<span data-ttu-id="b79e0-116">Der Zeichen folgen Ausdruck kann eckige Klammer Zeichen ( \[ \] ) enthalten, um optionale Wörter und vertikale Balken Zeichen ( \| ) anzugeben, um alternative Zeichen folgen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b79e0-116">Your string expression can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="b79e0-117">Alternativen müssen in Klammern eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="b79e0-117">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="b79e0-118">Beispiel: "(Hello \[ there \] \| HI)" weist die Sprach-Engine an, "Hello", "Hello There" oder "Hi" für den Befehl zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="b79e0-118">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="b79e0-119">Denken Sie daran, die entsprechenden Leerzeichen zwischen dem Text in Klammern oder Klammern und dem Text, der sich nicht in Klammern oder Klammern befindet, einzufügen.</span><span class="sxs-lookup"><span data-stu-id="b79e0-119">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span>

<span data-ttu-id="b79e0-120">Sie können den Stern ( \* )-Operator verwenden, um NULL oder mehr Instanzen der in der Gruppe enthaltenen Wörter anzugeben, oder den Plus (+)-Operator, um eine oder mehrere Instanzen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b79e0-120">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="b79e0-121">Der folgende Code führt z. b. zu einer Grammatik, die "try this", "try this", "try do this", mit unbegrenzten Iterationen von "bitte" unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b79e0-121">For example, the following results in a grammar that supports "try this", "please try this", "please please try this", with unlimited iterations of "please":</span></span>


```
   "please* try this"
```



<span data-ttu-id="b79e0-122">Das folgende Grammatik Format schließt "try this" aus, da der +-Operator mindestens eine Instanz von "bitte" definiert:</span><span class="sxs-lookup"><span data-stu-id="b79e0-122">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>


```
   "please+ try this"
```



<span data-ttu-id="b79e0-123">Die Wiederholungs Operatoren befolgen normale Rangfolge und gelten für das unmittelbar vorangehende Textelement.</span><span class="sxs-lookup"><span data-stu-id="b79e0-123">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="b79e0-124">Die folgende Grammatik ergibt beispielsweise "New York" und "New York York", aber nicht "New York New York":</span><span class="sxs-lookup"><span data-stu-id="b79e0-124">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>


```
   "New York+"
```



<span data-ttu-id="b79e0-125">Daher sollten Sie diese Operatoren in der Regel mit den Gruppierungs Zeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b79e0-125">Therefore, you typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="b79e0-126">Die folgende Grammatik enthält z. b. "New York" und "New York New York":</span><span class="sxs-lookup"><span data-stu-id="b79e0-126">For example, the following grammar includes both "New York" and "New York New York":</span></span>


```
   "(New York)+"
```



<span data-ttu-id="b79e0-127">Wiederholungs Operatoren sind nützlich, wenn Sie eine Grammatik verfassen möchten, die eine wiederholte Sequenz, z. b. eine Telefonnummer oder eine Angabe einer Liste von Elementen, enthält.</span><span class="sxs-lookup"><span data-stu-id="b79e0-127">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items.</span></span>


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



<span data-ttu-id="b79e0-128">Obwohl die Operatoren auch mit dem optionalen Gruppierungs Zeichen für eckige Klammern verwendet werden können, kann dadurch die Effizienz der Agentverarbeitung der Grammatik verringert werden.</span><span class="sxs-lookup"><span data-stu-id="b79e0-128">Although the operators can also be used with the optional square-brackets grouping character, doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="b79e0-129">Sie können auch ein Auslassungs Zeichen (...) verwenden, um die Erkennung von Wörtern zu unterstützen, d. h., das sprach Erkennungs Modul soll Wörter ignorieren, die an dieser Position in dem Ausdruck *gesprochen werden (* manchmal als " *Garbage* Words" bezeichnet)</span><span class="sxs-lookup"><span data-stu-id="b79e0-129">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="b79e0-130">Daher erkennt die Sprach-Engine nur bestimmte Wörter in der Zeichenfolge, unabhängig davon, wann Sie mit benachbarten Wörtern oder Ausdrücken gesprochen werden.</span><span class="sxs-lookup"><span data-stu-id="b79e0-130">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="b79e0-131">Wenn Sie diese Eigenschaft beispielsweise auf " \[ ... \] e-Mail-Überprüfung \[ ... \] ", die Spracherkennungs-Engine entspricht den Ausdrücken wie" Bitte überprüfen Sie e-Mail "oder" e-Mail überprüfen "auf diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="b79e0-131">For example, if you set this property to "\[...\] check mail \[...\]", the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="b79e0-132">Ellipsen können überall innerhalb einer Zeichenfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b79e0-132">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="b79e0-133">Seien Sie jedoch vorsichtig, wenn Sie diese Technik verwenden, da dadurch möglicherweise unerwünschte Übereinstimmungen entstehen.</span><span class="sxs-lookup"><span data-stu-id="b79e0-133">However, be careful using this technique as it may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="b79e0-134">Wenn Sie die Wort Grammatik für Ihren Befehl definieren, schließen Sie mindestens ein Wort ein, das erforderlich ist. Dies bedeutet, dass nur optionale Wörter bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b79e0-134">When defining the word grammar for your command, include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="b79e0-135">Stellen Sie außerdem sicher, dass das Wort nur sprechbare Wörter und Buchstaben enthält.</span><span class="sxs-lookup"><span data-stu-id="b79e0-135">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="b79e0-136">Bei Zahlen ist es besser, das Wort zu buchstabieren, anstatt eine mehrdeutige Darstellung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b79e0-136">For numbers, it is better to spell out the word rather than using an ambiguous representation.</span></span> <span data-ttu-id="b79e0-137">Beispielsweise ist "345" keine gute Grammatik Form.</span><span class="sxs-lookup"><span data-stu-id="b79e0-137">For example, "345" is not a good grammar form.</span></span> <span data-ttu-id="b79e0-138">Verwenden Sie auf ähnliche Weise anstelle von "IEEE" "I Triple E".</span><span class="sxs-lookup"><span data-stu-id="b79e0-138">Similarly, instead of "IEEE", use "I triple E".</span></span> <span data-ttu-id="b79e0-139">Lassen Sie außerdem alle Interpunktions Zeichen oder Symbole aus.</span><span class="sxs-lookup"><span data-stu-id="b79e0-139">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="b79e0-140">Verwenden Sie beispielsweise anstelle von "The \# $1 10 Pizza!" die Zahl 1 10 Dollar Pizza.</span><span class="sxs-lookup"><span data-stu-id="b79e0-140">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="b79e0-141">Das einschließen nicht-sprechbarer Zeichen oder Symbole für einen Befehl kann dazu führen, dass die Sprach-Engine die Grammatik für alle Befehle nicht kompiliert.</span><span class="sxs-lookup"><span data-stu-id="b79e0-141">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="b79e0-142">Legen Sie schließlich ihren Voice-Parameter so eindeutig wie möglich von anderen Sprachbefehlen, die Sie definieren.</span><span class="sxs-lookup"><span data-stu-id="b79e0-142">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="b79e0-143">Umso größer die Ähnlichkeit zwischen der Sprachgrammatik für Befehle, desto wahrscheinlicher wird die Sprach-Engine einen Erkennungs Fehler.</span><span class="sxs-lookup"><span data-stu-id="b79e0-143">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="b79e0-144">Sie können auch die Vertrauens Ergebnisse verwenden, um zwischen zwei Befehlen besser zu unterscheiden, die eine ähnliche oder ähnlich klingende Sprachgrammatik aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="b79e0-144">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="b79e0-145">Sie können in die Grammatik Wörter in Form von *Text \\ Aussprache* einschließen, wobei *Text* der angezeigte Text und die *Aussprache* Text ist, der die Aussprache verdeutlicht.</span><span class="sxs-lookup"><span data-stu-id="b79e0-145">You can include in your grammar words in the form of "*text\\pronunciation*", where *text* is the text displayed and *pronunciation* is text that clarifies the pronunciation.</span></span> <span data-ttu-id="b79e0-146">So würde z. b. die Grammatik "1st \\ First" erkannt werden, wenn der Benutzer "First" sagt, aber das [**Befehls**](/windows/desktop/lwef/the-command-object) Ereignis gibt den Text "1st \\ First" zurück.</span><span class="sxs-lookup"><span data-stu-id="b79e0-146">For example, the grammar, "1st\\first", would be recognized when the user says "first", but the [**Command**](/windows/desktop/lwef/the-command-object) event will return the text, "1st\\first".</span></span> <span data-ttu-id="b79e0-147">Sie können auch IPA (Internationales Phonetisches Alphabet) verwenden, um eine Aussprache anzugeben, indem Sie die Aussprache mit einem Nummern Zeichen (" \# ") beginnen und dann den Text einschließen, der die IPA-Aussprache darstellt.</span><span class="sxs-lookup"><span data-stu-id="b79e0-147">You can also use IPA (International Phonetic Alphabet) to specify a pronunciation by beginning the pronunciation with a pound sign character ("\#"), then include the text representing the IPA pronunciation.</span></span>

<span data-ttu-id="b79e0-148">Bei japanischen sprach Erkennungs Modulen können Sie die Grammatik in der Form "*Kana \\ Kanji*" definieren, um die alternativen Ausdrücke zu verringern und die Genauigkeit zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="b79e0-148">For Japanese speech recognition engines, you can define grammar in the form "*kana\\kanji*", reducing the alternative pronunciations and increasing the accuracy.</span></span> <span data-ttu-id="b79e0-149">(Die Reihenfolge wird aus Gründen der Abwärtskompatibilität umgekehrt.) Dies ist besonders wichtig für die Aussprache der richtigen Namen in Kanji.</span><span class="sxs-lookup"><span data-stu-id="b79e0-149">(The ordering is reversed for backward compatibility.) This is particularly important for the pronunciation of proper names in Kanji.</span></span> <span data-ttu-id="b79e0-150">Sie können jedoch nur Kanji ohne den Kana übergeben. in diesem Fall sollte die Engine alle zulässigen Ausdrücke für das Kanji überwachen.</span><span class="sxs-lookup"><span data-stu-id="b79e0-150">However, you can just pass in Kanji without the Kana, in which case the engine should listen for all acceptable pronunciations for the Kanji.</span></span> <span data-ttu-id="b79e0-151">Sie können auch nur Kana übergeben.</span><span class="sxs-lookup"><span data-stu-id="b79e0-151">You can also pass in just Kana.</span></span>

<span data-ttu-id="b79e0-152">Beachten Sie außerdem, dass bei Sprachen wie Japanisch, Chinesisch und Thailändisch, die keine Leerzeichen zum Angeben von Wort Umbrüchen verwenden, ein Unicode-Leerzeichen (0x200b) mit einer Breite von NULL Zeichen eingefügt werden, um logische Wort Umbrüche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b79e0-152">Also note that for languages such as Japanese, Chinese, and Thai, that do not use space characters to designate word breaks, insert a Unicode zero-width space character (0x200B) to indicate logical word breaks.</span></span>

<span data-ttu-id="b79e0-153">Mit Ausnahme von Fehlern bei Verwendung der Formatierungszeichen für die Gruppierung oder Wiederholung meldet der-Agent keine Fehler in der Grammatik, es sei denn, die Engine selbst meldet den Fehler.</span><span class="sxs-lookup"><span data-stu-id="b79e0-153">Except for errors using the grouping or repetition formatting characters, Agent will not report errors in your grammar, unless the engine itself reports the error.</span></span> <span data-ttu-id="b79e0-154">Wenn Sie Text in der Grammatik übergeben, dass die Engine nicht kompiliert werden kann, die Engine jedoch nicht verarbeitet und als Fehler zurückgibt, kann der-Agent den Fehler nicht melden.</span><span class="sxs-lookup"><span data-stu-id="b79e0-154">If you pass text in your grammar that the engine fails to compile, but the engine does not handle and return as an error, Agent cannot report the error.</span></span> <span data-ttu-id="b79e0-155">Daher muss die Client Anwendung die Grammatik für die [**Voice**](voice-property.md) -Eigenschaft sorgfältig definieren.</span><span class="sxs-lookup"><span data-stu-id="b79e0-155">Therefore, the client application must be carefully define grammar for the [**Voice**](voice-property.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="b79e0-156">Welche Grammatik Features verfügbar sind, hängt möglicherweise von der Spracherkennungs-Engine ab.</span><span class="sxs-lookup"><span data-stu-id="b79e0-156">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="b79e0-157">Möglicherweise möchten Sie sich an den Hersteller der Engine wenden, um zu ermitteln, welche Grammatik Optionen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b79e0-157">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="b79e0-158">Verwenden Sie [**srmodeid**](srmodeid-property.md) , um ein bestimmtes Modul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b79e0-158">Use the [**SRModeID**](srmodeid-property.md) to use a specific engine.</span></span>

 

<span data-ttu-id="b79e0-159">Der Vorgang dieser Eigenschaft hängt vom Status der sprach Erkennungs Eigenschaft des Servers ab.</span><span class="sxs-lookup"><span data-stu-id="b79e0-159">The operation of this property depends on the state of the server's speech recognition property.</span></span> <span data-ttu-id="b79e0-160">Wenn z. b. die Spracherkennung deaktiviert oder nicht installiert ist, hat diese Eigenschaft keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="b79e0-160">For example, if speech recognition is disabled or not installed, this property has no effect.</span></span>

 

 
