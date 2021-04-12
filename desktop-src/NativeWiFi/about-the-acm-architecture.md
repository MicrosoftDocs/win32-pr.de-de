---
description: Informationen zur ACM-Architektur
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: Informationen zur ACM-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f037a1823f7045ccaf1dc573c6d213beeebe0a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218199"
---
# <a name="about-the-acm-architecture"></a><span data-ttu-id="0521e-103">Informationen zur ACM-Architektur</span><span class="sxs-lookup"><span data-stu-id="0521e-103">About the ACM Architecture</span></span>

<span data-ttu-id="0521e-104">Das Auto Configuration Module (ACM) ist die neue drahtlose Konfigurationskomponente für Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0521e-104">The Auto Configuration Module (ACM) is the new wireless configuration component for Windows Vista.</span></span> <span data-ttu-id="0521e-105">Windows XP mit Service Pack 3 (SP3) und Wireless LAN API für Windows XP mit Service Pack 2 (SP2) verwenden stattdessen den WZC-Dienst (Wireless Zero Configuration).</span><span class="sxs-lookup"><span data-stu-id="0521e-105">Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2) use the Wireless Zero Configuration (WZC) service instead.</span></span>

<span data-ttu-id="0521e-106">Das ACM scannt Netzwerke in regelmäßigen Abständen und verwendet einen iterativen Prozess zum auswählen und verbinden mit dem bevorzugten Netzwerk im Bereich, wenn für dieses Netzwerk eine Schnittstelle für die automatische Verbindung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0521e-106">The ACM scans networks periodically and uses an iterative process to select and connect to the most preferred network in the range, if that network has an interface enabled for auto-connection.</span></span> <span data-ttu-id="0521e-107">Das ACM speichert und ruft auch Netzwerk Profile ab, die ACM, Media Specific Module (MSM), Security und IHV-Einstellungen (Independent Hardware Vendor) enthalten.</span><span class="sxs-lookup"><span data-stu-id="0521e-107">The ACM also saves and retrieves network profiles, which contain ACM, Media Specific Module (MSM), security, and independent hardware vendor (IHV) settings.</span></span> <span data-ttu-id="0521e-108">Diese Netzwerk Profile sind für die automatische Konfiguration vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="0521e-108">These network profiles are for auto configuration.</span></span>

<span data-ttu-id="0521e-109">Die automatische Konfiguration unterstützt sowohl globale als auch Schnittstellen spezifische Einstellungen und Netzwerk Profile.</span><span class="sxs-lookup"><span data-stu-id="0521e-109">Auto configuration supports both global and per-interface settings and network profiles.</span></span> <span data-ttu-id="0521e-110">Die globalen Einstellungen und Netzwerk Profile werden konfiguriert, wenn der Computer einer Domäne mit einem Gruppenrichtlinien Objekt (GPO) auf Domänen Ebene oder der Organisationseinheit (OU) in der Active Directory-Hierarchie (AD) hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="0521e-110">The global settings and network profiles are configured if the machine has joined a domain with a group policy object (GPO) either at the domain level or the organizational unit (OU) level in the Active Directory (AD) hierarchy.</span></span> <span data-ttu-id="0521e-111">Diese Gruppenrichtlinien Einstellungen und-Profile sind schreibgeschützt, werden auf jede 802,11-Schnittstelle im System angewendet und haben immer Vorrang vor den einzelnen Schnittstellen-und benutzerspezifischen Einstellungen und Netzwerk Profilen.</span><span class="sxs-lookup"><span data-stu-id="0521e-111">These group policy settings and profiles are read-only, applied to each 802.11 interface in the system, and always take precedence over the per-interface and per-user settings and network profiles.</span></span> <span data-ttu-id="0521e-112">Die Gruppenrichtlinien Profile werden am Anfang der Liste bevorzugter Netzwerk Profile auf jeder 802,11-Netzwerkschnittstelle platziert.</span><span class="sxs-lookup"><span data-stu-id="0521e-112">The group policy profiles are placed at the top of the preferred network profile list on each 802.11 network interface.</span></span>

<span data-ttu-id="0521e-113">Die ACM-Architektur ist erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="0521e-113">The ACM architecture is extensible.</span></span> <span data-ttu-id="0521e-114">IHVs können proprietäre drahtlose Funktionen implementieren, ohne das bereitgestellte Native 802,11-Framework zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0521e-114">IHVs can implement proprietary wireless functionality without altering the provided native 802.11 framework.</span></span> <span data-ttu-id="0521e-115">Die verfügbar gemachten IHV-Steuerungsfunktionen und-Strukturen ermöglichen diese Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="0521e-115">The exposed IHV control functions and structures enable this extensibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0521e-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0521e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0521e-117">Informationen zu nativem WiFi</span><span class="sxs-lookup"><span data-stu-id="0521e-117">About Native Wifi</span></span>](about-native-wifi.md)
</dt> </dl>

 

 



