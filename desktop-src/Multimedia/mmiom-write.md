---
title: MMIOM_WRITE Meldung (MMSYSTEM. h)
description: Die mmiom- \_ Schreib Nachricht wird von der mmiowrite-Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass Daten in eine geöffnete Datei geschrieben werden.
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- MMIOM_WRITE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MMIOM_WRITE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27cf96827f803608c369cc9022faa6235add9ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957085"
---
# <a name="mmiom_write-message"></a><span data-ttu-id="741ac-104">Mmiom- \_ Schreib Nachricht</span><span class="sxs-lookup"><span data-stu-id="741ac-104">MMIOM\_WRITE message</span></span>

<span data-ttu-id="741ac-105">Die **mmiom- \_ Schreib** Nachricht wird von der [**mmiowrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) -Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass Daten in eine geöffnete Datei geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="741ac-105">The **MMIOM\_WRITE** message is sent to an I/O procedure by the [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) function to request that data be written to an open file.</span></span>


```C++
MMIOM_WRITE 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a><span data-ttu-id="741ac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="741ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="741ac-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span><span class="sxs-lookup"><span data-stu-id="741ac-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="741ac-108">Zeiger auf einen Puffer, der die Daten enthält, die in die Datei geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="741ac-108">Pointer to a buffer containing the data to write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="741ac-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbwrite*</span><span class="sxs-lookup"><span data-stu-id="741ac-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span></span>
</dt> <dd>

<span data-ttu-id="741ac-110">Anzahl von Bytes, die in die Datei geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="741ac-110">Number of bytes to write to file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="741ac-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="741ac-111">Return Value</span></span>

<span data-ttu-id="741ac-112">Gibt die Anzahl der Bytes zurück, die tatsächlich in die Datei geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="741ac-112">Returns the number of bytes actually written to the file.</span></span> <span data-ttu-id="741ac-113">Wenn ein Fehler auftritt, ist der Rückgabewert 1.</span><span class="sxs-lookup"><span data-stu-id="741ac-113">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="741ac-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="741ac-114">Remarks</span></span>

<span data-ttu-id="741ac-115">Die e/a-Prozedur ist dafür verantwortlich, den **ldiskoffset** -Member der [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur zu aktualisieren, um die neue Dateiposition nach dem Schreibvorgang widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="741ac-115">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the write operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="741ac-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="741ac-116">Requirements</span></span>



| <span data-ttu-id="741ac-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="741ac-117">Requirement</span></span> | <span data-ttu-id="741ac-118">Wert</span><span class="sxs-lookup"><span data-stu-id="741ac-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="741ac-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="741ac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="741ac-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="741ac-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="741ac-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="741ac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="741ac-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="741ac-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="741ac-123">Header</span><span class="sxs-lookup"><span data-stu-id="741ac-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="741ac-124"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="741ac-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

