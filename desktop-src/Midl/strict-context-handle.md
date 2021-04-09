---
title: strict_context_handle-Attribut
description: Das Attribut \ Strict \_ context \_ handle \ ACF legt Einschränkungen für Kontext Handles fest.
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- strict_context_handle Attribut-Mittel l
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e66fd0754ec82de2354983e10e23ffc6329569
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948615"
---
# <a name="strict_context_handle-attribute"></a><span data-ttu-id="cd724-104">Strict- \_ Kontext \_ handle-Attribut</span><span class="sxs-lookup"><span data-stu-id="cd724-104">strict\_context\_handle attribute</span></span>

<span data-ttu-id="cd724-105">Das **\[ strikte \_ Kontext \_ handle \]** -ACF-Attribut legt Einschränkungen für Kontext Handles fest.</span><span class="sxs-lookup"><span data-stu-id="cd724-105">The **\[strict\_context\_handle\]** ACF attribute sets restrictions on context handles.</span></span>

``` syntax
[ 
    strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="cd724-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd724-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd724-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="cd724-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="cd724-108">Andere ACF-Attribute, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd724-108">Other ACF attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="cd724-109">Gültige Attribute sind [**Auto \_ handle**](auto-handle.md), [**implizites \_**](implicit-handle.md)handle, [**explizites \_ handle**](explicit-handle.md)und [**Optimierung**](optimize.md), [**Code**](code.md)oder [**NoCode**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="cd724-109">Valid attributes include [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), [**explicit\_handle**](explicit-handle.md), and [**optimize**](optimize.md), [**code**](code.md), or [**nocode**](nocode.md).</span></span> <span data-ttu-id="cd724-110">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="cd724-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="cd724-111">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="cd724-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="cd724-112">Der Name der Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cd724-112">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="cd724-113">*Interface-Definition-Anweisungen*</span><span class="sxs-lookup"><span data-stu-id="cd724-113">*interface-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="cd724-114">Eine oder mehrere-Mittell-Anweisungen, die die Elemente der- [**Schnittstelle**](interface.md)definieren.</span><span class="sxs-lookup"><span data-stu-id="cd724-114">One or more MIDL statements that define the elements of the [**interface**](interface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd724-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd724-115">Remarks</span></span>

<span data-ttu-id="cd724-116">Normalerweise wird das Handle, wenn ein-Befehl an eine Schnittstellen Methode ein Kontext Handle generiert, für jede andere Schnittstelle frei verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cd724-116">Normally, when a call to an interface method generates a context handle, that handle becomes freely available to any other interface.</span></span> <span data-ttu-id="cd724-117">Wenn Sie das **\[ strikte \_ Kontext \_ handle \]** -Attribut verwenden, gewährleisten Sie, dass die Methoden in dieser Schnittstelle nur Kontext Handles akzeptieren, die von einer Methode von derselben Schnittstelle erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="cd724-117">When you use the **\[strict\_context\_handle\]** attribute you guarantee that the methods in that interface will only accept context handles that were created by a method from the same interface.</span></span> <span data-ttu-id="cd724-118">Schnittstellen, die ohne **\[ Strict- \_ Kontext \_ handle \]** kompiliert werden, können keine Kontext Handles akzeptieren, die für Schnittstellen **\[ \_ \_ \]** erstellt werden</span><span class="sxs-lookup"><span data-stu-id="cd724-118">Interfaces compiled without **\[strict\_context\_handle\]** cannot accept context handles created on interfaces compiled with **\[strict\_context\_handle\]**.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd724-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd724-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd724-120">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="cd724-120">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="cd724-121">**Ordnung**</span><span class="sxs-lookup"><span data-stu-id="cd724-121">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="cd724-122">Kontext Handles</span><span class="sxs-lookup"><span data-stu-id="cd724-122">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="cd724-123">**Kontext \_ handle- \_ Serialisierung**</span><span class="sxs-lookup"><span data-stu-id="cd724-123">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="cd724-124">**Kontext \_ handle \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="cd724-124">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="cd724-125">**explizites \_ handle**</span><span class="sxs-lookup"><span data-stu-id="cd724-125">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="cd724-126">**implizites \_ handle**</span><span class="sxs-lookup"><span data-stu-id="cd724-126">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="cd724-127">**NoCode**</span><span class="sxs-lookup"><span data-stu-id="cd724-127">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="cd724-128">**optimiert**</span><span class="sxs-lookup"><span data-stu-id="cd724-128">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="cd724-129">Typ \_ Strict- \_ Kontext \_ handle</span><span class="sxs-lookup"><span data-stu-id="cd724-129">type\_strict\_context\_handle</span></span>](type-strict-context-handle.md)
</dt> </dl>

 

 