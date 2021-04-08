---
description: Informationen über die mmdevice-API
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: Informationen über die mmdevice-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82843bbecf004d0931575d73ec2459c3e72a3cf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748777"
---
# <a name="about-mmdevice-api"></a><span data-ttu-id="141f5-103">Informationen über die mmdevice-API</span><span class="sxs-lookup"><span data-stu-id="141f5-103">About MMDevice API</span></span>

<span data-ttu-id="141f5-104">Mit der API von Windows Multimedia Device (mmdevice) können audioclients [audioendpunktgeräte](audio-endpoint-devices.md)ermitteln, deren Funktionen ermitteln und Treiber Instanzen für diese Geräte erstellen.</span><span class="sxs-lookup"><span data-stu-id="141f5-104">The Windows Multimedia Device (MMDevice) API enables audio clients to discover [audio endpoint devices](audio-endpoint-devices.md), determine their capabilities, and create driver instances for those devices.</span></span>

<span data-ttu-id="141f5-105">Die Header Datei "mmdeviceapi. h" definiert die Schnittstellen in der mmdevice-API.</span><span class="sxs-lookup"><span data-stu-id="141f5-105">Header file Mmdeviceapi.h defines the interfaces in the MMDevice API.</span></span>

<span data-ttu-id="141f5-106">Die mmdevice-API besteht aus mehreren Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="141f5-106">The MMDevice API consists of several interfaces.</span></span> <span data-ttu-id="141f5-107">Der erste ist die [**immdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="141f5-107">The first of these is the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="141f5-108">Für den Zugriff auf die Schnittstellen in der mmdevice-API erhält ein Client einen Verweis auf die **immdeviceenumerator** -Schnittstelle eines Device-Enumerator-Objekts, indem er die [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufruft, wie im folgenden Code Fragment gezeigt:</span><span class="sxs-lookup"><span data-stu-id="141f5-108">To access the interfaces in the MMDevice API, a client obtains a reference to the **IMMDeviceEnumerator** interface of a device-enumerator object by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, as shown in the following code fragment:</span></span>


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



<span data-ttu-id="141f5-109">Im vorangehenden Code Fragment sind CLSID \_ mmdeviceenumerator und IID \_ immdeviceenumerator die GUID-Werte, die dem **mmdeviceenumerator** -Klassenobjekt und der [**immdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle als Attribute angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="141f5-109">In the preceding code fragment, CLSID\_MMDeviceEnumerator and IID\_IMMDeviceEnumerator are the GUID values that are attached as attributes to the **MMDeviceEnumerator** class object and to the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="141f5-110">Der [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Befehl übergibt diese Werte als Verweis.</span><span class="sxs-lookup"><span data-stu-id="141f5-110">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) call passes these values by reference.</span></span> <span data-ttu-id="141f5-111">Variable `hr` ist vom Typ **HRESULT**, und Variable `pEnumerator` ist ein Zeiger auf die **immdeviceenumerator** -Schnittstelle eines Device-Enumerator-Objekts.</span><span class="sxs-lookup"><span data-stu-id="141f5-111">Variable `hr` is of type **HRESULT**, and variable `pEnumerator` is a pointer to the **IMMDeviceEnumerator** interface of a device-enumerator object.</span></span> <span data-ttu-id="141f5-112">**Immdeviceenumerator** stellt Methoden zum Auflisten von audioendpunktgeräten bereit.</span><span class="sxs-lookup"><span data-stu-id="141f5-112">**IMMDeviceEnumerator** provides methods for enumerating audio endpoint devices.</span></span> <span data-ttu-id="141f5-113">Weitere Informationen über den **\_ \_ uuidof** -Operator, die **cokreateinstance** -Funktion und die CLSCTX \_ *xxx* -Konstanten finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="141f5-113">For information about the **\_\_uuidof** operator, the **CoCreateInstance** function, and the CLSCTX\_*Xxx* constants, see the Windows SDK documentation.</span></span>

<span data-ttu-id="141f5-114">Über die [**immdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle kann der Client Verweise auf die anderen Schnittstellen in der mmdevice-API abrufen.</span><span class="sxs-lookup"><span data-stu-id="141f5-114">Through the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, the client can obtain references to the other interfaces in the MMDevice API.</span></span> <span data-ttu-id="141f5-115">Die mmdevice-API implementiert die folgenden Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="141f5-115">The MMDevice API implements the following interfaces.</span></span>



| <span data-ttu-id="141f5-116">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="141f5-116">Interface</span></span>                                          | <span data-ttu-id="141f5-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="141f5-117">Description</span></span>                                     |
|----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="141f5-118">**Immdevice**</span><span class="sxs-lookup"><span data-stu-id="141f5-118">**IMMDevice**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | <span data-ttu-id="141f5-119">Stellt ein Audiogerät dar.</span><span class="sxs-lookup"><span data-stu-id="141f5-119">Represents an audio device.</span></span>                     |
| [<span data-ttu-id="141f5-120">**Immde vicecollection**</span><span class="sxs-lookup"><span data-stu-id="141f5-120">**IMMDeviceCollection**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | <span data-ttu-id="141f5-121">Stellt eine Auflistung von Audiogeräten dar.</span><span class="sxs-lookup"><span data-stu-id="141f5-121">Represents a collection of audio devices.</span></span>       |
| [<span data-ttu-id="141f5-122">**Immdeviceenumerator**</span><span class="sxs-lookup"><span data-stu-id="141f5-122">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | <span data-ttu-id="141f5-123">Stellt Methoden zum Auflisten von Audiogeräten bereit.</span><span class="sxs-lookup"><span data-stu-id="141f5-123">Provides methods for enumerating audio devices.</span></span> |
| [<span data-ttu-id="141f5-124">**Immendpoint**</span><span class="sxs-lookup"><span data-stu-id="141f5-124">**IMMEndpoint**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | <span data-ttu-id="141f5-125">Stellt ein audioendpunktgerät dar.</span><span class="sxs-lookup"><span data-stu-id="141f5-125">Represents an audio endpoint device.</span></span>            |



 

<span data-ttu-id="141f5-126">Außerdem sollten Clients der mmdevice-API, die Benachrichtigungen über Statusänderungen in audioendpunktgeräten erfordern, die folgende Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="141f5-126">In addition, clients of the MMDevice API that require notification of status changes in audio endpoint devices should implement the following interface.</span></span>



| <span data-ttu-id="141f5-127">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="141f5-127">Interface</span></span>                                              | <span data-ttu-id="141f5-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="141f5-128">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="141f5-129">**Immnotificationclient**</span><span class="sxs-lookup"><span data-stu-id="141f5-129">**IMMNotificationClient**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | <span data-ttu-id="141f5-130">Stellt Benachrichtigungen bereit, wenn ein audioendpunktgerät hinzugefügt oder entfernt wird, wenn sich der Zustand oder die Eigenschaften eines Geräts ändern oder wenn die Standard Rolle, die einem Gerät zugewiesen ist, geändert wird.</span><span class="sxs-lookup"><span data-stu-id="141f5-130">Provides notifications when an audio endpoint device is added or removed, when the state or properties of a device change, or when there is a change in the default role assigned to a device.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="141f5-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="141f5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="141f5-132">Audioendpunktgeräte</span><span class="sxs-lookup"><span data-stu-id="141f5-132">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> <dt>

[<span data-ttu-id="141f5-133">**Programmierverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="141f5-133">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 
