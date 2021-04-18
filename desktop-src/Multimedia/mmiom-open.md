---
title: MMIOM_OPEN Meldung (MMSYSTEM. h)
description: Die mmiom- \_ Nachricht wird von der mmioopen-Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass eine Datei geöffnet oder gelöscht wird.
ms.assetid: 02b2cf22-21a3-4f49-b90e-7b44478c0168
keywords:
- MMIOM_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MMIOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ea2b5ddc0c79cb3efe00038a628373ce3665bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345531"
---
# <a name="mmiom_open-message"></a><span data-ttu-id="056c8-104">Meldung zum Öffnen von mmiom \_</span><span class="sxs-lookup"><span data-stu-id="056c8-104">MMIOM\_OPEN message</span></span>

<span data-ttu-id="056c8-105">Die **mmiom \_** -Nachricht wird von der [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass eine Datei geöffnet oder gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="056c8-105">The **MMIOM\_OPEN** message is sent to an I/O procedure by the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to request that a file be opened or deleted.</span></span>


```C++
MMIOM_OPEN 
lParam1 = (LPARAM) lpszFileName 
lParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="056c8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="056c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="056c8-107"><span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszfilename*</span><span class="sxs-lookup"><span data-stu-id="056c8-107"><span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*</span></span>
</dt> <dd>

<span data-ttu-id="056c8-108">NULL-terminierte Zeichenfolge, die den Namen der zu öffnenden Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="056c8-108">Null-terminated string containing the name of the file to open.</span></span>

</dd> <dt>

<span data-ttu-id="056c8-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="056c8-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="056c8-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="056c8-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="056c8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="056c8-111">Return Value</span></span>

<span data-ttu-id="056c8-112">Gibt bei Erfolg "mmsyserr \_ noError" zurück oder andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="056c8-112">Returns MMSYSERR\_NOERROR if successful or an error otherwise.</span></span> <span data-ttu-id="056c8-113">Folgende Fehler Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="056c8-113">Possible error values include the following:</span></span>



| <span data-ttu-id="056c8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="056c8-114">Requirement</span></span> | <span data-ttu-id="056c8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="056c8-115">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="056c8-116">mmiom \_ cannotopen</span><span class="sxs-lookup"><span data-stu-id="056c8-116">MMIOM\_CANNOTOPEN</span></span>  | <span data-ttu-id="056c8-117">Die Datei konnte nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="056c8-117">The file could not be opened.</span></span>               |
| <span data-ttu-id="056c8-118">mmiom- \_ outo-Memory</span><span class="sxs-lookup"><span data-stu-id="056c8-118">MMIOM\_OUTOFMEMORY</span></span> | <span data-ttu-id="056c8-119">Der Arbeitsspeicher reicht nicht aus, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="056c8-119">Not enough memory to perform the operation.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="056c8-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="056c8-120">Remarks</span></span>

<span data-ttu-id="056c8-121">Der **dwFlags** -Member der [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur enthält Flags, die an die [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="056c8-121">The **dwFlags** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure contains flags passed to the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span>

<span data-ttu-id="056c8-122">Der **ldiskoffset** -Member der [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur wird mit 0 (null) initialisiert.</span><span class="sxs-lookup"><span data-stu-id="056c8-122">The **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure is initialized to zero.</span></span> <span data-ttu-id="056c8-123">Wenn dieser Wert falsch ist, muss er von der e/a-Prozedur korrigiert werden.</span><span class="sxs-lookup"><span data-stu-id="056c8-123">If this value is incorrect, the I/O procedure must correct it.</span></span>

<span data-ttu-id="056c8-124">Wenn die Anwendung eine [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur an [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)übergeben hat, wird der Rückgabewert im **werrorret** -Member zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="056c8-124">If the application passed an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), the return value is returned in the **wErrorRet** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="056c8-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="056c8-125">Requirements</span></span>



| <span data-ttu-id="056c8-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="056c8-126">Requirement</span></span> | <span data-ttu-id="056c8-127">Wert</span><span class="sxs-lookup"><span data-stu-id="056c8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="056c8-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="056c8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="056c8-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="056c8-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="056c8-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="056c8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="056c8-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="056c8-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="056c8-132">Header</span><span class="sxs-lookup"><span data-stu-id="056c8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="056c8-133"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="056c8-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

