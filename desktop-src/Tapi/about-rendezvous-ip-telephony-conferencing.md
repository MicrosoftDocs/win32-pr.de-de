---
description: Die TAPI-Steuerelemente von TAPI 3 bieten Mechanismen zum ankündigen und entdecken von Multimedia-IP-Konferenzen für mehr Parteien. Im folgenden wird eine Reihe von Component Object Model (com)-Komponenten und-Schnittstellen für die Implementierung von Konferenz Beschreibungen beschrieben.
ms.assetid: 0ca2edac-b507-497e-9e63-78a10466e2eb
title: Informationen zu Rendezvous-IP-Telefonkonferenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4bd06fb848088a42e34bd7b176358a7507e3d2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563389"
---
# <a name="about-rendezvous-ip-telephony-conferencing"></a><span data-ttu-id="5a3f7-104">Informationen zu Rendezvous-IP-Telefonkonferenzen</span><span class="sxs-lookup"><span data-stu-id="5a3f7-104">About Rendezvous IP Telephony Conferencing</span></span>

<span data-ttu-id="5a3f7-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5a3f7-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5a3f7-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="5a3f7-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5a3f7-107">Die TAPI-Steuerelemente von TAPI 3 bieten Mechanismen zum ankündigen und entdecken von Multimedia-IP-Konferenzen für mehr Parteien.</span><span class="sxs-lookup"><span data-stu-id="5a3f7-107">The TAPI 3 Rendezvous controls provide mechanisms to advertise and discover multiparty multimedia IP conferences.</span></span> <span data-ttu-id="5a3f7-108">Im folgenden wird eine Reihe von Component Object Model (com)-Komponenten und-Schnittstellen für die Implementierung von Konferenz Beschreibungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5a3f7-108">The following describes a set of Component Object Model (COM) components and interfaces to implement conferencing.</span></span>

<span data-ttu-id="5a3f7-109">COM ist das grundlegende Codierungs Modell für TAPI 3, und es wird davon ausgegangen, dass es in diesem Dokument vertraut ist.</span><span class="sxs-lookup"><span data-stu-id="5a3f7-109">COM is the basic coding model for TAPI 3, and familiarity with it is assumed throughout this document.</span></span> <span data-ttu-id="5a3f7-110">Weitere Informationen zu com finden Sie im Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="5a3f7-110">For information on COM, search the Platform Software Development Kit (SDK).</span></span>

## <a name="features"></a><span data-ttu-id="5a3f7-111">Features</span><span class="sxs-lookup"><span data-stu-id="5a3f7-111">Features</span></span>

-   <span data-ttu-id="5a3f7-112">Stellt die Abstraktion eines Konferenz Verzeichnisses zum Manipulieren von Ankündigungen von Multimedia-Konferenzen bereit.</span><span class="sxs-lookup"><span data-stu-id="5a3f7-112">Provides the abstraction of a conference directory for manipulating announcements of multimedia conferences</span></span>
-   <span data-ttu-id="5a3f7-113">Bietet Sicherheit durch Authentifizierung, Verschlüsselung und eine pro-Ankündigung-Zugriffs Steuerungs Schicht (ACL).</span><span class="sxs-lookup"><span data-stu-id="5a3f7-113">Provides security through authentication, encryption, and a per-announcement access control layer (ACL)</span></span>
-   <span data-ttu-id="5a3f7-114">Stellt ein gemeinsames Schema für eine Konferenzankündigung bereit und ermöglicht die Suche nach Attributwerten.</span><span class="sxs-lookup"><span data-stu-id="5a3f7-114">Provides a common schema for a conference announcement, enabling searches by attribute values</span></span>
-   <span data-ttu-id="5a3f7-115">Ermöglicht Erweiterungen durch ein vom Anbieter gesichertes Attribut (Conference BLOB) im Schema.</span><span class="sxs-lookup"><span data-stu-id="5a3f7-115">Allows extensions through a provider-maintained attribute (conference blob) in the schema</span></span>
-   <span data-ttu-id="5a3f7-116">Stellt einen COM-Wrapper für die MADCAP-API (Multicast Address Allocation) bereit.</span><span class="sxs-lookup"><span data-stu-id="5a3f7-116">Provides a COM wrapper for the multicast address allocation (MADCAP) API</span></span>

## <a name="architecture"></a><span data-ttu-id="5a3f7-117">Architektur</span><span class="sxs-lookup"><span data-stu-id="5a3f7-117">Architecture</span></span>

<span data-ttu-id="5a3f7-118">In den folgenden Beschreibungen und Diagrammen werden wichtige Aspekte der Systemarchitektur veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="5a3f7-118">The following descriptions and diagram illustrate key aspects of the system architecture.</span></span>

-   <span data-ttu-id="5a3f7-119">Der Client kann die in einem dynamischen ILS-Verzeichnis oder NTDS-Server gespeicherten Konferenzen mithilfe von Rendezvous-Steuerelementen bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5a3f7-119">The client can manipulate conferences stored on an ILS dynamic directory or NTDS server using Rendezvous controls.</span></span> <span data-ttu-id="5a3f7-120">Das Lightweight Directory Access Protocol (LDAP) wird für die Kommunikation mit einem ILS-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a3f7-120">The Lightweight Directory Access Protocol (LDAP) is used to communicate with an ILS server.</span></span>
-   <span data-ttu-id="5a3f7-121">Die Rendezvous-Steuerelemente bieten duale com-Schnittstellen für die Skripterstellung und Programmierung.</span><span class="sxs-lookup"><span data-stu-id="5a3f7-121">The Rendezvous controls provide dual COM interfaces for scripting and programming.</span></span>
-   <span data-ttu-id="5a3f7-122">Ein Sitzungs Ankündigungs Protokoll (SAP) mit direktem Zugriff auf das Internet lauscht auf Konferenzankündigungen im Internet und füllt dynamische Server mit den Konferenz Informationen auf.</span><span class="sxs-lookup"><span data-stu-id="5a3f7-122">A Session Announcement Protocol (SAP) server with direct access to the Internet listens to conference announcements on the Internet and populates ILS dynamic servers with the conference information.</span></span> <span data-ttu-id="5a3f7-123">Ebenso kündigt Sie auch die lokal erstellten Konferenzen an, deren Bereich das Internet umfasst.</span><span class="sxs-lookup"><span data-stu-id="5a3f7-123">Similarly, it also announces the locally created conferences whose scope includes the Internet.</span></span> <span data-ttu-id="5a3f7-124">(Der SAP-Server ist für Microsoft Windows 2000 nicht geplant.)</span><span class="sxs-lookup"><span data-stu-id="5a3f7-124">(The SAP server is not planned for Microsoft Windows 2000.)</span></span>

![Rendezvous-Systemarchitektur](images/rend1.png)

 

 



