---
description: Die onapplychanges-Methode wird aufgerufen, wenn der Benutzer Änderungen auf die Eigenschaften Seite anwendet.
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: Cbasepropertypage. onapplychanges-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnApplyChanges
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbcea308a8daaa8b9fdf15be765dc5d3a0df182c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369256"
---
# <a name="cbasepropertypageonapplychanges-method"></a><span data-ttu-id="f993d-103">Cbasepropertypage. onapplychanges-Methode</span><span class="sxs-lookup"><span data-stu-id="f993d-103">CBasePropertyPage.OnApplyChanges method</span></span>

<span data-ttu-id="f993d-104">Die- `OnApplyChanges` Methode wird aufgerufen, wenn der Benutzer Änderungen auf der Eigenschaften Seite anwendet.</span><span class="sxs-lookup"><span data-stu-id="f993d-104">The `OnApplyChanges` method is called when the user applies changes to the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="f993d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f993d-105">Syntax</span></span>


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a><span data-ttu-id="f993d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f993d-106">Parameters</span></span>

<span data-ttu-id="f993d-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f993d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f993d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f993d-108">Return value</span></span>

<span data-ttu-id="f993d-109">Die Basisklassen Implementierung gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="f993d-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f993d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f993d-110">Remarks</span></span>

<span data-ttu-id="f993d-111">Die [**cbasepropertypage:: apply**](cbasepropertypage-apply.md) -Methode ruft auf, `OnApplyChanges` Wenn das [**\_ bdirty-Flag "cbasepropertypage:: m**](cbasepropertypage-m-bdirty.md) " auf " **true**" fest.</span><span class="sxs-lookup"><span data-stu-id="f993d-111">The [**CBasePropertyPage::Apply**](cbasepropertypage-apply.md) method calls `OnApplyChanges` if the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag is **TRUE**.</span></span> <span data-ttu-id="f993d-112">`OnApplyChanges`Überschreiben Sie, um die Änderungen zu verarbeiten und **m \_ bdirty** auf **false** zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="f993d-112">Override `OnApplyChanges` to process the changes and reset **m\_bDirty** to **FALSE**.</span></span>

## <a name="examples"></a><span data-ttu-id="f993d-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f993d-113">Examples</span></span>


```C++
HRESULT CMyProp::OnApplyChanges(void)
{
    ASSERT(m_pOwningFilter != NULL);
    return m_pOwningFilter->SetSomeProperty(&m_lNewVal);
}
```



## <a name="requirements"></a><span data-ttu-id="f993d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f993d-114">Requirements</span></span>



| <span data-ttu-id="f993d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f993d-115">Requirement</span></span> | <span data-ttu-id="f993d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f993d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f993d-117">Header</span><span class="sxs-lookup"><span data-stu-id="f993d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f993d-118"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f993d-118"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="f993d-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f993d-119">Library</span></span><br/> | <dl> <span data-ttu-id="f993d-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f993d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f993d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f993d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f993d-122">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f993d-122">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




