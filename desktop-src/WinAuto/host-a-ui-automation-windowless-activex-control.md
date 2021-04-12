---
title: Hosten eines fensterlosen ActiveX-Steuer Elements für die Benutzeroberflächen Automatisierung
description: Erfahren Sie, wie Sie einen Steuerelement Container erstellen, der fensterlose Microsoft-ActiveX-Steuerelemente hosten kann, die Microsoft UI Automation implementieren.
ms.assetid: A0F82968-F434-4F5E-8052-CF7CE65DB120
keywords:
- UI-Automatisierung, fensterloses ActiveX-Steuerelement
- Fensterlose ActiveX-Steuerelement, UI-Automatisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77026d923ea6f0d2536cbd6a94966ec858443258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315290"
---
# <a name="host-a-ui-automation-windowless-activex-control"></a>Hosten eines fensterlosen ActiveX-Steuer Elements für die Benutzeroberflächen Automatisierung

Erfahren Sie, wie Sie einen Steuerelement Container erstellen, der fensterlose Microsoft-ActiveX-Steuerelemente hosten kann, die Microsoft UI Automation implementieren. Mithilfe der hier beschriebenen Schritte können Sie sicherstellen, dass Benutzeroberflächen Automatisierung fensterlose Steuerelemente, die in Ihrem Steuerelement Container gehostet werden, von Hilfstechnologien (bei) Client Anwendungen zugänglich sind.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [ActiveX-Steuerelemente](/windows/desktop/com/activex-controls)
-   [Benutzeroberflächenautomatisierung](entry-uiauto-win32.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmierung von Microsoft Win32 und Component Object Model (com)
-   Fensterlose ActiveX-Steuerelemente
-   Benutzeroberflächen-Automatisierungsanbieter

## <a name="instructions"></a>Anweisungen

### <a name="step-1-provide-the-irawelementprovidersimple-interface-on-behalf-of-the-windowless-control"></a>Schritt 1: Geben Sie die IRawElementProviderSimple-Schnittstelle für das fensterlose Steuerelement an.

Wenn das System den " [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) "-Zeiger für den Stamm eines fensterlosen Steuer Elements benötigt, fragt das System den Steuerelement Container ab. Zum Abrufen des Zeigers ruft der Container die Implementierung der [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) -Methode des fensterlosen Steuer Elements auf.

Wenn der Steuerelement Container über eine Benutzeroberflächenautomatisierungs-Implementierung verfügt, kann er den [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Zeiger des fensterlosen Steuer Elements auf das System zurückgeben.

Wenn der Steuerelement Container eine Microsoft Active Accessibility-Implementierung aufweist, rufen Sie die [**uiaiaccessiblefromprovider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) -Funktion auf, um einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger zu erhalten, der das Steuerelement darstellt, und geben Sie dann den **IAccessible** -Schnittstellen Zeiger auf das System zurück.

### <a name="step-2-implement-the-irawelementproviderwindowlesssite-interface"></a>Schritt 2: Implementieren Sie die "irawelementproviderwindowlesssite"-Schnittstelle.

Ein Steuerelement Container implementiert die [**irawelementproviderwindowlesssite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) -Schnittstelle und ermöglicht ein fensterloses Steuerelement, das auf der Benutzeroberflächen Automatisierung basiert, um seine Barrierefreiheits Informationen zu kommunizieren.

1.  Implementieren Sie [**irawelementproviderwindowlesssite:: getruntimeidprefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).

    Ein fensterloses Steuerelement Fragment muss eine eindeutige Lauf Zeit-ID für sich selbst erstellen. Um die Lauf Zeit-ID zu erstellen, Ruft ein fensterloses Steuerelement Fragment einen Präfix Wert durch Aufrufen der [**getruntimeidprefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) -Methode der Steuerungs Website ab und fügt dann an das Präfix einen ganzzahligen Wert an, der relativ zu allen anderen Fragmenten im fensterlosen Steuerelement eindeutig ist.

    Die Steuerungs Site für ein fensterloses Steuerelement sollte die [**getruntimeidprefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) -Methode implementieren, indem ein **SAFEARRAY** gebildet wird, das die Konstante **uiaappendruntimeid** enthält, gefolgt von einem ganzzahligen Wert, der für die Website eindeutig ist.

    Dieses Beispiel zeigt, wie ein Lauf Zeit-ID-Präfix für ein fensterloses Steuerelement zurückgegeben wird.

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetRuntimeIdPrefix(   
         SAFEARRAY **ppsaPrefix)   
    {   
        if (ppsaPrefix == NULL) 
        {
            return E_INVALIDARG;
        }

        // m_siteIndex is the index of the windowless control's
        // site. It is defined by the control container.
        int rId[] = { UiaAppendRuntimeId, m_siteIndex };
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);  
        if (psa == NULL)
        {
            return E_OUTOFMEMORY;
        }

        for (LONG i = 0; i < 2; i++)
        {
            SafeArrayPutElement(psa, &i, (void*)&(rId[i]));
        }

        *ppsaPrefix = psa;  
        return S_OK;  
    }  
    ```

    

2.  Implementieren Sie die Methode [**irawelementproviderwindowlesssite:: getaccessentfragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) .

    Ein Steuerelement, das die Benutzeroberflächen Automatisierung implementiert, muss einen Zeiger auf den übergeordneten Fragmentanbieter des-Steuer Elements

    Um das übergeordnete Element des Fragments zurückzugeben, muss ein Objekt, das die [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) -Schnittstelle implementiert, in der Lage sein, die [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) -Methode zu implementieren. Das Implementieren von **Navigate** ist für ein fensterloses Steuerelement schwierig, da das Steuerelement seine Position in der zugänglichen Struktur des übergeordneten Objekts möglicherweise nicht ermitteln kann. Die Methode [**irawelementproviderwindowlesssite:: getereigentfragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) ermöglicht dem fensterlosen Steuerelement, seine Website nach dem angrenzenden Fragment abzufragen und dieses Fragment dann an den Client zurückzugeben, der **Navigate** aufgerufen hat.

    Dieses Beispiel zeigt, wie ein Steuerelement Container das übergeordnete Fragment eines fensterlosen Steuer Elements abruft.

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetAdjacentFragment(
            enum NavigateDirection direction, IRawElementProviderFragment **ppFragment)   
    {
        if (ppFragment == NULL)
        {
            return E_INVALIDARG;
        }
        
        *ppFragment = NULL;
        HRESULT hr = S_OK;

        switch (direction)
        {
            case NavigateDirection_Parent:
                {  
                    IRawElementProviderSimple *pSimple = NULL;

                    // Call an application-defined function to retrieve the
                    // parent provider interface.
                    hr = GetParentProvider(&pSimple);  
                    if (SUCCEEDED(hr))  
                    {  
                        // Get the parent's IRawElementProviderFragment interface.
                        hr = pSimple->QueryInterface(IID_PPV_ARGS(ppFragment));  
                        pSimple->Release();  
                    } 
                }  
                break;  
      
            case NavigateDirection_FirstChild:
            case NavigateDirection_LastChild:
                hr = E_INVALIDARG;
                break;

            // Ignore NavigateDirection_NextSibling and NavigateDirection_PreviousSibling
            // because there are no adjacent fragments.
            default:  
                break;  
        }  
      
        return hr;  
    }   
    ```

    

### <a name="step-3-optional-implement-the-irawelementproviderhostingaccessibles-interface"></a>Schritt 3: optional: Implementieren Sie die irawelementproviderhostingaccessibles-Schnittstelle.

Implementieren Sie die-Schnittstelle [**irawelementproviderhostingaccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) , wenn Ihr Steuerelement Container über eine Benutzeroberflächenautomatisierungs-Anbieter Implementierung verfügt, die der Stamm einer Barrierefreiheits Struktur ist, die fensterlose ActiveX-Steuerelemente enthält, die Microsoft Active Accessibility unterstützen Die " **irawelementproviderhostingaccessibles** "-Schnittstelle verfügt über eine einzelne Methode, " [**getembeddedaccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles)", die die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger von allen Microsoft Active Accessibility basierten, fensterlosen ActiveX-Steuerelementen abruft, die von Ihrem Steuerelement Container gehostet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hosten eines Windows-losen ActiveX-Steuer Elements mit MSAA](host-an-msaa-windowless-activex-control.md)
</dt> <dt>

[Barrierefreiheit für das fensterlose ActiveX-Steuerelement](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 