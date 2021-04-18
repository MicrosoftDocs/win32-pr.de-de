---
title: Profil-Manager-Objekt
description: Profil-Manager-Objekt
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- Windows Media-Format-SDK, Profil-Manager-Objekte
- Advanced Systems Format (ASF), Profil-Manager-Objekte
- ASF (Advanced Systems Format), Profil-Manager-Objekte
- Objekte, Profil-Manager-Objekte
- Profile, Objekte
- Profile, Profil-Manager-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce3d77598f52e43a840c1b6b3ef58baa47f77bd
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106340891"
---
# <a name="profile-manager-object"></a><span data-ttu-id="33ed0-109">Profil-Manager-Objekt</span><span class="sxs-lookup"><span data-stu-id="33ed0-109">Profile Manager Object</span></span>

<span data-ttu-id="33ed0-110">Ein Profil ist ein Satz von Medien Parametern, die zum Erstellen einer ASF-Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33ed0-110">A profile is a set of media parameters used to create an ASF file.</span></span> <span data-ttu-id="33ed0-111">Das Profil-Manager-Objekt erstellt Profil Objekte zur Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="33ed0-111">The profile manager object creates profile objects for editing.</span></span> <span data-ttu-id="33ed0-112">Profil Objekte können ohne Daten erstellt oder aus vorhandenen Profildaten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="33ed0-112">Profile objects can be created without any data in them or built from existing profile data.</span></span> <span data-ttu-id="33ed0-113">Das Profil-Manager-Objekt stellt auch Methoden zum Auflisten unterstützter Codecs und zum Abfragen dieser Codecs für Informationen bereit.</span><span class="sxs-lookup"><span data-stu-id="33ed0-113">The profile manager object also provides methods for enumerating supported codecs and querying those codecs for information.</span></span>

<span data-ttu-id="33ed0-114">Das Profil-Manager-Objekt wird von der [**wmkreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion erstellt, mit der ein Zeiger auf eine [**iwmprofilemanager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) -Schnittstelle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="33ed0-114">The profile manager object is created by the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function, which sets a pointer to an [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="33ed0-115">Die anderen Schnittstellen des Profil-Manager-Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="33ed0-115">The other interfaces of the profile manager object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="33ed0-116">Die folgenden Schnittstellen werden vom Profil-Manager-Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="33ed0-116">The following interfaces are supported by the profile manager object.</span></span>



| <span data-ttu-id="33ed0-117">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="33ed0-117">Interface</span></span>                                                      | <span data-ttu-id="33ed0-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33ed0-118">Description</span></span>                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33ed0-119">**Iwmcodecinfo**</span><span class="sxs-lookup"><span data-stu-id="33ed0-119">**IWMCodecInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | <span data-ttu-id="33ed0-120">Ruft Informationen zu unterstützten Codecs und deren Formaten ab.</span><span class="sxs-lookup"><span data-stu-id="33ed0-120">Retrieves information about supported codecs and their formats.</span></span>                                                                              |
| [<span data-ttu-id="33ed0-121">**IWMCodecInfo2**</span><span class="sxs-lookup"><span data-stu-id="33ed0-121">**IWMCodecInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | <span data-ttu-id="33ed0-122">Ruft die Namen der unterstützten Codecs und die Beschreibungen ihrer Formate ab.</span><span class="sxs-lookup"><span data-stu-id="33ed0-122">Retrieves the names of the supported codecs and the descriptions of their formats.</span></span> <span data-ttu-id="33ed0-123">Erbt alle Methoden von **iwmcodecinfo**.</span><span class="sxs-lookup"><span data-stu-id="33ed0-123">Inherits all of the methods of **IWMCodecInfo**.</span></span>          |
| [<span data-ttu-id="33ed0-124">**IWMCodecInfo3**</span><span class="sxs-lookup"><span data-stu-id="33ed0-124">**IWMCodecInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | <span data-ttu-id="33ed0-125">Ruft Codec-Eigenschaften und-Abfragen für unterstützte Funktionen ab.</span><span class="sxs-lookup"><span data-stu-id="33ed0-125">Retrieves codec properties and queries codecs for supported features.</span></span> <span data-ttu-id="33ed0-126">Erbt alle Methoden von **iwmcodecinfo** und **IWMCodecInfo2**.</span><span class="sxs-lookup"><span data-stu-id="33ed0-126">Inherits all of the methods of **IWMCodecInfo** and **IWMCodecInfo2**.</span></span> |
| [<span data-ttu-id="33ed0-127">**Iwmprofilemanager**</span><span class="sxs-lookup"><span data-stu-id="33ed0-127">**IWMProfileManager**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | <span data-ttu-id="33ed0-128">Erstellt neue Profile, lädt vorhandene Profile und speichert benutzerdefinierte Profile.</span><span class="sxs-lookup"><span data-stu-id="33ed0-128">Creates new profiles, loads existing profiles, and saves custom profiles.</span></span>                                                                    |
| [<span data-ttu-id="33ed0-129">**IWMProfileManager2**</span><span class="sxs-lookup"><span data-stu-id="33ed0-129">**IWMProfileManager2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | <span data-ttu-id="33ed0-130">Steuert die Version der Systemprofile, die vom Profil-Manager aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="33ed0-130">Controls the version of system profiles enumerated by the profile manager.</span></span> <span data-ttu-id="33ed0-131">Erbt alle Methoden von **iwmprofilemanager**.</span><span class="sxs-lookup"><span data-stu-id="33ed0-131">Inherits all of the methods of **IWMProfileManager**.</span></span>             |
| [<span data-ttu-id="33ed0-132">**Iwmprofilemanagerlanguage**</span><span class="sxs-lookup"><span data-stu-id="33ed0-132">**IWMProfileManagerLanguage**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | <span data-ttu-id="33ed0-133">Steuert die Sprache der vom Profil-Manager analysierten Systemprofile.</span><span class="sxs-lookup"><span data-stu-id="33ed0-133">Controls the language of the system profiles parsed by the profile manager.</span></span>                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="33ed0-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33ed0-134">Remarks</span></span>

<span data-ttu-id="33ed0-135">Wenn ein Profil-Manager-Objekt erstellt wird, werden alle Systemprofile analysiert, was einige Sekunden dauern kann.</span><span class="sxs-lookup"><span data-stu-id="33ed0-135">When a profile manager object is created, it parses all of the system profiles, which can take several seconds.</span></span> <span data-ttu-id="33ed0-136">Wenn Sie einen Profil-Manager bei jeder Verwendung verwenden, wirkt sich dies negativ auf die Leistung aus.</span><span class="sxs-lookup"><span data-stu-id="33ed0-136">Creating and releasing a profile manager every time you need to use it will adversely affect performance.</span></span> <span data-ttu-id="33ed0-137">Sie sollten einen Profil-Manager einmal in der Anwendung erstellen und nur dann freigeben, wenn Sie ihn nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="33ed0-137">You should create a profile manager once in your application and release it only when you no longer need to use it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33ed0-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33ed0-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33ed0-139">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="33ed0-139">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="33ed0-140">**Profil Objekt**</span><span class="sxs-lookup"><span data-stu-id="33ed0-140">**Profile Object**</span></span>](profile-object.md)
</dt> <dt>

[<span data-ttu-id="33ed0-141">**Profiles**</span><span class="sxs-lookup"><span data-stu-id="33ed0-141">**Profiles**</span></span>](profiles.md)
</dt> </dl>

 

 




