---
description: Die Frame \_ deskriptorstruktur stellt beschreibende Informationen zu rohframes bereit.
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: FRAME_DESCRIPTOR Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c327ce1568eec07aabe3334013dae8b720ab7446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344404"
---
# <a name="frame_descriptor-structure"></a><span data-ttu-id="49525-103">Frame \_ deskriptorstruktur</span><span class="sxs-lookup"><span data-stu-id="49525-103">FRAME\_DESCRIPTOR structure</span></span>

<span data-ttu-id="49525-104">Die **Frame \_ deskriptorstruktur** stellt beschreibende Informationen zu rohframes bereit.</span><span class="sxs-lookup"><span data-stu-id="49525-104">The **FRAME\_DESCRIPTOR** structure provides descriptive information about raw frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="49525-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="49525-105">Syntax</span></span>


```C++
typedef struct _FRAME_DESCRIPTOR {
  LPBYTE       FramePointer;
  __int64      TimeStamp;
  DWORD        FrameLength;
  DWORD        nBytesAvail;
  WORD         Etype;
  BYTE         Sap;
  BYTE         LowProtocol;
  WORD         LowProtocolOffset;
  GENERIC_PORT HighPort;
  WORD         HighProtocolOffset;
} FRAME_DESCRIPTOR, *LPFRAME_DESCRIPTOR;
```



## <a name="members"></a><span data-ttu-id="49525-106">Member</span><span class="sxs-lookup"><span data-stu-id="49525-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="49525-107">**Framezeiger**</span><span class="sxs-lookup"><span data-stu-id="49525-107">**FramePointer**</span></span>
</dt> <dd>

<span data-ttu-id="49525-108">Zeiger auf Frame-Daten.</span><span class="sxs-lookup"><span data-stu-id="49525-108">Pointer to frame data.</span></span>

</dd> <dt>

<span data-ttu-id="49525-109">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="49525-109">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="49525-110">Die System Zeit in Mikrosekunden, zu der der Frame aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="49525-110">System time, in microseconds, when the frame was captured.</span></span> <span data-ttu-id="49525-111">Diese Zeit wird normalerweise verwendet, um das Intervall zwischen dem Erfassen von zwei Frames zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="49525-111">This time is typically used to determine the interval between the times two frames were captured.</span></span>

</dd> <dt>

<span data-ttu-id="49525-112">**Framelength**</span><span class="sxs-lookup"><span data-stu-id="49525-112">**FrameLength**</span></span>
</dt> <dd>

<span data-ttu-id="49525-113">Die Länge des Frames.</span><span class="sxs-lookup"><span data-stu-id="49525-113">Length of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="49525-114">**nbytesnütz**</span><span class="sxs-lookup"><span data-stu-id="49525-114">**nBytesAvail**</span></span>
</dt> <dd>

<span data-ttu-id="49525-115">Die tatsächliche kopierte Frame Länge.</span><span class="sxs-lookup"><span data-stu-id="49525-115">Actual frame length copied.</span></span>

</dd> <dt>

<span data-ttu-id="49525-116">**ETYPE**</span><span class="sxs-lookup"><span data-stu-id="49525-116">**Etype**</span></span>
</dt> <dd>

<span data-ttu-id="49525-117">ETYPE-Name.</span><span class="sxs-lookup"><span data-stu-id="49525-117">Etype name.</span></span>

</dd> <dt>

<span data-ttu-id="49525-118">**SAP**</span><span class="sxs-lookup"><span data-stu-id="49525-118">**Sap**</span></span>
</dt> <dd>

<span data-ttu-id="49525-119">SAP-Wert.</span><span class="sxs-lookup"><span data-stu-id="49525-119">SAP value.</span></span>

</dd> <dt>

<span data-ttu-id="49525-120">**Lowprotocol**</span><span class="sxs-lookup"><span data-stu-id="49525-120">**LowProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="49525-121">Der Index des gefundenen Protokolls.</span><span class="sxs-lookup"><span data-stu-id="49525-121">Index of protocol found.</span></span>

</dd> <dt>

<span data-ttu-id="49525-122">**Lowprotocoloffset**</span><span class="sxs-lookup"><span data-stu-id="49525-122">**LowProtocolOffset**</span></span>
</dt> <dd>

<span data-ttu-id="49525-123">Offset für Protokolldaten, die aus **lowprotocol** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="49525-123">Offset to protocol data obtained from **LowProtocol**.</span></span>

</dd> <dt>

<span data-ttu-id="49525-124">**Highport**</span><span class="sxs-lookup"><span data-stu-id="49525-124">**HighPort**</span></span>
</dt> <dd>

<span data-ttu-id="49525-125">Port des hohen Protokolls, identifiziert in **lowprotocol**.</span><span class="sxs-lookup"><span data-stu-id="49525-125">Port of high protocol identified in **LowProtocol**.</span></span>

</dd> <dt>

<span data-ttu-id="49525-126">**Highprotocoloffset**</span><span class="sxs-lookup"><span data-stu-id="49525-126">**HighProtocolOffset**</span></span>
</dt> <dd>

<span data-ttu-id="49525-127">Offset für Protokolldaten, die von **highport** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="49525-127">Offset to protocol data obtained from **HighPort**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49525-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49525-128">Requirements</span></span>



| <span data-ttu-id="49525-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49525-129">Requirement</span></span> | <span data-ttu-id="49525-130">Wert</span><span class="sxs-lookup"><span data-stu-id="49525-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="49525-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49525-131">Minimum supported client</span></span><br/> | <span data-ttu-id="49525-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49525-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="49525-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49525-133">Minimum supported server</span></span><br/> | <span data-ttu-id="49525-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49525-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="49525-135">Header</span><span class="sxs-lookup"><span data-stu-id="49525-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="49525-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="49525-136"><dt>Netmon.h</dt></span></span> </dl> |



 

 




