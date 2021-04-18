---
description: Die getdibdata-Methode ruft Informationen über das von diesem Objekt verwaltete GDI-geräteunabhängige Bitmap (DIB) ab.
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: Cimagesample. getdibdata-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.GetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd198152e7c0042a6d48cf942a48745540960d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364810"
---
# <a name="cimagesamplegetdibdata-method"></a><span data-ttu-id="ae063-103">Cimagesample. getdibdata-Methode</span><span class="sxs-lookup"><span data-stu-id="ae063-103">CImageSample.GetDIBData method</span></span>

<span data-ttu-id="ae063-104">Die- `GetDIBData` Methode ruft Informationen über die von diesem-Objekt verwaltete GDI-geräteunabhängige Bitmap (DIB) ab.</span><span class="sxs-lookup"><span data-stu-id="ae063-104">The `GetDIBData` method retrieves information about the GDI device-independent bitmap (DIB) that this object is managing.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae063-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae063-105">Syntax</span></span>


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a><span data-ttu-id="ae063-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae063-106">Parameters</span></span>

<span data-ttu-id="ae063-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ae063-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae063-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae063-108">Return value</span></span>

<span data-ttu-id="ae063-109">Gibt einen Zeiger auf eine [**dibdata**](dibdata.md) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="ae063-109">Returns a pointer to a [**DIBDATA**](dibdata.md) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae063-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae063-110">Remarks</span></span>

<span data-ttu-id="ae063-111">Der Aufrufer muss die **dibdata** -Struktur initialisieren, bevor diese Methode aufgerufen wird. Überprüfen Sie den Wert von **cimagesample:: m \_ binit**.</span><span class="sxs-lookup"><span data-stu-id="ae063-111">The caller must initialize the **DIBDATA** structure before calling this method; check the value of **CImageSample::m\_bInit**.</span></span> <span data-ttu-id="ae063-112">Um die Struktur zu initialisieren, müssen Sie die [**cimagesample:: setdibdata**](cimagesample-setdibdata.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ae063-112">To initialize the structure, call the [**CImageSample::SetDIBData**](cimagesample-setdibdata.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae063-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae063-113">Requirements</span></span>



| <span data-ttu-id="ae063-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae063-114">Requirement</span></span> | <span data-ttu-id="ae063-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ae063-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae063-116">Header</span><span class="sxs-lookup"><span data-stu-id="ae063-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ae063-117"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae063-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ae063-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ae063-118">Library</span></span><br/> | <dl> <span data-ttu-id="ae063-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ae063-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae063-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae063-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae063-121">**Cimagesample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ae063-121">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




