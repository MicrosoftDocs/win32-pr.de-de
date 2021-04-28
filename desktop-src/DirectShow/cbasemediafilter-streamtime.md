---
description: 'CBaseMediaFilter.StreamTime-Methode: Die StreamTime-Methode ruft die aktuelle Streamzeit ab.'
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: CBaseMediaFilter.StreamTime-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a90bb7d97825c14f11c75dd42d696fa302f8e3d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096248"
---
# <a name="cbasemediafilterstreamtime-method"></a><span data-ttu-id="936ec-103">CBaseMediaFilter.StreamTime-Methode</span><span class="sxs-lookup"><span data-stu-id="936ec-103">CBaseMediaFilter.StreamTime method</span></span>

<span data-ttu-id="936ec-104">Die `StreamTime` -Methode ruft die aktuelle Streamzeit ab.</span><span class="sxs-lookup"><span data-stu-id="936ec-104">The `StreamTime` method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="936ec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="936ec-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="936ec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="936ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="936ec-107">*rtStream* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="936ec-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="936ec-108">Verweis auf ein [**CRefTime-Objekt,**](creftime.md) das die aktuelle Streamzeit empfängt.</span><span class="sxs-lookup"><span data-stu-id="936ec-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="936ec-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="936ec-109">Return value</span></span>

<span data-ttu-id="936ec-110">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="936ec-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="936ec-111">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="936ec-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="936ec-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="936ec-112">Return code</span></span>                                                                                      | <span data-ttu-id="936ec-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="936ec-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="936ec-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="936ec-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="936ec-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="936ec-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="936ec-116"><dt>**VFW \_ E \_ NO \_ CLOCK**</dt></span><span class="sxs-lookup"><span data-stu-id="936ec-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="936ec-117">Es ist keine Referenzuhr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="936ec-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="936ec-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="936ec-118">Remarks</span></span>

<span data-ttu-id="936ec-119">Die Streamzeit wird als aktuelle Referenzzeit (wie von der Referenzuhr angegeben) abzüglich der Startzeit (angegeben durch [**CBaseMediaFilter::m \_ tStart**](cbasemediafilter-m-tstart.md)) definiert.</span><span class="sxs-lookup"><span data-stu-id="936ec-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseMediaFilter::m\_tStart**](cbasemediafilter-m-tstart.md)).</span></span> <span data-ttu-id="936ec-120">Der Zeitstempel eines Medienbeispiels gibt die Streamzeit an, zu der es gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="936ec-120">A media sample's time stamp specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="936ec-121">Wenn ein Beispiel mit einem Zeitstempel, der kleiner als die aktuelle Streamzeit ist, noch nicht gerendert wurde, ist es zu spät.</span><span class="sxs-lookup"><span data-stu-id="936ec-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

## <a name="requirements"></a><span data-ttu-id="936ec-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="936ec-122">Requirements</span></span>



| <span data-ttu-id="936ec-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="936ec-123">Requirement</span></span> | <span data-ttu-id="936ec-124">Wert</span><span class="sxs-lookup"><span data-stu-id="936ec-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="936ec-125">Header</span><span class="sxs-lookup"><span data-stu-id="936ec-125">Header</span></span><br/>  | <dl> <span data-ttu-id="936ec-126"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="936ec-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="936ec-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="936ec-127">Library</span></span><br/> | <dl> <span data-ttu-id="936ec-128"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="936ec-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="936ec-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="936ec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="936ec-130">**CBaseMediaFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="936ec-130">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




