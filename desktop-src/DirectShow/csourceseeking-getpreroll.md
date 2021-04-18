---
description: 'Die getpreroll-Methode ruft die Vorabversion ab. Diese Methode implementiert die imediaseeking:: getpreroll-Methode.'
ms.assetid: 2395d5b2-8c1f-40cd-8d4a-48620debe7a7
title: Csourceseeking. getpreroll-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 097af089a7221f005cf7f3aac74953166af3cb2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368599"
---
# <a name="csourceseekinggetpreroll-method"></a><span data-ttu-id="04143-104">Csourceseeking. getpreroll-Methode</span><span class="sxs-lookup"><span data-stu-id="04143-104">CSourceSeeking.GetPreroll method</span></span>

<span data-ttu-id="04143-105">Die- `GetPreroll` Methode ruft die Vorabversion ab.</span><span class="sxs-lookup"><span data-stu-id="04143-105">The `GetPreroll` method retrieves the preroll time.</span></span> <span data-ttu-id="04143-106">Diese Methode implementiert die [**imediaseeking:: getpreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) -Methode.</span><span class="sxs-lookup"><span data-stu-id="04143-106">This method implements the [**IMediaSeeking::GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="04143-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="04143-107">Syntax</span></span>


```C++
HRESULT GetPreroll(
   LONGLONG *pPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="04143-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="04143-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04143-109">*ppreroll*</span><span class="sxs-lookup"><span data-stu-id="04143-109">*pPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="04143-110">Ein Zeiger auf eine Variable, die die Vorabversion empfängt.</span><span class="sxs-lookup"><span data-stu-id="04143-110">Pointer to a variable that receives the preroll time.</span></span> <span data-ttu-id="04143-111">Der Wert wird auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04143-111">The value is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04143-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04143-112">Return value</span></span>

<span data-ttu-id="04143-113">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="04143-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="04143-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="04143-114">Return code</span></span>                                                                               | <span data-ttu-id="04143-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04143-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="04143-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="04143-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="04143-117">Erfolg</span><span class="sxs-lookup"><span data-stu-id="04143-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="04143-118"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="04143-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="04143-119">**Null** -Zeiger Wert</span><span class="sxs-lookup"><span data-stu-id="04143-119">**NULL** pointer value</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="04143-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04143-120">Requirements</span></span>



| <span data-ttu-id="04143-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04143-121">Requirement</span></span> | <span data-ttu-id="04143-122">Wert</span><span class="sxs-lookup"><span data-stu-id="04143-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04143-123">Header</span><span class="sxs-lookup"><span data-stu-id="04143-123">Header</span></span><br/>  | <dl> <span data-ttu-id="04143-124"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04143-124"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="04143-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="04143-125">Library</span></span><br/> | <dl> <span data-ttu-id="04143-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="04143-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04143-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04143-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04143-128">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="04143-128">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




