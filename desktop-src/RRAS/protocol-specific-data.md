---
title: PROTOCOL_SPECIFIC_DATA Struktur (RTM. h)
description: Die Protokoll \_ spezifische \_ Datenstruktur enthält Arbeitsspeicher, der für spezifische Daten eines bestimmten Routing Protokolls reserviert ist.
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- PROTOCOL_SPECIFIC_DATA Struktur-RAS
- PPROTOCOL_SPECIFIC_DATA-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- PROTOCOL_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3162aa377c051f6b329e993dfaca3bed17fae780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742192"
---
# <a name="protocol_specific_data-structure"></a><span data-ttu-id="f2d82-105">Protokoll \_ spezifische \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="f2d82-105">PROTOCOL\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="f2d82-106">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f2d82-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="f2d82-107">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="f2d82-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="f2d82-108">Die **Protokoll \_ spezifische \_ Daten** Struktur enthält Arbeitsspeicher, der für spezifische Daten eines bestimmten Routing Protokolls reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="f2d82-108">The **PROTOCOL\_SPECIFIC\_DATA** structure contains memory reserved for data specific to a particular routing protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2d82-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2d82-109">Syntax</span></span>


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="f2d82-110">Member</span><span class="sxs-lookup"><span data-stu-id="f2d82-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="f2d82-111">**PSD- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="f2d82-111">**PSD\_Data**</span></span>
</dt> <dd>

<span data-ttu-id="f2d82-112">Gibt ein Array von **DWORD** -Variablen an.</span><span class="sxs-lookup"><span data-stu-id="f2d82-112">Specifies an array of **DWORD** variables.</span></span> <span data-ttu-id="f2d82-113">Dieser Speicher ist für Daten reserviert, die für Routing Protokolle spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="f2d82-113">This memory is reserved for data that is specific to routing protocols.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2d82-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2d82-114">Requirements</span></span>



| <span data-ttu-id="f2d82-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2d82-115">Requirement</span></span> | <span data-ttu-id="f2d82-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f2d82-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f2d82-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2d82-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f2d82-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f2d82-118">None supported</span></span><br/>                                                        |
| <span data-ttu-id="f2d82-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2d82-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f2d82-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2d82-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f2d82-121">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f2d82-121">End of server support</span></span><br/>    | <span data-ttu-id="f2d82-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f2d82-122">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="f2d82-123">Header</span><span class="sxs-lookup"><span data-stu-id="f2d82-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2d82-124"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2d82-124"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2d82-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2d82-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2d82-126">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="f2d82-126">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="f2d82-127">Routing Tabellen-Manager, Version 1, Strukturen</span><span class="sxs-lookup"><span data-stu-id="f2d82-127">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="f2d82-128">**RTM \_ -IP- \_ Route**</span><span class="sxs-lookup"><span data-stu-id="f2d82-128">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="f2d82-129">**RTM- \_ IPX- \_ Route**</span><span class="sxs-lookup"><span data-stu-id="f2d82-129">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





