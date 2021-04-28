---
description: 'CPosPassThru.GetDuration-Methode: Die GetDuration-Methode ruft die Dauer des Streams ab. Diese Methode implementiert die IMediaSeeking::GetDuration-Methode.'
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: CPosPassThru.GetDuration-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b0af7bfaca405ed52a4e3c5a63c18b4bc087ba3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085578"
---
# <a name="cpospassthrugetduration-method"></a><span data-ttu-id="ef08c-104">CPosPassThru.GetDuration-Methode</span><span class="sxs-lookup"><span data-stu-id="ef08c-104">CPosPassThru.GetDuration method</span></span>

<span data-ttu-id="ef08c-105">Die `GetDuration` -Methode ruft die Dauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="ef08c-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="ef08c-106">Diese Methode implementiert die [**IMediaSeeking::GetDuration-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration)</span><span class="sxs-lookup"><span data-stu-id="ef08c-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef08c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef08c-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="ef08c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef08c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef08c-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="ef08c-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="ef08c-110">Zeiger auf eine Variable, die die Dauer in Einheiten des aktuellen Zeitformats empfängt.</span><span class="sxs-lookup"><span data-stu-id="ef08c-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef08c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef08c-111">Return value</span></span>

<span data-ttu-id="ef08c-112">Gibt den **HRESULT-Wert** aus dem verbundenen Pin zurück.</span><span class="sxs-lookup"><span data-stu-id="ef08c-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef08c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef08c-113">Requirements</span></span>



| <span data-ttu-id="ef08c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef08c-114">Requirement</span></span> | <span data-ttu-id="ef08c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ef08c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef08c-116">Header</span><span class="sxs-lookup"><span data-stu-id="ef08c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ef08c-117"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef08c-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ef08c-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ef08c-118">Library</span></span><br/> | <dl> <span data-ttu-id="ef08c-119"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ef08c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef08c-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ef08c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef08c-121">**CPosPassThru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ef08c-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




