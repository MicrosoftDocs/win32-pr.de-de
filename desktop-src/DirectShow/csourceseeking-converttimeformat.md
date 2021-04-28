---
description: 'CSourceSeeking.ConvertTimeFormat-Methode: Die ConvertTimeFormat-Methode konvertiert von einem Zeitformat in ein anderes. Diese Methode implementiert die IMediaSeeking::ConvertTimeFormat-Methode.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: CSourceSeeking.ConvertTimeFormat-Methode (Ctlutil.h)
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
ms.openlocfilehash: 6ba5c6808e091f48baac7d8928e327f45773e13a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085248"
---
# <a name="csourceseekingconverttimeformat-method"></a><span data-ttu-id="32b11-104">CSourceSeeking.ConvertTimeFormat-Methode</span><span class="sxs-lookup"><span data-stu-id="32b11-104">CSourceSeeking.ConvertTimeFormat method</span></span>

<span data-ttu-id="32b11-105">Die `ConvertTimeFormat` -Methode konvertiert von einem Zeitformat in ein anderes.</span><span class="sxs-lookup"><span data-stu-id="32b11-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="32b11-106">Diese Methode implementiert die [**IMediaSeeking::ConvertTimeFormat-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)</span><span class="sxs-lookup"><span data-stu-id="32b11-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="32b11-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="32b11-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="32b11-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="32b11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32b11-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="32b11-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="32b11-110">Zeiger auf eine Variable, die die konvertierte Zeit empfängt.</span><span class="sxs-lookup"><span data-stu-id="32b11-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="32b11-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="32b11-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="32b11-112">Zeiger auf die GUID des Zielformats.</span><span class="sxs-lookup"><span data-stu-id="32b11-112">Pointer to the GUID of the target format.</span></span> <span data-ttu-id="32b11-113">Bei **NULL** wird das aktuelle Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="32b11-113">If **NULL**, the current format is used.</span></span> <span data-ttu-id="32b11-114">Weitere Informationen finden Sie unter [**Zeitformat-GUIDs.**](time-format-guids.md)</span><span class="sxs-lookup"><span data-stu-id="32b11-114">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="32b11-115">*Quelle*</span><span class="sxs-lookup"><span data-stu-id="32b11-115">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="32b11-116">Der zu konvertierende Zeitwert.</span><span class="sxs-lookup"><span data-stu-id="32b11-116">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="32b11-117">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="32b11-117">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="32b11-118">Zeiger auf die GUID des Zeitformats des zu konvertierende Formats.</span><span class="sxs-lookup"><span data-stu-id="32b11-118">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="32b11-119">Bei **NULL** wird das aktuelle Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="32b11-119">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32b11-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32b11-120">Return value</span></span>

<span data-ttu-id="32b11-121">Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.</span><span class="sxs-lookup"><span data-stu-id="32b11-121">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="32b11-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="32b11-122">Return code</span></span>                                                                                  | <span data-ttu-id="32b11-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32b11-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="32b11-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="32b11-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="32b11-125">Erfolg</span><span class="sxs-lookup"><span data-stu-id="32b11-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="32b11-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="32b11-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="32b11-127">Ungültiges Argument</span><span class="sxs-lookup"><span data-stu-id="32b11-127">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="32b11-128"><dt>**E \_ POINTER**</dt></span><span class="sxs-lookup"><span data-stu-id="32b11-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="32b11-129">**NULL-Zeigerargument**</span><span class="sxs-lookup"><span data-stu-id="32b11-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="32b11-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32b11-130">Remarks</span></span>

<span data-ttu-id="32b11-131">Das einzige von der Basisklasse unterstützte Zeitformat ist TIME FORMAT MEDIA TIME (Einheiten von \_ \_ \_ 100 Nanosekunden).</span><span class="sxs-lookup"><span data-stu-id="32b11-131">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span> <span data-ttu-id="32b11-132">Diese Methode gibt E INVALIDARG zurück, außer in dem trivialen Fall, in dem \_ *sowohl pTargetFormat* als auch *pSourceFormat* TIME \_ FORMAT MEDIA TIME \_ \_ angeben.</span><span class="sxs-lookup"><span data-stu-id="32b11-132">This method returns E\_INVALIDARG, except in the trivial case where *pTargetFormat* and *pSourceFormat* both specify TIME\_FORMAT\_MEDIA\_TIME.</span></span>

## <a name="requirements"></a><span data-ttu-id="32b11-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32b11-133">Requirements</span></span>



| <span data-ttu-id="32b11-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32b11-134">Requirement</span></span> | <span data-ttu-id="32b11-135">Wert</span><span class="sxs-lookup"><span data-stu-id="32b11-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32b11-136">Header</span><span class="sxs-lookup"><span data-stu-id="32b11-136">Header</span></span><br/>  | <dl> <span data-ttu-id="32b11-137"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="32b11-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="32b11-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="32b11-138">Library</span></span><br/> | <dl> <span data-ttu-id="32b11-139"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="32b11-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b11-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="32b11-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b11-141">**CSourceSeeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="32b11-141">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




