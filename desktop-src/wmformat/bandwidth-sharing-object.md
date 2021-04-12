---
title: Bandbreiten Freigabe Objekt
description: Bandbreiten Freigabe Objekt
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- Windows Media-Format-SDK, Bandbreiten Freigabe von Objekten
- Advanced Systems Format (ASF), Bandbreiten Freigabe von Objekten
- ASF (Advanced Systems Format), Bandbreiten Freigabe von Objekten
- Objekte, Bandbreiten Freigabe von Objekten
- Bandbreiten Freigabe, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29048e3094f1a12775dfbec7422baf349c18be7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389896"
---
# <a name="bandwidth-sharing-object"></a><span data-ttu-id="c5f0c-108">Bandbreiten Freigabe Objekt</span><span class="sxs-lookup"><span data-stu-id="c5f0c-108">Bandwidth Sharing Object</span></span>

<span data-ttu-id="c5f0c-109">Ein Bandbreiten Freigabe Objekt wird verwendet, um anzugeben, dass zwei oder mehr Streams, unabhängig von den einzelnen Bitraten, niemals mehr als eine festgelegte Bandbreite zwischen Ihnen verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-109">A bandwidth sharing object is used to indicate that two or more streams, regardless of their individual bit rates, will never use more than a specified amount of bandwidth between them.</span></span> <span data-ttu-id="c5f0c-110">Dabei handelt es sich um ein reines Informationsobjekt. die darin festgelegten Bitraten werden von keinem Objekt dieses SDK Programm gesteuert erzwungen.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-110">This is a purely informational object; the bit rates set within it are not enforced programmatically by any object of this SDK.</span></span>

<span data-ttu-id="c5f0c-111">Informationen zur Bandbreiten Freigabe sind ein optionaler Teil eines Profils.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-111">Bandwidth sharing information is an optional part of a profile.</span></span> <span data-ttu-id="c5f0c-112">Bandbreiten Freigabe Objekte können für vorhandene Bandbreiten Freigabe Informationen in einem Profil erstellt werden, oder Sie können leer erstellt werden, um neue Daten zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-112">Bandwidth sharing objects can be created for existing bandwidth sharing information in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="c5f0c-113">Bandbreiten Freigabe Objekte können nicht unabhängig von einem Profil Objekt vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-113">Bandwidth sharing objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="c5f0c-114">Zum Speichern des Inhalts eines Bandbreiten Freigabe Objekts müssen Sie [**IWMProfile3:: addbandwidthsharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)abrufen.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-114">To save the contents of a bandwidth sharing object, you must call [**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).</span></span>

<span data-ttu-id="c5f0c-115">Rufen Sie eine der folgenden Methoden auf, um ein Bandbreiten Freigabe Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-115">To create a bandwidth sharing object, call one of the following methods.</span></span>



| <span data-ttu-id="c5f0c-116">Methode</span><span class="sxs-lookup"><span data-stu-id="c5f0c-116">Method</span></span>                                                                                  | <span data-ttu-id="c5f0c-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5f0c-117">Description</span></span>                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5f0c-118">**IWMProfile3:: kreatenewbandwidthsharing**</span><span class="sxs-lookup"><span data-stu-id="c5f0c-118">**IWMProfile3::CreateNewBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | <span data-ttu-id="c5f0c-119">Erstellt ein Bandbreiten Freigabe Objekt ohne Daten.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-119">Creates a bandwidth sharing object without any data.</span></span>                                                                                                           |
| [<span data-ttu-id="c5f0c-120">**IWMProfile3:: getbandwidthsharing**</span><span class="sxs-lookup"><span data-stu-id="c5f0c-120">**IWMProfile3::GetBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | <span data-ttu-id="c5f0c-121">Erstellt ein Bandbreiten Freigabe Objekt, das mit Daten aus einem Profil aufgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-121">Creates a bandwidth sharing object populated with data from a profile.</span></span> <span data-ttu-id="c5f0c-122">Verwendet den Bandbreiten Freigabe Index, um die gewünschten Informationen zur Bandbreiten Freigabe zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-122">Uses the bandwidth sharing index to identify the desired bandwidth sharing information.</span></span> |



 

<span data-ttu-id="c5f0c-123">Beide Methoden in der vorangehenden Tabelle legen einen Zeiger auf eine **iwmbandwidthsharing** -Schnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-123">Both methods in the preceding table set a pointer to an **IWMBandwidthSharing** interface.</span></span> <span data-ttu-id="c5f0c-124">Die **iwmstreamlist** -Schnittstelle wird von **iwmbandwidthsharing** geerbt, sodass keine **QueryInterface** mit diesem Objekt aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-124">The **IWMStreamList** interface is inherited by **IWMBandwidthSharing**, so there is no need to call **QueryInterface** with this object.</span></span>

<span data-ttu-id="c5f0c-125">Die folgenden Schnittstellen werden von jedem Bandbreiten Freigabe Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-125">The following interfaces are supported by every bandwidth sharing object.</span></span>



| <span data-ttu-id="c5f0c-126">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c5f0c-126">Interface</span></span>                                          | <span data-ttu-id="c5f0c-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5f0c-127">Description</span></span>                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="c5f0c-128">**Iwmbandwidthsharing**</span><span class="sxs-lookup"><span data-stu-id="c5f0c-128">**IWMBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | <span data-ttu-id="c5f0c-129">Verwaltet die Eigenschaften einer Gruppe von Streams, die Bandbreite gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-129">Manages the properties of a group of streams that will share bandwidth.</span></span> |
| [<span data-ttu-id="c5f0c-130">**Iwmstreamlist**</span><span class="sxs-lookup"><span data-stu-id="c5f0c-130">**IWMStreamList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | <span data-ttu-id="c5f0c-131">Verwaltet die Liste der Streams, die Bandbreite gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-131">Manages the list of streams that will share bandwidth.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="c5f0c-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5f0c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5f0c-133">**Bandbreiten Freigabe**</span><span class="sxs-lookup"><span data-stu-id="c5f0c-133">**Bandwidth Sharing**</span></span>](bandwidth-sharing.md)
</dt> <dt>

[<span data-ttu-id="c5f0c-134">**Profil-Manager-Objekt**</span><span class="sxs-lookup"><span data-stu-id="c5f0c-134">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="c5f0c-135">**Profil Objekt**</span><span class="sxs-lookup"><span data-stu-id="c5f0c-135">**Profile Object**</span></span>](profile-object.md)
</dt> </dl>

 

 




