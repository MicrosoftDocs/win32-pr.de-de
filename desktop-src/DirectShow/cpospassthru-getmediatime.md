---
description: 'CPosPassThru.GetMediaTime-Methode: Die GetMediaTime-Methode ruft die Zeitstempel für das aktuelle Beispiel ab.'
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: CPosPassThru.GetMediaTime-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 328a0ae09c80a687863cfedb994f5a80cebebf14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095258"
---
# <a name="cpospassthrugetmediatime-method"></a><span data-ttu-id="f4af4-103">CPosPassThru.GetMediaTime-Methode</span><span class="sxs-lookup"><span data-stu-id="f4af4-103">CPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="f4af4-104">Die `GetMediaTime` -Methode ruft die Zeitstempel für das aktuelle Beispiel ab.</span><span class="sxs-lookup"><span data-stu-id="f4af4-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4af4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4af4-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="f4af4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4af4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4af4-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="f4af4-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="f4af4-108">Zeiger auf eine Variable, die die Startzeit in Einheiten des aktuellen Zeitformats empfängt.</span><span class="sxs-lookup"><span data-stu-id="f4af4-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="f4af4-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="f4af4-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="f4af4-110">Zeiger auf eine Variable, die die Endzeit in Einheiten des aktuellen Zeitformats empfängt.</span><span class="sxs-lookup"><span data-stu-id="f4af4-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4af4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4af4-111">Return value</span></span>

<span data-ttu-id="f4af4-112">Gibt E \_ FAIL zurück.</span><span class="sxs-lookup"><span data-stu-id="f4af4-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4af4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4af4-113">Remarks</span></span>

<span data-ttu-id="f4af4-114">Überschreiben Sie diese Methode, wenn Ihr Filter die Zeitstempel für die empfangenen Beispiele zwischenspeichert.</span><span class="sxs-lookup"><span data-stu-id="f4af4-114">Override this method if your filter caches the time stamps on the samples it receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4af4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4af4-115">Requirements</span></span>



| <span data-ttu-id="f4af4-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4af4-116">Requirement</span></span> | <span data-ttu-id="f4af4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f4af4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4af4-118">Header</span><span class="sxs-lookup"><span data-stu-id="f4af4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f4af4-119"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4af4-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f4af4-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f4af4-120">Library</span></span><br/> | <dl> <span data-ttu-id="f4af4-121"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f4af4-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4af4-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f4af4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4af4-123">**CPosPassThru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f4af4-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




