---
title: Verwenden benutzerdefinierter gegenseitiger Ausschluss Typen
description: Verwenden benutzerdefinierter gegenseitiger Ausschluss Typen
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- Iwmmutualexclusion
- gegenseitiger Ausschluss, iwmmutualexclusion-Schnittstelle
- gegenseitiger Ausschluss, benutzerdefinierte Typen
- Profile, benutzerdefinierte gegenseitige Ausschluss Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051e95bfb3f5ef8e39af31368227cf4918b897d2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101262"
---
# <a name="using-custom-mutual-exclusion-types"></a><span data-ttu-id="ed53e-107">Verwenden benutzerdefinierter gegenseitiger Ausschluss Typen</span><span class="sxs-lookup"><span data-stu-id="ed53e-107">Using Custom Mutual Exclusion Types</span></span>

<span data-ttu-id="ed53e-108">Sie können Objekte mit gegenseitigem Ausschluss in einem Profil verwenden, um die Anforderungen von benutzerdefinierten Szenarios zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ed53e-108">You can use mutual exclusion objects in a profile to meet the needs of custom scenarios.</span></span> <span data-ttu-id="ed53e-109">Wenn Sie den GUID-Wert CLSID \_ wmmutex \_ Unknown an [**iwmmutualexclusion:: settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype)übergeben, informieren Sie das gegenseitige Ausschluss Objekt, dass Sie ein benutzerdefiniertes Szenario verwenden.</span><span class="sxs-lookup"><span data-stu-id="ed53e-109">By passing the GUID value CLSID\_WMMUTEX\_Unknown to [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), you inform the mutual exclusion object that you are using a custom scenario.</span></span>

<span data-ttu-id="ed53e-110">Sie müssen die Streamauswahl manuell steuern, wenn Sie eine Datei mit einem benutzerdefinierten gegenseitigen Ausschluss Wert lesen.</span><span class="sxs-lookup"><span data-stu-id="ed53e-110">You must manually control stream selection when you read a file with a custom mutual exclusion value.</span></span> <span data-ttu-id="ed53e-111">Das Reader-Objekt verwendet den ersten Stream, den Sie dem gegenseitigen Ausschluss als Standardwert hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ed53e-111">The reader object will use the first stream you add to the mutual exclusion as the default.</span></span>

<span data-ttu-id="ed53e-112">Verwenden Sie die folgenden Schritte, um ein benutzerdefiniertes gegenseitiges Ausschluss Objekt zu erstellen und es einem Profil hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="ed53e-112">Use the following steps to create a custom mutual exclusion object and add it to a profile:</span></span>

1.  <span data-ttu-id="ed53e-113">Erstellen Sie einen Profil-Manager, indem Sie die [**wmcreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ed53e-113">Create a profile manager by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="ed53e-114">Beginnen Sie mit einem vorhandenen Profil, oder erstellen Sie ein völlig neues Profil.</span><span class="sxs-lookup"><span data-stu-id="ed53e-114">Either start with an existing profile, or create an entirely new one.</span></span>
    -   <span data-ttu-id="ed53e-115">Wenn Sie ein vorhandenes Profil verwenden, können Sie eine der Load-Methoden der [**iwmprofilemanager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) -Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="ed53e-115">If you are using an existing profile, call one of the load methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="ed53e-116">Fahren Sie dann mit Schritt 4 fort.</span><span class="sxs-lookup"><span data-stu-id="ed53e-116">Then skip to step 4.</span></span>
    -   <span data-ttu-id="ed53e-117">Wenn Sie ein vollständig neues Profil erstellen, nennen Sie [**iwmprofilemanager:: | ateemptyprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span><span class="sxs-lookup"><span data-stu-id="ed53e-117">If you are creating an entirely new profile, call [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span></span>
3.  <span data-ttu-id="ed53e-118">Fügen Sie dem neuen Profildaten Ströme durch Aufrufen von [**iwmprofile:: createnewstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)hinzu.</span><span class="sxs-lookup"><span data-stu-id="ed53e-118">Add streams to the new profile by calling [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).</span></span> <span data-ttu-id="ed53e-119">Konfigurieren Sie die Streams nach Bedarf mithilfe der Methoden von [**iwmstreamconfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span><span class="sxs-lookup"><span data-stu-id="ed53e-119">Configure the streams as needed using the methods of [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span></span> <span data-ttu-id="ed53e-120">Sie können auch **QueryInterface** aufrufen, um auf andere Schnittstellen im Datenstrom-Konfigurationsobjekt zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ed53e-120">You can also call **QueryInterface** to access other interfaces in the stream configuration object.</span></span>

    <span data-ttu-id="ed53e-121">" **Kreatenewstream** " erstellt nur ein streamkonfigurationsobjekt und wirkt sich nicht auf das Profil aus.</span><span class="sxs-lookup"><span data-stu-id="ed53e-121">**CreateNewStream** creates only a stream configuration object, and does not affect the profile.</span></span> <span data-ttu-id="ed53e-122">Nachdem ein Stream ordnungsgemäß konfiguriert wurde, müssen Sie [**iwmprofile:: addstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) zum Hinzufügen des Streams zum Profil aufruft.</span><span class="sxs-lookup"><span data-stu-id="ed53e-122">After a stream is configured properly, you must call [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) to add the stream to the profile.</span></span>

4.  <span data-ttu-id="ed53e-123">Erstellen Sie ein gegenseitiges Ausschluss Objekt durch Aufrufen von [**iwmprofile:: createnewmutualexclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="ed53e-123">Create a mutual exclusion object by calling [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).</span></span>
5.  <span data-ttu-id="ed53e-124">Fügen Sie die gewünschten Datenströme dem gegenseitigen Ausschluss Objekt hinzu, indem Sie [**iwmstreamlist:: addstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) aufrufen (verfügbar direkt von [**iwmmutualexclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), das von [**iwmstreamlist**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)erbt).</span><span class="sxs-lookup"><span data-stu-id="ed53e-124">Add the desired streams to the mutual exclusion object by calling [**IWMStreamList::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (available directly from [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), which inherits from [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).</span></span>
6.  <span data-ttu-id="ed53e-125">Legen Sie den Typ des gegenseitigen Ausschlusses auf Custom fest, indem Sie [**iwmmutualexclusion:: settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ed53e-125">Set the type of mutual exclusion to custom by calling [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span></span> <span data-ttu-id="ed53e-126">Übergeben Sie die CLSID \_ wmmutex \_ Unknown als GUID-Typ.</span><span class="sxs-lookup"><span data-stu-id="ed53e-126">Pass the CLSID\_WMMUTEX\_Unknown as the type GUID.</span></span>
7.  <span data-ttu-id="ed53e-127">Fügen Sie dem Profil das konfigurierte Objekt für den gegenseitigen Ausschluss hinzu, indem Sie [**iwmprofile:: addmutualexclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ed53e-127">Add the configured mutual exclusion object to the profile by calling [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed53e-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ed53e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed53e-129">**Iwmmutualexclusion-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ed53e-129">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="ed53e-130">**Iwmprofile-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ed53e-130">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="ed53e-131">**Iwmprofilemanager-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ed53e-131">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="ed53e-132">**Iwmstreamconfig-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ed53e-132">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[<span data-ttu-id="ed53e-133">**Iwmstreamlist-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ed53e-133">**IWMStreamList Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[<span data-ttu-id="ed53e-134">**Verwenden von gegenseitigem Ausschluss**</span><span class="sxs-lookup"><span data-stu-id="ed53e-134">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="ed53e-135">**Wmkreateprofilemanager**</span><span class="sxs-lookup"><span data-stu-id="ed53e-135">**WMCreateProfileManager**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




