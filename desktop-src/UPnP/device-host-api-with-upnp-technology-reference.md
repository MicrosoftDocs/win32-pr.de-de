---
title: Referenz zur Geräte Host-API
description: Die folgenden Schnittstellen sind Teil der Geräte Host-API mit UPnP-Technologie. Der Geräte Host mit der UPnP-Technologie unterstützt Microsoft Visual Basic und C++.
ms.assetid: 48e20a09-7e78-4b8d-aa16-78751b6fb586
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62f42b43efcc1d51eb5e5581770260238640469
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388557"
---
# <a name="device-host-api-reference"></a><span data-ttu-id="0dff3-104">Referenz zur Geräte Host-API</span><span class="sxs-lookup"><span data-stu-id="0dff3-104">Device Host API Reference</span></span>

<span data-ttu-id="0dff3-105">Die folgenden Schnittstellen sind Teil der Geräte Host-API mit UPnP-Technologie.</span><span class="sxs-lookup"><span data-stu-id="0dff3-105">The following interfaces are part of the Device Host API with UPnP technology.</span></span> <span data-ttu-id="0dff3-106">Der Geräte Host mit der UPnP-Technologie unterstützt Microsoft Visual Basic und C++.</span><span class="sxs-lookup"><span data-stu-id="0dff3-106">The Device Host with UPnP technology supports Microsoft Visual Basic and C++.</span></span>

<span data-ttu-id="0dff3-107">Diese API bietet keine Unterstützung für Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="0dff3-107">This API does not provide support for Microsoft Visual Basic Scripting Edition (VBScript).</span></span>



| <span data-ttu-id="0dff3-108">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0dff3-108">Interface</span></span>                                                  | <span data-ttu-id="0dff3-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0dff3-109">Description</span></span>                                                                                         |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0dff3-110">**Iupnpde vicecontrol**</span><span class="sxs-lookup"><span data-stu-id="0dff3-110">**IUPnPDeviceControl**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol)           | <span data-ttu-id="0dff3-111">Wird vom Geräte Host zum Verwalten von Geräten und zugehörigen Diensten verwendet.</span><span class="sxs-lookup"><span data-stu-id="0dff3-111">Used by the device host to manage devices and related services.</span></span>                                     |
| [<span data-ttu-id="0dff3-112">**Iupnpdeviceprovider**</span><span class="sxs-lookup"><span data-stu-id="0dff3-112">**IUPnPDeviceProvider**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider)         | <span data-ttu-id="0dff3-113">Wird vom Geräte Host verwendet, um Geräte Anbieter zu starten und zu unterbinden.</span><span class="sxs-lookup"><span data-stu-id="0dff3-113">Used by the device host to start and stop device providers.</span></span>                                         |
| [<span data-ttu-id="0dff3-114">**Iupnpeer-Sink**</span><span class="sxs-lookup"><span data-stu-id="0dff3-114">**IUPnPEventSink**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink)                   | <span data-ttu-id="0dff3-115">Wird von Geräten verwendet, um Ereignis Benachrichtigungen an den Geräte Host zu senden.</span><span class="sxs-lookup"><span data-stu-id="0dff3-115">Used by devices to send event notifications to the device host.</span></span>                                     |
| [<span data-ttu-id="0dff3-116">**Iupnpeer-Source**</span><span class="sxs-lookup"><span data-stu-id="0dff3-116">**IUPnPEventSource**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource)               | <span data-ttu-id="0dff3-117">Wird vom Geräte Host zum abonnieren oder kündigen von Ereignissen verwendet, die vom gehosteten Dienst bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0dff3-117">Used by the device host to subscribe or unsubscribe to events provided by the hosted service.</span></span>       |
| [<span data-ttu-id="0dff3-118">**Iupnpregistrinar**</span><span class="sxs-lookup"><span data-stu-id="0dff3-118">**IUPnPRegistrar**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar)                   | <span data-ttu-id="0dff3-119">Wird von Geräten verwendet, um sich beim Geräte Host zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="0dff3-119">Used by devices to register with the device host.</span></span>                                                   |
| [<span data-ttu-id="0dff3-120">**Iupnpremoteendpointinfo**</span><span class="sxs-lookup"><span data-stu-id="0dff3-120">**IUPnPRemoteEndpointInfo**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) | <span data-ttu-id="0dff3-121">Wird von Geräten verwendet, um Informationen über einen Anforderer (d. h. einen Steuerungspunkt) und die Anforderung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0dff3-121">Used by devices to obtain information about a requester (that is, a control point) and the request.</span></span> |
| [<span data-ttu-id="0dff3-122">**Iupnpreregistrinar**</span><span class="sxs-lookup"><span data-stu-id="0dff3-122">**IUPnPReregistrar**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)               | <span data-ttu-id="0dff3-123">Wird von Geräten zum erneuten Registrieren beim Geräte Host verwendet.</span><span class="sxs-lookup"><span data-stu-id="0dff3-123">Used by devices to re-register with the device host.</span></span>                                                |



 

 

 




