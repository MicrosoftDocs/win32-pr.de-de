---
description: Enthält eine verkabelte LAN-Richtlinie.
ms.assetid: c06bdbc4-4199-4eec-a22f-684745912970
title: Lanpolicy-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b424a47405aa8f32276019a85902bd51b173cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347477"
---
# <a name="lanpolicy-element"></a><span data-ttu-id="9fff2-103">Lanpolicy-Element</span><span class="sxs-lookup"><span data-stu-id="9fff2-103">LANPolicy Element</span></span>

<span data-ttu-id="9fff2-104">Das lanpolicy-Element enthält eine verkabelte LAN-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="9fff2-104">The LANPolicy element contains a wired LAN policy.</span></span> <span data-ttu-id="9fff2-105">Dieses Element ist das eindeutige root-Element für ein kabelgebundenes Netzwerk Richtlinien Profil.</span><span class="sxs-lookup"><span data-stu-id="9fff2-105">This element is the unique root element for a wired network policy profile.</span></span>

<span data-ttu-id="9fff2-106">Der Ziel Namespace für das **lanpolicy** -Element ist `https://www.microsoft.com/networking/LAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="9fff2-106">The target namespace for the **LANPolicy** element is `https://www.microsoft.com/networking/LAN/policy/v1`.</span></span>

``` syntax
<xs:element name="LANPolicy">
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

## <a name="child-elements"></a><span data-ttu-id="9fff2-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fff2-107">Child elements</span></span>



| <span data-ttu-id="9fff2-108">Element</span><span class="sxs-lookup"><span data-stu-id="9fff2-108">Element</span></span>                                                                           | <span data-ttu-id="9fff2-109">type</span><span class="sxs-lookup"><span data-stu-id="9fff2-109">Type</span></span>                                                     | <span data-ttu-id="9fff2-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9fff2-110">Description</span></span>                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fff2-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9fff2-111">**description**</span></span>](lan-policyschema-description-lanpolicy-element.md)             | [<span data-ttu-id="9fff2-112">**nametype**</span><span class="sxs-lookup"><span data-stu-id="9fff2-112">**nameType**</span></span>](lan-policyschema-nametype-simpletype.md) | <span data-ttu-id="9fff2-113">Enthält die Beschreibung einer kabelgebundenen LAN-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="9fff2-113">Contains the description of a wired LAN policy.</span></span> <br/>                                                                                                                          |
| [<span data-ttu-id="9fff2-114">**enableautoconfig**</span><span class="sxs-lookup"><span data-stu-id="9fff2-114">**enableAutoConfig**</span></span>](lan-policyschema-enableautoconfig-globalflags-element.md) | <span data-ttu-id="9fff2-115">boolean</span><span class="sxs-lookup"><span data-stu-id="9fff2-115">boolean</span></span>                                                  | <span data-ttu-id="9fff2-116">Gibt an, ob Computer den integrierten automatischen Konfigurations Dienst zum Verwalten von Verbindungen mit verkabelten Netzwerken verwenden, die Layer 2-Authentifizierung erfordern (z. b. 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="9fff2-116">Specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span><br/> |
| [<span data-ttu-id="9fff2-117">**globalflags**</span><span class="sxs-lookup"><span data-stu-id="9fff2-117">**globalFlags**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)             |                                                          | <span data-ttu-id="9fff2-118">Enthält die globalen Einstellungen für die automatische Konfiguration von verkabelten Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="9fff2-118">Contains the global settings for the automatic configuration of wired networks.</span></span> <br/>                                                                                          |
| [<span data-ttu-id="9fff2-119">**Benennen**</span><span class="sxs-lookup"><span data-stu-id="9fff2-119">**name**</span></span>](lan-policyschema-name-lanpolicy-element.md)                           | [<span data-ttu-id="9fff2-120">**nametype**</span><span class="sxs-lookup"><span data-stu-id="9fff2-120">**nameType**</span></span>](lan-policyschema-nametype-simpletype.md) | <span data-ttu-id="9fff2-121">Enthält den Namen einer kabelgebundenen LAN-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="9fff2-121">Contains the name of a wired LAN policy.</span></span> <br/>                                                                                                                                 |
| [<span data-ttu-id="9fff2-122">**Profilliste**</span><span class="sxs-lookup"><span data-stu-id="9fff2-122">**profileList**</span></span>](lan-policyschema-profilelist-lanpolicy-element.md)             |                                                          | <span data-ttu-id="9fff2-123">Enthält eine Liste der Profile, die auf Domänen-oder Computer Ebene angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9fff2-123">Contains a list of profiles to be applied at the domain or machine level.</span></span> <br/>                                                                                                |



## <a name="remarks"></a><span data-ttu-id="9fff2-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fff2-124">Remarks</span></span>

<span data-ttu-id="9fff2-125">Informationen zum Anzeigen der Liste der untergeordneten Elemente in einer Struktur ähnlichen Struktur finden Sie unter [LAN- \_ Richtlinien Schema Elemente](lan-policyschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="9fff2-125">To view the list of child elements in a tree-like structure, see [LAN\_policy Schema Elements](lan-policyschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fff2-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fff2-126">Requirements</span></span>



| <span data-ttu-id="9fff2-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fff2-127">Requirement</span></span> | <span data-ttu-id="9fff2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9fff2-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9fff2-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9fff2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9fff2-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fff2-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9fff2-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9fff2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9fff2-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fff2-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




