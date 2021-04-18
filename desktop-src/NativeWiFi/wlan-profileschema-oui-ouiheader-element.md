---
description: Enthält eine hexbinär Datei mit 3 Bytes, die den IHV identifiziert.
ms.assetid: 0b2e73fb-df3a-48c4-b38d-970c37de46eb
title: OUI (ouiheader)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUI
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 49a9cceffb308c64c8d1addf7c257b422751661f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343275"
---
# <a name="oui-ouiheader-element"></a><span data-ttu-id="fa012-103">OUI (ouiheader)-Element</span><span class="sxs-lookup"><span data-stu-id="fa012-103">OUI (OUIHeader) Element</span></span>

<span data-ttu-id="fa012-104">Das OUI (ouiheader)-Element enthält ein 3-Byte-hexBinary, das den IHV identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fa012-104">The OUI (OUIHeader) element contains a 3 byte hexBinary that identifies the IHV.</span></span>

<span data-ttu-id="fa012-105">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fa012-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="OUI">
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:length
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="fa012-106">Das-Element wird durch das [**ouiheader**](wlan-profileschema-ouiheader-ihv-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="fa012-106">The element is defined by the [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa012-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa012-107">Requirements</span></span>



| <span data-ttu-id="fa012-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa012-108">Requirement</span></span> | <span data-ttu-id="fa012-109">Wert</span><span class="sxs-lookup"><span data-stu-id="fa012-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fa012-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa012-110">Minimum supported client</span></span><br/> | <span data-ttu-id="fa012-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa012-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fa012-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa012-112">Minimum supported server</span></span><br/> | <span data-ttu-id="fa012-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa012-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa012-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa012-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="fa012-115">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="fa012-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fa012-116">**Ouiheader**</span><span class="sxs-lookup"><span data-stu-id="fa012-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

<span data-ttu-id="fa012-117">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="fa012-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fa012-118">**Ouiheader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="fa012-118">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




