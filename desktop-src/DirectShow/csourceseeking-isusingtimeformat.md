---
description: Die isusingtimeformat-Methode bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist.
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: Csourceseeking. isusingtimeformat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8229387364a061febc7bd825e7bc76ee5d9b4a2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354644"
---
# <a name="csourceseekingisusingtimeformat-method"></a><span data-ttu-id="c7387-103">Csourceseeking. isusingtimeformat-Methode</span><span class="sxs-lookup"><span data-stu-id="c7387-103">CSourceSeeking.IsUsingTimeFormat method</span></span>

<span data-ttu-id="c7387-104">Die- `IsUsingTimeFormat` Methode bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist.</span><span class="sxs-lookup"><span data-stu-id="c7387-104">The `IsUsingTimeFormat` method determines whether a specified time format is the format currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7387-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7387-105">Syntax</span></span>


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="c7387-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7387-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7387-107">*pformat*</span><span class="sxs-lookup"><span data-stu-id="c7387-107">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="c7387-108">Zeiger auf eine Zeitformat-GUID.</span><span class="sxs-lookup"><span data-stu-id="c7387-108">Pointer to a time format GUID.</span></span> <span data-ttu-id="c7387-109">Siehe [**Zeit Format-GUIDs**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="c7387-109">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7387-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7387-110">Return value</span></span>

<span data-ttu-id="c7387-111">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c7387-111">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="c7387-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c7387-112">Return code</span></span>                                                                               | <span data-ttu-id="c7387-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7387-113">Description</span></span>                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="c7387-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c7387-114"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="c7387-115">Das angegebene Format ist nicht das aktuelle Format.</span><span class="sxs-lookup"><span data-stu-id="c7387-115">The specified format is not the current format.</span></span><br/> |
| <dl> <span data-ttu-id="c7387-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c7387-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="c7387-117">Das angegebene Format ist das aktuelle Format.</span><span class="sxs-lookup"><span data-stu-id="c7387-117">The specified format is the current format.</span></span><br/>     |
| <dl> <span data-ttu-id="c7387-118"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="c7387-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="c7387-119">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="c7387-119">**NULL** pointer argument.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="c7387-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7387-120">Remarks</span></span>

<span data-ttu-id="c7387-121">Das einzige von der Basisklasse unterstützte Zeitformat ist die Zeit \_ Format \_ Medien \_ Zeit (100-Nanosecond-Einheiten).</span><span class="sxs-lookup"><span data-stu-id="c7387-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7387-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7387-122">Requirements</span></span>



| <span data-ttu-id="c7387-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7387-123">Requirement</span></span> | <span data-ttu-id="c7387-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c7387-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7387-125">Header</span><span class="sxs-lookup"><span data-stu-id="c7387-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c7387-126"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7387-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c7387-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c7387-127">Library</span></span><br/> | <dl> <span data-ttu-id="c7387-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c7387-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7387-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7387-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7387-130">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c7387-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




