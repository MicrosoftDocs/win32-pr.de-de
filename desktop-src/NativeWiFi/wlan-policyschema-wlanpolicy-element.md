---
description: Enthält eine Drahtlos-LAN-Richtlinie.
ms.assetid: 16ffb682-f88b-4ca1-a902-d2db5e347975
title: Wlanpolicy-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ec26a3cab15014deabca4e9332c1fbef7a788b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130433"
---
# <a name="wlanpolicy-element"></a><span data-ttu-id="da199-103">Wlanpolicy-Element</span><span class="sxs-lookup"><span data-stu-id="da199-103">WLANPolicy Element</span></span>

<span data-ttu-id="da199-104">Das **wlanpolicy** -Element enthält eine Drahtlos-LAN-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="da199-104">The **WLANPolicy** element contains a wireless LAN policy.</span></span> <span data-ttu-id="da199-105">Dieses Element ist das eindeutige root-Element für ein drahtlos Richtlinien Profil.</span><span class="sxs-lookup"><span data-stu-id="da199-105">This element is the unique root element for a wireless policy profile.</span></span>

<span data-ttu-id="da199-106">Der Ziel Namespace für das **wlanpolicy** -Element ist `https://www.microsoft.com/networking/WLAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="da199-106">The target namespace for the **WLANPolicy** element is `https://www.microsoft.com/networking/WLAN/policy/v1`.</span></span>

``` syntax
<xs:element name="WLANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
                         />
                        <xs:element name="showDeniedNetwork"
                            type="boolean"
                         />
                        <xs:element name="allowEveryoneToCreateAllUserProfiles"
                            type="boolean"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="networkFilter"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="allowList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
                                     />
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="blockList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
                                     />
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="denyAllIBSS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:element name="denyAllESS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="profileList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="da199-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da199-107">Child elements</span></span>



| <span data-ttu-id="da199-108">Element</span><span class="sxs-lookup"><span data-stu-id="da199-108">Element</span></span>                                                                                                                    | <span data-ttu-id="da199-109">type</span><span class="sxs-lookup"><span data-stu-id="da199-109">Type</span></span>                                                                     | <span data-ttu-id="da199-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da199-110">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da199-111">**"Zuweisung von" "" "".**</span><span class="sxs-lookup"><span data-stu-id="da199-111">**allowEveryoneToCreateAllUserProfiles**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | <span data-ttu-id="da199-112">boolean</span><span class="sxs-lookup"><span data-stu-id="da199-112">boolean</span></span>                                                                  | <span data-ttu-id="da199-113">Gibt an, ob ein Benutzer ein Profil für alle Benutzer erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="da199-113">Specifies whether any user can create an all-user profile.</span></span> <br/>                                                               |
| [<span data-ttu-id="da199-114">**Zulassungs**</span><span class="sxs-lookup"><span data-stu-id="da199-114">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)                                                     |                                                                          | <span data-ttu-id="da199-115">Die Liste der Drahtlos-LAN-Netzwerke, denen jeder Computer eine Verbindung herstellen darf.</span><span class="sxs-lookup"><span data-stu-id="da199-115">The list of wireless LAN networks to which any machine must be allowed to connect.</span></span> <br/>                                       |
| [<span data-ttu-id="da199-116">**Blocklisten**</span><span class="sxs-lookup"><span data-stu-id="da199-116">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)                                                     |                                                                          | <span data-ttu-id="da199-117">Die Liste der Drahtlos-LAN-Netzwerke, mit denen ein Computer keine Verbindung herstellen darf.</span><span class="sxs-lookup"><span data-stu-id="da199-117">The list of wireless LAN networks to which a machine must not connect.</span></span><br/>                                                    |
| [<span data-ttu-id="da199-118">**denyalless**</span><span class="sxs-lookup"><span data-stu-id="da199-118">**denyAllESS**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)                                                   | <span data-ttu-id="da199-119">boolean</span><span class="sxs-lookup"><span data-stu-id="da199-119">boolean</span></span>                                                                  | <span data-ttu-id="da199-120">Gibt an, ob der Zugriff auf alle Infrastruktur Netzwerke blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="da199-120">Specifies if access to all infrastructure networks is blocked.</span></span> <br/>                                                           |
| [<span data-ttu-id="da199-121">**denyallibss**</span><span class="sxs-lookup"><span data-stu-id="da199-121">**denyAllIBSS**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md)                                                 | <span data-ttu-id="da199-122">boolean</span><span class="sxs-lookup"><span data-stu-id="da199-122">boolean</span></span>                                                                  | <span data-ttu-id="da199-123">Gibt an, ob der Zugriff auf alle Ad-hoc-Netzwerke blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="da199-123">Specifies if access to all ad-hoc networks is blocked.</span></span> <br/>                                                                   |
| [<span data-ttu-id="da199-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da199-124">**description**</span></span>](wlan-policyschema-description-wlanpolicy-element.md)                                                    | [<span data-ttu-id="da199-125">**nametype**</span><span class="sxs-lookup"><span data-stu-id="da199-125">**nameType**</span></span>](wlan-policyschema-nametype-simpletype.md)                | <span data-ttu-id="da199-126">Die Beschreibung einer Drahtlos-LAN-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="da199-126">The description of a wireless LAN policy.</span></span> <br/>                                                                                |
| [<span data-ttu-id="da199-127">**enableautoconfig**</span><span class="sxs-lookup"><span data-stu-id="da199-127">**enableAutoConfig**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | <span data-ttu-id="da199-128">boolean</span><span class="sxs-lookup"><span data-stu-id="da199-128">boolean</span></span>                                                                  | <span data-ttu-id="da199-129">Gibt an, ob Computer den integrierten automatischen Konfigurations Dienst (AutoConfig) zum Verwalten von Drahtlos Verbindungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="da199-129">Specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <br/> |
| [<span data-ttu-id="da199-130">**globalflags**</span><span class="sxs-lookup"><span data-stu-id="da199-130">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)                                                    |                                                                          | <span data-ttu-id="da199-131">Enthält die globalen Einstellungen für das Auto Configuration Module (ACM).</span><span class="sxs-lookup"><span data-stu-id="da199-131">Contains the global settings for the Auto Configuration Module (ACM).</span></span> <br/>                                                    |
| [<span data-ttu-id="da199-132">**Benennen**</span><span class="sxs-lookup"><span data-stu-id="da199-132">**name**</span></span>](wlan-policyschema-name-wlanpolicy-element.md)                                                                  | [<span data-ttu-id="da199-133">**nametype**</span><span class="sxs-lookup"><span data-stu-id="da199-133">**nameType**</span></span>](wlan-policyschema-nametype-simpletype.md)                | <span data-ttu-id="da199-134">Der Name einer Drahtlos-LAN-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="da199-134">The name of a wireless LAN policy.</span></span> <br/>                                                                                       |
| [<span data-ttu-id="da199-135">**Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="da199-135">**network**</span></span>](wlan-policyschema-network-allowlist-element.md)                                                             | [<span data-ttu-id="da199-136">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="da199-136">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="da199-137">Ein zulässiges Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="da199-137">An allowed network.</span></span> <br/>                                                                                                      |
| [<span data-ttu-id="da199-138">**Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="da199-138">**network**</span></span>](wlan-policyschema-network-blocklist-element.md)                                                             | [<span data-ttu-id="da199-139">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="da199-139">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="da199-140">Ein blockiertes Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="da199-140">A blocked network.</span></span> <br/>                                                                                                       |
| [<span data-ttu-id="da199-141">**Network Filter**</span><span class="sxs-lookup"><span data-stu-id="da199-141">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)                                                |                                                                          | <span data-ttu-id="da199-142">Die Liste der zugelassenen und verweigerten Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="da199-142">The list of allowed and denied networks.</span></span><br/>                                                                                  |
| [<span data-ttu-id="da199-143">**Profilliste**</span><span class="sxs-lookup"><span data-stu-id="da199-143">**profileList**</span></span>](wlan-policyschema-profilelist-wlanpolicy-element.md)                                                    |                                                                          | <span data-ttu-id="da199-144">Enthält eine Liste der Profile, die auf Domänen-oder Computer Ebene angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="da199-144">Contains a list of profiles to be applied at the domain or machine level.</span></span> <br/>                                                |
| [<span data-ttu-id="da199-145">**showdeniednetwork**</span><span class="sxs-lookup"><span data-stu-id="da199-145">**showDeniedNetwork**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | <span data-ttu-id="da199-146">boolean</span><span class="sxs-lookup"><span data-stu-id="da199-146">boolean</span></span>                                                                  | <span data-ttu-id="da199-147">Gibt an, ob abgelehnte Netzwerke im Assistenten **zum Herstellen einer Verbindung mit einem Netzwerk** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="da199-147">Specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <br/>                                         |



## <a name="remarks"></a><span data-ttu-id="da199-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da199-148">Remarks</span></span>

<span data-ttu-id="da199-149">Informationen zum Anzeigen der Liste der untergeordneten Elemente in einer Struktur ähnlichen Struktur finden Sie unter [WLAN- \_ Richtlinien Schema Elemente](wlan-policyschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="da199-149">To view the list of child elements in a tree-like structure, see [WLAN\_policy Schema Elements](wlan-policyschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da199-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da199-150">Requirements</span></span>



| <span data-ttu-id="da199-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da199-151">Requirement</span></span> | <span data-ttu-id="da199-152">Wert</span><span class="sxs-lookup"><span data-stu-id="da199-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="da199-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da199-153">Minimum supported client</span></span><br/> | <span data-ttu-id="da199-154">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da199-154">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="da199-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da199-155">Minimum supported server</span></span><br/> | <span data-ttu-id="da199-156">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da199-156">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




