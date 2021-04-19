---
description: Das Microsoft-telefonieprogrammierungs Modell abstrahiert die Kommunikationssteuerung von der Gerätesteuerung und gibt Endbenutzer Anwendungen und Gerätehersteller von der Notwendigkeit, im Sperr Schritt zu wechseln, frei.
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Microsoft Telefonie-Programmiermodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efb8947f3b428ab4a252301e3fdd5f94e29f6ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343027"
---
# <a name="microsoft-telephony-programming-model"></a><span data-ttu-id="5b3c2-103">Microsoft Telefonie-Programmiermodell</span><span class="sxs-lookup"><span data-stu-id="5b3c2-103">Microsoft Telephony Programming Model</span></span>

<span data-ttu-id="5b3c2-104">Das Microsoft-telefonieprogrammierungs Modell abstrahiert die Kommunikationssteuerung von der Gerätesteuerung und gibt Endbenutzer Anwendungen und Gerätehersteller von der Notwendigkeit, im Sperr Schritt zu wechseln, frei.</span><span class="sxs-lookup"><span data-stu-id="5b3c2-104">The Microsoft Telephony programming model abstracts communications control from device control, freeing end-user applications and device manufacturers from the need to march in lockstep.</span></span> <span data-ttu-id="5b3c2-105">Die Verwendung dieses Modells erfordert keine detaillierten Informationen zur Gerätesteuerung, und das Gerät muss nicht auf die Anwendung zugeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="5b3c2-105">Using this model, an end-user or server application does not require detailed information on device control and the device does not need to be tailored to the application.</span></span> <span data-ttu-id="5b3c2-106">Anwendungen und Geräte können Innovationen durchlaufen und sich ändern, ohne dass Sie für Kunden nutzlos werden.</span><span class="sxs-lookup"><span data-stu-id="5b3c2-106">Applications and devices can undergo innovation and change without rendering each other useless to customers.</span></span>

<span data-ttu-id="5b3c2-107">Im folgenden Diagramm wird veranschaulicht, wie diese Abstraktion erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="5b3c2-107">The following diagram illustrates how this abstraction is accomplished.</span></span>

![Zusammenfassung der Kommunikationssteuerung durch TAPI von der Gerätesteuerung](images/tapicomp.png)

<span data-ttu-id="5b3c2-109">Diese Komponenten können als Repository spezieller Kenntnisse angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="5b3c2-109">These components can be viewed as repositories of specialized knowledge.</span></span> <span data-ttu-id="5b3c2-110">Die TAPI-Anwendung (Application Programming Interface, Anwendungsprogrammierschnittstelle) kennt die Benutzer Anforderungen, die TAPI-dll und "tapisrv" die allgemeine Telefonie und die Dienstanbieter (TSP und MSP) eine ausführliche Gerätesteuerung.</span><span class="sxs-lookup"><span data-stu-id="5b3c2-110">The Telephony Application Programming Interface (TAPI) application knows user needs, the TAPI DLL and TAPISRV understand general telephony, and the service providers (TSP and MSP) know detailed device control.</span></span> <span data-ttu-id="5b3c2-111">Anwendungs Schreiber und Gerätehersteller benötigen nur allgemeine Kenntnisse der jeweiligen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="5b3c2-111">Application writers and device manufacturers require only general knowledge of each other's requirements.</span></span>

-   <span data-ttu-id="5b3c2-112">Eine Anwendung lädt die TAPI-dll in ihren Prozessbereich und verwendet TAPI, um die Anforderungen zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="5b3c2-112">An application loads the TAPI DLL into its process space and uses TAPI to communicate needs.</span></span>
-   <span data-ttu-id="5b3c2-113">TAPI stellt eine RPC-Link Kommunikation mit dem TAPI-Server her.</span><span class="sxs-lookup"><span data-stu-id="5b3c2-113">TAPI establishes an RPC link communications with the TAPI Server.</span></span>
-   <span data-ttu-id="5b3c2-114">Außerdem erstellt TAPI 3. x ein MSP-Objekt und kommuniziert mit dem Objekt mithilfe eines definierten Satzes von Befehlen, der Media Service Provider Interface (MSPi).</span><span class="sxs-lookup"><span data-stu-id="5b3c2-114">In addition, TAPI 3.x creates an MSP object and communicates with it using a defined set of commands, the Media Service Provider Interface (MSPI).</span></span>
-   <span data-ttu-id="5b3c2-115">Wenn eine Anwendung einen TAPI-Vorgang aufruft, überprüft und marshallt die TAPI-Dynamic-Link-Bibliothek die Parameter und leitet die Informationen an tapisrv weiter.</span><span class="sxs-lookup"><span data-stu-id="5b3c2-115">When an application calls a TAPI operation, the TAPI dynamic-link library validates and marshals the parameters, then forwards the information to TAPISRV.</span></span>
-   <span data-ttu-id="5b3c2-116">Tapisrv verfolgt Kommunikationsressourcen, die für den lokalen Computer verfügbar sind, und stellt mit den Telefoniedienstanbietern (Service Provider Interface, TSPI) eine Schnittstelle mit den Telefoniedienstanbietern</span><span class="sxs-lookup"><span data-stu-id="5b3c2-116">TAPISRV tracks communications resources available to the local machine and interfaces with the Telephony Service Providers (TSPs) using the Telephony Service Provider Interface (TSPI).</span></span>
-   <span data-ttu-id="5b3c2-117">Die Kommunikation zwischen einem TSP und einem MSP erfolgt über eine virtuelle Verbindung, die die TAPI-dll und den tapisrv durchläuft.</span><span class="sxs-lookup"><span data-stu-id="5b3c2-117">Communications between a TSP and an MSP take place using a virtual connection that passes through the TAPI DLL and TAPISRV.</span></span>
-   <span data-ttu-id="5b3c2-118">Das TSP/MSP-paar stellt Informationen zum Gerätestatus und zu den Funktionen bereit und implementiert die spezifischen Befehle, die für eine gewünschte Antwort erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5b3c2-118">The TSP/MSP pair supplies information on device state and capabilities and implements the specific commands required for a desired response.</span></span>

<span data-ttu-id="5b3c2-119">Das Ergebnis der Verwendung dieses Programmiermodells ist, dass Anwendungen Geräteänderungen ignorieren oder anpassen können. neue Geräte können sofort nützlich sein, anstatt auf Änderungen an der Codebasis zu warten.</span><span class="sxs-lookup"><span data-stu-id="5b3c2-119">The result of using this programming model is that applications can ignore or adjust to device changes and new devices can be instantly useful instead of waiting on code base changes.</span></span> <span data-ttu-id="5b3c2-120">Der potenzielle Marktanteil wird sowohl für Anwendungs Schreiber als auch für Gerätehersteller erweitert.</span><span class="sxs-lookup"><span data-stu-id="5b3c2-120">Potential market share is expanded for both application writers and device manufacturers.</span></span>

<span data-ttu-id="5b3c2-121">In den folgenden Themen werden die Microsoft-Telefoniekomponenten ausführlicher beschrieben:</span><span class="sxs-lookup"><span data-stu-id="5b3c2-121">The following topics describe the Microsoft Telephony components in more detail:</span></span>

-   [<span data-ttu-id="5b3c2-122">TAPI-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="5b3c2-122">TAPI Applications</span></span>](tapi-applications.md)
-   [<span data-ttu-id="5b3c2-123">TAPI-dll</span><span class="sxs-lookup"><span data-stu-id="5b3c2-123">TAPI DLL</span></span>](tapi-dll.md)
-   [<span data-ttu-id="5b3c2-124">TAPI-Server</span><span class="sxs-lookup"><span data-stu-id="5b3c2-124">TAPI Server</span></span>](tapi-server.md)
-   [<span data-ttu-id="5b3c2-125">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="5b3c2-125">Service Providers</span></span>](service-providers.md)
-   [<span data-ttu-id="5b3c2-126">Synchrones/Asynchrones Modell</span><span class="sxs-lookup"><span data-stu-id="5b3c2-126">Synchronous/Asynchronous Model</span></span>](synchronous-asynchronous-model.md)
-   [<span data-ttu-id="5b3c2-127">TAPI-Datenstrukturen</span><span class="sxs-lookup"><span data-stu-id="5b3c2-127">TAPI Data Structures</span></span>](tapi-data-structures.md)
-   [<span data-ttu-id="5b3c2-128">TAPI-Dienst Ebenen</span><span class="sxs-lookup"><span data-stu-id="5b3c2-128">TAPI Levels of Service</span></span>](tapi-levels-of-service.md)

 

 



