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
# <a name="how-to-enable-navigation-in-a-ui-automation-fragment-provider"></a>Aktivieren der Navigation in einem Benutzeroberflächenautomatisierungs-Fragmentanbieter

Dieses Thema enthält Beispielcode, der zeigt, wie die Navigation in einem Microsoft Benutzeroberflächenautomatisierungs-Anbieter für ein Element in einem Fragment aktiviert wird.

Im folgenden Beispielcode wird die [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) -Methode für ein Listenelement in einem benutzerdefinierten Listen Steuerelement implementiert. Das übergeordnete Element ist das benutzerdefinierte Listen Steuerelement, und die gleich geordneten Elemente sind andere Elemente in der Liste. Die-Methode legt den *pRetVal* -Parameter auf **null** fest, wenn kein Element in der angegebenen Richtung vorhanden ist.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Implementieren eines Server-Side Benutzeroberflächenautomatisierungs-Anbieters](uiauto-serversideprovider.md)
</dt> <dt>

[Gewusst-wie-Themen für Benutzeroberflächenautomatisierungs-Anbieter](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




