---
title: Aktivieren der Navigation in einem Benutzeroberflächenautomatisierungs-Fragmentanbieter
description: Dieses Thema enthält Beispielcode, der zeigt, wie die Navigation in einem Microsoft Benutzeroberflächenautomatisierungs-Anbieter für ein Element in einem Fragment aktiviert wird.
ms.assetid: 8c390e19-3c17-4e02-ade8-cd5c1ed9E938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495c48f6f355e7cc2a42b58ac0e32f88958361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036437"
---
# <a name="how-to-enable-navigation-in-a-ui-automation-fragment-provider"></a><span data-ttu-id="85d1d-103">Aktivieren der Navigation in einem Benutzeroberflächenautomatisierungs-Fragmentanbieter</span><span class="sxs-lookup"><span data-stu-id="85d1d-103">How to Enable Navigation in a UI Automation Fragment Provider</span></span>

<span data-ttu-id="85d1d-104">Dieses Thema enthält Beispielcode, der zeigt, wie die Navigation in einem Microsoft Benutzeroberflächenautomatisierungs-Anbieter für ein Element in einem Fragment aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="85d1d-104">This topic contains example code that shows how to enable navigation in a Microsoft UI Automation provider for an element in a fragment.</span></span>

<span data-ttu-id="85d1d-105">Im folgenden Beispielcode wird die [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) -Methode für ein Listenelement in einem benutzerdefinierten Listen Steuerelement implementiert.</span><span class="sxs-lookup"><span data-stu-id="85d1d-105">The following example code implements the [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method for a list item in a custom list control.</span></span> <span data-ttu-id="85d1d-106">Das übergeordnete Element ist das benutzerdefinierte Listen Steuerelement, und die gleich geordneten Elemente sind andere Elemente in der Liste.</span><span class="sxs-lookup"><span data-stu-id="85d1d-106">The parent element is the custom list control, and the sibling elements are other items in the list.</span></span> <span data-ttu-id="85d1d-107">Die-Methode legt den *pRetVal* -Parameter auf **null** fest, wenn kein Element in der angegebenen Richtung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="85d1d-107">The method sets the *pRetVal* parameter to **NULL** if there is no element in the specified direction.</span></span>


```C++
// Implementation of IRawElementProviderFragment::Navigate.
// Enables UI Automation to locate the element in the tree.
HRESULT STDMETHODCALLTYPE ListItemProvider::Navigate(NavigateDirection direction, IRawElementProviderFragment ** pRetVal)
{
    if (pRetVal == NULL) 
    {
        return E_INVALIDARG;
    }

    IRawElementProviderFragment* pFrag = NULL;
    switch(direction)
    {
        case NavigateDirection_Parent:
            pFrag = (IRawElementProviderFragment*) m_parentProvider;       
            break;

        case NavigateDirection_NextSibling:
            pFrag = (IRawElementProviderFragment*) m_nextSiblingProvider;
            break;

        case NavigateDirection_PreviousSibling:  
            pFrag = (IRawElementProviderFragment*) m_previousSiblingProvider;
            break;
    }
    *pRetVal = pFrag;
    if (pFrag != NULL) 
    {
        pFrag->AddRef();
    }
    return S_OK;
}              
```



## <a name="related-topics"></a><span data-ttu-id="85d1d-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="85d1d-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="85d1d-109">**Licher**</span><span class="sxs-lookup"><span data-stu-id="85d1d-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="85d1d-110">Implementieren eines Server-Side Benutzeroberflächenautomatisierungs-Anbieters</span><span class="sxs-lookup"><span data-stu-id="85d1d-110">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="85d1d-111">Gewusst-wie-Themen für Benutzeroberflächenautomatisierungs-Anbieter</span><span class="sxs-lookup"><span data-stu-id="85d1d-111">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




