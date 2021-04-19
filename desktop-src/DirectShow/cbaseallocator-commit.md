---
description: 'Die Commit-Methode ordnet den Speicher für die Puffer zu. Diese Methode implementiert die imemzuzucator:: Commit-Methode.'
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: Cbasezucator. Commit-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Commit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b49fae72e5588105b1235c1f0c461d5cc45cfa2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351326"
---
# <a name="cbaseallocatorcommit-method"></a><span data-ttu-id="697d3-104">Cbasezucator. Commit-Methode</span><span class="sxs-lookup"><span data-stu-id="697d3-104">CBaseAllocator.Commit method</span></span>

<span data-ttu-id="697d3-105">Die- `Commit` Methode ordnet den Speicher für die Puffer zu.</span><span class="sxs-lookup"><span data-stu-id="697d3-105">The `Commit` method allocates the memory for the buffers.</span></span> <span data-ttu-id="697d3-106">Diese Methode implementiert die [**imemzuzucator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) -Methode.</span><span class="sxs-lookup"><span data-stu-id="697d3-106">This method implements the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="697d3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="697d3-107">Syntax</span></span>


```C++
HRESULT Commit();
```



## <a name="parameters"></a><span data-ttu-id="697d3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="697d3-108">Parameters</span></span>

<span data-ttu-id="697d3-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="697d3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="697d3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="697d3-110">Return value</span></span>

<span data-ttu-id="697d3-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="697d3-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="697d3-112">Mögliche Werte sind in der folgenden Liste aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="697d3-112">Possible values include those in the following list.</span></span>



| <span data-ttu-id="697d3-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="697d3-113">Return code</span></span>                                                                                       | <span data-ttu-id="697d3-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="697d3-114">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="697d3-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="697d3-115"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="697d3-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="697d3-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="697d3-117"><dt>**VFW \_ E \_ sizenotset**</dt></span><span class="sxs-lookup"><span data-stu-id="697d3-117"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="697d3-118">Die Puffer Anforderungen wurden nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="697d3-118">Buffer requirements were not specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="697d3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="697d3-119">Remarks</span></span>

<span data-ttu-id="697d3-120">Rufen Sie vor dem Aufrufen dieser Methode die [**cbasezucator:: SetProperties**](cbaseallocator-setproperties.md) -Methode auf, um die Puffer Anforderungen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="697d3-120">Before calling this method, call the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method to specify the buffer requirements.</span></span>

<span data-ttu-id="697d3-121">Diese Methode ruft die virtuelle Methode [**cbaseallocator:: Alloc**](cbaseallocator-alloc.md) auf, um den Speicher für die Puffer zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="697d3-121">This method calls the virtual method [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) to allocate the memory for the buffers.</span></span> <span data-ttu-id="697d3-122">Abgeleitete Klassen können die **Zuweisung** überschreiben.</span><span class="sxs-lookup"><span data-stu-id="697d3-122">Derived classes can override **Alloc**.</span></span> <span data-ttu-id="697d3-123">Wenn ein Decommit-Vorgang aussteht, wird er abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="697d3-123">If a decommit operation is pending, it is canceled.</span></span>

<span data-ttu-id="697d3-124">Sie müssen diese Methode aufrufen, bevor Sie die [**cbasezucator:: GetBuffer**](cbaseallocator-getbuffer.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="697d3-124">You must call this method before calling the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="697d3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="697d3-125">Requirements</span></span>



| <span data-ttu-id="697d3-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="697d3-126">Requirement</span></span> | <span data-ttu-id="697d3-127">Wert</span><span class="sxs-lookup"><span data-stu-id="697d3-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="697d3-128">Header</span><span class="sxs-lookup"><span data-stu-id="697d3-128">Header</span></span><br/>  | <dl> <span data-ttu-id="697d3-129"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="697d3-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="697d3-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="697d3-130">Library</span></span><br/> | <dl> <span data-ttu-id="697d3-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="697d3-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="697d3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="697d3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="697d3-133">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="697d3-133">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




