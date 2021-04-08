---
title: Profil Objekt
description: Profil Objekt
ms.assetid: ec42889e-580e-4a65-9fe6-4a5f15c97eb0
keywords:
- Windows Media-Format-SDK, Profil Objekte
- Advanced Systems Format (ASF), Profil Objekte
- ASF (Advanced Systems Format), Profil Objekte
- Objekte, Profil Objekte
- Profile, Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6763d098819bde7d5db404aeffef3cd333d9b1
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103858080"
---
# <a name="profile-object"></a><span data-ttu-id="bbc26-108">Profil Objekt</span><span class="sxs-lookup"><span data-stu-id="bbc26-108">Profile Object</span></span>

<span data-ttu-id="bbc26-109">Ein Profil Objekt verwaltet die Einstellungen eines Profils.</span><span class="sxs-lookup"><span data-stu-id="bbc26-109">A profile object manages the settings of a profile.</span></span> <span data-ttu-id="bbc26-110">Profil Objekte können für vorhandene Profildaten erstellt werden, oder Sie können leer erstellt werden, um neue Daten zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="bbc26-110">Profile objects can be created for existing profile data or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="bbc26-111">Ein Profil Objekt wird auch vom Reader-Objekt (und dem synchronen Reader-Objekt) erstellt, wenn eine Datei zum Lesen geladen wird.</span><span class="sxs-lookup"><span data-stu-id="bbc26-111">A profile object is also created by the reader object (and the synchronous reader object) when a file is loaded for reading.</span></span> <span data-ttu-id="bbc26-112">In diesem Fall wird das Objekt mit den im Header der Datei gespeicherten Profilinformationen aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="bbc26-112">In this case the object is populated with the profile information stored in the header of the file.</span></span>

<span data-ttu-id="bbc26-113">Zum Speichern des Inhalts eines Profil Objekts müssen Sie [**iwmprofilemanager:: saveprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile)abrufen.</span><span class="sxs-lookup"><span data-stu-id="bbc26-113">To save the contents of a profile object, you must call [**IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).</span></span>

<span data-ttu-id="bbc26-114">Ein Profil enthält mehrere Objekte, die verschiedene Aspekte des Profils (z. b. Streams) steuern.</span><span class="sxs-lookup"><span data-stu-id="bbc26-114">A profile contains multiple objects that control various aspects of the profile (such as streams).</span></span> <span data-ttu-id="bbc26-115">Alle diese Objekte sind dem Profil Objekt untergeordnet.</span><span class="sxs-lookup"><span data-stu-id="bbc26-115">All of these objects are subordinate to the profile object.</span></span> <span data-ttu-id="bbc26-116">Sie erstellen diese Objekte nicht mit Erstellungs Funktionen wie bei den Hauptobjekten dieses SDK.</span><span class="sxs-lookup"><span data-stu-id="bbc26-116">You do not create these objects with creation functions as you would with the major objects of this SDK.</span></span> <span data-ttu-id="bbc26-117">Stattdessen enthalten die Schnittstellen des Profil Objekts Methoden, mit denen die untergeordneten Objekte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bbc26-117">Instead, the interfaces of the profile object contain methods that create the subordinate objects.</span></span>

<span data-ttu-id="bbc26-118">Rufen Sie eine der folgenden Methoden auf, um ein Profil Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bbc26-118">To create a profile object, call one of the following methods.</span></span>



| <span data-ttu-id="bbc26-119">Methode</span><span class="sxs-lookup"><span data-stu-id="bbc26-119">Method</span></span>                                                                                | <span data-ttu-id="bbc26-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bbc26-120">Description</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbc26-121">**Iwmprofilemanager:: kreateemptyprofile**</span><span class="sxs-lookup"><span data-stu-id="bbc26-121">**IWMProfileManager::CreateEmptyProfile**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) | <span data-ttu-id="bbc26-122">Erstellt ein Profil Objekt ohne Profildaten.</span><span class="sxs-lookup"><span data-stu-id="bbc26-122">Creates a profile object without any profile data.</span></span>                                                                                                              |
| [<span data-ttu-id="bbc26-123">**Iwmprofilemanager:: loadprofilebydata**</span><span class="sxs-lookup"><span data-stu-id="bbc26-123">**IWMProfileManager::LoadProfileByData**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)   | <span data-ttu-id="bbc26-124">Erstellt ein Profil Objekt, das mit Daten aus einem Profil aufgefüllt ist, das als Zeichenfolge gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="bbc26-124">Creates a profile object populated with data from a profile saved as a string.</span></span> <span data-ttu-id="bbc26-125">Dies ist die einzige Möglichkeit, ein Profil Objekt mit Daten aus einem benutzerdefinierten Profil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bbc26-125">This is the only way to create a profile object with data from a custom profile.</span></span> |
| [<span data-ttu-id="bbc26-126">**Iwmprofilemanager:: loadprofilebyid**</span><span class="sxs-lookup"><span data-stu-id="bbc26-126">**IWMProfileManager::LoadProfileByID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)       | <span data-ttu-id="bbc26-127">Erstellt ein Profil Objekt, das mit Daten aus einem Systemprofil aufgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="bbc26-127">Creates a profile object populated with data from a system profile.</span></span> <span data-ttu-id="bbc26-128">Verwendet die GUID, um das gewünschte Systemprofil zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bbc26-128">Uses the GUID to identify the desired system profile.</span></span>                                       |
| [<span data-ttu-id="bbc26-129">**Iwmprofilemanager:: loadsystemprofile**</span><span class="sxs-lookup"><span data-stu-id="bbc26-129">**IWMProfileManager::LoadSystemProfile**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)   | <span data-ttu-id="bbc26-130">Erstellt ein Profil Objekt, das mit Daten aus einem Systemprofil aufgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="bbc26-130">Creates a profile object populated with data from a system profile.</span></span> <span data-ttu-id="bbc26-131">Verwendet den Profil Index, um das gewünschte Systemprofil zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bbc26-131">Uses the profile index to identify the desired system profile.</span></span>                              |



 

<span data-ttu-id="bbc26-132">Alle Methoden in der vorangehenden Tabelle legen einen Zeiger auf eine **iwmprofile** -Schnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="bbc26-132">All of the methods in the preceding table set a pointer to an **IWMProfile** interface.</span></span> <span data-ttu-id="bbc26-133">Die anderen Schnittstellen des Profil Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bbc26-133">The other interfaces of the profile object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="bbc26-134">Die folgenden Schnittstellen werden von jedem Profil Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bbc26-134">The following interfaces are supported by every profile object.</span></span>



| <span data-ttu-id="bbc26-135">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="bbc26-135">Interface</span></span>                                  | <span data-ttu-id="bbc26-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bbc26-136">Description</span></span>                                                                                                                                       |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbc26-137">**Iwmlanguagelist**</span><span class="sxs-lookup"><span data-stu-id="bbc26-137">**IWMLanguageList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) | <span data-ttu-id="bbc26-138">Verwaltet eine Liste der Sprachen, die von einer ASF-Datei unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="bbc26-138">Manages a list of languages supported by an ASF file.</span></span>                                                                                             |
| [<span data-ttu-id="bbc26-139">**Iwmpacketsize**</span><span class="sxs-lookup"><span data-stu-id="bbc26-139">**IWMPacketSize**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)     | <span data-ttu-id="bbc26-140">Steuert die maximale Größe von Paketen in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="bbc26-140">Controls the maximum size of packets in a file.</span></span>                                                                                                   |
| [<span data-ttu-id="bbc26-141">**IWMPacketSize2**</span><span class="sxs-lookup"><span data-stu-id="bbc26-141">**IWMPacketSize2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)   | <span data-ttu-id="bbc26-142">Steuert die minimale Größe von Paketen in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="bbc26-142">Controls the minimum size of packets in a file.</span></span> <span data-ttu-id="bbc26-143">Erbt alle Methoden von **iwmpacketsize**.</span><span class="sxs-lookup"><span data-stu-id="bbc26-143">Inherits all of the methods of **IWMPacketSize**.</span></span>                                                 |
| [<span data-ttu-id="bbc26-144">**Iwmprofile**</span><span class="sxs-lookup"><span data-stu-id="bbc26-144">**IWMProfile**</span></span>](iwmprofile.md)           | <span data-ttu-id="bbc26-145">Steuert die grundlegenden Einstellungen und Objekte, die in einem Profil enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="bbc26-145">Controls the basic settings and objects included in a profile.</span></span>                                                                                    |
| [<span data-ttu-id="bbc26-146">**IWMProfile2**</span><span class="sxs-lookup"><span data-stu-id="bbc26-146">**IWMProfile2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)         | <span data-ttu-id="bbc26-147">Ruft die dem Profil zugeordnete Globally Unique Identifier (GUID) ab.</span><span class="sxs-lookup"><span data-stu-id="bbc26-147">Retrieves the globally unique identifier (GUID) associated with the profile.</span></span> <span data-ttu-id="bbc26-148">Erbt alle Methoden von **iwmprofile**.</span><span class="sxs-lookup"><span data-stu-id="bbc26-148">Inherits all of the methods of **IWMProfile**.</span></span>                       |
| [<span data-ttu-id="bbc26-149">**IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="bbc26-149">**IWMProfile3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)         | <span data-ttu-id="bbc26-150">Steuert die Bandbreiten Freigabe und streampriorisierungsinformationen in einem Profil.</span><span class="sxs-lookup"><span data-stu-id="bbc26-150">Controls bandwidth sharing and stream prioritization information in a profile.</span></span> <span data-ttu-id="bbc26-151">Erbt alle Methoden von **iwmprofile** und **IWMProfile2**.</span><span class="sxs-lookup"><span data-stu-id="bbc26-151">Inherits all of the methods of **IWMProfile** and **IWMProfile2**.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bbc26-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bbc26-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbc26-153">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="bbc26-153">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="bbc26-154">**Profil-Manager-Objekt**</span><span class="sxs-lookup"><span data-stu-id="bbc26-154">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="bbc26-155">**Profiles**</span><span class="sxs-lookup"><span data-stu-id="bbc26-155">**Profiles**</span></span>](profiles.md)
</dt> </dl>

 

 




