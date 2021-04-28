---
title: Einfacher UInt32Type-Typ (Windows-Ereignisprotokoll)
description: 'UInt32Type Simple Type (Windows-Ereignisprotokoll): Definiert einen Ganzzahltyp ohne Vorzeichen.'
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- UInt32Type simple type EventLog
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 631bb3e8424db8a5d781aaa43df6096730aaa4d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090568"
---
# <a name="uint32type-simple-type-windows-event-log"></a><span data-ttu-id="1d28b-104">Einfacher UInt32Type-Typ (Windows-Ereignisprotokoll)</span><span class="sxs-lookup"><span data-stu-id="1d28b-104">UInt32Type Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="1d28b-105">Definiert einen ganzzahligen Typ ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="1d28b-105">Defines an unsigned integer type.</span></span> <span data-ttu-id="1d28b-106">Der Wert kann als 4-Byte-Ganzzahl oder Hexadezimalwert im Bereich von 0 bis 4.294.967.295 angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1d28b-106">The value can be specified as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="1d28b-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d28b-107">Requirements</span></span>



| <span data-ttu-id="1d28b-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d28b-108">Requirement</span></span> | <span data-ttu-id="1d28b-109">Wert</span><span class="sxs-lookup"><span data-stu-id="1d28b-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1d28b-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d28b-110">Minimum supported client</span></span><br/> | <span data-ttu-id="1d28b-111">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d28b-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1d28b-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d28b-112">Minimum supported server</span></span><br/> | <span data-ttu-id="1d28b-113">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d28b-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





