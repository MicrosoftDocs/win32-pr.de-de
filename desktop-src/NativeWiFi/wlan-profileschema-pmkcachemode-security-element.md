---
description: Gibt an, ob die PMK-Zwischenspeicherung verwendet wird.
ms.assetid: 5650c893-6047-4e99-a2be-22722d6a809a
title: Pmkcachemode (Security)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 609660d6f3161cbaaa5e0505daf9c6b9180b6c32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128848"
---
# <a name="pmkcachemode-security-element"></a><span data-ttu-id="49d5a-103">Pmkcachemode (Security)-Element</span><span class="sxs-lookup"><span data-stu-id="49d5a-103">PMKCacheMode (security) Element</span></span>

<span data-ttu-id="49d5a-104">Das pmkcachemode (Security)-Element gibt an, ob die PMK-Zwischenspeicherung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49d5a-104">The PMKCacheMode (security) element indicates whether PMK caching will be used.</span></span> <span data-ttu-id="49d5a-105">Dieses Element ist nur für WPA2-definierte Netzwerke gültig.</span><span class="sxs-lookup"><span data-stu-id="49d5a-105">This element is valid only for WPA2-defined networks.</span></span> <span data-ttu-id="49d5a-106">Die PMK-Zwischenspeicherung wird in der Spezifikation [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="49d5a-106">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="49d5a-107">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="49d5a-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheMode"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="disabled"
             />
            <xs:enumeration
                value="enabled"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="49d5a-108">Das-Element wird durch das [**Security**](wlan-profileschema-security-msm-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="49d5a-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="49d5a-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49d5a-109">Requirements</span></span>



| <span data-ttu-id="49d5a-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49d5a-110">Requirement</span></span> | <span data-ttu-id="49d5a-111">Wert</span><span class="sxs-lookup"><span data-stu-id="49d5a-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49d5a-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49d5a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="49d5a-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49d5a-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="49d5a-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49d5a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="49d5a-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49d5a-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49d5a-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49d5a-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="49d5a-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="49d5a-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="49d5a-118">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="49d5a-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="49d5a-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="49d5a-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="49d5a-120">**Sicherheit (MSM)**</span><span class="sxs-lookup"><span data-stu-id="49d5a-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




