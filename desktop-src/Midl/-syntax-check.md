---
title: /syntax_check Schalter
description: Der \_ Schalter/Syntax Check gibt an, dass der Compiler nur die Syntax prüft und keine Ausgabedateien generiert.
ms.assetid: 8d9139d3-6018-48a7-bea5-0c843b6273d3
keywords:
- /syntax_check-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /syntax_check
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b064a096b5064e6996ea4288c9ae9d4a798c2e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718479"
---
# <a name="syntax_check-switch"></a><span data-ttu-id="b4ca7-104">/Syntax \_ aktivieren</span><span class="sxs-lookup"><span data-stu-id="b4ca7-104">/syntax\_check switch</span></span>

<span data-ttu-id="b4ca7-105">Der Schalter **/Syntax \_ Check** gibt an, dass der Compiler nur die Syntax prüft und keine Ausgabedateien generiert.</span><span class="sxs-lookup"><span data-stu-id="b4ca7-105">The **/syntax\_check** switch indicates that the compiler checks only syntax and does not generate output files.</span></span>

``` syntax
midl /syntax_check
midl /Zs
```

## <a name="switch-options"></a><span data-ttu-id="b4ca7-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="b4ca7-106">Switch Options</span></span>

<span data-ttu-id="b4ca7-107">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b4ca7-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4ca7-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4ca7-108">Remarks</span></span>

<span data-ttu-id="b4ca7-109">Dieser Schalter überschreibt alle anderen Switches, die Informationen zu Ausgabedateien angeben.</span><span class="sxs-lookup"><span data-stu-id="b4ca7-109">This switch overrides all other switches that specify information about output files.</span></span>

<span data-ttu-id="b4ca7-110">Sie können auch den Syntax Überprüfungs Modus mit der [**/ZS**](-zs.md)-Compileroption angeben.</span><span class="sxs-lookup"><span data-stu-id="b4ca7-110">You can also specify syntax-checking mode with the MIDL compiler option [**/Zs**](-zs.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b4ca7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4ca7-111">Examples</span></span>

<span data-ttu-id="b4ca7-112">**Mittel l/ZS Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="b4ca7-112">**midl /Zs filename.idl**</span></span>

<span data-ttu-id="b4ca7-113">**Mittel l/Syntax \_ Überprüfen von Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="b4ca7-113">**midl /syntax\_check filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="b4ca7-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4ca7-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4ca7-115">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="b4ca7-115">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="b4ca7-116">**/ZS**</span><span class="sxs-lookup"><span data-stu-id="b4ca7-116">**/Zs**</span></span>](-zs.md)
</dt> </dl>

 

 




