---
description: Enthält die globalen Einstellungen für das Auto Configuration Module (ACM).
ms.assetid: fb2b96d0-38cc-44fe-a82a-97e73b6a8f2a
title: globalflags-Element (wlanpolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 97d0b8ee90407efd94ac46cc1df6b084b9dcc54d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530092"
---
# <a name="globalflags-wlanpolicy-element"></a><span data-ttu-id="53afb-103">globalflags-Element (wlanpolicy)</span><span class="sxs-lookup"><span data-stu-id="53afb-103">globalFlags (WLANPolicy) Element</span></span>

<span data-ttu-id="53afb-104">Das globalflags-Element (wlanpolicy) enthält die globalen Einstellungen für das Auto Configuration Module (ACM).</span><span class="sxs-lookup"><span data-stu-id="53afb-104">The globalFlags (WLANPolicy) element contains the global settings for the Auto Configuration Module (ACM).</span></span> <span data-ttu-id="53afb-105">Dieses Element ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="53afb-105">This element is mandatory.</span></span>

``` syntax
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
```

<span data-ttu-id="53afb-106">Das **globalflags** -Element wird durch das [**wlanpolicy**](wlan-policyschema-wlanpolicy-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="53afb-106">The **globalFlags** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="53afb-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53afb-107">Child elements</span></span>



| <span data-ttu-id="53afb-108">Element</span><span class="sxs-lookup"><span data-stu-id="53afb-108">Element</span></span>                                                                                                                    | <span data-ttu-id="53afb-109">type</span><span class="sxs-lookup"><span data-stu-id="53afb-109">Type</span></span>    | <span data-ttu-id="53afb-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53afb-110">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53afb-111">**"Zuweisung von" "" "".**</span><span class="sxs-lookup"><span data-stu-id="53afb-111">**allowEveryoneToCreateAllUserProfiles**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | <span data-ttu-id="53afb-112">boolean</span><span class="sxs-lookup"><span data-stu-id="53afb-112">boolean</span></span> | <span data-ttu-id="53afb-113">Gibt an, ob ein Benutzer ein Profil für alle Benutzer erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="53afb-113">Specifies whether any user can create an all-user profile.</span></span> <br/>                                                               |
| [<span data-ttu-id="53afb-114">**enableautoconfig**</span><span class="sxs-lookup"><span data-stu-id="53afb-114">**enableAutoConfig**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | <span data-ttu-id="53afb-115">boolean</span><span class="sxs-lookup"><span data-stu-id="53afb-115">boolean</span></span> | <span data-ttu-id="53afb-116">Gibt an, ob Computer den integrierten automatischen Konfigurations Dienst (AutoConfig) zum Verwalten von Drahtlos Verbindungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="53afb-116">Specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <br/> |
| [<span data-ttu-id="53afb-117">**showdeniednetwork**</span><span class="sxs-lookup"><span data-stu-id="53afb-117">**showDeniedNetwork**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | <span data-ttu-id="53afb-118">boolean</span><span class="sxs-lookup"><span data-stu-id="53afb-118">boolean</span></span> | <span data-ttu-id="53afb-119">Gibt an, ob abgelehnte Netzwerke im Assistenten **zum Herstellen einer Verbindung mit einem Netzwerk** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="53afb-119">Specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <br/>                                         |



## <a name="requirements"></a><span data-ttu-id="53afb-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53afb-120">Requirements</span></span>



| <span data-ttu-id="53afb-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53afb-121">Requirement</span></span> | <span data-ttu-id="53afb-122">Wert</span><span class="sxs-lookup"><span data-stu-id="53afb-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53afb-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53afb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="53afb-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53afb-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53afb-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53afb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="53afb-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53afb-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53afb-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53afb-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="53afb-128">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="53afb-128">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="53afb-129">**Wlanpolicy**</span><span class="sxs-lookup"><span data-stu-id="53afb-129">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="53afb-130">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="53afb-130">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="53afb-131">**Wlanpolicy**</span><span class="sxs-lookup"><span data-stu-id="53afb-131">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




