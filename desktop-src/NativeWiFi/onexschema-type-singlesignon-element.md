---
description: Gibt an, wann einmaliges Anmelden ausgeführt wird.
ms.assetid: 23a7ab31-b29d-4f45-a384-bb2d2c18230f
title: Type (SingleSignOn)-Element
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
ms.openlocfilehash: 947c8801e5b2534f4c3b4e548a2a2f2c7a4250d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350471"
---
# <a name="type-singlesignon-element"></a><span data-ttu-id="2931b-103">Type (SingleSignOn)-Element</span><span class="sxs-lookup"><span data-stu-id="2931b-103">type (singleSignOn) Element</span></span>

<span data-ttu-id="2931b-104">Das Type (SingleSignOn)-Element gibt an, wann einmaliges Anmelden ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2931b-104">The type (singleSignOn) element specifies when single sign on is performed.</span></span> <span data-ttu-id="2931b-105">Wenn die Einstellung auf festgelegt `preLogon` ist, wird einmaliges Anmelden ausgeführt, bevor sich der Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="2931b-105">When set to `preLogon`, single sign on is performed before the user logs on.</span></span> <span data-ttu-id="2931b-106">Wenn der Wert auf festgelegt `postLogon` ist, wird das einmalige Anmelden sofort nach der Anmeldung des Benutzers ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2931b-106">When set to `postLogon`, single sign on is performed immediately after the user logs on.</span></span>

<span data-ttu-id="2931b-107">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2931b-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="type"
    minOccurs="1"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="preLogon"
             />
            <xs:enumeration
                value="postLogon"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="2931b-108">Das **Type** -Element wird durch das [**SingleSignOn**](onexschema-singlesignon-onex-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="2931b-108">The **type** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="2931b-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2931b-109">Requirements</span></span>



| <span data-ttu-id="2931b-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2931b-110">Requirement</span></span> | <span data-ttu-id="2931b-111">Wert</span><span class="sxs-lookup"><span data-stu-id="2931b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2931b-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2931b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="2931b-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2931b-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2931b-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2931b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="2931b-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2931b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2931b-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2931b-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="2931b-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="2931b-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2931b-118">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="2931b-118">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="2931b-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="2931b-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2931b-120">**SingleSignOn (Onex)**</span><span class="sxs-lookup"><span data-stu-id="2931b-120">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 




