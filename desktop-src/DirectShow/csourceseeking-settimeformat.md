---
description: 'Die settimeformat-Methode legt das Zeitformat fest. Diese Methode implementiert die imediaseeking:: settimeformat-Methode.'
ms.assetid: dbc7c950-8cc2-4f8e-adfa-8f5cdc1b56c7
title: Csourceseeking. settimeformat-Methode (ctlutil. h)
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
ms.openlocfilehash: 61ab0cdf7c954e0fa5f370127f00529bb9ef7b16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364497"
---
# <a name="csourceseekingsettimeformat-method"></a><span data-ttu-id="f2c58-104">Csourceseeking. settimeformat-Methode</span><span class="sxs-lookup"><span data-stu-id="f2c58-104">CSourceSeeking.SetTimeFormat method</span></span>

<span data-ttu-id="f2c58-105">Die- `SetTimeFormat` Methode legt das Zeitformat fest.</span><span class="sxs-lookup"><span data-stu-id="f2c58-105">The `SetTimeFormat` method sets the time format.</span></span> <span data-ttu-id="f2c58-106">Diese Methode implementiert die [**imediaseeking:: settimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f2c58-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2c58-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2c58-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="f2c58-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2c58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2c58-109">*pformat*</span><span class="sxs-lookup"><span data-stu-id="f2c58-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="f2c58-110">Zeiger auf eine Zeitformat-GUID.</span><span class="sxs-lookup"><span data-stu-id="f2c58-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="f2c58-111">Siehe [**Zeit Format-GUIDs**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="f2c58-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2c58-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2c58-112">Return value</span></span>

<span data-ttu-id="f2c58-113">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f2c58-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="f2c58-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f2c58-114">Return code</span></span>                                                                                  | <span data-ttu-id="f2c58-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2c58-115">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="f2c58-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f2c58-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f2c58-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="f2c58-117">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="f2c58-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="f2c58-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f2c58-119">Das angegebene Format wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f2c58-119">Specified format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="f2c58-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="f2c58-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="f2c58-121">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="f2c58-121">**NULL** pointer argument.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="f2c58-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2c58-122">Remarks</span></span>

<span data-ttu-id="f2c58-123">Das einzige von der Basisklasse unterstützte Zeitformat ist die Zeit \_ Format \_ Medien \_ Zeit (100-Nanosecond-Einheiten).</span><span class="sxs-lookup"><span data-stu-id="f2c58-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2c58-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2c58-124">Requirements</span></span>



| <span data-ttu-id="f2c58-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2c58-125">Requirement</span></span> | <span data-ttu-id="f2c58-126">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c58-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c58-127">Header</span><span class="sxs-lookup"><span data-stu-id="f2c58-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f2c58-128"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2c58-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f2c58-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2c58-129">Library</span></span><br/> | <dl> <span data-ttu-id="f2c58-130">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f2c58-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2c58-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2c58-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2c58-132">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f2c58-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




