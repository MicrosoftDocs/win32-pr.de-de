---
description: Die checksizes-Methode überprüft zuordnereigenschaften mit dem aktuellen Medientyp.
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: Cimageexeccator. checksizes-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CheckSizes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71184d4915911c29bff9d3a6fa9985942a4aaa44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368616"
---
# <a name="cimageallocatorchecksizes-method"></a><span data-ttu-id="ba931-103">Cimageexeccator. checksizes-Methode</span><span class="sxs-lookup"><span data-stu-id="ba931-103">CImageAllocator.CheckSizes method</span></span>

<span data-ttu-id="ba931-104">Die- `CheckSizes` Methode überprüft die zuordnereigenschaften mit dem aktuellen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="ba931-104">The `CheckSizes` method checks allocator properties against the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba931-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba931-105">Syntax</span></span>


```C++
HRESULT CheckSizes(
   ALLOCATOR_PROPERTIES *pRequest
);
```



## <a name="parameters"></a><span data-ttu-id="ba931-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba931-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba931-107">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="ba931-107">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="ba931-108">Ein Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die die angeforderten zuordnereigenschaften beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ba931-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that describes the requested allocator properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba931-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba931-109">Return value</span></span>

<span data-ttu-id="ba931-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ba931-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ba931-111">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="ba931-111">Possible values include the following.</span></span>



| <span data-ttu-id="ba931-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ba931-112">Return code</span></span>                                                                                           | <span data-ttu-id="ba931-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba931-113">Description</span></span>                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ba931-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ba931-114"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="ba931-115">Die angeforderten Eigenschaften sind mit dem Medientyp kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ba931-115">The requested properties are compatible with the media type.</span></span><br/>     |
| <dl> <span data-ttu-id="ba931-116"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ba931-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="ba931-117">Die angeforderten Eigenschaften sind mit dem Medientyp nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ba931-117">The requested properties are not compatible with the media type.</span></span><br/> |
| <dl> <span data-ttu-id="ba931-118"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="ba931-118"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="ba931-119">Die besitzende PIN ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="ba931-119">The owning pin is not connected.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="ba931-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba931-120">Remarks</span></span>

<span data-ttu-id="ba931-121">Wenn die-Methode zurückgibt, wenn der Rückgabewert S \_ OK ist, enthält das **cbbuffer** -Element von *pRequest* die tatsächliche Puffergröße.</span><span class="sxs-lookup"><span data-stu-id="ba931-121">When the method returns, if the return value is S\_OK, the **cbBuffer** member of *pRequest* contains the actual buffer size.</span></span> <span data-ttu-id="ba931-122">Diese ist möglicherweise größer als die angeforderte Größe, Sie ist jedoch nie kleiner.</span><span class="sxs-lookup"><span data-stu-id="ba931-122">This might be larger than the requested size, but will never be smaller.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba931-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba931-123">Requirements</span></span>



| <span data-ttu-id="ba931-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba931-124">Requirement</span></span> | <span data-ttu-id="ba931-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ba931-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba931-126">Header</span><span class="sxs-lookup"><span data-stu-id="ba931-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ba931-127"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba931-127"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ba931-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ba931-128">Library</span></span><br/> | <dl> <span data-ttu-id="ba931-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ba931-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba931-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba931-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba931-131">**Cimagezuordcator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ba931-131">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




