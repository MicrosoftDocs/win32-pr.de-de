---
title: Aufzählen von Geräten (WMDM)
description: Windows Media Geräte-Manager verwaltet einen Cache verbundener Geräte. Erfahren Sie, wie Windows Media Geräte-Manager den Cache verwaltet oder aktualisiert.
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Media Geräte-Manager,Aufzählen von Geräten
- Geräte-Manager,Aufzählen von Geräten
- Programmierhandbuch,Aufzählen von Geräten
- Dienstanbieter,Aufzählen von Geräten
- Erstellen von Dienstanbietern,Aufzählen von Geräten
- Aufzählen von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9b2fd3a891e2c52710bd9a2f6d46a78e9eb238
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112067907"
---
# <a name="enumerating-devices-wmdm"></a><span data-ttu-id="30013-110">Aufzählen von Geräten (WMDM)</span><span class="sxs-lookup"><span data-stu-id="30013-110">Enumerating devices (WMDM)</span></span>

<span data-ttu-id="30013-111">Windows Media Device Manager maintains a cache of connected devices that is updated when a Windows Media Device Manager application starts, when a Plug and Play (PnP) device connects or disconnects, or when the application calls [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span><span class="sxs-lookup"><span data-stu-id="30013-111">Windows Media Device Manager maintains a cache of connected devices that is updated when a Windows Media Device Manager application starts, when a Plug and Play (PnP) device connects or disconnects, or when the application calls [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span></span> <span data-ttu-id="30013-112">Dieser Cache wird für die Anwendung verfügbar gemacht, wenn [**sie IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) oder [**IWMDeviceManager2::EnumDevices2 aufruft.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2)</span><span class="sxs-lookup"><span data-stu-id="30013-112">This cache is exposed to the application when it calls [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) or [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2).</span></span> <span data-ttu-id="30013-113">Jedes Gerät wird als [**IWMDMDevice-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) für die Anwendung verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="30013-113">Each device is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="30013-114">Wenn der Dienstanbieter für die Handhabung von PnP-Geräten registriert ist, Geräte-Manager Windows Media Geräte-Manager die aktuelle Liste der verbundenen Geräte.</span><span class="sxs-lookup"><span data-stu-id="30013-114">If the service provider is registered to handle PnP devices, Windows Media Device Manager will be aware of the current list of connected devices.</span></span> <span data-ttu-id="30013-115">Wenn der Dienstanbieter für die Verarbeitung von Nicht-PnP-Geräten registriert ist, ist der Dienstanbieter für die Suche nach angeschlossenen Geräten verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="30013-115">If the service provider is registered to handle non-PnP devices, the service provider is responsible for discovering attached devices.</span></span> <span data-ttu-id="30013-116">Ein Dienstanbieter kann nur für PnP- oder Nicht-PnP-Geräte registriert werden, nie für beides.</span><span class="sxs-lookup"><span data-stu-id="30013-116">A service provider can only be registered for PnP or non-PnP devices, never both.</span></span>

<span data-ttu-id="30013-117">Die folgenden Aktionen zeigen, wie Windows Media Geräte-Manager ihren Cache verwaltet oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="30013-117">The following actions show how Windows Media Device Manager maintains or updates its cache.</span></span> <span data-ttu-id="30013-118">Beachten Sie, dass der Cache nie aktualisiert wird, wenn ein Nicht-PnP-Gerät eine Verbindung herstellt oder die Verbindung trennt.</span><span class="sxs-lookup"><span data-stu-id="30013-118">Notice that the cache is never updated when a non-PnP device connects or disconnects.</span></span>

<span data-ttu-id="30013-119">Eine Windows Media Geräte-Manager-Anwendung wird gestartet</span><span class="sxs-lookup"><span data-stu-id="30013-119">A Windows Media Device Manager application starts</span></span>

-   <span data-ttu-id="30013-120">Windows Media Geräte-Manager ruft eine Liste der angeschlossenen PnP-Geräte aus dem PnP-Subsystem ab und ruft [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) auf dem SP auf, der für jedes verbundene Gerät registriert ist.</span><span class="sxs-lookup"><span data-stu-id="30013-120">Windows Media Device Manager retrieves a list of attached PnP devices from the PnP subsystem, and calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on the SP registered for each connected device.</span></span> <span data-ttu-id="30013-121">(Der richtige Dienstanbieter wird durch Abfragen des WMDMSPCLSID-Geräteparameters nach der Klassen-ID des für dieses Gerät zuständigen Dienstanbieters gefunden.</span><span class="sxs-lookup"><span data-stu-id="30013-121">(It discovers the correct service provider by querying the WMDMSPCLSID device parameter for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="30013-122">Weitere [Informationen finden Sie](device-parameters.md) unter Geräteparameter.) Alle zurückgegebenen Geräte werden dem Windows Media-Geräte-Manager von Geräten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="30013-122">See [Device Parameters](device-parameters.md) for more information.) All devices returned are added to the Windows Media Device Manager cache of devices.</span></span>
-   <span data-ttu-id="30013-123">Windows Media Geräte-Manager sucht alle bei ihm registrierten Nicht-PnP-Dienstanbieter und ruft [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) auf jedem Dienstanbieter auf, um von jedem Dienstanbieter eine Liste der Geräte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="30013-123">Windows Media Device Manager finds all non-PnP service providers registered with it and calls [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) on each service provider to get a list devices from each one.</span></span> <span data-ttu-id="30013-124">Alle zurückgegebenen Geräte werden dem Cache hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="30013-124">All devices returned are added to the cache.</span></span>

<span data-ttu-id="30013-125">Die Anwendung ruft IWMDeviceManager/2::EnumDevices/2 auf.</span><span class="sxs-lookup"><span data-stu-id="30013-125">The application calls IWMDeviceManager/2::EnumDevices/2</span></span>

-   <span data-ttu-id="30013-126">Windows Media Geräte-Manager gibt die zwischengespeicherte Geräteliste zurück.</span><span class="sxs-lookup"><span data-stu-id="30013-126">Windows Media Device Manager returns its cached device list.</span></span>

<span data-ttu-id="30013-127">Ein PnP-Gerät stellt eine Verbindung</span><span class="sxs-lookup"><span data-stu-id="30013-127">A PnP device connects</span></span>

-   <span data-ttu-id="30013-128">Windows Media Geräte-Manager sucht den entsprechenden Dienstanbieter und ruft **IMDServiceProvider2::CreateDevice** auf und fügt das Gerät dem Cache hinzu.</span><span class="sxs-lookup"><span data-stu-id="30013-128">Windows Media Device Manager finds the relevant service provider and calls **IMDServiceProvider2::CreateDevice**, and adds the device to its cache.</span></span>
-   <span data-ttu-id="30013-129">Wenn die Anwendung [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)implementiert, ruft Windows Media Geräte-Manager [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) mit einer Ankunftsbenachrichtigung auf.</span><span class="sxs-lookup"><span data-stu-id="30013-129">If the application implements [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media Device Manager calls [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) with an arrival notification.</span></span>

<span data-ttu-id="30013-130">Die Verbindung eines PnP-Geräts wird getrennt.</span><span class="sxs-lookup"><span data-stu-id="30013-130">A PnP device disconnects</span></span>

-   <span data-ttu-id="30013-131">Windows Media Geräte-Manager entfernt das Element aus dem Cache.</span><span class="sxs-lookup"><span data-stu-id="30013-131">Windows Media Device Manager removes the item from its cache.</span></span>
-   <span data-ttu-id="30013-132">Wenn die Anwendung IWMDMNotification implementiert, ruft Windows Media Geräte-Manager IWMDMNotification::WMDMMessage mit einer Abflugbenachrichtigung auf.</span><span class="sxs-lookup"><span data-stu-id="30013-132">If the application implements IWMDMNotification, Windows Media Device Manager calls IWMDMNotification::WMDMMessage with a departure notification.</span></span>

<span data-ttu-id="30013-133">Die Anwendung ruft IWMDeviceManager2::Reinitialize auf.</span><span class="sxs-lookup"><span data-stu-id="30013-133">The application calls IWMDeviceManager2::Reinitialize</span></span>

-   <span data-ttu-id="30013-134">Aktualisiert den Cache mit allen verbundenen Geräten.</span><span class="sxs-lookup"><span data-stu-id="30013-134">Refreshes the cache with all connected devices.</span></span>

<span data-ttu-id="30013-135">Ein Nicht-PnP-Gerät verbindet oder trennt die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="30013-135">A non-PnP device connects or disconnects</span></span>

-   <span data-ttu-id="30013-136">Windows Media Geräte-Manager wird nicht über die Ankunft oder den Abflug informiert und führt keine Maßnahmen aus.</span><span class="sxs-lookup"><span data-stu-id="30013-136">Windows Media Device Manager is not informed of the arrival or departure, and takes no action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30013-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="30013-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30013-138">**Erstellen eines Dienstanbieters**</span><span class="sxs-lookup"><span data-stu-id="30013-138">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




