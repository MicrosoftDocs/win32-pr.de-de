---
description: Headerdateien und Systemkomponenten
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: Headerdateien und Systemkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a47125853b51a71f2f05dacf4534ce33cfedec
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424290"
---
# <a name="header-files-and-system-components"></a><span data-ttu-id="06ed9-103">Headerdateien und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="06ed9-103">Header Files and System Components</span></span>

<span data-ttu-id="06ed9-104">In der folgenden Tabelle sind die Headerdateien aufgeführt, die die Schnittstellendefinitionen für die vier Core Audio-Komponenten enthalten.</span><span class="sxs-lookup"><span data-stu-id="06ed9-104">The following table lists the header files that contain the interface definitions for the four Core Audio components.</span></span>



| <span data-ttu-id="06ed9-105">Kernaudiokomponente</span><span class="sxs-lookup"><span data-stu-id="06ed9-105">Core Audio component</span></span>                         | <span data-ttu-id="06ed9-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="06ed9-106">Header file</span></span>                  |
|----------------------------------------------|------------------------------|
| [<span data-ttu-id="06ed9-107">MMDevice-API</span><span class="sxs-lookup"><span data-stu-id="06ed9-107">MMDevice API</span></span>](mmdevice-api.md)             | <span data-ttu-id="06ed9-108">Mmdeviceapi.h</span><span class="sxs-lookup"><span data-stu-id="06ed9-108">Mmdeviceapi.h</span></span>                |
| [<span data-ttu-id="06ed9-109">WASAPI</span><span class="sxs-lookup"><span data-stu-id="06ed9-109">WASAPI</span></span>](wasapi.md)                         | <span data-ttu-id="06ed9-110">Audioclient.h, Audiopolicy.h</span><span class="sxs-lookup"><span data-stu-id="06ed9-110">Audioclient.h, Audiopolicy.h</span></span> |
| [<span data-ttu-id="06ed9-111">DeviceTopology-API</span><span class="sxs-lookup"><span data-stu-id="06ed9-111">DeviceTopology API</span></span>](devicetopology-api.md) | <span data-ttu-id="06ed9-112">Devicetopology.h</span><span class="sxs-lookup"><span data-stu-id="06ed9-112">Devicetopology.h</span></span>             |
| [<span data-ttu-id="06ed9-113">EndpointVolume-API</span><span class="sxs-lookup"><span data-stu-id="06ed9-113">EndpointVolume API</span></span>](endpointvolume-api.md) | <span data-ttu-id="06ed9-114">Endpointvolume.h</span><span class="sxs-lookup"><span data-stu-id="06ed9-114">Endpointvolume.h</span></span>             |



 

<span data-ttu-id="06ed9-115">Eine andere Headerdatei, Audiosessiontypes.h, definiert Konstanten, die von WASAPI verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06ed9-115">Another header file, Audiosessiontypes.h, defines constants that are used by WASAPI.</span></span> <span data-ttu-id="06ed9-116">Diese Headerdateien befinden sich im Verzeichnis %MSSdk% include, wobei %MSSdk% das Stammverzeichnis der Windows SDK auf Ihrem Computer \\ ist.</span><span class="sxs-lookup"><span data-stu-id="06ed9-116">These header files are located in the directory %MSSdk%\\include, where %MSSdk% is the root directory of the Windows SDK installation on your computer.</span></span>

<span data-ttu-id="06ed9-117">Jede API in der obigen Tabelle besteht aus einem Satz verwandter COM-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="06ed9-117">Each API in the preceding table consists of a set of related COM interfaces.</span></span> <span data-ttu-id="06ed9-118">Da einige Aspekte des Audiostreamings von geringer Latenz und präziser Synchronisierung abhängen, verwenden die Implementierungen der APIs MMDevice, WASAPI, DeviceTopology und EndpointVolume nicht das Microsoft .NET Framework oder die Verwaltete Ausführungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="06ed9-118">Because some aspects of audio streaming depend on low latency and precise synchronization, the implementations of the MMDevice, WASAPI, DeviceTopology, and EndpointVolume APIs do not use the Microsoft .NET Framework or managed-execution environment.</span></span>

<span data-ttu-id="06ed9-119">Die Core Audio-APIs werden in den Systemkomponenten des Benutzermodus Audioses.dll und Mmdevapi.dll.</span><span class="sxs-lookup"><span data-stu-id="06ed9-119">The Core Audio APIs are implemented in the user-mode system components Audioses.dll and Mmdevapi.dll.</span></span> <span data-ttu-id="06ed9-120">Clientanwendungen greifen nicht direkt auf die Einstiegspunkte in diesen DLLs zu.</span><span class="sxs-lookup"><span data-stu-id="06ed9-120">Client applications do not access the entry points in these DLLs directly.</span></span> <span data-ttu-id="06ed9-121">Stattdessen rufen Clients die **Funktion CoCreateInstance** oder **CoCreateInstanceEx** auf, um die [**IMMDeviceEnumerator-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) des MMDeviceEnumerator-Klassenobjekts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="06ed9-121">Instead, clients call the **CoCreateInstance** or **CoCreateInstanceEx** function to obtain the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface of the MMDeviceEnumerator class object.</span></span> <span data-ttu-id="06ed9-122">Dieses Objekt listet die [Audioendpunktgeräte](audio-endpoint-devices.md) im System auf.</span><span class="sxs-lookup"><span data-stu-id="06ed9-122">This object enumerates the [audio endpoint devices](audio-endpoint-devices.md) in the system.</span></span> <span data-ttu-id="06ed9-123">Die **IMMDeviceEnumerator-Schnittstelle** ist Teil der MMDevice-API.</span><span class="sxs-lookup"><span data-stu-id="06ed9-123">The **IMMDeviceEnumerator** interface is part of the MMDevice API.</span></span> <span data-ttu-id="06ed9-124">Über diese Schnittstelle können Clients direkt oder indirekt die anderen Schnittstellen in der MMDevice-API abrufen, einschließlich der [**IMMDevice-Schnittstelle.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)</span><span class="sxs-lookup"><span data-stu-id="06ed9-124">From this interface, clients can directly or indirectly obtain the other interfaces in the MMDevice API, including the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface.</span></span> <span data-ttu-id="06ed9-125">**IMMDevice** stellt ein bestimmtes Audioendpunktgerät dar.</span><span class="sxs-lookup"><span data-stu-id="06ed9-125">**IMMDevice** represents a particular audio endpoint device.</span></span> <span data-ttu-id="06ed9-126">Über **IMMDevice** können Clients die gerätespezifischen Schnittstellen in WASAPI, der DeviceTopology-API und der EndpointVolume-API direkt oder indirekt abrufen.</span><span class="sxs-lookup"><span data-stu-id="06ed9-126">Through **IMMDevice**, clients can directly or indirectly obtain the device-specific interfaces in WASAPI, the DeviceTopology API, and the EndpointVolume API.</span></span> <span data-ttu-id="06ed9-127">Weitere Informationen zu **CoCreateInstance** und **CoCreateInstanceEx** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="06ed9-127">For more information about **CoCreateInstance** and **CoCreateInstanceEx**, see the Windows SDK documentation.</span></span> <span data-ttu-id="06ed9-128">Weitere Informationen zum Zugriff auf die Schnittstellen in den Core Audio-APIs finden Sie unter [Aufzählen von Audiogeräten.](enumerating-audio-devices.md)</span><span class="sxs-lookup"><span data-stu-id="06ed9-128">For more information about accessing the interfaces in the Core Audio APIs, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06ed9-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06ed9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06ed9-130">Informationen zu Windows Core-Audio-APIs</span><span class="sxs-lookup"><span data-stu-id="06ed9-130">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



