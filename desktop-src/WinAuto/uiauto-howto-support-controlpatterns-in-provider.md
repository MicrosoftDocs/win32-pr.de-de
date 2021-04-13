---
title: Unterstützung von Steuerelementmustern in einem Benutzeroberflächenautomatisierungs-Anbieter
description: In diesem Thema wird gezeigt, wie ein Microsoft UI Automation-Anbieter Steuerelement Muster für ein Steuerelement implementiert. Steuerelement Muster ermöglichen es Client Anwendungen, das Steuerelement zu bearbeiten und Informationen dazu zu erhalten.
ms.assetid: 504d0ed8-32c1-43ed-9f71-328a013ab350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54e75fa12dba891bc4eded5fd9763f7825eb7f88
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "104313578"
---
# <a name="support-control-patterns-in-a-ui-automation-provider"></a>Unterstützung von Steuerelementmustern in einem Benutzeroberflächenautomatisierungs-Anbieter

In diesem Thema wird gezeigt, wie ein Microsoft UI Automation-Anbieter Steuerelement Muster für ein Steuerelement implementiert. Steuerelement Muster ermöglichen es Client Anwendungen, das Steuerelement zu bearbeiten und Informationen dazu zu erhalten.

Ein Anbieter implementiert ein Steuerelement Muster, indem er die folgenden Schritte ausführt:

1.  Implementieren Sie die Anbieter Schnittstelle, die das-Steuerelement Muster unterstützt. Um z. b. das [Auswahl](uiauto-implementingselection.md) Steuerelement Muster zu unterstützen, würde ein Anbieter für ein benutzerdefiniertes Listen Steuerelement die [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) -Schnittstelle implementieren.
2.  Gibt ein Objekt zurück, das die Schnittstelle des Steuerelement Muster Anbieters enthält, wenn die Benutzeroberflächen Automatisierung die Methode [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) des Anbieters aufruft.

Das folgende Beispiel zeigt die Implementierung der [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) -Schnittstelle für ein benutzerdefiniertes Listen Steuerelement für die einfache Auswahl. Die-Implementierung enthält Methoden zum Abrufen von Eigenschaften für die Eigenschaften IsSelectionRequired und CanSelectMultiple sowie eine Methode zum Abrufen des Anbieters für das ausgewählte Listenelement.


```C++
// Specifies whether the list control supports the selection of
// multiple items at the same time.
IFACEMETHODIMP ListProvider::get_CanSelectMultiple(BOOL *pRetVal)
{
    *pRetVal = FALSE;
    return S_OK;
} 

// Specifies whether the list must have an item selected at all times.
IFACEMETHODIMP ListProvider::get_IsSelectionRequired(BOOL *pRetVal)
{
   *pRetVal = TRUE;
   return S_OK;
}

// Retrieves the provider of the selected item in a custom list control. 
//
// m_pControl - pointer to an application-defined object for managing
//   the custom list control. 
//
// ListItemProvider - application-defined class that inherits the 
//   IRawElementProviderSimple interface.
//
// GetItemProviderByIndex - application-defined method that retrieves the 
//   IRawElementProviderSimple interface of the selected item.
IFACEMETHODIMP ListProvider::GetSelection(SAFEARRAY** pRetVal)
{
    // Create a safe array to store the IRawElementProviderSimple pointer.
    SAFEARRAY *psa = SafeArrayCreateVector(VT_UNKNOWN, 0, 1);

    // Retrieve the index of the selected list item. 
    int index = m_pControl->GetSelectedIndex(); 

    // Retrieve the IRawElementProviderSimple pointer of the selected list
    // item. ListItemProvider is an application-defined class that 
    // inherits the IRawElementProviderSimple interface. 
    ListItemProvider* pItem = GetItemProviderByIndex(index); 
    if (pItem != NULL)
    {
        LONG i = 0;
        SafeArrayPutElement(psa, &i, pItem);
    }
    *pRetVal = psa;
    return S_OK;
}
```



Das folgende Beispiel zeigt eine Implementierung von [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) , die ein Objekt zurückgibt, das [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)implementiert. Die meisten Listen Steuerelemente unterstützen auch andere Muster, in diesem Beispiel wird jedoch ein NULL-Verweis für alle anderen Steuerelement Muster Bezeichner zurückgegeben.


```C++
// Retrieves an object that supports the control pattern provider interface 
// for the specified control pattern. 
IFACEMETHODIMP ListProvider::GetPatternProvider(PATTERNID patternId, IUnknown** pRetVal)
{
    *pRetVal = NULL;
    if (patternId == UIA_SelectionPatternId) 
    {
        // Return the object that implements ISelectionProvider. In this example, 
        // ISelectionProvider is implemented in the current object (this).
        *pRetVal = static_cast<IRawElementProviderSimple*>(this);
        AddRef();  
    }
    return S_OK;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Gewusst-wie-Themen für Benutzeroberflächenautomatisierungs-Anbieter](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




