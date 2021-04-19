---
title: D1115-Enumerationswert ist ungültig.
description: D1115-Enumerationswert ist ungültig.
ms.assetid: cfffd2b8-a7d3-4a60-8586-81d8435936a6
keywords:
- D1115-Enumerationswert ungültig Direct2D
topic_type:
- apiref
api_name:
- D1115 Enumeration Value Not Valid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edcfe70c67e61a3b8bfc435adfdaa017a1c62b22
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2021
ms.locfileid: "106360469"
---
# <a name="d1115-enumeration-value-not-valid"></a><span data-ttu-id="a75b2-104">D1115: der Enumerationswert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a75b2-104">D1115: Enumeration Value Not Valid</span></span>

<span data-ttu-id="a75b2-105">Der Parameter Parameter mit dem Wert "Value" für die " \[  \] \[  \] *Interface*::*method* " ist kein gültiger Enumerationswert.</span><span class="sxs-lookup"><span data-stu-id="a75b2-105">The parameter \[*parameter*\] with value \[*value*\] for *interface*::*method* is not a valid enumeration value.</span></span>

## <a name="placeholders"></a><span data-ttu-id="a75b2-106">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="a75b2-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="a75b2-107"><span id="parameter"></span><span id="PARAMETER"></span>*Parame*</span><span class="sxs-lookup"><span data-stu-id="a75b2-107"><span id="parameter"></span><span id="PARAMETER"></span>*parameter*</span></span>
</dt> <dd>

<span data-ttu-id="a75b2-108">Der Name des Parameters, der den unerwarteten Typ empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="a75b2-108">The name of the parameter that received the unexpected type.</span></span>

</dd> <dt>

<span data-ttu-id="a75b2-109"><span id="value"></span><span id="VALUE"></span>*Wert*</span><span class="sxs-lookup"><span data-stu-id="a75b2-109"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="a75b2-110">Der ungültige Enumerationswert.</span><span class="sxs-lookup"><span data-stu-id="a75b2-110">The invalid enumeration value.</span></span>

</dd> <dt>

<span data-ttu-id="a75b2-111"><span id="interface"></span><span id="INTERFACE"></span>*berfläche*</span><span class="sxs-lookup"><span data-stu-id="a75b2-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="a75b2-112">Der Name der Schnittstelle, zu der die *Methode* gehört.</span><span class="sxs-lookup"><span data-stu-id="a75b2-112">The name of the interface to which the *method* belongs.</span></span>

</dd> <dt>

<span data-ttu-id="a75b2-113"><span id="method"></span><span id="METHOD"></span>*anzuwenden*</span><span class="sxs-lookup"><span data-stu-id="a75b2-113"><span id="method"></span><span id="METHOD"></span>*method*</span></span>
</dt> <dd>

<span data-ttu-id="a75b2-114">Der Name der Methode, die den ungültigen Enumerationswert empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="a75b2-114">The name of the method that received the invalid enumeration value.</span></span>

</dd> </dl> 




 

## <a name="examples"></a><span data-ttu-id="a75b2-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a75b2-115">Examples</span></span>

<span data-ttu-id="a75b2-116">Im folgenden Beispiel wird der Enumerationswert " [**D2D1 \_ Rendering \_ Target \_ Type**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) " von 30 angegeben, der außerhalb des erwarteten Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="a75b2-116">The following example specifies a [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) enumeration value of 30, which is outside the expected range.</span></span>


```C++
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties((D2D1_RENDER_TARGET_TYPE)(30)),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



<span data-ttu-id="a75b2-117">Dieses Beispiel erzeugt die folgende Debugmeldung:</span><span class="sxs-lookup"><span data-stu-id="a75b2-117">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG ERROR - The parameter [renderTargetProperties->type] with value [30] 
for ID2D1Factory::CreateHwndRenderTarget is not a valid enumeration value.
```

## <a name="possible-causes"></a><span data-ttu-id="a75b2-118">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="a75b2-118">Possible Causes</span></span>

<span data-ttu-id="a75b2-119">Ein Parameter hat einen ungültigen Enumerationswert verwendet.</span><span class="sxs-lookup"><span data-stu-id="a75b2-119">A parameter used an invalid enumeration value.</span></span>

## <a name="fixes"></a><span data-ttu-id="a75b2-120">Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="a75b2-120">Fixes</span></span>

<span data-ttu-id="a75b2-121">Verwenden Sie einen gültigen-Enumerationswert.</span><span class="sxs-lookup"><span data-stu-id="a75b2-121">Use a valid enumeration value.</span></span>

> [!Note]  
> <span data-ttu-id="a75b2-122">Die debugschicht überprüft derzeit nur die einzelnen Enumerationswerte. Es wird nicht überprüft, ob eine bitweise Kombination gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a75b2-122">The debug layer currently checks only the individual enumeration values; it does not check whether a bitwise combination is valid.</span></span>

 

 

 
