---
description: Definiert die Typen von Drahtlos Netzwerken.
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: einfacher networktypetype-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d0acb998c879e718a0e201418610bb0aa6db8c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364188"
---
# <a name="networktypetype-simple-type"></a><span data-ttu-id="979a7-103">einfacher networktypetype-Typ</span><span class="sxs-lookup"><span data-stu-id="979a7-103">networkTypeType Simple Type</span></span>

<span data-ttu-id="979a7-104">Der einfache Typ networktypetype definiert die Typen von Drahtlos Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="979a7-104">The networkTypeType simple type defines the wireless network types.</span></span> <span data-ttu-id="979a7-105">Es gibt zwei Arten von Netzwerken: Infrastruktur Netzwerke (ESS) und Ad-hoc-Netzwerke (IBSS).</span><span class="sxs-lookup"><span data-stu-id="979a7-105">There are two types of networks: infrastructure networks (ESS) and ad-hoc networks (IBSS).</span></span>

``` syntax
<xs:simpleType name="networkTypeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="IBSS"
         />
        <xs:enumeration
            value="ESS"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="979a7-106">Enumerationswerte</span><span class="sxs-lookup"><span data-stu-id="979a7-106">Enumeration values</span></span>

<span data-ttu-id="979a7-107">Der einfache Typ **Network Typetype** definiert die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="979a7-107">The **networkTypeType** simple type defines the following values.</span></span>



| <span data-ttu-id="979a7-108">Wert</span><span class="sxs-lookup"><span data-stu-id="979a7-108">Value</span></span> | <span data-ttu-id="979a7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="979a7-109">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="979a7-110">IBSS</span><span class="sxs-lookup"><span data-stu-id="979a7-110">IBSS</span></span>  |             |
| <span data-ttu-id="979a7-111">Lich</span><span class="sxs-lookup"><span data-stu-id="979a7-111">ESS</span></span>   |             |



## <a name="requirements"></a><span data-ttu-id="979a7-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="979a7-112">Requirements</span></span>



| <span data-ttu-id="979a7-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="979a7-113">Requirement</span></span> | <span data-ttu-id="979a7-114">Wert</span><span class="sxs-lookup"><span data-stu-id="979a7-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="979a7-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="979a7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="979a7-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="979a7-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="979a7-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="979a7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="979a7-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="979a7-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




