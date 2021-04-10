---
description: Header Dateien und System Komponenten
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: Header Dateien und System Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4b93c63e7d32944dfdf2bf6872bd3a3153e4a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127440"
---
# <a name="header-files-and-system-components"></a><span data-ttu-id="a6825-103">Header Dateien und System Komponenten</span><span class="sxs-lookup"><span data-stu-id="a6825-103">Header Files and System Components</span></span>

<span data-ttu-id="a6825-104">In der folgenden Tabelle werden die Header Dateien aufgelistet, die die Schnittstellendefinitionen für die vier kernaudiokomponenten enthalten.</span><span class="sxs-lookup"><span data-stu-id="a6825-104">The following table lists the header files that contain the interface definitions for the four Core Audio components.</span></span>



|                                              |                              |
|----------------------------------------------|------------------------------|
| <span data-ttu-id="a6825-105">Kernaudiokomponente</span><span class="sxs-lookup"><span data-stu-id="a6825-105">Core Audio component</span></span>                         | <span data-ttu-id="a6825-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a6825-106">Header file</span></span>                  |
| [<span data-ttu-id="a6825-107">Mmdevice-API</span><span class="sxs-lookup"><span data-stu-id="a6825-107">MMDevice API</span></span>](mmdevice-api.md)             | <span data-ttu-id="a6825-108">Mmdeviceapi. h</span><span class="sxs-lookup"><span data-stu-id="a6825-108">Mmdeviceapi.h</span></span>                |
| [<span data-ttu-id="a6825-109">WASAPI</span><span class="sxs-lookup"><span data-stu-id="a6825-109">WASAPI</span></span>](wasapi.md)                         | <span data-ttu-id="a6825-110">AudioClient. h, audiopolicy. h</span><span class="sxs-lookup"><span data-stu-id="a6825-110">Audioclient.h, Audiopolicy.h</span></span> |
| [<span data-ttu-id="a6825-111">Debug-opology-API</span><span class="sxs-lookup"><span data-stu-id="a6825-111">DeviceTopology API</span></span>](devicetopology-api.md) | <span data-ttu-id="a6825-112">"Tvicetopology. h"</span><span class="sxs-lookup"><span data-stu-id="a6825-112">Devicetopology.h</span></span>             |
| [<span data-ttu-id="a6825-113">Endpointvolume-API</span><span class="sxs-lookup"><span data-stu-id="a6825-113">EndpointVolume API</span></span>](endpointvolume-api.md) | <span data-ttu-id="a6825-114">Endpointvolume. h</span><span class="sxs-lookup"><span data-stu-id="a6825-114">Endpointvolume.h</span></span>             |



 

<span data-ttu-id="a6825-115">Eine andere Header Datei, audiosessiontypes. h, definiert Konstanten, die von WASAPI verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6825-115">Another header file, Audiosessiontypes.h, defines constants that are used by WASAPI.</span></span> <span data-ttu-id="a6825-116">Diese Header Dateien befinden sich im Verzeichnis% MSSDK% \\ include, wobei% MSSDK% das Stammverzeichnis der Windows SDK Installation auf Ihrem Computer ist.</span><span class="sxs-lookup"><span data-stu-id="a6825-116">These header files are located in the directory %MSSdk%\\include, where %MSSdk% is the root directory of the Windows SDK installation on your computer.</span></span>

<span data-ttu-id="a6825-117">Jede API in der vorangehenden Tabelle besteht aus einem Satz verwandter com-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="a6825-117">Each API in the preceding table consists of a set of related COM interfaces.</span></span> <span data-ttu-id="a6825-118">Da einige Aspekte des audiostreamings von geringer Latenz und präziser Synchronisierung abhängen, verwenden die Implementierungen der APIs "mmdevice", "WASAPI", "debuetopology" und "endpointvolume" nicht das Microsoft .NET Framework oder die verwaltete Ausführungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="a6825-118">Because some aspects of audio streaming depend on low latency and precise synchronization, the implementations of the MMDevice, WASAPI, DeviceTopology, and EndpointVolume APIs do not use the Microsoft .NET Framework or managed-execution environment.</span></span>

<span data-ttu-id="a6825-119">Die Kern-audioapis werden in den Systemkomponenten des Benutzermodus implementiert Audioses.dll und Mmdevapi.dll.</span><span class="sxs-lookup"><span data-stu-id="a6825-119">The Core Audio APIs are implemented in the user-mode system components Audioses.dll and Mmdevapi.dll.</span></span> <span data-ttu-id="a6825-120">Client Anwendungen greifen nicht direkt auf die Einstiegspunkte in diesen DLLs zu.</span><span class="sxs-lookup"><span data-stu-id="a6825-120">Client applications do not access the entry points in these DLLs directly.</span></span> <span data-ttu-id="a6825-121">Stattdessen rufen Clients die Funktion **cokreateinstance** oder **cokreateinstanceex** auf, um die [**immdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle des mmdeviceenumerator-Klassen Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a6825-121">Instead, clients call the **CoCreateInstance** or **CoCreateInstanceEx** function to obtain the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface of the MMDeviceEnumerator class object.</span></span> <span data-ttu-id="a6825-122">Dieses Objekt listet die [audioendpunktgeräte](audio-endpoint-devices.md) im System auf.</span><span class="sxs-lookup"><span data-stu-id="a6825-122">This object enumerates the [audio endpoint devices](audio-endpoint-devices.md) in the system.</span></span> <span data-ttu-id="a6825-123">Die **immdeviceenumerator** -Schnittstelle ist Teil der mmdevice-API.</span><span class="sxs-lookup"><span data-stu-id="a6825-123">The **IMMDeviceEnumerator** interface is part of the MMDevice API.</span></span> <span data-ttu-id="a6825-124">Über diese Schnittstelle können Clients die anderen Schnittstellen in der mmdevice-API (einschließlich der [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle) direkt oder indirekt abrufen.</span><span class="sxs-lookup"><span data-stu-id="a6825-124">From this interface, clients can directly or indirectly obtain the other interfaces in the MMDevice API, including the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface.</span></span> <span data-ttu-id="a6825-125">**Immdevice** stellt ein bestimmtes audioendpunktgerät dar.</span><span class="sxs-lookup"><span data-stu-id="a6825-125">**IMMDevice** represents a particular audio endpoint device.</span></span> <span data-ttu-id="a6825-126">Über **immdevice** können Clients die gerätespezifischen Schnittstellen direkt oder indirekt in der WASAPI, der devicetopology-API und der endpointvolume-API abrufen.</span><span class="sxs-lookup"><span data-stu-id="a6825-126">Through **IMMDevice**, clients can directly or indirectly obtain the device-specific interfaces in WASAPI, the DeviceTopology API, and the EndpointVolume API.</span></span> <span data-ttu-id="a6825-127">Weitere Informationen zu **cokreateinstance** und **cokreateinstanceex** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a6825-127">For more information about **CoCreateInstance** and **CoCreateInstanceEx**, see the Windows SDK documentation.</span></span> <span data-ttu-id="a6825-128">Weitere Informationen zum Zugreifen auf die Schnittstellen in den kernaudioapis finden Sie unter Auflisten von [Audiogeräten](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="a6825-128">For more information about accessing the interfaces in the Core Audio APIs, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6825-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6825-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6825-130">Informationen zu den Windows Core-audioapis</span><span class="sxs-lookup"><span data-stu-id="a6825-130">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



