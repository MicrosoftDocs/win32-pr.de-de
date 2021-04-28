---
description: 'CSourceSeeking.IsFormatSupported-Methode: Die IsFormatSupported-Methode bestimmt, ob ein angegebenes Zeitformat unterstützt wird. Diese Methode implementiert die IMediaSeeking::IsFormatSupported-Methode.'
ms.assetid: 79b6dfd4-7f03-479b-b855-8f389bf6cbc7
title: CSourceSeeking.IsFormatSupported-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c58e8edd908c101c3045e221cc86420cbb5cb94
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098748"
---
# <a name="csourceseekingisformatsupported-method"></a><span data-ttu-id="d6c6e-104">CSourceSeeking.IsFormatSupported-Methode</span><span class="sxs-lookup"><span data-stu-id="d6c6e-104">CSourceSeeking.IsFormatSupported method</span></span>

<span data-ttu-id="d6c6e-105">Die `IsFormatSupported` -Methode bestimmt, ob ein angegebenes Zeitformat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d6c6e-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="d6c6e-106">Diese Methode implementiert die [**IMediaSeeking::IsFormatSupported-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)</span><span class="sxs-lookup"><span data-stu-id="d6c6e-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6c6e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6c6e-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="d6c6e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6c6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6c6e-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="d6c6e-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="d6c6e-110">Zeiger auf eine GUID im Zeitformat.</span><span class="sxs-lookup"><span data-stu-id="d6c6e-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="d6c6e-111">Weitere Informationen finden Sie unter [**Zeitformat-GUIDs.**](time-format-guids.md)</span><span class="sxs-lookup"><span data-stu-id="d6c6e-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6c6e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6c6e-112">Return value</span></span>

<span data-ttu-id="d6c6e-113">Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.</span><span class="sxs-lookup"><span data-stu-id="d6c6e-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="d6c6e-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d6c6e-114">Return code</span></span>                                                                               | <span data-ttu-id="d6c6e-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6c6e-115">Description</span></span>                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="d6c6e-116"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="d6c6e-116"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="d6c6e-117">Das Format wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6c6e-117">The format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="d6c6e-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d6c6e-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="d6c6e-119">Das Format wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6c6e-119">The format is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="d6c6e-120"><dt>**E \_ POINTER**</dt></span><span class="sxs-lookup"><span data-stu-id="d6c6e-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="d6c6e-121">**NULL-Zeigerargument.**</span><span class="sxs-lookup"><span data-stu-id="d6c6e-121">**NULL** pointer argument.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="d6c6e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6c6e-122">Remarks</span></span>

<span data-ttu-id="d6c6e-123">Das einzige zeitformat, das von der Basisklasse unterstützt wird, ist TIME FORMAT MEDIA TIME (Einheiten von \_ \_ \_ 100 Nanosekunden).</span><span class="sxs-lookup"><span data-stu-id="d6c6e-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6c6e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6c6e-124">Requirements</span></span>



| <span data-ttu-id="d6c6e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6c6e-125">Requirement</span></span> | <span data-ttu-id="d6c6e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d6c6e-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c6e-127">Header</span><span class="sxs-lookup"><span data-stu-id="d6c6e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d6c6e-128"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6c6e-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d6c6e-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d6c6e-129">Library</span></span><br/> | <dl> <span data-ttu-id="d6c6e-130"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d6c6e-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6c6e-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d6c6e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6c6e-132">**CSourceSeeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d6c6e-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




