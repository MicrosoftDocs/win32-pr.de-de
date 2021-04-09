---
title: /WX-Schalter
description: Der/WX-Schalter weist den Mittelwert Compiler an, alle Fehler auf der angegebenen Warnstufe als Fehler zu behandeln.
ms.assetid: 1dd9791c-0488-4ca3-8a29-082ae03c3cd4
keywords:
- /WX-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /WX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b502cea5f686de2951f6f21ab92fdbffef779b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857503"
---
# <a name="wx-switch"></a><span data-ttu-id="18f8c-104">/WX-Schalter</span><span class="sxs-lookup"><span data-stu-id="18f8c-104">/WX switch</span></span>

<span data-ttu-id="18f8c-105">Der **/WX** -Schalter weist den Mittelwert Compiler an, alle Fehler auf der angegebenen Warnstufe als Fehler zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="18f8c-105">The **/WX** switch instructs the MIDL compiler to handle all errors at the given warning level as errors.</span></span>

``` syntax
midl /WX
```

## <a name="switch-options"></a><span data-ttu-id="18f8c-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="18f8c-106">Switch Options</span></span>

<span data-ttu-id="18f8c-107">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="18f8c-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="18f8c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18f8c-108">Remarks</span></span>

<span data-ttu-id="18f8c-109">Wenn der Schalter **/WX** angegeben wird und der Schalter [**/W**](-w.md)*n* nicht angegeben ist, werden alle Warnungen auf der Standard Ebene Ebene 1 als Fehler behandelt.</span><span class="sxs-lookup"><span data-stu-id="18f8c-109">If the **/WX** switch is specified and the [**/W**](-w.md)*n* switch is not specified, all warnings at the default level, level 1, are treated as errors.</span></span>

<span data-ttu-id="18f8c-110">Der Schalter [**/W**](-w.md)*n* weist den Compiler an, alle Warnungen auf der Ebene *n* anzuzeigen, und **/WX** weist den Compiler an, alle Warnungen als Fehler zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="18f8c-110">The [**/W**](-w.md)*n* switch directs the compiler to display all warnings at level *n* and **/WX** directs the compiler to handle all warnings as errors.</span></span> <span data-ttu-id="18f8c-111">Die Kombination dieser beiden Switches bewirkt, dass der Compiler alle Warnungen auf Ebene *n* als Fehler behandelt.</span><span class="sxs-lookup"><span data-stu-id="18f8c-111">The combination of these two switches directs the compiler to handle all warnings at level *n* as errors.</span></span>

<span data-ttu-id="18f8c-112">Fehler unterscheiden sich von Warnungen.</span><span class="sxs-lookup"><span data-stu-id="18f8c-112">Errors are different from warnings.</span></span> <span data-ttu-id="18f8c-113">Fehler bewirken, dass der Mittell-Compiler die Verarbeitung der IDL-Datei stoppt.</span><span class="sxs-lookup"><span data-stu-id="18f8c-113">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="18f8c-114">Warnungen bewirken, dass der Mittell-Compiler eine Informations Meldung ausgibt und die Verarbeitung der IDL-Datei fortsetzt.</span><span class="sxs-lookup"><span data-stu-id="18f8c-114">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="18f8c-115">Warning-Level NULL (0) weist den Mittelwert Compiler an, Warn Informationen zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="18f8c-115">Warning-level zero (0) directs the MIDL compiler to suppress warning information.</span></span> <span data-ttu-id="18f8c-116">Wenn die Schalter **/W0** und **/WX** kombiniert werden, unterdrückt der kompil-Compiler alle Warn Informationen.</span><span class="sxs-lookup"><span data-stu-id="18f8c-116">When the **/W0** and **/WX** switches are combined, the MIDL compiler suppresses all warning information.</span></span> <span data-ttu-id="18f8c-117">In diesem Fall hat der Schalter **/WX** keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="18f8c-117">In this case, the **/WX** switch has no effect.</span></span>

## <a name="examples"></a><span data-ttu-id="18f8c-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18f8c-118">Examples</span></span>

<span data-ttu-id="18f8c-119">**Mittel l/WX Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="18f8c-119">**midl /WX filename.idl**</span></span>

<span data-ttu-id="18f8c-120">**Mittel l/w3/WX filename. idl**</span><span class="sxs-lookup"><span data-stu-id="18f8c-120">**midl /W3 /WX filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="18f8c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18f8c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18f8c-122">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="18f8c-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="18f8c-123">**/W**</span><span class="sxs-lookup"><span data-stu-id="18f8c-123">**/W**</span></span>](-w.md)
</dt> </dl>

 

 




