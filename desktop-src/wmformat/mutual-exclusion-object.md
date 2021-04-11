---
title: Gegenseitiges Ausschluss Objekt
description: Gegenseitiges Ausschluss Objekt
ms.assetid: dd1f7865-e409-4bf9-9fa0-769a29eaed60
keywords:
- Windows Media-Format-SDK, gegenseitige Ausschluss Objekte
- Advanced Systems Format (ASF), Objekte für gegenseitigen Ausschluss
- ASF (Advanced Systems Format), gegenseitige Ausschluss Objekte
- Objekte, Objekte für gegenseitigen Ausschluss
- gegenseitiger Ausschluss, Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8522b66f82bd88479b8c7b1d0d0b45bd038fdab3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101331"
---
# <a name="mutual-exclusion-object"></a><span data-ttu-id="f27f6-108">Gegenseitiges Ausschluss Objekt</span><span class="sxs-lookup"><span data-stu-id="f27f6-108">Mutual Exclusion Object</span></span>

<span data-ttu-id="f27f6-109">Ein gegenseitiges Ausschluss Objekt wird verwendet, um eine Anzahl von Streams anzugeben, von denen jeweils nur eine übermittelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f27f6-109">A mutual exclusion object is used to specify a number of streams, of which only one can be delivered at a time.</span></span> <span data-ttu-id="f27f6-110">Dies kann auf verschiedene Weise verwendet werden, wie z. b. das Bereitstellen eines Audiodatenstroms in mehreren Sprachen als Sound für einen Videodaten Strom.</span><span class="sxs-lookup"><span data-stu-id="f27f6-110">This can be used in several ways, such as providing an audio stream in several languages as the soundtrack for one video stream.</span></span>

<span data-ttu-id="f27f6-111">Der gegenseitige Ausschluss ist ein optionaler Teil eines Profils.</span><span class="sxs-lookup"><span data-stu-id="f27f6-111">Mutual exclusion is an optional part of a profile.</span></span> <span data-ttu-id="f27f6-112">Gegenseitige Ausschluss Objekte können für vorhandene gegenseitige Ausschluss Informationen in einem Profil erstellt werden, oder Sie können leer erstellt werden, um neue Daten zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="f27f6-112">Mutual exclusion objects can be created for existing mutual exclusion information in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="f27f6-113">Gegenseitige Ausschluss Objekte können nicht unabhängig von einem Profil Objekt vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f27f6-113">Mutual exclusion objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="f27f6-114">Zum Speichern des Inhalts eines gegenseitigen Ausschluss Objekts müssen Sie [**iwmprofile:: addmutualexclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f27f6-114">To save the contents of a mutual exclusion object, you must call [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span></span>

<span data-ttu-id="f27f6-115">Verwenden Sie zum Erstellen eines gegenseitigen Ausschluss Objekts eine der folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="f27f6-115">To create a mutual exclusion object, use one of the following methods.</span></span>



| <span data-ttu-id="f27f6-116">Methode</span><span class="sxs-lookup"><span data-stu-id="f27f6-116">Method</span></span>                                                                              | <span data-ttu-id="f27f6-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f27f6-117">Description</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f27f6-118">**Iwmprofile:: kreatenewmutualexclusion**</span><span class="sxs-lookup"><span data-stu-id="f27f6-118">**IWMProfile::CreateNewMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | <span data-ttu-id="f27f6-119">Erstellt ein gegenseitiges Ausschluss Objekt ohne Daten.</span><span class="sxs-lookup"><span data-stu-id="f27f6-119">Creates a mutual exclusion object without any data.</span></span>                                                                                                         |
| [<span data-ttu-id="f27f6-120">**Iwmprofile:: getmutualexclusion**</span><span class="sxs-lookup"><span data-stu-id="f27f6-120">**IWMProfile::GetMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | <span data-ttu-id="f27f6-121">Erstellt ein gegenseitiges Ausschluss Objekt, das mit Daten aus einem Profil aufgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="f27f6-121">Creates a mutual exclusion object populated with data from a profile.</span></span> <span data-ttu-id="f27f6-122">Verwendet den gegenseitigen Ausschluss Index, um die gewünschten gegenseitigen Ausschluss Informationen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f27f6-122">Uses the mutual exclusion index to identify the desired mutual exclusion information.</span></span> |



 

<span data-ttu-id="f27f6-123">Beide Methoden in der vorangehenden Tabelle legen einen Zeiger auf eine **iwmmutualexclusion** -Schnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="f27f6-123">Both methods in the preceding table set a pointer to an **IWMMutualExclusion** interface.</span></span> <span data-ttu-id="f27f6-124">Die **iwmstreamlist** -Schnittstelle wird von **iwmmutualexclusion** geerbt und muss niemals direkt darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f27f6-124">The **IWMStreamList** interface is inherited by **IWMMutualExclusion** and never needs to be accessed directly.</span></span> <span data-ttu-id="f27f6-125">Die andere Schnittstelle des gegenseitigen Ausschluss Objekts kann durch Aufrufen der **QueryInterface** -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f27f6-125">The other interface of the mutual exclusion object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="f27f6-126">Die folgenden Schnittstellen werden von jedem gegenseitigen Ausschluss Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f27f6-126">The following interfaces are supported by every mutual exclusion object.</span></span>



| <span data-ttu-id="f27f6-127">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f27f6-127">Interface</span></span>                                          | <span data-ttu-id="f27f6-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f27f6-128">Description</span></span>                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f27f6-129">**Iwmmutualexclusion**</span><span class="sxs-lookup"><span data-stu-id="f27f6-129">**IWMMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)   | <span data-ttu-id="f27f6-130">Legt den Typ des zu verwendenden gegenseitigen Ausschlusses fest und ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="f27f6-130">Sets and retrieves the type of mutual exclusion to be used.</span></span>                                                                                            |
| [<span data-ttu-id="f27f6-131">**IWMMutualExclusion2**</span><span class="sxs-lookup"><span data-stu-id="f27f6-131">**IWMMutualExclusion2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) | <span data-ttu-id="f27f6-132">Organisiert Streams in Datensätze, die zum Erstellen komplexer gegenseitiger Ausschluss Szenarien verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f27f6-132">Organizes streams into records, which can be used to create complex mutual exclusion scenarios.</span></span> <span data-ttu-id="f27f6-133">Erbt alle Methoden von **iwmmutualexclusion**.</span><span class="sxs-lookup"><span data-stu-id="f27f6-133">Inherits all of the methods of **IWMMutualExclusion**.</span></span> |
| [<span data-ttu-id="f27f6-134">**Iwmstreamlist**</span><span class="sxs-lookup"><span data-stu-id="f27f6-134">**IWMStreamList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | <span data-ttu-id="f27f6-135">Verwaltet die Liste von sich gegenseitig ausschließenden Datenströmen.</span><span class="sxs-lookup"><span data-stu-id="f27f6-135">Manages the list of mutually exclusive streams.</span></span>                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="f27f6-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f27f6-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f27f6-137">**Gegenseitiger Ausschluss**</span><span class="sxs-lookup"><span data-stu-id="f27f6-137">**Mutual Exclusion**</span></span>](mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="f27f6-138">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="f27f6-138">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="f27f6-139">**Profil-Manager-Objekt**</span><span class="sxs-lookup"><span data-stu-id="f27f6-139">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> </dl>

 

 




