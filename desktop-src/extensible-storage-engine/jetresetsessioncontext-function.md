---
description: 'Weitere Informationen finden Sie hier: jetresetungessioncontext-Funktion'
title: Jetresetzessioncontext-Funktion
TOCTitle: JetResetSessionContext Function
ms:assetid: 537a4753-b804-457a-9a13-53e8d1056eab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269250(v=EXCHG.10)
ms:contentKeyID: 32765552
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ee02050a9583aa67f50fbe53d710c352c196048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216294"
---
# <a name="jetresetsessioncontext-function"></a><span data-ttu-id="ec2a0-103">Jetresetzessioncontext-Funktion</span><span class="sxs-lookup"><span data-stu-id="ec2a0-103">JetResetSessionContext Function</span></span>


<span data-ttu-id="ec2a0-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ec2a0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetresetsessioncontext-function"></a><span data-ttu-id="ec2a0-105">Jetresetzessioncontext-Funktion</span><span class="sxs-lookup"><span data-stu-id="ec2a0-105">JetResetSessionContext Function</span></span>

<span data-ttu-id="ec2a0-106">Die **jetresetsessioncontext** -Funktion trennt eine Sitzung vom aktuellen Thread.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-106">The **JetResetSessionContext** function disassociates a session from the current thread.</span></span>

```cpp
    JET_ERR JET_API JetResetSessionContext(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a><span data-ttu-id="ec2a0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec2a0-107">Parameters</span></span>

<span data-ttu-id="ec2a0-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="ec2a0-108">*sesid*</span></span>

<span data-ttu-id="ec2a0-109">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-109">The session to use for this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="ec2a0-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec2a0-110">Return Value</span></span>

<span data-ttu-id="ec2a0-111">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ec2a0-112">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ec2a0-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec2a0-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ec2a0-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="ec2a0-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec2a0-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec2a0-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ec2a0-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ec2a0-116">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec2a0-117">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ec2a0-117">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ec2a0-118">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-118">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="ec2a0-119">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-119">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec2a0-120">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ec2a0-120">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ec2a0-121">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-121">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec2a0-122">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ec2a0-122">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ec2a0-123">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-123">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec2a0-124">JET_errSessionContextNotSetByThisThread</span><span class="sxs-lookup"><span data-stu-id="ec2a0-124">JET_errSessionContextNotSetByThisThread</span></span></p></td>
<td><p><span data-ttu-id="ec2a0-125">Die Zuordnung der Sitzung zum aktuellen Thread konnte nicht aufgehoben werden, da Sie mit einem anderen Thread verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-125">The session could not be disassociated from the current thread because it is associated with a different thread.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec2a0-126">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ec2a0-126">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ec2a0-127">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-127">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ec2a0-128">Bei Erfolg wird die Zuordnung der Sitzung zum aktuellen Thread aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-128">On success, the session will be disassociated from the current thread.</span></span> <span data-ttu-id="ec2a0-129">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-129">No change to the database state will occur.</span></span>

<span data-ttu-id="ec2a0-130">Bei einem Fehler bleibt der Sitzungs Status unverändert.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-130">On failure, the session state will remain unchanged.</span></span> <span data-ttu-id="ec2a0-131">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-131">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ec2a0-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec2a0-132">Remarks</span></span>

<span data-ttu-id="ec2a0-133">**Jetresetessioncontext** muss in demselben Thread aufgerufen werden, der [jetsezessioncontext](./jetsetsessioncontext-function.md) für eine bestimmte Sitzung aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-133">**JetResetSessionContext** must be called on the same thread that called [JetSetSessionContext](./jetsetsessioncontext-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ec2a0-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec2a0-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec2a0-135"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ec2a0-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ec2a0-136">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec2a0-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ec2a0-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ec2a0-138">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec2a0-139"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ec2a0-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ec2a0-140">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec2a0-141"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="ec2a0-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ec2a0-142">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec2a0-143"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ec2a0-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ec2a0-144">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ec2a0-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ec2a0-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ec2a0-145">See Also</span></span>

[<span data-ttu-id="ec2a0-146">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="ec2a0-146">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="ec2a0-147">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ec2a0-147">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ec2a0-148">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ec2a0-148">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ec2a0-149">Jetabessioncontext</span><span class="sxs-lookup"><span data-stu-id="ec2a0-149">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)
