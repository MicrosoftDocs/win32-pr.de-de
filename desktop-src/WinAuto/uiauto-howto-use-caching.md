---
title: Verwenden der Zwischenspeicherung
description: Dieses Thema enthält Beispielcode, in dem gezeigt wird, wie die Funktionen zum Zwischenspeichern (oder Massen Abruf) der Microsoft UI Automation Tree verwendet werden.
ms.assetid: d72fa637-35ca-4c28-922d-263f469cb1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8758621a8499202b820a6ffc3459fade57c2a485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338383"
---
# <a name="how-to-use-caching"></a>Verwenden der Zwischenspeicherung

Dieses Thema enthält Beispielcode, in dem gezeigt wird, wie die Funktionen zum Zwischenspeichern (oder Massen Abruf) der Microsoft UI Automation Tree verwendet werden. In diesem Thema werden die folgenden Themen behandelt:

-   [Abrufen von Eigenschaften und Steuerelement Mustern im Cache](#fetching-properties-and-control-patterns-into-the-cache)
-   [Abrufen von Eigenschaften und Steuerelement Mustern aus dem Cache](#retrieving-properties-and-control-patterns-from-the-cache)
-   [Zugehörige Themen](#related-topics)

## <a name="fetching-properties-and-control-patterns-into-the-cache"></a>Abrufen von Eigenschaften und Steuerelement Mustern im Cache

Das folgende Codebeispiel zeigt eine Funktion, die Elemente aus einem Listen Steuerelement abruft und das SelectionItem-Steuerelement Muster und die Name-Eigenschaft für jedes Element zwischenspeichert. Standardmäßig werden die Listenelemente mit einer vollständigen Referenz zurückgegeben, sodass alle aktuellen Eigenschaften weiterhin verfügbar sind.


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



## <a name="retrieving-properties-and-control-patterns-from-the-cache"></a>Abrufen von Eigenschaften und Steuerelement Mustern aus dem Cache

Der folgende Code veranschaulicht, wie Eigenschaften und Steuerelement Muster aus dem Cache abgerufen werden. Das SelectionItem-Steuerelement Muster und die Name-Eigenschaft für ein Listenelement werden abgerufen.


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

**Licher**
</dt> <dt>

[Zwischenspeichern von Eigenschaften der Benutzeroberflächen Automatisierung und Steuerelement Mustern](uiauto-cachingforclients.md)
</dt> <dt>

[Themen zur Vorgehensweise für Benutzeroberflächenautomatisierungs-Clients](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




