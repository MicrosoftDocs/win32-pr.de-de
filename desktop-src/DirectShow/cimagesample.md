---
description: Die cimagesample-Klasse implementiert ein Medien Beispiel, das eine GDI-geräteunabhängige Bitmap (DIB) verwaltet.
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: Cimagesample-Klasse (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2235d50c952ce1b76e4a70eda0341f0fe3c4167c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356340"
---
# <a name="cimagesample-class"></a><span data-ttu-id="8be77-103">Cimagesample-Klasse</span><span class="sxs-lookup"><span data-stu-id="8be77-103">CImageSample class</span></span>

![cimagesample-Klassenhierarchie](images/wutil03.png)

<span data-ttu-id="8be77-105">Die- `CImageSample` Klasse implementiert ein Medien Beispiel, das eine GDI-geräteunabhängige Bitmap (DIB) verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8be77-105">The `CImageSample` class implements a media sample that manages a GDI device-independent bitmap (DIB).</span></span> <span data-ttu-id="8be77-106">Diese Klasse wird von der [**cmediasample**](cmediasample.md) -Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8be77-106">This class derives from the [**CMediaSample**](cmediasample.md) class.</span></span> <span data-ttu-id="8be77-107">Es ist für die Verwendung mit der [**cimagezuordcator**](cimageallocator.md) -Klasse vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="8be77-107">It is intended to be used with the [**CImageAllocator**](cimageallocator.md) class.</span></span> <span data-ttu-id="8be77-108">Die **cimagezuordcator** -Klasse stellt eine Zuweisung bereit, die- `CImageSample` Objekte erstellt.</span><span class="sxs-lookup"><span data-stu-id="8be77-108">The **CImageAllocator** class provides an allocator that creates `CImageSample` objects.</span></span>



| <span data-ttu-id="8be77-109">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="8be77-109">Protected Member Variables</span></span>                        | <span data-ttu-id="8be77-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8be77-110">Description</span></span>                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="8be77-111">**Mio. \_ dibdata**</span><span class="sxs-lookup"><span data-stu-id="8be77-111">**m\_DibData**</span></span>](cimagesample-m-dibdata.md)      | <span data-ttu-id="8be77-112">Enthält Informationen über das DIB, das von diesem-Objekt verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="8be77-112">Contains information about the DIB that this object is managing.</span></span>  |
| [<span data-ttu-id="8be77-113">**m- \_ binit**</span><span class="sxs-lookup"><span data-stu-id="8be77-113">**m\_bInit**</span></span>](cimagesample-m-binit.md)          | <span data-ttu-id="8be77-114">Gibt an, ob das Objekt initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8be77-114">Indicates whether the object has been initialized.</span></span>                |
| <span data-ttu-id="8be77-115">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="8be77-115">Public Methods</span></span>                                    | <span data-ttu-id="8be77-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8be77-116">Description</span></span>                                                       |
| [<span data-ttu-id="8be77-117">**Cimagesample**</span><span class="sxs-lookup"><span data-stu-id="8be77-117">**CImageSample**</span></span>](cimagesample-cimagesample.md) | <span data-ttu-id="8be77-118">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="8be77-118">Constructor method.</span></span>                                               |
| [<span data-ttu-id="8be77-119">**Getdibdata**</span><span class="sxs-lookup"><span data-stu-id="8be77-119">**GetDIBData**</span></span>](cimagesample-getdibdata.md)     | <span data-ttu-id="8be77-120">Ruft Informationen über das DIB ab, das von diesem-Objekt verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="8be77-120">Retrieves information about the DIB that this object is managing.</span></span> |
| [<span data-ttu-id="8be77-121">**Setdibdata**</span><span class="sxs-lookup"><span data-stu-id="8be77-121">**SetDIBData**</span></span>](cimagesample-setdibdata.md)     | <span data-ttu-id="8be77-122">Legt Informationen über das DIB fest, das von diesem-Objekt verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="8be77-122">Sets information about the DIB that this object is managing.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="8be77-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8be77-123">Requirements</span></span>



| <span data-ttu-id="8be77-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8be77-124">Requirement</span></span> | <span data-ttu-id="8be77-125">Wert</span><span class="sxs-lookup"><span data-stu-id="8be77-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8be77-126">Header</span><span class="sxs-lookup"><span data-stu-id="8be77-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8be77-127"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8be77-127"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8be77-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8be77-128">Library</span></span><br/> | <dl> <span data-ttu-id="8be77-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8be77-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




