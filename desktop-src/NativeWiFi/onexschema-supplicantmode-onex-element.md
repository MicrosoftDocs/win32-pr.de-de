---
description: Gibt die Übertragungsmethode an, die für EAPOL-Start Nachrichten verwendet wird.
ms.assetid: 8d49d19a-8122-4191-bb46-92a2016bcfee
title: supplicantmode-Element (Onex)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- supplicantMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33d58bd247a220ca93ed4d2a05886be107afd4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368731"
---
# <a name="supplicantmode-onex-element"></a><span data-ttu-id="3f5fd-103">supplicantmode-Element (Onex)</span><span class="sxs-lookup"><span data-stu-id="3f5fd-103">supplicantMode (OneX) Element</span></span>

<span data-ttu-id="3f5fd-104">Das supplicantmode (Onex)-Element gibt die Übertragungsmethode an, die für EAPOL-Start Nachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3f5fd-104">The supplicantMode (OneX) element specifies the method of transmission used for EAPOL-Start messages.</span></span> <span data-ttu-id="3f5fd-105">In der folgenden Tabelle sind die möglichen Werte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3f5fd-105">The following table describes the possible values.</span></span>



| <span data-ttu-id="3f5fd-106">Wert</span><span class="sxs-lookup"><span data-stu-id="3f5fd-106">Value</span></span>               | <span data-ttu-id="3f5fd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f5fd-107">Description</span></span>                                                                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f5fd-108">inhibittransmission</span><span class="sxs-lookup"><span data-stu-id="3f5fd-108">inhibitTransmission</span></span> | <span data-ttu-id="3f5fd-109">EAPOL-Start-Nachrichten werden nicht übertragen.</span><span class="sxs-lookup"><span data-stu-id="3f5fd-109">EAPOL-Start messages are not transmitted.</span></span> <span data-ttu-id="3f5fd-110">Nur für kabelgebundene LAN-profile gültig.</span><span class="sxs-lookup"><span data-stu-id="3f5fd-110">Valid for wired LAN profiles only.</span></span>                                                                                             |
| <span data-ttu-id="3f5fd-111">includelta-Gewinn</span><span class="sxs-lookup"><span data-stu-id="3f5fd-111">includeLearning</span></span>     | <span data-ttu-id="3f5fd-112">Der Client legt fest, wann EAPOL-Start Pakete auf der Grundlage der Netzwerkfunktion gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3f5fd-112">The client determines when to send EAPOL-Start packets based on network capability.</span></span> <span data-ttu-id="3f5fd-113">EAPOL-Start Meldungen werden nur bei Bedarf gesendet.</span><span class="sxs-lookup"><span data-stu-id="3f5fd-113">EAPOL-Start messages are only sent when required.</span></span> <span data-ttu-id="3f5fd-114">Nur für kabelgebundene LAN-profile gültig.</span><span class="sxs-lookup"><span data-stu-id="3f5fd-114">Valid for wired LAN profiles only.</span></span> |
| <span data-ttu-id="3f5fd-115">Kompatibel</span><span class="sxs-lookup"><span data-stu-id="3f5fd-115">compliant</span></span>           | <span data-ttu-id="3f5fd-116">EAPOL-Start-Nachrichten werden gemäß 802.1 x übertragen.</span><span class="sxs-lookup"><span data-stu-id="3f5fd-116">EAPOL-Start messages are transmitted as specified by 802.1X.</span></span> <span data-ttu-id="3f5fd-117">Gültig für Kabel-und Drahtlos-LAN-Profile.</span><span class="sxs-lookup"><span data-stu-id="3f5fd-117">Valid for both wired and wireless LAN profiles.</span></span>                                                             |



 

<span data-ttu-id="3f5fd-118">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3f5fd-118">This element is optional.</span></span> <span data-ttu-id="3f5fd-119">Wenn supplicantmode nicht in einem Profil angegeben ist, wird der Wert `compliant` für Kabel-und Drahtlos LAN-Profile verwendet.</span><span class="sxs-lookup"><span data-stu-id="3f5fd-119">When supplicantMode is not specified in a profile, a value of `compliant` is used for both wired and wireless LAN profiles.</span></span>

<span data-ttu-id="3f5fd-120">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3f5fd-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="supplicantMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="inhibitTransmission"
             />
            <xs:enumeration
                value="includeLearning"
             />
            <xs:enumeration
                value="compliant"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="3f5fd-121">Das **supplicantmode** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="3f5fd-121">The **supplicantMode** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f5fd-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f5fd-122">Requirements</span></span>



| <span data-ttu-id="3f5fd-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f5fd-123">Requirement</span></span> | <span data-ttu-id="3f5fd-124">Wert</span><span class="sxs-lookup"><span data-stu-id="3f5fd-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3f5fd-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f5fd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3f5fd-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f5fd-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3f5fd-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f5fd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3f5fd-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f5fd-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f5fd-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f5fd-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="3f5fd-130">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="3f5fd-130">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3f5fd-131">**Onex**</span><span class="sxs-lookup"><span data-stu-id="3f5fd-131">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="3f5fd-132">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="3f5fd-132">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3f5fd-133">**Onex**</span><span class="sxs-lookup"><span data-stu-id="3f5fd-133">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




