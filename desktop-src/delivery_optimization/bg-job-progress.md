---
title: BG_JOB_PROGRESS-Struktur (deliveryoptimization. h)
description: Die BG_JOB_PROGRESS Struktur bietet auftragsbezogene Statusinformationen, wie z. b. die Anzahl von Bytes und übertragenen Dateien. Bei Uploadaufträgen gilt der Fortschritt für die Uploaddatei, nicht für die Antwortdatei.
ms.assetid: F07BBDDE-FD34-4779-9E17-3789A8098616
keywords:
- BG_JOB_PROGRESS Struktur
topic_type:
- apiref
api_name:
- BG_JOB_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e45c4a2833f80644ff763fc85a6846f9858fb3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518548"
---
# <a name="bg_job_progress-structure"></a><span data-ttu-id="59d34-105">BG_JOB_PROGRESS Struktur</span><span class="sxs-lookup"><span data-stu-id="59d34-105">BG_JOB_PROGRESS structure</span></span>

<span data-ttu-id="59d34-106">Die **BG_JOB_PROGRESS** Struktur bietet auftragsbezogene Statusinformationen, wie z. b. die Anzahl von Bytes und übertragenen Dateien.</span><span class="sxs-lookup"><span data-stu-id="59d34-106">The **BG_JOB_PROGRESS** structure provides job-related progress information, such as the number of bytes and files transferred.</span></span> <span data-ttu-id="59d34-107">Bei Uploadaufträgen gilt der Fortschritt für die Uploaddatei, nicht für die Antwortdatei.</span><span class="sxs-lookup"><span data-stu-id="59d34-107">For upload jobs, the progress applies to the upload file, not the reply file.</span></span>

## <a name="syntax"></a><span data-ttu-id="59d34-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="59d34-108">Syntax</span></span>


```C++
typedef struct _BG_JOB_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  ULONG  FilesTotal;
  ULONG  FilesTransferred;
} BG_JOB_PROGRESS;
```



## <a name="members"></a><span data-ttu-id="59d34-109">Member</span><span class="sxs-lookup"><span data-stu-id="59d34-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="59d34-110">**BytesTotal**</span><span class="sxs-lookup"><span data-stu-id="59d34-110">**BytesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="59d34-111">Gesamtanzahl der Bytes, die für alle Dateien im Auftrag übertragen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="59d34-111">Total number of bytes to transfer for all files in the job.</span></span> <span data-ttu-id="59d34-112">Wenn der Wert BG_SIZE_UNKNOWN ist, wurde die Gesamtgröße aller Dateien im Auftrag nicht ermittelt.</span><span class="sxs-lookup"><span data-stu-id="59d34-112">If the value is BG_SIZE_UNKNOWN, the total size of all files in the job has not been determined.</span></span> <span data-ttu-id="59d34-113">Dieser Wert wird nicht festgelegt, wenn nicht die Größe einer der Dateien bestimmt werden kann.</span><span class="sxs-lookup"><span data-stu-id="59d34-113">DO does not set this value if it cannot determine the size of one of the files.</span></span> <span data-ttu-id="59d34-114">Wenn z. b. die angegebene Datei bzw. der angegebene Server nicht vorhanden ist, kann die Größe der Datei von nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="59d34-114">For example, if the specified file or server does not exist, DO cannot determine the size of the file.</span></span>

<span data-ttu-id="59d34-115">Wenn Sie Bereiche aus der Datei herunterladen, enthält **bytesTotal** die Gesamtzahl der Bytes, die Sie aus der Datei herunterladen möchten.</span><span class="sxs-lookup"><span data-stu-id="59d34-115">If you are downloading ranges from the file, **BytesTotal** includes the total number of bytes you want to download from the file.</span></span>

</dd> <dt>

<span data-ttu-id="59d34-116">**BytesTransferred**</span><span class="sxs-lookup"><span data-stu-id="59d34-116">**BytesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="59d34-117">Anzahl der übertragenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="59d34-117">Number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="59d34-118">**Filestotal**</span><span class="sxs-lookup"><span data-stu-id="59d34-118">**FilesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="59d34-119">Die Gesamtanzahl der Dateien, die für diesen Auftrag übertragen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="59d34-119">Total number of files to transfer for this job.</span></span>

</dd> <dt>

<span data-ttu-id="59d34-120">**Filestransferred**</span><span class="sxs-lookup"><span data-stu-id="59d34-120">**FilesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="59d34-121">Anzahl der übertragenen Dateien.</span><span class="sxs-lookup"><span data-stu-id="59d34-121">Number of files transferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59d34-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59d34-122">Requirements</span></span>



| <span data-ttu-id="59d34-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59d34-123">Requirement</span></span> | <span data-ttu-id="59d34-124">Wert</span><span class="sxs-lookup"><span data-stu-id="59d34-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59d34-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59d34-125">Minimum supported client</span></span><br/> | <span data-ttu-id="59d34-126">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59d34-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="59d34-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59d34-127">Minimum supported server</span></span><br/> | <span data-ttu-id="59d34-128">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59d34-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="59d34-129">Header</span><span class="sxs-lookup"><span data-stu-id="59d34-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="59d34-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="59d34-130"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59d34-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59d34-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59d34-132">**BG_FILE_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="59d34-132">**BG_FILE_PROGRESS**</span></span>](bg-file-progress.md)
</dt> <dt>

[<span data-ttu-id="59d34-133">**Ibackgroundcopyjob:: GetProgress**</span><span class="sxs-lookup"><span data-stu-id="59d34-133">**IBackgroundCopyJob::GetProgress**</span></span>](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





