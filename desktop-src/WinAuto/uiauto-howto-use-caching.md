---
title: Verwenden der Zwischenspeicherung
description: Dieses Thema enthält Beispielcode, der zeigt, wie die Zwischenspeicherungsfunktionen (oder das Massenabrufen) von Microsoft Benutzeroberflächenautomatisierung werden.
ms.assetid: d72fa637-35ca-4c28-922d-263f469cb1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a020f200384f88e1e4f06f9418676e8fc567851424ed03b1c36e2e6299f98e45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133253"
---
# <a name="how-to-use-caching"></a>Verwenden der Zwischenspeicherung

Dieses Thema enthält Beispielcode, der zeigt, wie die Zwischenspeicherungsfunktionen (oder das Massenabrufen) von Microsoft Benutzeroberflächenautomatisierung werden. Es werden die folgenden Themen erläutert:

-   [Abrufen von Eigenschaften und Steuerelementmustern in den Cache](#fetching-properties-and-control-patterns-into-the-cache)
-   [Abrufen von Eigenschaften und Steuerelementmustern aus dem Cache](#retrieving-properties-and-control-patterns-from-the-cache)
-   [Zugehörige Themen](#related-topics)

## <a name="fetching-properties-and-control-patterns-into-the-cache"></a>Abrufen von Eigenschaften und Steuerelementmustern in den Cache

Das folgende Codebeispiel zeigt eine Funktion, die Elemente aus einem Listensteuerelement abruft und das SelectionItem-Steuerelementmuster und die Name-Eigenschaft für jedes Element zwischenspeichert. Standardmäßig werden die Listenelemente mit einem vollständigen Verweis zurückgegeben, sodass alle aktuellen Eigenschaften weiterhin verfügbar sind.


```C++
// Given a list element, caches a control pattern and a property for
// all the list items.
IUIAutomationElementArray* FindAndCacheListItems(IUIAutomationElement* pList)
{
    if (pList == NULL)
        return NULL;
    
    IUIAutomationCondition* pCondition = NULL;
    IUIAutomationCacheRequest* pCacheRequest = NULL;
    IUIAutomationElementArray* pFound = NULL;

    HRESULT hr = g_pAutomation->CreateTrueCondition(&pCondition);
    if (FAILED(hr))
        goto cleanup;

    hr = g_pAutomation->CreateCacheRequest(&pCacheRequest);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddPattern(UIA_SelectionItemPatternId);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddProperty(UIA_NamePropertyId);
    if (FAILED(hr))
        goto cleanup;

    pList->FindAllBuildCache(TreeScope_Children, pCondition, pCacheRequest, &pFound);
    
cleanup:
    if (pCondition != NULL)
        pCondition->Release();

    if (pCacheRequest != NULL)
        pCacheRequest->Release();

    return pFound;
}
```



## <a name="retrieving-properties-and-control-patterns-from-the-cache"></a>Abrufen von Eigenschaften und Steuerelementmustern aus dem Cache

Der folgende Code veranschaulicht, wie Eigenschaften und Steuerelementmuster aus dem Cache abgerufen werden. Sie ruft das SelectionItem-Steuerelementmuster und die Name-Eigenschaft für ein Listenelement ab.


```C++
// Demonstrates retrieval of cached properties from a list item
// obtained in FindAndCacheListItems.
HRESULT GetCachedListItem(IUIAutomationElement* pItem)
{           
    if (pItem == NULL)
    {
        return E_INVALIDARG;
    }

    IUIAutomationSelectionItemPattern* pSelectionItemPattern;
    HRESULT hr = pItem->GetCachedPatternAs(UIA_SelectionItemPatternId, 
        IID_IUIAutomationSelectionItemPattern, (void**)&pSelectionItemPattern);
    if (pSelectionItemPattern != NULL)
    {
        // ... To do: Do something with the pattern.

        pSelectionItemPattern->Release();
    }

    // Retrieve a cached property.
    BSTR bstrName;
    hr = pItem->get_CachedName(&bstrName);
    if (SUCCEEDED(hr))
    {
        // ... To do: Do something with the property.

        // Clean up when done with name.
        SysFreeString(bstrName);
        bstrName = NULL;
    }

    BOOL isControl;

    // The following returns E_INVALIDARG because the property was not cached.
    // hr = pItem->get_CachedIsControlElement(&isControl);

    // The following is valid because we have a full reference to the object, therefore
    // we can get current properties. If the cache request had been made with 
    // AutomationElementMode_None, no current properties would be available from
    // this IUIAutomationElement.
    hr = pItem->get_CurrentIsControlElement(&isControl);
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Zwischenspeichern Benutzeroberflächenautomatisierung Eigenschaften und Steuerelementmustern](uiauto-cachingforclients.md)
</dt> <dt>

[How-To Topics for Benutzeroberflächenautomatisierung Clients (Themen zur Benutzeroberflächenautomatisierung Clients)](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




