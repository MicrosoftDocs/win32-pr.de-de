---
title: Untersuchen eines Geräts
description: Untersuchen eines Geräts
ms.assetid: 8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0
keywords:
- Windows Media Device Manager, untersuchen von Geräten
- Device Manager, untersuchen von Geräten
- Programmier Handbuch, untersuchen von Geräten
- Desktop Anwendungen, untersuchen von Geräten
- Erstellen von Windows Media Device Manager-Anwendungen, untersuchen von Geräten
- Untersuchen von Geräten
- Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc154960a4c95efbdf2626271ba90000df99ae8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388348"
---
# <a name="exploring-a-device"></a><span data-ttu-id="89911-110">Untersuchen eines Geräts</span><span class="sxs-lookup"><span data-stu-id="89911-110">Exploring a Device</span></span>

<span data-ttu-id="89911-111">Das Durchsuchen eines Geräts ähnelt dem untersuchen eines Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="89911-111">Exploring a device is similar to exploring a disk drive.</span></span> <span data-ttu-id="89911-112">Alle Objekte auf einem Gerät werden als " *Speicher*" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="89911-112">All objects on a device are called *storages*.</span></span> <span data-ttu-id="89911-113">Ein Speicher kann eine Datei, ein Ordner oder ein abstraktes Objekt (z. b. eine Wiedergabeliste) auf dem Gerät sein.</span><span class="sxs-lookup"><span data-stu-id="89911-113">A storage can be a file, folder, or abstract object (such as a playlist) on the device.</span></span> <span data-ttu-id="89911-114">Sie müssen die Attribute und Metadaten eines Speichers überprüfen (falls unterstützt), um zu verstehen, welche Art von Speicher er ist.</span><span class="sxs-lookup"><span data-stu-id="89911-114">You must examine a storage's attributes and metadata (if supported) to understand what kind of storage it is.</span></span> <span data-ttu-id="89911-115">Storages sind hierarchisch auf dem Gerät organisiert. jeder Speicher verfügt über genau ein übergeordnetes Element, und alle Speicher werden letztendlich von einem einzelnen Stamm Gerätespeicher mit dem Namen " \\ " abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="89911-115">Storages are organized hierarchically on the device; every storage has exactly one parent, and all storages ultimately descend from a single root device storage, typically named "\\".</span></span>

<span data-ttu-id="89911-116">In den folgenden Schritten wird beschrieben, wie Sie ein Gerät durchsuchen:</span><span class="sxs-lookup"><span data-stu-id="89911-116">The following steps describe how to explore a device:</span></span>

1.  <span data-ttu-id="89911-117">Holen Sie sich die [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Schnittstelle eines Geräts, wie unter Auflisten von [Geräten](enumerating-devices.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="89911-117">Get the [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface of a device as described in [Enumerating Devices](enumerating-devices.md).</span></span>
2.  <span data-ttu-id="89911-118">Rufen Sie [**iwmdmdevice:: enumstorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) auf, um eine [**iwmdmenumstorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="89911-118">Call [**IWMDMDevice::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) to retrieve an [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) interface.</span></span> <span data-ttu-id="89911-119">Diese Schnittstelle wird verwendet, um alle untergeordneten Objekte des Speichers zu erhalten, der diese Schnittstelle zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="89911-119">This interface is used to get all child objects of the storage that returns this interface.</span></span> <span data-ttu-id="89911-120">Wenn Sie diese Schnittstelle vom Gerät erhalten, so wie es hier der Fall ist, enthält Sie nur einen Speicher: den Stamm Gerätespeicher.</span><span class="sxs-lookup"><span data-stu-id="89911-120">When getting this interface from the device, as we are here, it will hold only one storage: the root device storage.</span></span>
3.  <span data-ttu-id="89911-121">Rufen Sie [**iwmdmenumschlag:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) mit einer Anzahl von 1 auf, um die [**iwmdmstorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) -Schnittstelle für den Stamm Gerätespeicher abzurufen.</span><span class="sxs-lookup"><span data-stu-id="89911-121">Call [**IWMDMEnumStorage::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) with a count of 1 to retrieve the [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) interface for the root device storage.</span></span> <span data-ttu-id="89911-122">(Sie können nicht mehr als ein untergeordnetes Element vom Gerät anfordern.)</span><span class="sxs-lookup"><span data-stu-id="89911-122">(You cannot request more than one child from the device.)</span></span>
4.  <span data-ttu-id="89911-123">Überprüfen Sie alle Speicherplatz auf dem Gerät, indem Sie " [**iwmdmstorage:: enumstorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) " rekursiv aufrufen und anschließend " **iwmdmenumstorage:: Next** ", um untergeordnete Elemente eines Speichers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="89911-123">Examine all storages on the device by recursively calling [**IWMDMStorage::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) and then **IWMDMEnumStorage::Next** to get children of a storage.</span></span> <span data-ttu-id="89911-124">Wenn Sie feststellen möchten, ob ein Speicher über untergeordnete Elemente verfügt, um die Aufrufe von **enumstorage** und **Next** zu vermeiden, können Sie [**iwmdmstorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) aufrufen, um nach den Flags zu suchen, in denen WMDM \_ Storage \_ attr \_ Dateien aufweist, \_ oder der WMDM- \_ Speicher \_ attr \_ \_</span><span class="sxs-lookup"><span data-stu-id="89911-124">To see if a storage has children to avoid the calls to **EnumStorage** and **Next**, you can call [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) to check for the flags WMDM\_STORAGE\_ATTR\_HAS\_FILES or WMDM\_STORAGE\_ATTR\_HAS\_FOLDERS.</span></span> <span data-ttu-id="89911-125">Weitere Informationen zum Ermitteln der Eigenschaften eines Speichers finden Sie unter Get [and Setting Metadata and Attribute](getting-and-setting-metadata-and-attributes.md) und get [and Setting Metadata and Attribute in the Application](getting-and-setting-metadata-and-attributes-in-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="89911-125">For more information about how to get the properties of a storage, see [Getting and Setting Metadata and Attributes](getting-and-setting-metadata-and-attributes.md) and [Getting and Setting Metadata and Attributes in the Application](getting-and-setting-metadata-and-attributes-in-the-application.md).</span></span>

<span data-ttu-id="89911-126">Windows Media Device Manager macht keinen Standardsatz von Ordnern verfügbar, die Medien eines bestimmten Typs enthalten (z. b. den Ordner "meine Wiedergabe" für Wiedergabelisten).</span><span class="sxs-lookup"><span data-stu-id="89911-126">Windows Media Device Manager does not expose a standard set of folders to hold media of a specific type (for example, a "My Playlists" folder for playlists).</span></span> <span data-ttu-id="89911-127">Jedes Gerät verfügt über ein eindeutiges Dateisystem, und Sie müssen sich an einem geeigneten Ort entscheiden, um eine bestimmte Datei zu suchen oder zu senden.</span><span class="sxs-lookup"><span data-stu-id="89911-127">Every device has a unique file system, and you will have to decide on an appropriate place to look for, or to send, a specific file.</span></span>

> [!Note]  
> <span data-ttu-id="89911-128">In Windows-Explorer können virtuelle Ordner angezeigt werden, die nicht tatsächlich auf dem Gerät vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="89911-128">Windows Explorer can show virtual folders that do not actually exist on the device.</span></span> <span data-ttu-id="89911-129">Virtuelle Beispiel Ordner sind die Ordner "Media" und "Data", die für MTP-Geräte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="89911-129">Example virtual folders are the "Media" and "Data" folders displayed for MTP devices.</span></span> <span data-ttu-id="89911-130">Diese Ordner werden von Windows erstellt, um die Downloads für Endbenutzer zu vereinfachen. Sie sind nicht tatsächlich auf dem Gerät vorhanden.</span><span class="sxs-lookup"><span data-stu-id="89911-130">These folders are created by Windows to make downloads simpler for end users; they do not actually exist on the device.</span></span> <span data-ttu-id="89911-131">Die Anwendung sollte nicht von der Suche nach diesen Typen allgemeiner Ordner abhängen.</span><span class="sxs-lookup"><span data-stu-id="89911-131">Your application should not depend on finding these types of general folders.</span></span> <span data-ttu-id="89911-132">Im Gegensatz dazu zeigt Windows-Explorer möglicherweise einige Ordner oder Objekte an, die auf dem Gerät vorhanden sind (z. b. Wiedergabelisten).</span><span class="sxs-lookup"><span data-stu-id="89911-132">Conversely, Windows Explorer might not show some folders or objects that do exist on the device (for example, playlists).</span></span>

 

<span data-ttu-id="89911-133">Der folgende C++-Beispielcode veranschaulicht die rekursive Untersuchung eines Geräts.</span><span class="sxs-lookup"><span data-stu-id="89911-133">The following C++ example code demonstrates the recursive exploration of a device.</span></span> <span data-ttu-id="89911-134">Es verwendet zwei Funktionen:</span><span class="sxs-lookup"><span data-stu-id="89911-134">It uses two functions:</span></span>

-   <span data-ttu-id="89911-135">"Exploredevice", eine Start Funktion, die einen Geräte Zeiger empfängt und einen Zeiger auf den Stamm Enumerator für dieses Gerät erhält.</span><span class="sxs-lookup"><span data-stu-id="89911-135">ExploreDevice, a starting function that receives a device pointer and obtains a pointer to the root enumerator for that device.</span></span>
-   <span data-ttu-id="89911-136">Recursiveexplorestorage, das aufgerufen wird, um ein Gerät rekursiv zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="89911-136">RecursiveExploreStorage, which is called to explore a device recursively.</span></span>


```C++
// Get the root enumerator and start the recursive function.
HRESULT ExploreDevice(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get a root enumerator.
    CComPtr<IWMDMEnumStorage> pEnumStorage;
    hr = pDevice->EnumStorage(&pEnumStorage);
    if (SUCCEEDED(hr))
    {
        RecursiveExploreStorage(pEnumStorage);
    }
    return hr;
}

// Recursively explore a storage.
void RecursiveExploreStorage(IWMDMEnumStorage* pEnumStorage)
{
    HRESULT hr = S_OK;
    CComPtr<IWMDMStorage> pStorage;

    ULONG numRetrieved = 0;
    // Loop through all storages in the current storage.
    while((pEnumStorage->Next(1, &pStorage, &numRetrieved) == S_OK) && (numRetrieved == 1))
    {
        // Get the name of the object.
        const UINT MAX_LEN = 255;
        WCHAR name[MAX_LEN];
        hr = pStorage->GetName((LPWSTR)&name, MAX_LEN);
        // TODO: Display the retrieved storage name

        // If this is a folder, recurse into it.
        if (attributes & WMDM_FILE_ATTR_FOLDER)
        {
            CComPtr<IWMDMEnumStorage> pEnumSubStorage;
            hr = pStorage->EnumStorage(&pEnumSubStorage);
            if (SUCCEEDED(hr)
            {
                RecursiveExploreStorage(pEnumSubStorage);
            }
        }
        pStorage.Release();
    } // Get the next storage pointer.
    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="89911-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="89911-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89911-138">**Erstellen einer Windows Media Device Manager-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="89911-138">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




