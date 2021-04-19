---
title: /no_format_opt Schalter
description: Der Schalter "/No \_ Format \_ Opt" ändert die Art und Weise, in der die-Methode Typen und Prozedur Deskriptoren optimiert
ms.assetid: 721ac828-7b47-4991-8bce-f9babf6c77a8
keywords:
- /no_format_opt-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /no_format_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d6e54b963c9637c4f5a583fc9d8f44a0f2880e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341282"
---
# <a name="no_format_opt-switch"></a><span data-ttu-id="28a69-104">/No \_ Format- \_ opt-Schalter</span><span class="sxs-lookup"><span data-stu-id="28a69-104">/no\_format\_opt switch</span></span>

<span data-ttu-id="28a69-105">Der Schalter " **/No \_ Format \_ opt** " ändert die Art und Weise, in der die-Methode Typen und Prozedur Deskriptoren optimiert</span><span class="sxs-lookup"><span data-stu-id="28a69-105">The **/no\_format\_opt** switch changes the way MIDL optimizes type and procedure descriptors.</span></span>

``` syntax
midl /no_format_opt
```

## <a name="switch-options"></a><span data-ttu-id="28a69-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="28a69-106">Switch Options</span></span>

<span data-ttu-id="28a69-107">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="28a69-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="28a69-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28a69-108">Remarks</span></span>

<span data-ttu-id="28a69-109">In der Standardeinstellung beseitigt die Mittel Menge doppelte Typen-und Prozedur Deskriptoren, um die Größe des generierten stubcodes zu verringern.</span><span class="sxs-lookup"><span data-stu-id="28a69-109">By default, MIDL eliminates duplicate type and procedure descriptors in order to reduce the size of the generated stub code.</span></span> <span data-ttu-id="28a69-110">Wenn Sie den Schalter **/No \_ Format \_ opt** verwenden, wird dieses Optimierungs Verhalten deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="28a69-110">Using the **/no\_format\_opt** switch turns off this optimizing behavior.</span></span>

## <a name="examples"></a><span data-ttu-id="28a69-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28a69-111">Examples</span></span>

<span data-ttu-id="28a69-112">**Mittel l/No \_ Formatieren von \_ mylean. idl**</span><span class="sxs-lookup"><span data-stu-id="28a69-112">**midl /no\_format\_opt mylean.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="28a69-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28a69-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28a69-114">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="28a69-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="28a69-115">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="28a69-115">**/Oi**</span></span>](-oi.md)
</dt> </dl>

 

 




