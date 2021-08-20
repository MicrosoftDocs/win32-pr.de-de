---
title: D1108 Falsche Factory
ms.assetid: eb851118-0541-4c9a-a22d-b98f041852bb
description: Die Ressource wurde von Factory 1 zugeordnet und mit Factory 2 verwendet.
keywords:
- D1108 Falsche Factory Direct2D
topic_type:
- apiref
api_name:
- D1108 Wrong Factory
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: c9eeadfb38acd39e5861c5661e2f4117ef2a8ce415e3e21374f197763d4b315e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160991"
---
# <a name="d1108-wrong-factory"></a>D1108: Falsche Factory

Die \[ *Ressourcenressource* \] wurde von Factory 1 zugeordnet und mit Factory \[  \] \[ *2* \] verwendet.

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Ressource*
</dt> <dd>

Die Adresse der Schnittstelle.

</dd> <dt>

<span id="factory_1"></span><span id="FACTORY_1"></span>*Factory 1*
</dt> <dd>

Die Adresse der Factory, der die *Ressource* zugeordnet wurde.

</dd> <dt>

<span id="factory_2"></span><span id="FACTORY_2"></span>*Factory 2*
</dt> <dd>

Die Adresse der Factory, mit der die *Ressource* verwendet wurde.

</dd> </dl> 




 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel werden zunächst zwei debugfähige [**ID2D1Factory-Objekte**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) erstellt: anschließend wird eine Geometrie aus der ersten Factory und ein Pinsel aus der zweiten Factory erstellt. Schließlich ruft sie [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)auf und übergibt die Geometrie und den Pinsel.


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
<th>C++</th>
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
<th>C++</th>
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
<th>C++</th>
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



In diesem Beispiel wird die folgende Debugmeldung erzeugt:


```
 D2D DEBUG ERROR - The resource [003BD628] was allocated 
by factory [002ED698] and used with factory [002ED470].
```



## <a name="possible-causes"></a>Mögliche Ursachen

Ungültige Ressourcenverwendung. Eine von einer Factory zugeordnete Ressource wurde mit einer anderen Factory verwendet.

 

 
