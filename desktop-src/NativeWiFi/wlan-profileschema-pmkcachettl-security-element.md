---
description: Gibt die Zeitdauer in Minuten an, die ein PMK-Cache aufbewahrt wird.
ms.assetid: d9e3b839-48f6-490c-ab83-067368cdcca2
title: Pmkcachettl (Security)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheTTL
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bdfe0edb163dc2bc9766ba8562defb026bbe21fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340181"
---
# <a name="pmkcachettl-security-element"></a><span data-ttu-id="75628-103">Pmkcachettl (Security)-Element</span><span class="sxs-lookup"><span data-stu-id="75628-103">PMKCacheTTL (security) Element</span></span>

<span data-ttu-id="75628-104">Das Element pmkcachettl (Security) gibt die Zeitspanne in Minuten an, die ein PMK-Cache aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="75628-104">The PMKCacheTTL (security) element indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="75628-105">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen [**pmkcachemode**](wlan-profileschema-pmkcachemode-security-element.md) auf "aktiviert" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="75628-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span>

<span data-ttu-id="75628-106">Die PMK-Zwischenspeicherung wird in der Spezifikation [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="75628-106">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="75628-107">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="75628-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheTTL"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="5"
             />
            <xs:maxInclusive
                value="1440"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="75628-108">Das-Element wird durch das [**Security**](wlan-profileschema-security-msm-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="75628-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="75628-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75628-109">Requirements</span></span>



| <span data-ttu-id="75628-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75628-110">Requirement</span></span> | <span data-ttu-id="75628-111">Wert</span><span class="sxs-lookup"><span data-stu-id="75628-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="75628-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75628-112">Minimum supported client</span></span><br/> | <span data-ttu-id="75628-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75628-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="75628-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75628-114">Minimum supported server</span></span><br/> | <span data-ttu-id="75628-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75628-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75628-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75628-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="75628-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="75628-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="75628-118">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="75628-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="75628-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="75628-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="75628-120">**Sicherheit (MSM)**</span><span class="sxs-lookup"><span data-stu-id="75628-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




