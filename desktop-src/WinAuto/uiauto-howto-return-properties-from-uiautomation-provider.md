---
title: Zurückgeben von Eigenschaften von einem Benutzeroberflächenautomatisierung-Anbieter
description: Dieses Thema enthält Beispielcode, der zeigt, wie ein Microsoft Benutzeroberflächenautomatisierung-Anbieter Eigenschaften eines Benutzeroberflächenelements an Clientanwendungen zurückgibt.
ms.assetid: 6932de16-5548-4aa3-9f29-5daa57bb202b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1284e2969d726006b4f8a8b0b6b3e63a7e421a14fb688dae5cbf8b8aa53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859459"
---
# <a name="how-to-return-properties-from-a-ui-automation-provider"></a>Zurückgeben von Eigenschaften von einem Benutzeroberflächenautomatisierung-Anbieter

Dieses Thema enthält Beispielcode, der zeigt, wie ein Microsoft Benutzeroberflächenautomatisierung-Anbieter Eigenschaften eines Benutzeroberflächenelements an Clientanwendungen zurückgibt.

Um einen Eigenschaftswert vom Anbieter abzurufen, ruft Benutzeroberflächenautomatisierung die Implementierung der [**IRawElementProviderSimple::GetPropertyValue-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) eines Anbieters auf, übergibt die ID der abzurufenden Eigenschaft und einen Zeiger auf eine [**VARIANT-Struktur.**](/windows/win32/api/oaidl/ns-oaidl-variant) Wenn der Anbieter die angegebene Eigenschaft unterstützt, kopiert er den Datentyp und den Wert der Eigenschaft in die **VARIANT-Struktur.** Wenn die -Eigenschaft nicht unterstützt wird, legt der Anbieter den **vt-Member** der **VARIANT-Struktur** auf VT \_ EMPTY fest.


```C++
IFACEMETHODIMP Provider::GetPropertyValue(PROPERTYID propertyId, VARIANT* pRetVal)
{
    // The Name property is typically the same as the Caption property of the 
    // control window, if it has one. Here, the Name is overridden for the 
    // sake of illustration. 
    if (propertyId == UIA_NamePropertyId) 
    {
        pRetVal->vt = VT_BSTR;
        pRetVal->bstrVal = SysAllocString(L"Custom button");
    }
    
    else if (propertyId == UIA_ControlTypePropertyId) 
    {
        pRetVal->vt = VT_I4;
        pRetVal->lVal = UIA_ButtonControlTypeId; 
    }

    else if (propertyId == UIA_IsContentElementPropertyId) 
    {
        pRetVal->vt = VT_BOOL;
        pRetVal->lVal = TRUE; 
    }

    else if (propertyId == UIA_IsControlElementPropertyId) 
    {
        pRetVal->vt = VT_BOOL;
        pRetVal->lVal = TRUE; 
    }

    //
    // Return other properties as appropriate for the control type. 
    //

    else
    {
        pRetVal->vt = VT_EMPTY;
        // UI Automation will attempt to get the property from the  
        // provider for window that hosts the control.
    }
    return S_OK;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> <dt>

[Themen zur Vorgehensweise für Benutzeroberflächenautomatisierung-Anbieter](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 