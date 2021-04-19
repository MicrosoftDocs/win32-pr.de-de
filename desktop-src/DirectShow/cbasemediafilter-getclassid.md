---
description: 'Die GetClassID-Methode ruft den Klassen Bezeichner ab. Diese Methode implementiert die ipersistent:: GetClassID-Methode.'
ms.assetid: 95038b11-b56f-4ab9-aefa-4735651c3731
title: Cbasemediafilter. GetClassID-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dafacba684711c5c04a155d2609e0bc68450fa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369421"
---
# <a name="cbasemediafiltergetclassid-method"></a><span data-ttu-id="7e47c-104">Cbasemediafilter. GetClassID-Methode</span><span class="sxs-lookup"><span data-stu-id="7e47c-104">CBaseMediaFilter.GetClassID method</span></span>

<span data-ttu-id="7e47c-105">Die- `GetClassID` Methode ruft den Klassen Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="7e47c-105">The `GetClassID` method retrieves the class identifier.</span></span> <span data-ttu-id="7e47c-106">Diese Methode implementiert die **ipersistent:: GetClassID-** Methode.</span><span class="sxs-lookup"><span data-stu-id="7e47c-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e47c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e47c-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="7e47c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e47c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e47c-109">*pclsid*</span><span class="sxs-lookup"><span data-stu-id="7e47c-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="7e47c-110">Ein Zeiger auf eine Variable, die den Klassen Bezeichner empfängt.</span><span class="sxs-lookup"><span data-stu-id="7e47c-110">Pointer to a variable that receives the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e47c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e47c-111">Return value</span></span>

<span data-ttu-id="7e47c-112">Gibt den S \_ OK-oder E- \_ Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="7e47c-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e47c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e47c-113">Requirements</span></span>



| <span data-ttu-id="7e47c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e47c-114">Requirement</span></span> | <span data-ttu-id="7e47c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7e47c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e47c-116">Header</span><span class="sxs-lookup"><span data-stu-id="7e47c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7e47c-117"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e47c-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7e47c-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7e47c-118">Library</span></span><br/> | <dl> <span data-ttu-id="7e47c-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7e47c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e47c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e47c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e47c-121">**Cbasemediafilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7e47c-121">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




