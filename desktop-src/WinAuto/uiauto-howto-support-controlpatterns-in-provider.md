---
title: Unterstützung von Steuerelementmustern in einem Benutzeroberflächenautomatisierungs-Anbieter
description: In diesem Thema wird gezeigt, wie ein Microsoft Benutzeroberflächenautomatisierung-Anbieter Steuerelementmuster für ein Steuerelement implementiert. Mit Steuerelementmustern können Clientanwendungen das Steuerelement bearbeiten und Informationen dazu abrufen.
ms.assetid: 504d0ed8-32c1-43ed-9f71-328a013ab350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649f9419c5e3003c0185f435cba4d38f4a25c3d7adc1bdc7cf9c53cd06b32a6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759230"
---
# <a name="support-control-patterns-in-a-ui-automation-provider"></a>Unterstützung von Steuerelementmustern in einem Benutzeroberflächenautomatisierungs-Anbieter

In diesem Thema wird gezeigt, wie ein Microsoft Benutzeroberflächenautomatisierung-Anbieter Steuerelementmuster für ein Steuerelement implementiert. Mit Steuerelementmustern können Clientanwendungen das Steuerelement bearbeiten und Informationen dazu abrufen.

Ein Anbieter implementiert ein Steuerelementmuster, indem er die folgenden Hauptschritte durchführt:

1.  Implementieren Sie die Anbieterschnittstelle, die das Steuerelementmuster unterstützt. Um beispielsweise das [Selection-Steuerelementmuster](uiauto-implementingselection.md) zu unterstützen, implementiert ein Anbieter für ein benutzerdefiniertes Listensteuerelement die [**ISelectionProvider-Schnittstelle.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)
2.  Gibt ein Objekt zurück, das die Schnittstelle des Steuerelementmusteranbieters enthält, wenn Benutzeroberflächenautomatisierung die [**IRawElementProviderSimple::GetPatternProvider-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) des Anbieters aufruft.

Das folgende Beispiel zeigt die [**ISelectionProvider-Schnittstellenimplementierung**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) für ein benutzerdefiniertes Einzelauswahllisten-Steuerelement. Die Implementierung umfasst Methoden zum Abrufen von Eigenschaften für die Eigenschaften IsSelectionRequired und CanSelectMultiple sowie eine Methode zum Abrufen des Anbieters für das ausgewählte Listenelement.


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



Das folgende Beispiel zeigt eine Implementierung von [**IRawElementProviderSimple::GetPatternProvider,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) die ein Objekt zurückgibt, das [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)implementiert. Die meisten Listensteuerelemente unterstützen auch andere Muster, aber in diesem Beispiel wird ein NULL-Verweis für alle anderen Steuerelementmusterbezeichner zurückgegeben.


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

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Anleitungsthemen für Benutzeroberflächenautomatisierung-Anbieter](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




