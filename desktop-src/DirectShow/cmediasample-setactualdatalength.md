---
description: 'Die setactualdatalength-Methode legt die Länge der gültigen Daten im Puffer fest. Diese Methode implementiert die imediasample:: setactualdatalength-Methode.'
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: Cmediasample. setactualdatalength-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825b02f43195424f9ceb5ecd23c4dcf26727ef8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360313"
---
# <a name="cmediasamplesetactualdatalength-method"></a><span data-ttu-id="c344c-104">Cmediasample. setactualdatalength-Methode</span><span class="sxs-lookup"><span data-stu-id="c344c-104">CMediaSample.SetActualDataLength method</span></span>

<span data-ttu-id="c344c-105">Die- `SetActualDataLength` Methode legt die Länge der gültigen Daten im Puffer fest.</span><span class="sxs-lookup"><span data-stu-id="c344c-105">The `SetActualDataLength` method sets the length of the valid data in the buffer.</span></span> <span data-ttu-id="c344c-106">Diese Methode implementiert die [**imediasample:: setactualdatalength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c344c-106">This method implements the [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c344c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c344c-107">Syntax</span></span>


```C++
HRESULT SetActualDataLength(
   long lLen
);
```



## <a name="parameters"></a><span data-ttu-id="c344c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c344c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c344c-109">*Verdammten*</span><span class="sxs-lookup"><span data-stu-id="c344c-109">*lLen*</span></span> 
</dt> <dd>

<span data-ttu-id="c344c-110">Länge der gültigen Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c344c-110">Length of the valid data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c344c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c344c-111">Return value</span></span>

<span data-ttu-id="c344c-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c344c-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="c344c-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c344c-113">Return code</span></span>                                                                                             | <span data-ttu-id="c344c-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c344c-114">Description</span></span>                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="c344c-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c344c-115"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="c344c-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="c344c-116">Success.</span></span><br/>                                         |
| <dl> <span data-ttu-id="c344c-117"><dt>**VFW \_ E- \_ Puffer \_ Überlauf**</dt></span><span class="sxs-lookup"><span data-stu-id="c344c-117"><dt>**VFW\_E\_BUFFER\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="c344c-118">*lLen* ist größer als die zugeordnete Puffergröße.</span><span class="sxs-lookup"><span data-stu-id="c344c-118">*lLen* is larger than the allocated buffer size.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c344c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c344c-119">Remarks</span></span>

<span data-ttu-id="c344c-120">Diese Methode legt die Element Variable [**cmediasample: \_ : m**](cmediasample-m-lactual.md) fest.</span><span class="sxs-lookup"><span data-stu-id="c344c-120">This method sets the [**CMediaSample::m\_lActual**](cmediasample-m-lactual.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="c344c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c344c-121">Requirements</span></span>



| <span data-ttu-id="c344c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c344c-122">Requirement</span></span> | <span data-ttu-id="c344c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c344c-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c344c-124">Header</span><span class="sxs-lookup"><span data-stu-id="c344c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c344c-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c344c-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c344c-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c344c-126">Library</span></span><br/> | <dl> <span data-ttu-id="c344c-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c344c-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c344c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c344c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c344c-129">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c344c-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




