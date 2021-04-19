---
description: 'Weitere Informationen finden Sie hier: JET_LOGINFO Struktur'
title: JET_LOGINFO Struktur
TOCTitle: JET_LOGINFO Structure
ms:assetid: b34b3f24-5d19-4e11-a657-a0e59204d628
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294063(v=EXCHG.10)
ms:contentKeyID: 32765678
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7e643d775d1fb8e0c19286bfb7a50d887644e99
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106350741"
---
# <a name="jet_loginfo-structure"></a><span data-ttu-id="79c8d-103">JET_LOGINFO Struktur</span><span class="sxs-lookup"><span data-stu-id="79c8d-103">JET_LOGINFO Structure</span></span>


<span data-ttu-id="79c8d-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="79c8d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_loginfo-structure"></a><span data-ttu-id="79c8d-105">JET_LOGINFO Struktur</span><span class="sxs-lookup"><span data-stu-id="79c8d-105">JET_LOGINFO Structure</span></span>

<span data-ttu-id="79c8d-106">Die **JET_LOGINFO** -Struktur gibt strukturierte Informationen über den Satz von Transaktionsprotokoll Dateien zurück, die Teil eines Sicherungsdatei Satzes sein sollten.</span><span class="sxs-lookup"><span data-stu-id="79c8d-106">The **JET_LOGINFO** structure returns structured information about the set of transaction log files that should be a part of a backup file set.</span></span> <span data-ttu-id="79c8d-107">Die **JET_LOGINFO** Struktur ist der minimale Satz von Informationen, die erforderlich sind, um einen Bereich von Protokollen darzustellen, der mit [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) abgerufen oder für eine feste Wiederherstellung mit [JetExternalRestore2](./jetexternalrestore2-function.md)angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="79c8d-107">The **JET_LOGINFO** structure is the minimal set of information needed to represent a range of logs that is retrieved with [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) or specified for a hard recovery with [JetExternalRestore2](./jetexternalrestore2-function.md).</span></span>

```cpp
typedef struct {
  unsigned long cbSize;
  unsigned long ulGenLow;
  unsigned long ulGenHigh;
  tchar szBaseName[JET_BASE_NAME_LENGTH + 1];
} JET_LOGINFO;
```

### <a name="members"></a><span data-ttu-id="79c8d-108">Member</span><span class="sxs-lookup"><span data-stu-id="79c8d-108">Members</span></span>

<span data-ttu-id="79c8d-109">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="79c8d-109">**cbSize**</span></span>

<span data-ttu-id="79c8d-110">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="79c8d-110">The size of the structure, in bytes.</span></span>

<span data-ttu-id="79c8d-111">Dieser Member ermöglicht die zukünftige Erweiterung dieser Struktur, während die Abwärtskompatibilität aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="79c8d-111">This member enables future expansion of this structure while enabling backwards compatibility.</span></span> <span data-ttu-id="79c8d-112">Er sollte immer auf sizeof (JET_LOGINFO) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="79c8d-112">It should always be set to sizeof( JET_LOGINFO ).</span></span>

<span data-ttu-id="79c8d-113">**ulgenlow**</span><span class="sxs-lookup"><span data-stu-id="79c8d-113">**ulGenLow**</span></span>

<span data-ttu-id="79c8d-114">Die niedrigste (oder älteste) Protokolldatei Nummer, die wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="79c8d-114">The lowest (or oldest) log file number that is restored.</span></span> <span data-ttu-id="79c8d-115">Die vollständige Genauigkeit eines langen Zeichens ohne Vorzeichen sollte beibehalten werden, aber in den aktuellen Versionen der Engine ist diese Zahl eine hexadezimale Zahl im Bereich von 0x00000 bis 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="79c8d-115">The full fidelity of an unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="79c8d-116">Dies kann sich in zukünftigen Versionen ändern.</span><span class="sxs-lookup"><span data-stu-id="79c8d-116">This might change in future versions.</span></span>

<span data-ttu-id="79c8d-117">**ulgenhigh**</span><span class="sxs-lookup"><span data-stu-id="79c8d-117">**ulGenHigh**</span></span>

<span data-ttu-id="79c8d-118">Die höchste (oder letzte) Protokolldatei Nummer, die wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="79c8d-118">The highest (or most recent) log file number that is restored.</span></span> <span data-ttu-id="79c8d-119">Die vollständige Genauigkeit eines langen Zeichens ohne Vorzeichen sollte beibehalten werden, aber in den aktuellen Versionen der Engine ist diese Zahl eine hexadezimale Zahl im Bereich von 0x00000 bis 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="79c8d-119">The full fidelity of a unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="79c8d-120">Dies kann sich in zukünftigen Versionen ändern.</span><span class="sxs-lookup"><span data-stu-id="79c8d-120">This might change in future versions.</span></span>

<span data-ttu-id="79c8d-121">**szbasename**</span><span class="sxs-lookup"><span data-stu-id="79c8d-121">**szBaseName**</span></span>

<span data-ttu-id="79c8d-122">Das Präfix, das zum Benennen der Transaktionsprotokoll Dateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="79c8d-122">The prefix used to name the transaction log files.</span></span>

<span data-ttu-id="79c8d-123">Der Wert, der in diesem Member zurückgegeben wird, entspricht immer der-Einstellung für [JET_paramBaseName](./transaction-log-parameters.md) für die-Instanz, die diese Informationen generiert hat.</span><span class="sxs-lookup"><span data-stu-id="79c8d-123">The value that is returned in this member is always equal to the setting for [JET_paramBaseName](./transaction-log-parameters.md) for the instance that generated this information.</span></span>

### <a name="remarks"></a><span data-ttu-id="79c8d-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79c8d-124">Remarks</span></span>

<span data-ttu-id="79c8d-125">Transaktionsprotokoll Dateien werden nach dem instanzbasisnamen und der Generations Nummer der Protokolldatei benannt.</span><span class="sxs-lookup"><span data-stu-id="79c8d-125">Transaction log files are named according to the instance base name and the generation number of the log file.</span></span> <span data-ttu-id="79c8d-126">Der Name hat das Format "bbbxxxxx". Angezeigt.</span><span class="sxs-lookup"><span data-stu-id="79c8d-126">The name is of the format BBBXXXXX.LOG.</span></span> <span data-ttu-id="79c8d-127">BBB entspricht dem Basis Namen für die Protokolldatei und weist immer eine Länge von drei Zeichen auf.</span><span class="sxs-lookup"><span data-stu-id="79c8d-127">BBB corresponds to the base name for the log file and is always three characters in length.</span></span> <span data-ttu-id="79c8d-128">Xxxxx entspricht der Generations Nummer der Protokolldatei in 0 (null) und ist immer fünf Zeichen lang.</span><span class="sxs-lookup"><span data-stu-id="79c8d-128">XXXXX corresponds to the generation number of the log file in zero padded hexadecimal and is always five characters in length.</span></span> <span data-ttu-id="79c8d-129">Log ist die Dateierweiterung, die von der-Engine immer an Transaktionsprotokoll Dateien übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="79c8d-129">LOG is the file extension that is always given to transaction log files by the engine.</span></span>

<span data-ttu-id="79c8d-130">Es wird davon abgeraten, diese strukturierten Informationen zu verwenden, da die Anwendung das Benennungs Schema für Transaktionsprotokoll Dateien mit einem Grundkenntnissen kennt.</span><span class="sxs-lookup"><span data-stu-id="79c8d-130">Use of this structured information is discouraged because it causes the application to have intimate knowledge of this naming scheme for transaction log files.</span></span> <span data-ttu-id="79c8d-131">Wenn das Benennungs Schema in Zukunft geändert wird, funktioniert eine solche Anwendung nicht mehr ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="79c8d-131">If the naming scheme ever changes in the future then such an application will no longer function properly.</span></span> <span data-ttu-id="79c8d-132">Es ist zu berücksichtigen, dass sich das Protokoll Format in Zukunft in 8 hexadezimal Ziffern einfügt.</span><span class="sxs-lookup"><span data-stu-id="79c8d-132">It is conceivable that the log format will change to incorporate 8 hex digits in the future.</span></span> <span data-ttu-id="79c8d-133">Anwendungen sollten stattdessen die explizite Liste der von [jetgetloginfo](./jetgetloginfo-function.md) zurückgegebenen Dateinamen verwenden.</span><span class="sxs-lookup"><span data-stu-id="79c8d-133">Applications should use the explicit list of file names returned by [JetGetLogInfo](./jetgetloginfo-function.md) instead.</span></span>

### <a name="requirements"></a><span data-ttu-id="79c8d-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79c8d-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79c8d-135"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="79c8d-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="79c8d-136">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="79c8d-136">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79c8d-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="79c8d-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="79c8d-138">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="79c8d-138">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79c8d-139"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="79c8d-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="79c8d-140">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="79c8d-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79c8d-141"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="79c8d-141"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="79c8d-142">Wird als <strong>JET_LOGINFO_W</strong> (Unicode) und <strong>JET_LOGINFO_A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="79c8d-142">Implemented as <strong>JET_LOGINFO_W</strong> (Unicode) and <strong>JET_LOGINFO_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="79c8d-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="79c8d-143">See Also</span></span>

[<span data-ttu-id="79c8d-144">JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="79c8d-144">JetExternalRestore2</span></span>](./jetexternalrestore2-function.md)  
[<span data-ttu-id="79c8d-145">Jetgetloginfo</span><span class="sxs-lookup"><span data-stu-id="79c8d-145">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="79c8d-146">JetGetLogInfoInstance2</span><span class="sxs-lookup"><span data-stu-id="79c8d-146">JetGetLogInfoInstance2</span></span>](./jetgetloginfoinstance2-function.md)  
[<span data-ttu-id="79c8d-147">System Parameter</span><span class="sxs-lookup"><span data-stu-id="79c8d-147">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
