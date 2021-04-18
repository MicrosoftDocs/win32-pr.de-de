---
description: 'Weitere Informationen finden Sie in den folgenden Informationen: jejessnapshotgetfrezeinfo-Funktion'
title: Jejessnapshotgetfrezeinfo-Funktion
TOCTitle: JetOSSnapshotGetFreezeInfo Function
ms:assetid: b94eaf91-7407-4c62-ab1e-3249ad076c1a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294070(v=EXCHG.10)
ms:contentKeyID: 32765685
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotGetFreezeInfo
- JetOSSnapshotGetFreezeInfoA
- JetOSSnapshotGetFreezeInfoW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2fbfd3fb31567ea73b8266b5aeba506d62be7714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352436"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a><span data-ttu-id="b4a9c-103">Jejessnapshotgetfrezeinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="b4a9c-103">JetOSSnapshotGetFreezeInfo Function</span></span>


<span data-ttu-id="b4a9c-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b4a9c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotgetfreezeinfo-function"></a><span data-ttu-id="b4a9c-105">Jejessnapshotgetfrezeinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="b4a9c-105">JetOSSnapshotGetFreezeInfo Function</span></span>

<span data-ttu-id="b4a9c-106">Die **jedessnapshotgetfrezeinfo** -Funktion Ruft die Liste der Instanzen und Datenbanken ab, die zu einem beliebigen Zeitpunkt Teil der Momentaufnahme Sitzung sind.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-106">The **JetOSSnapshotGetFreezeInfo** function retrieves the list of instances and databases that are part of the snapshot session at any given moment.</span></span>

<span data-ttu-id="b4a9c-107">**Windows Vista:**  **jedessnapshotgetfrezeinfo** wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-107">**Windows Vista:**  **JetOSSnapshotGetFreezeInfo** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotGetFreezeInfo(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="b4a9c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4a9c-108">Parameters</span></span>

<span data-ttu-id="b4a9c-109">*snapid*</span><span class="sxs-lookup"><span data-stu-id="b4a9c-109">*snapId*</span></span>

<span data-ttu-id="b4a9c-110">Der Bezeichner der Momentaufnahme Sitzung, die gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-110">The identifier of the snapshot session to be started.</span></span>

<span data-ttu-id="b4a9c-111">*pcinstanceingefo*</span><span class="sxs-lookup"><span data-stu-id="b4a9c-111">*pcInstanceInfo*</span></span>

<span data-ttu-id="b4a9c-112">Die Anzahl der Instanzen, die zurzeit ausgeführt werden und Teil der Momentaufnahme Sitzung sind.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-112">The number of instances currently running that are part of the snapshot session.</span></span>

<span data-ttu-id="b4a9c-113">*painstanceingefo*</span><span class="sxs-lookup"><span data-stu-id="b4a9c-113">*paInstanceInfo*</span></span>

<span data-ttu-id="b4a9c-114">Ein Array von-Strukturen, eines für jede laufende Instanz, das die Instanz und die darin vorhandenen Datenbanken beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-114">An array of structures, one for each running instance, describing the instance and the databases that are part of it.</span></span>

<span data-ttu-id="b4a9c-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b4a9c-115">*grbit*</span></span>

<span data-ttu-id="b4a9c-116">Die Optionen für diesen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-116">The options for this call.</span></span> <span data-ttu-id="b4a9c-117">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-117">This parameter is reserved for future use.</span></span> <span data-ttu-id="b4a9c-118">Der einzige gültige Wert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b4a9c-118">The only valid value is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="b4a9c-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4a9c-119">Return Value</span></span>

<span data-ttu-id="b4a9c-120">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b4a9c-121">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b4a9c-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4a9c-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b4a9c-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="b4a9c-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4a9c-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4a9c-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b4a9c-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b4a9c-125">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4a9c-126">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="b4a9c-126">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="b4a9c-127">Die Funktion konnte aufgrund einer nicht genügend Arbeitsspeicher Bedingung nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-127">The function failed due to an out-of-memory condition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4a9c-128">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b4a9c-128">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b4a9c-129"><em>pcinstanceingefo</em> oder <em>painstanceingefo</em> ist <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-129"><em>pcInstanceInfo</em> or <em>paInstanceInfo</em> is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4a9c-130">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="b4a9c-130">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="b4a9c-131">Der Bezeichner für die Momentaufnahme Sitzung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-131">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4a9c-132">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="b4a9c-132">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="b4a9c-133">Eine Momentaufnahme Sitzung wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-133">A snapshot session is not in progress.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b4a9c-134">Wenn diese Funktion erfolgreich ausgeführt wird, werden die Instanzinformationen ordnungsgemäß ausgefüllt und müssen später freigegeben werden, indem [jetfrebuffer](./jetfreebuffer-function.md) mit dem Zeiger auf das zurückgegebene instanzinformationsarray aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-134">If this function succeeds, the instance information is properly filled and it must be freed later by calling [JetFreeBuffer](./jetfreebuffer-function.md) with the pointer to the instance info array that was returned.</span></span>

<span data-ttu-id="b4a9c-135">Wenn diese Funktion fehlschlägt, erfolgt keine Änderung des Engine-Zustands.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-135">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b4a9c-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4a9c-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4a9c-137"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b4a9c-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b4a9c-138">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-138">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4a9c-139"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b4a9c-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b4a9c-140">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-140">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4a9c-141"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b4a9c-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b4a9c-142">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-142">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4a9c-143"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="b4a9c-143"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b4a9c-144">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-144">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4a9c-145"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b4a9c-145"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b4a9c-146">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b4a9c-146">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4a9c-147"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="b4a9c-147"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="b4a9c-148">Implementiert als <strong>jeumssnapshotgetfrezeinfow</strong> (Unicode) und <strong>jeto ssnapshotgetfrezeinfoa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b4a9c-148">Implemented as <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) and <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b4a9c-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b4a9c-149">See Also</span></span>

[<span data-ttu-id="b4a9c-150">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="b4a9c-150">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="b4a9c-151">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="b4a9c-151">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="b4a9c-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b4a9c-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b4a9c-153">Jetfrebuffer</span><span class="sxs-lookup"><span data-stu-id="b4a9c-153">JetFreeBuffer</span></span>](./jetfreebuffer-function.md)  
[<span data-ttu-id="b4a9c-154">Jejessnapshotabort</span><span class="sxs-lookup"><span data-stu-id="b4a9c-154">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="b4a9c-155">Jeto ssnapshotfreeze</span><span class="sxs-lookup"><span data-stu-id="b4a9c-155">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="b4a9c-156">Jejessnapshotthaw</span><span class="sxs-lookup"><span data-stu-id="b4a9c-156">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
