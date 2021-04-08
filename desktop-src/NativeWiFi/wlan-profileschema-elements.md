---
description: 'Das WLAN- \_ Profil Schema definiert die folgenden Elemente:'
ms.assetid: 9eb0f446-1202-4770-b09e-250e83524119
title: Schema Elemente WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a94394c32712d8ee8871ada753f342861e1f530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752305"
---
# <a name="wlan_profile-schema-elements"></a><span data-ttu-id="b92e4-103">WLAN- \_ Profil Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="b92e4-103">WLAN\_profile Schema Elements</span></span>

<span data-ttu-id="b92e4-104">Das WLAN- \_ Profil Schema definiert die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="b92e4-104">The WLAN\_profile schema defines the following elements.</span></span> <span data-ttu-id="b92e4-105">Die meisten-Elemente befinden sich im-Namespace `https://www.microsoft.com/networking/WLAN/profile/v1` , mit Ausnahme von " [**fpsmode" (authencryption)**](wlan-profileschema-fipsmode-authencryption-element.md), die sich im-Namespace befindet `https://www.microsoft.com/networking/WLAN/profile/v2` .</span><span class="sxs-lookup"><span data-stu-id="b92e4-105">Most elements are in the namespace `https://www.microsoft.com/networking/WLAN/profile/v1`, except for [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md), which is in the namespace `https://www.microsoft.com/networking/WLAN/profile/v2`.</span></span>

<span data-ttu-id="b92e4-106">In der folgenden Liste werden die definierten Elemente in der Reihenfolge angezeigt, in der die Elemente in einem Profil angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b92e4-106">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="b92e4-107">Die Reihenfolge der Elemente wird erzwungen.</span><span class="sxs-lookup"><span data-stu-id="b92e4-107">The ordering of elements is enforced.</span></span> <span data-ttu-id="b92e4-108">Nicht alle Elemente befinden sich in jedem Profil, da einige Elemente optional sind.</span><span class="sxs-lookup"><span data-stu-id="b92e4-108">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="b92e4-109">In dieser Liste werden nicht alle möglichen Elemente angezeigt, die in einem drahtlos Profil angezeigt werden können, da Elemente in **xs: beliebige** Einfügepunkte hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="b92e4-109">This list does not show all possible elements that can appear in a wireless profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="b92e4-110">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="b92e4-110">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
    -   [<span data-ttu-id="b92e4-111">**Name (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-111">**name (WLANProfile)**</span></span>](wlan-profileschema-name-wlanprofile-element.md)
    -   [<span data-ttu-id="b92e4-112">**Ssidconfig (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-112">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
        -   [<span data-ttu-id="b92e4-113">**SSID (ssidconfig)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-113">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
            -   [<span data-ttu-id="b92e4-114">**Hex (SSID)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-114">**hex (SSID)**</span></span>](wlan-profileschema-hex-ssid-element.md)
            -   [<span data-ttu-id="b92e4-115">**Name (SSID)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-115">**name (SSID)**</span></span>](wlan-profileschema-name-ssid-element.md)
        -   [<span data-ttu-id="b92e4-116">**nicht Broadcast (ssidconfig)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-116">**nonBroadcast (SSIDConfig)**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md)
    -   [<span data-ttu-id="b92e4-117">**Hotspot2 (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-117">**Hotspot2 (WLANProfile)**</span></span>](wlan-profileschema-hotspot2-element.md)
        -   [<span data-ttu-id="b92e4-118">**Domain Name (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-118">**DomainName (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-domainname-element.md)
        -   [<span data-ttu-id="b92e4-119">**Nairealm (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-119">**NAIRealm (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-nairealm-element.md)
        -   [<span data-ttu-id="b92e4-120">**Network3GPP (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-120">**Network3GPP (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-network3gpp-element.md)
        -   [<span data-ttu-id="b92e4-121">**Roamingconsortium (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-121">**RoamingConsortium (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-roamingconsortium-element.md)
    -   [<span data-ttu-id="b92e4-122">**connectionType (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-122">**connectionType (WLANProfile)**</span></span>](wlan-profileschema-connectiontype-wlanprofile-element.md)
    -   [<span data-ttu-id="b92e4-123">**ConnectionMode (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-123">**connectionMode (WLANProfile)**</span></span>](wlan-profileschema-connectionmode-wlanprofile-element.md)
    -   [<span data-ttu-id="b92e4-124">**autoswitch (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-124">**autoSwitch (WLANProfile)**</span></span>](wlan-profileschema-autoswitch-wlanprofile-element.md)
    -   [<span data-ttu-id="b92e4-125">**MSM (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-125">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
        -   [<span data-ttu-id="b92e4-126">**Konnektivität (MSM)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-126">**connectivity (MSM)**</span></span>](wlan-profileschema-connectivity-msm-element.md)
            -   [<span data-ttu-id="b92e4-127">**phytype (Konnektivität)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-127">**phyType (connectivity)**</span></span>](wlan-profileschema-phytype-connectivity-element.md)
        -   [<span data-ttu-id="b92e4-128">**Sicherheit (MSM)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-128">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
            -   [<span data-ttu-id="b92e4-129">**authencryption (Sicherheit)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-129">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
                -   [<span data-ttu-id="b92e4-130">**Authentifizierung (authencryption)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-130">**authentication (authEncryption)**</span></span>](wlan-profileschema-authentication-authencryption-element.md)
                -   [<span data-ttu-id="b92e4-131">**Verschlüsselung (authencryption)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-131">**encryption (authEncryption)**</span></span>](wlan-profileschema-encryption-authencryption-element.md)
                -   [<span data-ttu-id="b92e4-132">**useonex (authencryption)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-132">**useOneX (authEncryption)**</span></span>](wlan-profileschema-useonex-authencryption-element.md)
                -   [<span data-ttu-id="b92e4-133">**"Fpsmode" (authencryption)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-133">**FIPSMode (authEncryption)**</span></span>](wlan-profileschema-fipsmode-authencryption-element.md)
            -   [<span data-ttu-id="b92e4-134">**sharedkey (Sicherheit)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-134">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
                -   [<span data-ttu-id="b92e4-135">**KeyType (sharedkey)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-135">**keyType (sharedKey)**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)
                -   [<span data-ttu-id="b92e4-136">**geschützt (sharedkey)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-136">**protected (sharedKey)**</span></span>](wlan-profileschema-protected-sharedkey-element.md)
                -   [<span data-ttu-id="b92e4-137">**Keymaterial (sharedkey)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-137">**keyMaterial (sharedKey)**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)
            -   [<span data-ttu-id="b92e4-138">**KeyIndex (Sicherheit)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-138">**keyIndex (security)**</span></span>](wlan-profileschema-keyindex-security-element.md)
            -   [<span data-ttu-id="b92e4-139">**Pmkcachemode (Sicherheit)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-139">**PMKCacheMode (security)**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)
            -   [<span data-ttu-id="b92e4-140">**Pmkcachettl (Sicherheit)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-140">**PMKCacheTTL (security)**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)
            -   [<span data-ttu-id="b92e4-141">**Pmkcachesize (Sicherheit)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-141">**PMKCacheSize (security)**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)
            -   [<span data-ttu-id="b92e4-142">**preauthmode (Sicherheit)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-142">**preAuthMode (security)**</span></span>](wlan-profileschema-preauthmode-security-element.md)
            -   [<span data-ttu-id="b92e4-143">**preauththrottle (Sicherheit)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-143">**preAuthThrottle (security)**</span></span>](wlan-profileschema-preauththrottle-security-element.md)
    -   [<span data-ttu-id="b92e4-144">**IHV (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-144">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
        -   [<span data-ttu-id="b92e4-145">**Ouiheader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-145">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
            -   [<span data-ttu-id="b92e4-146">**OUI (ouiheader)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-146">**OUI (OUIHeader)**</span></span>](wlan-profileschema-oui-ouiheader-element.md)
            -   [<span data-ttu-id="b92e4-147">**Type (ouiheader)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-147">**type (OUIHeader)**</span></span>](wlan-profileschema-type-ouiheader-element.md)
        -   [<span data-ttu-id="b92e4-148">**Konnektivität (IHV)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-148">**connectivity (IHV)**</span></span>](wlan-profileschema-connectivity-ihv-element.md)
        -   [<span data-ttu-id="b92e4-149">**Sicherheit (IHV)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-149">**security (IHV)**</span></span>](wlan-profileschema-security-ihv-element.md)
        -   [<span data-ttu-id="b92e4-150">**usemsonex (IHV)**</span><span class="sxs-lookup"><span data-stu-id="b92e4-150">**useMSOneX (IHV)**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)

 

 



