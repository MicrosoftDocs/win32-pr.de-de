---
description: Enthält Sicherheitseinstellungen für verkabelte Netzwerke.
ms.assetid: 08470cf4-3722-4cb9-9877-13eca2f7d04e
title: Security (MSM)-Element (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2bd052679f207cd0778f212a73663d4dfd8ce165
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106357290"
---
# <a name="security-msm-element-lan_policy"></a><span data-ttu-id="2519f-103">Security (MSM)-Element (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="2519f-103">Security (MSM) Element (LAN_policy)</span></span>

<span data-ttu-id="2519f-104">Das Security (MSM)-Element enthält Sicherheitseinstellungen für verkabelte Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="2519f-104">The security (MSM) element contains security settings for wired networks.</span></span> <span data-ttu-id="2519f-105">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="2519f-105">This element is optional.</span></span>

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OneXEnforced"
                type="boolean"
             />
            <xs:element name="OneXEnabled"
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

<span data-ttu-id="2519f-106">Das **Security** -Element wird durch das [**MSM**](lan-profileschema-msm-lanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="2519f-106">The **security** element is defined by the [**MSM**](lan-profileschema-msm-lanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2519f-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2519f-107">Child elements</span></span>



| <span data-ttu-id="2519f-108">Element</span><span class="sxs-lookup"><span data-stu-id="2519f-108">Element</span></span>                                                                 | <span data-ttu-id="2519f-109">type</span><span class="sxs-lookup"><span data-stu-id="2519f-109">Type</span></span>    | <span data-ttu-id="2519f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2519f-110">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2519f-111">**Onexaktiviert**</span><span class="sxs-lookup"><span data-stu-id="2519f-111">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="2519f-112">boolean</span><span class="sxs-lookup"><span data-stu-id="2519f-112">boolean</span></span> | <span data-ttu-id="2519f-113">Gibt an, ob der Dienst für die automatische Konfiguration von Kabel Netzwerken mithilfe von 802.1 x eine Port Authentifizierung durchführen soll.</span><span class="sxs-lookup"><span data-stu-id="2519f-113">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <br/>      |
| [<span data-ttu-id="2519f-114">**Onexerzwungen**</span><span class="sxs-lookup"><span data-stu-id="2519f-114">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="2519f-115">boolean</span><span class="sxs-lookup"><span data-stu-id="2519f-115">boolean</span></span> | <span data-ttu-id="2519f-116">Gibt an, ob für den automatischen Konfigurations Dienst für verkabelte Netzwerke die Verwendung von 802.1 x für die Port Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2519f-116">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="2519f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2519f-117">Requirements</span></span>



| <span data-ttu-id="2519f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2519f-118">Requirement</span></span> | <span data-ttu-id="2519f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2519f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2519f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2519f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2519f-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2519f-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2519f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2519f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2519f-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2519f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2519f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2519f-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="2519f-125">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="2519f-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2519f-126">**MSM**</span><span class="sxs-lookup"><span data-stu-id="2519f-126">**MSM**</span></span>](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

<span data-ttu-id="2519f-127">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="2519f-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2519f-128">**MSM (lanprofile)**</span><span class="sxs-lookup"><span data-stu-id="2519f-128">**MSM (LANProfile)**</span></span>](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 




