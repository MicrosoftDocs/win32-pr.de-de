---
description: Implementiert eine Zuweisung, die die imemzuordcator-Schnittstelle unterstützt.
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: Cmemzuordcator-Klasse (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adf390b7abf8fcbdb017ecde04bde76bf4bc001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372425"
---
# <a name="cmemallocator-class"></a><span data-ttu-id="581da-103">Cmemzuordcator-Klasse</span><span class="sxs-lookup"><span data-stu-id="581da-103">CMemAllocator class</span></span>

![cmemzuordcator-Klassenhierarchie](images/filter10.png)

<span data-ttu-id="581da-105">Implementiert eine Zuweisung, die die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="581da-105">Implements an allocator that supports the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="581da-106">Diese Klasse wird von [**cbasezucator**](cbaseallocator.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="581da-106">This class derives from [**CBaseAllocator**](cbaseallocator.md).</span></span> <span data-ttu-id="581da-107">Weitere Informationen zu Zuordnungen finden Sie in der Dokumentation zu [**cbasezuweisung**](cbaseallocator.md).</span><span class="sxs-lookup"><span data-stu-id="581da-107">For more information about allocators, refer to the documentation for [**CBaseAllocator**](cbaseallocator.md).</span></span>



| <span data-ttu-id="581da-108">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="581da-108">Protected Member Variables</span></span>                              | <span data-ttu-id="581da-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="581da-109">Description</span></span>                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="581da-110">**m \_ pbuffer**</span><span class="sxs-lookup"><span data-stu-id="581da-110">**m\_pBuffer**</span></span>](cmemallocator-m-pbuffer.md)           | <span data-ttu-id="581da-111">Zeiger auf den Speicherblock, der die Puffer enthält.</span><span class="sxs-lookup"><span data-stu-id="581da-111">Pointer to the memory block that contains the buffers.</span></span>                   |
| <span data-ttu-id="581da-112">Geschützte Methoden</span><span class="sxs-lookup"><span data-stu-id="581da-112">Protected Methods</span></span>                                       | <span data-ttu-id="581da-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="581da-113">Description</span></span>                                                              |
| [<span data-ttu-id="581da-114">**Kostenlos**</span><span class="sxs-lookup"><span data-stu-id="581da-114">**Free**</span></span>](cmemallocator-free.md)                      | <span data-ttu-id="581da-115">Platzhalter Methode; wird während eines Decommit-Vorgangs aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="581da-115">Placeholder method; called during a decommit operation.</span></span>                  |
| [<span data-ttu-id="581da-116">**Kostenlos**</span><span class="sxs-lookup"><span data-stu-id="581da-116">**ReallyFree**</span></span>](cmemallocator-reallyfree.md)          | <span data-ttu-id="581da-117">Gibt den Arbeitsspeicher für die Puffer frei.</span><span class="sxs-lookup"><span data-stu-id="581da-117">Releases the memory for the buffers.</span></span>                                     |
| [<span data-ttu-id="581da-118">**Zuordnungseinheits**</span><span class="sxs-lookup"><span data-stu-id="581da-118">**Alloc**</span></span>](cmemallocator-alloc.md)                    | <span data-ttu-id="581da-119">Belegt Speicher für die Puffer.</span><span class="sxs-lookup"><span data-stu-id="581da-119">Allocates memory for the buffers.</span></span>                                        |
| <span data-ttu-id="581da-120">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="581da-120">Public Methods</span></span>                                          | <span data-ttu-id="581da-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="581da-121">Description</span></span>                                                              |
| [<span data-ttu-id="581da-122">**Cmemzuordcator**</span><span class="sxs-lookup"><span data-stu-id="581da-122">**CMemAllocator**</span></span>](cmemallocator-cmemallocator.md)    | <span data-ttu-id="581da-123">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="581da-123">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="581da-124">**~ Cmemzuordcator**</span><span class="sxs-lookup"><span data-stu-id="581da-124">**~ CMemAllocator**</span></span>](cmemallocator--cmemallocator.md) | <span data-ttu-id="581da-125">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="581da-125">Destructor method.</span></span>                                                       |
| [<span data-ttu-id="581da-126">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="581da-126">**CreateInstance**</span></span>](cmemallocator-createinstance.md)  | <span data-ttu-id="581da-127">Erstellt eine neue Instanz der **cmemzuordcator** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="581da-127">Creates a new instance of the **CMemAllocator** class.</span></span>                   |
| <span data-ttu-id="581da-128">Imemzuordcator-Methoden</span><span class="sxs-lookup"><span data-stu-id="581da-128">IMemAllocator Methods</span></span>                                   | <span data-ttu-id="581da-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="581da-129">Description</span></span>                                                              |
| [<span data-ttu-id="581da-130">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="581da-130">**SetProperties**</span></span>](cmemallocator-setproperties.md)    | <span data-ttu-id="581da-131">Gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an.</span><span class="sxs-lookup"><span data-stu-id="581da-131">Specifies the number of buffers to allocate and the size of each buffer.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="581da-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="581da-132">Requirements</span></span>



| <span data-ttu-id="581da-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="581da-133">Requirement</span></span> | <span data-ttu-id="581da-134">Wert</span><span class="sxs-lookup"><span data-stu-id="581da-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="581da-135">Header</span><span class="sxs-lookup"><span data-stu-id="581da-135">Header</span></span><br/>  | <dl> <span data-ttu-id="581da-136"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="581da-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="581da-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="581da-137">Library</span></span><br/> | <dl> <span data-ttu-id="581da-138">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="581da-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="581da-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="581da-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="581da-140">Bereitstellen einer benutzerdefinierten Zuweisung</span><span class="sxs-lookup"><span data-stu-id="581da-140">Providing a Custom Allocator</span></span>](providing-a-custom-allocator.md)
</dt> </dl>

 

 




