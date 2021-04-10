---
title: CHANGE_LOG_ENTRY Struktur
description: Ein Änderungsprotokoll Eintrag.
ms.assetid: adbdc6e6-895e-486d-a194-c74d2cbd0052
keywords:
- CHANGE_LOG_ENTRY Struktur System Wiederherstellung
- PCHANGE_LOG_ENTRY Struktur Zeiger System Wiederherstellung
topic_type:
- apiref
api_name:
- CHANGE_LOG_ENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a129b7c8368e6af1d259d6c19a9dde963d9deef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040250"
---
# <a name="change_log_entry-structure"></a><span data-ttu-id="0847d-105">\_Struktur der Protokoll \_ Einträge ändern</span><span class="sxs-lookup"><span data-stu-id="0847d-105">CHANGE\_LOG\_ENTRY structure</span></span>

<span data-ttu-id="0847d-106">\[Diese Informationen gelten nur für Windows XP mit Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="0847d-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="0847d-107">Ein Änderungsprotokoll Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0847d-107">A change log entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="0847d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0847d-108">Syntax</span></span>


```C++
typedef struct _CHANGE_LOG_ENTRY {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwEntryType;
  DWORD         dwEntryFlags;
  DWORD         dwAttributes;
  INT64         i64SequenceNum;
  WCHAR         szProcName[16];
} CHANGE_LOG_ENTRY, *PCHANGE_LOG_ENTRY;
```



## <a name="members"></a><span data-ttu-id="0847d-109">Member</span><span class="sxs-lookup"><span data-stu-id="0847d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="0847d-110">**Recordheader**</span><span class="sxs-lookup"><span data-stu-id="0847d-110">**RecordHeader**</span></span>
</dt> <dd>

<span data-ttu-id="0847d-111">Eine [**Daten Satz \_ Header**](record-header.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0847d-111">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="0847d-112">Der **dwrecordtype** -Member sollte auf **recordtypelogentry** (1) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0847d-112">The **dwRecordType** member should be set to **RecordTypeLogEntry** (1).</span></span>

</dd> <dt>

<span data-ttu-id="0847d-113">**dwmagicnum**</span><span class="sxs-lookup"><span data-stu-id="0847d-113">**dwMagicNum**</span></span>
</dt> <dd>

<span data-ttu-id="0847d-114">Dieser Member sollte auf 0xabcdef12 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0847d-114">This member should be set to 0xabcdef12.</span></span>

</dd> <dt>

<span data-ttu-id="0847d-115">**dwentrytype**</span><span class="sxs-lookup"><span data-stu-id="0847d-115">**dwEntryType**</span></span>
</dt> <dd>

<span data-ttu-id="0847d-116">Dieser Member kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="0847d-116">This member can be one of the following values:</span></span>

<dl><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0x2_"></span><span id="change_log_entrytypes_aclchange__0x2_"></span><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0X2_"></span><dt>

<span data-ttu-id="0847d-117">Change \_ \_ logentrytypes \_ aclchange \* \* (0x2) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-117">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ACLCHANGE\*\* (0x2)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0x4_"></span><span id="change_log_entrytypes_attrchange__0x4_"></span><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0X4_"></span><dt>

<span data-ttu-id="0847d-118">Change \_ \_ logentrytypes \_ attrchange \* \* (0x4) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-118">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ATTRCHANGE\*\* (0x4)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0x80_"></span><span id="change_log_entrytypes_dircreate__0x80_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0X80_"></span><dt>

<span data-ttu-id="0847d-119">Change \_ \_ logentrytypes \_ dircreate \* \* (0x80) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-119">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRCREATE\*\* (0x80)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0x100_"></span><span id="change_log_entrytypes_dirrename__0x100_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0X100_"></span><dt>

<span data-ttu-id="0847d-120">Change \_ \_ logentrytypes \_ dirrename \* \* (0x100) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-120">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRRENAME\*\* (0x100)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0x200_"></span><span id="change_log_entrytypes_dirdelete__0x200_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0X200_"></span><dt>

<span data-ttu-id="0847d-121">Change \_ \_ logentrytypes \_ dirdelete \* \* (0x200) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-121">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRDELETE\*\* (0x200)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0x20_"></span><span id="change_log_entrytypes_filecreate__0x20_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0X20_"></span><dt>

<span data-ttu-id="0847d-122">Change \_ \_ logentrytypes \_ filecreate \* \* (0x20) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-122">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILECREATE\*\* (0x20)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0x10_"></span><span id="change_log_entrytypes_filedelete__0x10_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0X10_"></span><dt>

<span data-ttu-id="0847d-123">Change \_ \_ logentrytypes \_ filedelete \* \* (0x10) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-123">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILEDELETE\*\* (0x10)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0x40_"></span><span id="change_log_entrytypes_filerename__0x40_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0X40_"></span><dt>

<span data-ttu-id="0847d-124">Change \_ \_ logentrytypes \_ filerename \* \* (0x40) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-124">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILERENAME\*\* (0x40)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0x100000_"></span><span id="change_log_entrytypes_inprecreate__0x100000_"></span><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0X100000_"></span><dt>

<span data-ttu-id="0847d-125">Change \_ \_ logentrytypes \_ inprecreate \* \* (0x100000) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-125">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_INPRECREATE\*\* (0x100000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0x20000_"></span><span id="change_log_entrytypes_isdir__0x20000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0X20000_"></span><dt>

<span data-ttu-id="0847d-126">Change \_ \_ logentrytypes \_ isDir \* \* (0x20000) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-126">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ISDIR\*\* (0x20000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0x40000_"></span><span id="change_log_entrytypes_isnotdir__0x40000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0X40000_"></span><dt>

<span data-ttu-id="0847d-127">Change \_ \_ logentrytypes \_ isnotdir \* \* (0x40000) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-127">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ISNOTDIR\*\* (0x40000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0x400_"></span><span id="change_log_entrytypes_mountcreate__0x400_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0X400_"></span><dt>

<span data-ttu-id="0847d-128">Change \_ \_ logentrytypes \_ mountcreate \* \* (0x400) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-128">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_MOUNTCREATE\*\* (0x400)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0x800_"></span><span id="change_log_entrytypes_mountdelete__0x800_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0X800_"></span><dt>

<span data-ttu-id="0847d-129">Change \_ \_ logentrytypes \_ mountdelete \* \* (0x800) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-129">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_MOUNTDELETE\*\* (0x800)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0x10000_"></span><span id="change_log_entrytypes_nooptimize__0x10000_"></span><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0X10000_"></span><dt>

<span data-ttu-id="0847d-130">Change \_ \_ logentrytypes \_ nooptimiert \* \* (0x10000) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-130">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_NOOPTIMIZE\*\* (0x10000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0x200000_"></span><span id="change_log_entrytypes_openbyid__0x200000_"></span><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0X200000_"></span><dt>

<span data-ttu-id="0847d-131">Change \_ \_ logentrytypes \_ openbyid \* \* (0x200000) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-131">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_OPENBYID\*\* (0x200000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0x80000_"></span><span id="change_log_entrytypes_simulatedelete__0x80000_"></span><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0X80000_"></span><dt>

<span data-ttu-id="0847d-132">Change \_ \_ logentrytypes \_ simulatedelete \* \* (0x80000) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-132">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_SIMULATEDELETE\*\* (0x80000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0x1_"></span><span id="change_log_entrytypes_streamchange__0x1_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0X1_"></span><dt>

<span data-ttu-id="0847d-133">Change \_ \_ logentrytypes \_ streamchange \* \* (0x1) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-133">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMCHANGE\*\* (0x1)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0x2000_"></span><span id="change_log_entrytypes_streamcreate__0x2000_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0X2000_"></span><dt>

<span data-ttu-id="0847d-134">Change \_ \_ logentrytypes \_ streamcreate \* \* (0x2000) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-134">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMCREATE\*\* (0x2000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0x8_"></span><span id="change_log_entrytypes_streamoverwrite__0x8_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0X8_"></span><dt>

<span data-ttu-id="0847d-135">Change \_ \_ logentrytypes \_ streamüberschreit \* \* (0x8) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-135">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMOVERWRITE\*\* (0x8)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0x1000_"></span><span id="change_log_entrytypes_volumeerror__0x1000_"></span><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0X1000_"></span><dt>

<span data-ttu-id="0847d-136">Change \_ \_ logentrytypes \_ volumeerror \* \* (0x1000) \* \*</span><span class="sxs-lookup"><span data-stu-id="0847d-136">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_VOLUMEERROR\*\* (0x1000)\*\*</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="0847d-137">**dwentryflags**</span><span class="sxs-lookup"><span data-stu-id="0847d-137">**dwEntryFlags**</span></span>
</dt> <dd>

<span data-ttu-id="0847d-138">Dieser Member kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="0847d-138">This member can be one of the following values:</span></span>

<dl><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0x4_"></span><span id="change_log_entryflags_aclinfo__0x4_"></span><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0X4_"></span><dt>

<span data-ttu-id="0847d-139">**Changesets- \_ \_ \_ aclinfo ändern (0x4)**</span><span class="sxs-lookup"><span data-stu-id="0847d-139">**CHANGE\_LOG\_ENTRYFLAGS\_ACLINFO (0x4)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0x8_"></span><span id="change_log_entryflags_debuginfo__0x8_"></span><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0X8_"></span><dt>

<span data-ttu-id="0847d-140">**Change \_ \_ logentryflags \_ debuginfo (0x8)**</span><span class="sxs-lookup"><span data-stu-id="0847d-140">**CHANGE\_LOG\_ENTRYFLAGS\_DEBUGINFO (0x8)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0x2_"></span><span id="change_log_entryflags_secondpath__0x2_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0X2_"></span><dt>

<span data-ttu-id="0847d-141">**Change \_ \_ logentryflags \_ secondpath (0x2)**</span><span class="sxs-lookup"><span data-stu-id="0847d-141">**CHANGE\_LOG\_ENTRYFLAGS\_SECONDPATH (0x2)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0x10_"></span><span id="change_log_entryflags_shortname__0x10_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0X10_"></span><dt>

<span data-ttu-id="0847d-142">**Changesetflags- \_ \_ \_ Kurzname ändern (0x10)**</span><span class="sxs-lookup"><span data-stu-id="0847d-142">**CHANGE\_LOG\_ENTRYFLAGS\_SHORTNAME (0x10)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0x1_"></span><span id="change_log_entryflags_temppath__0x1_"></span><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0X1_"></span><dt>

<span data-ttu-id="0847d-143">**Change \_ \_ logentryflags \_ TEMPPATH (0x1)**</span><span class="sxs-lookup"><span data-stu-id="0847d-143">**CHANGE\_LOG\_ENTRYFLAGS\_TEMPPATH (0x1)**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="0847d-144">**dwattributes**</span><span class="sxs-lookup"><span data-stu-id="0847d-144">**dwAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="0847d-145">Die Dateiattribute der Änderungsprotokoll Datei.</span><span class="sxs-lookup"><span data-stu-id="0847d-145">The file attributes of the change log file.</span></span> <span data-ttu-id="0847d-146">Wenn keine Attribute angegeben werden, sollte dieser Wert auf "0xffffffff" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0847d-146">If no attributes are specified, this value should be set to 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="0847d-147">**i64SequenceNum**</span><span class="sxs-lookup"><span data-stu-id="0847d-147">**i64SequenceNum**</span></span>
</dt> <dd>

<span data-ttu-id="0847d-148">Die Sequenznummer, die dem Änderungsprotokoll Eintrag zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0847d-148">The sequence number assigned to the change log entry.</span></span>

</dd> <dt>

<span data-ttu-id="0847d-149">**szprocname**</span><span class="sxs-lookup"><span data-stu-id="0847d-149">**szProcName**</span></span>
</dt> <dd>

<span data-ttu-id="0847d-150">Der Name des Prozesses, der die Änderung vornimmt.</span><span class="sxs-lookup"><span data-stu-id="0847d-150">The name of the process making the change.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0847d-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0847d-151">Remarks</span></span>

<span data-ttu-id="0847d-152">Auf diese Struktur folgt eine Variable Anzahl von Datensätzen variabler Länge sowie ein **DWORD** -Wert, der mit dem Wert des **dwrecordsize** -Members von **recordheader** identisch sein sollte.</span><span class="sxs-lookup"><span data-stu-id="0847d-152">This structure is followed by a variable number of variable-length data records, plus a **DWORD** value that should be identical to the value of the **dwRecordSize** member of **RecordHeader**.</span></span>

<span data-ttu-id="0847d-153">Die Datensätze variabler Länge bestehen aus einer Daten [**Satz \_ Header**](record-header.md) Struktur sowie aus Daten, die verwendet werden können, um den Änderungsprotokoll Eintrag wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="0847d-153">The variable-length data records consist of a [**RECORD\_HEADER**](record-header.md) structure plus data that can be used to restore the change log entry.</span></span> <span data-ttu-id="0847d-154">Das Format der Daten hängt vom Wert des **dwrecordtype** -Members der **Datensatz- \_ Header** Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="0847d-154">The format of the data depends on the value of the **dwRecordType** member of the **RECORD\_HEADER** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0847d-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0847d-155">Requirements</span></span>



| <span data-ttu-id="0847d-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0847d-156">Requirement</span></span> | <span data-ttu-id="0847d-157">Wert</span><span class="sxs-lookup"><span data-stu-id="0847d-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0847d-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0847d-158">Minimum supported client</span></span><br/> | <span data-ttu-id="0847d-159">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0847d-159">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0847d-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0847d-160">Minimum supported server</span></span><br/> | <span data-ttu-id="0847d-161">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0847d-161">None supported</span></span><br/>                            |
| <span data-ttu-id="0847d-162">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0847d-162">End of client support</span></span><br/>    | <span data-ttu-id="0847d-163">Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="0847d-163">Windows XP with SP2</span></span><br/>                       |



 

 





