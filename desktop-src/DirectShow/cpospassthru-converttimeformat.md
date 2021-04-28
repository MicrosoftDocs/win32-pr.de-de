---
description: 'CPosPassThru.ConvertTimeFormat-Methode: Die ConvertTimeFormat-Methode konvertiert von einem Zeitformat in ein anderes. Diese Methode implementiert die IMediaSeeking::ConvertTimeFormat-Methode.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: CPosPassThru.ConvertTimeFormat-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc463cb6dc891e677266289971a1dac8b335a8c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098958"
---
# <a name="cpospassthruconverttimeformat-method"></a><span data-ttu-id="f36d8-104">CPosPassThru.ConvertTimeFormat-Methode</span><span class="sxs-lookup"><span data-stu-id="f36d8-104">CPosPassThru.ConvertTimeFormat method</span></span>

<span data-ttu-id="f36d8-105">Die `ConvertTimeFormat` -Methode konvertiert von einem Zeitformat in ein anderes.</span><span class="sxs-lookup"><span data-stu-id="f36d8-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="f36d8-106">Diese Methode implementiert die [**IMediaSeeking::ConvertTimeFormat-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)</span><span class="sxs-lookup"><span data-stu-id="f36d8-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f36d8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f36d8-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="f36d8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f36d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f36d8-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="f36d8-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="f36d8-110">Zeiger auf eine Variable, die die konvertierte Zeit empfängt.</span><span class="sxs-lookup"><span data-stu-id="f36d8-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="f36d8-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="f36d8-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="f36d8-112">Zeiger auf die GUID des Zeitformats des Zielformats.</span><span class="sxs-lookup"><span data-stu-id="f36d8-112">Pointer to the time format GUID of the target format.</span></span> <span data-ttu-id="f36d8-113">Bei **NULL** wird das aktuelle Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="f36d8-113">If **NULL**, the current format is used.</span></span>

</dd> <dt>

<span data-ttu-id="f36d8-114">*Quelle*</span><span class="sxs-lookup"><span data-stu-id="f36d8-114">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="f36d8-115">Der zu konvertierende Zeitwert.</span><span class="sxs-lookup"><span data-stu-id="f36d8-115">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="f36d8-116">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="f36d8-116">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="f36d8-117">Zeiger auf die Guid des Zeitformats des zu konvertierende Formats.</span><span class="sxs-lookup"><span data-stu-id="f36d8-117">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="f36d8-118">Bei **NULL** wird das aktuelle Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="f36d8-118">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f36d8-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f36d8-119">Return value</span></span>

<span data-ttu-id="f36d8-120">Gibt den **HRESULT-Wert** aus dem verbundenen Pin zurück.</span><span class="sxs-lookup"><span data-stu-id="f36d8-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="f36d8-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f36d8-121">Requirements</span></span>



| <span data-ttu-id="f36d8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f36d8-122">Requirement</span></span> | <span data-ttu-id="f36d8-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f36d8-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f36d8-124">Header</span><span class="sxs-lookup"><span data-stu-id="f36d8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f36d8-125"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f36d8-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f36d8-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f36d8-126">Library</span></span><br/> | <dl> <span data-ttu-id="f36d8-127"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f36d8-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f36d8-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f36d8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f36d8-129">**CPosPassThru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f36d8-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="f36d8-130">**Zeitformat-GUIDs**</span><span class="sxs-lookup"><span data-stu-id="f36d8-130">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




