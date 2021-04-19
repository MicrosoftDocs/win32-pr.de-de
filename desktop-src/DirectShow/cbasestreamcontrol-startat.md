---
description: 'Die StartAt-Methode informiert die PIN, wann mit der Übermittlung von Daten begonnen werden soll. Diese Methode implementiert die iamstreamcontrol:: StartAt-Methode.'
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: Cbasestreamcontrol. StartAt-Methode ("strinmctl. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StartAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7adcf7cbd435992333bb8ae59d5ab1674056223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370492"
---
# <a name="cbasestreamcontrolstartat-method"></a><span data-ttu-id="70879-104">Cbasestreamcontrol. StartAt-Methode</span><span class="sxs-lookup"><span data-stu-id="70879-104">CBaseStreamControl.StartAt method</span></span>

<span data-ttu-id="70879-105">Die- `StartAt` Methode informiert den PIN, wann die Übermittlung von Daten beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="70879-105">The `StartAt` method informs the pin when to start delivering data.</span></span> <span data-ttu-id="70879-106">Diese Methode implementiert die [**iamstreamcontrol:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="70879-106">This method implements the [**IAMStreamControl::StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="70879-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="70879-107">Syntax</span></span>


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a><span data-ttu-id="70879-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="70879-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70879-109">*ptstart*</span><span class="sxs-lookup"><span data-stu-id="70879-109">*ptStart*</span></span> 
</dt> <dd>

<span data-ttu-id="70879-110">Ein Zeiger auf einen [**Verweis \_ Zeitwert**](reference-time.md) , der angibt, wann die PIN mit der Übermittlung von Daten beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="70879-110">Pointer to a [**REFERENCE\_TIME**](reference-time.md) value that specifies when the pin should start delivering data.</span></span>

</dd> <dt>

<span data-ttu-id="70879-111">*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="70879-111">*dwCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="70879-112">Gibt einen Wert an, der zusammen mit der Start Benachrichtigung gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="70879-112">Specifies a value to send along with the start notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70879-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70879-113">Return value</span></span>

<span data-ttu-id="70879-114">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="70879-114">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="70879-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70879-115">Requirements</span></span>



| <span data-ttu-id="70879-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70879-116">Requirement</span></span> | <span data-ttu-id="70879-117">Wert</span><span class="sxs-lookup"><span data-stu-id="70879-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70879-118">Header</span><span class="sxs-lookup"><span data-stu-id="70879-118">Header</span></span><br/>  | <dl> <span data-ttu-id="70879-119"><dt>"Strauch. h" (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70879-119"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="70879-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="70879-120">Library</span></span><br/> | <dl> <span data-ttu-id="70879-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="70879-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70879-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70879-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70879-123">**Cbasestreamcontrol-Klasse**</span><span class="sxs-lookup"><span data-stu-id="70879-123">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




