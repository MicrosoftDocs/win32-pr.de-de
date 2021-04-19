---
description: Schreibt die Filterdaten in den angegebenen Stream.
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: Cpersiststream. Write Items-Methode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.WriteToStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 893d58986db92e50cbafefe74676481162808abf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361293"
---
# <a name="cpersiststreamwritetostream-method"></a><span data-ttu-id="f8075-103">Cpersiststream. Write-Methode</span><span class="sxs-lookup"><span data-stu-id="f8075-103">CPersistStream.WriteToStream method</span></span>

<span data-ttu-id="f8075-104">Schreibt die Filterdaten in den angegebenen Stream.</span><span class="sxs-lookup"><span data-stu-id="f8075-104">Writes the filter's data to the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8075-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8075-105">Syntax</span></span>


```C++
virtual HRESULT WriteToStream(
   IStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="f8075-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8075-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8075-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="f8075-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="f8075-108">Zeiger auf eine **IStream** -Schnittstelle, die den Zielstream der Filterdaten angibt.</span><span class="sxs-lookup"><span data-stu-id="f8075-108">Pointer to an **IStream** interface that specifies the filter data's destination stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8075-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8075-109">Return value</span></span>

<span data-ttu-id="f8075-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="f8075-110">Returns S\_OK.</span></span> <span data-ttu-id="f8075-111">Die abgeleitete Klasse sollte einen gültigen **HRESULT** -Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f8075-111">The derived class should return a valid **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8075-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8075-112">Remarks</span></span>

<span data-ttu-id="f8075-113">Die Standardversion schreibt nichts. Sie kann überschrieben werden, um Daten zu schreiben, die für Ihre Klasse spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="f8075-113">The default version writes nothing; it can be overridden to write data specific to your class.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8075-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8075-114">Requirements</span></span>



| <span data-ttu-id="f8075-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8075-115">Requirement</span></span> | <span data-ttu-id="f8075-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f8075-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8075-117">Header</span><span class="sxs-lookup"><span data-stu-id="f8075-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f8075-118"><dt>PStream. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8075-118"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f8075-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f8075-119">Library</span></span><br/> | <dl> <span data-ttu-id="f8075-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f8075-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8075-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8075-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8075-122">**Cpersiststream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f8075-122">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




