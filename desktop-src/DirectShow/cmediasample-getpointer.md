---
description: 'Die getpointer-Methode ruft einen Lese-/Schreib-Zeiger auf den Puffer ab. Diese Methode implementiert die imediasample:: getpointer-Methode.'
ms.assetid: dd797ad5-6066-4366-a56f-621132f2e6ea
title: Cmediasample. getpointer-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe8d8785bd52fbe601d9980f8fc146a2c6f41e40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371045"
---
# <a name="cmediasamplegetpointer-method"></a><span data-ttu-id="ee3f9-104">Cmediasample. getpointer-Methode</span><span class="sxs-lookup"><span data-stu-id="ee3f9-104">CMediaSample.GetPointer method</span></span>

<span data-ttu-id="ee3f9-105">Die `GetPointer` -Methode ruft einen Lese-/schreibzeiger auf den Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="ee3f9-105">The `GetPointer` method retrieves a read/write pointer to the buffer.</span></span> <span data-ttu-id="ee3f9-106">Diese Methode implementiert die [**imediasample:: getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ee3f9-106">This method implements the [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee3f9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee3f9-107">Syntax</span></span>


```C++
HRESULT GetPointer(
   BYTE **ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="ee3f9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee3f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee3f9-109">*ppBuffer*</span><span class="sxs-lookup"><span data-stu-id="ee3f9-109">*ppBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="ee3f9-110">Adresse einer Variablen, die einen Zeiger auf den Puffer empfängt.</span><span class="sxs-lookup"><span data-stu-id="ee3f9-110">Address of a variable that receives a pointer to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee3f9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee3f9-111">Return value</span></span>

<span data-ttu-id="ee3f9-112">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="ee3f9-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee3f9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee3f9-113">Requirements</span></span>



| <span data-ttu-id="ee3f9-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee3f9-114">Requirement</span></span> | <span data-ttu-id="ee3f9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ee3f9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3f9-116">Header</span><span class="sxs-lookup"><span data-stu-id="ee3f9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ee3f9-117"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee3f9-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ee3f9-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ee3f9-118">Library</span></span><br/> | <dl> <span data-ttu-id="ee3f9-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ee3f9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee3f9-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee3f9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee3f9-121">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ee3f9-121">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




