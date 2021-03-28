---
title: '\#define-Direktive (Makro)'
description: Eine Präprozessordirektive, die ein Funktions ähnliches Makro erstellt.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8de5a47fc92c02e9f565c80f600359e8e5b32f9
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104993278"
---
# <a name="define-directive-macro"></a><span data-ttu-id="33e3d-103">\#define-Direktive (Makro)</span><span class="sxs-lookup"><span data-stu-id="33e3d-103">\#define directive (macro)</span></span>

<span data-ttu-id="33e3d-104">Eine Präprozessordirektive, die ein Funktions ähnliches Makro erstellt.</span><span class="sxs-lookup"><span data-stu-id="33e3d-104">Preprocessor directive that creates a function-like macro.</span></span>



| <span data-ttu-id="33e3d-105">\#*Bezeichner* definieren ( *argument0*,..., *argumentn-1* ) *Tokenzeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="33e3d-105">\#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string*</span></span> |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="33e3d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33e3d-106">Parameters</span></span>



| <span data-ttu-id="33e3d-107">Element</span><span class="sxs-lookup"><span data-stu-id="33e3d-107">Item</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="33e3d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33e3d-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33e3d-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*Figur*</span><span class="sxs-lookup"><span data-stu-id="33e3d-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                                                                                                                                                             | <span data-ttu-id="33e3d-110">Der Bezeichner des Makros.</span><span class="sxs-lookup"><span data-stu-id="33e3d-110">Identifier of the macro.</span></span> <br/> <span data-ttu-id="33e3d-111">Eine zweite [ \# Definition](dx-graphics-hlsl-appendix-pre-define.md) für ein Makro mit einem Bezeichner, der bereits im aktuellen Kontext vorhanden ist, generiert einen Fehler, es sei denn, die zweite tokensequenz ist mit der ersten identisch.</span><span class="sxs-lookup"><span data-stu-id="33e3d-111">A second [\#define](dx-graphics-hlsl-appendix-pre-define.md) for a macro with an identifier that already exists in the current context generates an error unless the second token sequence is identical to the first.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="33e3d-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*,..., *argumentn-1* )</span><span class="sxs-lookup"><span data-stu-id="33e3d-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* )</span></span> <br/> | <span data-ttu-id="33e3d-113">Liste der Argumente für das Makro.</span><span class="sxs-lookup"><span data-stu-id="33e3d-113">List of arguments to the macro.</span></span> <span data-ttu-id="33e3d-114">Die Argumentliste ist durch Kommas getrennt, kann eine beliebige Länge aufweisen und muss in Klammern eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="33e3d-114">The argument list is comma-delimited, can be of any length, and must be enclosed in parentheses.</span></span> <span data-ttu-id="33e3d-115">Jeder Argument Name in der Liste muss eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="33e3d-115">Each argument name in the list must be unique.</span></span> <span data-ttu-id="33e3d-116">Der *bezeichnerparameter* und die öffnende Klammer können nicht durch Leerzeichen getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="33e3d-116">No white space can separate the *identifier* parameter and the opening parenthesis.</span></span> <br/> <span data-ttu-id="33e3d-117">Zeilen Verkettung platzieren platzieren Sie einen umgekehrten Schrägstrich ( \) unmittelbar vor dem Zeilen Umleitungs Zeichen, um lange Direktiven in mehrere Quellzeilen aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="33e3d-117">Use line concatenation place a backslash (\) immediately before the newline character to split long directives onto multiple source lines.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="33e3d-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*Tokenzeichenfolge* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="33e3d-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[optional\]</span></span> <br/>                                                                                                                     | <span data-ttu-id="33e3d-119">Der Wert des Makros.</span><span class="sxs-lookup"><span data-stu-id="33e3d-119">Value of the macro.</span></span> <span data-ttu-id="33e3d-120">Dieser Parameter besteht aus einer Reihe von Token, wie z. b. Schlüsselwörtern, Konstanten oder Complete-Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="33e3d-120">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="33e3d-121">Dieser Parameter muss von einem oder mehreren Leerzeichen vom *bezeichnerparameter* getrennt werden. Dieser Leerraum wird nicht als Teil des ersetzten Texts betrachtet, und es ist kein Leerraum nach dem letzten Token des Texts enthalten.</span><span class="sxs-lookup"><span data-stu-id="33e3d-121">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <span data-ttu-id="33e3d-122">Nehmen Sie eine liberale Verwendung von Klammern vor, um sicherzustellen, dass komplizierte Argumente ordnungsgemäß interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="33e3d-122">Make liberal use of parentheses to ensure that complicated arguments are interpreted correctly.</span></span> <br/> <span data-ttu-id="33e3d-123">Wenn der Wert des *bezeichnerparameters* innerhalb des *Tokenzeichenfolgen-* Parameters auftritt (auch als Ergebnis einer anderen Makro Erweiterung), wird er nicht erweitert.</span><span class="sxs-lookup"><span data-stu-id="33e3d-123">If the value of the *identifier* parameter occurs within the *token-string* parameter (even as a result of another macro expansion), it is not expanded.</span></span> <br/> <span data-ttu-id="33e3d-124">Wenn Sie diesen Parameter ausschließen, werden alle Instanzen des *bezeichnerparameters* aus der Quelldatei entfernt.</span><span class="sxs-lookup"><span data-stu-id="33e3d-124">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="33e3d-125">Der Bezeichner bleibt definiert und kann mithilfe der Direktiven [ \# if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef und \# ifndef getestet werden.</span><span class="sxs-lookup"><span data-stu-id="33e3d-125">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="33e3d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33e3d-126">Remarks</span></span>

<span data-ttu-id="33e3d-127">Alle Instanzen des *bezeichnerparameters* , die nach der [ \# define](dx-graphics-hlsl-appendix-pre-define.md) -Direktive in der Quelldatei auftreten, bilden einen Makro-Aufrufwert, und der Bezeichner wird durch eine Version des *Tokenzeichenfolgen-* Parameters ersetzt, der tatsächliche Argumente für formale Parameter ersetzt.</span><span class="sxs-lookup"><span data-stu-id="33e3d-127">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file constitute a macro call, and the identifier will be replaced by a version of the *token-string* parameter that has actual arguments substituted for formal parameters.</span></span> <span data-ttu-id="33e3d-128">Die Anzahl der Parameter im-Aufrufwert muss mit der Anzahl von Parametern in der Makro Definition identisch sein.</span><span class="sxs-lookup"><span data-stu-id="33e3d-128">The number of parameters in the call must match the number of parameters in the macro definition.</span></span> <span data-ttu-id="33e3d-129">Der Bezeichner wird nur ersetzt, wenn er ein Token bildet. Beispielsweise wird der Bezeichner nicht ersetzt, wenn er in einem Kommentar, innerhalb einer Zeichenfolge oder als Teil eines längeren Bezeichners angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="33e3d-129">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="33e3d-130">Die [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) -Direktive weist den Präprozessor an, die Definition eines Bezeichners zu vergessen. Weitere Informationen finden Sie unter \# undef-Direktive (DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="33e3d-130">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="33e3d-131">Das Definieren von Konstanten mit der/D-Compileroption hat dieselbe Auswirkung wie die Verwendung der [ \# define](dx-graphics-hlsl-appendix-pre-define.md) -Direktive am Anfang der Datei.</span><span class="sxs-lookup"><span data-stu-id="33e3d-131">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="33e3d-132">Bis zu 30 Makros können mit der/D-Option definiert werden.</span><span class="sxs-lookup"><span data-stu-id="33e3d-132">Up to 30 macros can be defined with the /D option.</span></span>

<span data-ttu-id="33e3d-133">Die tatsächlichen Argumente im Makro-Befehl werden mit den entsprechenden formalen Argumenten in der Makro Definition abgeglichen.</span><span class="sxs-lookup"><span data-stu-id="33e3d-133">The actual arguments in the macro call are matched to the corresponding formal arguments in the macro definition.</span></span> <span data-ttu-id="33e3d-134">Jedes formale Argument in der Tokenzeichenfolge wird durch das entsprechende tatsächliche Argument ersetzt, es sei denn, dem Argument ist ein \# Zeichen folgen Operator (), ein \# Zeichen (@) oder ein tokeneinfügeoperator ( \# \# ) oder ein \# \# Operator gefolgt.</span><span class="sxs-lookup"><span data-stu-id="33e3d-134">Each formal argument in the token string is replaced by the corresponding actual argument, unless the argument is preceded by a stringizing (\#), charizing (\#@), or token-pasting (\#\#) operator, or is followed by a \#\# operator.</span></span> <span data-ttu-id="33e3d-135">Alle Makros im tatsächlichen Argument werden erweitert, bevor die Anweisung den formalen Parameter ersetzt.</span><span class="sxs-lookup"><span data-stu-id="33e3d-135">Any macros in the actual argument are expanded before the directive replaces the formal parameter.</span></span>

<span data-ttu-id="33e3d-136">Das Einfügen von Token im HLSL-Compiler unterscheidet sich geringfügig von der tokeneinfügefunktion im C-Compiler, da die eingefügten Token selbst gültige Token sein müssen.</span><span class="sxs-lookup"><span data-stu-id="33e3d-136">Token pasting in the HLSL compiler is slightly different from token pasting in the C compiler, in that the pasted tokens must be valid tokens on their own.</span></span> <span data-ttu-id="33e3d-137">Beachten Sie beispielsweise die folgende Makro Definition:</span><span class="sxs-lookup"><span data-stu-id="33e3d-137">For example, consider the following macro definition:</span></span>


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



<span data-ttu-id="33e3d-138">Im C-Compiler führt dies zu folgendem:</span><span class="sxs-lookup"><span data-stu-id="33e3d-138">In the C compiler, this results in the following:</span></span>


```
float4x4 test
```



<span data-ttu-id="33e3d-139">Im HLSL-Compiler führt dies jedoch zu folgendem:</span><span class="sxs-lookup"><span data-stu-id="33e3d-139">In the HLSL compiler however, this results in the following:</span></span>


```
float4 x4 test
```



<span data-ttu-id="33e3d-140">Sie können dieses Verhalten umgehen, indem Sie stattdessen die folgende Makro Definition verwenden.</span><span class="sxs-lookup"><span data-stu-id="33e3d-140">You can work around this behavior by using the following macro definition instead.</span></span>


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a><span data-ttu-id="33e3d-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33e3d-141">Examples</span></span>

<span data-ttu-id="33e3d-142">Im folgenden Beispiel wird ein-Makro zum Definieren von Cursor Linien verwendet.</span><span class="sxs-lookup"><span data-stu-id="33e3d-142">The following example uses a macro to define cursor lines.</span></span>


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



<span data-ttu-id="33e3d-143">Im folgenden Beispiel wird ein Makro definiert, das eine Pseudo Zufalls-Ganzzahl im angegebenen Bereich abruft.</span><span class="sxs-lookup"><span data-stu-id="33e3d-143">The following example defines a macro that retrieves a pseudorandom integer in the specified range.</span></span>


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a><span data-ttu-id="33e3d-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33e3d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33e3d-145">Präprozessordirektiven (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33e3d-145">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="33e3d-146">\#Definieren von über Ladungen</span><span class="sxs-lookup"><span data-stu-id="33e3d-146">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="33e3d-147">\#undef-Direktive (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33e3d-147">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





