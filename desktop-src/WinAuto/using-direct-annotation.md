---
title: Verwenden der direkten Anmerkung
description: Verwenden der direkten Anmerkung
ms.assetid: d9d78e74-dcab-4974-945f-e8c5d42c04b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f0bdea5af896329b6836d21ca1dcee25bc2739
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315662"
---
# <a name="using-direct-annotation"></a>Verwenden der direkten Anmerkung

**So verwenden Sie die direkte Anmerkung, um den Wert einer Eigenschaft zu überschreiben**

1.  Verwenden Sie die Funktion [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) oder [cokreateinstanceex](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) , um das Objekt [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) zu erstellen.
2.  Wenden Sie [**IAccPropServices:: SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop)an, und übergeben Sie das **HWND**, die Objekt-ID, die untergeordnete ID, die Eigenschaft, die überschrieben werden soll, und eine [Variante](/windows/win32/api/oaidl/ns-oaidl-variant) , die den neuen Wert der Eigenschaft enthält. In diesem Schritt wird der Wert kommentiert.
3.  Freigeben der Schnittstellen Zeiger und Freigeben von Arbeitsspeicher.

Im folgenden Beispiel wird gezeigt, wie die [**Role**](role-property.md) -Eigenschaft eines statischen Text-Steuer Elements mit Anmerkungen versehen wird.


```C++
HRESULT CMyTextControl::SetAccessibleProperties()
{
  // COM is assumed to be initialized...
  IAccPropServices* pAccPropServices = NULL;

  HRESULT hr = CoCreateInstance(CLSID_AccPropServices,
    NULL, CLSCTX_SERVER, IID_IAccPropServices, 
    (void**)&pAccPropServices);

  if (SUCCEEDED(hr))
  {
    // Annotating the Role of this object to be STATICTEXT
    VARIANT var;
    var.vt = VT_I4;
    var.lVal = ROLE_SYSTEM_STATICTEXT;

    hr = pAccPropServices->SetHwndProp(_hwnd,
      OBJID_CLIENT,
      CHILDID_SELF,
      PROPID_ACC_ROLE,
      var);

    pAccPropServices->Release();
  }
  return hr;
}
```



## <a name="properties-supported-when-specifying-a-value"></a>Unterstützte Eigenschaften beim Angeben eines Werts

Die folgenden Eigenschaften von Microsoft Active Accessibility können mit Anmerkungen versehen werden, wenn ein Wert (wobei der Wert vom notierten Typ sein muss) für die direkte Anmerkung angegeben wird. Wenn Sie einem Steuerelement eine Microsoft UI Automation-Eigenschaft außer Kraft setzen oder hinzufügen möchten, können Sie anstelle der Eigenschaften-ID der Microsoft Active Accessibility die Benutzeroberflächenautomatisierungs-Eigenschaften-ID angeben Eine Liste der Benutzeroberflächenautomatisierungs-IDs finden Sie unter [Property Identifiers](uiauto-entry-propids.md).



| Eigenschaft                      | type     |
|-------------------------------|----------|
| Name des PROPID- \_ ACC \_             | VT \_ BSTR |
| Beschreibung des PROPID- \_ ACC \_      | VT \_ BSTR |
| PROPID- \_ Rolle "ACC" \_             | VT \_ I4   |
| Status des PROPID- \_ ACC \_            | VT \_ I4   |
| PROPID \_ - \_ Hilfe zum ACC             | VT \_ BSTR |
| PROPID \_ ACC \_ KeyboardShortcut | VT \_ BSTR |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR |
| PROPID- \_ ACC ( \_ ValueMap)         | VT \_ BSTR |
| PROPID- \_ ACC- \_ rolemap          | VT \_ BSTR |
| PROPID- \_ ACC- \_ statemap         | VT \_ BSTR |



 

 

 