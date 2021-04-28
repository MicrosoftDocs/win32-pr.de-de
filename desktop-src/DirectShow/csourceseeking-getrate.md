---
description: 'CSourceSeeking.GetRate-Methode: Die GetRate-Methode ruft die Wiedergaberate ab. Diese Methode implementiert die IMediaSeeking::GetRate-Methode.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: CSourceSeeking.GetRate-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fef379ef06cd0982f1eb5742ac2624d706ed73a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085228"
---
# <a name="csourceseekinggetrate-method"></a><span data-ttu-id="d5830-104">CSourceSeeking.GetRate-Methode</span><span class="sxs-lookup"><span data-stu-id="d5830-104">CSourceSeeking.GetRate method</span></span>

<span data-ttu-id="d5830-105">Die `GetRate` -Methode ruft die Wiedergaberate ab.</span><span class="sxs-lookup"><span data-stu-id="d5830-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="d5830-106">Diese Methode implementiert die [**IMediaSeeking::GetRate-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate)</span><span class="sxs-lookup"><span data-stu-id="d5830-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5830-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5830-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="d5830-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5830-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5830-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="d5830-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="d5830-110">Zeiger auf eine Variable, die die Wiedergaberate empfängt.</span><span class="sxs-lookup"><span data-stu-id="d5830-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5830-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5830-111">Return value</span></span>

<span data-ttu-id="d5830-112">Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.</span><span class="sxs-lookup"><span data-stu-id="d5830-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="d5830-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d5830-113">Return code</span></span>                                                                               | <span data-ttu-id="d5830-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5830-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="d5830-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d5830-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="d5830-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="d5830-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="d5830-117"><dt>**E \_ POINTER**</dt></span><span class="sxs-lookup"><span data-stu-id="d5830-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="d5830-118">**NULL-Zeigerwert**</span><span class="sxs-lookup"><span data-stu-id="d5830-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d5830-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5830-119">Remarks</span></span>

<span data-ttu-id="d5830-120">Die Wiedergaberate wird durch die [**Membervariable CSourceSeeking::m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="d5830-120">The playback rate is specified by the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5830-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5830-121">Requirements</span></span>



| <span data-ttu-id="d5830-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5830-122">Requirement</span></span> | <span data-ttu-id="d5830-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d5830-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5830-124">Header</span><span class="sxs-lookup"><span data-stu-id="d5830-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d5830-125"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5830-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d5830-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d5830-126">Library</span></span><br/> | <dl> <span data-ttu-id="d5830-127"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d5830-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5830-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d5830-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5830-129">**CSourceSeeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d5830-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




