---
title: /ZS-Schalter
description: Der Schalter/ZS gibt an, dass der Compiler nur die Syntax überprüft und keine Ausgabedateien generiert.
ms.assetid: 5ff44607-12c3-4a2d-8a7f-2056504990e2
keywords:
- /ZS-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /Zs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 469802434d54319aa55c1e409ccb8d64e942836f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718162"
---
# <a name="zs-switch"></a><span data-ttu-id="f4ab5-104">/ZS-Schalter</span><span class="sxs-lookup"><span data-stu-id="f4ab5-104">/Zs switch</span></span>

<span data-ttu-id="f4ab5-105">Der Schalter **/ZS** gibt an, dass der Compiler nur die Syntax überprüft und keine Ausgabedateien generiert.</span><span class="sxs-lookup"><span data-stu-id="f4ab5-105">The **/Zs** switch indicates that the compiler only checks syntax and does not generate output files.</span></span>

``` syntax
midl /Zs
midl /syntax_check
```

## <a name="switch-options"></a><span data-ttu-id="f4ab5-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="f4ab5-106">Switch Options</span></span>

<span data-ttu-id="f4ab5-107">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f4ab5-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4ab5-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4ab5-108">Remarks</span></span>

<span data-ttu-id="f4ab5-109">Dieser Schalter überschreibt alle anderen Switches, die Informationen zu Ausgabedateien angeben.</span><span class="sxs-lookup"><span data-stu-id="f4ab5-109">This switch overrides all other switches that specify information about output files.</span></span>

<span data-ttu-id="f4ab5-110">Sie können auch den Syntax Überprüfungs Modus mit dem Mittell-Compilerschalter [**/Syntax \_ Check**](-syntax-check.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="f4ab5-110">You can also specify syntax-checking mode with the MIDL compiler switch [**/syntax\_check**](-syntax-check.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f4ab5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4ab5-111">Examples</span></span>

<span data-ttu-id="f4ab5-112">**Mittel l/ZS Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="f4ab5-112">**midl /Zs filename.idl**</span></span>

<span data-ttu-id="f4ab5-113">**Mittel l/Syntax \_ Überprüfen von Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="f4ab5-113">**midl /syntax\_check filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="f4ab5-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4ab5-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ab5-115">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="f4ab5-115">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="f4ab5-116">**/Syntax \_ überprüfen**</span><span class="sxs-lookup"><span data-stu-id="f4ab5-116">**/syntax\_check**</span></span>](-syntax-check.md)
</dt> </dl>

 

 




