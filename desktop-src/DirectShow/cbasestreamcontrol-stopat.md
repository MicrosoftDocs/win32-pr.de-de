---
description: 'Die STOPAT-Methode informiert den PIN, wann die Übermittlung von Daten beendet werden soll. Diese Methode implementiert die iamstreamcontrol:: STOPAT-Methode.'
ms.assetid: cc9f0fdc-253b-4feb-95ce-56ebc575a49b
title: Cbasestreamcontrol. STOPAT-Methode ("strinmctl. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StopAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e6b794f5f05721f403d943252c2aabd48614519
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373564"
---
# <a name="cbasestreamcontrolstopat-method"></a><span data-ttu-id="154b1-104">Cbasestreamcontrol. STOPAT-Methode</span><span class="sxs-lookup"><span data-stu-id="154b1-104">CBaseStreamControl.StopAt method</span></span>

<span data-ttu-id="154b1-105">Die- `StopAt` Methode informiert den PIN, wann die Übermittlung von Daten beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="154b1-105">The `StopAt` method informs the pin when to stop delivering data.</span></span> <span data-ttu-id="154b1-106">Diese Methode implementiert die [**iamstreamcontrol:: STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="154b1-106">This method implements the [**IAMStreamControl::StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="154b1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="154b1-107">Syntax</span></span>


```C++
HRESULT StopAt(
   const REFERENCE_TIME *ptStop = NULL,
         BOOL           bSendExtra = FALSE,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a><span data-ttu-id="154b1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="154b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="154b1-109">*ptstopps*</span><span class="sxs-lookup"><span data-stu-id="154b1-109">*ptStop*</span></span> 
</dt> <dd>

<span data-ttu-id="154b1-110">Ein Zeiger auf einen [**Verweis \_ Zeitwert**](reference-time.md) , der angibt, wann die PIN die Übermittlung von Daten beenden soll.</span><span class="sxs-lookup"><span data-stu-id="154b1-110">Pointer to a [**REFERENCE\_TIME**](reference-time.md) value that specifies when the pin should stop delivering data.</span></span>

</dd> <dt>

<span data-ttu-id="154b1-111">*bsendextra*</span><span class="sxs-lookup"><span data-stu-id="154b1-111">*bSendExtra*</span></span> 
</dt> <dd>

<span data-ttu-id="154b1-112">Gibt einen booleschen Wert an, der angibt, ob nach der geplanten Endzeit ein zusätzliches Beispiel gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="154b1-112">Specifies a Boolean value that indicates whether to send an extra sample after the scheduled stop time.</span></span> <span data-ttu-id="154b1-113">**True** gibt an, dass die PIN ein zusätzliches Beispiel sendet.</span><span class="sxs-lookup"><span data-stu-id="154b1-113">If **TRUE**, the pin sends one extra sample.</span></span>

</dd> <dt>

<span data-ttu-id="154b1-114">*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="154b1-114">*dwCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="154b1-115">Gibt einen Wert an, der zusammen mit der Start Benachrichtigung gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="154b1-115">Specifies a value to send along with the start notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="154b1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="154b1-116">Return value</span></span>

<span data-ttu-id="154b1-117">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="154b1-117">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="154b1-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="154b1-118">Requirements</span></span>



| <span data-ttu-id="154b1-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="154b1-119">Requirement</span></span> | <span data-ttu-id="154b1-120">Wert</span><span class="sxs-lookup"><span data-stu-id="154b1-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="154b1-121">Header</span><span class="sxs-lookup"><span data-stu-id="154b1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="154b1-122"><dt>"Strauch. h" (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="154b1-122"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="154b1-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="154b1-123">Library</span></span><br/> | <dl> <span data-ttu-id="154b1-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="154b1-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="154b1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="154b1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="154b1-126">**Cbasestreamcontrol-Klasse**</span><span class="sxs-lookup"><span data-stu-id="154b1-126">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




