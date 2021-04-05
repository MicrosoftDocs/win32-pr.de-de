---
title: Informationen zu NAP
description: Informationen zu NAP
ms.assetid: c5dc4956-dcb7-4fcf-b4cc-2fac016427dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4227e1291945fa2d3b7876df27c2cc18cdfde2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707824"
---
# <a name="about-nap"></a><span data-ttu-id="0da20-103">Informationen zu NAP</span><span class="sxs-lookup"><span data-stu-id="0da20-103">About NAP</span></span>

> [!Note]  
> <span data-ttu-id="0da20-104">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0da20-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0da20-105">Der Netzwerk Zugriffsschutz (Network Access Protection, NAP) soll Administratoren dabei helfen, die Integrität der Computer im Netzwerk beizubehalten, die wiederum die Gesamt Integrität des Netzwerks aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="0da20-105">Network Access Protection (NAP) is designed to help administrators maintain the health of the computers on the network, which in turns helps maintain the overall integrity of the network.</span></span> <span data-ttu-id="0da20-106">Es ist nicht zum Sichern eines Netzwerks vor böswilligen Benutzern vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="0da20-106">It is not designed to secure a network from malicious users.</span></span> <span data-ttu-id="0da20-107">Wenn ein Computer beispielsweise über die gesamte Software und Konfigurationen verfügt, die für die Netzwerk Zugriffs Richtlinie erforderlich sind, wird der Computer als fehlerfrei oder kompatibel eingestuft und erhält den entsprechenden Zugriff auf das Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0da20-107">For example, if a computer has all the software and configurations that the network access policy requires, the computer is considered healthy or compliant, and it will be granted the appropriate access to the network.</span></span> <span data-ttu-id="0da20-108">NAP verhindert nicht, dass ein autorisierter Benutzer mit einem kompatiblen Computer ein schädliches Programm in das Netzwerk hochladen oder ein anderes ungeeignetes Verhalten einbindet.</span><span class="sxs-lookup"><span data-stu-id="0da20-108">NAP does not prevent an authorized user with a compliant computer from uploading a malicious program to the network or engaging in other inappropriate behavior.</span></span>

<span data-ttu-id="0da20-109">Um den Zugriff auf ein Netzwerk zu schützen, muss eine Netzwerkinfrastruktur die folgenden Funktionsbereiche bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="0da20-109">To protect access to a network, a network infrastructure needs to provide the following areas of functionality:</span></span>

-   <span data-ttu-id="0da20-110">Integritäts Überprüfung: bestimmt, ob die Computer den System Integritäts Anforderungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0da20-110">Health validation: Determines whether the computers are compliant with system health requirements.</span></span>
-   <span data-ttu-id="0da20-111">Netzwerk Einschränkung: schränkt den Zugriff auf das Netzwerk oder die Kommunikation für Clients ein, die nicht den System Integritäts Anforderungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0da20-111">Network restriction: Restricts access to the network or communication for clients that do not comply with system health requirements.</span></span>
-   <span data-ttu-id="0da20-112">Wiederherstellung: Stellt erforderliche Updates bereit, damit der Computer seinen nicht kompatiblen Integritäts Status korrigieren kann.</span><span class="sxs-lookup"><span data-stu-id="0da20-112">Remediation: Provides necessary updates to allow the computer to correct its noncompliant health state.</span></span>
-   <span data-ttu-id="0da20-113">Fortlaufende Konformität: ermöglicht den Zugriff auf das Netzwerk, solange der Computer des Benutzers die Integritäts Richtlinien Anforderungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="0da20-113">Ongoing compliance: Permits access to the network as long as the user's computer meets health policy requirements.</span></span>

<span data-ttu-id="0da20-114">Windows XP mit Service Pack 3 (SP3), Windows Vista und Windows Server 2008 stellen NAP-Erzwingungs Methoden für die DHCP-Adress Konfiguration (Dynamic Host Configuration Protocol), RAS-basierte VPN (Virtual Private Network)-Verbindungen, IEEE 802.1 x-authentifizierte Kabel-und Drahtlos Verbindungen und IPSec-basierte (Internet Protocol Security) Kommunikation bereit.</span><span class="sxs-lookup"><span data-stu-id="0da20-114">Windows XP with Service Pack 3 (SP3), Windows Vista, and Windows Server 2008 provide NAP enforcement methods for Dynamic Host Configuration Protocol (DHCP) address configuration, remote access-based virtual private network (VPN) connections, IEEE 802.1X-authenticated wired and wireless connections, and Internet Protocol security (IPsec)-based communications.</span></span> <span data-ttu-id="0da20-115">Die NAP-Plattform unterstützt zusätzlich eine Architektur, durch die Integritäts Überprüfung, Netzwerk Einschränkung, Wiederherstellung und fortlaufende Konformität von zusätzlichen Komponenten unterstützt werden, die von Drittanbietern oder von Microsoft bereitgestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="0da20-115">The NAP platform additionally supports an architecture through which health validation, network restriction, remediation, and ongoing compliance are supported by additional components that can be supplied by third-party software vendors or by Microsoft.</span></span>

<span data-ttu-id="0da20-116">Die NAP-Plattform umfasst die folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="0da20-116">The NAP platform includes the following components:</span></span>

-   [<span data-ttu-id="0da20-117">NAP-Client Architektur</span><span class="sxs-lookup"><span data-stu-id="0da20-117">NAP Client Architecture</span></span>](nap-client-architecture.md)
-   [<span data-ttu-id="0da20-118">Server seitige NAP-Architektur</span><span class="sxs-lookup"><span data-stu-id="0da20-118">NAP Server-side Architecture</span></span>](nap-server-side-architecture.md)
-   [<span data-ttu-id="0da20-119">Kommunikation zwischen NAP-Client und Server seitiger Komponente</span><span class="sxs-lookup"><span data-stu-id="0da20-119">NAP Client and Server-side Component Communication</span></span>](nap-client-and-server-side-component-communication.md)

<span data-ttu-id="0da20-120">Der NAP-Client erfordert Windows Vista, Windows XP mit SP3 oder Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="0da20-120">The NAP client requires Windows Vista, Windows XP with SP3, or Windows Server 2008.</span></span> <span data-ttu-id="0da20-121">Der NAP-Integritäts Richtlinien Server und NAP-Erzwingungs Punkte für DHCP-, VPN-und IPsec-Erzwingung erfordern Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="0da20-121">The NAP health policy server and NAP enforcement points for DHCP, VPN, and IPsec enforcement require Windows Server 2008.</span></span>

 

 




