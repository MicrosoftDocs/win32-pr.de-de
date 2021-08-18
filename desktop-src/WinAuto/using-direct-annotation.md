---
title: Verwenden der direkten Anmerkung
description: Verwenden der direkten Anmerkung
ms.assetid: d9d78e74-dcab-4974-945f-e8c5d42c04b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8543b5aa4e6beb86b6119d13fe71ad45c1a34776e19095170cb48d8d9f48e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744885"
---
# <a name="using-direct-annotation"></a>Verwenden der direkten Anmerkung

**So verwenden Sie eine direkte Anmerkung zum Überschreiben des Werts einer Eigenschaft**

1.  Verwenden Sie die [Funktion CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) oder [CoCreateInstanceEx,](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) um das [**IAccPropServices-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) zu erstellen.
2.  Rufen Sie [**IAccPropServices::SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop)auf, und übergeben Sie den **HWND,** die Objekt-ID, die untergeordnete ID, die zu überschreibende Eigenschaft und eine [VARIANT-Eigenschaft,](/windows/win32/api/oaidl/ns-oaidl-variant) die den neuen Wert der Eigenschaft enthält. In diesem Schritt wird der Wert kommentiert.
3.  Geben Sie die Schnittstellenzeiger frei, und geben Sie Arbeitsspeicher frei.

Im folgenden Beispiel wird gezeigt, wie die [**Role-Eigenschaft**](role-property.md) eines statischen Textsteuerelements kommentiert wird.


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



## <a name="properties-supported-when-specifying-a-value"></a>Eigenschaften, die beim Angeben eines Werts unterstützt werden

Die folgenden Microsoft Active Accessibility Eigenschaften können bei der Angabe eines Werts (wobei der Wert vom notierten Typ sein muss) für die direkte Anmerkung mit Anmerkungen versehen werden. Zum Überschreiben oder Hinzufügen einer Microsoft Benutzeroberflächenautomatisierung-Eigenschaft zu einem Steuerelement können Sie die Benutzeroberflächenautomatisierung Eigenschaften-ID anstelle der Microsoft Active Accessibility Eigenschaften-ID angeben. Eine Liste der Benutzeroberflächenautomatisierung-IDs finden Sie unter [Eigenschaftenbezeichner.](uiauto-entry-propids.md)



| Eigenschaft                      | type     |
|-------------------------------|----------|
| PROPID \_ ACC \_ NAME             | VT \_ BSTR |
| PROPID \_ ACC \_ DESCRIPTION      | VT \_ BSTR |
| PROPID \_ ACC \_ ROLE             | VT \_ I4   |
| PROPID \_ ACC \_ STATE            | VT \_ I4   |
| PROPID \_ ACC \_ HELP             | VT \_ BSTR |
| PROPID \_ ACC \_ KEYBOARDSHORTCUT | VT \_ BSTR |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR |
| PROPID \_ ACC \_ VALUEMAP         | VT \_ BSTR |
| PROPID \_ ACC \_ ROLEMAP          | VT \_ BSTR |
| PROPID \_ ACC \_ STATEMAP         | VT \_ BSTR |



 

 

 