---
description: Definiert die Liste der zulässigen und verweigerten Netzwerke für Computer.
ms.assetid: 21502c97-36a4-4cd6-9dd0-ee44c4cc522f
title: Network Filter (wlanpolicy)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkFilter
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d78a23ba1a456f1ad45745fcc25580c27de148c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353910"
---
# <a name="networkfilter-wlanpolicy-element"></a><span data-ttu-id="9fe63-103">Network Filter (wlanpolicy)-Element</span><span class="sxs-lookup"><span data-stu-id="9fe63-103">networkFilter (WLANPolicy) Element</span></span>

<span data-ttu-id="9fe63-104">Das NetworkFilter (wlanpolicy)-Element definiert die Liste der zulässigen und verweigerten Netzwerke für Computer.</span><span class="sxs-lookup"><span data-stu-id="9fe63-104">The networkFilter (WLANPolicy) element defines the list of allowed and denied networks for machines.</span></span>

``` syntax
<xs:element name="networkFilter">
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
```

<span data-ttu-id="9fe63-105">Das **NetworkFilter** -Element wird durch das [**wlanpolicy**](wlan-policyschema-wlanpolicy-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="9fe63-105">The **networkFilter** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9fe63-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fe63-106">Child elements</span></span>



| <span data-ttu-id="9fe63-107">Element</span><span class="sxs-lookup"><span data-stu-id="9fe63-107">Element</span></span>                                                                    | <span data-ttu-id="9fe63-108">type</span><span class="sxs-lookup"><span data-stu-id="9fe63-108">Type</span></span>                                                                     | <span data-ttu-id="9fe63-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9fe63-109">Description</span></span>                                                                                    |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fe63-110">**Zulassungs**</span><span class="sxs-lookup"><span data-stu-id="9fe63-110">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)     |                                                                          | <span data-ttu-id="9fe63-111">Die Liste der Drahtlos-LAN-Netzwerke, denen jeder Computer eine Verbindung herstellen darf.</span><span class="sxs-lookup"><span data-stu-id="9fe63-111">The list of wireless LAN networks to which any machine must be allowed to connect.</span></span> <br/> |
| [<span data-ttu-id="9fe63-112">**Blocklisten**</span><span class="sxs-lookup"><span data-stu-id="9fe63-112">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)     |                                                                          | <span data-ttu-id="9fe63-113">Die Liste der Drahtlos-LAN-Netzwerke, mit denen ein Computer keine Verbindung herstellen darf.</span><span class="sxs-lookup"><span data-stu-id="9fe63-113">The list of wireless LAN networks to which a machine must not connect.</span></span><br/>              |
| [<span data-ttu-id="9fe63-114">**denyalless**</span><span class="sxs-lookup"><span data-stu-id="9fe63-114">**denyAllESS**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)   | <span data-ttu-id="9fe63-115">boolean</span><span class="sxs-lookup"><span data-stu-id="9fe63-115">boolean</span></span>                                                                  | <span data-ttu-id="9fe63-116">Gibt an, ob der Zugriff auf alle Infrastruktur Netzwerke blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="9fe63-116">Specifies if access to all infrastructure networks is blocked.</span></span> <br/>                     |
| [<span data-ttu-id="9fe63-117">**denyallibss**</span><span class="sxs-lookup"><span data-stu-id="9fe63-117">**denyAllIBSS**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md) | <span data-ttu-id="9fe63-118">boolean</span><span class="sxs-lookup"><span data-stu-id="9fe63-118">boolean</span></span>                                                                  | <span data-ttu-id="9fe63-119">Gibt an, ob der Zugriff auf alle Ad-hoc-Netzwerke blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="9fe63-119">Specifies if access to all ad-hoc networks is blocked.</span></span> <br/>                             |
| [<span data-ttu-id="9fe63-120">**Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="9fe63-120">**network**</span></span>](wlan-policyschema-network-allowlist-element.md)             | [<span data-ttu-id="9fe63-121">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="9fe63-121">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="9fe63-122">Ein zulässiges Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="9fe63-122">An allowed network.</span></span> <br/>                                                                |
| [<span data-ttu-id="9fe63-123">**Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="9fe63-123">**network**</span></span>](wlan-policyschema-network-blocklist-element.md)             | [<span data-ttu-id="9fe63-124">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="9fe63-124">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="9fe63-125">Ein blockiertes Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="9fe63-125">A blocked network.</span></span> <br/>                                                                 |



## <a name="requirements"></a><span data-ttu-id="9fe63-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fe63-126">Requirements</span></span>



| <span data-ttu-id="9fe63-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fe63-127">Requirement</span></span> | <span data-ttu-id="9fe63-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9fe63-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9fe63-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9fe63-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9fe63-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fe63-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9fe63-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9fe63-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9fe63-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fe63-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9fe63-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fe63-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="9fe63-134">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="9fe63-134">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9fe63-135">**Wlanpolicy**</span><span class="sxs-lookup"><span data-stu-id="9fe63-135">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="9fe63-136">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="9fe63-136">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9fe63-137">**Wlanpolicy**</span><span class="sxs-lookup"><span data-stu-id="9fe63-137">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




