---
title: MMIOM_SEEK Meldung (MMSYSTEM. h)
description: Die mmiom- \_ Suchmeldung wird von der mmioseek-Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass die aktuelle Dateiposition verschoben werden soll.
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- MMIOM_SEEK-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MMIOM_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4855ec4e610f1456e1bf26ee05800e31933f05fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345513"
---
# <a name="mmiom_seek-message"></a><span data-ttu-id="94a5e-104">Mmiom- \_ Suchmeldung</span><span class="sxs-lookup"><span data-stu-id="94a5e-104">MMIOM\_SEEK message</span></span>

<span data-ttu-id="94a5e-105">Die **mmiom- \_ Such** Meldung wird von der [**mmioseek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) -Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass die aktuelle Dateiposition verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="94a5e-105">The **MMIOM\_SEEK** message is sent to an I/O procedure by the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function to request that the current file position be moved.</span></span>


```C++
MMIOM_SEEK 
lParam1 = (LPARAM) lNewFilePos 
lParam2 = (LPARAM) lChangeFlag 
```



## <a name="parameters"></a><span data-ttu-id="94a5e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="94a5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94a5e-107"><span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lnewfilepos*</span><span class="sxs-lookup"><span data-stu-id="94a5e-107"><span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*</span></span>
</dt> <dd>

<span data-ttu-id="94a5e-108">Neue Dateiposition.</span><span class="sxs-lookup"><span data-stu-id="94a5e-108">New file position.</span></span> <span data-ttu-id="94a5e-109">Die Bedeutung dieses Werts hängt von dem in **lchangeflag** angegebenen Flag ab.</span><span class="sxs-lookup"><span data-stu-id="94a5e-109">The meaning of this value is dependent on the flag specified in **lChangeFlag**.</span></span>

</dd> <dt>

<span data-ttu-id="94a5e-110"><span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lchangeflag*</span><span class="sxs-lookup"><span data-stu-id="94a5e-110"><span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*</span></span>
</dt> <dd>

<span data-ttu-id="94a5e-111">Flag, das angibt, wie die Dateiposition geändert wird.</span><span class="sxs-lookup"><span data-stu-id="94a5e-111">Flag specifying how the file position is changed.</span></span> <span data-ttu-id="94a5e-112">Die folgenden Werte sind definiert:</span><span class="sxs-lookup"><span data-stu-id="94a5e-112">The following values are defined:</span></span>



| <span data-ttu-id="94a5e-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94a5e-113">Requirement</span></span> | <span data-ttu-id="94a5e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="94a5e-114">Value</span></span> |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94a5e-115">\_cur suchen</span><span class="sxs-lookup"><span data-stu-id="94a5e-115">SEEK\_CUR</span></span> | <span data-ttu-id="94a5e-116">Verschieben Sie die Dateiposition an der aktuellen Position in *lnewfilepos* bytes.</span><span class="sxs-lookup"><span data-stu-id="94a5e-116">Move the file position to be *lNewFilePos* bytes from the current position.</span></span> <span data-ttu-id="94a5e-117">*lnewfilepos* können positiv oder negativ sein.</span><span class="sxs-lookup"><span data-stu-id="94a5e-117">*lNewFilePos* can be positive or negative.</span></span> |
| <span data-ttu-id="94a5e-118">\_Ende suchen</span><span class="sxs-lookup"><span data-stu-id="94a5e-118">SEEK\_END</span></span> | <span data-ttu-id="94a5e-119">Verschieben Sie die Dateiposition als *lnewfilepos* Bytes vom Dateiende.</span><span class="sxs-lookup"><span data-stu-id="94a5e-119">Move the file position to be *lNewFilePos* bytes from the end of the file.</span></span>                                             |
| <span data-ttu-id="94a5e-120">\_Suchsatz</span><span class="sxs-lookup"><span data-stu-id="94a5e-120">SEEK\_SET</span></span> | <span data-ttu-id="94a5e-121">Verschieben Sie die Dateiposition vom Anfang der Datei in *lnewfilepos* bytes.</span><span class="sxs-lookup"><span data-stu-id="94a5e-121">Move the file position to be *lNewFilePos* bytes from the beginning of the file.</span></span>                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94a5e-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94a5e-122">Return Value</span></span>

<span data-ttu-id="94a5e-123">Gibt die neue Dateiposition zurück.</span><span class="sxs-lookup"><span data-stu-id="94a5e-123">Returns the new file position.</span></span> <span data-ttu-id="94a5e-124">Wenn ein Fehler auftritt, ist der Rückgabewert 1.</span><span class="sxs-lookup"><span data-stu-id="94a5e-124">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="94a5e-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94a5e-125">Remarks</span></span>

<span data-ttu-id="94a5e-126">Die e/a-Prozedur ist dafür verantwortlich, die aktuelle Dateiposition im **ldiskoffset** -Member der [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="94a5e-126">The I/O procedure is responsible for maintaining the current file position in the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="94a5e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94a5e-127">Requirements</span></span>



| <span data-ttu-id="94a5e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94a5e-128">Requirement</span></span> | <span data-ttu-id="94a5e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="94a5e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94a5e-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94a5e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="94a5e-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94a5e-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="94a5e-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94a5e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="94a5e-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94a5e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="94a5e-134">Header</span><span class="sxs-lookup"><span data-stu-id="94a5e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="94a5e-135"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94a5e-135"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

