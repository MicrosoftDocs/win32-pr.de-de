---
description: Enthält IHV-bezogene Konnektivitätseinstellungen. Es ist zurzeit nicht implementiert.
ms.assetid: d943e82a-8660-4df7-8f5c-42ed83f17313
title: konnektivitätselement (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectivity
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 257addbcbd721e5930405e3954dcb348f367af93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753752"
---
# <a name="connectivity-ihv-element"></a><span data-ttu-id="ee7c8-104">konnektivitätselement (IHV)</span><span class="sxs-lookup"><span data-stu-id="ee7c8-104">connectivity (IHV) Element</span></span>

<span data-ttu-id="ee7c8-105">Das Element Connectivity (IHV) enthält IHV-bezogene Konnektivitätseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="ee7c8-105">The connectivity (IHV) element contains IHV-related connectivity settings.</span></span> <span data-ttu-id="ee7c8-106">Es ist zurzeit nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ee7c8-106">It is not currently implemented.</span></span>

<span data-ttu-id="ee7c8-107">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ee7c8-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="ee7c8-108">Das-Element wird durch das [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="ee7c8-108">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee7c8-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee7c8-109">Requirements</span></span>



| <span data-ttu-id="ee7c8-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee7c8-110">Requirement</span></span> | <span data-ttu-id="ee7c8-111">Wert</span><span class="sxs-lookup"><span data-stu-id="ee7c8-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ee7c8-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee7c8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ee7c8-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee7c8-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ee7c8-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee7c8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ee7c8-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee7c8-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee7c8-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee7c8-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="ee7c8-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="ee7c8-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ee7c8-118">**IHV**</span><span class="sxs-lookup"><span data-stu-id="ee7c8-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="ee7c8-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="ee7c8-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ee7c8-120">**IHV (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="ee7c8-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




