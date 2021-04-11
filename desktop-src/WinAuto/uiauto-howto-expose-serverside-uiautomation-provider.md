---
title: Verfügbar machen eines Server-Side Benutzeroberflächenautomatisierungs-Anbieters
description: Dieses Thema enthält Beispielcode, der zeigt, wie ein serverseitiger Microsoft-Benutzeroberflächenautomatisierungs-Anbieter für ein benutzerdefiniertes Steuerelement verfügbar gemacht wird.
ms.assetid: 68bf16c7-fbab-478a-97be-47d1195028f3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5af3fa9e663bc737df95015db94cdedc1073ab9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206969"
---
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a><span data-ttu-id="c9c6d-103">Verfügbar machen eines Server-Side Benutzeroberflächenautomatisierungs-Anbieters</span><span class="sxs-lookup"><span data-stu-id="c9c6d-103">How to Expose a Server-Side UI Automation Provider</span></span>

<span data-ttu-id="c9c6d-104">Dieses Thema enthält Beispielcode, der zeigt, wie ein serverseitiger Microsoft-Benutzeroberflächenautomatisierungs-Anbieter für ein benutzerdefiniertes Steuerelement verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="c9c6d-104">This topic contains example code that shows how to expose a server-side Microsoft UI Automation provider for a custom control.</span></span>

<span data-ttu-id="c9c6d-105">Microsoft UI Automation sendet die [**WM- \_ GetObject**](wm-getobject.md) -Nachricht an eine Anbieter Anwendung, um Informationen zu einem vom Anbieter unterstützten zugänglichen Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c9c6d-105">Microsoft UI Automation sends the [**WM\_GETOBJECT**](wm-getobject.md) message to a provider application to retrieve information about an accessible object supported by the provider.</span></span> <span data-ttu-id="c9c6d-106">Die Benutzeroberflächenautomatisierung sendet das **WM- \_ GetObject** -Element, wenn ein Client [**iuiautomation:: elementfromhandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**elementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)und [**getfocucements**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)aufruft und Ereignisse behandelt, die vom Client registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="c9c6d-106">UI Automation sends **WM\_GETOBJECT** when a client calls [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint), and [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), and when handling events for which the client has registered.</span></span>

<span data-ttu-id="c9c6d-107">Wenn ein Anbieter eine [**WM- \_ GetObject**](wm-getobject.md) -Nachricht empfängt, sollte überprüft werden, ob der *LPARAM* -Parameter mit **uiarootobjectid** übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c9c6d-107">When a provider receives a [**WM\_GETOBJECT**](wm-getobject.md) message, it should check whether the *lParam* parameter is equal to **UiaRootObjectId**.</span></span> <span data-ttu-id="c9c6d-108">Wenn dies der Fall ist, sollte der Anbieter die [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle des Objekts zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c9c6d-108">If it is, the provider should return the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface of the object.</span></span> <span data-ttu-id="c9c6d-109">Der Anbieter gibt die-Schnittstelle zurück, indem er die [**uiareturnrawelementprovider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="c9c6d-109">The provider returns the interface by calling the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>

<span data-ttu-id="c9c6d-110">Das folgende Beispiel zeigt, wie auf [**WM \_ GetObject**](wm-getobject.md)reagiert wird.</span><span class="sxs-lookup"><span data-stu-id="c9c6d-110">The following example demonstrates shows how to respond to [**WM\_GETOBJECT**](wm-getobject.md).</span></span>


```C++
    // Expose the custom button's server-side provider to UI Automation.
    case WM_GETOBJECT:
        {
            // If lParam matches UiaRootObjectId, return IRawElementProviderSimple.
            if (static_cast<long>(lParam) == static_cast<long>(UiaRootObjectId))
            {
                // Retrieve the pointer to the custom button object from the
                // window data.
                CustomButton* pControl = reinterpret_cast<CustomButton*>(
                    GetWindowLongPtr(hwnd, GWLP_USERDATA));

                // Call an application-defined method to get the
                // IRawElementProviderSimple pointer.
                IRawElementProviderSimple* pRootProvider = 
                    pControl->GetUIAutomationProvider(hwnd);

                // Return the IRawElementProviderSimple pointer to UI Automation.
                return UiaReturnRawElementProvider(hwnd, wParam, lParam, 
                    pRootProvider);
            }
            return 0;
        }
```



## <a name="related-topics"></a><span data-ttu-id="c9c6d-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9c6d-111">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c9c6d-112">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c9c6d-112">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c9c6d-113">Implementieren eines Server-Side Benutzeroberflächenautomatisierungs-Anbieters</span><span class="sxs-lookup"><span data-stu-id="c9c6d-113">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="c9c6d-114">Die WM- \_ GetObject-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c9c6d-114">The WM\_GETOBJECT Message</span></span>](the-wm-getobject-message.md)
</dt> <dt>

[<span data-ttu-id="c9c6d-115">Gewusst-wie-Themen für Benutzeroberflächenautomatisierungs-Anbieter</span><span class="sxs-lookup"><span data-stu-id="c9c6d-115">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




