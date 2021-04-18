---
title: Geräte Registrierungs Objekt
description: Geräte Registrierungs Objekt
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- Windows Media-Format-SDK, Geräte Registrierungs Objekte
- Advanced Systems Format (ASF), Geräte Registrierungs Objekte
- ASF (Advanced Systems Format), Geräte Registrierungs Objekte
- Objekte, Geräte Registrierungs Objekte
- Geräte Registrierungs Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6b72637cf7ba439d0bb38109645742cda4ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106337634"
---
# <a name="device-registration-object"></a><span data-ttu-id="7517e-108">Geräte Registrierungs Objekt</span><span class="sxs-lookup"><span data-stu-id="7517e-108">Device Registration Object</span></span>

<span data-ttu-id="7517e-109">Mit dem Geräte Registrierungs Objekt wird die Geräte Registrierungsdatenbank verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7517e-109">The device registration object manages the device registration database.</span></span> <span data-ttu-id="7517e-110">In dieser Datenbank werden Informationen zu Netzwerkgeräten, wie z. b. Set-Top-Video Playern, gespeichert, die mit dem Client Computer verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="7517e-110">This database stores information about network devices, such as set-top video players, that are connected to the client computer.</span></span> <span data-ttu-id="7517e-111">Der primäre Zweck der Geräte Registrierungsdatenbank ist die Verwaltung von Geräten, von denen das Windows Media DRM 10 for Network Devices-Protokoll verwendet wird, um gesicherte Datenströme zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="7517e-111">The primary purpose of the device registration database is to manage devices that use the Windows Media DRM 10 for Network Devices protocol to receive secured data streams.</span></span>

<span data-ttu-id="7517e-112">Wenn Ihre Anwendung Windows Media DRM 10 für Netzwerkgeräte unterstützt, müssen Sie die Schnittstellen dieses Objekts verwenden, um Netzwerkgeräte zu registrieren und diese Geräte zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7517e-112">If your application supports Windows Media DRM 10 for Network Devices, you must use the interfaces of this object to register network devices, and to validate those devices.</span></span> <span data-ttu-id="7517e-113">Sie können die Geräte Registrierungsdatenbank auch zum Speichern von Informationen zu Netzwerkgeräten verwenden, die nicht Windows Media DRM 10 für Netzwerkgeräte verwenden, obwohl nicht alle Informationen in der-Datenbank auf solche Geräte angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7517e-113">You can also use the device registration database to store information about network devices that do not use Windows Media DRM 10 for Network Devices, although not all of the information in the database will apply to such devices.</span></span>

<span data-ttu-id="7517e-114">Das Geräte Registrierungs Objekt wird von der [**wmkreatedeviceregistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) -Funktion erstellt, mit der ein Zeiger auf eine **iwmdeviceregistration** -Schnittstelle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7517e-114">The device registration object is created by the [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) function, which sets a pointer to an **IWMDeviceRegistration** interface.</span></span> <span data-ttu-id="7517e-115">Die anderen Methoden des Geräte Registrierungs Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7517e-115">The other methods of the device registration object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="7517e-116">Die folgenden Schnittstellen werden vom Geräte Registrierungs Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7517e-116">The following interfaces are supported by the device registration object.</span></span>



| <span data-ttu-id="7517e-117">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7517e-117">Interface</span></span>                                              | <span data-ttu-id="7517e-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7517e-118">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="7517e-119">**Iwmdeviceregistration**</span><span class="sxs-lookup"><span data-stu-id="7517e-119">**IWMDeviceRegistration**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | <span data-ttu-id="7517e-120">Verwaltet die Geräte Registrierungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="7517e-120">Manages the device registration database.</span></span> |
| [<span data-ttu-id="7517e-121">**Iwmdrmmessageparser**</span><span class="sxs-lookup"><span data-stu-id="7517e-121">**IWMDRMMessageParser**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | <span data-ttu-id="7517e-122">Analysiert Nachrichten, die von Geräten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7517e-122">Parses messages sent by devices.</span></span>          |
| [<span data-ttu-id="7517e-123">**Iwmproximityerkennung**</span><span class="sxs-lookup"><span data-stu-id="7517e-123">**IWMProximityDetection**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | <span data-ttu-id="7517e-124">Verwaltet die Gerätevalidierung.</span><span class="sxs-lookup"><span data-stu-id="7517e-124">Manages device validation.</span></span>                |



 

<span data-ttu-id="7517e-125">Die folgende Rückruf Schnittstelle muss von der Anwendung implementiert werden, damit die-Methoden der **iwmproximityerkennungs** -Schnittstelle verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="7517e-125">The following callback interface must be implemented by the application in order to use the methods of the **IWMProximityDetection** interface.</span></span>



| <span data-ttu-id="7517e-126">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7517e-126">Interface</span></span>                                      | <span data-ttu-id="7517e-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7517e-127">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="7517e-128">**Iwmstatus Callback**</span><span class="sxs-lookup"><span data-stu-id="7517e-128">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="7517e-129">Empfängt Statusmeldungen von Prozessen, die in einem separaten Thread ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7517e-129">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7517e-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7517e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7517e-131">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="7517e-131">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




