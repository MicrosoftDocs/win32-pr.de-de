---
title: '\#define-Direktive (Makro)'
description: Präprozessordi directive that creates a function-like macro.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d0c54c0c433c91522c8a72c5955a419eb72f9eee
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387516"
---
# <a name="define-directive-macro"></a><span data-ttu-id="45767-103">\#define-Direktive (Makro)</span><span class="sxs-lookup"><span data-stu-id="45767-103">\#define directive (macro)</span></span>

<span data-ttu-id="45767-104">Präprozessordi directive that creates a function-like macro.</span><span class="sxs-lookup"><span data-stu-id="45767-104">Preprocessor directive that creates a function-like macro.</span></span>



| <span data-ttu-id="45767-105">\#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string*</span><span class="sxs-lookup"><span data-stu-id="45767-105">\#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string*</span></span> |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="45767-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="45767-106">Parameters</span></span>



| <span data-ttu-id="45767-107">Element</span><span class="sxs-lookup"><span data-stu-id="45767-107">Item</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="45767-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45767-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45767-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*Bezeichner*</span><span class="sxs-lookup"><span data-stu-id="45767-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                                                                                                                                                             | <span data-ttu-id="45767-110">Bezeichner des Makros.</span><span class="sxs-lookup"><span data-stu-id="45767-110">Identifier of the macro.</span></span> <br/> <span data-ttu-id="45767-111">Eine zweite [ \# Definition für](dx-graphics-hlsl-appendix-pre-define.md) ein Makro mit einem Bezeichner, der bereits im aktuellen Kontext vorhanden ist, generiert einen Fehler, es sei denn, die zweite Tokensequenz ist mit der ersten identisch.</span><span class="sxs-lookup"><span data-stu-id="45767-111">A second [\#define](dx-graphics-hlsl-appendix-pre-define.md) for a macro with an identifier that already exists in the current context generates an error unless the second token sequence is identical to the first.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="45767-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* )</span><span class="sxs-lookup"><span data-stu-id="45767-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* )</span></span> <br/> | <span data-ttu-id="45767-113">Liste der Argumente für das Makro.</span><span class="sxs-lookup"><span data-stu-id="45767-113">List of arguments to the macro.</span></span> <span data-ttu-id="45767-114">Die Argumentliste ist durch Kommas getrennt, kann eine beliebige Länge haben und muss in Klammern eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="45767-114">The argument list is comma-delimited, can be of any length, and must be enclosed in parentheses.</span></span> <span data-ttu-id="45767-115">Jeder Argumentname in der Liste muss eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="45767-115">Each argument name in the list must be unique.</span></span> <span data-ttu-id="45767-116">Der Bezeichnerparameter und die öffnende *Klammer* können nicht durch Leerzeichen getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="45767-116">No white space can separate the *identifier* parameter and the opening parenthesis.</span></span> <br/> <span data-ttu-id="45767-117">Verwenden Sie die Zeilenkonkettierung, um einen zurücken Schrägstrich ( ) direkt vor dem Zeilenumbruchzeichen zu platzieren, um lange Anweisungen auf mehrere \\ Quellzeilen zu teilen.</span><span class="sxs-lookup"><span data-stu-id="45767-117">Use line concatenation place a backslash (\\) immediately before the newline character to split long directives onto multiple source lines.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="45767-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="45767-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[optional\]</span></span> <br/>                                                                                                                     | <span data-ttu-id="45767-119">Der Wert des Makros.</span><span class="sxs-lookup"><span data-stu-id="45767-119">Value of the macro.</span></span> <span data-ttu-id="45767-120">Dieser Parameter besteht aus einer Reihe von Token, z. B. Schlüsselwörtern, Konstanten oder vollständigen Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="45767-120">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="45767-121">Mindestens ein Leerzeichen muss diesen Parameter vom *Bezeichnerparameter* trennen. dieses Leerzeichen wird weder als Teil des ersetzten Texts noch als Leerzeichen nach dem letzten Token des Texts betrachtet.</span><span class="sxs-lookup"><span data-stu-id="45767-121">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <span data-ttu-id="45767-122">Verwenden Sie Klammern, um sicherzustellen, dass komplizierte Argumente richtig interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="45767-122">Make liberal use of parentheses to ensure that complicated arguments are interpreted correctly.</span></span> <br/> <span data-ttu-id="45767-123">Wenn der Wert  des Bezeichnerparameters im Tokenzeichenfolgenparameter auftritt (auch als Ergebnis einer anderen Makroerweiterung), wird er nicht erweitert. </span><span class="sxs-lookup"><span data-stu-id="45767-123">If the value of the *identifier* parameter occurs within the *token-string* parameter (even as a result of another macro expansion), it is not expanded.</span></span> <br/> <span data-ttu-id="45767-124">Wenn Sie diesen Parameter ausschließen,  werden alle Instanzen des Bezeichnerparameters aus der Quelldatei entfernt.</span><span class="sxs-lookup"><span data-stu-id="45767-124">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="45767-125">Der Bezeichner bleibt definiert und kann mithilfe der [ \# if-definierten](dx-graphics-hlsl-appendix-pre-ifdef.md)Anweisungen , \# ifdef und \# ifndef getestet werden.</span><span class="sxs-lookup"><span data-stu-id="45767-125">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="45767-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45767-126">Remarks</span></span>

<span data-ttu-id="45767-127">Alle Instanzen des  Bezeichnerparameters, die nach der [ \# define-Direktive](dx-graphics-hlsl-appendix-pre-define.md) in der Quelldatei auftreten, bilden einen Makroaufruf, und der Bezeichner wird durch eine Version des *Tokenzeichenfolgenparameters* ersetzt, der tatsächliche Argumente durch formale Parameter ersetzt.</span><span class="sxs-lookup"><span data-stu-id="45767-127">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file constitute a macro call, and the identifier will be replaced by a version of the *token-string* parameter that has actual arguments substituted for formal parameters.</span></span> <span data-ttu-id="45767-128">Die Anzahl der Parameter im Aufruf muss mit der Anzahl der Parameter in der Makrodefinition übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="45767-128">The number of parameters in the call must match the number of parameters in the macro definition.</span></span> <span data-ttu-id="45767-129">Der Bezeichner wird nur ersetzt, wenn er ein Token bildet. Beispielsweise wird der Bezeichner nicht ersetzt, wenn er in einem Kommentar, innerhalb einer Zeichenfolge oder als Teil eines längeren Bezeichners angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="45767-129">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="45767-130">Die [ \# Undef-Direktive](dx-graphics-hlsl-appendix-pre-undef.md) weist den Präprozessor an, die Definition eines Bezeichners zu vergessen. Weitere Informationen finden Sie unter \# undef Directive (DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="45767-130">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="45767-131">Das Definieren von Konstanten mit der Compileroption /D hat die gleiche Wirkung wie die Verwendung der [ \# define-Direktive](dx-graphics-hlsl-appendix-pre-define.md) am Anfang der Datei.</span><span class="sxs-lookup"><span data-stu-id="45767-131">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="45767-132">Mit der Option /D können bis zu 30 Makros definiert werden.</span><span class="sxs-lookup"><span data-stu-id="45767-132">Up to 30 macros can be defined with the /D option.</span></span>

<span data-ttu-id="45767-133">Die tatsächlichen Argumente im Makroaufruf werden mit den entsprechenden formalen Argumenten in der Makrodefinition übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="45767-133">The actual arguments in the macro call are matched to the corresponding formal arguments in the macro definition.</span></span> <span data-ttu-id="45767-134">Jedes formale Argument in der Tokenzeichenfolge wird durch das entsprechende tatsächliche Argument ersetzt, es sei denn, dem Argument ist ein Zeichenfolgenoperator ( ), ein Zeichenoperator ( @) oder ein Operator gefolgt von einem -Operator \# \# \# \# \# \# vorangegangen.</span><span class="sxs-lookup"><span data-stu-id="45767-134">Each formal argument in the token string is replaced by the corresponding actual argument, unless the argument is preceded by a stringizing (\#), charizing (\#@), or token-pasting (\#\#) operator, or is followed by a \#\# operator.</span></span> <span data-ttu-id="45767-135">Alle Makros im tatsächlichen Argument werden erweitert, bevor die Anweisung den formalen Parameter ersetzt.</span><span class="sxs-lookup"><span data-stu-id="45767-135">Any macros in the actual argument are expanded before the directive replaces the formal parameter.</span></span>

<span data-ttu-id="45767-136">Das Einfing von Token im HLSL-Compiler ist etwas anders als das Einfing von Token im C-Compiler, da die einzugebenden Token selbst gültige Token sein müssen.</span><span class="sxs-lookup"><span data-stu-id="45767-136">Token pasting in the HLSL compiler is slightly different from token pasting in the C compiler, in that the pasted tokens must be valid tokens on their own.</span></span> <span data-ttu-id="45767-137">Betrachten Sie beispielsweise die folgende Makrodefinition:</span><span class="sxs-lookup"><span data-stu-id="45767-137">For example, consider the following macro definition:</span></span>


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



<span data-ttu-id="45767-138">Im C-Compiler führt dies zu Folgendem:</span><span class="sxs-lookup"><span data-stu-id="45767-138">In the C compiler, this results in the following:</span></span>


```
float4x4 test
```



<span data-ttu-id="45767-139">Im HLSL-Compiler führt dies jedoch zu Folgendem:</span><span class="sxs-lookup"><span data-stu-id="45767-139">In the HLSL compiler however, this results in the following:</span></span>


```
float4 x4 test
```



<span data-ttu-id="45767-140">Sie können dieses Verhalten mithilfe der folgenden Makrodefinition vermeiden.</span><span class="sxs-lookup"><span data-stu-id="45767-140">You can work around this behavior by using the following macro definition instead.</span></span>


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a><span data-ttu-id="45767-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45767-141">Examples</span></span>

<span data-ttu-id="45767-142">Im folgenden Beispiel wird ein Makro verwendet, um Cursorzeilen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="45767-142">The following example uses a macro to define cursor lines.</span></span>


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



<span data-ttu-id="45767-143">Im folgenden Beispiel wird ein Makro definiert, das eine pseudozufällige ganze Zahl im angegebenen Bereich abruft.</span><span class="sxs-lookup"><span data-stu-id="45767-143">The following example defines a macro that retrieves a pseudorandom integer in the specified range.</span></span>


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a><span data-ttu-id="45767-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="45767-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45767-145">Präprozessordirektiven (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="45767-145">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="45767-146">\#Definieren von Überladungen</span><span class="sxs-lookup"><span data-stu-id="45767-146">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="45767-147">\#undef-Direktive (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="45767-147">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





