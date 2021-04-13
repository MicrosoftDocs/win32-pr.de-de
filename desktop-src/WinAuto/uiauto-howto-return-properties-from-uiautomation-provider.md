---
title: Zurückgeben von Eigenschaften aus einem Benutzeroberflächenautomatisierungs-Anbieter
description: Dieses Thema enthält Beispielcode, der zeigt, wie ein Microsoft UI Automation-Anbieter Eigenschaften eines UI-Elements an Client Anwendungen zurückgibt.
ms.assetid: 6932de16-5548-4aa3-9f29-5daa57bb202b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4133a53df3c59e6d5c93b1c9cd8e6aa942b4bd56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390374"
---
# <a name="how-to-return-properties-from-a-ui-automation-provider"></a>Zurückgeben von Eigenschaften aus einem Benutzeroberflächenautomatisierungs-Anbieter

Dieses Thema enthält Beispielcode, der zeigt, wie ein Microsoft UI Automation-Anbieter Eigenschaften eines UI-Elements an Client Anwendungen zurückgibt.

Um einen Eigenschafts Wert vom Anbieter abzurufen, ruft die Benutzeroberflächen Automatisierung die Implementierung der Methode [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) eines Anbieters auf, übergibt die ID der abzurufenden Eigenschaft und einen Zeiger auf eine [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur. Wenn der Anbieter die angegebene Eigenschaft unterstützt, kopiert er den Datentyp und den Wert der-Eigenschaft in die **Variant** -Struktur. Wenn die Eigenschaft nicht unterstützt wird, legt der Anbieter den **VT** -Member der **Variant** -Struktur auf VT \_ Empty fest.


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

**Licher**
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> <dt>

[Gewusst-wie-Themen für Benutzeroberflächenautomatisierungs-Anbieter](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 