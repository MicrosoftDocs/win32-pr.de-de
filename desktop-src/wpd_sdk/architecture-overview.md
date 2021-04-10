---
description: Übersicht über die Architektur
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: Übersicht über die Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f911a14e60465efc8f8f8d798b7ddf527bf4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868271"
---
# <a name="architecture-overview"></a><span data-ttu-id="1c0a3-103">Übersicht über die Architektur</span><span class="sxs-lookup"><span data-stu-id="1c0a3-103">Architecture Overview</span></span>

<span data-ttu-id="1c0a3-104">Die WPD-Architektur kann in drei Prozesse unterteilt werden.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-104">The WPD architecture can be divided into three processes.</span></span> <span data-ttu-id="1c0a3-105">Innerhalb dieser Prozesse sind die drei primären Komponenten von WPD: die API, das Serialisierungsprogramm und der Treiber.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-105">Within these processes are the three primary components of WPD: the API, the serializer, and the driver.</span></span> <span data-ttu-id="1c0a3-106">In der folgenden Abbildung werden die Prozesse und Komponenten dargestellt, die die WPD-Architektur bilden.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-106">The following illustration depicts the processes and components that constitute the WPD architecture.</span></span>

![Abbildung der API-, Serialisierungsprogramme-und Treiber Komponenten von WPD](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a><span data-ttu-id="1c0a3-108">Die WPD-Anwendungsprogrammierschnittstelle</span><span class="sxs-lookup"><span data-stu-id="1c0a3-108">The WPD Application Programming Interface</span></span>

<span data-ttu-id="1c0a3-109">Die WPD-API wird als in-proc-com-Server implementiert.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-109">The WPD API is implemented as an in-proc COM server.</span></span> <span data-ttu-id="1c0a3-110">Die API verwendet standardmäßige Microsoft-Win32-APIs, um mit dem entsprechenden WPD-Treiber zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-110">The API uses standard Microsoft Win32 APIs to communicate with the appropriate WPD driver.</span></span> <span data-ttu-id="1c0a3-111">Eine Komponente, die als WPD-Serialisierungsprogramm bezeichnet wird, wird sowohl von API-Objekten als auch vom Treiber verwendet, um Parameter in oder aus Windows Driver Foundation (WDF)-, User-Mode Driver Framework</span><span class="sxs-lookup"><span data-stu-id="1c0a3-111">A component called the WPD serializer is used by both API objects and the driver to pack or unpack parameters to or from Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF) buffers.</span></span>

## <a name="the-wpd-serializer"></a><span data-ttu-id="1c0a3-112">Der WPD-Serialisierer</span><span class="sxs-lookup"><span data-stu-id="1c0a3-112">The WPD Serializer</span></span>

<span data-ttu-id="1c0a3-113">Das WPD-Serialisierungsprogramm wird als in-proc-com-Server implementiert.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-113">The WPD serializer is implemented as an in-proc COM server.</span></span> <span data-ttu-id="1c0a3-114">Die WPD-API verwendet das Serialisierungsprogramm, um Befehle und Parameter in Nachrichten Puffer zu packen, die an den Treiber gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-114">The WPD API uses the serializer to pack commands and parameters into message buffers that are sent to the driver.</span></span> <span data-ttu-id="1c0a3-115">Der Treiber verwendet das Serialisierungsprogramm, um diese Nachrichten Puffer für die Verarbeitung zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-115">The driver uses the serializer to unpack these message buffers for processing.</span></span> <span data-ttu-id="1c0a3-116">Der Treiber verwendet auch das Serialisierungsprogramm zum Packen von Daten und Parametern in Antwort Puffer, die an die WPD-API zurückgegeben werden, und die WPD-API verwendet das Serialisierungsprogramm, um diese Antwort Puffer zum zurückkehren zu Aufrufern zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-116">The driver also uses the serializer to pack data and parameters into response buffers that are returned to the WPD API, and the WPD API uses the serializer to unpack these response buffers to return to callers.</span></span>

## <a name="wpd-driver"></a><span data-ttu-id="1c0a3-117">WPD-Treiber</span><span class="sxs-lookup"><span data-stu-id="1c0a3-117">WPD Driver</span></span>

<span data-ttu-id="1c0a3-118">Der WPD-Treiber ist als Standardtreiber für Windows Driver Foundation (WDF), User Mode Driver Framework (UMDF) implementiert.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-118">The WPD driver is implemented as a standard Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF) driver.</span></span> <span data-ttu-id="1c0a3-119">WPD-Treiber werden von der-Funktion in einem separaten Prozess gehostet, der als Treiber Host bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-119">WPD drivers are hosted by UMDF in a separate process called the Driver Host.</span></span>

<span data-ttu-id="1c0a3-120">Der Treiber empfängt Nachrichten vom Umschlag "um DF" (Dies wird im Diagramm nicht angezeigt, da die Puffer Informationen für den Treiber nicht wichtig sind.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-120">The driver receives messages from the UMDF reflector (this is not shown in the diagram, since how the buffers are received is not important to the driver.</span></span> <span data-ttu-id="1c0a3-121">Weitere Informationen finden Sie in der Umschlag Dokumentation.)</span><span class="sxs-lookup"><span data-stu-id="1c0a3-121">See UMDF documentation for more information).</span></span> <span data-ttu-id="1c0a3-122">Der Treiber implementiert einen WPD-spezifischen e/a-Steuerungs Code (iocl)-Handler, um von der WPD-API empfangene WPD-Nachrichten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-122">The driver implements a WPD-specific I/O Control code (IOCL) handler to process WPD messages received by the WPD API.</span></span> <span data-ttu-id="1c0a3-123">Der Treiber verwendet das WPD-Serialisierungsprogramm, um Befehle und Parameter aus diesen Nachrichten Puffern zu entpacken und die Antwort in den Rückgabe Puffer zu packen.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-123">The driver uses the WPD serializer to unpack commands and parameters from these message buffers, and to pack the response into the return buffer.</span></span>

<span data-ttu-id="1c0a3-124">WPD-Treiber können mit ihren Geräten kommunizieren, indem Sie einen Kernelmodustreiber durchlaufen. der Zugriff erfolgt in der Regel über Win32-Datei Vorgänge (d. h. "", "", "", "", "Write file" usw.)</span><span class="sxs-lookup"><span data-stu-id="1c0a3-124">WPD drivers may communicate with their devices by going through a kernel-mode driver, typically accessed via Win32 file operations (that is, CreateFile, ReadFile, WriteFile, and so on).</span></span> <span data-ttu-id="1c0a3-125">Bei den gängigen Bussen werden von Microsoft standardmäßige Kernel Treiber für die zu verwendenden Anbieter bereitgestellt, die es Anbietern ermöglichen, eine Treiber Lösung im Benutzermodus zu liefern.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-125">For the common buses, Microsoft will provide standard kernel drivers for vendors to use, which will allow vendors to ship a user-mode-only driver solution.</span></span> <span data-ttu-id="1c0a3-126">Darüber hinaus stellt Microsoft für MTP-Geräte (Media Transfer Protocol) und MSC-Geräte (Massenspeicher Klasse) WPD-Klassen Treiber bereit.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-126">In addition, for Media Transfer Protocol (MTP) and Mass Storage Class (MSC) devices, Microsoft will provide WPD class drivers.</span></span>

<span data-ttu-id="1c0a3-127">Weitere Informationen zu WPD-Treibern finden Sie im Windows-Treiberkit unter Treiber Dokumentation für tragbare Windows-Geräte.</span><span class="sxs-lookup"><span data-stu-id="1c0a3-127">For more information about WPD drivers, see the Windows Portable Devices Driver documentation in the Windows Driver Kit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c0a3-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1c0a3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c0a3-129">**Anwendungs Übersicht**</span><span class="sxs-lookup"><span data-stu-id="1c0a3-129">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



