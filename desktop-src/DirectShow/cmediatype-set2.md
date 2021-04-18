---
description: Die Set-Methode legt den Medientyp von einem anderen Medientyp fest.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: Cmediatype. Set-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afe99c3f5ee10e6aacd3dadf69af320b110688af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358267"
---
# <a name="cmediatypeset-method-mtypeh"></a><span data-ttu-id="16e91-103">Cmediatype. Set-Methode (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="16e91-103">CMediaType.Set method (Mtype.h)</span></span>

<span data-ttu-id="16e91-104">Die- `Set` Methode legt den Medientyp von einem anderen Medientyp fest.</span><span class="sxs-lookup"><span data-stu-id="16e91-104">The `Set` method sets the media type from another media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="16e91-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="16e91-105">Syntax</span></span>


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="16e91-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="16e91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16e91-107">*mtype* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="16e91-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="16e91-108">Verweis auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="16e91-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16e91-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16e91-109">Return value</span></span>

<span data-ttu-id="16e91-110">Gibt " \_ OK" oder "E \_ outo" zurück.</span><span class="sxs-lookup"><span data-stu-id="16e91-110">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="16e91-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16e91-111">Remarks</span></span>

<span data-ttu-id="16e91-112">Diese Methode kopiert den gesamten Medientyp aus *mtype*.</span><span class="sxs-lookup"><span data-stu-id="16e91-112">This method copies the entire media type from *mtype*.</span></span>

## <a name="requirements"></a><span data-ttu-id="16e91-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16e91-113">Requirements</span></span>



| <span data-ttu-id="16e91-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16e91-114">Requirement</span></span> | <span data-ttu-id="16e91-115">Wert</span><span class="sxs-lookup"><span data-stu-id="16e91-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16e91-116">Header</span><span class="sxs-lookup"><span data-stu-id="16e91-116">Header</span></span><br/>  | <dl> <span data-ttu-id="16e91-117"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16e91-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="16e91-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="16e91-118">Library</span></span><br/> | <dl> <span data-ttu-id="16e91-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="16e91-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16e91-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16e91-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16e91-121">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="16e91-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




