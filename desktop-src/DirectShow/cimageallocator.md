---
description: Die cimagezuordcator-Klasse implementiert einen Zuweiser, der GDI-geräteunabhängige Bitmaps (Disb) verwaltet. Diese Klasse wird von der cbasezucator-Klasse abgeleitet. Es werden Medien Beispiele erstellt, die mithilfe der cimagesample-Klasse implementiert werden.
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: Cimagezuordcator-Klasse (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea37dfe8cbbc7baf90e6065f0c54af1a60c3284b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354050"
---
# <a name="cimageallocator-class"></a><span data-ttu-id="939b9-105">Cimagezuordcator-Klasse</span><span class="sxs-lookup"><span data-stu-id="939b9-105">CImageAllocator class</span></span>

![cimagezuordnerklassenhierarchie](images/wutil04.png)

<span data-ttu-id="939b9-107">Die- `CImageAllocator` Klasse implementiert einen Zuweiser, der GDI-geräteunabhängige Bitmaps (Disb) verwaltet.</span><span class="sxs-lookup"><span data-stu-id="939b9-107">The `CImageAllocator` class implements an allocator that manages GDI device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="939b9-108">Diese Klasse wird von der [**cbasezucator**](cbaseallocator.md) -Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="939b9-108">This class derives from the [**CBaseAllocator**](cbaseallocator.md) class.</span></span> <span data-ttu-id="939b9-109">Es werden Medien Beispiele erstellt, die mithilfe der [**cimagesample**](cimagesample.md) -Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="939b9-109">It creates media samples that are implemented using the [**CImageSample**](cimagesample.md) class.</span></span>

<span data-ttu-id="939b9-110">Eine Zuweisung wird von zwei verbundenen Pins gemeinsam genutzt, gehört aber immer zu einem der Filter in der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="939b9-110">An allocator is shared by two connected pins, but is always owned by one of the filters in the connection.</span></span> <span data-ttu-id="939b9-111">Ein Filter, der verwendet, `CImageAllocator` muss nachverfolgen, ob die Zuweisung von sich selbst oder über den anderen Filter bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="939b9-111">A filter that uses `CImageAllocator` must keep track of whether the allocator was provided by itself or by the other filter.</span></span> <span data-ttu-id="939b9-112">Wenn die Zuweisung von sich selbst bereitgestellt wurde, kann sich der besitzende Filter auf die Tatsache verlassen, dass alle Medien Beispiele aus der Zuweisung **cimagesample** -Objekte sind.</span><span class="sxs-lookup"><span data-stu-id="939b9-112">If the allocator was provided by itself, the owning filter can rely on the fact that all media samples from the allocator are **CImageSample** objects.</span></span> <span data-ttu-id="939b9-113">Daher kann das **cimagesample** -Objekt verwendet werden, um Informationen über das DIB zu erhalten, das in einer [**dibdata**](dibdata.md) -Struktur gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="939b9-113">It can therefore use the **CImageSample** object to obtain information about the DIB, which is stored in a [**DIBDATA**](dibdata.md) structure.</span></span>

<span data-ttu-id="939b9-114">Der besitzende Filter sollte immer dann **notifymediatype** anrufen, wenn sich der Medientyp ändert.</span><span class="sxs-lookup"><span data-stu-id="939b9-114">The owning filter should call **NotifyMediaType** whenever the media type changes.</span></span>



| <span data-ttu-id="939b9-115">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="939b9-115">Protected Member Variables</span></span>                                     | <span data-ttu-id="939b9-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="939b9-116">Description</span></span>                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="939b9-117">**m \_ pFilter**</span><span class="sxs-lookup"><span data-stu-id="939b9-117">**m\_pFilter**</span></span>](cimageallocator-m-pfilter.md)                | <span data-ttu-id="939b9-118">Zeiger auf den besitzenden Filter.</span><span class="sxs-lookup"><span data-stu-id="939b9-118">Pointer to the owning filter.</span></span>                                            |
| [<span data-ttu-id="939b9-119">**m \_ pmediatype**</span><span class="sxs-lookup"><span data-stu-id="939b9-119">**m\_pMediaType**</span></span>](cimageallocator-m-pmediatype.md)          | <span data-ttu-id="939b9-120">Zeiger auf den aktuellen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="939b9-120">Pointer to the current media type.</span></span>                                       |
| <span data-ttu-id="939b9-121">Geschützte Methoden</span><span class="sxs-lookup"><span data-stu-id="939b9-121">Protected Methods</span></span>                                              | <span data-ttu-id="939b9-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="939b9-122">Description</span></span>                                                              |
| [<span data-ttu-id="939b9-123">**Zuordnungseinheits**</span><span class="sxs-lookup"><span data-stu-id="939b9-123">**Alloc**</span></span>](cimageallocator-alloc.md)                         | <span data-ttu-id="939b9-124">Belegt Speicher für die Puffer.</span><span class="sxs-lookup"><span data-stu-id="939b9-124">Allocates memory for the buffers.</span></span>                                        |
| [<span data-ttu-id="939b9-125">**Prüf Größen**</span><span class="sxs-lookup"><span data-stu-id="939b9-125">**CheckSizes**</span></span>](cimageallocator-checksizes.md)               | <span data-ttu-id="939b9-126">Überprüft zuordnereigenschaften auf den aktuellen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="939b9-126">Checks allocator properties against the current media type.</span></span>              |
| [<span data-ttu-id="939b9-127">**"Kreatedib"**</span><span class="sxs-lookup"><span data-stu-id="939b9-127">**CreateDIB**</span></span>](cimageallocator-createdib.md)                 | <span data-ttu-id="939b9-128">Erstellt ein DIB.</span><span class="sxs-lookup"><span data-stu-id="939b9-128">Creates a DIB.</span></span>                                                           |
| [<span data-ttu-id="939b9-129">**"Kreateimagesample"**</span><span class="sxs-lookup"><span data-stu-id="939b9-129">**CreateImageSample**</span></span>](cimageallocator-createimagesample.md) | <span data-ttu-id="939b9-130">Erstellt ein Medien Beispiel.</span><span class="sxs-lookup"><span data-stu-id="939b9-130">Creates a media sample.</span></span> <span data-ttu-id="939b9-131">Virtu.</span><span class="sxs-lookup"><span data-stu-id="939b9-131">Virtual.</span></span>                                         |
| [<span data-ttu-id="939b9-132">**Kostenlos**</span><span class="sxs-lookup"><span data-stu-id="939b9-132">**Free**</span></span>](cimageallocator-free.md)                           | <span data-ttu-id="939b9-133">Gibt den gesamten Puffer Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="939b9-133">Releases all of the buffer memory.</span></span>                                       |
| <span data-ttu-id="939b9-134">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="939b9-134">Public Methods</span></span>                                                 | <span data-ttu-id="939b9-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="939b9-135">Description</span></span>                                                              |
| [<span data-ttu-id="939b9-136">**Cimagezuordcator**</span><span class="sxs-lookup"><span data-stu-id="939b9-136">**CImageAllocator**</span></span>](cimageallocator-cimageallocator.md)     | <span data-ttu-id="939b9-137">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="939b9-137">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="939b9-138">**Notifymediatype**</span><span class="sxs-lookup"><span data-stu-id="939b9-138">**NotifyMediaType**</span></span>](cimageallocator-notifymediatype.md)     | <span data-ttu-id="939b9-139">Informiert das-Objekt über den aktuellen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="939b9-139">Informs the object of the current media type.</span></span>                            |
| <span data-ttu-id="939b9-140">Imemzuordcator-Methoden</span><span class="sxs-lookup"><span data-stu-id="939b9-140">IMemAllocator Methods</span></span>                                          | <span data-ttu-id="939b9-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="939b9-141">Description</span></span>                                                              |
| [<span data-ttu-id="939b9-142">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="939b9-142">**SetProperties**</span></span>](cimageallocator-setproperties.md)         | <span data-ttu-id="939b9-143">Gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an.</span><span class="sxs-lookup"><span data-stu-id="939b9-143">Specifies the number of buffers to allocate and the size of each buffer.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="939b9-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="939b9-144">Requirements</span></span>



| <span data-ttu-id="939b9-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="939b9-145">Requirement</span></span> | <span data-ttu-id="939b9-146">Wert</span><span class="sxs-lookup"><span data-stu-id="939b9-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="939b9-147">Header</span><span class="sxs-lookup"><span data-stu-id="939b9-147">Header</span></span><br/>  | <dl> <span data-ttu-id="939b9-148"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="939b9-148"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="939b9-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="939b9-149">Library</span></span><br/> | <dl> <span data-ttu-id="939b9-150">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="939b9-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="939b9-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="939b9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="939b9-152">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="939b9-152">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




