---
description: 'Die converttimeformat-Methode konvertiert von einem Zeitformat in ein anderes. Diese Methode implementiert die imediaseeking:: converttimeformat-Methode.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: Csourceseeking. converttimeformat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3869ef5bc9656414ca5b465a04d04a4ca4be41e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354063"
---
# <a name="csourceseekingconverttimeformat-method"></a><span data-ttu-id="ef33c-104">Csourceseeking. converttimeformat-Methode</span><span class="sxs-lookup"><span data-stu-id="ef33c-104">CSourceSeeking.ConvertTimeFormat method</span></span>

<span data-ttu-id="ef33c-105">Die- `ConvertTimeFormat` Methode konvertiert von einem Zeitformat in ein anderes.</span><span class="sxs-lookup"><span data-stu-id="ef33c-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="ef33c-106">Diese Methode implementiert die [**imediaseeking:: converttimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ef33c-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef33c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef33c-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="ef33c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef33c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef33c-109">*pTARGET*</span><span class="sxs-lookup"><span data-stu-id="ef33c-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="ef33c-110">Ein Zeiger auf eine Variable, die die konvertierte Zeit empfängt.</span><span class="sxs-lookup"><span data-stu-id="ef33c-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="ef33c-111">*ptargetformat*</span><span class="sxs-lookup"><span data-stu-id="ef33c-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="ef33c-112">Zeiger auf die GUID des Ziel Formats.</span><span class="sxs-lookup"><span data-stu-id="ef33c-112">Pointer to the GUID of the target format.</span></span> <span data-ttu-id="ef33c-113">Wenn der Wert **null** ist, wird das aktuelle Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef33c-113">If **NULL**, the current format is used.</span></span> <span data-ttu-id="ef33c-114">Siehe [**Zeit Format-GUIDs**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="ef33c-114">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef33c-115">*Quelle*</span><span class="sxs-lookup"><span data-stu-id="ef33c-115">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="ef33c-116">Zeitwert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef33c-116">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="ef33c-117">*psourceformat*</span><span class="sxs-lookup"><span data-stu-id="ef33c-117">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="ef33c-118">Ein Zeiger auf die Zeitformat-GUID des zu konvertierenden Formats.</span><span class="sxs-lookup"><span data-stu-id="ef33c-118">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="ef33c-119">Wenn der Wert **null** ist, wird das aktuelle Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef33c-119">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef33c-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef33c-120">Return value</span></span>

<span data-ttu-id="ef33c-121">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ef33c-121">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="ef33c-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ef33c-122">Return code</span></span>                                                                                  | <span data-ttu-id="ef33c-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef33c-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="ef33c-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef33c-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ef33c-125">Erfolg</span><span class="sxs-lookup"><span data-stu-id="ef33c-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="ef33c-126"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ef33c-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ef33c-127">Ungültiges Argument</span><span class="sxs-lookup"><span data-stu-id="ef33c-127">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="ef33c-128"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="ef33c-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="ef33c-129">**Null** -Zeigerargument</span><span class="sxs-lookup"><span data-stu-id="ef33c-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef33c-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef33c-130">Remarks</span></span>

<span data-ttu-id="ef33c-131">Das einzige von der Basisklasse unterstützte Zeitformat ist die Zeit \_ Format \_ Medien \_ Zeit (100-Nanosecond-Einheiten).</span><span class="sxs-lookup"><span data-stu-id="ef33c-131">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span> <span data-ttu-id="ef33c-132">Diese Methode gibt E \_ invalidArg zurück, außer in dem trivialen Fall, in dem *ptargetformat* und *psourceformat* beide die Zeit \_ Format \_ Medien \_ Zeit angeben.</span><span class="sxs-lookup"><span data-stu-id="ef33c-132">This method returns E\_INVALIDARG, except in the trivial case where *pTargetFormat* and *pSourceFormat* both specify TIME\_FORMAT\_MEDIA\_TIME.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef33c-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef33c-133">Requirements</span></span>



| <span data-ttu-id="ef33c-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef33c-134">Requirement</span></span> | <span data-ttu-id="ef33c-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ef33c-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef33c-136">Header</span><span class="sxs-lookup"><span data-stu-id="ef33c-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ef33c-137"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef33c-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ef33c-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ef33c-138">Library</span></span><br/> | <dl> <span data-ttu-id="ef33c-139">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ef33c-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef33c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef33c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef33c-141">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ef33c-141">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




