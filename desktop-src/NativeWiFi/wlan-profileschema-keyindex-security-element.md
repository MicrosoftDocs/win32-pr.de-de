---
description: Gibt an, welcher Schlüssel Index verwendet werden soll, um drahtlosen Datenverkehr zu verschlüsseln. Dies wird nur verwendet, wenn KeyType auf &\# 0034; networkkey&0034; festgelegt ist \# .
ms.assetid: 5629605d-4c23-4318-8f09-939e13302552
title: KeyIndex (Security)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyIndex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 43bb802d46abb3c4684b63206377d3464078e2c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131937"
---
# <a name="keyindex-security-element"></a><span data-ttu-id="66c7a-104">KeyIndex (Security)-Element</span><span class="sxs-lookup"><span data-stu-id="66c7a-104">keyIndex (security) Element</span></span>

<span data-ttu-id="66c7a-105">Das KeyIndex (Security)-Element gibt an, welcher Schlüssel Index verwendet werden soll, um drahtlosen Datenverkehr zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="66c7a-105">The keyIndex (security) element specifies which key index should be used to encrypt wireless traffic.</span></span> <span data-ttu-id="66c7a-106">Dies wird nur verwendet, wenn [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) auf "networkkey" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="66c7a-106">This is only used when [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) is set to "networkKey".</span></span>

``` syntax
<xs:element name="keyIndex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="0"
             />
            <xs:maxInclusive
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="66c7a-107">Das-Element wird durch das [**Security**](wlan-profileschema-security-msm-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="66c7a-107">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="66c7a-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66c7a-108">Requirements</span></span>



| <span data-ttu-id="66c7a-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66c7a-109">Requirement</span></span> | <span data-ttu-id="66c7a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="66c7a-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="66c7a-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66c7a-111">Minimum supported client</span></span><br/> | <span data-ttu-id="66c7a-112">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66c7a-112">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="66c7a-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66c7a-113">Minimum supported server</span></span><br/> | <span data-ttu-id="66c7a-114">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66c7a-114">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="66c7a-115">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="66c7a-115">Redistributable</span></span><br/>          | <span data-ttu-id="66c7a-116">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="66c7a-116">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="66c7a-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66c7a-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="66c7a-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="66c7a-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="66c7a-119">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="66c7a-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="66c7a-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="66c7a-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="66c7a-121">**Sicherheit (MSM)**</span><span class="sxs-lookup"><span data-stu-id="66c7a-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




