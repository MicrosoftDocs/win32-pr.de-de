---
title: idempotente Attribute
description: Das Attribut "\ idempotent \" gibt an, dass ein Vorgang Zustandsinformationen nicht ändert und bei jeder Ausführung die gleichen Ergebnisse zurückgibt. Die mehrmalige Ausführung der Routine hat denselben Effekt wie die einmalige Ausführung.
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- idempotente Attribute-Mittell
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82364c6222f6b566ef6aacb5b71a72b49c213f5a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516220"
---
# <a name="idempotent-attribute"></a><span data-ttu-id="7ec2e-105">idempotente Attribute</span><span class="sxs-lookup"><span data-stu-id="7ec2e-105">idempotent attribute</span></span>

<span data-ttu-id="7ec2e-106">Das **\[ idempotente \]** -Attribut gibt an, dass ein Vorgang Zustandsinformationen nicht ändert und bei jeder Ausführung dieselben Ergebnisse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7ec2e-106">The **\[idempotent\]** attribute specifies that an operation does not modify state information and returns the same results each time it is performed.</span></span> <span data-ttu-id="7ec2e-107">Die mehrmalige Ausführung der Routine hat denselben Effekt wie die einmalige Ausführung.</span><span class="sxs-lookup"><span data-stu-id="7ec2e-107">Performing the routine more than once has the same effect as performing it once.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [idempotent [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="7ec2e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ec2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ec2e-109">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="7ec2e-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7ec2e-110">Gibt eine Liste von 0 (null) oder mehr IDL-Attributen an, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ec2e-110">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="7ec2e-111">Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="7ec2e-111">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="7ec2e-112">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="7ec2e-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7ec2e-113">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="7ec2e-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="7ec2e-114">*Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="7ec2e-114">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7ec2e-115">Gibt zusätzliche Attribute an, die auf die Funktion angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7ec2e-115">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="7ec2e-116">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="7ec2e-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="7ec2e-117">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="7ec2e-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="7ec2e-118">Gibt den Rückgabetyp der Funktion an.</span><span class="sxs-lookup"><span data-stu-id="7ec2e-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="7ec2e-119">*function-name*</span><span class="sxs-lookup"><span data-stu-id="7ec2e-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7ec2e-120">Gibt den Namen der Funktion an, auf die das **\[ idempotente \]** Attribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7ec2e-120">Specifies the name of the function to which the **\[idempotent\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="7ec2e-121">*params*</span><span class="sxs-lookup"><span data-stu-id="7ec2e-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="7ec2e-122">Funktionsparameter Liste.</span><span class="sxs-lookup"><span data-stu-id="7ec2e-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ec2e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ec2e-123">Remarks</span></span>

<span data-ttu-id="7ec2e-124">RPC unterstützt zwei Arten von Remote Aufruf Semantik: Aufrufe von Vorgängen mit dem **\[ idempotenten \]** Attribut und Aufrufe von Vorgängen (*idempotente* Vorgänge) ohne das **\[ idempotente \]** Attribut (*nicht idempotente* Vorgänge).</span><span class="sxs-lookup"><span data-stu-id="7ec2e-124">RPC supports two types of remote call semantics: calls to operations with the **\[idempotent\]** attribute and calls to operations (*idempotent* operations) without the **\[idempotent\]** attribute (*non-idempotent* operations).</span></span> <span data-ttu-id="7ec2e-125">Ein idempotenter Vorgang kann mehrmals durchgeführt werden, ohne dass dies nicht beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="7ec2e-125">An idempotent operation can be carried out more than once with no ill effect.</span></span> <span data-ttu-id="7ec2e-126">Umgekehrt kann ein nicht idempotenter Vorgang nicht mehr als einmal ausgeführt werden, da er entweder jedes Mal andere Ergebnisse zurückgibt oder einen bestimmten Zustand ändert.</span><span class="sxs-lookup"><span data-stu-id="7ec2e-126">Conversely, a non-idempotent operation cannot be executed more than once because it will either return different results each time or because it modifies some state.</span></span>

<span data-ttu-id="7ec2e-127">Um sicherzustellen, dass eine Prozedur automatisch erneut ausgeführt wird, wenn der Aufruf nicht abgeschlossen ist, verwenden Sie das **\[ idempotente \]** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="7ec2e-127">To ensure that a procedure is automatically re-executed if the call does not complete, use the **\[idempotent\]** attribute.</span></span> <span data-ttu-id="7ec2e-128">Wenn die Attribute " **\[ \] idempotent**", " **\[** [**Broadcast**](broadcast.md)" **\]** oder " **\[** [**vielleicht**](maybe.md) " **\]** nicht vorhanden sind, verwendet die Prozedur standardmäßig nicht idempotente Semantik.</span><span class="sxs-lookup"><span data-stu-id="7ec2e-128">If the **\[idempotent\]**, **\[**[**broadcast**](broadcast.md)**\]**, or **\[**[**maybe**](maybe.md)**\]** attributes are not present, the procedure will use non-idempotent semantics by default.</span></span> <span data-ttu-id="7ec2e-129">In diesem Fall wird der Vorgang nur einmal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ec2e-129">In this case, the operation is executed only once.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ec2e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ec2e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec2e-131">**aus**</span><span class="sxs-lookup"><span data-stu-id="7ec2e-131">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="7ec2e-132">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="7ec2e-132">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7ec2e-133">**auch**</span><span class="sxs-lookup"><span data-stu-id="7ec2e-133">**maybe**</span></span>](maybe.md)
</dt> </dl>

 

 




