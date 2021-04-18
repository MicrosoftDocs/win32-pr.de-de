---
description: TAPI Version 3,1 ist eine COM-basierte API, die klassische und IP-Telefonie zusammenfasst. Mögliche Anwendungen reichen von einfachen sprach aufrufen über das Public-Switched-Telefon Netzwerk (PSTN) bis hin zu Multicast-Multimedia-IP-Konferenzen mit Dienst Qualität (Quality of Service, QoS).
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: TAPI 3,1 (Übersicht)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30b70ccdc1c4a0985107d2bd2fc36bfbe4e3fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368736"
---
# <a name="tapi-31-overview"></a><span data-ttu-id="2c515-104">TAPI 3,1 (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="2c515-104">TAPI 3.1 Overview</span></span>

<span data-ttu-id="2c515-105">TAPI Version 3,1 ist eine COM-basierte API, die klassische und IP-Telefonie zusammenfasst.</span><span class="sxs-lookup"><span data-stu-id="2c515-105">TAPI version 3.1 is a COM-based API that merges classic and IP telephony.</span></span> <span data-ttu-id="2c515-106">Mögliche Anwendungen reichen von einfachen sprach aufrufen über das Public-Switched-Telefon Netzwerk (PSTN) bis hin zu Multicast-Multimedia-IP-Konferenzen mit Dienst Qualität (Quality of Service, QoS).</span><span class="sxs-lookup"><span data-stu-id="2c515-106">Possible applications range from simple voice calls over the Public Switched Telephone Network (PSTN) to multicast multimedia IP conferencing with quality of service (QOS).</span></span>

<span data-ttu-id="2c515-107">Weitere Informationen zu TAPI 3,1-IP-Telefoniefunktionen finden Sie im Whitepaper "IP-Telefonie mit TAPI 3", das sich auf der Microsoft-Website befindet.</span><span class="sxs-lookup"><span data-stu-id="2c515-107">For additional information on TAPI 3.1 IP Telephony capabilities, please consult the "IP Telephony with TAPI 3" white paper, which can be found on the Microsoft web site.</span></span>

<span data-ttu-id="2c515-108">Es gibt vier Hauptkomponenten zu TAPI 3,1:</span><span class="sxs-lookup"><span data-stu-id="2c515-108">There are four major components to TAPI 3.1:</span></span>

-   <span data-ttu-id="2c515-109">COM-API</span><span class="sxs-lookup"><span data-stu-id="2c515-109">COM API</span></span>
-   <span data-ttu-id="2c515-110">TAPI-Server</span><span class="sxs-lookup"><span data-stu-id="2c515-110">TAPI Server</span></span>
-   <span data-ttu-id="2c515-111">Telefoniedienstanbieter (TSPS)</span><span class="sxs-lookup"><span data-stu-id="2c515-111">Telephony Service Providers (TSPs)</span></span>
-   <span data-ttu-id="2c515-112">Medienstrom Anbieter (MSPs)</span><span class="sxs-lookup"><span data-stu-id="2c515-112">Media Stream Providers (MSPs)</span></span>

<span data-ttu-id="2c515-113">Das folgende Diagramm veranschaulicht die TAPI 3,1-Architektur:</span><span class="sxs-lookup"><span data-stu-id="2c515-113">The following diagram illustrates the TAPI 3.1 architecture:</span></span>

![TAPI 3-Architektur](images/callarc-gif-1.png)

<span data-ttu-id="2c515-115">Die API wird als Suite von Component Object Model (com)-Objekten implementiert.</span><span class="sxs-lookup"><span data-stu-id="2c515-115">The API is implemented as a suite of Component Object Model (COM) objects.</span></span> <span data-ttu-id="2c515-116">Das Verschieben von TAPI in das objektorientierte com-Modell ermöglicht Entwicklern das Schreiben von TAPI-fähigen Anwendungen in vielen Sprachen, wie z. b. Java, Visual Basic oder C/C++.</span><span class="sxs-lookup"><span data-stu-id="2c515-116">Moving TAPI to the object-oriented COM model allows developers to write TAPI-enabled applications in many languages, such as Java, Visual Basic, or C/C++.</span></span> <span data-ttu-id="2c515-117">Die Verwendung von com ermöglicht Komponenten Upgrades von TAPI-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="2c515-117">Use of COM enables component upgrades of TAPI features.</span></span>

<span data-ttu-id="2c515-118">Der TAPI-Server Prozess (tapisrv) abstrahiert die TAPI Service Provider Interface (TSPI) von TAPI 3. x und TAPI 2. x und ermöglicht so die Verwendung von TAPI 2. x-Telefoniedienstanbietern mit TAPI 3. x, wobei der interne Status von TAPI beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="2c515-118">The TAPI Server process (TAPISRV) abstracts the TAPI Service Provider Interface (TSPI) from TAPI 3.x and TAPI 2.x, allowing TAPI 2.x Telephony Service Providers to be used with TAPI 3.x, maintaining the internal state of TAPI.</span></span> <span data-ttu-id="2c515-119">Tapisrv ist als Dienst Prozess innerhalb von svchost implementiert.</span><span class="sxs-lookup"><span data-stu-id="2c515-119">TAPISRV is implemented as a service process within SVCHOST.</span></span>

<span data-ttu-id="2c515-120">[Dienstanbieter](./tapi-service-providers.md) : abstrakte anbieterspezifische Medien Transportmechanismen.</span><span class="sxs-lookup"><span data-stu-id="2c515-120">[Service Providers](./tapi-service-providers.md) abstract provider-specific media transport mechanisms.</span></span> <span data-ttu-id="2c515-121">Sie sind in der Regel paarweise vorhanden – einem Telefoniedienstanbieter (TSP) für die Callcenter-Steuerung und einem Media Service Provider (MSP) für die Mediensteuerung.</span><span class="sxs-lookup"><span data-stu-id="2c515-121">They typically exist in pairs – a Telephony Service Provider (TSP) for call control and a Media Service Provider (MSP) for media control.</span></span>

<span data-ttu-id="2c515-122">[Telefoniedienstanbieter](./telephony-service-providers-start-page.md) (TSPS) sind dafür verantwortlich, das Protokoll unabhängige Aufrufmodell von TAPI in Protokoll spezifische Aufrufe der Steuerungsmechanismen aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="2c515-122">[Telephony Service Providers](./telephony-service-providers-start-page.md) (TSPs) are responsible for resolving the protocol-independent call model of TAPI into protocol-specific call control mechanisms.</span></span> <span data-ttu-id="2c515-123">TAPI 3,1 bietet Abwärtskompatibilität mit TAPI 2,1 TSPS.</span><span class="sxs-lookup"><span data-stu-id="2c515-123">TAPI 3.1 provides backward compatibility with TAPI 2.1 TSPs.</span></span> <span data-ttu-id="2c515-124">Zwei IP-Telefoniedienstanbieter (und die zugehörigen MSPs) werden standardmäßig mit TAPI 3,1 ausgeliefert: dem H. 323 TSP und dem IP-Multicast Konferenz-TSP.</span><span class="sxs-lookup"><span data-stu-id="2c515-124">Two IP Telephony service providers (and their associated MSPs) ship by default with TAPI 3.1: the H.323 TSP and the IP Multicast Conferencing TSP.</span></span>

<span data-ttu-id="2c515-125">[Media Service Providers](media-service-providers-start-page.md) (MSPs) bieten eine einheitliche Methode für den Zugriff auf die Mediendaten Ströme in einem-Befehl, wobei die DirectShow<sup>TM</sup> -API als primärer Mediendaten Strom Handler unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2c515-125">[Media Service Providers](media-service-providers-start-page.md) (MSPs) provide a uniform way to access the media streams in a call, supporting the DirectShow<sup>TM</sup> API as the primary media stream handler.</span></span> <span data-ttu-id="2c515-126">TAPI-MSPs implementieren DirectShow-Schnittstellen für einen bestimmten TSP und sind für alle Telefoniedienste erforderlich, die DirectShow-Streaming verwenden.</span><span class="sxs-lookup"><span data-stu-id="2c515-126">TAPI MSPs implement DirectShow interfaces for a particular TSP and are required for any telephony service that makes use of DirectShow streaming.</span></span> <span data-ttu-id="2c515-127">Generische Streams werden von der Anwendung behandelt.</span><span class="sxs-lookup"><span data-stu-id="2c515-127">Generic streams are handled by the application.</span></span>

 

 
