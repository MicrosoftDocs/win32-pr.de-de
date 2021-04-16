---
title: RECORD_HEADER Struktur
description: Der Daten Satz Header, der von den Changesets für Änderungs \_ Protokoll \_ und Änderungs \_ Protokoll Header verwendet wird \_ .
ms.assetid: f8d2147c-ad13-4be4-94d7-ae0ca26511da
keywords:
- RECORD_HEADER Struktur System Wiederherstellung
- PRECORD_HEADER Struktur Zeiger System Wiederherstellung
topic_type:
- apiref
api_name:
- RECORD_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fd304d2f1b6a5ece08d3d3535aacd7a1abcf614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478291"
---
# <a name="record_header-structure"></a><span data-ttu-id="b197e-105">Daten Satz- \_ Header Struktur</span><span class="sxs-lookup"><span data-stu-id="b197e-105">RECORD\_HEADER structure</span></span>

<span data-ttu-id="b197e-106">\[Diese Informationen gelten nur für Windows XP mit Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="b197e-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="b197e-107">Der Daten Satz Header, der von den Changesets für [**Änderungs \_ Protokoll \_**](change-log-entry.md) und [**Änderungs \_ Protokoll \_ Header**](change-log-header.md) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b197e-107">The record header used by the [**CHANGE\_LOG\_ENTRY**](change-log-entry.md) and [**CHANGE\_LOG\_HEADER**](change-log-header.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="b197e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b197e-108">Syntax</span></span>


```C++
typedef struct _RECORD_HEADER {
  DWORD dwRecordSize;
  DWORD dwRecordType;
} RECORD_HEADER, *PRECORD_HEADER;
```



## <a name="members"></a><span data-ttu-id="b197e-109">Member</span><span class="sxs-lookup"><span data-stu-id="b197e-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="b197e-110">**dwrecordsize**</span><span class="sxs-lookup"><span data-stu-id="b197e-110">**dwRecordSize**</span></span>
</dt> <dd>

<span data-ttu-id="b197e-111">Die Gesamtgröße des Datensatzes, einschließlich des Headers, in Byte.</span><span class="sxs-lookup"><span data-stu-id="b197e-111">The total size of the record, including the header, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b197e-112">**dwrecordtype**</span><span class="sxs-lookup"><span data-stu-id="b197e-112">**dwRecordType**</span></span>
</dt> <dd>

<span data-ttu-id="b197e-113">Der Datensatztyp.</span><span class="sxs-lookup"><span data-stu-id="b197e-113">The record type.</span></span> <span data-ttu-id="b197e-114">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b197e-114">This member may be one of the following values.</span></span>



| <span data-ttu-id="b197e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b197e-115">Value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="b197e-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b197e-116">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RecordTypeLogHeader"></span><span id="recordtypelogheader"></span><span id="RECORDTYPELOGHEADER"></span><dl> <span data-ttu-id="b197e-117"><dt>**Recordtypelogheader**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b197e-117"><dt>**RecordTypeLogHeader**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="b197e-118">Der Datensatz ist die Kopfzeile für das Änderungsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="b197e-118">The record is the header for the change log.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="RecordTypeLogEntry"></span><span id="recordtypelogentry"></span><span id="RECORDTYPELOGENTRY"></span><dl> <span data-ttu-id="b197e-119"><dt>**Recordtypelogentry**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b197e-119"><dt>**RecordTypeLogEntry**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="b197e-120">Der Datensatz ist der Header für einen Änderungsprotokoll Eintrag.</span><span class="sxs-lookup"><span data-stu-id="b197e-120">The record is the header for a change log entry.</span></span><br/>                                                                                                                                                                                                                        |
| <span id="RecordTypeVolumePath"></span><span id="recordtypevolumepath"></span><span id="RECORDTYPEVOLUMEPATH"></span><dl> <span data-ttu-id="b197e-121"><dt>**Recordtypevolumepath**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b197e-121"><dt>**RecordTypeVolumePath**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="b197e-122">Bei den Daten handelt es sich um den Volumepfad für den Änderungsprotokoll Eintrag.</span><span class="sxs-lookup"><span data-stu-id="b197e-122">The data is the volume path for the change log entry.</span></span><br/>                                                                                                                                                                                                                   |
| <span id="RecordTypeFirstPath"></span><span id="recordtypefirstpath"></span><span id="RECORDTYPEFIRSTPATH"></span><dl> <span data-ttu-id="b197e-123"><dt>**Recordtypefirstpath**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b197e-123"><dt>**RecordTypeFirstPath**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="b197e-124">Bei den Daten handelt es sich um den Dateipfad für den Änderungsprotokoll Eintrag.</span><span class="sxs-lookup"><span data-stu-id="b197e-124">The data is the file path for the change log entry.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="RecordTypeSecondPath"></span><span id="recordtypesecondpath"></span><span id="RECORDTYPESECONDPATH"></span><dl> <span data-ttu-id="b197e-125"><dt>**Recordtypesecondpath**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b197e-125"><dt>**RecordTypeSecondPath**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="b197e-126">Die Daten werden verwendet, wenn Änderungsprotokoll Einträge umbenannt werden. in diesem Pfad wird die umbenannte Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b197e-126">The data is used when renaming change log entries; this path is where the renamed file is stored.</span></span><br/>                                                                                                                                                                       |
| <span id="RecordTypeTempPath"></span><span id="recordtypetemppath"></span><span id="RECORDTYPETEMPPATH"></span><dl> <span data-ttu-id="b197e-127"><dt>**Recordtypetemppath**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="b197e-127"><dt>**RecordTypeTempPath**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="b197e-128">Die Daten sind der Name der Sicherungsdatei, die zum Wiederherstellen des Änderungsprotokoll Eintrags verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b197e-128">The data is the name of the backup file used to restore the change log entry.</span></span> <span data-ttu-id="b197e-129">Die Sicherungsdateien befinden sich im Ordner "RP *n* ".</span><span class="sxs-lookup"><span data-stu-id="b197e-129">The backup files are located in the RP *n* folder.</span></span> <span data-ttu-id="b197e-130">Der Dateiname weist das folgende Format auf:*xxxxxxx*. *ext*, wobei *xxxxxxx* eine siebenstellige Zahl und *ext* die Dateinamenerweiterung ist.</span><span class="sxs-lookup"><span data-stu-id="b197e-130">The file name has the following format: A *xxxxxxx*.*ext*, where *xxxxxxx* is a seven-digit number and *ext* is the file name extension.</span></span><br/> |
| <span id="RecordTypeAclInline"></span><span id="recordtypeaclinline"></span><span id="RECORDTYPEACLINLINE"></span><dl> <span data-ttu-id="b197e-131"><dt>**Recordtypeaclinline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b197e-131"><dt>**RecordTypeAclInline**</dt> <dt>6</dt></span></span> </dl>     | <span data-ttu-id="b197e-132">Bei den Daten handelt es sich um eine ACL.</span><span class="sxs-lookup"><span data-stu-id="b197e-132">The data is an ACL.</span></span> <span data-ttu-id="b197e-133">Das Datenformat ist eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="b197e-133">The data format is a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure.</span></span> <br/> <span data-ttu-id="b197e-134">Dieser Wert darf nicht größer als 8.192 Bytes sein.</span><span class="sxs-lookup"><span data-stu-id="b197e-134">This value cannot be larger than 8,192 bytes.</span></span> <span data-ttu-id="b197e-135">Um einen Wert anzugeben, der größer als 8.192 Byte ist, verwenden Sie den **recordtypeaclfile** -Member.</span><span class="sxs-lookup"><span data-stu-id="b197e-135">To specify a value larger than 8,192 bytes, use the **RecordTypeAclFile** member.</span></span><br/>                |
| <span id="RecordTypeAclFile"></span><span id="recordtypeaclfile"></span><span id="RECORDTYPEACLFILE"></span><dl> <span data-ttu-id="b197e-136"><dt>**Recordtypeaclfile**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b197e-136"><dt>**RecordTypeAclFile**</dt> <dt>7</dt></span></span> </dl>             | <span data-ttu-id="b197e-137">Bei den Daten handelt es sich um den Namen der ACL-Datei, die zum Speichern der ACL verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b197e-137">The data is the name of the ACL file used to store the ACL.</span></span> <span data-ttu-id="b197e-138">Die ACL-Dateien befinden sich im Ordner "RP *n* ".</span><span class="sxs-lookup"><span data-stu-id="b197e-138">The ACL files are located in the RP *n* folder.</span></span> <span data-ttu-id="b197e-139">Der Dateiname hat das folgende Format: S *xxxxxxx*. ACL, wobei *xxxxxxx* eine siebenstellige Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="b197e-139">The file name has the following format: S *xxxxxxx*.acl, where *xxxxxxx* is a seven-digit number.</span></span><br/>                                                             |
| <span id="RecordTypeDebugInfo"></span><span id="recordtypedebuginfo"></span><span id="RECORDTYPEDEBUGINFO"></span><dl> <span data-ttu-id="b197e-140"><dt>**Recordtypedebuginfo**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b197e-140"><dt>**RecordTypeDebugInfo**</dt> <dt>8</dt></span></span> </dl>     | <span data-ttu-id="b197e-141">Bei den Daten handelt es sich um Debuginformationen für den Änderungsprotokoll Eintrag.</span><span class="sxs-lookup"><span data-stu-id="b197e-141">The data is debug information for the change log entry.</span></span> <span data-ttu-id="b197e-142">Das Datenformat ist eine **SR \_ log \_ Debug \_ Info** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b197e-142">The data format is a **SR\_LOG\_DEBUG\_INFO** structure.</span></span> <span data-ttu-id="b197e-143">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="b197e-143">For more information, see Remarks.</span></span><br/>                                                                                                                     |
| <span id="RecordTypeShortName"></span><span id="recordtypeshortname"></span><span id="RECORDTYPESHORTNAME"></span><dl> <span data-ttu-id="b197e-144"><dt>**Recordtypeshortname**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="b197e-144"><dt>**RecordTypeShortName**</dt> <dt>9</dt></span></span> </dl>     | <span data-ttu-id="b197e-145">Bei den Daten handelt es sich um den Kurznamen der Sicherungsdatei.</span><span class="sxs-lookup"><span data-stu-id="b197e-145">The data is the short name of the backup file.</span></span><br/>                                                                                                                                                                                                                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b197e-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b197e-146">Remarks</span></span>

<span data-ttu-id="b197e-147">Die **SR \_ log \_ Debug \_ Info** -Struktur ist wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="b197e-147">The **SR\_LOG\_DEBUG\_INFO** structure is defined as follows.</span></span>

``` syntax
typedef struct _SR_LOG_DEBUG_INFO {
    RECORD_HEADER Header;         // log entry header
    HANDLE ThreadId;              // thread identifier
    HANDLE ProcessId;             // process identifier
    ULARGER_INTEGER TimeStamp;    // event time stamp
    CHAR ProcesName[13];          // process name
} SR_LOG_DEBUG_INFO, *PSR_LOG_DEBUG_INFO;
```

## <a name="requirements"></a><span data-ttu-id="b197e-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b197e-148">Requirements</span></span>



| <span data-ttu-id="b197e-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b197e-149">Requirement</span></span> | <span data-ttu-id="b197e-150">Wert</span><span class="sxs-lookup"><span data-stu-id="b197e-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b197e-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b197e-151">Minimum supported client</span></span><br/> | <span data-ttu-id="b197e-152">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b197e-152">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b197e-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b197e-153">Minimum supported server</span></span><br/> | <span data-ttu-id="b197e-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b197e-154">None supported</span></span><br/>                            |
| <span data-ttu-id="b197e-155">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b197e-155">End of client support</span></span><br/>    | <span data-ttu-id="b197e-156">Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="b197e-156">Windows XP with SP2</span></span><br/>                       |



 

