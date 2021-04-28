---
description: 'CSourceSeeking.SetTimeFormat-Methode: Die SetTimeFormat-Methode legt das Zeitformat fest. Diese Methode implementiert die IMediaSeeking::SetTimeFormat-Methode.'
ms.assetid: dbc7c950-8cc2-4f8e-adfa-8f5cdc1b56c7
title: CSourceSeeking.SetTimeFormat-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdb3889ecfa5bdcd49b4054822a2b2d09df58fa6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085198"
---
# <a name="csourceseekingsettimeformat-method"></a><span data-ttu-id="e8043-104">CSourceSeeking.SetTimeFormat-Methode</span><span class="sxs-lookup"><span data-stu-id="e8043-104">CSourceSeeking.SetTimeFormat method</span></span>

<span data-ttu-id="e8043-105">Die `SetTimeFormat` -Methode legt das Zeitformat fest.</span><span class="sxs-lookup"><span data-stu-id="e8043-105">The `SetTimeFormat` method sets the time format.</span></span> <span data-ttu-id="e8043-106">Diese Methode implementiert die [**IMediaSeeking::SetTimeFormat-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)</span><span class="sxs-lookup"><span data-stu-id="e8043-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8043-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8043-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="e8043-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8043-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8043-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="e8043-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="e8043-110">Zeiger auf eine GUID im Zeitformat.</span><span class="sxs-lookup"><span data-stu-id="e8043-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="e8043-111">Weitere Informationen finden Sie unter [**Zeitformat-GUIDs.**](time-format-guids.md)</span><span class="sxs-lookup"><span data-stu-id="e8043-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8043-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8043-112">Return value</span></span>

<span data-ttu-id="e8043-113">Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.</span><span class="sxs-lookup"><span data-stu-id="e8043-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="e8043-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e8043-114">Return code</span></span>                                                                                  | <span data-ttu-id="e8043-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8043-115">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="e8043-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e8043-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e8043-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e8043-117">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="e8043-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e8043-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e8043-119">Das angegebene Format wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e8043-119">Specified format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="e8043-120"><dt>**E \_ POINTER**</dt></span><span class="sxs-lookup"><span data-stu-id="e8043-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="e8043-121">**NULL-Zeigerargument.**</span><span class="sxs-lookup"><span data-stu-id="e8043-121">**NULL** pointer argument.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="e8043-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8043-122">Remarks</span></span>

<span data-ttu-id="e8043-123">Das einzige zeitformat, das von der Basisklasse unterstützt wird, ist TIME FORMAT MEDIA TIME (Einheiten von \_ \_ \_ 100 Nanosekunden).</span><span class="sxs-lookup"><span data-stu-id="e8043-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8043-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8043-124">Requirements</span></span>



| <span data-ttu-id="e8043-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8043-125">Requirement</span></span> | <span data-ttu-id="e8043-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e8043-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8043-127">Header</span><span class="sxs-lookup"><span data-stu-id="e8043-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e8043-128"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8043-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e8043-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e8043-129">Library</span></span><br/> | <dl> <span data-ttu-id="e8043-130"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e8043-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8043-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e8043-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8043-132">**CSourceSeeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e8043-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




