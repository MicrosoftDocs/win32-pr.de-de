---
description: Identifiziert den IHV.
ms.assetid: a99c231c-afd7-44e6-81af-3d49ffef8714
title: Ouiheader (IHV)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUIHeader
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a31feb123e31489c751b7844e06d5c344278778e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347140"
---
# <a name="ouiheader-ihv-element"></a><span data-ttu-id="de372-103">Ouiheader (IHV)-Element</span><span class="sxs-lookup"><span data-stu-id="de372-103">OUIHeader (IHV) Element</span></span>

<span data-ttu-id="de372-104">Das ouiheader (IHV)-Element identifiziert den IHV.</span><span class="sxs-lookup"><span data-stu-id="de372-104">The OUIHeader (IHV) element identifies the IHV.</span></span>

<span data-ttu-id="de372-105">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="de372-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="OUIHeader">
    <xs:complexType>
        <xs:sequence>
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

<span data-ttu-id="de372-106">Das-Element wird durch das [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="de372-106">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="de372-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="de372-107">Child elements</span></span>



| <span data-ttu-id="de372-108">Element</span><span class="sxs-lookup"><span data-stu-id="de372-108">Element</span></span>                                                   | <span data-ttu-id="de372-109">type</span><span class="sxs-lookup"><span data-stu-id="de372-109">Type</span></span> | <span data-ttu-id="de372-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de372-110">Description</span></span>                                                                                |
|-----------------------------------------------------------|------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de372-111">**Ische**</span><span class="sxs-lookup"><span data-stu-id="de372-111">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)   |      | <span data-ttu-id="de372-112">Enthält eine hexbinär Datei mit 3 Bytes, die den IHV identifiziert.</span><span class="sxs-lookup"><span data-stu-id="de372-112">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/>                            |
| [<span data-ttu-id="de372-113">**Sorte**</span><span class="sxs-lookup"><span data-stu-id="de372-113">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md) |      | <span data-ttu-id="de372-114">Enthält eine hexbinär Datei mit 1 Byte, die zur Unterscheidung von NICs durch denselben IHV verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="de372-114">Contains a 1 byte hexBinary that is used to differentiate NICs by the same IHV.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="de372-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de372-115">Requirements</span></span>



| <span data-ttu-id="de372-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de372-116">Requirement</span></span> | <span data-ttu-id="de372-117">Wert</span><span class="sxs-lookup"><span data-stu-id="de372-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="de372-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de372-118">Minimum supported client</span></span><br/> | <span data-ttu-id="de372-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de372-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="de372-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de372-120">Minimum supported server</span></span><br/> | <span data-ttu-id="de372-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de372-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de372-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de372-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="de372-123">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="de372-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="de372-124">**IHV**</span><span class="sxs-lookup"><span data-stu-id="de372-124">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="de372-125">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="de372-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="de372-126">**IHV (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="de372-126">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




