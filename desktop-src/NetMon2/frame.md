---
description: Ein tatsächlicher Frame des Treibers.
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: Frame-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b4ff8d66f88b18988cbb33bbcd8196cc01177b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344661"
---
# <a name="frame-structure"></a><span data-ttu-id="2bd03-103">Frame Struktur</span><span class="sxs-lookup"><span data-stu-id="2bd03-103">FRAME structure</span></span>

<span data-ttu-id="2bd03-104">Die **Frame** -Struktur ist ein tatsächlicher Frame des Treibers.</span><span class="sxs-lookup"><span data-stu-id="2bd03-104">The **FRAME** structure is an actual frame from the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bd03-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bd03-105">Syntax</span></span>


```C++
typedef struct _FRAME {
  __int64 TimeStamp;
  DWORD   FrameLength;
  DWORD   nBytesAvail;
  BYTE    MacFrame[];
} FRAME, *LPFRAME, *ULPFRAME;
```



## <a name="members"></a><span data-ttu-id="2bd03-106">Member</span><span class="sxs-lookup"><span data-stu-id="2bd03-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2bd03-107">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="2bd03-107">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="2bd03-108">Verstrichene Zeit (in Mikrosekunden) zwischen dem Start der Erfassung und dem Zeitpunkt, zu dem der Rahmen aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="2bd03-108">Elapsed time, in microseconds, between the start of the capture and the time when the frame was captured.</span></span>

</dd> <dt>

<span data-ttu-id="2bd03-109">**Framelength**</span><span class="sxs-lookup"><span data-stu-id="2bd03-109">**FrameLength**</span></span>
</dt> <dd>

<span data-ttu-id="2bd03-110">Mac-Frame Länge.</span><span class="sxs-lookup"><span data-stu-id="2bd03-110">MAC frame length.</span></span>

</dd> <dt>

<span data-ttu-id="2bd03-111">**nbytesnütz**</span><span class="sxs-lookup"><span data-stu-id="2bd03-111">**nBytesAvail**</span></span>
</dt> <dd>

<span data-ttu-id="2bd03-112">Die tatsächliche kopierte Frame Länge.</span><span class="sxs-lookup"><span data-stu-id="2bd03-112">Actual frame length copied.</span></span>

</dd> <dt>

<span data-ttu-id="2bd03-113">**Macframe**</span><span class="sxs-lookup"><span data-stu-id="2bd03-113">**MacFrame**</span></span>
</dt> <dd>

<span data-ttu-id="2bd03-114">Frame-Daten.</span><span class="sxs-lookup"><span data-stu-id="2bd03-114">Frame data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2bd03-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bd03-115">Requirements</span></span>



| <span data-ttu-id="2bd03-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bd03-116">Requirement</span></span> | <span data-ttu-id="2bd03-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2bd03-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd03-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2bd03-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd03-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bd03-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2bd03-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2bd03-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd03-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bd03-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2bd03-122">Header</span><span class="sxs-lookup"><span data-stu-id="2bd03-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bd03-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bd03-123"><dt>Netmon.h</dt></span></span> </dl> |



 

 




