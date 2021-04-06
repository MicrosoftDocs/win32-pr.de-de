---
title: BG_FILE_PROGRESS-Struktur (deliveryoptimization. h)
description: Die BG_FILE_PROGRESS-Struktur liefert Datei bezogene Statusinformationen, wie z. b. die Anzahl der übertragenen Bytes.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- BG_FILE_PROGRESS Struktur
topic_type:
- apiref
api_name:
- BG_FILE_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 93507b8aeefa9c0ea16f70f67e221ecc4218427f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742865"
---
# <a name="bg_file_progress-structure"></a><span data-ttu-id="07c38-104">BG_FILE_PROGRESS Struktur</span><span class="sxs-lookup"><span data-stu-id="07c38-104">BG_FILE_PROGRESS structure</span></span>

<span data-ttu-id="07c38-105">Die **BG_FILE_PROGRESS** -Struktur liefert Datei bezogene Statusinformationen, wie z. b. die Anzahl der übertragenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="07c38-105">The **BG_FILE_PROGRESS** structure provides file-related progress information, such as the number of bytes transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="07c38-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="07c38-106">Syntax</span></span>


```C++
typedef struct _BG_FILE_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  BOOL   Completed;
} BG_FILE_PROGRESS;
```



## <a name="members"></a><span data-ttu-id="07c38-107">Member</span><span class="sxs-lookup"><span data-stu-id="07c38-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="07c38-108">**BytesTotal**</span><span class="sxs-lookup"><span data-stu-id="07c38-108">**BytesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="07c38-109">Die Länge der Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="07c38-109">Size of the file in bytes.</span></span> <span data-ttu-id="07c38-110">Wenn die Größe der Datei nicht ermitteln kann (z. b. wenn die Datei oder der Server nicht vorhanden ist), wird der Wert DO_UNKNOWN_FILE_SIZE.</span><span class="sxs-lookup"><span data-stu-id="07c38-110">If DO cannot determine the size of the file (for example, if the file or server does not exist), the value is DO_UNKNOWN_FILE_SIZE.</span></span>

<span data-ttu-id="07c38-111">Wenn Sie Bereiche aus einer Datei herunterladen, spiegelt **bytesTotal** die Gesamtzahl der Bytes wider, die Sie aus der Datei herunterladen möchten.</span><span class="sxs-lookup"><span data-stu-id="07c38-111">If you are downloading ranges from a file, **BytesTotal** reflects the total number of bytes you want to download from the file.</span></span>

</dd> <dt>

<span data-ttu-id="07c38-112">**BytesTransferred**</span><span class="sxs-lookup"><span data-stu-id="07c38-112">**BytesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="07c38-113">Anzahl der übertragenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="07c38-113">Number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="07c38-114">**Abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="07c38-114">**Completed**</span></span>
</dt> <dd>

<span data-ttu-id="07c38-115">Für Downloads ist der Wert **true** , wenn die Datei für den Benutzer verfügbar ist. Andernfalls ist der Wert **false**.</span><span class="sxs-lookup"><span data-stu-id="07c38-115">For downloads, the value is **TRUE** if the file is available to the user; otherwise, the value is **FALSE**.</span></span> <span data-ttu-id="07c38-116">Dateien sind nach dem Aufrufen der [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) -Methode für den Benutzer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07c38-116">Files are available to the user after calling the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span> <span data-ttu-id="07c38-117">Wenn die **Complete** -Methode einen vorübergehenden Fehler generiert, sind die Dateien, die vor dem Auftreten des Fehlers verarbeitet wurden, für den Benutzer verfügbar. bei anderen handelt es sich nicht um.</span><span class="sxs-lookup"><span data-stu-id="07c38-117">If the **Complete** method generates a transient error, those files processed before the error occurred are available to the user; the others are not.</span></span> <span data-ttu-id="07c38-118">Verwenden Sie den **abgeschlossenen** Member, um zu ermitteln, ob die Datei für den Benutzer verfügbar ist, wenn der Vorgang **abgeschlossen** ist.</span><span class="sxs-lookup"><span data-stu-id="07c38-118">Use the **Completed** member to determine if the file is available to the user when **Complete** fails.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07c38-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07c38-119">Remarks</span></span>

<span data-ttu-id="07c38-120">Um festzustellen, ob die Datei übertragen wird, haben Sie folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="07c38-120">To determine if DO transferred the file, you can:</span></span>

-   <span data-ttu-id="07c38-121">Vergleichen Sie **bytesTransferred** mit **bytesTotal**.</span><span class="sxs-lookup"><span data-stu-id="07c38-121">Compare **BytesTransferred** to **BytesTotal**.</span></span>

## <a name="requirements"></a><span data-ttu-id="07c38-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07c38-122">Requirements</span></span>



| <span data-ttu-id="07c38-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07c38-123">Requirement</span></span> | <span data-ttu-id="07c38-124">Wert</span><span class="sxs-lookup"><span data-stu-id="07c38-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07c38-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07c38-125">Minimum supported client</span></span><br/> | <span data-ttu-id="07c38-126">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07c38-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="07c38-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07c38-127">Minimum supported server</span></span><br/> | <span data-ttu-id="07c38-128">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07c38-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="07c38-129">Header</span><span class="sxs-lookup"><span data-stu-id="07c38-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="07c38-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="07c38-130"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07c38-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07c38-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c38-132">**BG_JOB_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="07c38-132">**BG_JOB_PROGRESS**</span></span>](bg-job-progress.md)
</dt> <dt>

[<span data-ttu-id="07c38-133">**Ibackgroundcopyfile:: GetProgress**</span><span class="sxs-lookup"><span data-stu-id="07c38-133">**IBackgroundCopyFile::GetProgress**</span></span>](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





