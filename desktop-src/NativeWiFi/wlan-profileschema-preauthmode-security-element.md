---
description: Gibt an, ob die Vorauthentifizierung vom Client verwendet wird.
ms.assetid: 305d77b6-fe2d-45c6-ac91-5769f91de152
title: preauthmode (Security)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ac74f193fb89c260b1a121b673f239147658865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345685"
---
# <a name="preauthmode-security-element"></a><span data-ttu-id="3a2c0-103">preauthmode (Security)-Element</span><span class="sxs-lookup"><span data-stu-id="3a2c0-103">preAuthMode (security) Element</span></span>

<span data-ttu-id="3a2c0-104">Das preauthmode (Security)-Element gibt an, ob die Vorauthentifizierung vom Client verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a2c0-104">The preAuthMode (security) element indicates whether pre-authentication will be used by the client.</span></span> <span data-ttu-id="3a2c0-105">Die Vorauthentifizierung ist für das sichere schnelle Roaming von WPA2 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3a2c0-105">Pre-authentication is necessary for WPA2 secure fast roaming.</span></span> <span data-ttu-id="3a2c0-106">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen [**pmkcachemode**](wlan-profileschema-pmkcachemode-security-element.md) auf "aktiviert" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3a2c0-106">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="3a2c0-107">Wenn **pmkcachemode** aktiviert ist und dieses Element nicht vorhanden ist, ist der Standardwert "deaktiviert".</span><span class="sxs-lookup"><span data-stu-id="3a2c0-107">If **PMKCacheMode** is enabled, and this element is absent, the default value is "disabled".</span></span>

<span data-ttu-id="3a2c0-108">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a2c0-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="preAuthMode"
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

<span data-ttu-id="3a2c0-109">Das-Element wird durch das [**Security**](wlan-profileschema-security-msm-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="3a2c0-109">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a2c0-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a2c0-110">Requirements</span></span>



| <span data-ttu-id="3a2c0-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a2c0-111">Requirement</span></span> | <span data-ttu-id="3a2c0-112">Wert</span><span class="sxs-lookup"><span data-stu-id="3a2c0-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3a2c0-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a2c0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3a2c0-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a2c0-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3a2c0-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a2c0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3a2c0-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a2c0-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a2c0-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a2c0-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a2c0-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="3a2c0-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3a2c0-119">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="3a2c0-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="3a2c0-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="3a2c0-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3a2c0-121">**Sicherheit (MSM)**</span><span class="sxs-lookup"><span data-stu-id="3a2c0-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




