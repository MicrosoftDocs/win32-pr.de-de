---
description: Die checkvideotype-Methode überprüft, ob ein bestimmtes videoinfo-Format mit dem Anzeige Format kompatibel ist.
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: Cimagedisplay. checkvideotype-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckVideoType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7db198270804053993352c4969b924fa7edc891f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372680"
---
# <a name="cimagedisplaycheckvideotype-method"></a><span data-ttu-id="bc54a-103">Cimagedisplay. checkvideotype-Methode</span><span class="sxs-lookup"><span data-stu-id="bc54a-103">CImageDisplay.CheckVideoType method</span></span>

<span data-ttu-id="bc54a-104">Die- `CheckVideoType` Methode überprüft, ob ein angegebenes [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Format mit dem Anzeige Format kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="bc54a-104">The `CheckVideoType` method checks whether a specified [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) format is compatible with the display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc54a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc54a-105">Syntax</span></span>


```C++
HRESULT CheckVideoType(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="bc54a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc54a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc54a-107">*pinput*</span><span class="sxs-lookup"><span data-stu-id="bc54a-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="bc54a-108">Zeiger auf eine **videoinfo** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="bc54a-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc54a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc54a-109">Return value</span></span>

<span data-ttu-id="bc54a-110">Gibt S \_ OK zurück, wenn das Format kompatibel ist, \_ andernfalls E invalidArg.</span><span class="sxs-lookup"><span data-stu-id="bc54a-110">Returns S\_OK if the format is compatible, or E\_INVALIDARG otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc54a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc54a-111">Remarks</span></span>

<span data-ttu-id="bc54a-112">Diese Methode gibt S \_ OK zurück, wenn der vorgeschlagene Typ unter den aktuellen Anzeigeeinstellungen problemlos angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bc54a-112">This method returns S\_OK if the proposed type can be displayed easily under the current display settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc54a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc54a-113">Requirements</span></span>



| <span data-ttu-id="bc54a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc54a-114">Requirement</span></span> | <span data-ttu-id="bc54a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="bc54a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc54a-116">Header</span><span class="sxs-lookup"><span data-stu-id="bc54a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bc54a-117"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc54a-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bc54a-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bc54a-118">Library</span></span><br/> | <dl> <span data-ttu-id="bc54a-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bc54a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc54a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc54a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc54a-121">**Cimagedisplay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bc54a-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




