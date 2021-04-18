---
title: /OS-Schalter
description: Der Schalter/OS gibt die Methode im gemischten Modus an, um Stubcode zu Mars Hallen, der zwischen Client und Server übermittelt wird.
ms.assetid: dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb
keywords:
- /OS-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /Os
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbbef54501e195c91bdcc0cec8045f2eec763820
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106340460"
---
# <a name="os-switch"></a><span data-ttu-id="4fa00-104">/OS-Schalter</span><span class="sxs-lookup"><span data-stu-id="4fa00-104">/Os switch</span></span>

<span data-ttu-id="4fa00-105">Der Schalter **/OS** gibt die Methode im gemischten Modus an, um Stubcode zu Mars Hallen, der zwischen Client und Server übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="4fa00-105">The **/Os** switch specifies the mixed-mode method to marshal stub code passed between client and server.</span></span>

``` syntax
midl /Os
```

## <a name="switch-options"></a><span data-ttu-id="4fa00-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="4fa00-106">Switch Options</span></span>

<span data-ttu-id="4fa00-107">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4fa00-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fa00-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fa00-108">Remarks</span></span>

<span data-ttu-id="4fa00-109">Es gibt wichtige Punkte, die Sie berücksichtigen sollten, bevor Sie sich für die Methode zum Marshalling von Code entscheiden.</span><span class="sxs-lookup"><span data-stu-id="4fa00-109">There are important issues to consider before deciding on the method for marshaling code.</span></span> <span data-ttu-id="4fa00-110">Diese Probleme betreffen die Größe und Leistung.</span><span class="sxs-lookup"><span data-stu-id="4fa00-110">These issues concern size and performance.</span></span> <span data-ttu-id="4fa00-111">Der mittlerer l-Compiler stellt zwei Methoden zum Mars Hallen von Code bereit: gemischter Modus (**/OS**) und vollständig interpretiert ([**/Oi**](-oi.md)).</span><span class="sxs-lookup"><span data-stu-id="4fa00-111">The MIDL compiler provides two methods for marshaling code: mixed-mode (**/Os**) and fully-interpreted ([**/Oi**](-oi.md)).</span></span> <span data-ttu-id="4fa00-112">Die vollständig interpretierte Methode Marshalls Daten vollständig offline.</span><span class="sxs-lookup"><span data-stu-id="4fa00-112">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="4fa00-113">Dadurch wird die Größe des stubcodes beträchtlich reduziert, dies führt jedoch auch zu einer geringeren Leistung.</span><span class="sxs-lookup"><span data-stu-id="4fa00-113">This reduces the size of the stub code considerably, but it also results in decreased performance.</span></span>

<span data-ttu-id="4fa00-114">Verwenden Sie den mittleren l-Standardmodus **/Oicf** /robust für alle anderen Zwecke als die Abwärtskompatibilität.</span><span class="sxs-lookup"><span data-stu-id="4fa00-114">Use MIDL default mode **/Oicf** /robust for all purposes other than backward compatibility.</span></span> <span data-ttu-id="4fa00-115">Dieser Modus ist der sichere Standardmodus des Mittel l-Compilers. jeder andere Modus sollte nur nach sorgfältiger Überlegung der Sicherheits Implikation verwendet werden, um zu erkennen, dass zukünftige Erweiterungen nur für den Standardmodus implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="4fa00-115">This mode is the secure standard mode of MIDL compiler; any other mode should be used only after careful consideration to the security implication, realizing that future extensions will only be implemented for default mode.</span></span> <span data-ttu-id="4fa00-116">Im gemischten Modus Marshalls der Compiler einige Parameter inline in den generierten stubmodus.</span><span class="sxs-lookup"><span data-stu-id="4fa00-116">In mixed mode, the compiler marshals some parameters inline in the generated stubs.</span></span> <span data-ttu-id="4fa00-117">Dies führt zwar zu einer größeren stubgröße, bietet jedoch möglicherweise eine höhere Leistung.</span><span class="sxs-lookup"><span data-stu-id="4fa00-117">While this results in larger stub size, it also may offer increased performance.</span></span>

<span data-ttu-id="4fa00-118">Die mittlere Unterstützung für mehrdimensionale Arrays und Zeiger mit mehrdimensionalen Größen ist nur im [**/Oicf**](-oi.md) -Modus enthalten.</span><span class="sxs-lookup"><span data-stu-id="4fa00-118">MIDL provides full support for multidimensional arrays and multidimensional-sized pointers only in [**/Oicf**](-oi.md) mode.</span></span> <span data-ttu-id="4fa00-119">In den Modi **/OS** und **/Oi** unterstützt der Compiler einfache Fälle, z. b. Arrays mit fester Größe.</span><span class="sxs-lookup"><span data-stu-id="4fa00-119">In **/Os** and **/Oi** modes, the compiler supports simple cases, such as fixed-size arrays.</span></span> <span data-ttu-id="4fa00-120">Die Verwendung von mehrdimensionalen Arrays im **/OS** -oder **/Oi** -Modus kann zu Parametern führen, die nicht ordnungsgemäß gemarshallt werden</span><span class="sxs-lookup"><span data-stu-id="4fa00-120">Using multidimensional arrays in **/Os** or **/Oi** modes can result in parameters that are not marshaled correctly.</span></span> <span data-ttu-id="4fa00-121">Microsoft empfiehlt die Verwendung des Befehls Zeilenschalters **/Oicf** , wenn Ihre Schnittstelle Parameter definiert, die mehrdimensionale Arrays oder Zeiger mit mehrdimensionalen Größen sind.</span><span class="sxs-lookup"><span data-stu-id="4fa00-121">Microsoft recommends that you use the **/Oicf** command line switch when your interface defines parameters that are multidimensional arrays or multidimensional-sized pointers.</span></span>

<span data-ttu-id="4fa00-122">Zum weiteren definieren der gradgradgradgradmenge in der Art und Weise, in der Daten gemarshallt werden, stellt diese RPC- \[ [](optimize.md) Version ein \]</span><span class="sxs-lookup"><span data-stu-id="4fa00-122">To further define the level of gradation in how data is marshaled, this version of RPC provides an \[[**optimize**](optimize.md)\] attribute.</span></span> <span data-ttu-id="4fa00-123">Dieses Attribut wird als ACF-Schnittstellen Attribut oder Vorgangs Attribut verwendet, um den marshallingmodus auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4fa00-123">This attribute is used as an ACF interface attribute or operation attribute to select the marshaling mode.</span></span>

## <a name="examples"></a><span data-ttu-id="4fa00-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4fa00-124">Examples</span></span>

<span data-ttu-id="4fa00-125">**Mittel l/OS Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="4fa00-125">**midl /Os filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="4fa00-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fa00-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fa00-127">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="4fa00-127">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="4fa00-128">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="4fa00-128">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="4fa00-129">**optimiert**</span><span class="sxs-lookup"><span data-stu-id="4fa00-129">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="4fa00-130">**/No \_ Format \_ Opt**</span><span class="sxs-lookup"><span data-stu-id="4fa00-130">**/no\_format\_opt**</span></span>](-no-format-opt.md)
</dt> </dl>

 

 




