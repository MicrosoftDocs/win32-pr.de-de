---
description: Die Methode "kreateimagesample" erstellt ein Medien Beispiel.
ms.assetid: dae71692-5cbc-4bc7-a363-41766ef17c58
title: Cimagezuzuordcator. kreateimagesample-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57463a7025ea816b6fe6bcaa8b964231458903de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361991"
---
# <a name="cimageallocatorcreateimagesample-method"></a><span data-ttu-id="4257a-103">Cimagezuzuordcator. kreateimagesample-Methode</span><span class="sxs-lookup"><span data-stu-id="4257a-103">CImageAllocator.CreateImageSample method</span></span>

<span data-ttu-id="4257a-104">Die- `CreateImageSample` Methode erstellt ein Medien Beispiel.</span><span class="sxs-lookup"><span data-stu-id="4257a-104">The `CreateImageSample` method creates a media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="4257a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4257a-105">Syntax</span></span>


```C++
virtual CImageSample* CreateImageSample(
   LPBYTE pData,
   LONG   Length
);
```



## <a name="parameters"></a><span data-ttu-id="4257a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4257a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4257a-107">*pData*</span><span class="sxs-lookup"><span data-stu-id="4257a-107">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="4257a-108">Zeiger auf einen Puffer der Größen *Länge*, der vom Aufrufer zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="4257a-108">Pointer to a buffer of size *Length*, allocated by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="4257a-109">*Länge*</span><span class="sxs-lookup"><span data-stu-id="4257a-109">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="4257a-110">Die Länge des Puffers.</span><span class="sxs-lookup"><span data-stu-id="4257a-110">Length of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4257a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4257a-111">Return value</span></span>

<span data-ttu-id="4257a-112">Gibt ein [**cimagesample**](cimagesample.md) -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="4257a-112">Returns a [**CImageSample**](cimagesample.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4257a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4257a-113">Remarks</span></span>

<span data-ttu-id="4257a-114">Diese Methode erstellt ein neues Medien Beispiel, das als **cimagesample** -Objekt implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="4257a-114">This method creates a new media sample, implemented as a **CImageSample** object.</span></span> <span data-ttu-id="4257a-115">Die [**imediasample:: getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) -Methode des Beispiels gibt einen Zeiger auf den Puffer zurück, der im *pData* -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4257a-115">The sample's [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method returns a pointer to the buffer specified in the *pData* parameter.</span></span>

<span data-ttu-id="4257a-116">Wenn Sie eine neue zuordnerklasse von [**cimagezuordcator**](cimageallocator.md) und eine neue Media-Beispiel Klasse von [**cimagesample**](cimagesample.md)ableiten, sollten Sie diese Methode überschreiben, um eine Instanz der Media Sample-Klasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4257a-116">If you derive a new allocator class from [**CImageAllocator**](cimageallocator.md) and a new media sample class from [**CImageSample**](cimagesample.md), you should override this method to create an instance of your media sample class.</span></span>

## <a name="requirements"></a><span data-ttu-id="4257a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4257a-117">Requirements</span></span>



| <span data-ttu-id="4257a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4257a-118">Requirement</span></span> | <span data-ttu-id="4257a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4257a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4257a-120">Header</span><span class="sxs-lookup"><span data-stu-id="4257a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="4257a-121"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4257a-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4257a-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4257a-122">Library</span></span><br/> | <dl> <span data-ttu-id="4257a-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4257a-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4257a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4257a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4257a-125">**Cimagezuordcator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4257a-125">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> <dt>

[<span data-ttu-id="4257a-126">**Cimagezuordcator:: zuzuweisung**</span><span class="sxs-lookup"><span data-stu-id="4257a-126">**CImageAllocator::Alloc**</span></span>](cimageallocator-alloc.md)
</dt> </dl>

 

 




