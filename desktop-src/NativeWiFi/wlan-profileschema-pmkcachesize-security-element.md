---
description: Gibt die Anzahl der Einträge im PMK-Cache auf dem Client an.
ms.assetid: 3a53f7fd-7f12-43d3-94e6-a11bec389a34
title: Pmkcachesize (Security)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheSize
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b21054ddc97c51212ea3a06207617ad85228270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348373"
---
# <a name="pmkcachesize-security-element"></a><span data-ttu-id="4f2d1-103">Pmkcachesize (Security)-Element</span><span class="sxs-lookup"><span data-stu-id="4f2d1-103">PMKCacheSize (security) Element</span></span>

<span data-ttu-id="4f2d1-104">Das pmkcachesize (Security)-Element gibt die Anzahl der Einträge im PMK-Cache auf dem Client an.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-104">The PMKCacheSize (security) element specifies the number of entries in the PMK cache on the client.</span></span> <span data-ttu-id="4f2d1-105">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen [**pmkcachemode**](wlan-profileschema-pmkcachemode-security-element.md) auf "aktiviert" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="4f2d1-106">Wenn **pmkcachemode** aktiviert ist und dieses Element nicht vorhanden ist, wird die Größe des Caches standardmäßig auf 128 Einträge eingestellt.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-106">If **PMKCacheMode** is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span>

<span data-ttu-id="4f2d1-107">Die PMK-Zwischenspeicherung wird in der Spezifikation [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-107">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="4f2d1-108">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheSize"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="255"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="4f2d1-109">Das-Element wird durch das [**Security**](wlan-profileschema-security-msm-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-109">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f2d1-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f2d1-110">Requirements</span></span>



| <span data-ttu-id="4f2d1-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f2d1-111">Requirement</span></span> | <span data-ttu-id="4f2d1-112">Wert</span><span class="sxs-lookup"><span data-stu-id="4f2d1-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4f2d1-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f2d1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4f2d1-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f2d1-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4f2d1-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f2d1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4f2d1-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f2d1-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f2d1-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f2d1-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="4f2d1-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="4f2d1-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4f2d1-119">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="4f2d1-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="4f2d1-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="4f2d1-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4f2d1-121">**Sicherheit (MSM)**</span><span class="sxs-lookup"><span data-stu-id="4f2d1-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




