---
title: D1108 falsche Factory
ms.assetid: eb851118-0541-4c9a-a22d-b98f041852bb
description: Die Ressource wurde von Factory 1 zugeordnet und mit Factory 2 verwendet.
keywords:
- D1108 falsche Factory Direct2D
topic_type:
- apiref
api_name:
- D1108 Wrong Factory
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 17c58c72a56af8c480a176259d9fbcb9df586942
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2021
ms.locfileid: "106370965"
---
# <a name="d1108-wrong-factory"></a><span data-ttu-id="964f1-104">D1108: falsche Factory</span><span class="sxs-lookup"><span data-stu-id="964f1-104">D1108: Wrong Factory</span></span>

<span data-ttu-id="964f1-105">Die Ressourcen \[ *Ressource* \] wurde von Factory \[ *Factory 1* zugeordnet \] und mit Factory \[ *Factory 2* verwendet \] .</span><span class="sxs-lookup"><span data-stu-id="964f1-105">The resource \[*resource*\] was allocated by factory \[*factory 1*\] and used with factory \[*factory 2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="964f1-106">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="964f1-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="964f1-107"><span id="resource"></span><span id="RESOURCE"></span>*Ressource*</span><span class="sxs-lookup"><span data-stu-id="964f1-107"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="964f1-108">Die Adresse der-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="964f1-108">The address of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="964f1-109"><span id="factory_1"></span><span id="FACTORY_1"></span>*Factory 1*</span><span class="sxs-lookup"><span data-stu-id="964f1-109"><span id="factory_1"></span><span id="FACTORY_1"></span>*factory 1*</span></span>
</dt> <dd>

<span data-ttu-id="964f1-110">Die Adresse der Factory, die die *Ressource* zugeordnet hat.</span><span class="sxs-lookup"><span data-stu-id="964f1-110">The address of the factory that allocated *resource*.</span></span>

</dd> <dt>

<span data-ttu-id="964f1-111"><span id="factory_2"></span><span id="FACTORY_2"></span>*Factory 2*</span><span class="sxs-lookup"><span data-stu-id="964f1-111"><span id="factory_2"></span><span id="FACTORY_2"></span>*factory 2*</span></span>
</dt> <dd>

<span data-ttu-id="964f1-112">Die Adresse der Factory, mit der die *Ressource* verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="964f1-112">The address of the factory with which *resource* was used.</span></span>

</dd> </dl> 




 

## <a name="examples"></a><span data-ttu-id="964f1-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="964f1-113">Examples</span></span>

<span data-ttu-id="964f1-114">Im folgenden Beispiel werden zuerst zwei Debug-aktivierte [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Objekte erstellt. Er erstellt dann eine Geometrie aus der ersten Factory und einen Pinsel aus der zweiten Factory.</span><span class="sxs-lookup"><span data-stu-id="964f1-114">The following example first creates two debug-enabled [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) objects; it then creates a geometry from the first factory, and a brush from the second factory.</span></span> <span data-ttu-id="964f1-115">Schließlich ruft Sie [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)auf und übergibt die Geometrie und den Pinsel.</span><span class="sxs-lookup"><span data-stu-id="964f1-115">Lastly, it calls [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry), passing in the geometry and the brush.</span></span>


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif


        // Domain violation. Create a second Direct2D factory.
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory1
            );

        // Create a geometry from the second factory.
        hr = m_pD2DFactory1->CreateRectangleGeometry(
            D2D1::RectF(100, 50, 400, 160),
            &m_pRectangleGeometry
            );
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="964f1-116">C++</span><span class="sxs-lookup"><span data-stu-id="964f1-116">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        // Create a render target from the first factory.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );</code></pre></td>
</tr>
</tbody>
</table>

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="964f1-117">C++</span><span class="sxs-lookup"><span data-stu-id="964f1-117">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
                &m_pBlackBrush
                );
        }</code></pre></td>
</tr>
</tbody>
</table>

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="964f1-118">C++</span><span class="sxs-lookup"><span data-stu-id="964f1-118">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        m_pRenderTarget->FillGeometry(
            m_pRectangleGeometry,   //The rectangle geometry created from the second factory.
            m_pBlackBrush   //The black brush created from the first factory.
            );</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="964f1-119">Dieses Beispiel erzeugt die folgende Debugmeldung:</span><span class="sxs-lookup"><span data-stu-id="964f1-119">This example produces the following debug message:</span></span>


```
 D2D DEBUG ERROR - The resource [003BD628] was allocated 
by factory [002ED698] and used with factory [002ED470].
```



## <a name="possible-causes"></a><span data-ttu-id="964f1-120">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="964f1-120">Possible Causes</span></span>

<span data-ttu-id="964f1-121">Ungültige Ressourcenverwendung.</span><span class="sxs-lookup"><span data-stu-id="964f1-121">Invalid resource usage.</span></span> <span data-ttu-id="964f1-122">Eine von einer Factory zugeordnete Ressource wurde mit einer anderen Factory verwendet.</span><span class="sxs-lookup"><span data-stu-id="964f1-122">A resource allocated by one factory was used with another factory.</span></span>

 

 
