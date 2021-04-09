---
description: 'Weitere Informationen zu: jetidle-Funktion'
title: Jetidle-Funktion
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0adf2845997b97eb93b39b779da4ad19bb9ee066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866820"
---
# <a name="jetidle-function"></a><span data-ttu-id="181dc-103">Jetidle-Funktion</span><span class="sxs-lookup"><span data-stu-id="181dc-103">JetIdle Function</span></span>


<span data-ttu-id="181dc-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="181dc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetidle-function"></a><span data-ttu-id="181dc-105">Jetidle-Funktion</span><span class="sxs-lookup"><span data-stu-id="181dc-105">JetIdle Function</span></span>

<span data-ttu-id="181dc-106">Die **jetidle** -Funktion ist veraltet und sollte nur zu Testzwecken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="181dc-106">The **JetIdle** function is defunct, and should only be used for testing purposes.</span></span> <span data-ttu-id="181dc-107">**Jetidle** kann verwendet werden, um Cleanuptasks im Leerlauf auszuführen oder den Versionsspeicher Status in ESE zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="181dc-107">**JetIdle** can be used to perform idle cleanup tasks or check the version store status in ESE.</span></span>

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="181dc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="181dc-108">Parameters</span></span>

<span data-ttu-id="181dc-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="181dc-109">*sesid*</span></span>

<span data-ttu-id="181dc-110">Die Sitzung, die für diesen-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="181dc-110">The session that will be used for this call.</span></span>

<span data-ttu-id="181dc-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="181dc-111">*grbit*</span></span>

<span data-ttu-id="181dc-112">Eine Gruppe von Bits, die die Optionen enthalten, die für diesen-Befehl verwendet werden sollen, einschließlich 0 (null) oder mehr der folgenden Bits:</span><span class="sxs-lookup"><span data-stu-id="181dc-112">A group of bits that contain the options to be used for this call, which include zero or more of the following bits:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="181dc-113">Wert</span><span class="sxs-lookup"><span data-stu-id="181dc-113">Value</span></span></p></th>
<th><p><span data-ttu-id="181dc-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="181dc-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="181dc-115">JET_bitIdleCompact</span><span class="sxs-lookup"><span data-stu-id="181dc-115">JET_bitIdleCompact</span></span></p></td>
<td><p><span data-ttu-id="181dc-116">Löst die Bereinigung des Versionsspeicher aus.</span><span class="sxs-lookup"><span data-stu-id="181dc-116">Triggers cleanup of the version store.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="181dc-117">JET_bitIdleFlushBuffers</span><span class="sxs-lookup"><span data-stu-id="181dc-117">JET_bitIdleFlushBuffers</span></span></p></td>
<td><p><span data-ttu-id="181dc-118">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="181dc-118">Reserved for future use.</span></span> <span data-ttu-id="181dc-119">Wenn dieses Flag angegeben wird, gibt die API JET_errInvalidgrbit zurück.</span><span class="sxs-lookup"><span data-stu-id="181dc-119">If this flag is specified, the API will return JET_errInvalidgrbit.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="181dc-120">JET_bitIdleStatus</span><span class="sxs-lookup"><span data-stu-id="181dc-120">JET_bitIdleStatus</span></span></p></td>
<td><p><span data-ttu-id="181dc-121">Gibt JET_wrnIdleFull zurück, wenn der Versionsspeicher größer als der Halbwert ist.</span><span class="sxs-lookup"><span data-stu-id="181dc-121">Returns JET_wrnIdleFull if version store is more than half full.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="181dc-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="181dc-122">Return Value</span></span>

<span data-ttu-id="181dc-123">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="181dc-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="181dc-124">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="181dc-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="181dc-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="181dc-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="181dc-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="181dc-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="181dc-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="181dc-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="181dc-128">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="181dc-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="181dc-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="181dc-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="181dc-130">Ein für die API bereitgestellter <em>grbit</em> -Parameter war ungültig.</span><span class="sxs-lookup"><span data-stu-id="181dc-130">A <em>grbit</em> parameter that was provided to the API was not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="181dc-131">Wenn diese Funktion erfolgreich ausgeführt wird, wird der entsprechende Vorgang ausgelöst, oder es wird ein Fehlercode angezeigt, der angibt, wie voll der Versionsspeicher vom angegebenen *grbit* ist.</span><span class="sxs-lookup"><span data-stu-id="181dc-131">If this function succeeds, the appropriate operation will be triggered, or an error code indicating how full the version store is depending on the *grbit* provided.</span></span>

<span data-ttu-id="181dc-132">Wenn diese Funktion fehlschlägt, wurde der angeforderte Vorgang nicht erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="181dc-132">If this function fails, the requested operation will not have completed successfully.</span></span>

#### <a name="remarks"></a><span data-ttu-id="181dc-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="181dc-133">Remarks</span></span>

<span data-ttu-id="181dc-134">Der Versionsspeicher verwaltet den Snapshot-Isolations Mechanismus von ESE.</span><span class="sxs-lookup"><span data-stu-id="181dc-134">The version store maintains ESE's snapshot isolation mechanism.</span></span> <span data-ttu-id="181dc-135">Wenn der Versionsspeicher größer als der Halbwert ist, kann das Programm Transaktionen mit langer Laufzeit schließen.</span><span class="sxs-lookup"><span data-stu-id="181dc-135">If the version store is more than half full, the program might close long-running transactions.</span></span> <span data-ttu-id="181dc-136">Wenn eine Transaktion mit langer Ausführungsdauer den Versionsspeicher erschöpft, hält ESE Schreibvorgänge für die Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="181dc-136">If a long-running transaction exhausts the version store, ESE will stop allowing write operations to the database.</span></span>

#### <a name="requirements"></a><span data-ttu-id="181dc-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="181dc-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="181dc-138"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="181dc-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="181dc-139">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="181dc-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="181dc-140"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="181dc-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="181dc-141">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="181dc-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="181dc-142"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="181dc-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="181dc-143">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="181dc-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="181dc-144"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="181dc-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="181dc-145">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="181dc-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="181dc-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="181dc-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="181dc-147">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="181dc-147">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="181dc-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="181dc-148">See Also</span></span>

[<span data-ttu-id="181dc-149">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="181dc-149">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="181dc-150">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="181dc-150">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="181dc-151">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="181dc-151">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="181dc-152">Jetcommittransaction</span><span class="sxs-lookup"><span data-stu-id="181dc-152">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)
