---
title: /sal_local Schalter
description: Der \_ lokale Switch/SAL leitet die mittlere Anmerkung für Parameter von Schnittstellen Methoden, die als "\ local \" gekennzeichnet sind. Der Schalter/SAL muss ebenfalls vorhanden sein.
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /sal_local-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03263b94b809407d1c3e55c2f3dacc5e10684bc1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341487"
---
# <a name="sal_local-switch"></a><span data-ttu-id="59ca4-105">/SAL \_ lokaler Switch</span><span class="sxs-lookup"><span data-stu-id="59ca4-105">/sal\_local switch</span></span>

<span data-ttu-id="59ca4-106">Der **\_ lokale Switch/SAL** leitet die mittlere Anmerkung für Parameter von Schnittstellen Methoden, die als [**\[ \] local**](local.md)gekennzeichnet sind</span><span class="sxs-lookup"><span data-stu-id="59ca4-106">The **/sal\_local** switch directs MIDL to also generate SAL annotations for parameters of interface methods marked [**\[local\]**](local.md).</span></span> <span data-ttu-id="59ca4-107">Der Schalter [**/SAL**](-sal.md) muss ebenfalls vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="59ca4-107">The [**/sal**](-sal.md) switch must also be present.</span></span>

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a><span data-ttu-id="59ca4-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="59ca4-108">Switch Options</span></span>

<span data-ttu-id="59ca4-109">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="59ca4-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="59ca4-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59ca4-110">Remarks</span></span>

<span data-ttu-id="59ca4-111">Ändert das Verhalten des [**/SAL**](-sal.md) -Schalters, damit auch Anmerkungen zu den Parametern von Schnittstellen Methoden bereitgestellt werden, die mit dem [**\[ lokalen \]**](local.md) -Attribut gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="59ca4-111">Modifies the behavior of the [**/sal**](-sal.md) switch to also provide annotations on the parameters of interface methods marked with the [**\[local\]**](local.md) attribute.</span></span> <span data-ttu-id="59ca4-112">Verwenden Sie das [**\[ kommentieren \]**](annotate.md)-Attribut, um die mit der Mitte generierte Anmerkung mit einer anderen Anmerkung der Anmerkung zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="59ca4-112">Use the [**\[annotate\]**](annotate.md)attribute to override the MIDL-generated annotation with a different annotation string.</span></span>

## <a name="see-also"></a><span data-ttu-id="59ca4-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59ca4-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ca4-114">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="59ca4-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="59ca4-115">**/sal**</span><span class="sxs-lookup"><span data-stu-id="59ca4-115">**/sal**</span></span>](-sal.md)
</dt> <dt>

<span data-ttu-id="59ca4-116">[**\[kommentieren\]**](annotate.md)</span><span class="sxs-lookup"><span data-stu-id="59ca4-116">[**\[annotate\]**](annotate.md)</span></span>
</dt> </dl>

 

 




