---
title: MCI_MAKE_TMSF-Makro (mciapi. h)
description: Das MCI \_ make \_ TMSF-Makro erstellt einen Uhrzeitwert im TMAs-Format (gepackt/Minutes/seconds/seconds/Frames) aus den angegebenen Pfaden, Minuten, Sekunden und Rahmen Werten.
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- MCI_MAKE_TMSF Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_TMSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06cd6a400f742b49dc29063e8473465ad7e32dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338799"
---
# <a name="mci_make_tmsf-macro"></a><span data-ttu-id="bc899-104">MCI \_ make \_ TMSF-Makro</span><span class="sxs-lookup"><span data-stu-id="bc899-104">MCI\_MAKE\_TMSF macro</span></span>

<span data-ttu-id="bc899-105">Das **MCI \_ make \_ TMSF** -Makro erstellt einen Uhrzeitwert im TMAs-Format (gepackt/Minutes/seconds/seconds/Frames) aus den angegebenen Pfaden, Minuten, Sekunden und Rahmen Werten.</span><span class="sxs-lookup"><span data-stu-id="bc899-105">The **MCI\_MAKE\_TMSF** macro creates a time value in packed tracks/minutes/seconds/frames (TMSF) format from the given tracks, minutes, seconds, and frames values.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc899-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc899-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_TMSF(
   BYTE tracks,
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a><span data-ttu-id="bc899-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc899-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc899-108">*spürt*</span><span class="sxs-lookup"><span data-stu-id="bc899-108">*tracks*</span></span> 
</dt> <dd>

<span data-ttu-id="bc899-109">Anzahl der Spuren.</span><span class="sxs-lookup"><span data-stu-id="bc899-109">Number of tracks.</span></span>

</dd> <dt>

<span data-ttu-id="bc899-110">*minutes*</span><span class="sxs-lookup"><span data-stu-id="bc899-110">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="bc899-111">Anzahl der Minuten.</span><span class="sxs-lookup"><span data-stu-id="bc899-111">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="bc899-112">*Sekunden*</span><span class="sxs-lookup"><span data-stu-id="bc899-112">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="bc899-113">Anzahl der Sekunden.</span><span class="sxs-lookup"><span data-stu-id="bc899-113">Number of seconds.</span></span>

</dd> <dt>

<span data-ttu-id="bc899-114">*SSE*</span><span class="sxs-lookup"><span data-stu-id="bc899-114">*frames*</span></span> 
</dt> <dd>

<span data-ttu-id="bc899-115">Anzahl der Frames.</span><span class="sxs-lookup"><span data-stu-id="bc899-115">Number of frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc899-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc899-116">Return value</span></span>

<span data-ttu-id="bc899-117">Gibt die Zeit im gepackten TMSF-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="bc899-117">Returns the time in packed TMSF format.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc899-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc899-118">Remarks</span></span>

<span data-ttu-id="bc899-119">Die Zeit im TMSF-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das die Nachverfolgung enthält, dem nächst bedeutsamen Byte mit den Minuten, dem nächstniedrigsten Byte mit den Sekunden und dem signifikantesten Byte mit Frames ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="bc899-119">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="bc899-120">Das **MCI \_ make \_ TMSF** -Makro wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="bc899-120">The **MCI\_MAKE\_TMSF** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_TMSF(t, m, s, f) ((DWORD)(((BYTE)(t) | \ 
                                  ((WORD)(m) << 8)) | \ 
                                  (((DWORD)(BYTE)(s) | \ 
                                  ((WORD)(f) << 8)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="bc899-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc899-121">Requirements</span></span>



| <span data-ttu-id="bc899-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc899-122">Requirement</span></span> | <span data-ttu-id="bc899-123">Wert</span><span class="sxs-lookup"><span data-stu-id="bc899-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bc899-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc899-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bc899-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc899-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bc899-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc899-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bc899-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc899-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bc899-128">Header</span><span class="sxs-lookup"><span data-stu-id="bc899-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc899-129"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc899-129"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc899-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc899-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc899-131">MCI</span><span class="sxs-lookup"><span data-stu-id="bc899-131">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bc899-132">MCI-Makros</span><span class="sxs-lookup"><span data-stu-id="bc899-132">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





