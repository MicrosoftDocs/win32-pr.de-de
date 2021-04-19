---
description: 'Die querypreferredformat-Methode ruft das bevorzugte Zeitformat des Objekts ab. Diese Methode implementiert die imediaseeking:: querypreferredformat-Methode.'
ms.assetid: 3b73b7cf-1ba7-47c5-8442-5f138b74f335
title: Csourceseeking. querypreferredformat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8916e23756279dd30eaf177ef839944a4c68d61a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353010"
---
# <a name="csourceseekingquerypreferredformat-method"></a><span data-ttu-id="f7667-104">Csourceseeking. querypreferredformat-Methode</span><span class="sxs-lookup"><span data-stu-id="f7667-104">CSourceSeeking.QueryPreferredFormat method</span></span>

<span data-ttu-id="f7667-105">Die `QueryPreferredFormat` -Methode ruft das bevorzugte Zeitformat des Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="f7667-105">The `QueryPreferredFormat` method retrieves the object's preferred time format.</span></span> <span data-ttu-id="f7667-106">Diese Methode implementiert die [**imediaseeking:: querypreferredformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f7667-106">This method implements the [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7667-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7667-107">Syntax</span></span>


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="f7667-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7667-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7667-109">*pformat*</span><span class="sxs-lookup"><span data-stu-id="f7667-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="f7667-110">Ein Zeiger auf eine Variable, die eine Zeitformat-GUID empfängt.</span><span class="sxs-lookup"><span data-stu-id="f7667-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="f7667-111">Siehe [**Zeit Format-GUIDs**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="f7667-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7667-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7667-112">Return value</span></span>

<span data-ttu-id="f7667-113">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f7667-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="f7667-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f7667-114">Return code</span></span>                                                                               | <span data-ttu-id="f7667-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7667-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="f7667-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f7667-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="f7667-117">Erfolg</span><span class="sxs-lookup"><span data-stu-id="f7667-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="f7667-118"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="f7667-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="f7667-119">**Null** -Zeiger Wert</span><span class="sxs-lookup"><span data-stu-id="f7667-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7667-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7667-120">Remarks</span></span>

<span data-ttu-id="f7667-121">Das einzige von der Basisklasse unterstützte Zeitformat ist die Zeit \_ Format \_ Medien \_ Zeit (100-Nanosecond-Einheiten).</span><span class="sxs-lookup"><span data-stu-id="f7667-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7667-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7667-122">Requirements</span></span>



| <span data-ttu-id="f7667-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7667-123">Requirement</span></span> | <span data-ttu-id="f7667-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f7667-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7667-125">Header</span><span class="sxs-lookup"><span data-stu-id="f7667-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f7667-126"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7667-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f7667-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f7667-127">Library</span></span><br/> | <dl> <span data-ttu-id="f7667-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f7667-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7667-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7667-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7667-130">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f7667-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




