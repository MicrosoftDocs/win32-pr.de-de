---
description: Die OnConnect-Methode stellt einen IUnknown-Zeiger auf das-Objekt bereit, das der Eigenschaften Seite zugeordnet ist.
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: Cbasepropertypage. OnConnect-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38f83a7c491f1591cece8d5d85eb4525a1059d2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365654"
---
# <a name="cbasepropertypageonconnect-method"></a><span data-ttu-id="3b63c-103">Cbasepropertypage. OnConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="3b63c-103">CBasePropertyPage.OnConnect method</span></span>

<span data-ttu-id="3b63c-104">Die- `OnConnect` Methode stellt einen **IUnknown** -Zeiger auf das-Objekt bereit, das der Eigenschaften Seite zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3b63c-104">The `OnConnect` method provides an **IUnknown** pointer to the object associated with the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b63c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b63c-105">Syntax</span></span>


```C++
virtual HRESULT OnConnect(
   IUnknown *pUnknown
);
```



## <a name="parameters"></a><span data-ttu-id="3b63c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b63c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b63c-107">*pUnknown*</span><span class="sxs-lookup"><span data-stu-id="3b63c-107">*pUnknown*</span></span> 
</dt> <dd>

<span data-ttu-id="3b63c-108">Ein Zeiger auf die **IUnknown** -Schnittstelle des Objekts.</span><span class="sxs-lookup"><span data-stu-id="3b63c-108">Pointer to the **IUnknown** interface of the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b63c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b63c-109">Return value</span></span>

<span data-ttu-id="3b63c-110">Die Basisklassen Implementierung gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="3b63c-110">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b63c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b63c-111">Remarks</span></span>

<span data-ttu-id="3b63c-112">Die [**cbasepropertypage:: abtobjects**](cbasepropertypage-setobjects.md) -Methode ruft die- `OnConnect` Methode auf.</span><span class="sxs-lookup"><span data-stu-id="3b63c-112">The [**CBasePropertyPage::SetObjects**](cbasepropertypage-setobjects.md) method calls the `OnConnect` method.</span></span> <span data-ttu-id="3b63c-113">Überschreiben Sie diese Methode, um einen Zeiger auf das von *punknown* angegebene Objekt zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3b63c-113">Override this method to store a pointer to the object specified by *pUnknown*.</span></span> <span data-ttu-id="3b63c-114">Sie können entweder den *punknown* -Zeiger selbst speichern oder diesen Zeiger für andere Schnittstellen Abfragen.</span><span class="sxs-lookup"><span data-stu-id="3b63c-114">You can either store the *pUnknown* pointer itself, or query that pointer for other interfaces.</span></span> <span data-ttu-id="3b63c-115">Wenn Sie den *punknown* -Zeiger speichern, wird vor der Rückgabe von " **adressf** " aufgerufen `OnConnect` .</span><span class="sxs-lookup"><span data-stu-id="3b63c-115">If you store the *pUnknown* pointer, call **AddRef** before `OnConnect` returns.</span></span>

<span data-ttu-id="3b63c-116">Verwenden Sie in der [**cbasepropertypage:: onaktivierungs**](cbasepropertypage-onactivate.md) -Methode den gespeicherten Zeiger (oder Zeiger), um die Anfangswerte für die Dialog Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3b63c-116">In the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method, use the stored pointer (or pointers) to retrieve initial values for the dialog properties.</span></span> <span data-ttu-id="3b63c-117">Wenden Sie in der [**cbasepropertypage:: onapplychanges**](cbasepropertypage-onapplychanges.md) -Methode alle Änderungen auf das-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="3b63c-117">In the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method, apply any changes back to the object.</span></span> <span data-ttu-id="3b63c-118">Geben Sie alle Zeiger in der [**cbasepropertypage:: OnDisconnect**](cbasepropertypage-ondisconnect.md) -Methode frei.</span><span class="sxs-lookup"><span data-stu-id="3b63c-118">Release all pointers in the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="3b63c-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b63c-119">Examples</span></span>


```C++
HRESULT CMyProp::OnConnect(IUnknown *pUnk)
{
    ASSERT(m_pOwningFilter == NULL);
    HRESULT hr;
    // Query pUnk for the filter's custom interface.
    hr = pUnk->QueryInterface(IID_ISomeCustomInterface,
             reinterpret_cast<void**>(&m_pOwningFilter));
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="3b63c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b63c-120">Requirements</span></span>



| <span data-ttu-id="3b63c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b63c-121">Requirement</span></span> | <span data-ttu-id="3b63c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="3b63c-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b63c-123">Header</span><span class="sxs-lookup"><span data-stu-id="3b63c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3b63c-124"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b63c-124"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="3b63c-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3b63c-125">Library</span></span><br/> | <dl> <span data-ttu-id="3b63c-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3b63c-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b63c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b63c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b63c-128">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3b63c-128">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




