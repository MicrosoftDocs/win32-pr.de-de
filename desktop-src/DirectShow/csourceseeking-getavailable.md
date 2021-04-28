---
description: 'CSourceSeeking.GetAvailable-Methode: Die GetAvailable-Methode ruft den Zeitbereich ab, in dem Suchfunktionen effizient sind. Diese Methode implementiert die IMediaSeeking::GetAvailable-Methode.'
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: CSourceSeeking.GetAvailable-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24bc667eec4f5b21c90415e4721aa8cf0a0ad4c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085238"
---
# <a name="csourceseekinggetavailable-method"></a><span data-ttu-id="b9614-104">CSourceSeeking.GetAvailable-Methode</span><span class="sxs-lookup"><span data-stu-id="b9614-104">CSourceSeeking.GetAvailable method</span></span>

<span data-ttu-id="b9614-105">Die `GetAvailable` -Methode ruft den Zeitbereich ab, in dem Suchfunktionen effizient sind.</span><span class="sxs-lookup"><span data-stu-id="b9614-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="b9614-106">Diese Methode implementiert die [**IMediaSeeking::GetAvailable-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable)</span><span class="sxs-lookup"><span data-stu-id="b9614-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9614-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9614-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="b9614-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9614-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9614-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="b9614-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="b9614-110">Zeiger auf eine Variable, die die früheste Zeit für effiziente Suche empfängt.</span><span class="sxs-lookup"><span data-stu-id="b9614-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span> <span data-ttu-id="b9614-111">Die Variable ist auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b9614-111">The variable is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b9614-112">*pLatest*</span><span class="sxs-lookup"><span data-stu-id="b9614-112">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="b9614-113">Zeiger auf eine Variable, die die letzte Zeit für effiziente Suche empfängt.</span><span class="sxs-lookup"><span data-stu-id="b9614-113">Pointer to a variable that receives the latest time for efficient seeking.</span></span> <span data-ttu-id="b9614-114">Die Variable wird auf den Wert der [**CSourceSeeking::m \_ rtDuration-Membervariablen**](csourceseeking-m-rtduration.md) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b9614-114">The variable is set to the value of the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9614-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9614-115">Return value</span></span>

<span data-ttu-id="b9614-116">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b9614-116">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9614-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9614-117">Requirements</span></span>



| <span data-ttu-id="b9614-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9614-118">Requirement</span></span> | <span data-ttu-id="b9614-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b9614-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9614-120">Header</span><span class="sxs-lookup"><span data-stu-id="b9614-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b9614-121"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9614-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b9614-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b9614-122">Library</span></span><br/> | <dl> <span data-ttu-id="b9614-123"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b9614-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9614-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b9614-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9614-125">**CSourceSeeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b9614-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




