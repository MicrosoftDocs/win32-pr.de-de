---
description: Mit den TAPI-Steuerelementen von TAPI 3 können Programmierer Anwendungen erstellen, die Multicast-Multicast-IP-Konferenzen erstellen und entdecken.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Rendezvous-IP-telefoniekonferenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1cbfc3a1e07fdc245af0ae6b93277c90083a75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215989"
---
# <a name="rendezvous-ip-telephony-conferencing"></a><span data-ttu-id="6d351-103">Rendezvous-IP-telefoniekonferenzen</span><span class="sxs-lookup"><span data-stu-id="6d351-103">Rendezvous IP Telephony Conferencing</span></span>

<span data-ttu-id="6d351-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6d351-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6d351-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="6d351-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6d351-106">Mit den TAPI-Steuerelementen von TAPI 3 können Programmierer Anwendungen erstellen, die Multicast-Multicast-IP-Konferenzen erstellen und entdecken.</span><span class="sxs-lookup"><span data-stu-id="6d351-106">The TAPI 3 Rendezvous controls enable a programmer to create applications that can create and discover multimedia multicast IP conferences.</span></span>

<span data-ttu-id="6d351-107">Die wichtigsten Komponenten von Rendezvous:</span><span class="sxs-lookup"><span data-stu-id="6d351-107">The key components of Rendezvous:</span></span>

<span data-ttu-id="6d351-108">[Verzeichnis Steuerelemente](directory-controls.md) sind eine Abstraktion von Konferenz Auflistungen auf einem ILS-oder NTDS-Server.</span><span class="sxs-lookup"><span data-stu-id="6d351-108">[Directory Controls](directory-controls.md) are an abstraction of conference listings on an ILS or NTDS server.</span></span>

<span data-ttu-id="6d351-109">[Konferenz-BLOB](conference-blob-controls.md) -Steuerelemente stellen Konferenz spezifische Informationen dar, wie z. b. Start-und Endzeit.</span><span class="sxs-lookup"><span data-stu-id="6d351-109">[Conference Blob Controls](conference-blob-controls.md) represent conference-specific information such as start and stop time.</span></span> <span data-ttu-id="6d351-110">Spezielle Schnittstellen werden für SDP-protokollblobzeichen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6d351-110">Special interfaces are provided for SDP protocol blobs.</span></span> <span data-ttu-id="6d351-111">Ausführliche Informationen finden Sie unter RFC 2327 mit dem Titel "SDP: Sitzungs Beschreibungs Protokoll".</span><span class="sxs-lookup"><span data-stu-id="6d351-111">For detailed information, see RFC 2327 entitled "SDP: Session Description Protocol."</span></span> <span data-ttu-id="6d351-112">Eine aktuelle Kopie dieser RFC kann mithilfe einer Internet Suchmaschine gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="6d351-112">A current copy of this RFC can be located using an Internet search engine.</span></span>

<span data-ttu-id="6d351-113">[Multicast-com-Schnittstellen](multicast-com-interfaces.md) sind COM-Wrapper für die MADCAP-Funktionen, die zuvor als MDHCP bekannt waren.</span><span class="sxs-lookup"><span data-stu-id="6d351-113">[Multicast COM Interfaces](multicast-com-interfaces.md) are COM wrappers for the MADCAP functions, formerly know as MDHCP.</span></span> <span data-ttu-id="6d351-114">Diese Schnittstellen ermöglichen es einer Anwendung, Multicast Adressen von einem Multicast Adress Zuordnungs Server zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6d351-114">These interfaces allow an application to get multicast addresses from a multicast address allocation server.</span></span>

<span data-ttu-id="6d351-115">Das folgende Material enthält eine allgemeine Übersicht und einige Verwendungs Beispiele für die Rendezvous-Steuerelemente für IP-Telefonie und Konferenzen.</span><span class="sxs-lookup"><span data-stu-id="6d351-115">The following material provides a general overview and some usage examples of the Rendezvous controls for IP telephony and conferencing.</span></span>

 

 



