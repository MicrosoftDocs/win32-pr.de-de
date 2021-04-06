---
title: Auflisten von Geräten (WMDM)
description: Auflisten von Geräten
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Media Device Manager, Auflisten von Geräten
- Device Manager, Auflisten von Geräten
- Programmier Handbuch zum Auflisten von Geräten
- Dienstanbieter, Auflisten von Geräten
- Erstellen von Dienstanbietern, Auflisten von Geräten
- Auflisten von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316b87f6ad3f5680e0c22da832da7b1efec24629
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "103719553"
---
# <a name="enumerating-devices-wmdm"></a><span data-ttu-id="4f983-109">Auflisten von Geräten (WMDM)</span><span class="sxs-lookup"><span data-stu-id="4f983-109">Enumerating devices (WMDM)</span></span>

<span data-ttu-id="4f983-110">Windows Media Device Manager verwaltet einen Cache verbundener Geräte, die beim Starten einer Windows Media Device Manager-Anwendung aktualisiert werden, wenn ein Plug & Play (PNP)-Gerät eine Verbindung herstellt oder trennt oder wenn die Anwendung [**IWMDeviceManager2:: Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize)aufruft.</span><span class="sxs-lookup"><span data-stu-id="4f983-110">Windows Media Device Manager maintains a cache of connected devices that is updated when a Windows Media Device Manager application starts, when a Plug and Play (PnP) device connects or disconnects, or when the application calls [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span></span> <span data-ttu-id="4f983-111">Dieser Cache wird für die Anwendung verfügbar gemacht, wenn er [**iwmdevicemanager:: enumdevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) oder [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2)aufruft.</span><span class="sxs-lookup"><span data-stu-id="4f983-111">This cache is exposed to the application when it calls [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) or [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2).</span></span> <span data-ttu-id="4f983-112">Jedes Gerät wird für die Anwendung als [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Schnittstelle verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="4f983-112">Each device is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="4f983-113">Wenn der Dienstanbieter für die Behandlung von PNP-Geräten registriert ist, ist die aktuelle Liste der verbundenen Geräte in Windows Media Device Manager bekannt.</span><span class="sxs-lookup"><span data-stu-id="4f983-113">If the service provider is registered to handle PnP devices, Windows Media Device Manager will be aware of the current list of connected devices.</span></span> <span data-ttu-id="4f983-114">Wenn der Dienstanbieter für die Behandlung von nicht-PnP-Geräten registriert ist, ist der Dienstanbieter für die Ermittlung angefügter Geräte verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="4f983-114">If the service provider is registered to handle non-PnP devices, the service provider is responsible for discovering attached devices.</span></span> <span data-ttu-id="4f983-115">Ein Dienstanbieter kann nur für PNP-oder nicht-PNP-Geräte registriert werden.</span><span class="sxs-lookup"><span data-stu-id="4f983-115">A service provider can only be registered for PnP or non-PnP devices, never both.</span></span>

<span data-ttu-id="4f983-116">Die folgenden Aktionen zeigen, wie der Cache von Windows Media Device Manager verwaltet oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="4f983-116">The following actions show how Windows Media Device Manager maintains or updates its cache.</span></span> <span data-ttu-id="4f983-117">Beachten Sie, dass der Cache nie aktualisiert wird, wenn ein nicht-PNP-Gerät eine Verbindung herstellt oder die Verbindung trennt.</span><span class="sxs-lookup"><span data-stu-id="4f983-117">Notice that the cache is never updated when a non-PnP device connects or disconnects.</span></span>

<span data-ttu-id="4f983-118">Ein Windows Media Device Manager-Anwendung wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="4f983-118">A Windows Media Device Manager application starts</span></span>

-   <span data-ttu-id="4f983-119">Windows Media Device Manager ruft eine Liste angefügter PNP-Geräte aus dem PNP-Subsystem ab und ruft [**IMDServiceProvider2:: foratedevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) auf dem SP auf, der für jedes verbundene Gerät registriert ist.</span><span class="sxs-lookup"><span data-stu-id="4f983-119">Windows Media Device Manager retrieves a list of attached PnP devices from the PnP subsystem, and calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on the SP registered for each connected device.</span></span> <span data-ttu-id="4f983-120">(Er ermittelt den korrekten Dienstanbieter durch Abfragen des wmdmspclsid-Geräte Parameters auf die Klassen-ID des für dieses Gerät Verantwortlichen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="4f983-120">(It discovers the correct service provider by querying the WMDMSPCLSID device parameter for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="4f983-121">Weitere Informationen finden Sie unter [Geräteparameter](device-parameters.md) .) Alle zurückgegebenen Geräte werden dem Windows Media Device Manager-Cache von Geräten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4f983-121">See [Device Parameters](device-parameters.md) for more information.) All devices returned are added to the Windows Media Device Manager cache of devices.</span></span>
-   <span data-ttu-id="4f983-122">Windows Media Device Manager findet alle nicht-PNP-Dienstanbieter, die bei ihm registriert sind, und ruft [**imdserviceprovider:: enumdevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) für jeden Dienstanbieter auf, um eine Liste der Geräte von jedem Dienstanbieter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4f983-122">Windows Media Device Manager finds all non-PnP service providers registered with it and calls [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) on each service provider to get a list devices from each one.</span></span> <span data-ttu-id="4f983-123">Alle zurückgegebenen Geräte werden dem Cache hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4f983-123">All devices returned are added to the cache.</span></span>

<span data-ttu-id="4f983-124">Die Anwendung ruft iwmdevicemanager/2:: enumdevices/2 auf.</span><span class="sxs-lookup"><span data-stu-id="4f983-124">The application calls IWMDeviceManager/2::EnumDevices/2</span></span>

-   <span data-ttu-id="4f983-125">Die Liste der zwischengespeicherten Geräte wird von Windows Media Device Manager zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f983-125">Windows Media Device Manager returns its cached device list.</span></span>

<span data-ttu-id="4f983-126">Ein PNP-Gerät verbindet</span><span class="sxs-lookup"><span data-stu-id="4f983-126">A PnP device connects</span></span>

-   <span data-ttu-id="4f983-127">Windows Media Device Manager findet den relevanten Dienstanbieter und ruft **IMDServiceProvider2:: anatedevice** auf und fügt das Gerät seinem Cache hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f983-127">Windows Media Device Manager finds the relevant service provider and calls **IMDServiceProvider2::CreateDevice**, and adds the device to its cache.</span></span>
-   <span data-ttu-id="4f983-128">Wenn die Anwendung [**iwmdmnotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)implementiert, ruft Windows Media Device Manager mit einer Ankunfts Benachrichtigung [**iwmdmnotification:: wmdmmess**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) auf.</span><span class="sxs-lookup"><span data-stu-id="4f983-128">If the application implements [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media Device Manager calls [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) with an arrival notification.</span></span>

<span data-ttu-id="4f983-129">Ein PNP-Gerät trennt die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="4f983-129">A PnP device disconnects</span></span>

-   <span data-ttu-id="4f983-130">Windows Media Device Manager entfernt das Element aus dem Cache.</span><span class="sxs-lookup"><span data-stu-id="4f983-130">Windows Media Device Manager removes the item from its cache.</span></span>
-   <span data-ttu-id="4f983-131">Wenn die Anwendung iwmdmnotification implementiert, ruft Windows Media Device Manager iwmdmnotification:: wmdmmess mit einer Abflug Benachrichtigung auf.</span><span class="sxs-lookup"><span data-stu-id="4f983-131">If the application implements IWMDMNotification, Windows Media Device Manager calls IWMDMNotification::WMDMMessage with a departure notification.</span></span>

<span data-ttu-id="4f983-132">Die Anwendung ruft IWMDeviceManager2:: Reinitialize auf.</span><span class="sxs-lookup"><span data-stu-id="4f983-132">The application calls IWMDeviceManager2::Reinitialize</span></span>

-   <span data-ttu-id="4f983-133">Aktualisiert den Cache mit allen verbundenen Geräten.</span><span class="sxs-lookup"><span data-stu-id="4f983-133">Refreshes the cache with all connected devices.</span></span>

<span data-ttu-id="4f983-134">Ein nicht-PNP-Gerät stellt eine Verbindung her und trennt die Verbindung</span><span class="sxs-lookup"><span data-stu-id="4f983-134">A non-PnP device connects or disconnects</span></span>

-   <span data-ttu-id="4f983-135">Windows Media Device Manager wird nicht über die Ankunft oder den Abbruch informiert und führt keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="4f983-135">Windows Media Device Manager is not informed of the arrival or departure, and takes no action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f983-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4f983-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f983-137">**Erstellen eines Dienstanbieters**</span><span class="sxs-lookup"><span data-stu-id="4f983-137">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




