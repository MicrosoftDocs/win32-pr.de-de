---
description: 'CSourceSeeking.GetTimeFormat-Methode: Die GetTimeFormat-Methode ruft das aktuelle Zeitformat ab. Diese Methode implementiert die IMediaSeeking::GetTimeFormat-Methode.'
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: CSourceSeeking.GetTimeFormat-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a56f9a490699d68d7a043e9385ad458562058f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085218"
---
# <a name="csourceseekinggettimeformat-method"></a><span data-ttu-id="7dc3a-104">CSourceSeeking.GetTimeFormat-Methode</span><span class="sxs-lookup"><span data-stu-id="7dc3a-104">CSourceSeeking.GetTimeFormat method</span></span>

<span data-ttu-id="7dc3a-105">Die `GetTimeFormat` -Methode ruft das aktuelle Zeitformat ab.</span><span class="sxs-lookup"><span data-stu-id="7dc3a-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="7dc3a-106">Diese Methode implementiert die [**IMediaSeeking::GetTimeFormat-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)</span><span class="sxs-lookup"><span data-stu-id="7dc3a-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc3a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7dc3a-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="7dc3a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7dc3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dc3a-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="7dc3a-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="7dc3a-110">Zeiger auf eine Variable, die eine Zeitformat-GUID empfängt.</span><span class="sxs-lookup"><span data-stu-id="7dc3a-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="7dc3a-111">Weitere Informationen finden Sie unter [**Zeitformat-GUIDs.**](time-format-guids.md)</span><span class="sxs-lookup"><span data-stu-id="7dc3a-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dc3a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7dc3a-112">Return value</span></span>

<span data-ttu-id="7dc3a-113">Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.</span><span class="sxs-lookup"><span data-stu-id="7dc3a-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="7dc3a-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7dc3a-114">Return code</span></span>                                                                               | <span data-ttu-id="7dc3a-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7dc3a-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="7dc3a-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7dc3a-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="7dc3a-117">Erfolg</span><span class="sxs-lookup"><span data-stu-id="7dc3a-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="7dc3a-118"><dt>**E \_ POINTER**</dt></span><span class="sxs-lookup"><span data-stu-id="7dc3a-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="7dc3a-119">**NULL-Zeigerwert**</span><span class="sxs-lookup"><span data-stu-id="7dc3a-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7dc3a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7dc3a-120">Remarks</span></span>

<span data-ttu-id="7dc3a-121">Das einzige zeitformat, das von der Basisklasse unterstützt wird, ist TIME FORMAT MEDIA TIME (Einheiten von \_ \_ \_ 100 Nanosekunden).</span><span class="sxs-lookup"><span data-stu-id="7dc3a-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc3a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7dc3a-122">Requirements</span></span>



| <span data-ttu-id="7dc3a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7dc3a-123">Requirement</span></span> | <span data-ttu-id="7dc3a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="7dc3a-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc3a-125">Header</span><span class="sxs-lookup"><span data-stu-id="7dc3a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7dc3a-126"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7dc3a-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7dc3a-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7dc3a-127">Library</span></span><br/> | <dl> <span data-ttu-id="7dc3a-128"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7dc3a-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dc3a-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7dc3a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc3a-130">**CSourceSeeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7dc3a-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




