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
# <a name="using-direct-annotation"></a><span data-ttu-id="a66de-103">Verwenden der direkten Anmerkung</span><span class="sxs-lookup"><span data-stu-id="a66de-103">Using Direct Annotation</span></span>

<span data-ttu-id="a66de-104">**So verwenden Sie die direkte Anmerkung, um den Wert einer Eigenschaft zu überschreiben**</span><span class="sxs-lookup"><span data-stu-id="a66de-104">**To use direct annotation to override the value of a property**</span></span>

1.  <span data-ttu-id="a66de-105">Verwenden Sie die Funktion [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) oder [cokreateinstanceex](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) , um das Objekt [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a66de-105">Use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) or [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) function to create the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) object.</span></span>
2.  <span data-ttu-id="a66de-106">Wenden Sie [**IAccPropServices:: SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop)an, und übergeben Sie das **HWND**, die Objekt-ID, die untergeordnete ID, die Eigenschaft, die überschrieben werden soll, und eine [Variante](/windows/win32/api/oaidl/ns-oaidl-variant) , die den neuen Wert der Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="a66de-106">Call [**IAccPropServices::SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), passing the **HWND**, object ID, child ID, the property to be overridden, and a [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) containing the new value of the property.</span></span> <span data-ttu-id="a66de-107">In diesem Schritt wird der Wert kommentiert.</span><span class="sxs-lookup"><span data-stu-id="a66de-107">This step annotates the value.</span></span>
3.  <span data-ttu-id="a66de-108">Freigeben der Schnittstellen Zeiger und Freigeben von Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a66de-108">Release the interface pointers and free memory.</span></span>

<span data-ttu-id="a66de-109">Im folgenden Beispiel wird gezeigt, wie die [**Role**](role-property.md) -Eigenschaft eines statischen Text-Steuer Elements mit Anmerkungen versehen wird.</span><span class="sxs-lookup"><span data-stu-id="a66de-109">The following example shows how to annotate the [**Role**](role-property.md) property of a static text control.</span></span>


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



## <a name="properties-supported-when-specifying-a-value"></a><span data-ttu-id="a66de-110">Unterstützte Eigenschaften beim Angeben eines Werts</span><span class="sxs-lookup"><span data-stu-id="a66de-110">Properties Supported When Specifying a Value</span></span>

<span data-ttu-id="a66de-111">Die folgenden Eigenschaften von Microsoft Active Accessibility können mit Anmerkungen versehen werden, wenn ein Wert (wobei der Wert vom notierten Typ sein muss) für die direkte Anmerkung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a66de-111">The following Microsoft Active Accessibility properties can be annotated when specifying a value (where the value must be of the noted type) for direct annotation.</span></span> <span data-ttu-id="a66de-112">Wenn Sie einem Steuerelement eine Microsoft UI Automation-Eigenschaft außer Kraft setzen oder hinzufügen möchten, können Sie anstelle der Eigenschaften-ID der Microsoft Active Accessibility die Benutzeroberflächenautomatisierungs-Eigenschaften-ID angeben</span><span class="sxs-lookup"><span data-stu-id="a66de-112">To override or add a Microsoft UI Automation property to a control, you can specify the UI Automation property ID instead of the Microsoft Active Accessibility property ID.</span></span> <span data-ttu-id="a66de-113">Eine Liste der Benutzeroberflächenautomatisierungs-IDs finden Sie unter [Property Identifiers](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="a66de-113">For a list of UI Automation IDs, see [Property Identifiers](uiauto-entry-propids.md).</span></span>



| <span data-ttu-id="a66de-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a66de-114">Property</span></span>                      | <span data-ttu-id="a66de-115">type</span><span class="sxs-lookup"><span data-stu-id="a66de-115">Type</span></span>     |
|-------------------------------|----------|
| <span data-ttu-id="a66de-116">Name des PROPID- \_ ACC \_</span><span class="sxs-lookup"><span data-stu-id="a66de-116">PROPID\_ACC\_NAME</span></span>             | <span data-ttu-id="a66de-117">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="a66de-117">VT\_BSTR</span></span> |
| <span data-ttu-id="a66de-118">Beschreibung des PROPID- \_ ACC \_</span><span class="sxs-lookup"><span data-stu-id="a66de-118">PROPID\_ACC\_DESCRIPTION</span></span>      | <span data-ttu-id="a66de-119">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="a66de-119">VT\_BSTR</span></span> |
| <span data-ttu-id="a66de-120">PROPID- \_ Rolle "ACC" \_</span><span class="sxs-lookup"><span data-stu-id="a66de-120">PROPID\_ACC\_ROLE</span></span>             | <span data-ttu-id="a66de-121">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a66de-121">VT\_I4</span></span>   |
| <span data-ttu-id="a66de-122">Status des PROPID- \_ ACC \_</span><span class="sxs-lookup"><span data-stu-id="a66de-122">PROPID\_ACC\_STATE</span></span>            | <span data-ttu-id="a66de-123">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a66de-123">VT\_I4</span></span>   |
| <span data-ttu-id="a66de-124">PROPID \_ - \_ Hilfe zum ACC</span><span class="sxs-lookup"><span data-stu-id="a66de-124">PROPID\_ACC\_HELP</span></span>             | <span data-ttu-id="a66de-125">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="a66de-125">VT\_BSTR</span></span> |
| <span data-ttu-id="a66de-126">PROPID \_ ACC \_ KeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="a66de-126">PROPID\_ACC\_KEYBOARDSHORTCUT</span></span> | <span data-ttu-id="a66de-127">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="a66de-127">VT\_BSTR</span></span> |
| <span data-ttu-id="a66de-128">PROPID \_ ACC \_ DEFAULTACTION</span><span class="sxs-lookup"><span data-stu-id="a66de-128">PROPID\_ACC\_DEFAULTACTION</span></span>    | <span data-ttu-id="a66de-129">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="a66de-129">VT\_BSTR</span></span> |
| <span data-ttu-id="a66de-130">PROPID- \_ ACC ( \_ ValueMap)</span><span class="sxs-lookup"><span data-stu-id="a66de-130">PROPID\_ACC\_VALUEMAP</span></span>         | <span data-ttu-id="a66de-131">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="a66de-131">VT\_BSTR</span></span> |
| <span data-ttu-id="a66de-132">PROPID- \_ ACC- \_ rolemap</span><span class="sxs-lookup"><span data-stu-id="a66de-132">PROPID\_ACC\_ROLEMAP</span></span>          | <span data-ttu-id="a66de-133">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="a66de-133">VT\_BSTR</span></span> |
| <span data-ttu-id="a66de-134">PROPID- \_ ACC- \_ statemap</span><span class="sxs-lookup"><span data-stu-id="a66de-134">PROPID\_ACC\_STATEMAP</span></span>         | <span data-ttu-id="a66de-135">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="a66de-135">VT\_BSTR</span></span> |



 

 

 