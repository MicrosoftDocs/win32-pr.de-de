---
title: Abrufen eines virtualisierten Elements
description: Dieses Thema enthält Beispielcode, in dem gezeigt wird, wie Sie Benutzeroberflächen Informationen zu virtualisierten Elementen in einem-Steuerelement suchen und abrufen können.
ms.assetid: 1882b8a9-0d03-4388-a1d0-1bff0ab9fc66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae878ce25dd4d279211948ddaa6f9d0965ce9b40
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039849"
---
# <a name="how-to-retrieve-a-virtualized-item"></a><span data-ttu-id="52fef-103">Abrufen eines virtualisierten Elements</span><span class="sxs-lookup"><span data-stu-id="52fef-103">How to Retrieve a Virtualized Item</span></span>

<span data-ttu-id="52fef-104">Dieses Thema enthält Beispielcode, in dem gezeigt wird, wie Sie Benutzeroberflächen Informationen zu virtualisierten Elementen in einem-Steuerelement suchen und abrufen können.</span><span class="sxs-lookup"><span data-stu-id="52fef-104">This topic contains example code that shows how to find and retrieve UI information about virtualized items in a control.</span></span>


<span data-ttu-id="52fef-105">Im folgenden Beispiel wird ein Container nach einem Element durchsucht, das über den angegebenen Namen verfügt und die [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle für das Element abruft.</span><span class="sxs-lookup"><span data-stu-id="52fef-105">The following example searches a container for an item that has the specified name and retrieves the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface for the item.</span></span> <span data-ttu-id="52fef-106">Das Beispiel sucht zuerst in der Benutzeroberflächenautomatisierungs-Unterstruktur.</span><span class="sxs-lookup"><span data-stu-id="52fef-106">The example looks in the UI Automation subtree first.</span></span> <span data-ttu-id="52fef-107">Wenn das Element nicht vorhanden ist, wird im Beispiel die [**iuiautomationitemcontainerpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) -Container-Schnittstelle verwendet, um das Element zu suchen, und dann wird das Element mit der [**iuiautomationvirtualizeditempattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) -Schnittstelle erkannt.</span><span class="sxs-lookup"><span data-stu-id="52fef-107">If the item is not there, the example uses the container [**IUIAutomationItemContainerPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) interface to find the item, and then uses the item [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) interface to realize the item.</span></span>


```C++
HRESULT GetContainerItem (BSTR bstrItemName, IUIAutomationElement *pContainerElement, 
                          IUIAutomationElement **ppItemElement)                                  
{
    HRESULT hr;
    VARIANT varNameStr;
    IUIAutomationCondition *pNamePropertyCond = NULL;
    IUIAutomationElement *pFoundElement = NULL;
    IUIAutomationItemContainerPattern *pItemContainer = NULL;

    // Make sure the pointers are valid.
    if (ppItemElement == NULL || pContainerElement == NULL || bstrItemName == NULL)
        return E_INVALIDARG;
    
    *ppItemElement = NULL;

    // Try to find the item in the UI Automation tree. This attempt will fail if the
    // item is virtualized. Note: g_pAutomation is a global pointer to the IUIAutomation interface.
    varNameStr.vt = VT_BSTR;
    varNameStr.bstrVal = SysAllocString(bstrItemName);
    hr = g_pAutomation->CreatePropertyCondition(UIA_NamePropertyId, varNameStr, &pNamePropertyCond);
    if (pNamePropertyCond == NULL)
        goto cleanup;

    hr = pContainerElement->FindFirst(TreeScope_Subtree, pNamePropertyCond, &pFoundElement);
    if (pFoundElement == NULL) { 

        // The item is not in the UI Automation tree, so it may be virtualized. Try
        // using the ItemContainer control pattern to find the item.
        hr = pContainerElement->GetCurrentPatternAs(UIA_ItemContainerPatternId, 
                                                    __uuidof(IUIAutomationItemContainerPattern), 
                                                    (void**)&pItemContainer);
        if (pItemContainer == NULL)
            goto cleanup;

        hr = pItemContainer->FindItemByProperty(NULL, UIA_NamePropertyId, varNameStr, &pFoundElement);
        if (pFoundElement == NULL) // container has no item with the specified name
            goto cleanup;
    }

    // Attempt to get the name property. The attempt will fail with 
    // UIA_E_ELEMENTNOTAVAILABLE if the item is virtualized. 
    BSTR bstrName; 
    hr = pFoundElement->get_CurrentName(&bstrName);
    if (hr == UIA_E_ELEMENTNOTAVAILABLE) 
    {
        // The item might be virtualized. Use the VirtualizedItem control pattern to 
        // realize the item. 
        IUIAutomationVirtualizedItemPattern *pVirtualizedItem;
        hr = pFoundElement->GetCurrentPatternAs(UIA_VirtualizedItemPatternId, 
                    __uuidof(IUIAutomationVirtualizedItemPattern), (void**)&pVirtualizedItem);
        if (pVirtualizedItem == NULL)
            goto cleanup;

        hr = pVirtualizedItem->Realize();
        pVirtualizedItem->Release();

        if (hr != S_OK)
            goto cleanup;

        // Try to get the name again. 
        hr = pFoundElement->get_CurrentName(&bstrName);
    }    

    if (SUCCEEDED(hr))
    {
        // Make sure the item is the one we're looking for.
        if (wcscmp(bstrName, bstrItemName) == 0)
        {
            *ppItemElement = pFoundElement;
            pFoundElement = NULL;
        }
    }


cleanup:
        VariantClear(&varNameStr);

        if (pNamePropertyCond != NULL) pNamePropertyCond->Release();
        if (pFoundElement != NULL) pFoundElement->Release();
        if (pItemContainer != NULL) pItemContainer->Release();

        return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="52fef-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="52fef-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="52fef-109">**Licher**</span><span class="sxs-lookup"><span data-stu-id="52fef-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="52fef-110">Arbeiten mit virtualisierten Elementen</span><span class="sxs-lookup"><span data-stu-id="52fef-110">Working with Virtualized Items</span></span>](uiauto-workingwithvirtualizeditems.md)
</dt> <dt>

[<span data-ttu-id="52fef-111">Themen zur Vorgehensweise für Benutzeroberflächenautomatisierungs-Clients</span><span class="sxs-lookup"><span data-stu-id="52fef-111">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




