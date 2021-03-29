---
description: Diese Klasse ist die Ereignistyp Klasse für Ereignisse von ALPC-End-wait. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 89a357dd-c217-4b55-994a-4252fa3cae1c
title: ALPC_Unwait-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Unwait
- ALPC_Unwait.Status
api_type:
- NA
api_location: ''
ms.openlocfilehash: f0846eae1ebb88e8892f1fe9b8dd07fd1be9d146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527056"
---
# <a name="alpc_unwait-class"></a><span data-ttu-id="37a5e-104">ALPC- \_ Klasse "Unwait"</span><span class="sxs-lookup"><span data-stu-id="37a5e-104">ALPC\_Unwait class</span></span>

<span data-ttu-id="37a5e-105">Diese Klasse ist die Ereignistyp Klasse für Ereignisse von ALPC-End-wait.</span><span class="sxs-lookup"><span data-stu-id="37a5e-105">This class is the event type class for ALPC end wait events.</span></span>

<span data-ttu-id="37a5e-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="37a5e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="37a5e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="37a5e-107">Syntax</span></span>

``` syntax
[EventType(37), EventTypeName("ALPC-Unwait")]
class ALPC_Unwait : ALPC
{
  uint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="37a5e-108">Member</span><span class="sxs-lookup"><span data-stu-id="37a5e-108">Members</span></span>

<span data-ttu-id="37a5e-109">Die **ALPC- \_ Unwait** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="37a5e-109">The **ALPC\_Unwait** class has these types of members:</span></span>

-   [<span data-ttu-id="37a5e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37a5e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37a5e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37a5e-111">Properties</span></span>

<span data-ttu-id="37a5e-112">Die **ALPC- \_ Unwait** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="37a5e-112">The **ALPC\_Unwait** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37a5e-113">**Status**</span><span class="sxs-lookup"><span data-stu-id="37a5e-113">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37a5e-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37a5e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37a5e-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37a5e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37a5e-116">Status des warte Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="37a5e-116">Status from wait operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37a5e-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="37a5e-117">Requirements</span></span>



| <span data-ttu-id="37a5e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37a5e-118">Requirement</span></span> | <span data-ttu-id="37a5e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="37a5e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="37a5e-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37a5e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="37a5e-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37a5e-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="37a5e-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37a5e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="37a5e-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37a5e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




