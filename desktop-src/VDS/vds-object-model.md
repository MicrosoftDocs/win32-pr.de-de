---
description: VDS-Objektmodell
ms.assetid: e5fcc19a-e170-4918-85eb-c1457776795a
title: VDS-Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae998955c5d0b7834cf4d88b901537f3644a2ab
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104218902"
---
# <a name="vds-object-model"></a><span data-ttu-id="5523f-103">VDS-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="5523f-103">VDS Object Model</span></span>

<span data-ttu-id="5523f-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="5523f-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="5523f-105">VDS bietet indirekten Zugriff auf Host basierte Speichergeräte, z. b. Datenträger und CD-ROM-Geräte, sowie auf Datenträger Arrays, die von Hardware-RAID-Controllern verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="5523f-105">VDS provides indirect access to host-based storage devices, such as disks and CD-ROM devices, and to disk arrays that are managed by hardware RAID controllers.</span></span> <span data-ttu-id="5523f-106">Während einige Speicher Entitäten physische Geräte modellieren, sind andere Modell-VM-Konstrukte: Volumes, Partitionen usw.</span><span class="sxs-lookup"><span data-stu-id="5523f-106">While some storage entities model physical devices, others model virtual constructs: volumes, partitions, and so on.</span></span> <span data-ttu-id="5523f-107">Die in diesem Thema beschriebenen Objekte stellen die physischen und virtuellen Entitäten von VDS dar.</span><span class="sxs-lookup"><span data-stu-id="5523f-107">The objects that are described in this topic represent both the physical and virtual entities of VDS.</span></span>

<span data-ttu-id="5523f-108">Anwendungen rufen die Methoden auf, die von diesen Objekten verfügbar gemacht werden, und VDS Ruft den entsprechenden Anbieter auf, um die angeforderten Speichervorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5523f-108">Applications call the methods that are exposed by these objects and VDS calls the appropriate provider to perform the requested storage operations.</span></span> <span data-ttu-id="5523f-109">Eine Anwendung ruft ein Anbieter Programm niemals direkt auf.</span><span class="sxs-lookup"><span data-stu-id="5523f-109">An application never calls a provider program directly.</span></span>

### <a name="classification-of-objects"></a><span data-ttu-id="5523f-110">Klassifizierung von Objekten</span><span class="sxs-lookup"><span data-stu-id="5523f-110">Classification of Objects</span></span>

<span data-ttu-id="5523f-111">Wie die folgende Abbildung zeigt, implementieren Softwareanbieter Programme Objekte, die Host basierte Entitäten modellieren. Hardware Anbieter Programme implementieren Objekte, die interne und externe Hardware-RAID-Geräte modellieren. die verbleibenden allgemeinen Objekte sind entweder Anbieter unabhängig oder werden von VDS implementiert.</span><span class="sxs-lookup"><span data-stu-id="5523f-111">As the following illustration shows, software provider programs implement objects that model host-based entities; hardware provider programs implement objects that model internal and external hardware RAID devices; the remaining common objects are either provider-independent, or are implemented by VDS.</span></span> <span data-ttu-id="5523f-112">Eine Spindel, bei der es sich nicht um ein VDS-Objekt handelt, ist ein Begriff für generische Speichermedien, die aus Datenträger-oder Laufwerks Blöcken bestehen.</span><span class="sxs-lookup"><span data-stu-id="5523f-112">A spindle, which is not a VDS object, is a term for generic storage media that comprises of disk or drive extents.</span></span>

![Diagramm, das eine Klassifizierung von Objekten anzeigt, die als "Common Objects", "Software Provider Objects" und "Hardware Provider Objects" definiert sind.](images/vdsobjectmodel.png)

<span data-ttu-id="5523f-114">Weitere Informationen zum Verhalten der einzelnen Objekte finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="5523f-114">To learn more about the behavior of each object, select from the following topics:</span></span>

-   <span data-ttu-id="5523f-115">Dienst Lade-und Dienst Objekte finden Sie unter [Start-und Dienst Objekte](startup-and-service-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5523f-115">Service loader and service objects, see [Startup and Service Objects](startup-and-service-objects.md).</span></span>
-   <span data-ttu-id="5523f-116">Zu Enumerations-und asynchronen Objekten finden Sie unter [Helper-Objekte](helper-objects.md)</span><span class="sxs-lookup"><span data-stu-id="5523f-116">Enumeration and async objects, see [Helper Objects](helper-objects.md).</span></span>
-   <span data-ttu-id="5523f-117">Anbieter Objekt finden Sie unter [Provider Object](provider-object.md).</span><span class="sxs-lookup"><span data-stu-id="5523f-117">Provider object, see [Provider Object](provider-object.md).</span></span>
-   <span data-ttu-id="5523f-118">Zu Paket-, Datenträger-, Volume-und volumeplex-Objekten finden Sie unter [Software Provider Objects](software-provider-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5523f-118">Pack, disk, volume, and volume plex objects, see [Software Provider Objects](software-provider-objects.md).</span></span>
-   <span data-ttu-id="5523f-119">Zu den Objekten Subsystem, Controller, Laufwerk, LUN und LUN Plex finden Sie unter [Hardware Anbieter Objekte](hardware-provider-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5523f-119">Subsystem, controller, drive, LUN, and LUN plex objects, see [Hardware Provider Objects](hardware-provider-objects.md).</span></span>

### <a name="object-creation"></a><span data-ttu-id="5523f-120">Objekterstellung</span><span class="sxs-lookup"><span data-stu-id="5523f-120">Object Creation</span></span>

<span data-ttu-id="5523f-121">Die Konfigurations-und Abfrage Vorgänge, die mit der Objekt Erstellung verknüpft sind, können viel Zeit in Anspruch nehmen. Daher ruft VDS alle Methoden asynchron auf.</span><span class="sxs-lookup"><span data-stu-id="5523f-121">The configuration and query operations that are associated with object creation can take considerable time to complete; as such, VDS invokes all methods asynchronously.</span></span> <span data-ttu-id="5523f-122">Der Ermittlungs Anbieter gibt alle Abschluss-, Fehler-oder Status Änderungs Ereignisse zurück.</span><span class="sxs-lookup"><span data-stu-id="5523f-122">The discovering provider returns all completion, error, or state change events.</span></span> <span data-ttu-id="5523f-123">Software Anbieter protokollieren außerdem alle Fehler und erheblichen Zustandsänderungen.</span><span class="sxs-lookup"><span data-stu-id="5523f-123">Software providers also log all the errors and significant state changes.</span></span>

### <a name="object-deletion"></a><span data-ttu-id="5523f-124">Löschen von Objekten</span><span class="sxs-lookup"><span data-stu-id="5523f-124">Object Deletion</span></span>

<span data-ttu-id="5523f-125">Mit mehreren VDS-Methoden werden VDS-Objekte gelöscht oder transformiert.</span><span class="sxs-lookup"><span data-stu-id="5523f-125">Several VDS methods delete or transform VDS objects.</span></span> <span data-ttu-id="5523f-126">Ein Aufrufer kann einen Verweis über einen Schnittstellen Zeiger auf ein gelöschtes Objekt speichern, nachdem die Methode zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5523f-126">A caller can hold a reference, by way of an interface pointer, to a deleted object after the method returns.</span></span> <span data-ttu-id="5523f-127">Wenn der Aufrufer die-Schnittstelle freigibt, löscht VDS das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5523f-127">When the caller releases the interface, VDS deletes the object.</span></span>

<span data-ttu-id="5523f-128">Im Hinblick auf das Löschen von Objekten sollten Aufrufer keine Ausnahme von der [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für diese Schnittstellen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5523f-128">With regard to object deletion, callers should refrain from invoking anything except the [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on these interfaces.</span></span> <span data-ttu-id="5523f-129">Der Anbieter muss robust genug sein, um mit fehlgeleiteten-Aufrufern zu umgehen. Wenn ein Aufrufer eine Methode für ein gelöschtes Objekt aufruft, sollte der Anbieter das **VDS \_ E- \_ Objekt \_ gelöscht** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5523f-129">The provider must be robust enough to deal with errant callers; if a caller invokes a method on a deleted object, the provider should return **VDS\_E\_OBJECT\_DELETED**.</span></span>

### <a name="service-initialization"></a><span data-ttu-id="5523f-130">Dienstinitialisierung</span><span class="sxs-lookup"><span data-stu-id="5523f-130">Service Initialization</span></span>

<span data-ttu-id="5523f-131">VDS stellt einen Klassen Bezeichner (CLSID) für das Dienst Lade Programm und die Dienst Objekte bereit, aber nur die Dienst Lade Programm-CLSID ist öffentlich.</span><span class="sxs-lookup"><span data-stu-id="5523f-131">VDS supplies a class identifier (Clsid) for the service loader and the service objects, but only the service loader Clsid is public.</span></span> <span data-ttu-id="5523f-132">Die Dienst Initialisierung tritt auf, wenn die Anbieter, eine aufrufenden Anwendung und der Dienst die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="5523f-132">Service initialization occurs when the providers, a calling application, and the service perform the following tasks:</span></span>

-   <span data-ttu-id="5523f-133">Jeder neue Anbieter ruft während der Installation die [**ivdsadmin:: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) -Methode auf, um sich bei VDS zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="5523f-133">Each new provider invokes the [**IVdsAdmin::RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) method during installation to register with VDS.</span></span> <span data-ttu-id="5523f-134">Der-Befehl erstellt einen Registrierungsschlüssel unter der System Struktur, der durch die Objekt-GUID des Anbieters gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="5523f-134">The call creates a registry key under the SYSTEM hive, identified by the object GUID of the provider.</span></span> <span data-ttu-id="5523f-135">Unter diesem Schlüssel ist die CLSID des Anbieter Objekts, der Name, die Version und die Versions-GUID des Anbieters enthalten.</span><span class="sxs-lookup"><span data-stu-id="5523f-135">Contained under this key is the Clsid of the provider object, the name, version, and the version GUID of the provider.</span></span>
    > [!Note]  
    > <span data-ttu-id="5523f-136">Anbieter Objekt-GUIDs sind persistent. die Software-und Hardware Objekt-GUIDs sind nicht.</span><span class="sxs-lookup"><span data-stu-id="5523f-136">Provider object GUIDs are persistent; software and hardware object GUIDs are not.</span></span>

     

-   <span data-ttu-id="5523f-137">Eine Anwendung ruft die [**cokreatzustance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion auf und übergibt die Dienst Ladefunktion CLSID als Argument.</span><span class="sxs-lookup"><span data-stu-id="5523f-137">An application calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, passing the service loader Clsid as an argument.</span></span> <span data-ttu-id="5523f-138">Mit einem Zeiger auf das Service Loader-Objekt kann die Anwendung VDS entweder lokal oder Remote starten, indem der gewünschte Computername als Parameter an die [**ivdsserviceloader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) -Methode übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5523f-138">With a pointer to the service loader object, the application can start VDS either locally or remotely by passing the desired computer name as a parameter to the [**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) method.</span></span>
-   <span data-ttu-id="5523f-139">Wenn die anfängliche Anwendung an den Dienst angefügt wird, ruft VDS zuerst [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) für jede CLSID auf, die unter dem Registrierungsschlüssel gefunden wurde, und ruft dann die [**ivdsproviderprivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) -Methode für jeden Anbieter auf, um die Programme zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="5523f-139">When the initial application attaches to the service, VDS first calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on each Clsid found under the registry key, and then calls the [**IVdsProviderPrivate::OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) method on each provider to initialize the programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5523f-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5523f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5523f-141">Informationen zu VDS</span><span class="sxs-lookup"><span data-stu-id="5523f-141">About VDS</span></span>](about-vds.md)
</dt> <dt>

[<span data-ttu-id="5523f-142">**Ivdsadmin:: RegisterProvider**</span><span class="sxs-lookup"><span data-stu-id="5523f-142">**IVdsAdmin::RegisterProvider**</span></span>](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider)
</dt> <dt>

[<span data-ttu-id="5523f-143">**Ivdsserviceloader:: loadservice**</span><span class="sxs-lookup"><span data-stu-id="5523f-143">**IVdsServiceLoader::LoadService**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[<span data-ttu-id="5523f-144">**Ivdsproviderprivate:: OnLoad**</span><span class="sxs-lookup"><span data-stu-id="5523f-144">**IVdsProviderPrivate::OnLoad**</span></span>](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> </dl>

 

 
