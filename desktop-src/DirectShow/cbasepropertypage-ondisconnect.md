---
description: Die OnDisconnect-Methode wird aufgerufen, wenn auf der Eigenschaften Seite das zugeordnete-Objekt freigegeben werden soll.
ms.assetid: 55bab0ca-587e-405c-9025-f391cf08a620
title: Cbasepropertypage. OnDisconnect-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDisconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd251d20ca82ad0374a613d9ee73f0eaee21d31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364821"
---
# <a name="cbasepropertypageondisconnect-method"></a><span data-ttu-id="be740-103">Cbasepropertypage. OnDisconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="be740-103">CBasePropertyPage.OnDisconnect method</span></span>

<span data-ttu-id="be740-104">Die- `OnDisconnect` Methode wird aufgerufen, wenn die Eigenschaften Seite das zugeordnete-Objekt freigeben soll.</span><span class="sxs-lookup"><span data-stu-id="be740-104">The `OnDisconnect` method is called when the property page should release the associated object.</span></span>

## <a name="syntax"></a><span data-ttu-id="be740-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be740-105">Syntax</span></span>


```C++
virtual HRESULT OnDisconnect();
```



## <a name="parameters"></a><span data-ttu-id="be740-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="be740-106">Parameters</span></span>

<span data-ttu-id="be740-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="be740-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be740-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be740-108">Return value</span></span>

<span data-ttu-id="be740-109">Die Basisklassen Implementierung gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="be740-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="be740-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be740-110">Remarks</span></span>

<span data-ttu-id="be740-111">Die [**cbasepropertypage:: abtobjects**](cbasepropertypage-setobjects.md) -Methode ruft die- `OnDisconnect` Methode auf.</span><span class="sxs-lookup"><span data-stu-id="be740-111">The [**CBasePropertyPage::SetObjects**](cbasepropertypage-setobjects.md) method calls the `OnDisconnect` method.</span></span> <span data-ttu-id="be740-112">`OnDisconnect`Überschreiben Sie, um alle Zeiger freizugeben, die in der [**cbasepropertypage:: OnConnect**](cbasepropertypage-onconnect.md) -Methode abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="be740-112">Override `OnDisconnect` to release any pointers that were obtained in the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="be740-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be740-113">Examples</span></span>


```C++
HRESULT CMyProp::OnDisconnect(void)
{
    if (m_pOwningFilter)
    {
        m_pOwningFilter->Release();
        m_pOwningFilter = NULL;
    }
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="be740-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be740-114">Requirements</span></span>



| <span data-ttu-id="be740-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be740-115">Requirement</span></span> | <span data-ttu-id="be740-116">Wert</span><span class="sxs-lookup"><span data-stu-id="be740-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be740-117">Header</span><span class="sxs-lookup"><span data-stu-id="be740-117">Header</span></span><br/>  | <dl> <span data-ttu-id="be740-118"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be740-118"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="be740-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="be740-119">Library</span></span><br/> | <dl> <span data-ttu-id="be740-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="be740-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be740-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be740-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be740-122">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="be740-122">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




