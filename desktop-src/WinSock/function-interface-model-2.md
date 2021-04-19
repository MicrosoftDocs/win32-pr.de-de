---
description: Windows Sockets Transport und Namespace&\# 8211; Dienstanbieter sind DLLs mit einem einzelnen exportierten Prozedur Einstiegspunkt für die Dienstanbieter-Initialisierungsfunktion WSPStartup bzw. NSPStartup.
ms.assetid: a3422513-92e2-4011-a756-04ed853e9d56
title: Funktions Schnittstellen Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a500de391dd5f65da610ba79d33938443794262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356757"
---
# <a name="function-interface-model"></a><span data-ttu-id="12bbb-103">Funktions Schnittstellen Modell</span><span class="sxs-lookup"><span data-stu-id="12bbb-103">Function Interface Model</span></span>

<span data-ttu-id="12bbb-104">Windows Sockets Transport und Namespace – Dienstanbieter sind DLLs mit einem einzelnen exportierten Prozedur Einstiegspunkt für die Dienstanbieter-Initialisierungsfunktion [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) bzw. [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup).</span><span class="sxs-lookup"><span data-stu-id="12bbb-104">Windows Sockets transport and namespace–service providers are DLLs with a single exported procedure entry point for the service provider initialization function [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) or [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup), respectively.</span></span> <span data-ttu-id="12bbb-105">Alle anderen Dienstanbieter Funktionen werden für die Ws2 \_ -32.dll über die Verteilungs Tabelle des Dienstanbieters zugänglich gemacht.</span><span class="sxs-lookup"><span data-stu-id="12bbb-105">All other service provider functions are made accessible to the Ws2\_32.dll through the service provider's dispatch table.</span></span> <span data-ttu-id="12bbb-106">Dienstanbieter-dll-32.dll Ws2 werden nur bei Bedarf in den Arbeitsspeicher geladen \_ und werden entladen, wenn ihre Dienste nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="12bbb-106">Service provider DLL's are loaded into memory by the Ws2\_32.dll only when needed, and are unloaded when their services are no longer required.</span></span>

<span data-ttu-id="12bbb-107">Die SPI definiert auch mehrere Umstände, in denen ein Transport Dienstanbieter den Ws2- \_32.dll (upcalls) aufruft, um dll-Supportdienste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="12bbb-107">The SPI also defines several circumstances in which a transport service provider calls up into the Ws2\_32.dll (upcalls) to obtain DLL support services.</span></span> <span data-ttu-id="12bbb-108">Die Transportdienst Anbieter-DLL erhält die \_ *upcalltable* -Tabelle des Ws2-32.dll über den upcalltable-Parameter an [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span><span class="sxs-lookup"><span data-stu-id="12bbb-108">The transport service provider DLL is given the Ws2\_32.dll's upcall dispatch table through the *UpcallTable* parameter to [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span></span>

<span data-ttu-id="12bbb-109">Für Dienstanbieter sollte die Dateinamenerweiterung von "dll" in "" geändert werden. WSP "oder". NSP ".</span><span class="sxs-lookup"><span data-stu-id="12bbb-109">Service providers should have their file name extension changed from "DLL" to ".WSP" or ".NSP".</span></span> <span data-ttu-id="12bbb-110">Diese Anforderung ist nicht strikt.</span><span class="sxs-lookup"><span data-stu-id="12bbb-110">This requirement is not strict.</span></span> <span data-ttu-id="12bbb-111">Ein Dienstanbieter arbeitet weiterhin mit dem Ws2- \_32.dll mit einer beliebigen Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="12bbb-111">A service provider will still operate with the Ws2\_32.dll with any file name extension.</span></span>

<span data-ttu-id="12bbb-112">Die Winsock SPI verwendet die folgende funktionspräfix-Benennungs Konvention:</span><span class="sxs-lookup"><span data-stu-id="12bbb-112">The Winsock SPI uses the following function prefix naming convention:</span></span>

| <span data-ttu-id="12bbb-113">Präfix</span><span class="sxs-lookup"><span data-stu-id="12bbb-113">Prefix</span></span> | <span data-ttu-id="12bbb-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="12bbb-114">Meaning</span></span>                          | <span data-ttu-id="12bbb-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12bbb-115">Description</span></span>                                       |
|--------|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="12bbb-116">WSP</span><span class="sxs-lookup"><span data-stu-id="12bbb-116">WSP</span></span>    | <span data-ttu-id="12bbb-117">Windows Sockets-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="12bbb-117">Windows Sockets Service Provider</span></span> | <span data-ttu-id="12bbb-118">Einstiegspunkte des Transport Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="12bbb-118">Transport service provider entry points</span></span>           |
| <span data-ttu-id="12bbb-119">WPU</span><span class="sxs-lookup"><span data-stu-id="12bbb-119">WPU</span></span>    | <span data-ttu-id="12bbb-120">Windows Sockets-Anbieter-uprufe</span><span class="sxs-lookup"><span data-stu-id="12bbb-120">Windows Sockets Provider Upcall</span></span>  | <span data-ttu-id="12bbb-121">Ws2 \_32.dll Einstiegspunkte für Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="12bbb-121">Ws2\_32.dll entry points for service providers</span></span>    |
| <span data-ttu-id="12bbb-122">WSC</span><span class="sxs-lookup"><span data-stu-id="12bbb-122">WSC</span></span>    | <span data-ttu-id="12bbb-123">Windows Sockets-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="12bbb-123">Windows Sockets Configuration</span></span>    | <span data-ttu-id="12bbb-124">Ws2 \_32.dll Einstiegspunkte für Installations-Applets</span><span class="sxs-lookup"><span data-stu-id="12bbb-124">WS2\_32.dll entry points for installation applets</span></span> |
| <span data-ttu-id="12bbb-125">NSP</span><span class="sxs-lookup"><span data-stu-id="12bbb-125">NSP</span></span>    | <span data-ttu-id="12bbb-126">Namespace Anbieter</span><span class="sxs-lookup"><span data-stu-id="12bbb-126">Namespace Provider</span></span>               | <span data-ttu-id="12bbb-127">Einstiegspunkte des Namespace Anbieters</span><span class="sxs-lookup"><span data-stu-id="12bbb-127">Namespace provider entry points</span></span>                   |



 

<span data-ttu-id="12bbb-128">Wie oben beschrieben, werden diese Einstiegspunkte nicht exportiert (mit Ausnahme von [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) und [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), aber der Zugriff erfolgt über einen Austausch von Dispatchtabellen.</span><span class="sxs-lookup"><span data-stu-id="12bbb-128">As described above, these entry points are not exported (with the exception of [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) and [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), but are accessed through an exchange of dispatch tables.</span></span>

 

 



