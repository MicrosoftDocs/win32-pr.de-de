---
title: Vielleicht-Attribut
description: Das Schlüsselwort \ vielleicht \ gibt an, dass der Remote Prozedur Aufruf nicht jedes Mal ausgeführt werden muss, wenn er aufgerufen wird und der Client keine Antwort erwartet. Beachten Sie, dass das \ Maybe \-Protokoll weder die Übermittlung noch den Abschluss des Aufrufens sicherstellt.
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- Vielleicht attributmittell
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68704e19d421150444933d74f6b78fc5bada46f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037818"
---
# <a name="maybe-attribute"></a><span data-ttu-id="8ba74-105">Vielleicht-Attribut</span><span class="sxs-lookup"><span data-stu-id="8ba74-105">maybe attribute</span></span>

<span data-ttu-id="8ba74-106">Das Schlüsselwort gibt **\[ möglicherweise \]** an, dass der Remote Prozedur Aufruf nicht jedes Mal ausgeführt werden muss, wenn er aufgerufen wird und der Client keine Antwort erwartet.</span><span class="sxs-lookup"><span data-stu-id="8ba74-106">The keyword **\[maybe\]** indicates that the remote procedure call does not need to execute every time it is called and the client does not expect a response.</span></span> <span data-ttu-id="8ba74-107">Beachten Sie, dass das **\[ vielleicht \]** -Protokoll weder die Übermittlung noch den Abschluss des Aufrufes ermöglicht</span><span class="sxs-lookup"><span data-stu-id="8ba74-107">Note that the **\[maybe\]** protocol ensures neither delivery nor completion of the call.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [maybe [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="8ba74-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ba74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ba74-109">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="8ba74-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8ba74-110">Gibt eine Liste von 0 (null) oder mehr IDL-Attributen an, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8ba74-110">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="8ba74-111">Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="8ba74-111">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="8ba74-112">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="8ba74-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8ba74-113">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="8ba74-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="8ba74-114">*Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="8ba74-114">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8ba74-115">Gibt zusätzliche Attribute an, die auf die Funktion angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8ba74-115">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="8ba74-116">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="8ba74-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="8ba74-117">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="8ba74-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="8ba74-118">Gibt den Rückgabetyp der Funktion an.</span><span class="sxs-lookup"><span data-stu-id="8ba74-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="8ba74-119">*function-name*</span><span class="sxs-lookup"><span data-stu-id="8ba74-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8ba74-120">Gibt den Namen der Funktion an, auf die das Attribut " **\[ vielleicht \]** " angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8ba74-120">Specifies the name of the function to which the **\[maybe\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="8ba74-121">*params*</span><span class="sxs-lookup"><span data-stu-id="8ba74-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="8ba74-122">Funktionsparameter Liste.</span><span class="sxs-lookup"><span data-stu-id="8ba74-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ba74-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ba74-123">Remarks</span></span>

<span data-ttu-id="8ba74-124">Ein Aufruf mit dem Attribut " **\[ vielleicht \]** " kann keine Ausgabeparameter enthalten und ist implizit ein **\[** [**idempotenter**](idempotent.md) **\]** Aufruf.</span><span class="sxs-lookup"><span data-stu-id="8ba74-124">A call with the **\[maybe\]** attribute cannot contain output parameters and is implicitly an **\[**[**idempotent**](idempotent.md)**\]** call.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ba74-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ba74-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba74-126">**aus**</span><span class="sxs-lookup"><span data-stu-id="8ba74-126">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="8ba74-127">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="8ba74-127">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="8ba74-128">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="8ba74-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




