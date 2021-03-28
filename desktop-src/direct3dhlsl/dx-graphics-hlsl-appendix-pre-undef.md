---
title: " undef-Direktive"
description: Eine Präprozessordirektive, mit der die aktuelle Definition einer Konstante oder eines Makros entfernt wird, die zuvor mit der \ define-Direktive definiert wurde.
ms.assetid: ba6bbe6b-ecfa-40cb-887f-e42b6e22c7bd
keywords:
- undef-Direktive HLSL
topic_type:
- apiref
api_name:
- undef Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7358dc60d002e784394f64773934a18f7413e493
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312552"
---
# <a name="undef-directive"></a><span data-ttu-id="e50be-104">\#undef-Direktive</span><span class="sxs-lookup"><span data-stu-id="e50be-104">\#undef Directive</span></span>

<span data-ttu-id="e50be-105">Eine Präprozessordirektive, die die aktuelle Definition einer Konstante oder eines Makros entfernt, die zuvor mit der [ \# define](dx-graphics-hlsl-appendix-pre-define.md) -Direktive definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e50be-105">Preprocessor directive that removes the current definition of a constant or macro that was previously defined using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive.</span></span>



| <span data-ttu-id="e50be-106">\#undef- *Bezeichner*</span><span class="sxs-lookup"><span data-stu-id="e50be-106">\#undef *identifier*</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="e50be-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e50be-107">Parameters</span></span>



| <span data-ttu-id="e50be-108">Element</span><span class="sxs-lookup"><span data-stu-id="e50be-108">Item</span></span>                                                                              | <span data-ttu-id="e50be-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e50be-109">Description</span></span>                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e50be-110"><span id="identifier"></span><span id="IDENTIFIER"></span>*Figur*</span><span class="sxs-lookup"><span data-stu-id="e50be-110"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/> | <span data-ttu-id="e50be-111">Der Bezeichner der Konstante oder des Makros, dessen Definition entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e50be-111">Identifier of the constant or macro to remove the definition of.</span></span> <span data-ttu-id="e50be-112">Wenn Sie ein Makro definieren, geben Sie nur den Bezeichner und nicht die Parameterliste an.</span><span class="sxs-lookup"><span data-stu-id="e50be-112">If you are undefining a macro, provide only the identifier, not the parameter list.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="e50be-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e50be-113">Remarks</span></span>

<span data-ttu-id="e50be-114">Sie können die \# undef-Direktive auf einen Bezeichner anwenden, der keine vorherige Definition hat. Dadurch wird sichergestellt, dass der Bezeichner nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e50be-114">You can apply the \#undef directive to an identifier that has no previous definition; this ensures that the identifier is undefined.</span></span> <span data-ttu-id="e50be-115">Makro Ersetzung wird nicht innerhalb von \# undef-Anweisungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e50be-115">Macro replacement is not performed within \#undef statements.</span></span>

<span data-ttu-id="e50be-116">Die \# undef-Direktive wird in der Regel mit einer [ \# define](dx-graphics-hlsl-appendix-pre-define.md) -Direktive gekoppelt, um einen Bereich in einem Quell Programm zu erstellen, in dem ein Bezeichner eine besondere Bedeutung hat.</span><span class="sxs-lookup"><span data-stu-id="e50be-116">The \#undef directive is typically paired with a [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive to create a region in a source program in which an identifier has a special meaning.</span></span> <span data-ttu-id="e50be-117">Beispielsweise kann eine bestimmte Funktion des Quellprogramms Manifestkonstanten verwenden, um umgebungsspezifische Werte zu definieren, die sich nicht auf das übrige Programm auswirken.</span><span class="sxs-lookup"><span data-stu-id="e50be-117">For example, a specific function of the source program can use manifest constants to define environment-specific values that do not affect the rest of the program.</span></span> <span data-ttu-id="e50be-118">Die \# undef-Direktive funktioniert auch mit der [)-Direktive, um die bedingte Kompilierung des Quell Programms zu steuern.</span><span class="sxs-lookup"><span data-stu-id="e50be-118">The \#undef directive also works with the [) directive to control conditional compilation of the source program.</span></span>

<span data-ttu-id="e50be-119">Konstanten und Makros können mithilfe der/U-Option in der Befehlszeile nicht definiert werden, gefolgt von den bezeichlern, die nicht definiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e50be-119">Constants and macros can be undefined from the command line using the /U option, followed by the identifiers to be undefined.</span></span> <span data-ttu-id="e50be-120">Dies entspricht dem Hinzufügen einer Sequenz von \# undef-Direktiven am Anfang der Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="e50be-120">This is equivalent to adding a sequence of \#undef directives at the beginning of the source file.</span></span>

## <a name="examples"></a><span data-ttu-id="e50be-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e50be-121">Examples</span></span>

<span data-ttu-id="e50be-122">Im folgenden Beispiel wird gezeigt, wie die \# undef-Direktive verwendet wird, um Definitionen einer symbolischen Konstante und eines Makros zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="e50be-122">The following example shows how to use the \#undef directive to remove definitions of a symbolic constant and a macro.</span></span>


```
#define WIDTH           80
#define ADD( X, Y )     (X) + (Y)

#undef WIDTH
#undef ADD
```



## <a name="see-also"></a><span data-ttu-id="e50be-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e50be-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e50be-124">Präprozessordirektiven (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e50be-124">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="e50be-125">\#define-Direktive (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e50be-125">\#define Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="e50be-126">\#Wenn,)</span><span class="sxs-lookup"><span data-stu-id="e50be-126">\#if, )</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





