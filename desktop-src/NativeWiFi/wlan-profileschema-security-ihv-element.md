---
description: Enthält verschiedene Sicherheitseinstellungen, die von unabhängigen Hardwareanbietern verwendet werden.
ms.assetid: 237c5d98-3f3c-4279-b2ad-b0d05df041f9
title: Security (IHV)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ace1bb0ca31f40fdc9d10fba13832797d8d4306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373087"
---
# <a name="security-ihv-element"></a><span data-ttu-id="85fb0-103">Security (IHV)-Element</span><span class="sxs-lookup"><span data-stu-id="85fb0-103">security (IHV) Element</span></span>

<span data-ttu-id="85fb0-104">Das Sicherheitselement (IHV) enthält verschiedene Sicherheitseinstellungen, die von unabhängigen Hardwareanbietern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85fb0-104">The security (IHV) element contains various security settings used by independent hardware vendors.</span></span>

<span data-ttu-id="85fb0-105">Die Sicherheitseinstellungen von Microsoft und die IHV-Sicherheitseinstellungen schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="85fb0-105">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="85fb0-106">Wenn beide Gruppen von Sicherheitseinstellungen im gleichen Profil vorhanden sind, ist das Profil ungültig.</span><span class="sxs-lookup"><span data-stu-id="85fb0-106">If both sets of security settings are present in the same profile, the profile is invalid.</span></span>

<span data-ttu-id="85fb0-107">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="85fb0-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="security">
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

<span data-ttu-id="85fb0-108">Das **Security** -Element wird durch das [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="85fb0-108">The **security** element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="85fb0-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85fb0-109">Requirements</span></span>



| <span data-ttu-id="85fb0-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85fb0-110">Requirement</span></span> | <span data-ttu-id="85fb0-111">Wert</span><span class="sxs-lookup"><span data-stu-id="85fb0-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="85fb0-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85fb0-112">Minimum supported client</span></span><br/> | <span data-ttu-id="85fb0-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85fb0-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="85fb0-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85fb0-114">Minimum supported server</span></span><br/> | <span data-ttu-id="85fb0-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85fb0-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85fb0-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85fb0-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="85fb0-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="85fb0-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="85fb0-118">**IHV**</span><span class="sxs-lookup"><span data-stu-id="85fb0-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="85fb0-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="85fb0-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="85fb0-120">**IHV (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="85fb0-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




