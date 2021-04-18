---
description: 'Die ispagedirty-Methode gibt an, ob die Eigenschaften Seite seit der Aktivierung oder seit dem letzten Aufrufen von IPropertyPage:: apply geändert wurde. Diese Methode implementiert die IPropertyPage:: ispagedirty-Methode.'
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: Cbasepropertypage. ispagedirty-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.IsPageDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c69c2e7d480f63542e146c73e56b9e692693f665
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371443"
---
# <a name="cbasepropertypageispagedirty-method"></a><span data-ttu-id="2b6ca-104">Cbasepropertypage. ispagedirty-Methode</span><span class="sxs-lookup"><span data-stu-id="2b6ca-104">CBasePropertyPage.IsPageDirty method</span></span>

<span data-ttu-id="2b6ca-105">Die- `IsPageDirty` Methode gibt an, ob die Eigenschaften Seite seit der Aktivierung oder seit dem letzten Aufrufen von **IPropertyPage:: apply** geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="2b6ca-105">The `IsPageDirty` method indicates whether the property page has changed since it was activated or since the most recent call to **IPropertyPage::Apply**.</span></span> <span data-ttu-id="2b6ca-106">Diese Methode implementiert die **IPropertyPage:: ispagedirty** -Methode.</span><span class="sxs-lookup"><span data-stu-id="2b6ca-106">This method implements the **IPropertyPage::IsPageDirty** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b6ca-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b6ca-107">Syntax</span></span>


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a><span data-ttu-id="2b6ca-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b6ca-108">Parameters</span></span>

<span data-ttu-id="2b6ca-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2b6ca-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b6ca-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b6ca-110">Return value</span></span>

<span data-ttu-id="2b6ca-111">Gibt "s OK" zurück \_ , wenn " [**cbasepropertypage:: m \_ bdirty**](cbasepropertypage-m-bdirty.md) " den Wert **true** hat, \_ andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="2b6ca-111">Returns S\_OK if [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) is **TRUE**, or S\_FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b6ca-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b6ca-112">Requirements</span></span>



| <span data-ttu-id="2b6ca-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b6ca-113">Requirement</span></span> | <span data-ttu-id="2b6ca-114">Wert</span><span class="sxs-lookup"><span data-stu-id="2b6ca-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b6ca-115">Header</span><span class="sxs-lookup"><span data-stu-id="2b6ca-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2b6ca-116"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b6ca-116"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="2b6ca-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2b6ca-117">Library</span></span><br/> | <dl> <span data-ttu-id="2b6ca-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2b6ca-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b6ca-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b6ca-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b6ca-120">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2b6ca-120">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




