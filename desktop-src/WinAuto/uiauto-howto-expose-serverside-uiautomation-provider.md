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
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a>Verfügbar machen eines Server-Side Benutzeroberflächenautomatisierungs-Anbieters

Dieses Thema enthält Beispielcode, der zeigt, wie ein serverseitiger Microsoft-Benutzeroberflächenautomatisierungs-Anbieter für ein benutzerdefiniertes Steuerelement verfügbar gemacht wird.

Microsoft UI Automation sendet die [**WM- \_ GetObject**](wm-getobject.md) -Nachricht an eine Anbieter Anwendung, um Informationen zu einem vom Anbieter unterstützten zugänglichen Objekt abzurufen. Die Benutzeroberflächenautomatisierung sendet das **WM- \_ GetObject** -Element, wenn ein Client [**iuiautomation:: elementfromhandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**elementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)und [**getfocucements**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)aufruft und Ereignisse behandelt, die vom Client registriert wurden.

Wenn ein Anbieter eine [**WM- \_ GetObject**](wm-getobject.md) -Nachricht empfängt, sollte überprüft werden, ob der *LPARAM* -Parameter mit **uiarootobjectid** übereinstimmt. Wenn dies der Fall ist, sollte der Anbieter die [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle des Objekts zurückgeben. Der Anbieter gibt die-Schnittstelle zurück, indem er die [**uiareturnrawelementprovider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) -Funktion aufruft.

Das folgende Beispiel zeigt, wie auf [**WM \_ GetObject**](wm-getobject.md)reagiert wird.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Implementieren eines Server-Side Benutzeroberflächenautomatisierungs-Anbieters](uiauto-serversideprovider.md)
</dt> <dt>

[Die WM- \_ GetObject-Nachricht](the-wm-getobject-message.md)
</dt> <dt>

[Gewusst-wie-Themen für Benutzeroberflächenautomatisierungs-Anbieter](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




