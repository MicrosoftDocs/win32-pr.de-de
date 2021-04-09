---
description: Die Frametable-Struktur, ein Zirkel Puffer von Frame Zeigern, wird an Anwendungen zurückgegeben, die an die ITRC-Schnittstelle der NPP angefügt sind.
ms.assetid: 6e2d4f8d-46f2-4d53-bc28-7b0706663490
title: Frametable-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAMETABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95d7930d7943b26ebba1bb194d083ca8beb9dcf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128352"
---
# <a name="frametable-structure"></a><span data-ttu-id="74f3f-103">Frametable-Struktur</span><span class="sxs-lookup"><span data-stu-id="74f3f-103">FRAMETABLE structure</span></span>

<span data-ttu-id="74f3f-104">Die **Frametable** -Struktur, ein Zirkel Puffer von Frame Zeigern, wird an Anwendungen zurückgegeben, die an die **ITRC** -Schnittstelle der NPP angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="74f3f-104">The **FRAMETABLE** structure, a circular buffer of frame pointers, is handed back to applications attached to the **ITRC** interface of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="74f3f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="74f3f-105">Syntax</span></span>


```C++
typedef struct _FRAMETABLE {
  DWORD            FrameTableLength;
  DWORD            StartIndex;
  DWORD            EndIndex;
  DWORD            FrameCount;
  FRAME_DESCRIPTOR Frames[1];
} FRAMETABLE, *LPFRAMETABLE;
```



## <a name="members"></a><span data-ttu-id="74f3f-106">Member</span><span class="sxs-lookup"><span data-stu-id="74f3f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="74f3f-107">**Frametablelength**</span><span class="sxs-lookup"><span data-stu-id="74f3f-107">**FrameTableLength**</span></span>
</dt> <dd>

<span data-ttu-id="74f3f-108">Die Gesamtlänge der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="74f3f-108">The total length of the table.</span></span>

</dd> <dt>

<span data-ttu-id="74f3f-109">**Start Index**</span><span class="sxs-lookup"><span data-stu-id="74f3f-109">**StartIndex**</span></span>
</dt> <dd>

<span data-ttu-id="74f3f-110">Der erste Index in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="74f3f-110">The first index within the table.</span></span>

</dd> <dt>

<span data-ttu-id="74f3f-111">**EndIndex sein**</span><span class="sxs-lookup"><span data-stu-id="74f3f-111">**EndIndex**</span></span>
</dt> <dd>

<span data-ttu-id="74f3f-112">Der letzte Index in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="74f3f-112">The last index within the table.</span></span>

</dd> <dt>

<span data-ttu-id="74f3f-113">**FrameCount**</span><span class="sxs-lookup"><span data-stu-id="74f3f-113">**FrameCount**</span></span>
</dt> <dd>

<span data-ttu-id="74f3f-114">Die Anzahl der Frames, die von dieser Tabelle beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="74f3f-114">The number of frames described by this table.</span></span>

</dd> <dt>

<span data-ttu-id="74f3f-115">**Frames**</span><span class="sxs-lookup"><span data-stu-id="74f3f-115">**Frames**</span></span>
</dt> <dd>

<span data-ttu-id="74f3f-116">Das tatsächliche Array von Frame Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="74f3f-116">The actual array of frame descriptors.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74f3f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74f3f-117">Requirements</span></span>



| <span data-ttu-id="74f3f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74f3f-118">Requirement</span></span> | <span data-ttu-id="74f3f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="74f3f-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="74f3f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74f3f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="74f3f-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74f3f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="74f3f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74f3f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="74f3f-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74f3f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="74f3f-124">Header</span><span class="sxs-lookup"><span data-stu-id="74f3f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="74f3f-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="74f3f-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




