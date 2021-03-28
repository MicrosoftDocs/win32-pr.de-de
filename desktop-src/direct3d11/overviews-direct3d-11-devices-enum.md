---
title: Auflisten von Adaptern
description: In diesem Thema wird gezeigt, wie die Microsoft DirectX Graphics Infrastructure (DXGI) zum Auflisten der verfügbaren Grafikadapter auf einem Computer verwendet wird.
ms.assetid: f8ef981c-363e-4ac8-8734-69c68f346950
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af16aba0131d93a5f72732931a68f132126b5d48
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993479"
---
# <a name="how-to-enumerate-adapters"></a><span data-ttu-id="42750-103">Gewusst wie: Aufzählen von Adaptern</span><span class="sxs-lookup"><span data-stu-id="42750-103">How To: Enumerate Adapters</span></span>

<span data-ttu-id="42750-104">In diesem Thema wird gezeigt, wie die Microsoft DirectX Graphics Infrastructure (DXGI) zum Auflisten der verfügbaren Grafikadapter auf einem Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="42750-104">This topic shows how to use Microsoft DirectX Graphics Infrastructure (DXGI) to enumerate the available graphics adapters on a computer.</span></span> <span data-ttu-id="42750-105">Direct3D 10 und 11 können DXGI zum Auflisten von Adaptern verwenden.</span><span class="sxs-lookup"><span data-stu-id="42750-105">Direct3D 10 and 11 can use DXGI to enumerate adapters.</span></span>

<span data-ttu-id="42750-106">In der Regel müssen Sie Adapter aus folgenden Gründen auflisten:</span><span class="sxs-lookup"><span data-stu-id="42750-106">You generally need to enumerate adapters for these reasons:</span></span>

-   <span data-ttu-id="42750-107">So bestimmen Sie, wie viele Grafikkarten auf einem Computer installiert sind</span><span class="sxs-lookup"><span data-stu-id="42750-107">To determine how many graphics adapters are installed on a computer.</span></span>
-   <span data-ttu-id="42750-108">Die Auswahl des Adapters, der zum Erstellen eines Direct3D-Geräts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="42750-108">To help you choose which adapter to use to create a Direct3D device.</span></span>
-   <span data-ttu-id="42750-109">Zum Abrufen eines [**idxgiadapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) -Objekts, das Sie zum Abrufen von Gerätefunktionen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="42750-109">To retrieve an [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) object that you can use to retrieve device capabilities.</span></span>

<span data-ttu-id="42750-110">**So zählen Sie Adapter auf**</span><span class="sxs-lookup"><span data-stu-id="42750-110">**To enumerate adapters**</span></span>

1.  <span data-ttu-id="42750-111">Erstellen Sie ein [**idxgifactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) -Objekt, indem Sie die [**createdxgifactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="42750-111">Create an [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) object by calling the [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) function.</span></span> <span data-ttu-id="42750-112">Im folgenden Codebeispiel wird veranschaulicht, wie ein **idxgifactory** -Objekt initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="42750-112">The following code example demonstrates how to initialize an **IDXGIFactory** object.</span></span>
    ```
    IDXGIFactory * pFactory = NULL;

    CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)
    ```

    

2.  <span data-ttu-id="42750-113">Durch Aufrufen der [**idxgifactory:: enumadapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) -Methode durchlaufen Sie jeden Adapter.</span><span class="sxs-lookup"><span data-stu-id="42750-113">Enumerate through each adapter by calling the [**IDXGIFactory::EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) method.</span></span> <span data-ttu-id="42750-114">Der *Adapter* Parameter ermöglicht es Ihnen, eine Null basierte Indexnummer des Adapters anzugeben, der aufgelistet werden soll.</span><span class="sxs-lookup"><span data-stu-id="42750-114">The *Adapter* parameter allows you to specify a zero-based index number of the adapter to enumerate.</span></span> <span data-ttu-id="42750-115">Wenn am angegebenen Index kein Adapter verfügbar ist, gibt die Methode den [**DXGI- \_ Fehler \_ nicht \_ gefunden**](/windows/desktop/direct3ddxgi/dxgi-error)zurück.</span><span class="sxs-lookup"><span data-stu-id="42750-115">If no adapter is available at the specified index, the method returns [**DXGI\_ERROR\_NOT\_FOUND**](/windows/desktop/direct3ddxgi/dxgi-error).</span></span>

    <span data-ttu-id="42750-116">Im folgenden Codebeispiel wird veranschaulicht, wie die Adapter auf einem Computer aufgezählt werden.</span><span class="sxs-lookup"><span data-stu-id="42750-116">The following code example demonstrates how to enumerate through the adapters on a computer.</span></span>

    ```
    for (UINT i = 0; 
         pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND; 
         ++i) 
    { ... }
    ```

    

<span data-ttu-id="42750-117">Im folgenden Codebeispiel wird veranschaulicht, wie alle Adapter auf einem Computer aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="42750-117">The following code example demonstrates how to enumerate all adapters on a computer.</span></span>

> [!Note]  
> <span data-ttu-id="42750-118">Für Direct3D 11,0 und höher wird empfohlen, dass apps stattdessen immer [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) und [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) verwenden.</span><span class="sxs-lookup"><span data-stu-id="42750-118">For Direct3D 11.0 and later, we recommend that apps always use [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) and [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) instead.</span></span>

 


```C++
std::vector <IDXGIAdapter*> EnumerateAdapters(void)
{
    IDXGIAdapter * pAdapter; 
    std::vector <IDXGIAdapter*> vAdapters; 
    IDXGIFactory* pFactory = NULL; 
    

    // Create a DXGIFactory object.
    if(FAILED(CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)))
    {
        return vAdapters;
    }


    for ( UINT i = 0;
          pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND;
          ++i )
    {
        vAdapters.push_back(pAdapter); 
    } 


    if(pFactory)
    {
        pFactory->Release();
    }

    return vAdapters;

}
```



## <a name="related-topics"></a><span data-ttu-id="42750-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="42750-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42750-120">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="42750-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 