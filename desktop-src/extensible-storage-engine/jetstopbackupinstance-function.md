---
description: Weitere Informationen finden Sie in der jetstopbackupinstance-Funktion.
title: Jetstopbackupinstance-Funktion
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1813658ed1fb569795bdfa65ccada3ef8ee629c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128632"
---
# <a name="jetstopbackupinstance-function"></a><span data-ttu-id="a8435-103">Jetstopbackupinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="a8435-103">JetStopBackupInstance Function</span></span>


<span data-ttu-id="a8435-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a8435-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopbackupinstance-function"></a><span data-ttu-id="a8435-105">Jetstopbackupinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="a8435-105">JetStopBackupInstance Function</span></span>

<span data-ttu-id="a8435-106">Die **jetstopbackupinstance** -Funktion verhindert, dass streamingsicherungsbezogene Aktivitäten auf einer bestimmten laufenden Instanz fortgesetzt werden, sodass die Streamingsicherung auf vorhersagbare Weise beendet wird.</span><span class="sxs-lookup"><span data-stu-id="a8435-106">The **JetStopBackupInstance** function prevents streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span>

<span data-ttu-id="a8435-107">**Windows XP:**  **jetstopbackupinstance** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a8435-107">**Windows XP:**  **JetStopBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="a8435-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8435-108">Parameters</span></span>

<span data-ttu-id="a8435-109">*lichen*</span><span class="sxs-lookup"><span data-stu-id="a8435-109">*instance*</span></span>

<span data-ttu-id="a8435-110">Identifiziert die für den API-Befehl zu verwendende laufende Instanz.</span><span class="sxs-lookup"><span data-stu-id="a8435-110">Identifies the running instance to use for the API call.</span></span>

### <a name="return-value"></a><span data-ttu-id="a8435-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8435-111">Return Value</span></span>

<span data-ttu-id="a8435-112">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="a8435-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a8435-113">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a8435-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8435-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a8435-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="a8435-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8435-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8435-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a8435-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a8435-117">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a8435-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8435-118">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a8435-118">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a8435-119">Der angegebene Instanzparameter weist einen ungültigen Wert auf (keine Instanz, die derzeit ausgeführt wird).</span><span class="sxs-lookup"><span data-stu-id="a8435-119">The specified instance parameter has an invalid value (not an instance that is currently running).</span></span></p>
<p><span data-ttu-id="a8435-120"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a8435-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a8435-121">Wenn diese Funktion erfolgreich ausgeführt wird, startet die Instanz, die angegeben wurde, alle neuen Streamingsicherungs-APIs.</span><span class="sxs-lookup"><span data-stu-id="a8435-121">If this function succeeds, the instance that was specified will start failing any new streaming backup APIs.</span></span>

<span data-ttu-id="a8435-122">Wenn diese Funktion fehlschlägt, werden keine Schritte zur Vorbereitung der Sicherung auf der-Instanz ausgeführt, und es wird keine Änderung am Instanzzustand vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="a8435-122">If this function fails, no steps to prepare for the backup termination on the instance will be taken and no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a8435-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8435-123">Remarks</span></span>

<span data-ttu-id="a8435-124">Die Sicherung wird in der Regel durch ein Ereignis außerhalb des Prozess Mechanismus ausgelöst. durch die Verwendung dieser API führt die ESENT-Anwendung selbst weitere Aufrufe an die Streamingsicherungs-APIs aus.</span><span class="sxs-lookup"><span data-stu-id="a8435-124">Backup is usually triggered by an event outside the process mechanism and by using this API, the ESENT application itself will make any further calls to the streaming backup APIs to fail.</span></span> <span data-ttu-id="a8435-125">Der Großteil der APIs für die Streaming-Sicherung beginnt mit dem JET_errBackupAbortByServer.</span><span class="sxs-lookup"><span data-stu-id="a8435-125">The majority of streaming backup APIs will start failing with JET_errBackupAbortByServer.</span></span> <span data-ttu-id="a8435-126">Daher wird bei allen streamingsicherungsweiterungen (z. b. [jetreadfilanstance](./jetreadfileinstance-function.md)) ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8435-126">As such, any streaming backup progress (such as [JetReadFileInstance](./jetreadfileinstance-function.md)) will return an error.</span></span> <span data-ttu-id="a8435-127">Sicherungs Vorgänge, die Teil der Sicherungs Beendigung sind (z. b. [jetendexternalbackupinstance](./jetendexternalbackupinstance-function.md)), sind weiterhin zulässig.</span><span class="sxs-lookup"><span data-stu-id="a8435-127">Backup operations which are part of the backup termination (like [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) will still be allowed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a8435-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8435-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8435-129"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a8435-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a8435-130">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a8435-130">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8435-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a8435-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a8435-132">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a8435-132">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8435-133"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a8435-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a8435-134">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="a8435-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8435-135"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="a8435-135"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a8435-136">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a8435-136">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8435-137"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a8435-137"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a8435-138">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a8435-138">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a8435-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a8435-139">See Also</span></span>

[<span data-ttu-id="a8435-140">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a8435-140">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a8435-141">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a8435-141">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a8435-142">Jetendexternalbackupinstance</span><span class="sxs-lookup"><span data-stu-id="a8435-142">JetEndExternalBackupInstance</span></span>](./jetendexternalbackupinstance-function.md)  
[<span data-ttu-id="a8435-143">Jetreadfilinput Stance</span><span class="sxs-lookup"><span data-stu-id="a8435-143">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="a8435-144">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="a8435-144">JetStopService</span></span>](./jetstopservice-function.md)
