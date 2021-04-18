---
description: Die setdibdata-Methode gibt Informationen über die von diesem Objekt verwaltete GDI-geräteunabhängige Bitmap (DIB) an. Ruft diese Methode auf, um das cimagesample-Objekt zu initialisieren.
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: Cimagesample. setdibdata-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.SetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 418263da0416b325b1b080713dd6289f3bcc688e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358247"
---
# <a name="cimagesamplesetdibdata-method"></a><span data-ttu-id="0f93c-104">Cimagesample. setdibdata-Methode</span><span class="sxs-lookup"><span data-stu-id="0f93c-104">CImageSample.SetDIBData method</span></span>

<span data-ttu-id="0f93c-105">Die- `SetDIBData` Methode gibt Informationen über die von diesem Objekt verwaltete GDI-geräteunabhängige Bitmap (DIB) an.</span><span class="sxs-lookup"><span data-stu-id="0f93c-105">The `SetDIBData` method specifies information about the GDI device-independent bitmap (DIB) that this object is managing.</span></span> <span data-ttu-id="0f93c-106">Ruft diese Methode auf, um das **cimagesample** -Objekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="0f93c-106">Call this method to initialize the **CImageSample** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f93c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f93c-107">Syntax</span></span>


```C++
void SetDIBData(
   DIBDATA *pDibData
);
```



## <a name="parameters"></a><span data-ttu-id="0f93c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f93c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f93c-109">*pdibdata*</span><span class="sxs-lookup"><span data-stu-id="0f93c-109">*pDibData*</span></span> 
</dt> <dd>

<span data-ttu-id="0f93c-110">Zeiger auf eine [**dibdata**](dibdata.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0f93c-110">Pointer to a [**DIBDATA**](dibdata.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f93c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f93c-111">Return value</span></span>

<span data-ttu-id="0f93c-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0f93c-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f93c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f93c-113">Requirements</span></span>



| <span data-ttu-id="0f93c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f93c-114">Requirement</span></span> | <span data-ttu-id="0f93c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="0f93c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f93c-116">Header</span><span class="sxs-lookup"><span data-stu-id="0f93c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0f93c-117"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f93c-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0f93c-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0f93c-118">Library</span></span><br/> | <dl> <span data-ttu-id="0f93c-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0f93c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f93c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f93c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f93c-121">**Cimagesample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0f93c-121">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




