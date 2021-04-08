---
title: Vorgehensweise beim Durchlaufen der Benutzeroberflächenautomatisierungs-Struktur
description: Dieses Thema enthält Beispielcode, der zeigt, wie die iuiautomationtreewalker-Schnittstelle verwendet wird, um die Elemente in der Microsoft UI Automation-Struktur zu durchlaufen und zu untersuchen.
ms.assetid: 41ca783d-56d1-4ad5-8f07-c265ff2e07bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed5c6c1bec961d4f0df83687cd19eecba6ed179
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855992"
---
# <a name="how-to-walk-the-ui-automation-tree"></a>Vorgehensweise beim Durchlaufen der Benutzeroberflächenautomatisierungs-Struktur

Dieses Thema enthält Beispielcode, der zeigt, wie die [**iuiautomationtreewalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) -Schnittstelle verwendet wird, um die Elemente in der Microsoft UI Automation-Struktur zu durchlaufen und zu untersuchen. In diesem Thema werden die folgenden Themen behandelt:

-   [Durchlaufen der nachfolgenden Elemente eines Elements](#walking-through-descendants-of-an-element)
-   [Durchlaufen von Vorgänger Elementen](#walking-through-ancestor-elements)
-   [Zugehörige Themen](#related-topics)

## <a name="walking-through-descendants-of-an-element"></a>Durchlaufen der nachfolgenden Elemente eines Elements

Das folgende Codebeispiel ist eine rekursive Funktion, die alle Nachfolger eines UI-Elements durchläuft und deren Steuerelement Typen in einer hierarchischen Liste anzeigt.


```C++
// CAUTION: Do not pass in the root (desktop) element. Traversing the entire subtree
// of the desktop could take a very long time and even lead to a stack overflow.
void ListDescendants(IUIAutomationElement* pParent, int indent)
{
    if (pParent == NULL)
        return;

    IUIAutomationTreeWalker* pControlWalker = NULL;
    IUIAutomationElement* pNode = NULL;

    g_pAutomation->get_ControlViewWalker(&pControlWalker);
    if (pControlWalker == NULL)
        goto cleanup;

    pControlWalker->GetFirstChildElement(pParent, &pNode);
    if (pNode == NULL)
        goto cleanup;

    while (pNode)
    {
        BSTR desc;
        pNode->get_CurrentLocalizedControlType(&desc);
        for (int x = 0; x <= indent; x++)
        {
            std::wcout << L"   ";
        }
        std::wcout << desc << L"\n";
        SysFreeString(desc);

        ListDescendants(pNode, indent+1);
        IUIAutomationElement* pNext;
        pControlWalker->GetNextSiblingElement(pNode, &pNext);
        pNode->Release();
        pNode = pNext;
    }

cleanup:
    if (pControlWalker != NULL)
        pControlWalker->Release();

    if (pNode != NULL)
        pNode->Release();

    return;
}
```



## <a name="walking-through-ancestor-elements"></a>Durchlaufen von Vorgänger Elementen

Das folgende Codebeispiel stellt eine Funktion dar, die die übergeordneten Elemente eines-Elements durchläuft, um das übergeordnete Element zu identifizieren. Dies ist hilfreich, wenn Sie das übergeordnete Fenster eines Steuer Elements identifizieren müssen. Die-Funktion gibt **null** für Elemente der obersten Ebene zurück. Das heißt, Elemente, deren übergeordnetes Element der Desktop ist.


```C++
IUIAutomationElement* GetContainingWindow(IUIAutomationElement* pChild)
{

    if (pChild == NULL)
        return NULL;

    IUIAutomationElement* pDesktop = NULL;
    HRESULT hr = g_pAutomation->GetRootElement(&pDesktop);
    if (FAILED(hr))
        return NULL;

    BOOL same;
    g_pAutomation->CompareElements(pChild, pDesktop, &same);
    if (same)
    {
        pDesktop->Release();
        return NULL; // No parent, so return NULL.
    }

    IUIAutomationElement* pParent = NULL;
    IUIAutomationElement* pNode = pChild;

    // Create the treewalker.
    IUIAutomationTreeWalker* pWalker = NULL;
    g_pAutomation->get_ControlViewWalker(&pWalker);
    if (pWalker == NULL)
        goto cleanup;

    // Walk up the tree.
    while (TRUE)
    {
        hr = pWalker->GetParentElement(pNode, &pParent);
        if (FAILED(hr) || pParent == NULL)
        {
            break;
        }
        g_pAutomation->CompareElements(pParent, pDesktop, &same);
        if (same)
        {
            pDesktop->Release();
            pParent->Release();
            pWalker->Release();
            // Reached desktop, so return next element below it.
            return pNode;
        }
        if (pNode != pChild) // Do not release the in-param.
            pNode->Release();
        pNode = pParent;
    }

cleanup:
    if ((pNode != NULL) && (pNode != pChild)) 
        pNode->Release();

    if (pDesktop != NULL)
        pDesktop->Release();

    if (pWalker != NULL)
        pWalker->Release();

    if (pParent != NULL)
        pParent->Release();

    return NULL;  
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Abrufen von Benutzeroberflächenautomatisierungs-Elementen](uiauto-obtainingelements.md)
</dt> <dt>

[Themen zur Vorgehensweise für Benutzeroberflächenautomatisierungs-Clients](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




