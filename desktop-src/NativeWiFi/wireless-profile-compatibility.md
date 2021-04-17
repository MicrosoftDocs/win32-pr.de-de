---
description: Aufgrund der zugrunde liegenden architektonischen Unterschiede im Betriebssystem unterstützen Windows XP mit Service Pack 3 (SP3) und die Wireless LAN-API für Windows XP mit Service Pack 2 (SP2) nur eine Teilmenge der Elemente, die im WLAN \_ -Profil Schema und im Onex-Schema Referenzmaterial beschrieben sind.
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: Kompatibilität von drahtlos Profilen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e0eebfa627fb99d50490907108a2ddc7360202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529240"
---
# <a name="wireless-profile-compatibility"></a><span data-ttu-id="d56f2-103">Kompatibilität von drahtlos Profilen</span><span class="sxs-lookup"><span data-stu-id="d56f2-103">Wireless Profile Compatibility</span></span>

<span data-ttu-id="d56f2-104">Aufgrund der zugrunde liegenden architektonischen Unterschiede im Betriebssystem unterstützen Windows XP mit Service Pack 3 (SP3) und die Wireless LAN-API für Windows XP mit Service Pack 2 (SP2) nur eine Teilmenge der Elemente, die im [WLAN- \_ Profil Schema](wlan-profileschema-schema.md) und im [Onex-Schema](onexschema-schema.md) Referenzmaterial beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="d56f2-104">Because of underlying architectural differences in the operating system, Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2) support only a subset of the elements described in the [WLAN\_profile Schema](wlan-profileschema-schema.md) and [OneX Schema](onexschema-schema.md) reference material.</span></span>

<span data-ttu-id="d56f2-105">Alle Profile, die den Anforderungen Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2 entsprechen, können auch unter Windows Vista und Windows Server 2008 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d56f2-105">All profiles that conform to Windows XP with SP3 and Wireless LAN API for Windows XP with SP2 requirements can also be used on Windows Vista and Windows Server 2008.</span></span>

## <a name="wlan_profile-support"></a><span data-ttu-id="d56f2-106">WLAN- \_ Profil Unterstützung</span><span class="sxs-lookup"><span data-stu-id="d56f2-106">WLAN\_profile Support</span></span>

<span data-ttu-id="d56f2-107">Die folgenden WLAN- \_ Profil Elemente werden in Windows XP mit SP3 oder der Wireless LAN-API für Windows XP mit SP2 nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d56f2-107">The following WLAN\_profile elements are not supported in Windows XP with SP3 or Wireless LAN API for Windows XP with SP2:</span></span>

-   <span data-ttu-id="d56f2-108">Konnektivität (IHV)</span><span class="sxs-lookup"><span data-stu-id="d56f2-108">connectivity (IHV)</span></span>
-   <span data-ttu-id="d56f2-109">IHV (wlanprofile)</span><span class="sxs-lookup"><span data-stu-id="d56f2-109">IHV (WLANProfile)</span></span>
-   <span data-ttu-id="d56f2-110">OUI (ouiheader)</span><span class="sxs-lookup"><span data-stu-id="d56f2-110">OUI (OUIHeader)</span></span>
-   <span data-ttu-id="d56f2-111">phytype (Konnektivität)</span><span class="sxs-lookup"><span data-stu-id="d56f2-111">phyType (connectivity)</span></span>
-   <span data-ttu-id="d56f2-112">Pmkcachemode (Sicherheit)</span><span class="sxs-lookup"><span data-stu-id="d56f2-112">PMKCacheMode (security)</span></span>
-   <span data-ttu-id="d56f2-113">Pmkcachesize (Sicherheit)</span><span class="sxs-lookup"><span data-stu-id="d56f2-113">PMKCacheSize (security)</span></span>
-   <span data-ttu-id="d56f2-114">Pmkcachettl (Sicherheit)</span><span class="sxs-lookup"><span data-stu-id="d56f2-114">PMKCacheTTL (security)</span></span>
-   <span data-ttu-id="d56f2-115">preauthmode (Sicherheit)</span><span class="sxs-lookup"><span data-stu-id="d56f2-115">preAuthMode (security)</span></span>
-   <span data-ttu-id="d56f2-116">preauththrottle (Sicherheit)</span><span class="sxs-lookup"><span data-stu-id="d56f2-116">preAuthThrottle (security)</span></span>
-   <span data-ttu-id="d56f2-117">Sicherheit (IHV)</span><span class="sxs-lookup"><span data-stu-id="d56f2-117">security (IHV)</span></span>
-   <span data-ttu-id="d56f2-118">Type (ouiheader)</span><span class="sxs-lookup"><span data-stu-id="d56f2-118">type (OUIHeader)</span></span>
-   <span data-ttu-id="d56f2-119">usemsonex (IHV)</span><span class="sxs-lookup"><span data-stu-id="d56f2-119">useMSOneX (IHV)</span></span>

<span data-ttu-id="d56f2-120">In der folgenden Tabelle sind die WLAN \_ -Profil Elemente mit eingeschränkten Werten für Windows XP mit SP3 und die drahtlose LAN-API für Windows XP mit SP2 aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d56f2-120">The following table shows WLAN\_profile elements with constrained values for Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:</span></span>



| <span data-ttu-id="d56f2-121">Element</span><span class="sxs-lookup"><span data-stu-id="d56f2-121">Element</span></span>                                                                               | <span data-ttu-id="d56f2-122">Constraint</span><span class="sxs-lookup"><span data-stu-id="d56f2-122">Constraint</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d56f2-123">**Name (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="d56f2-123">**name (WLANProfile)**</span></span>](wlan-profileschema-name-wlanprofile-element.md)             | <span data-ttu-id="d56f2-124">Das Name-Element wird ignoriert, wenn das Profil im Profil Speicher gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="d56f2-124">The name element is ignored when the profile is saved in the profile store.</span></span> <span data-ttu-id="d56f2-125">Der Name des Profils wird automatisch von der SSID des Netzwerks abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d56f2-125">The name of the profile is derived automatically from the SSID of the network.</span></span> <span data-ttu-id="d56f2-126">Bei Infrastrukturnetzwerk Profilen ist der Name des Profils die SSID des Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="d56f2-126">For infrastructure network profiles, the name of the profile is the SSID of the network.</span></span> <span data-ttu-id="d56f2-127">Bei Ad-hoc-Netzwerk Profilen ist der Name des Profils die SSID des Ad-hoc-Netzwerks gefolgt von `-adhoc` .</span><span class="sxs-lookup"><span data-stu-id="d56f2-127">For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by `-adhoc`.</span></span> |
| [<span data-ttu-id="d56f2-128">**geschützt (sharedkey)**</span><span class="sxs-lookup"><span data-stu-id="d56f2-128">**protected (sharedKey)**</span></span>](wlan-profileschema-protected-sharedkey-element.md)       | <span data-ttu-id="d56f2-129">Muss den Wert false aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d56f2-129">Must have a value of FALSE.</span></span>                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="d56f2-130">**Ssidconfig (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="d56f2-130">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md) | <span data-ttu-id="d56f2-131">Beschränkt auf ein untergeordnetes [**SSID-Element (ssidconfig)**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d56f2-131">Restricted to one child [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a><span data-ttu-id="d56f2-132">Onex-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="d56f2-132">OneX Support</span></span>

<span data-ttu-id="d56f2-133">Nur das [**eapconfig**](onexschema-eapconfig-onex-element.md) -Element wird unter Windows XP mit SP3 und der Wireless LAN-API für Windows XP mit SP2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d56f2-133">Only the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is supported on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span> <span data-ttu-id="d56f2-134">Andere Onex-Elemente, sofern Sie in einem Profil vorhanden sind, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d56f2-134">Other OneX elements, if present in a profile, will be ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d56f2-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d56f2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d56f2-136">Informationen zur nativen WiFi-API</span><span class="sxs-lookup"><span data-stu-id="d56f2-136">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="d56f2-137">Native WiFi-API-Unterstützung unter Windows XP</span><span class="sxs-lookup"><span data-stu-id="d56f2-137">Native Wifi API Support on Windows XP</span></span>](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



