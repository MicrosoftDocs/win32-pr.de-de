---
description: Zugreifen auf Dienst Objekteigenschaften
ms.assetid: 66d9802b-ad28-47a4-8151-9df7aff07d61
title: Zugreifen auf Dienst Objekteigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028ffc178f29f21aa60295b137b48c0fa2357a28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347152"
---
# <a name="accessing-service-object-properties"></a><span data-ttu-id="6890d-103">Zugreifen auf Dienst Objekteigenschaften</span><span class="sxs-lookup"><span data-stu-id="6890d-103">Accessing Service Object Properties</span></span>

<span data-ttu-id="6890d-104">Eine Anwendung kann Eigenschaften für ein einzelnes Objekt in einem Dienst, für mehrere Objekte, die durch Objekt Bezeichner oder für mehrere Objekte desselben Typs identifiziert werden, lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="6890d-104">An application can read and write properties for a single object on a service, for multiple objects identified by object identifiers, or for multiple objects of the same type.</span></span> <span data-ttu-id="6890d-105">Das Thema " [Abrufen von Objekteigenschaften](retrieving-content-object-properties.md) " beschreibt das Lesen von Eigenschaften für ein einzelnes Objekt in einem Dienst.</span><span class="sxs-lookup"><span data-stu-id="6890d-105">The [Retrieving Object Properties](retrieving-content-object-properties.md) topic describes reading properties for a single object on a service.</span></span> <span data-ttu-id="6890d-106">Das Thema [Schreiben von Objekteigenschaften](writing-content-object-properties.md) beschreibt das Schreiben von Eigenschaften für ein einzelnes Objekt in einem Dienst.</span><span class="sxs-lookup"><span data-stu-id="6890d-106">The [Writing Object Properties](writing-content-object-properties.md) topic describes writing properties for a single object on a service.</span></span>

<span data-ttu-id="6890d-107">Weitere Informationen zum Abrufen von Eigenschaften für mehrere Objekte finden Sie im Abschnitt " [Erweiterte Aufgaben](advanced-tasks.md) ".</span><span class="sxs-lookup"><span data-stu-id="6890d-107">Refer to the [Advanced Tasks](advanced-tasks.md) section for a description of property retrieval for multiple objects.</span></span>

## <a name="when-to-use-service-property-definitions"></a><span data-ttu-id="6890d-108">Verwendungszwecke von Dienst Eigenschafts Definitionen</span><span class="sxs-lookup"><span data-stu-id="6890d-108">When to use Service Property Definitions</span></span>

<span data-ttu-id="6890d-109">Die WPD-API-Aufrufe zum Abrufen und Festlegen von Objekteigenschaften für einen Dienst sind identisch mit den Aufrufen zum Abrufen von Objekteigenschaften für ein Gerät (Vergleich "Abrufen von Eigenschaften für ein einzelnes Objekt").</span><span class="sxs-lookup"><span data-stu-id="6890d-109">The WPD API calls used for retrieving and setting object properties for a service are the same as the calls for retrieving object properties for a device (compare "Retrieving Properties for a Single Object" for an example).</span></span> <span data-ttu-id="6890d-110">Der Hauptunterschied besteht darin, dass ein anderer Satz von PropertyKeys verwendet wird, um Objekteigenschaften abzufragen.</span><span class="sxs-lookup"><span data-stu-id="6890d-110">The key difference is that a different set of PROPERTYKEYs are used to query object properties.</span></span> <span data-ttu-id="6890d-111">Für wpdserviceapisample werden Geräte Dienst-PropertyKeys verwendet (z. **b. pkey \_ Generika \_ Name**); für wpdapisample werden WPD PropertyKeys (z. b. **WPD- \_ Objekt \_ Name**) verwendet.</span><span class="sxs-lookup"><span data-stu-id="6890d-111">For the WpdServiceApiSample, device service PROPERTYKEYs are used (such as **PKEY\_GenericObj\_Name**); for the WpdApiSample, WPD PROPERTYKEYs are used (such as **WPD\_OBJECT\_NAME**).</span></span>

<span data-ttu-id="6890d-112">Die Eigenschafts Schlüssel für den Geräte Dienst sind in bridgedeviceservices. h (enthalten in jeder Dienst Header Datei) definiert und stellen den gemeinsamen Satz von PropertyKeys dar, die sowohl von Geräte Dienst Anwendungen als auch von der Firmware-Implementierung auf dem Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6890d-112">Device service PROPERTYKEYs are defined in BridgeDeviceServices.h (included by each service header file), and represent the common set of PROPERTYKEYS employed by both device services applications and the firmware implementation on the device.</span></span> <span data-ttu-id="6890d-113">Dies ermöglicht einen konsistenten Satz von Definitionen im gesamten Geräte Stapel mit minimaler Übersetzung, gruppiert PropertyKeys auf der Grundlage des Diensts und ermöglicht das einfache Definieren neuer Dienste, ohne das WPD-Schema aktualisieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="6890d-113">This allows a consistent set of definitions throughout the device stack with minimal translation, groups PROPERTYKEYs based on the service, and enables new services to be more easily defined without having to update the WPD schema.</span></span>

<span data-ttu-id="6890d-114">Der verwendete Satz von PropertyKeys hängt von den Anforderungen der Anwendung ab:</span><span class="sxs-lookup"><span data-stu-id="6890d-114">The set of PROPERTYKEYs used will depend on your application's needs:</span></span>

-   <span data-ttu-id="6890d-115">Wenn Ihre Anwendung mit dem Gerät durch Aufrufen von [**iportabledevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)kommuniziert, verwenden Sie die in portabledevice. h definierten PropertyKeys.</span><span class="sxs-lookup"><span data-stu-id="6890d-115">If your application is communicating with the device by calling [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), use the PROPERTYKEYs defined in PortableDevice.h.</span></span> <span data-ttu-id="6890d-116">Ein Beispiel für eine solche Anwendung ist wpdapisample.</span><span class="sxs-lookup"><span data-stu-id="6890d-116">An example of such an application is the WpdApiSample.</span></span>
-   <span data-ttu-id="6890d-117">Wenn Ihre Anwendung mit den Geräte Diensten kommuniziert, indem Sie [**iportabledeviceservice:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)aufrufen, verwenden Sie die in bridgedeviceservices. h definierten PropertyKeys.</span><span class="sxs-lookup"><span data-stu-id="6890d-117">If your application is communicating with device services by calling [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), use the PROPERTYKEYS defined in BridgeDeviceServices.h.</span></span> <span data-ttu-id="6890d-118">Ein Beispiel für eine solche Anwendung ist wpdservicesapisample.</span><span class="sxs-lookup"><span data-stu-id="6890d-118">An example of such an application is the WpdServicesApiSample.</span></span>
-   <span data-ttu-id="6890d-119">Wenn Sie eine komplexe Anwendung schreiben, die eine Hybrid Geräte Dienste und ein Gerät unterstützen muss (Dies bedeutet, dass Ihre Anwendung beide **iportabledevice** -Befehle aufruft: Open und **iportabledeviceservice:: Open**) Sie müssen die WPD PropertyKeys verwenden, wenn Sie iportabledevice und seine abgeleiteten Schnittstellen und den Geräte Dienst PropertyKeys verwenden, wenn Sie [iportabledeviceservice](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) und seine abgeleiteten Schnittstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="6890d-119">If you are writing a complex application that needs to support a hybrid of both device services and the device (this means your application calls both **IPortableDevice::Open** and **IPortableDeviceService::Open**), you will need to use the WPD PROPERTYKEYs when using IPortableDevice and its derived interfaces, and device service PROPERTYKEYs when using [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) and its derived interfaces.</span></span>

<span data-ttu-id="6890d-120">Die meisten WPD-Anwendungen sollten in die erste oder zweite Kategorie fallen.</span><span class="sxs-lookup"><span data-stu-id="6890d-120">Most WPD applications should fall into the first or second category.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6890d-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6890d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6890d-122">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="6890d-122">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="6890d-123">**Iportabledeviceproperties**</span><span class="sxs-lookup"><span data-stu-id="6890d-123">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="6890d-124">Abrufen von Objekteigenschaften</span><span class="sxs-lookup"><span data-stu-id="6890d-124">Retrieving Object Properties</span></span>](retrieving-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="6890d-125">Schreiben von Objekteigenschaften</span><span class="sxs-lookup"><span data-stu-id="6890d-125">Writing Object Properties</span></span>](writing-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="6890d-126">Wpdservicesapisample</span><span class="sxs-lookup"><span data-stu-id="6890d-126">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



