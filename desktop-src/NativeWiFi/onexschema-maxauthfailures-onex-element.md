---
description: Gibt die maximale Anzahl von Authentifizierungs Fehlern an, die für einen Satz von Anmelde Informationen zulässig sind.
ms.assetid: 191b6b03-8b27-4b35-8623-1ccec632f208
title: maxauthfailure (Onex)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxAuthFailures
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 31dae7a8805275254a1d398108128380b1aa2e54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529030"
---
# <a name="maxauthfailures-onex-element"></a><span data-ttu-id="acf9a-103">maxauthfailure (Onex)-Element</span><span class="sxs-lookup"><span data-stu-id="acf9a-103">maxAuthFailures (OneX) Element</span></span>

<span data-ttu-id="acf9a-104">Das maxauthfailure (Onex)-Element gibt die maximale Anzahl von Authentifizierungs Fehlern an, die für einen Satz von Anmelde Informationen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="acf9a-104">The maxAuthFailures (OneX) element specifies the maximum number of authentication failures allowed for a set of credentials.</span></span>

<span data-ttu-id="acf9a-105">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="acf9a-105">This element is optional.</span></span> <span data-ttu-id="acf9a-106">Wenn maxauthfailure nicht in einem Profil angegeben ist, wird der Wert 1 verwendet.</span><span class="sxs-lookup"><span data-stu-id="acf9a-106">When maxAuthFailures is not specified in a profile, a value of one is used.</span></span>

<span data-ttu-id="acf9a-107">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="acf9a-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxAuthFailures">
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

<span data-ttu-id="acf9a-108">Das **maxauthfailure** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="acf9a-108">The **maxAuthFailures** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="acf9a-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acf9a-109">Requirements</span></span>



| <span data-ttu-id="acf9a-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acf9a-110">Requirement</span></span> | <span data-ttu-id="acf9a-111">Wert</span><span class="sxs-lookup"><span data-stu-id="acf9a-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="acf9a-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="acf9a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="acf9a-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acf9a-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="acf9a-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="acf9a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="acf9a-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acf9a-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="acf9a-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acf9a-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="acf9a-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="acf9a-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="acf9a-118">**Onex**</span><span class="sxs-lookup"><span data-stu-id="acf9a-118">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="acf9a-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="acf9a-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="acf9a-120">**Onex**</span><span class="sxs-lookup"><span data-stu-id="acf9a-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




