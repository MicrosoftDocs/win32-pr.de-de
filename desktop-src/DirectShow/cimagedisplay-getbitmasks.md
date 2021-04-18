---
description: Die getBitMasks-Methode ruft die Farb Masken für ein angegebenes videoinfo-Format ab.
ms.assetid: 72a9ba44-96de-4fff-a3fb-675d3dd080d8
title: Cimagedisplay. getBitMasks-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetBitMasks
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2defe5e80a0d7311adcd19dca67119019623993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371776"
---
# <a name="cimagedisplaygetbitmasks-method"></a><span data-ttu-id="4e3dc-103">Cimagedisplay. getBitMasks-Methode</span><span class="sxs-lookup"><span data-stu-id="4e3dc-103">CImageDisplay.GetBitMasks method</span></span>

<span data-ttu-id="4e3dc-104">Die- `GetBitMasks` Methode ruft die Farb Masken für ein angegebenes [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Format ab.</span><span class="sxs-lookup"><span data-stu-id="4e3dc-104">The `GetBitMasks` method retrieves the color masks for a specified [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) format.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e3dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e3dc-105">Syntax</span></span>


```C++
const DWORD* GetBitMasks(
   const VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4e3dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e3dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e3dc-107">*pvideoinfo*</span><span class="sxs-lookup"><span data-stu-id="4e3dc-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="4e3dc-108">Ein Zeiger auf die **videoinfo** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4e3dc-108">Pointer to the **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e3dc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e3dc-109">Return value</span></span>

<span data-ttu-id="4e3dc-110">Gibt ein Array von drei **DWORD** -Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="4e3dc-110">Returns an array of three **DWORD** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e3dc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e3dc-111">Remarks</span></span>

<span data-ttu-id="4e3dc-112">Wenn der **bicompression** -Member BI- \_ Bitfields ist, gibt die Methode einen Zeiger auf die Farb Masken zurück, die im **dwbitmasks** -Member bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4e3dc-112">If the **biCompression** member is BI\_BITFIELDS, the method returns a pointer to the color masks that are supplied in the **dwBitMasks** member.</span></span> <span data-ttu-id="4e3dc-113">Wenn der **bicompression** -Member BI \_ RGB ist, gibt die Methode die Farb Masken zurück, die der Bittiefe entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4e3dc-113">If the **biCompression** member is BI\_RGB, the method returns the color masks that correspond to the bit depth.</span></span> <span data-ttu-id="4e3dc-114">Wenn die Methode fehlschlägt (z. b. die Bittiefe ist kleiner als 16), gibt die Methode das Array zurück {0,0,0} .</span><span class="sxs-lookup"><span data-stu-id="4e3dc-114">If the method fails (for example, the bit depth is less than 16), the method returns the array {0,0,0}.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e3dc-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e3dc-115">Requirements</span></span>



| <span data-ttu-id="4e3dc-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e3dc-116">Requirement</span></span> | <span data-ttu-id="4e3dc-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4e3dc-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e3dc-118">Header</span><span class="sxs-lookup"><span data-stu-id="4e3dc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4e3dc-119"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e3dc-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4e3dc-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4e3dc-120">Library</span></span><br/> | <dl> <span data-ttu-id="4e3dc-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4e3dc-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e3dc-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e3dc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e3dc-123">**Cimagedisplay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4e3dc-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




