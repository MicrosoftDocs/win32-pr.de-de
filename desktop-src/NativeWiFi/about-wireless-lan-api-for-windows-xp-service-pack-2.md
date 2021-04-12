---
description: Eine Teilmenge der nativen WiFi-API-Funktionen wird unter Windows XP mit Service Pack 2 (SP2) und Windows XP mit Service Pack 3 (SP3) unterstützt.
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Native WiFi-API-Unterstützung unter Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cd422c6589b37f516b9d45d072489c9d5e00b82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346009"
---
# <a name="native-wifi-api-support-on-windows-xp"></a><span data-ttu-id="0dfe2-103">Native WiFi-API-Unterstützung unter Windows XP</span><span class="sxs-lookup"><span data-stu-id="0dfe2-103">Native Wifi API Support on Windows XP</span></span>

<span data-ttu-id="0dfe2-104">Eine Teilmenge der nativen WiFi-API-Funktionen wird unter Windows XP mit Service Pack 2 (SP2) und Windows XP mit Service Pack 3 (SP3) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0dfe2-104">A subset of the Native Wifi API functionality is supported on Windows XP with Service Pack 2 (SP2) and Windows XP with Service Pack 3 (SP3).</span></span> <span data-ttu-id="0dfe2-105">Diese Funktionalität ist standardmäßig in Windows XP mit SP3 enthalten.</span><span class="sxs-lookup"><span data-stu-id="0dfe2-105">This functionality is included in Windows XP with SP3 by default.</span></span> <span data-ttu-id="0dfe2-106">In Windows XP mit SP2 kann diese Funktionalität hinzugefügt werden, indem ein Hotfix angewendet wird, der als drahtlose LAN-API für Windows XP mit Service Pack 2 (SP2) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="0dfe2-106">In Windows XP with SP2, this functionality can be added by applying a hotfix, which is known as Wireless LAN API for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="0dfe2-107">Weitere Informationen oder das Herunterladen des Hotfixes finden Sie unter "Entwickler können keine drahtlosen Client Programme erstellen, die drahtlos Profile und Verbindungen über den drahtlos Konfigurations Dienst für drahtlose Daten in Microsoft Windows XP Service Pack 2 (SP2)" in der Hilfe-und Support-Wissensdatenbank unter Verwalten [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) .</span><span class="sxs-lookup"><span data-stu-id="0dfe2-107">For more information or to download the hotfix, see "Developers cannot create wireless client programs that manage wireless profiles and connections over the Wireless Zero Configuration service in Microsoft Windows XP Service Pack 2 (SP2)" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997).</span></span>

<span data-ttu-id="0dfe2-108">Aufgrund der zugrunde liegenden architektonischen Unterschiede in Windows XP gelten für die native WiFi-API von einige Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="0dfe2-108">Because of underlying architectural differences in Windows XP, the Native Wifi API on has some limitations.</span></span> <span data-ttu-id="0dfe2-109">Im folgenden finden Sie eine Liste der Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="0dfe2-109">Here is a list of limitations:</span></span>

-   <span data-ttu-id="0dfe2-110">Höchstens eine SSID kann einem Profil zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0dfe2-110">At most one SSID can be associated with a profile.</span></span>
-   <span data-ttu-id="0dfe2-111">Infrastruktur Netzwerke werden immer vor Ad-hoc-Netzwerken in der Profil Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0dfe2-111">Infrastructure networks always appear before ad hoc networks in the profile list.</span></span>
-   <span data-ttu-id="0dfe2-112">Profilnamen werden von der SSID abgeleitet und können vom Benutzer nicht auf eine beliebige Zeichenfolge festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0dfe2-112">Profile names are derived from the SSID, and cannot be set by the user to an arbitrary string.</span></span>
-   <span data-ttu-id="0dfe2-113">PHY-Typen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0dfe2-113">PHY types are not supported.</span></span>
-   <span data-ttu-id="0dfe2-114">PMK-Zwischenspeicherung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0dfe2-114">Pairwise master key (PMK) caching is not supported.</span></span>
-   <span data-ttu-id="0dfe2-115">IHV-Erweiterbarkeits Funktionen (Independent Hardware Vendor) werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0dfe2-115">Independent hardware vendor (IHV) extensibility functions are not supported.</span></span>
-   <span data-ttu-id="0dfe2-116">Profil Berechtigungen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0dfe2-116">Profile permissions are not supported.</span></span>
-   <span data-ttu-id="0dfe2-117">Es sind nur die WLAN \_ -Benachrichtigungs \_ -ACM \_ -Verbindung und die verbindungsverbindungen mit \_ WLAN- \_ Benachrichtigungs- \_ ACM \_ verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0dfe2-117">Only the wlan\_notification\_acm\_connection\_complete and the wlan\_notification\_acm\_disconnected notifications are available.</span></span>
-   <span data-ttu-id="0dfe2-118">Globale 802.1 x-und EAPOL-Konfigurationseinstellungen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0dfe2-118">Global 802.1X and EAPOL configuration settings are not supported.</span></span>

<span data-ttu-id="0dfe2-119">Die folgenden Funktionen werden von Windows XP mit SP3 und der Wireless LAN-API für Windows XP mit SP2 unterstützt:</span><span class="sxs-lookup"><span data-stu-id="0dfe2-119">The following functions are supported by Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:</span></span>

-   [<span data-ttu-id="0dfe2-120">**WLAN- \_ Benachrichtigungs \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-120">**WLAN\_NOTIFICATION\_CALLBACK**</span></span>](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
-   [<span data-ttu-id="0dfe2-121">**Wlanbelegcatememory**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-121">**WlanAllocateMemory**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory)
-   [<span data-ttu-id="0dfe2-122">**Wlanclosehandle**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-122">**WlanCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle)
-   [<span data-ttu-id="0dfe2-123">**Wlanconnect**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-123">**WlanConnect**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect)
-   [<span data-ttu-id="0dfe2-124">**Wlandeleteprofile**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-124">**WlanDeleteProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   [<span data-ttu-id="0dfe2-125">**Wlandisconnect**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-125">**WlanDisconnect**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)
-   [<span data-ttu-id="0dfe2-126">**Wlanenuminterfaces**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-126">**WlanEnumInterfaces**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   [<span data-ttu-id="0dfe2-127">**Wlanfrememory**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-127">**WlanFreeMemory**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory)
-   [<span data-ttu-id="0dfe2-128">**Wlangetavailablenetworklist**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-128">**WlanGetAvailableNetworkList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   [<span data-ttu-id="0dfe2-129">**Wlangetprofile**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-129">**WlanGetProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)
-   [<span data-ttu-id="0dfe2-130">**Wlangetprofilelist**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-130">**WlanGetProfileList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist)
-   [<span data-ttu-id="0dfe2-131">**Wlanopenhandle**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-131">**WlanOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle)
-   [<span data-ttu-id="0dfe2-132">**Wlanqueryinterface**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-132">**WlanQueryInterface**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   [<span data-ttu-id="0dfe2-133">**Wlanreasoncodedestring**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-133">**WlanReasonCodeToString**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
-   [<span data-ttu-id="0dfe2-134">**Wlanregisternotification**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-134">**WlanRegisterNotification**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
-   [<span data-ttu-id="0dfe2-135">**Wlanscan**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-135">**WlanScan**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   [<span data-ttu-id="0dfe2-136">**Wlansetinterface**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-136">**WlanSetInterface**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
-   [<span data-ttu-id="0dfe2-137">**WLanSetProfile**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-137">**WlanSetProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
-   [<span data-ttu-id="0dfe2-138">**Wlansetprofileeapxmluserdata**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-138">**WlanSetProfileEapXmlUserData**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata)
-   [<span data-ttu-id="0dfe2-139">**Wlansetprofilelist**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-139">**WlanSetProfileList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist)
-   [<span data-ttu-id="0dfe2-140">**Wlansetprofileposition**</span><span class="sxs-lookup"><span data-stu-id="0dfe2-140">**WlanSetProfilePosition**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition)

## <a name="related-topics"></a><span data-ttu-id="0dfe2-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0dfe2-141">Related topics</span></span>

<dl> <dt>

[https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997)
</dt> <dt>

[<span data-ttu-id="0dfe2-142">Informationen zu nativem WiFi</span><span class="sxs-lookup"><span data-stu-id="0dfe2-142">About Native Wifi</span></span>](about-native-wifi.md)
</dt> </dl>

 

 
