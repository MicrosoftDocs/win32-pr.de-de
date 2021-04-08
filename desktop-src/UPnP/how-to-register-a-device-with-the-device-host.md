---
title: Registrieren eines Geräts beim Geräte Host
description: Sie können entweder ein Betriebs Endes Gerät oder ein Gerät registrieren, das nicht ausgeführt wird.
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3be1561d82741ce33e7eb05e63b015d5cb38f52
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037001"
---
# <a name="how-to-register-a-device-with-the-device-host"></a><span data-ttu-id="982b2-103">Registrieren eines Geräts beim Geräte Host</span><span class="sxs-lookup"><span data-stu-id="982b2-103">How to Register a Device with the Device Host</span></span>

<span data-ttu-id="982b2-104">Sie können entweder ein Betriebs Endes Gerät oder ein Gerät registrieren, das nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="982b2-104">You can register either a running device or a non-running device.</span></span>

## <a name="registering-a-running-device"></a><span data-ttu-id="982b2-105">Registrieren eines laufenden Geräts</span><span class="sxs-lookup"><span data-stu-id="982b2-105">Registering a Running Device</span></span>

<span data-ttu-id="982b2-106">Geräte werden mithilfe der [**iupnpregistrinar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) -Schnittstelle registriert.</span><span class="sxs-lookup"><span data-stu-id="982b2-106">Devices are registered using the [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) interface.</span></span> <span data-ttu-id="982b2-107">Nur Administratoren sind berechtigt, die Ausführung von Geräten zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="982b2-107">Only administrators are allowed to register running devices.</span></span> <span data-ttu-id="982b2-108">Um ein Gerät zu registrieren, das ein Geräte Steuerungsobjekt enthält, muss eine Anwendung [**iupnpregistranar:: registerrunningdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)aufrufen und dabei Folgendes übergeben:</span><span class="sxs-lookup"><span data-stu-id="982b2-108">To register a device that has a running device control object, an application must invoke [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), passing the following:</span></span>

-   <span data-ttu-id="982b2-109">Der Text der Beschreibung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="982b2-109">The text of the device's description.</span></span>
-   <span data-ttu-id="982b2-110">Ein **IUnknown** -Zeiger auf das Geräte Steuerungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="982b2-110">An **IUnknown** pointer to the device control object.</span></span>
-   <span data-ttu-id="982b2-111">Eine Initialisierungs Zeichenfolge, die an die [**iupnpdevicecontrol:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) -Methode des Geräte Steuerungs Objekts übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="982b2-111">An initialization string that is passed to the device control object's [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method.</span></span>
-   <span data-ttu-id="982b2-112">Der Speicherort des Ressourcen Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="982b2-112">The location of the resource directory.</span></span>
-   <span data-ttu-id="982b2-113">Die Lebensdauer des Geräts.</span><span class="sxs-lookup"><span data-stu-id="982b2-113">The lifetime of the device.</span></span>
-   <span data-ttu-id="982b2-114">Der Geräte-ID-Parameter (ein out-Parameter), der der Rückgabewert dieses Aufrufes ist. Ein Zeiger auf die Geräte-ID wird in C++ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="982b2-114">The Device ID parameter (an OUT parameter), which is the return value of this call; a pointer to the Device ID is returned in C++.</span></span>

## <a name="registering-a-non-running-device"></a><span data-ttu-id="982b2-115">Registrieren eines Geräts, das nicht ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="982b2-115">Registering a Non-Running Device</span></span>

<span data-ttu-id="982b2-116">Standardmäßig sind nur Administratoren und interaktive Benutzer berechtigt, nicht laufende Geräte zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="982b2-116">By default, only administrators and interactive users are allowed to register non-running devices.</span></span> <span data-ttu-id="982b2-117">Zum Registrieren eines Geräts bei einem Geräte Steuerungsobjekt, das nicht ausgeführt wird, verwendet die Anwendung die [**iupnpregistrinster:: registerdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) -Methode.</span><span class="sxs-lookup"><span data-stu-id="982b2-117">To register a device with a device control object that is not running, the application uses the [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) method.</span></span>

<span data-ttu-id="982b2-118">Zum programmgesteuerten Registrieren eines Geräts bei einem Geräte Steuerungsobjekt, das nicht ausgeführt wird, muss die Anwendung [**iupnpregistranar:: registerdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) aufrufen und die folgenden Parameter übergeben:</span><span class="sxs-lookup"><span data-stu-id="982b2-118">To programmatically register a device with a non-running device control object, the application must invoke [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) and pass it the following parameters:</span></span>

-   <span data-ttu-id="982b2-119">Der Text der Beschreibung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="982b2-119">The text of the device's description.</span></span>
-   <span data-ttu-id="982b2-120">Die ProgID des Geräte Steuerungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="982b2-120">The ProgID of the device control object.</span></span>
-   <span data-ttu-id="982b2-121">Eine Initialisierungs Zeichenfolge, die an die [**iupnpdevicecontrol:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) -Methode des Geräte Steuerungs Objekts übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="982b2-121">An initialization string that is passed to the device control object's [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method.</span></span>
-   <span data-ttu-id="982b2-122">Eine Container-ID.</span><span class="sxs-lookup"><span data-stu-id="982b2-122">A container ID.</span></span>
-   <span data-ttu-id="982b2-123">Der Speicherort des Ressourcen Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="982b2-123">The location of the resource directory.</span></span>
-   <span data-ttu-id="982b2-124">Die Lebensdauer des Geräts.</span><span class="sxs-lookup"><span data-stu-id="982b2-124">The lifetime of the device.</span></span>
-   <span data-ttu-id="982b2-125">Der Geräte-ID-Parameter (ein out-Parameter), der der Rückgabewert dieses Aufrufes ist. Ein Zeiger auf die Geräte-ID wird in C++ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="982b2-125">The Device ID parameter (an OUT parameter), which is the return value of this call; a pointer to the Device ID is returned in C++.</span></span>

<span data-ttu-id="982b2-126">Die Registrierungen nicht laufender Geräte können so konfiguriert werden, dass Sie über Systemstarts hinweg beibehalten werden (die Geräte werden während der Herunterfahr Phase nicht veröffentlicht).</span><span class="sxs-lookup"><span data-stu-id="982b2-126">The registrations of non-running devices can be configured to persist across system boots (the devices are unpublished during the shutdown phase).</span></span> <span data-ttu-id="982b2-127">Wenn Sie auf diese Weise konfiguriert werden, werden Geräte bei jedem Neustart des Computers veröffentlicht und angekündigt.</span><span class="sxs-lookup"><span data-stu-id="982b2-127">Therefore, if they are configured this way, devices are published and announced every time the computer is booted.</span></span>

 

 




