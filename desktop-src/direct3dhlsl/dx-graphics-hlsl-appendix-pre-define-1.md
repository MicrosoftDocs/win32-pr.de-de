---
title: '\#define-Direktive (Konstante)'
description: Eine Präprozessordirektive, die einer Konstanten in der Anwendung einen aussagekräftigen Namen zuweist.
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: deae1ca92c2280cd31cbec2bf3482c61fcf2b88a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104038380"
---
# <a name="define-directive-constant"></a><span data-ttu-id="c7d29-103">\#define-Direktive (Konstante)</span><span class="sxs-lookup"><span data-stu-id="c7d29-103">\#define directive (constant)</span></span>

<span data-ttu-id="c7d29-104">Eine Präprozessordirektive, die einer Konstanten in der Anwendung einen aussagekräftigen Namen zuweist.</span><span class="sxs-lookup"><span data-stu-id="c7d29-104">Preprocessor directive that assigns a meaningful name to a constant in your application.</span></span>



| <span data-ttu-id="c7d29-105">\#" *identifiertoken-String* " definieren</span><span class="sxs-lookup"><span data-stu-id="c7d29-105">\#define *identifiertoken-string*</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="c7d29-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7d29-106">Parameters</span></span>



| <span data-ttu-id="c7d29-107">Element</span><span class="sxs-lookup"><span data-stu-id="c7d29-107">Item</span></span>                                                                                                                       | <span data-ttu-id="c7d29-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7d29-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d29-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*Figur*</span><span class="sxs-lookup"><span data-stu-id="c7d29-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                          | <span data-ttu-id="c7d29-110">Der Bezeichner der Konstanten.</span><span class="sxs-lookup"><span data-stu-id="c7d29-110">Identifier of the constant.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="c7d29-111"><span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*Tokenzeichenfolge* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="c7d29-111"><span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*token-string* \[optional\]</span></span><br/> | <span data-ttu-id="c7d29-112">Der Wert der Konstanten.</span><span class="sxs-lookup"><span data-stu-id="c7d29-112">Value of the constant.</span></span> <span data-ttu-id="c7d29-113">Dieser Parameter besteht aus einer Reihe von Token, wie z. b. Schlüsselwörtern, Konstanten oder Complete-Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="c7d29-113">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="c7d29-114">Dieser Parameter muss von einem oder mehreren Leerzeichen vom *bezeichnerparameter* getrennt werden. Dieser Leerraum wird nicht als Teil des ersetzten Texts betrachtet, und es ist kein Leerraum nach dem letzten Token des Texts enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7d29-114">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <br/> <span data-ttu-id="c7d29-115">Wenn Sie diesen Parameter ausschließen, werden alle Instanzen des *bezeichnerparameters* aus der Quelldatei entfernt.</span><span class="sxs-lookup"><span data-stu-id="c7d29-115">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="c7d29-116">Der Bezeichner bleibt definiert und kann mithilfe der Direktiven [ \# if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef und \# ifndef getestet werden.</span><span class="sxs-lookup"><span data-stu-id="c7d29-116">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="c7d29-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7d29-117">Remarks</span></span>

<span data-ttu-id="c7d29-118">Alle Instanzen des *bezeichnerparameters* , die nach der [ \# define](dx-graphics-hlsl-appendix-pre-define.md) -Direktive in der Quelldatei auftreten, werden durch den Wert des *Tokenzeichenfolgen-* Parameters ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c7d29-118">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file will be replaced by the value of the *token-string* parameter.</span></span> <span data-ttu-id="c7d29-119">Der Bezeichner wird nur ersetzt, wenn er ein Token bildet. Beispielsweise wird der Bezeichner nicht ersetzt, wenn er in einem Kommentar, innerhalb einer Zeichenfolge oder als Teil eines längeren Bezeichners angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c7d29-119">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="c7d29-120">Die [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) -Direktive weist den Präprozessor an, die Definition eines Bezeichners zu vergessen. Weitere Informationen finden Sie unter \# undef-Direktive (DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="c7d29-120">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="c7d29-121">Das Definieren von Konstanten mit der/D-Compileroption hat dieselbe Auswirkung wie die Verwendung der [ \# define](dx-graphics-hlsl-appendix-pre-define.md) -Direktive am Anfang der Datei.</span><span class="sxs-lookup"><span data-stu-id="c7d29-121">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="c7d29-122">Bis zu 30 Konstanten können mit der/D-Option definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c7d29-122">Up to 30 constants can be defined with the /D option.</span></span> <span data-ttu-id="c7d29-123">Ein Beispiel für die Verwendung dieser Vorgehensweise finden Sie im Abschnitt "Beispiele" von [ \# ifdef und)](dx-graphics-hlsl-appendix-pre-ifdef.md).</span><span class="sxs-lookup"><span data-stu-id="c7d29-123">For an example of how this can be used, see the Examples section of [\#ifdef and )](dx-graphics-hlsl-appendix-pre-ifdef.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c7d29-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7d29-124">Examples</span></span>

<span data-ttu-id="c7d29-125">Im folgenden Beispiel wird die bezeichnerbreite als ganzzahlige Konstante 80 definiert, und anschließend wird die Länge in Bezug auf die Breite und die ganzzahlige Konstante 10 definiert.</span><span class="sxs-lookup"><span data-stu-id="c7d29-125">The following example defines the identifier WIDTH as the integer constant 80 and then defines LENGTH in terms of WIDTH and the integer constant 10.</span></span>


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



<span data-ttu-id="c7d29-126">Jede nachfolgende Instanz der Länge wird durch (Width + 10) ersetzt, und jede nachfolgende Instanz der Breite + 10 wird durch den Ausdruck ersetzt (80 + 10).</span><span class="sxs-lookup"><span data-stu-id="c7d29-126">Every subsequent instance of LENGTH is replaced by (WIDTH + 10), and every subsequent instance of WIDTH + 10 is replaced by the expression (80 + 10).</span></span> <span data-ttu-id="c7d29-127">Die Klammern um Breite + 10 sind wichtig, da Sie die Interpretation in Anweisungen wie den folgenden Steuern.</span><span class="sxs-lookup"><span data-stu-id="c7d29-127">The parentheses around WIDTH + 10 are important because they control the interpretation in statements such as the following.</span></span>


```
var = LENGTH * 20;
```



<span data-ttu-id="c7d29-128">Nach der Vorverarbeitungs Phase wird die-Anweisung wie folgt ausgewertet und ergibt den Wert 1.800.</span><span class="sxs-lookup"><span data-stu-id="c7d29-128">After the preprocessing stage the statement becomes the following, which evaluates to 1,800.</span></span>


```
var = ( 80 + 10 ) * 20;
```



<span data-ttu-id="c7d29-129">Ohne Klammern wäre das Ergebnis das folgende, das als 280 ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="c7d29-129">Without parentheses, the result would be the following, which evaluates to 280.</span></span>


```
var = 80 + 10 * 20;
```



## <a name="related-topics"></a><span data-ttu-id="c7d29-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c7d29-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7d29-131">Präprozessordirektiven (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7d29-131">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="c7d29-132">\#Definieren von über Ladungen</span><span class="sxs-lookup"><span data-stu-id="c7d29-132">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="c7d29-133">\#undef-Direktive (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7d29-133">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





