---
title: D1114 nicht optionaler Zeiger NULL
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: 'Der-Parameter für die Interface:: method ist nicht optional. Ein NULL-Zeiger wurde übermittelt. Dadurch stürzt Direct2D ab.'
keywords:
- D1114 nicht optionaler Zeiger NULL Direct2D
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: abf8f070e339f2dcda5f818f5ffd5386c33d0e29
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2021
ms.locfileid: "106368698"
---
# <a name="d1114-non-optional-pointer-null"></a><span data-ttu-id="65f11-106">D1114: nicht optionaler Zeiger NULL</span><span class="sxs-lookup"><span data-stu-id="65f11-106">D1114: Non Optional Pointer NULL</span></span>

<span data-ttu-id="65f11-107">Der Parameter \[ *Parameter* \] für die *Interface*::*method* ist nicht optional.</span><span class="sxs-lookup"><span data-stu-id="65f11-107">The parameter \[*parameter*\] for *interface*::*method* is not optional.</span></span> <span data-ttu-id="65f11-108">Ein **null** -Zeiger wurde übermittelt.</span><span class="sxs-lookup"><span data-stu-id="65f11-108">A **NULL** pointer was passed.</span></span> <span data-ttu-id="65f11-109">Dadurch stürzt Direct2D ab.</span><span class="sxs-lookup"><span data-stu-id="65f11-109">This will cause Direct2D to crash.</span></span>

### <a name="placeholders"></a><span data-ttu-id="65f11-110">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="65f11-110">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="65f11-111"><span id="parameter"></span><span id="PARAMETER"></span>*Parame*</span><span class="sxs-lookup"><span data-stu-id="65f11-111"><span id="parameter"></span><span id="PARAMETER"></span>*parameter*</span></span>
</dt> <dd>

<span data-ttu-id="65f11-112">Der Name des Parameters, der den **null** -Zeiger enthält.</span><span class="sxs-lookup"><span data-stu-id="65f11-112">The name of the parameter that contains the **NULL** pointer.</span></span>

</dd> <dt>

<span data-ttu-id="65f11-113"><span id="interface"></span><span id="INTERFACE"></span>*berfläche*</span><span class="sxs-lookup"><span data-stu-id="65f11-113"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="65f11-114">Der Name der Schnittstelle, zu der die *Methode* gehört.</span><span class="sxs-lookup"><span data-stu-id="65f11-114">The name of the interface to which the *method* belongs.</span></span>

</dd> <dt>

<span data-ttu-id="65f11-115"><span id="method"></span><span id="METHOD"></span>*anzuwenden*</span><span class="sxs-lookup"><span data-stu-id="65f11-115"><span id="method"></span><span id="METHOD"></span>*method*</span></span>
</dt> <dd>

<span data-ttu-id="65f11-116">Der Name der Methode, die den ungültigen Parameter empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="65f11-116">The name of the method that received the invalid parameter.</span></span>

</dd> </dl> 




 

### <a name="examples"></a><span data-ttu-id="65f11-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65f11-117">Examples</span></span>

<span data-ttu-id="65f11-118">Das folgende Beispiel zeigt, dass die [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode einen NULL-Zeiger für den nicht optionalen *Geometry* -Parameter erhält.</span><span class="sxs-lookup"><span data-stu-id="65f11-118">The following example shows that the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method receives a NULL pointer for the non-optional *geometry* parameter.</span></span>


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



<span data-ttu-id="65f11-119">Dieses Beispiel erzeugt die folgende Debugmeldung:</span><span class="sxs-lookup"><span data-stu-id="65f11-119">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a><span data-ttu-id="65f11-120">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="65f11-120">Possible Causes</span></span>

<span data-ttu-id="65f11-121">Ein NULL-Zeiger wurde für einen nicht optionalen Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="65f11-121">A NULL pointer was passed for a non-optional parameter.</span></span>

## <a name="fixes"></a><span data-ttu-id="65f11-122">Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="65f11-122">Fixes</span></span>

<span data-ttu-id="65f11-123">Stellen Sie sicher, dass ein nicht optionaler Parameter keinen NULL-Zeiger hat.</span><span class="sxs-lookup"><span data-stu-id="65f11-123">Ensure that a non-optional parameter does not have a NULL pointer.</span></span>

 

 
