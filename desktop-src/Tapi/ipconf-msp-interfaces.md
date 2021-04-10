---
description: Der MSP für die IP-Konferenz implementiert mehrere anbieterspezifische Schnittstellen für die Teilnehmer Steuerung. Diese Schnittstellen werden für das-Objekt aufgerufen, wenn dieser MSP dem-Befehl zugeordnet ist.
ms.assetid: 01af2452-de2d-42ce-970d-82a83ae0b428
title: Ipconf-MSP-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edb3c04a93909d237ae25e06c3ed2e0fcc5db9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131044"
---
# <a name="ipconf-msp-interfaces"></a><span data-ttu-id="b3bd6-104">Ipconf-MSP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b3bd6-104">IPConf MSP Interfaces</span></span>

<span data-ttu-id="b3bd6-105">\[ Die ipconf-MSP-Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b3bd6-105">\[ The IPConf MSP Interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b3bd6-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="b3bd6-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b3bd6-107">Der MSP für die IP-Konferenz implementiert mehrere anbieterspezifische Schnittstellen für die Teilnehmer Steuerung.</span><span class="sxs-lookup"><span data-stu-id="b3bd6-107">The IP conferencing MSP implements several provider-specific interfaces for participant control.</span></span> <span data-ttu-id="b3bd6-108">Diese Schnittstellen werden für das-Objekt aufgerufen, wenn dieser MSP dem-Befehl zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b3bd6-108">These interfaces are exposed on the call object, if this MSP is associated with the call.</span></span>

<span data-ttu-id="b3bd6-109">Die [**itparticipvorgänger Vent**](itparticipantevent.md) -Schnittstelle und die [**ienumparticipants**](ienumparticipant.md) -Schnittstelle sind eigenständige Objekte und werden hier zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="b3bd6-109">The [**ITParticipantEvent**](itparticipantevent.md) and [**IEnumParticipant**](ienumparticipant.md) interfaces are stand-alone objects, and are listed here for reference convenience.</span></span>



| <span data-ttu-id="b3bd6-110">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b3bd6-110">Interface</span></span>                                            | <span data-ttu-id="b3bd6-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3bd6-111">Description</span></span>                                                                                                                                               |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3bd6-112">**Imulticastcontrol**</span><span class="sxs-lookup"><span data-stu-id="b3bd6-112">**IMulticastControl**</span></span>](imulticastcontrol.md)       | <span data-ttu-id="b3bd6-113">Ermöglicht es einer Anwendung, den Loopback Modus ( [**Multicast- \_ Loopback \_ Modus**](multicast-loopback-mode.md)) für ein Multicast Konferenz Objekt festzulegen und zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b3bd6-113">Allows an application to set and get the loopback mode ( [**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md)) for a multicast conference object.</span></span> |
| [<span data-ttu-id="b3bd6-114">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="b3bd6-114">**ITParticipant**</span></span>](itparticipant.md)               | <span data-ttu-id="b3bd6-115">Ermöglicht einer Anwendung das Abrufen von Informationen zu Konferenzteilnehmern und das Abrufen von Zeigern auf die Streams, die diesen Teilnehmern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b3bd6-115">Allows an application to retrieve information on conference participants, and get pointers to the streams associated with those participants.</span></span>             |
| [<span data-ttu-id="b3bd6-116">**Itparticipantcontrol**</span><span class="sxs-lookup"><span data-stu-id="b3bd6-116">**ITParticipantControl**</span></span>](itparticipantcontrol.md) | <span data-ttu-id="b3bd6-117">Ermöglicht es einer Anwendung, Zeiger auf die Teilnehmer einer Konferenz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3bd6-117">Allows an application to retrieve pointers to the participants in a conference.</span></span>                                                                           |
| [<span data-ttu-id="b3bd6-118">**Itparticipvorgänger Vent**</span><span class="sxs-lookup"><span data-stu-id="b3bd6-118">**ITParticipantEvent**</span></span>](itparticipantevent.md)     | <span data-ttu-id="b3bd6-119">Ermöglicht es einer Anwendung, Ereignis Informationen zu einem Konferenzteilnehmer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3bd6-119">Allows an application to retrieve event information concerning a conference participant.</span></span>                                                                  |
| [<span data-ttu-id="b3bd6-120">**Ienumteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="b3bd6-120">**IEnumParticipant**</span></span>](ienumparticipant.md)         | <span data-ttu-id="b3bd6-121">Listet den [**itteilnehmer**](itparticipant.md)auf.</span><span class="sxs-lookup"><span data-stu-id="b3bd6-121">Enumerates [**ITParticipant**](itparticipant.md).</span></span>                                                                                                        |



 

 

 



