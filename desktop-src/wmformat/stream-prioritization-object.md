---
title: Streampriorisierungsobjekt
description: Streampriorisierungsobjekt
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- Windows Media-Format-SDK, streampriorisierungsobjekte
- Advanced Systems Format (ASF), streampriorisierungsobjekte
- ASF (Advanced Systems Format), streampriorisierungsobjekte
- Objekte, streampriorisierungsobjekte
- streampriorisierungsobjekte
- Streams, streampriorisierungsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cce4189f64e85cca4e0d649dbc00409cf9d7c06
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106340683"
---
# <a name="stream-prioritization-object"></a><span data-ttu-id="d0629-109">Streampriorisierungsobjekt</span><span class="sxs-lookup"><span data-stu-id="d0629-109">Stream Prioritization Object</span></span>

<span data-ttu-id="d0629-110">Ein streampriorisierungsobjekt wird verwendet, um eine Wichtigkeits Reihenfolge für die Datenströme in einem Profil anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d0629-110">A stream prioritization object is used to specify an order of importance for the streams in a profile.</span></span> <span data-ttu-id="d0629-111">Wenn die vollständige Wiedergabe aufgrund von Bitraten Einschränkungen nicht möglich ist, werden die Datenströme mit niedrigster Priorität als erstes gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d0629-111">When full playback is not possible due to bit-rate limitations, the lowest priority streams will be the first to be dropped.</span></span>

<span data-ttu-id="d0629-112">Streampriorisierungsobjekte können für vorhandene Datenstrom Priorisierungs Daten in einem Profil erstellt werden, oder Sie können leer erstellt werden, um neue Daten zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d0629-112">Stream prioritization objects can be created for existing stream prioritization data in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="d0629-113">Streampriorisierungsobjekte können nicht unabhängig von einem Profil Objekt vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d0629-113">Stream prioritization objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="d0629-114">Zum Speichern des Inhalts eines streampriorisierungsobjekts muss [**IWMProfile3:: setstreampriorisierung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d0629-114">To save the contents of a stream prioritization object, you must call [**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization).</span></span> <span data-ttu-id="d0629-115">Verwenden Sie zum Erstellen eines streampriorisierungsobjekts eine der folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="d0629-115">To create a stream prioritization object, use one of the following methods.</span></span>



| <span data-ttu-id="d0629-116">Methode</span><span class="sxs-lookup"><span data-stu-id="d0629-116">Method</span></span>                                                                                          | <span data-ttu-id="d0629-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0629-117">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="d0629-118">**IWMProfile3:: kreatenewstreampriorisierung**</span><span class="sxs-lookup"><span data-stu-id="d0629-118">**IWMProfile3::CreateNewStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | <span data-ttu-id="d0629-119">Erstellt ein streampriorisierungsobjekt ohne Daten.</span><span class="sxs-lookup"><span data-stu-id="d0629-119">Creates a stream prioritization object without any data.</span></span>                     |
| [<span data-ttu-id="d0629-120">**IWMProfile3:: getstreamprioritisierung**</span><span class="sxs-lookup"><span data-stu-id="d0629-120">**IWMProfile3::GetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | <span data-ttu-id="d0629-121">Erstellt ein Datenstrom Priorisierungs Objekt, das mit Daten aus dem Profil aufgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="d0629-121">Creates a stream prioritization object populated with data from the profile.</span></span> |



 

<span data-ttu-id="d0629-122">Beide Methoden in der vorangehenden Tabelle legen einen Zeiger auf eine **iwmstreampriorisierungsschnittstelle** fest.</span><span class="sxs-lookup"><span data-stu-id="d0629-122">Both methods in the preceding table set a pointer to an **IWMStreamPrioritization** interface.</span></span> <span data-ttu-id="d0629-123">Dies ist die einzige Schnittstelle, die vom streampriorisierungsobjekt unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d0629-123">This is the only interface supported by the stream prioritization object.</span></span>



| <span data-ttu-id="d0629-124">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d0629-124">Interface</span></span>                                                  | <span data-ttu-id="d0629-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0629-125">Description</span></span>                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="d0629-126">**Iwmstreampriorisierung**</span><span class="sxs-lookup"><span data-stu-id="d0629-126">**IWMStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | <span data-ttu-id="d0629-127">Verwaltet die Liste der Streams im streampriorisierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="d0629-127">Manages the list of streams within the stream prioritization object.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d0629-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0629-128">Remarks</span></span>

<span data-ttu-id="d0629-129">Für ein bestimmtes Profil kann nur eine streampriorisierung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d0629-129">Only one stream prioritization can exist for a given profile.</span></span> <span data-ttu-id="d0629-130">Wenn Sie eine neue streampriorisierung für ein Profil erstellen, das bereits eine streampriorisierung enthält, wird das alte gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d0629-130">If you create a new stream prioritization for a profile that already contains a stream prioritization, the old one will be deleted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0629-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d0629-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0629-132">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="d0629-132">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="d0629-133">**Profil Objekt**</span><span class="sxs-lookup"><span data-stu-id="d0629-133">**Profile Object**</span></span>](profile-object.md)
</dt> <dt>

[<span data-ttu-id="d0629-134">**Verwenden der streampriorisierung**</span><span class="sxs-lookup"><span data-stu-id="d0629-134">**Using Stream Prioritization**</span></span>](using-stream-prioritization.md)
</dt> </dl>

 

 




