---
description: Gibt die Zeitdauer in Sekunden an, die gewartet werden soll, bevor eine EAPOL-Start gesendet wird.
ms.assetid: 6163eeb9-23a8-4e34-ad3f-016946e241e2
title: startperiod (Onex)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- startPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a583403a354cbefe93387be2d5af06958bbf6b28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345348"
---
# <a name="startperiod-onex-element"></a><span data-ttu-id="efc0c-103">startperiod (Onex)-Element</span><span class="sxs-lookup"><span data-stu-id="efc0c-103">startPeriod (OneX) Element</span></span>

<span data-ttu-id="efc0c-104">Das startperiod-Element (Onex) gibt die Zeitspanne in Sekunden an, die gewartet werden soll, bevor eine EAPOL-Start gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="efc0c-104">The startPeriod (OneX) element specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span> <span data-ttu-id="efc0c-105">Eine EAPOL-Start Nachricht wird gesendet, um den 802.1 x-Authentifizierungsprozess zu starten.</span><span class="sxs-lookup"><span data-stu-id="efc0c-105">An EAPOL-Start message is sent to start the 802.1X authentication process.</span></span>

<span data-ttu-id="efc0c-106">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="efc0c-106">This element is optional.</span></span> <span data-ttu-id="efc0c-107">Wenn "startperiod" nicht in einem Profil angegeben ist, wird ein Wert von 5 Sekunden verwendet.</span><span class="sxs-lookup"><span data-stu-id="efc0c-107">When startPeriod is not specified in a profile, a value of 5 seconds is used.</span></span>

<span data-ttu-id="efc0c-108">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="efc0c-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="startPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="efc0c-109">Das **startperiod** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="efc0c-109">The **startPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="efc0c-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="efc0c-110">Requirements</span></span>



| <span data-ttu-id="efc0c-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="efc0c-111">Requirement</span></span> | <span data-ttu-id="efc0c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="efc0c-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="efc0c-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="efc0c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="efc0c-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="efc0c-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="efc0c-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="efc0c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="efc0c-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="efc0c-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="efc0c-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efc0c-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="efc0c-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="efc0c-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="efc0c-119">**Onex**</span><span class="sxs-lookup"><span data-stu-id="efc0c-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="efc0c-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="efc0c-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="efc0c-121">**Onex**</span><span class="sxs-lookup"><span data-stu-id="efc0c-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




