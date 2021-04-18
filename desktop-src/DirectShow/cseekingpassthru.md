---
description: Die cseekingpassthru-Klasse ist ein Hilfsobjekt, das cpospassthru-und crendererpospassthru-Objekte erstellt.
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: Cseekingpassthru-Klasse (seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 273f9b6686c4455452924dc43628801fae5d518a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371982"
---
# <a name="cseekingpassthru-class"></a><span data-ttu-id="49b3f-103">Cseekingpassthru-Klasse</span><span class="sxs-lookup"><span data-stu-id="49b3f-103">CSeekingPassThru class</span></span>

<span data-ttu-id="49b3f-104">Die `CSeekingPassThru` -Klasse ist ein Hilfsobjekt, das [**cpospassthru**](cpospassthru.md) -und [**crendererpospassthru**](crendererpospassthru.md) -Objekte erstellt.</span><span class="sxs-lookup"><span data-stu-id="49b3f-104">The `CSeekingPassThru` class is a helper object that creates [**CPosPassThru**](cpospassthru.md) and [**CRendererPosPassThru**](crendererpospassthru.md) objects.</span></span>

<span data-ttu-id="49b3f-105">Die **cpospassthru** -Klasse und die **crendererpospassthru** -Klasse sind Hilfsobjekte, die Suchbefehle an Upstream übergeben, sodass die- `CSeekingPassThru` Klasse ein Hilfsobjekt zum Erstellen von Hilfsobjekten ist.</span><span class="sxs-lookup"><span data-stu-id="49b3f-105">The **CPosPassThru** and **CRendererPosPassThru** classes are helper objects that pass seeking commands upstream, so the `CSeekingPassThru` class is a helper object for creating helper objects.</span></span>

<span data-ttu-id="49b3f-106">Es ist nicht erforderlich, diese Klasse direkt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="49b3f-106">It is not necessary to use this class directly.</span></span> <span data-ttu-id="49b3f-107">Verwenden Sie stattdessen die Funktion " [**kreatepospassthru**](createpospassthru.md) ", die alle Details der Verwendung dieser Klasse behandelt.</span><span class="sxs-lookup"><span data-stu-id="49b3f-107">Instead, use the [**CreatePosPassThru**](createpospassthru.md) function, which handles all of the details of using this class.</span></span> <span data-ttu-id="49b3f-108">Dies hat den weiteren Vorteil, dass das Objekt aus Quartz.dll geladen wird, wodurch die Codegröße Ihres Filters etwas verringert wird.</span><span class="sxs-lookup"><span data-stu-id="49b3f-108">It has the further advantage of loading the object from Quartz.dll, which reduces the code size of your filter somewhat.</span></span> <span data-ttu-id="49b3f-109">Weitere Informationen finden Sie unter [**cpospassthru**](cpospassthru.md).</span><span class="sxs-lookup"><span data-stu-id="49b3f-109">For more information, see [**CPosPassThru**](cpospassthru.md).</span></span>

<span data-ttu-id="49b3f-110">Die- `CSeekingPassThru` Klasse macht die [**iseekingpassthru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="49b3f-110">The `CSeekingPassThru` class exposes the [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) interface.</span></span> <span data-ttu-id="49b3f-111">Die [**iseekingpassthru:: init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) -Methode initialisiert das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="49b3f-111">The [**ISeekingPassThru::Init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) method initializes the object.</span></span> <span data-ttu-id="49b3f-112">Nachdem das Objekt initialisiert wurde, kann es vom Filter für die Schnittstellen [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) und [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="49b3f-112">After the object is initialized, the filter can query it for the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) and [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interfaces.</span></span>



| <span data-ttu-id="49b3f-113">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="49b3f-113">Public Methods</span></span>                                                  | <span data-ttu-id="49b3f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49b3f-114">Description</span></span>                        |
|-----------------------------------------------------------------|------------------------------------|
| [<span data-ttu-id="49b3f-115">**Cseekingpassthru**</span><span class="sxs-lookup"><span data-stu-id="49b3f-115">**CSeekingPassThru**</span></span>](cseekingpassthru-cseekingpassthru.md)   | <span data-ttu-id="49b3f-116">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="49b3f-116">Constructor method.</span></span>                |
| [<span data-ttu-id="49b3f-117">**~ Cseekingpassthru**</span><span class="sxs-lookup"><span data-stu-id="49b3f-117">**~CSeekingPassThru**</span></span>](cseekingpassthru--cseekingpassthru.md) | <span data-ttu-id="49b3f-118">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="49b3f-118">Destructor method.</span></span>                 |
| [<span data-ttu-id="49b3f-119">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="49b3f-119">**CreateInstance**</span></span>](cseekingpassthru-createinstance.md)       | <span data-ttu-id="49b3f-120">Erstellt eine Instanz des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="49b3f-120">Creates an instance of the object.</span></span> |
| <span data-ttu-id="49b3f-121">Iseekingpassthru-Methoden</span><span class="sxs-lookup"><span data-stu-id="49b3f-121">ISeekingPassThru Methods</span></span>                                        | <span data-ttu-id="49b3f-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49b3f-122">Description</span></span>                        |
| [<span data-ttu-id="49b3f-123">**Init**</span><span class="sxs-lookup"><span data-stu-id="49b3f-123">**Init**</span></span>](cseekingpassthru-init.md)                           | <span data-ttu-id="49b3f-124">Initialisiert das Objekt.</span><span class="sxs-lookup"><span data-stu-id="49b3f-124">Initializes the object.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="49b3f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49b3f-125">Requirements</span></span>



| <span data-ttu-id="49b3f-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49b3f-126">Requirement</span></span> | <span data-ttu-id="49b3f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="49b3f-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49b3f-128">Header</span><span class="sxs-lookup"><span data-stu-id="49b3f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="49b3f-129"><dt>Seekpt. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49b3f-129"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="49b3f-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="49b3f-130">Library</span></span><br/> | <dl> <span data-ttu-id="49b3f-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="49b3f-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




