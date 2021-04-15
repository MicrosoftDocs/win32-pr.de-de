---
description: Gibt an, wie viele vorauthentifizierungs Versuche für benachbarte APS versucht werden.
ms.assetid: 7e89e962-7544-4efb-9e3c-c108bee22aea
title: preauththrottle (Security)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthThrottle
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 499401affb264238a065c0861f1230f23936206e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525754"
---
# <a name="preauththrottle-security-element"></a><span data-ttu-id="a3322-103">preauththrottle (Security)-Element</span><span class="sxs-lookup"><span data-stu-id="a3322-103">preAuthThrottle (security) Element</span></span>

<span data-ttu-id="a3322-104">Das preauththrottle (Security)-Element gibt die Anzahl von vorauthentifizierungs versuchen für benachbarte APS an.</span><span class="sxs-lookup"><span data-stu-id="a3322-104">The preAuthThrottle (security) element specifies the number pre-authentication attempts to try on neighboring APs.</span></span> <span data-ttu-id="a3322-105">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen [**pmkcachemode**](wlan-profileschema-pmkcachemode-security-element.md) auf "aktiviert" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a3322-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="a3322-106">Wenn **pmkcachemode** aktiviert ist und dieses Element nicht vorhanden ist, wird für die Anzahl von versuchen standardmäßig der Wert 3 verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3322-106">If **PMKCacheMode** is enabled, and this element is absent, the number of tries defaults to 3.</span></span>

<span data-ttu-id="a3322-107">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a3322-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="preAuthThrottle"
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
                value="16"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="a3322-108">Das-Element wird durch das [**Security**](wlan-profileschema-security-msm-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="a3322-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3322-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3322-109">Requirements</span></span>



| <span data-ttu-id="a3322-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3322-110">Requirement</span></span> | <span data-ttu-id="a3322-111">Wert</span><span class="sxs-lookup"><span data-stu-id="a3322-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a3322-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3322-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a3322-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3322-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a3322-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3322-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a3322-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3322-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a3322-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3322-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="a3322-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="a3322-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a3322-118">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="a3322-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="a3322-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="a3322-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a3322-120">**Sicherheit (MSM)**</span><span class="sxs-lookup"><span data-stu-id="a3322-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




