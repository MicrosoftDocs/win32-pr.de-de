---
description: 'CSourceSeeking.GetDuration-Methode: Die GetDuration-Methode ruft die Dauer des Streams ab. Diese Methode implementiert die IMediaSeeking::GetDuration-Methode.'
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: CSourceSeeking.GetDuration-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d5b961ad62d65c1f728af71e82de1373ea20b1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098768"
---
# <a name="csourceseekinggetduration-method"></a><span data-ttu-id="4a634-104">CSourceSeeking.GetDuration-Methode</span><span class="sxs-lookup"><span data-stu-id="4a634-104">CSourceSeeking.GetDuration method</span></span>

<span data-ttu-id="4a634-105">Die `GetDuration` -Methode ruft die Dauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="4a634-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="4a634-106">Diese Methode implementiert die [**IMediaSeeking::GetDuration-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration)</span><span class="sxs-lookup"><span data-stu-id="4a634-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a634-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a634-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="4a634-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a634-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a634-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="4a634-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="4a634-110">Zeiger auf eine Variable, die die Dauer in Einheiten des aktuellen Zeitformats empfängt.</span><span class="sxs-lookup"><span data-stu-id="4a634-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a634-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a634-111">Return value</span></span>

<span data-ttu-id="4a634-112">Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.</span><span class="sxs-lookup"><span data-stu-id="4a634-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="4a634-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4a634-113">Return code</span></span>                                                                               | <span data-ttu-id="4a634-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a634-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="4a634-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4a634-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="4a634-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="4a634-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="4a634-117"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="4a634-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="4a634-118">**NULL-Zeigerwert**</span><span class="sxs-lookup"><span data-stu-id="4a634-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a634-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a634-119">Remarks</span></span>

<span data-ttu-id="4a634-120">Die Dauer wird von der [**CSourceSeeking::m \_ rtDuration-Membervariablen**](csourceseeking-m-rtduration.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="4a634-120">The duration is specified by the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a634-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a634-121">Requirements</span></span>



| <span data-ttu-id="4a634-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a634-122">Requirement</span></span> | <span data-ttu-id="4a634-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4a634-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a634-124">Header</span><span class="sxs-lookup"><span data-stu-id="4a634-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4a634-125"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a634-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a634-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4a634-126">Library</span></span><br/> | <dl> <span data-ttu-id="4a634-127"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4a634-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a634-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4a634-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a634-129">**CSourceSeeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4a634-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




