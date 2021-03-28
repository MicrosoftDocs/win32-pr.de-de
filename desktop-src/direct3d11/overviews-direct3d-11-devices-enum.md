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
# <a name="how-to-enumerate-adapters"></a>Gewusst wie: Aufzählen von Adaptern

In diesem Thema wird gezeigt, wie die Microsoft DirectX Graphics Infrastructure (DXGI) zum Auflisten der verfügbaren Grafikadapter auf einem Computer verwendet wird. Direct3D 10 und 11 können DXGI zum Auflisten von Adaptern verwenden.

In der Regel müssen Sie Adapter aus folgenden Gründen auflisten:

-   So bestimmen Sie, wie viele Grafikkarten auf einem Computer installiert sind
-   Die Auswahl des Adapters, der zum Erstellen eines Direct3D-Geräts verwendet werden soll.
-   Zum Abrufen eines [**idxgiadapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) -Objekts, das Sie zum Abrufen von Gerätefunktionen verwenden können.

**So zählen Sie Adapter auf**

1.  Erstellen Sie ein [**idxgifactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) -Objekt, indem Sie die [**createdxgifactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) -Funktion aufrufen. Im folgenden Codebeispiel wird veranschaulicht, wie ein **idxgifactory** -Objekt initialisiert wird.
    ```
    IDXGIFactory * pFactory = NULL;

    CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)
    ```

    

2.  Durch Aufrufen der [**idxgifactory:: enumadapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) -Methode durchlaufen Sie jeden Adapter. Der *Adapter* Parameter ermöglicht es Ihnen, eine Null basierte Indexnummer des Adapters anzugeben, der aufgelistet werden soll. Wenn am angegebenen Index kein Adapter verfügbar ist, gibt die Methode den [**DXGI- \_ Fehler \_ nicht \_ gefunden**](/windows/desktop/direct3ddxgi/dxgi-error)zurück.

    Im folgenden Codebeispiel wird veranschaulicht, wie die Adapter auf einem Computer aufgezählt werden.

    ```
    for (UINT i = 0; 
         pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND; 
         ++i) 
    { ... }
    ```

    

Im folgenden Codebeispiel wird veranschaulicht, wie alle Adapter auf einem Computer aufgelistet werden.

> [!Note]  
> Für Direct3D 11,0 und höher wird empfohlen, dass apps stattdessen immer [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) und [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) verwenden.

 


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 