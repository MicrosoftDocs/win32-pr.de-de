---
title: Verfügbar machen eines Server-Side Benutzeroberflächenautomatisierung Anbieters
description: Dieses Thema enthält Beispielcode, der zeigt, wie sie einen serverseitigen Microsoft Benutzeroberflächenautomatisierung für ein benutzerdefiniertes Steuerelement verfügbar machen.
ms.assetid: 68bf16c7-fbab-478a-97be-47d1195028f3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771e81a058af16320673e46a7981cf49ee22105fa841807bc07e3a528ff223cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133313"
---
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a>Verfügbar machen eines Server-Side Benutzeroberflächenautomatisierung Anbieters

Dieses Thema enthält Beispielcode, der zeigt, wie sie einen serverseitigen Microsoft Benutzeroberflächenautomatisierung für ein benutzerdefiniertes Steuerelement verfügbar machen.

Microsoft Benutzeroberflächenautomatisierung sendet die [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) an eine Anbieteranwendung, um Informationen zu einem barrierefreien Objekt abzurufen, das vom Anbieter unterstützt wird. Benutzeroberflächenautomatisierung sendet **WM \_ GETOBJECT,** wenn ein Client [**IUIAutomation::ElementFromHandle,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle) [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)und [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)aufruft, und wenn Ereignisse behandelt werden, für die der Client registriert wurde.

Wenn ein Anbieter eine [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) empfängt, sollte er überprüfen, ob der *lParam-Parameter* gleich **UiaRootObjectId ist.** Wenn dies der Fehler ist, sollte der Anbieter die [**IRawElementProviderSimple-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) des Objekts zurückgeben. Der Anbieter gibt die Schnittstelle zurück, indem er die [**UiaReturnRawElementProvider-Funktion**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) aufruft.

Im folgenden Beispiel wird veranschaulicht, wie auf [**WM \_ GETOBJECT reagiert wird.**](wm-getobject.md)


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

**Konzeptionellen**
</dt> <dt>

[Implementieren eines Server-Side Benutzeroberflächenautomatisierung Anbieters](uiauto-serversideprovider.md)
</dt> <dt>

[DIE WM \_ GETOBJECT-Nachricht](the-wm-getobject-message.md)
</dt> <dt>

[How-To Topics for Benutzeroberflächenautomatisierung Providers](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




