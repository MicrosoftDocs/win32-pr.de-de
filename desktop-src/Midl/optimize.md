---
title: Attribut optimieren
description: Das Attribut "\ optimieren \ ACF" wird verwendet, um den Grad der Verlauf für das Marshalling von Daten zu optimieren.
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- Attribut-Mittel l optimieren
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6025c40465ecf2e8fe7a33dcda50ece07d34b9d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341272"
---
# <a name="optimize-attribute"></a><span data-ttu-id="21893-104">Attribut optimieren</span><span class="sxs-lookup"><span data-stu-id="21893-104">optimize attribute</span></span>

<span data-ttu-id="21893-105">Das ACF-Attribut "optimieren" wird verwendet, um den Grad der Verlauf für das Marshalling von Daten zu **\[ optimieren \]** .</span><span class="sxs-lookup"><span data-stu-id="21893-105">The **\[optimize\]** ACF attribute is used to fine tune the level of gradation for marshaling data.</span></span>

> [!Note]  
> <span data-ttu-id="21893-106">Dieses Schlüsselwort ist nicht mehr verwendende und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21893-106">This keyword is superceeded and should not be used.</span></span> <span data-ttu-id="21893-107">Die aktuellen Mittell-Kompilierungen sollten stattdessen [**/Oicf**](-oi.md)[**/robust**](-robust.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="21893-107">Current MIDL compilations should use [**/Oicf**](-oi.md)[**/robust**](-robust.md) instead.</span></span>

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a><span data-ttu-id="21893-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="21893-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21893-109">*Optimierung: Optionen*</span><span class="sxs-lookup"><span data-stu-id="21893-109">*optimization-options*</span></span> 
</dt> <dd>

<span data-ttu-id="21893-110">Gibt die Methode für das Mars Hallen von Daten an.</span><span class="sxs-lookup"><span data-stu-id="21893-110">Specifies the method of marshaling data.</span></span> <span data-ttu-id="21893-111">Verwenden Sie entweder "s" für das Marshalling in gemischtem Modus oder "i" für interpretiertes Marshalling.</span><span class="sxs-lookup"><span data-stu-id="21893-111">Use either "s" for mixed-mode marshaling or "i" for interpreted marshaling.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21893-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21893-112">Remarks</span></span>

<span data-ttu-id="21893-113">Diese RPC-Version bietet zwei Methoden zum Marshalling von Daten: gemischter Modus ("s") und interpretiertes ("i").</span><span class="sxs-lookup"><span data-stu-id="21893-113">This version of RPC provides two methods for marshaling data: mixed-mode ("s") and interpreted ("i").</span></span> <span data-ttu-id="21893-114">Diese Methoden entsprechen den Befehls zeilenschaltern [**/OS**](-os.md) und [**/Oi**](-oi.md) .</span><span class="sxs-lookup"><span data-stu-id="21893-114">These methods correspond to the [**/Os**](-os.md) and [**/Oi**](-oi.md) command-line switches.</span></span> <span data-ttu-id="21893-115">Die interpretierte-Methode Marshalls Daten vollständig offline.</span><span class="sxs-lookup"><span data-stu-id="21893-115">The interpreted method marshals data completely offline.</span></span> <span data-ttu-id="21893-116">Obwohl dies die Größe des Stubs erheblich verringern kann, kann die Leistung beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="21893-116">While this can reduce the size of the stub considerably, performance can be affected.</span></span>

<span data-ttu-id="21893-117">Wenn die Leistung von Bedeutung ist, kann die Methode mit gemischtem Modus die beste Vorgehensweise sein.</span><span class="sxs-lookup"><span data-stu-id="21893-117">If performance is a concern, the mixed-mode method can be the best approach.</span></span> <span data-ttu-id="21893-118">Der gemischte Modus ermöglicht es dem Mittelwert Compiler, die Bestimmung zwischen den Daten, die Inline gemarshallt werden, und die durch einen Rückruf einer Offline-Dynamic Link Library gemarshallt werden.</span><span class="sxs-lookup"><span data-stu-id="21893-118">Mixed-mode allows the MIDL compiler to make the determination between which data will be marshaled inline and which will be marshaled by a call to an offline dynamic-link library.</span></span> <span data-ttu-id="21893-119">Wenn viele Prozeduren dieselben Datentypen verwenden, kann eine einzelne Prozedur wiederholt aufgerufen werden, um die Daten zu Mars Hallen.</span><span class="sxs-lookup"><span data-stu-id="21893-119">If many procedures use the same data types, a single procedure can be called repeatedly to marshal the data.</span></span> <span data-ttu-id="21893-120">Auf diese Weise werden Daten, die am besten für das Inline Marshalling geeignet sind, Inline verarbeitet, während andere Daten effizienter im Offline Modus gemarshallt werden können.</span><span class="sxs-lookup"><span data-stu-id="21893-120">In this way, data that is most suited to inline marshaling is processed inline while other data can be more efficiently marshaled offline.</span></span>

<span data-ttu-id="21893-121">Beachten Sie, dass das Attribut " **\[ optimieren \]** " als Schnittstellen Attribut oder als Vorgangs Attribut verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="21893-121">Note that the **\[optimize\]** attribute can be used as an interface attribute or as an operation attribute.</span></span> <span data-ttu-id="21893-122">Wenn Sie als Schnittstellen Attribut verwendet wird, wird der Standardwert für die gesamte Schnittstelle festgelegt und Befehls Zeilenschalter überschrieben.</span><span class="sxs-lookup"><span data-stu-id="21893-122">If it is used as an interface attribute, it sets the default for the entire interface, overriding command-line switches.</span></span> <span data-ttu-id="21893-123">Wenn Sie jedoch als Vorgangs Attribut verwendet wird, wirkt sich dies nur auf diesen Vorgang aus, wobei Befehls Zeilenschalter und der Standard der-Schnittstelle überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="21893-123">If, however, it is used as an operation attribute, it affects only that operation, overriding command-line switches and the interface default.</span></span>

## <a name="examples"></a><span data-ttu-id="21893-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21893-124">Examples</span></span>

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a><span data-ttu-id="21893-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="21893-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21893-126">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="21893-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="21893-127">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="21893-127">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="21893-128">**/OS**</span><span class="sxs-lookup"><span data-stu-id="21893-128">**/Os**</span></span>](-os.md)
</dt> <dt>

[<span data-ttu-id="21893-129">**/robust**</span><span class="sxs-lookup"><span data-stu-id="21893-129">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




