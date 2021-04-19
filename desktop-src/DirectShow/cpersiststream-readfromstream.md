---
description: Liest die Filterdaten aus dem angegebenen Stream.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: Cpersiststream. Read FromStream-Methode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.ReadFromStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce6c037fbce9fbaeabf7491b1b840000f67e25d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361295"
---
# <a name="cpersiststreamreadfromstream-method"></a><span data-ttu-id="85235-103">Cpersiststream. Read FromStream-Methode</span><span class="sxs-lookup"><span data-stu-id="85235-103">CPersistStream.ReadFromStream method</span></span>

<span data-ttu-id="85235-104">Liest die Filterdaten aus dem angegebenen Stream.</span><span class="sxs-lookup"><span data-stu-id="85235-104">Reads the filter's data from the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="85235-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="85235-105">Syntax</span></span>


```C++
virtual HRESULT ReadFromStream(
   IStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="85235-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85235-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85235-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="85235-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="85235-108">Zeiger auf eine **IStream** -Schnittstelle, aus der Daten gelesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85235-108">Pointer to an **IStream** interface from which data is to be read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85235-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85235-109">Return value</span></span>

<span data-ttu-id="85235-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="85235-110">Returns S\_OK.</span></span> <span data-ttu-id="85235-111">Die abgeleitete Klasse sollte einen gültigen **HRESULT** -Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="85235-111">The derived class should return a valid **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85235-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85235-112">Remarks</span></span>

<span data-ttu-id="85235-113">Die Standardversion liest nichts. Sie kann überschrieben werden, um Daten zu lesen, die für Ihre Klasse spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="85235-113">The default version reads nothing; it can be overridden to read data specific to your class.</span></span>

## <a name="requirements"></a><span data-ttu-id="85235-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85235-114">Requirements</span></span>



| <span data-ttu-id="85235-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85235-115">Requirement</span></span> | <span data-ttu-id="85235-116">Wert</span><span class="sxs-lookup"><span data-stu-id="85235-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85235-117">Header</span><span class="sxs-lookup"><span data-stu-id="85235-117">Header</span></span><br/>  | <dl> <span data-ttu-id="85235-118"><dt>PStream. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85235-118"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="85235-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="85235-119">Library</span></span><br/> | <dl> <span data-ttu-id="85235-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="85235-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85235-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85235-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85235-122">**Cpersiststream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="85235-122">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




