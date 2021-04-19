---
description: Speichert Informationen zu freigegebenen Speicherabschnitten.
ms.assetid: 73a650ee-110c-43f2-a5e2-783d52fd29ee
title: SHAREDMEMORY_HEADER Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHAREDMEMORY_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 695f3ef09cb5e7e67de757ee3926df6fde7ddff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363225"
---
# <a name="sharedmemory_header-structure"></a><span data-ttu-id="15bda-103">SharedMemory- \_ Header Struktur</span><span class="sxs-lookup"><span data-stu-id="15bda-103">SHAREDMEMORY\_HEADER structure</span></span>

<span data-ttu-id="15bda-104">Speichert Informationen zu freigegebenen Speicherabschnitten.</span><span class="sxs-lookup"><span data-stu-id="15bda-104">Stores information about shared memory sections.</span></span>

## <a name="syntax"></a><span data-ttu-id="15bda-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15bda-105">Syntax</span></span>


```C++
typedef struct _SHAREDMEMORY_HEADER {
  DWORD             cbTotal;
  DWORD             cbOffsetSns;
  DWORD             idxEvent;
  DWORD             dwEvent;
  CURSOR_ID         cid;
  DWORD             sn;
  SYSTEM_EVENT      sysEvt;
  SYSTEM_EVENT_DATA sysEvtData;
  DWORD             cPackets;
  DWORD             cbPackets;
  BOOL              fSnsPresent;
} SHAREDMEMORY_HEADER, *PSHAREDMEMORY_HEADER;
```



## <a name="members"></a><span data-ttu-id="15bda-106">Member</span><span class="sxs-lookup"><span data-stu-id="15bda-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="15bda-107">**cbtotal**</span><span class="sxs-lookup"><span data-stu-id="15bda-107">**cbTotal**</span></span>
</dt> <dd>

<span data-ttu-id="15bda-108">Die Größe der Daten in Bytes, auf die von dieser Header Struktur verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="15bda-108">The size, in bytes, of the data referenced by this header structure.</span></span>

</dd> <dt>

<span data-ttu-id="15bda-109">**cboffsekunden**</span><span class="sxs-lookup"><span data-stu-id="15bda-109">**cbOffsetSns**</span></span>
</dt> <dd>

<span data-ttu-id="15bda-110">Die Größe in Bytes, in der die Seriennummern von der Header Struktur versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="15bda-110">The size, in bytes, that the serial numbers are offset from the header structure.</span></span>

</dd> <dt>

<span data-ttu-id="15bda-111">**idxevent**</span><span class="sxs-lookup"><span data-stu-id="15bda-111">**idxEvent**</span></span>
</dt> <dd>

<span data-ttu-id="15bda-112">Der Ereignis Index.</span><span class="sxs-lookup"><span data-stu-id="15bda-112">The event index.</span></span> <span data-ttu-id="15bda-113">Dieser Wert wird mit aufeinander folgenden Ereignissen inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="15bda-113">This value is incremented with successive events.</span></span>

</dd> <dt>

<span data-ttu-id="15bda-114">**dwevent**</span><span class="sxs-lookup"><span data-stu-id="15bda-114">**dwEvent**</span></span>
</dt> <dd>

<span data-ttu-id="15bda-115">Das Ereignis, das diesem Header zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="15bda-115">The event associated with this header.</span></span>

</dd> <dt>

<span data-ttu-id="15bda-116">**zid**</span><span class="sxs-lookup"><span data-stu-id="15bda-116">**cid**</span></span>
</dt> <dd>

<span data-ttu-id="15bda-117">Der Cursor Bezeichner, auf den vom Shared Memory-Header verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="15bda-117">The cursor identifier referenced by the shared memory header.</span></span>

</dd> <dt>

<span data-ttu-id="15bda-118">**sn**</span><span class="sxs-lookup"><span data-stu-id="15bda-118">**sn**</span></span>
</dt> <dd>

<span data-ttu-id="15bda-119">Die Seriennummer für den Header des freigegebenen Speichers.</span><span class="sxs-lookup"><span data-stu-id="15bda-119">The serial number for the shared memory header.</span></span>

</dd> <dt>

<span data-ttu-id="15bda-120">**sysegvt**</span><span class="sxs-lookup"><span data-stu-id="15bda-120">**sysEvt**</span></span>
</dt> <dd>

<span data-ttu-id="15bda-121">Das System Ereignis, dem vorangestellten Präfix \_ \* , das diesem Header zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="15bda-121">The system event, prefixed SE\_\*, associated with this header.</span></span> <span data-ttu-id="15bda-122">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="15bda-122">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="15bda-123">**syabvtdata**</span><span class="sxs-lookup"><span data-stu-id="15bda-123">**sysEvtData**</span></span>
</dt> <dd>

<span data-ttu-id="15bda-124">Die [**System \_ Ereignis \_ Daten**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) Struktur, die dem System Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="15bda-124">The [**SYSTEM\_EVENT\_DATA**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) structure associated with the system event.</span></span>

</dd> <dt>

<span data-ttu-id="15bda-125">**cpakete**</span><span class="sxs-lookup"><span data-stu-id="15bda-125">**cPackets**</span></span>
</dt> <dd>

<span data-ttu-id="15bda-126">Gibt die Anzahl der Pakete an, die dem aktuellen Shared Memory-Abschnitt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="15bda-126">A count of the packets associated with the current shared memory section.</span></span>

</dd> <dt>

<span data-ttu-id="15bda-127">**CB-Pakete**</span><span class="sxs-lookup"><span data-stu-id="15bda-127">**cbPackets**</span></span>
</dt> <dd>

<span data-ttu-id="15bda-128">Die Größe der dem aktuellen Shared Memory-Abschnitt zugeordneten Pakete in Bytes.</span><span class="sxs-lookup"><span data-stu-id="15bda-128">The size, in bytes, of the packets associated with the current shared memory section.</span></span>

</dd> <dt>

<span data-ttu-id="15bda-129">**"f"**</span><span class="sxs-lookup"><span data-stu-id="15bda-129">**fSnsPresent**</span></span>
</dt> <dd>

<span data-ttu-id="15bda-130">Ein Flag, das angibt, ob Seriennummern im aktuellen Shared Memory-Abschnitt vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="15bda-130">A flag indicating whether serial numbers are present in the current shared memory section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15bda-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15bda-131">Remarks</span></span>

<span data-ttu-id="15bda-132">Die folgenden Werte sind für den **sysegvt** -Member definiert.</span><span class="sxs-lookup"><span data-stu-id="15bda-132">The following values are defined for the **sysEvt** member.</span></span>


```C++
#define SE_NONE                  0x00000000
#define SE_TAP                   0x00000010
#define SE_DBL_TAP               0x00000011
#define SE_RIGHT_TAP             0x00000012
#define SE_DRAG                  0x00000013
#define SE_RIGHT_DRAG            0x00000014
#define SE_HOLD_ENTER            0x00000015
#define SE_HOLD_LEAVE            0x00000016
#define SE_HOVER_ENTER           0x00000017
#define SE_HOVER_LEAVE           0x00000018
#define SE_FLICK                 0x0000001F
```



## <a name="see-also"></a><span data-ttu-id="15bda-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15bda-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15bda-134">**System \_ Ereignis \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="15bda-134">**SYSTEM\_EVENT\_DATA**</span></span>](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 



