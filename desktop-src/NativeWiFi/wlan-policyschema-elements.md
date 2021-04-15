---
description: Ein System eigenes WLAN-Richtlinien Profil besteht aus den folgenden Schema Elementen.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: Schema Elemente WLAN_policy
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8346aab6aba209933b20790cf3747d5c0944f972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525763"
---
# <a name="wlan_policy-schema-elements"></a><span data-ttu-id="b6031-103">Schema Elemente für WLAN- \_ Richtlinien</span><span class="sxs-lookup"><span data-stu-id="b6031-103">WLAN\_policy Schema Elements</span></span>

<span data-ttu-id="b6031-104">Ein System eigenes WLAN-Richtlinien Profil besteht aus den folgenden Schema Elementen.</span><span class="sxs-lookup"><span data-stu-id="b6031-104">A Native Wifi wireless LAN (WLAN) policy profile is composed of the following schema elements.</span></span> <span data-ttu-id="b6031-105">Alle benannten Elemente befinden sich im-Namespace `https://www.microsoft.com/networking/WLAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="b6031-105">All of the named elements are in the namespace `https://www.microsoft.com/networking/WLAN/policy/v1`.</span></span>

<span data-ttu-id="b6031-106">In der folgenden Liste werden die definierten Elemente in der Reihenfolge angezeigt, in der die Elemente in einem Profil angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b6031-106">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="b6031-107">Die Reihenfolge der Elemente wird erzwungen.</span><span class="sxs-lookup"><span data-stu-id="b6031-107">The ordering of elements is enforced.</span></span> <span data-ttu-id="b6031-108">Nicht alle Elemente befinden sich in jedem Profil, da einige Elemente optional sind.</span><span class="sxs-lookup"><span data-stu-id="b6031-108">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="b6031-109">In dieser Liste werden nicht alle möglichen Elemente angezeigt, die in einem Profil angezeigt werden können, da Elemente in **xs: beliebige** Einfügepunkte hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="b6031-109">This list does not show all possible elements that can appear in a profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="b6031-110">**Wlanpolicy**</span><span class="sxs-lookup"><span data-stu-id="b6031-110">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
    -   [<span data-ttu-id="b6031-111">**Name (wlanpolicy)**</span><span class="sxs-lookup"><span data-stu-id="b6031-111">**name (WLANPolicy)**</span></span>](wlan-policyschema-name-wlanpolicy-element.md)
    -   [<span data-ttu-id="b6031-112">**Beschreibung (wlanpolicy)**</span><span class="sxs-lookup"><span data-stu-id="b6031-112">**description (WLANPolicy)**</span></span>](wlan-policyschema-description-wlanpolicy-element.md)
    -   [<span data-ttu-id="b6031-113">**globalflags (wlanpolicy)**</span><span class="sxs-lookup"><span data-stu-id="b6031-113">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [<span data-ttu-id="b6031-114">**enableautoconfig (globalflags)**</span><span class="sxs-lookup"><span data-stu-id="b6031-114">**enableAutoConfig (globalFlags)**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [<span data-ttu-id="b6031-115">**showdeniednetwork (globalflags)**</span><span class="sxs-lookup"><span data-stu-id="b6031-115">**showDeniedNetwork (globalFlags)**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [<span data-ttu-id="b6031-116">**' zugweveryonetoken ' (globalflags)**</span><span class="sxs-lookup"><span data-stu-id="b6031-116">**allowEveryoneToCreateAllUserProfiles (globalFlags)**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [<span data-ttu-id="b6031-117">**Network Filter (wlanpolicy)**</span><span class="sxs-lookup"><span data-stu-id="b6031-117">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [<span data-ttu-id="b6031-118">**AllowList (NetworkFilter)**</span><span class="sxs-lookup"><span data-stu-id="b6031-118">**allowList (networkFilter)**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [<span data-ttu-id="b6031-119">**Netzwerk (AllowList)**</span><span class="sxs-lookup"><span data-stu-id="b6031-119">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
                -   [<span data-ttu-id="b6031-120">**Network Name (networkitemtype)**</span><span class="sxs-lookup"><span data-stu-id="b6031-120">**networkName (networkItemType)**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [<span data-ttu-id="b6031-121">**NetworkType (networkitemtype)**</span><span class="sxs-lookup"><span data-stu-id="b6031-121">**networkType (networkItemType)**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [<span data-ttu-id="b6031-122">**blocklist (NetworkFilter)**</span><span class="sxs-lookup"><span data-stu-id="b6031-122">**blockList (networkFilter)**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [<span data-ttu-id="b6031-123">**Netzwerk (blocklist)**</span><span class="sxs-lookup"><span data-stu-id="b6031-123">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
                -   [<span data-ttu-id="b6031-124">**Network Name (networkitemtype)**</span><span class="sxs-lookup"><span data-stu-id="b6031-124">**networkName (networkItemType)**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [<span data-ttu-id="b6031-125">**NetworkType (networkitemtype)**</span><span class="sxs-lookup"><span data-stu-id="b6031-125">**networkType (networkItemType)**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [<span data-ttu-id="b6031-126">**denyallibss (NetworkFilter)**</span><span class="sxs-lookup"><span data-stu-id="b6031-126">**denyAllIBSS (networkFilter)**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [<span data-ttu-id="b6031-127">**denyalless (NetworkFilter)**</span><span class="sxs-lookup"><span data-stu-id="b6031-127">**denyAllESS (networkFilter)**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [<span data-ttu-id="b6031-128">**ProfileList (wlanpolicy)**</span><span class="sxs-lookup"><span data-stu-id="b6031-128">**profileList (WLANPolicy)**</span></span>](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



