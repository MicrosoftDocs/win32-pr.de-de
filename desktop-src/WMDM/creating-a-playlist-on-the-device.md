---
title: Erstellen einer Wiedergabeliste auf dem Gerät
description: Erstellen einer Wiedergabeliste auf dem Gerät
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Windows Media Device Manager, Wiedergabelisten
- Device Manager, Wiedergabelisten
- Programmier Handbuch, Wiedergabelisten
- Desktop Anwendungen, Wiedergabelisten
- Erstellen von Windows Media Device Manager-Anwendungen, Wiedergabelisten
- abstrakte Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287cc406b795db07fde3f10103822dea32185a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309772"
---
# <a name="creating-a-playlist-on-the-device"></a><span data-ttu-id="81cd8-109">Erstellen einer Wiedergabeliste auf dem Gerät</span><span class="sxs-lookup"><span data-stu-id="81cd8-109">Creating a Playlist on the Device</span></span>

<span data-ttu-id="81cd8-110">Das Windows Media Device Manager SDK bietet die Möglichkeit, dass eine MTP-Anwendung eine Wiedergabeliste auf einem Gerät erstellt.</span><span class="sxs-lookup"><span data-stu-id="81cd8-110">The Windows Media Device Manager SDK provides the means for an MTP application to create a playlist on a device.</span></span> <span data-ttu-id="81cd8-111">Diese Art von Wiedergabeliste wird als *abstrakte* Wiedergabeliste bezeichnet, da die Datei, die auf dem Gerät erstellt wird, keine Mediendaten enthält, sondern nur Metadaten, die die Links zu Mediendateien in der Wiedergabeliste enthalten.</span><span class="sxs-lookup"><span data-stu-id="81cd8-111">This type of playlist is called an *abstract* playlist, because the file created on the device contains no media data, but only metadata, which holds the links to media files in the playlist.</span></span>

<span data-ttu-id="81cd8-112">Andere abstrakte Elemente, die auf dem Gerät erstellt werden können, umfassen Alben (im wesentlichen Wiedergabelisten mit zusätzlichen Eigenschaften wie z. b. Cover Art), Kontakte und Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="81cd8-112">Other abstract items that can be created on the device include albums (essentially playlists with extra properties such as cover art), contacts, and messages.</span></span>

<span data-ttu-id="81cd8-113">**So erstellen Sie eine Wiedergabeliste**</span><span class="sxs-lookup"><span data-stu-id="81cd8-113">**To create a playlist**</span></span>

1.  <span data-ttu-id="81cd8-114">Beschaffen einer [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) -Schnittstelle für das Zielgerät.</span><span class="sxs-lookup"><span data-stu-id="81cd8-114">Acquire an [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) interface to the target device.</span></span>
2.  <span data-ttu-id="81cd8-115">Rufen Sie [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) auf, um die Eigenschaft "g \_ wszwmdmformatssupported" zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="81cd8-115">Call [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) to obtain the g\_wszWMDMFormatsSupported property.</span></span>
3.  <span data-ttu-id="81cd8-116">Wenn keine Wiedergabelisten Formate unterstützt werden, lassen Sie das Senden von Wiedergabelisten an das Gerät nicht zu und überspringen Sie die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="81cd8-116">If no playlist formats are supported, disallow sending playlists to the device, and skip the following steps.</span></span> <span data-ttu-id="81cd8-117">Wählen Sie andernfalls den Geräte gestützten Formatierungs Code aus, der dem gewünschten Objekttyp am ehesten entspricht.</span><span class="sxs-lookup"><span data-stu-id="81cd8-117">Otherwise, choose the device-supported format code that matches most closely the intended object type.</span></span> <span data-ttu-id="81cd8-118">Die allgemeinen Codes "WMDM \_ Formatcode \_ abstractaudiovideoplaylist" und "WMDM \_ Formatcode \_ abstractaudiolaylist" werden am häufigsten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81cd8-118">The generic WMDM\_FORMATCODE\_ABSTRACTAUDIOVIDEOPLAYLIST and WMDM\_FORMATCODE\_ABSTRACTAUDIOLAYLIST format codes are the most commonly supported.</span></span>
4.  <span data-ttu-id="81cd8-119">Rufen Sie eine [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) -Schnittstelle für den Speicher (das Stammverzeichnis oder einen Ordner) ab, in dem Sie das Objekt erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="81cd8-119">Obtain an [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) interface for the storage (the root or a folder) where you want to create the object.</span></span> <span data-ttu-id="81cd8-120">Einige Geräte funktionieren am besten, wenn das Wiedergabelisten Objekt in einem Ordner der obersten Ebene mit dem Namen "Playlists" platziert wird.</span><span class="sxs-lookup"><span data-stu-id="81cd8-120">Some devices work best if the playlist object is placed in a top level folder named "Playlists".</span></span>
5.  <span data-ttu-id="81cd8-121">Erstellen Sie ein leeres Metadatenobjekt mithilfe von [**IWMDMStorage3:: CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span><span class="sxs-lookup"><span data-stu-id="81cd8-121">Create an empty metadata object by using [**IWMDMStorage3::CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span></span>
6.  <span data-ttu-id="81cd8-122">Wenn Sie die im vorherigen Schritt abzurufende **iwmdmmetadata** -Schnittstelle verwenden, nennen Sie [**iwmdmmetadata:: AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) , um den ausgewählten Format Code (aus Schritt 3) den speichermetadateneigenschaften hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="81cd8-122">Using the **IWMDMMetaData** interface obtained in the previous step, call [**IWMDMMetaData::AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) to add your chosen format code (from step 3) to the storage metadata properties.</span></span>
7.  <span data-ttu-id="81cd8-123">Abrufen der [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) -Schnittstelle von der **IWMDMStorage3** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="81cd8-123">Obtain the [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) interface from the **IWMDMStorage3** interface.</span></span>
8.  <span data-ttu-id="81cd8-124">Ruft [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) auf, um eine neue Wiedergabelisten Datei in den ausgewählten Speicher einzufügen.</span><span class="sxs-lookup"><span data-stu-id="81cd8-124">Call [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) to insert a new playlist file in the selected storage.</span></span> <span data-ttu-id="81cd8-125">Diese Datei enthält die Metadaten, die von der in Schritt 5 erstellten **iwmdmmetadata** -Schnittstelle dargestellt und an **Insert3** übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="81cd8-125">This file contains the metadata represented by the **IWMDMMetaData** interface you created in step 5 and passed to **Insert3**.</span></span> <span data-ttu-id="81cd8-126">Die-Methode gibt eine **iwmdmstorage** -Schnittstelle für die Wiedergabelisten Datei zurück. Sie können die [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) -Schnittstelle Abfragen.</span><span class="sxs-lookup"><span data-stu-id="81cd8-126">The method returns an **IWMDMStorage** interface for the playlist file; you can query for the [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) interface.</span></span>
9.  <span data-ttu-id="81cd8-127">Rufen Sie [**IWMDMStorage4:: setreferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) auf, um Verweise auf die **iwmdmstorage** -Schnittstellen der Mediendateien in der Wiedergabeliste zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="81cd8-127">Call [**IWMDMStorage4::SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) to create references to the **IWMDMStorage** interfaces of the media files in the playlist.</span></span>

<span data-ttu-id="81cd8-128">Beispielcode finden Sie in der \_ onkreatewiedergabe-Funktion in der [Beispiel-Desktop Anwendung](sample-desktop-application.md).</span><span class="sxs-lookup"><span data-stu-id="81cd8-128">For example code, see the \_OnCreatePlaylist function in the [Sample Desktop Application](sample-desktop-application.md).</span></span>

> [!Note]  
> <span data-ttu-id="81cd8-129">Der von Microsoft bereitgestellte MTP-Dienstanbieter ermöglicht es einer Anwendung, Verweise in Metadaten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="81cd8-129">The Microsoft-provided MTP service provider enables an application to set references in metadata.</span></span> <span data-ttu-id="81cd8-130">Zum Implementieren von Wiedergabelisten muss Ihre Anwendung mit einem MTP-Gerät kommunizieren, oder es muss ein benutzerdefinierter Dienstanbieter verwendet werden, der abstrakte Objekte verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="81cd8-130">To implement playlists, your application must be communicating with an MTP device or using a custom service provider that can handle abstract objects.</span></span> <span data-ttu-id="81cd8-131">Der CE-Dienstanbieter verarbeitet Wiedergabelisten-und Album Objekte.</span><span class="sxs-lookup"><span data-stu-id="81cd8-131">The CE service provider handles playlist and album objects.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="81cd8-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="81cd8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81cd8-133">**Schreiben von Dateien auf das Gerät**</span><span class="sxs-lookup"><span data-stu-id="81cd8-133">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




