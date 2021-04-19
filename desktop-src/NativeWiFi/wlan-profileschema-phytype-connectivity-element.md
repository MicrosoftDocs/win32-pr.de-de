---
description: Gibt den 802,11 Wireless LAN-Standard an, der in einem Drahtlos Netzwerk verwendet wird.
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: phytype (Connectivity)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- phyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 71a58e464528136244cec745aed2e59c6fea737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353040"
---
# <a name="phytype-connectivity-element"></a><span data-ttu-id="386b3-103">phytype (Connectivity)-Element</span><span class="sxs-lookup"><span data-stu-id="386b3-103">phyType (connectivity) Element</span></span>

<span data-ttu-id="386b3-104">Das Element "phytype (Connectivity)" gibt den 802,11 Wireless LAN-Standard an, der in einem Drahtlos Netzwerk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="386b3-104">The phyType (connectivity) element specifies the 802.11 wireless LAN standard used on a wireless LAN.</span></span>

<span data-ttu-id="386b3-105">Sie können mehrere **phytype** s angeben.</span><span class="sxs-lookup"><span data-stu-id="386b3-105">You can specify multiple **phyType** s.</span></span> <span data-ttu-id="386b3-106">Wenn kein " **phytype** " angegeben ist, kann das Profil verwendet werden, um eine Verbindung mit einem beliebigen " **phytype**" herzustellen.</span><span class="sxs-lookup"><span data-stu-id="386b3-106">If no **phyType** is specified, the profile can be used to connect to any **phyType**.</span></span> <span data-ttu-id="386b3-107">Der Wert "n" wird nur unter Windows Vista mit Service Pack 1 (SP1) und höheren Versionen des Betriebssystems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="386b3-107">The value "n" is only supported on Windows Vista with Service Pack 1 (SP1) and later versions of the operating system.</span></span>

<span data-ttu-id="386b3-108">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="386b3-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="phyType"
    minOccurs="0"
    maxOccurs="4"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="a"
             />
            <xs:enumeration
                value="b"
             />
            <xs:enumeration
                value="g"
             />
            <xs:enumeration
                value="n"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="386b3-109">Das-Element wird durch das [**konnektivitätselement**](wlan-profileschema-connectivity-msm-element.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="386b3-109">The element is defined by the [**connectivity**](wlan-profileschema-connectivity-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="386b3-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="386b3-110">Requirements</span></span>



| <span data-ttu-id="386b3-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="386b3-111">Requirement</span></span> | <span data-ttu-id="386b3-112">Wert</span><span class="sxs-lookup"><span data-stu-id="386b3-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="386b3-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="386b3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="386b3-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="386b3-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="386b3-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="386b3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="386b3-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="386b3-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="386b3-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="386b3-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="386b3-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="386b3-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="386b3-119">**Stech**</span><span class="sxs-lookup"><span data-stu-id="386b3-119">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

<span data-ttu-id="386b3-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="386b3-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="386b3-121">**Konnektivität (MSM)**</span><span class="sxs-lookup"><span data-stu-id="386b3-121">**connectivity (MSM)**</span></span>](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




