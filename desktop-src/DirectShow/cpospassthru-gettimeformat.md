---
description: 'CPosPassThru.GetTimeFormat-Methode: Die GetTimeFormat-Methode ruft das aktuelle Zeitformat ab. Diese Methode implementiert die IMediaSeeking::GetTimeFormat-Methode.'
ms.assetid: 445c1873-da6f-42be-a4cf-0c475c5f0723
title: CPosPassThru.GetTimeFormat-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 903d1c6163d4cad5c5b9ca22213b02542bb3da49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085588"
---
# <a name="cpospassthrugettimeformat-method"></a><span data-ttu-id="78c24-104">CPosPassThru.GetTimeFormat-Methode</span><span class="sxs-lookup"><span data-stu-id="78c24-104">CPosPassThru.GetTimeFormat method</span></span>

<span data-ttu-id="78c24-105">Die `GetTimeFormat` -Methode ruft das aktuelle Zeitformat ab.</span><span class="sxs-lookup"><span data-stu-id="78c24-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="78c24-106">Diese Methode implementiert die [**IMediaSeeking::GetTimeFormat-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)</span><span class="sxs-lookup"><span data-stu-id="78c24-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="78c24-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="78c24-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="78c24-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="78c24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78c24-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="78c24-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="78c24-110">Zeiger auf eine Variable, die eine Zeitformat-GUID empfängt.</span><span class="sxs-lookup"><span data-stu-id="78c24-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78c24-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78c24-111">Return value</span></span>

<span data-ttu-id="78c24-112">Gibt den **HRESULT-Wert** aus dem verbundenen Pin zurück.</span><span class="sxs-lookup"><span data-stu-id="78c24-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="78c24-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78c24-113">Requirements</span></span>



| <span data-ttu-id="78c24-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78c24-114">Requirement</span></span> | <span data-ttu-id="78c24-115">Wert</span><span class="sxs-lookup"><span data-stu-id="78c24-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78c24-116">Header</span><span class="sxs-lookup"><span data-stu-id="78c24-116">Header</span></span><br/>  | <dl> <span data-ttu-id="78c24-117"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="78c24-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="78c24-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78c24-118">Library</span></span><br/> | <dl> <span data-ttu-id="78c24-119"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="78c24-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78c24-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="78c24-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c24-121">**CPosPassThru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="78c24-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="78c24-122">**Zeitformat-GUIDs**</span><span class="sxs-lookup"><span data-stu-id="78c24-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




