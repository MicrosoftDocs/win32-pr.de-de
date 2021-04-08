---
description: Enthält eine 1-Byte-hexbinär Datei, die verwendet wird, um zwischen NICs zu unterscheiden, die vom gleichen IHV erstellt werden.
ms.assetid: fd6bae3d-27a8-4bff-9340-b444312b8216
title: Type (ouiheader)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 12637e5a70409166e5a31aa0fc98f4df1b9f6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866028"
---
# <a name="type-ouiheader-element"></a><span data-ttu-id="2c680-103">Type (ouiheader)-Element</span><span class="sxs-lookup"><span data-stu-id="2c680-103">type (OUIHeader) Element</span></span>

<span data-ttu-id="2c680-104">Das "Type (ouiheader)"-Element enthält eine 1-Byte-hexbinär Datei, die verwendet wird, um zwischen NICs zu unterscheiden, die von derselben IHV-Datei</span><span class="sxs-lookup"><span data-stu-id="2c680-104">The type (OUIHeader) element contains a 1-byte hexBinary that is used to differentiate between NICs made by the same IHV.</span></span>

<span data-ttu-id="2c680-105">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2c680-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="type">
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:length
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="2c680-106">Das-Element wird durch das [**ouiheader**](wlan-profileschema-ouiheader-ihv-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="2c680-106">The element is defined by the [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c680-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c680-107">Requirements</span></span>



| <span data-ttu-id="2c680-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c680-108">Requirement</span></span> | <span data-ttu-id="2c680-109">Wert</span><span class="sxs-lookup"><span data-stu-id="2c680-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2c680-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c680-110">Minimum supported client</span></span><br/> | <span data-ttu-id="2c680-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c680-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2c680-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c680-112">Minimum supported server</span></span><br/> | <span data-ttu-id="2c680-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c680-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2c680-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c680-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="2c680-115">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="2c680-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2c680-116">**Ouiheader**</span><span class="sxs-lookup"><span data-stu-id="2c680-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

<span data-ttu-id="2c680-117">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="2c680-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2c680-118">**Ouiheader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="2c680-118">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




