---
description: Gibt die maximale Anzahl von EAPOL-Start gesendeten Nachrichten an.
ms.assetid: 4e48f8b6-46eb-426e-ad22-3aa53cb66a17
title: maxstart (Onex)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxStart
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 14bf40538eafb3c8e78b68b7a435d0d37d401960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350204"
---
# <a name="maxstart-onex-element"></a><span data-ttu-id="9dda2-103">maxstart (Onex)-Element</span><span class="sxs-lookup"><span data-stu-id="9dda2-103">maxStart (OneX) Element</span></span>

<span data-ttu-id="9dda2-104">Das maxstart (Onex)-Element gibt die maximale Anzahl von EAPOL-Start gesendeten Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="9dda2-104">The maxStart (OneX) element specifies the maximum number of EAPOL-Start messages sent.</span></span> <span data-ttu-id="9dda2-105">Nachdem die maximale Anzahl von EAPOL-Start-Nachrichten gesendet wurde, nimmt der Client an, dass im Netzwerk kein Authentifikator vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9dda2-105">After the maximum number of EAPOL-Start messages has been sent, the client assumes that there is no authenticator present on the network.</span></span>

<span data-ttu-id="9dda2-106">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="9dda2-106">This element is optional.</span></span> <span data-ttu-id="9dda2-107">Wenn maxstart nicht in einem Profil angegeben ist, wird der Wert 3 Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="9dda2-107">When maxStart is not specified in a profile, a value of 3 messages is used.</span></span>

<span data-ttu-id="9dda2-108">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9dda2-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxStart">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="9dda2-109">Das **maxstart** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="9dda2-109">The **maxStart** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dda2-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9dda2-110">Requirements</span></span>



| <span data-ttu-id="9dda2-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9dda2-111">Requirement</span></span> | <span data-ttu-id="9dda2-112">Wert</span><span class="sxs-lookup"><span data-stu-id="9dda2-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9dda2-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9dda2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9dda2-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dda2-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9dda2-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9dda2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9dda2-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dda2-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9dda2-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9dda2-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="9dda2-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="9dda2-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9dda2-119">**Onex**</span><span class="sxs-lookup"><span data-stu-id="9dda2-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="9dda2-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="9dda2-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9dda2-121">**Onex**</span><span class="sxs-lookup"><span data-stu-id="9dda2-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




