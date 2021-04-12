---
title: type_strict_context_handle-Attribut
description: Verwenden Sie den "\ Type \_ Strict \_ context \_ handle \" in einer ACF-Datei, um Einschränkungen für Kontext Handles festzulegen.
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- type_strict_context_handle Attribut-Mittel l
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e16c9ae74d618b1b0cafef2c5bf618085d79284
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472789"
---
# <a name="type_strict_context_handle-attribute"></a><span data-ttu-id="df84e-104">Typ \_ Strict- \_ Kontext \_ handle-Attribut</span><span class="sxs-lookup"><span data-stu-id="df84e-104">type\_strict\_context\_handle attribute</span></span>

<span data-ttu-id="df84e-105">Verwenden Sie den **\[ Typ \_ Strict- \_ Kontext \_ handle \]** in einer ACF-Datei, um Einschränkungen für Kontext Handles festzulegen.</span><span class="sxs-lookup"><span data-stu-id="df84e-105">Use the **\[type\_strict\_context\_handle\]** in an ACF file to set restrictions on context handles.</span></span>

``` syntax
[ 
    type_strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="df84e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="df84e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df84e-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="df84e-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="df84e-108">Andere ACF-Attribute, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="df84e-108">Other ACF attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="df84e-109">Gültige Attribute sind [**Auto \_ handle**](auto-handle.md), [**implizites \_**](implicit-handle.md)handle, [**explizites \_ handle**](explicit-handle.md)und [**Optimierung**](optimize.md), [**Code**](code.md)oder [**NoCode**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="df84e-109">Valid attributes include [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), [**explicit\_handle**](explicit-handle.md), and [**optimize**](optimize.md), [**code**](code.md), or [**nocode**](nocode.md).</span></span> <span data-ttu-id="df84e-110">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="df84e-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="df84e-111">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="df84e-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="df84e-112">Der Name der Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="df84e-112">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="df84e-113">*Interface-Definition-Anweisungen*</span><span class="sxs-lookup"><span data-stu-id="df84e-113">*interface-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="df84e-114">Eine oder mehrere-Mittell-Anweisungen, die die Elemente der- [**Schnittstelle**](interface.md)definieren.</span><span class="sxs-lookup"><span data-stu-id="df84e-114">One or more MIDL statements that define the elements of the [**interface**](interface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df84e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df84e-115">Remarks</span></span>

<span data-ttu-id="df84e-116">Um dieses Attribut zu verwenden, muss das-Target-Flag beim Ausführen von midl.exe auf nt60 (oder höher) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="df84e-116">In order to use this attribute, the -target flag must be set to NT60 (or higher) when running midl.exe.</span></span>

<span data-ttu-id="df84e-117">\[\_der Typ Strict- \_ Kontext \_ handle \] ist eine Funktions Übermenge eines \[ strengen \_ Kontext \_ Handles \] .</span><span class="sxs-lookup"><span data-stu-id="df84e-117">\[type\_strict\_context\_handle\] is a functional superset of \[strict\_context\_handle\].</span></span> <span data-ttu-id="df84e-118">Im \[ Strict- \_ Kontext \_ handle \] ist die Typ-ID des Handles immer 0. im \[ Typ \_ Strict- \_ Kontext Handle wird \_ \] eine eindeutige Typ-ID vom Mittelwert Compiler zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="df84e-118">In \[strict\_context\_handle\], the type ID of the handle is always 0; in \[type\_strict\_context\_handle\], a unique type ID is assigned by the MIDL compiler.</span></span>

<span data-ttu-id="df84e-119">Es wird empfohlen, das \[ \_ typstrikte \_ Kontext \_ handle \] anstelle eines \[ strengen \_ Kontext \_ Handles \] zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="df84e-119">It is recommended to use \[type\_strict\_context\_handle\] rather than \[strict\_context\_handle\].</span></span> <span data-ttu-id="df84e-120">Kontext Handles sind nicht standardmäßig mit einem bestimmten Typ verknüpft.</span><span class="sxs-lookup"><span data-stu-id="df84e-120">Context handles are not associated with a specific type by default.</span></span> <span data-ttu-id="df84e-121">Wenn im gleichen Prozess mehrere Typen von Kontext Handles verwendet werden, ist es möglich, dass ein böswilliger Client ein Kontext Handle anstelle eines anderen übergibt, um unerwünschte Ergebnisse zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="df84e-121">When multiple types of context handles are used in the same process, it is possible for a malicious client to pass a context handle in place of another to produce undesirable results.</span></span> <span data-ttu-id="df84e-122">Durch die Verwendung \[ des \_ Typs \_ Strict \_ -Kontext Handle \] können Anwendungen die Konsistenz des Kontext Handles erzwingen und jede nicht übereinstimmende Kontext Handle-Typverwendung verhindern.</span><span class="sxs-lookup"><span data-stu-id="df84e-122">The use of \[type\_strict\_context\_handle\] allows applications to enforce context handle type consistency and prevent any mismatched context handle type usage.</span></span>

<span data-ttu-id="df84e-123">Ein mit dem Typ Strict-Kontext Handle attributiertes Kontext Handle \[ \_ \_ \_ \] kann nicht auch mit einem \[ Strict-Kontext Handle attributiert werden \_ \_ \] .</span><span class="sxs-lookup"><span data-stu-id="df84e-123">A context handle attributed with \[type\_strict\_context\_handle\] cannot also be attributed with \[strict\_context\_handle\].</span></span>

## <a name="see-also"></a><span data-ttu-id="df84e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df84e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df84e-125">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="df84e-125">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="df84e-126">**Ordnung**</span><span class="sxs-lookup"><span data-stu-id="df84e-126">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="df84e-127">Kontext Handles</span><span class="sxs-lookup"><span data-stu-id="df84e-127">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="df84e-128">**Kontext \_ handle- \_ Serialisierung**</span><span class="sxs-lookup"><span data-stu-id="df84e-128">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="df84e-129">**Kontext \_ handle \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="df84e-129">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="df84e-130">**explizites \_ handle**</span><span class="sxs-lookup"><span data-stu-id="df84e-130">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="df84e-131">**implizites \_ handle**</span><span class="sxs-lookup"><span data-stu-id="df84e-131">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="df84e-132">**NoCode**</span><span class="sxs-lookup"><span data-stu-id="df84e-132">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="df84e-133">**optimiert**</span><span class="sxs-lookup"><span data-stu-id="df84e-133">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="df84e-134">Strict- \_ Kontext \_ handle</span><span class="sxs-lookup"><span data-stu-id="df84e-134">strict\_context\_handle</span></span>](strict-context-handle.md)
</dt> </dl>

 

 