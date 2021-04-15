---
title: MMIOM_RENAME Meldung (MMSYSTEM. h)
description: Die mmiom- \_ Umbenennungs Meldung wird von der mmiorename-Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass die angegebene Datei umbenannt wird.
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- MMIOM_RENAME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MMIOM_RENAME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71770dec6a92693a50e8e0210da3f9b8028587c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478456"
---
# <a name="mmiom_rename-message"></a><span data-ttu-id="4eac7-104">Mmiom- \_ Umbenennungs Meldung</span><span class="sxs-lookup"><span data-stu-id="4eac7-104">MMIOM\_RENAME message</span></span>

<span data-ttu-id="4eac7-105">Die **mmiom- \_ Umbenennungs** Meldung wird von der [**mmiorename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) -Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass die angegebene Datei umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="4eac7-105">The **MMIOM\_RENAME** message is sent to an I/O procedure by the [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) function to request that the specified file be renamed.</span></span>


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a><span data-ttu-id="4eac7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4eac7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eac7-107"><span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszoldfilename*</span><span class="sxs-lookup"><span data-stu-id="4eac7-107"><span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*</span></span>
</dt> <dd>

<span data-ttu-id="4eac7-108">Ein Zeiger auf eine Zeichenfolge, die den Dateinamen der umzubenennenden Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="4eac7-108">Pointer to a string containing the filename of the file to rename.</span></span>

</dd> <dt>

<span data-ttu-id="4eac7-109"><span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpsznewfilename*</span><span class="sxs-lookup"><span data-stu-id="4eac7-109"><span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*</span></span>
</dt> <dd>

<span data-ttu-id="4eac7-110">Zeiger auf eine Zeichenfolge, die den neuen Dateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="4eac7-110">Pointer to a string containing the new filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eac7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4eac7-111">Return Value</span></span>

<span data-ttu-id="4eac7-112">Wenn die Datei erfolgreich umbenannt wurde, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="4eac7-112">If the file is renamed successfully, the return value is zero.</span></span> <span data-ttu-id="4eac7-113">Wenn die angegebene Datei nicht gefunden wurde, lautet der Rückgabewert mmioerr \_ fileotfound.</span><span class="sxs-lookup"><span data-stu-id="4eac7-113">If the specified file was not found, the return value is MMIOERR\_FILENOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eac7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4eac7-114">Requirements</span></span>



| <span data-ttu-id="4eac7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4eac7-115">Requirement</span></span> | <span data-ttu-id="4eac7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4eac7-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eac7-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4eac7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4eac7-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4eac7-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4eac7-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4eac7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4eac7-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4eac7-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4eac7-121">Header</span><span class="sxs-lookup"><span data-stu-id="4eac7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eac7-122"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4eac7-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

