---
description: 'Die isformatsupported-Methode bestimmt, ob ein angegebenes Zeitformat unterstützt wird. Diese Methode implementiert die imediaseeking:: isformatsupported-Methode.'
ms.assetid: 79b6dfd4-7f03-479b-b855-8f389bf6cbc7
title: Csourceseeking. isformatsupported-Methode (ctlutil. h)
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
ms.openlocfilehash: 7d027a2ee6e94e4ccf4944c27e77f02d1d1c5edb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358613"
---
# <a name="csourceseekingisformatsupported-method"></a><span data-ttu-id="3c008-104">Csourceseeking. isformatsupported-Methode</span><span class="sxs-lookup"><span data-stu-id="3c008-104">CSourceSeeking.IsFormatSupported method</span></span>

<span data-ttu-id="3c008-105">Die- `IsFormatSupported` Methode bestimmt, ob ein angegebenes Zeitformat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3c008-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="3c008-106">Diese Methode implementiert die [**imediaseeking:: isformatsupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3c008-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c008-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c008-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="3c008-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c008-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c008-109">*pformat*</span><span class="sxs-lookup"><span data-stu-id="3c008-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="3c008-110">Zeiger auf eine Zeitformat-GUID.</span><span class="sxs-lookup"><span data-stu-id="3c008-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="3c008-111">Siehe [**Zeit Format-GUIDs**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3c008-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c008-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c008-112">Return value</span></span>

<span data-ttu-id="3c008-113">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="3c008-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="3c008-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3c008-114">Return code</span></span>                                                                               | <span data-ttu-id="3c008-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c008-115">Description</span></span>                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="3c008-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="3c008-116"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="3c008-117">Das Format wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c008-117">The format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="3c008-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3c008-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="3c008-119">Das Format wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c008-119">The format is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="3c008-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="3c008-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="3c008-121">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="3c008-121">**NULL** pointer argument.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="3c008-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c008-122">Remarks</span></span>

<span data-ttu-id="3c008-123">Das einzige von der Basisklasse unterstützte Zeitformat ist die Zeit \_ Format \_ Medien \_ Zeit (100-Nanosecond-Einheiten).</span><span class="sxs-lookup"><span data-stu-id="3c008-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c008-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c008-124">Requirements</span></span>



| <span data-ttu-id="3c008-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c008-125">Requirement</span></span> | <span data-ttu-id="3c008-126">Wert</span><span class="sxs-lookup"><span data-stu-id="3c008-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c008-127">Header</span><span class="sxs-lookup"><span data-stu-id="3c008-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3c008-128"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c008-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3c008-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3c008-129">Library</span></span><br/> | <dl> <span data-ttu-id="3c008-130">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3c008-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c008-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c008-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c008-132">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3c008-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




