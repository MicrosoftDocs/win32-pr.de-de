---
description: Enthält verschiedene Konnektivitätseinstellungen.
ms.assetid: 2938f607-47a1-49eb-bf3f-247cab8637ec
title: konnektivitätselement (MSM)
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
ms.openlocfilehash: 938e5b19ffab490066fbbe299bd250191d9226a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351144"
---
# <a name="connectivity-msm-element"></a><span data-ttu-id="51d5a-103">konnektivitätselement (MSM)</span><span class="sxs-lookup"><span data-stu-id="51d5a-103">connectivity (MSM) Element</span></span>

<span data-ttu-id="51d5a-104">Das konnektivitätselement (MSM) enthält verschiedene Konnektivitätseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="51d5a-104">The connectivity (MSM) element contains various connectivity settings.</span></span>

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
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

<span data-ttu-id="51d5a-105">Das-Element wird durch das [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="51d5a-105">The element is defined by the [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="51d5a-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="51d5a-106">Child elements</span></span>



| <span data-ttu-id="51d5a-107">Element</span><span class="sxs-lookup"><span data-stu-id="51d5a-107">Element</span></span>                                                            | <span data-ttu-id="51d5a-108">type</span><span class="sxs-lookup"><span data-stu-id="51d5a-108">Type</span></span> |
|--------------------------------------------------------------------|------|
| [<span data-ttu-id="51d5a-109">**phytype**</span><span class="sxs-lookup"><span data-stu-id="51d5a-109">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md) |      |



## <a name="examples"></a><span data-ttu-id="51d5a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51d5a-110">Examples</span></span>

<span data-ttu-id="51d5a-111">Beispiel Profile mit dem **konnektivitätselement** finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="51d5a-111">To view sample profiles that use the **connectivity** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51d5a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51d5a-112">Requirements</span></span>



| <span data-ttu-id="51d5a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51d5a-113">Requirement</span></span> | <span data-ttu-id="51d5a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="51d5a-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="51d5a-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51d5a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="51d5a-116">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51d5a-116">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="51d5a-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51d5a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="51d5a-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51d5a-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="51d5a-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="51d5a-119">Redistributable</span></span><br/>          | <span data-ttu-id="51d5a-120">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="51d5a-120">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="51d5a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51d5a-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="51d5a-122">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="51d5a-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="51d5a-123">**MSM**</span><span class="sxs-lookup"><span data-stu-id="51d5a-123">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="51d5a-124">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="51d5a-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="51d5a-125">**MSM (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="51d5a-125">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 




