---
description: 'Weitere Informationen finden Sie unter: jetgetinstancinput Info-Funktion'
title: Jetgetinstancinput Info-Funktion
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8c8e9a279f536622cfdfccb8bc8882914aeee64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866824"
---
# <a name="jetgetinstanceinfo-function"></a><span data-ttu-id="f6c74-103">Jetgetinstancinput Info-Funktion</span><span class="sxs-lookup"><span data-stu-id="f6c74-103">JetGetInstanceInfo Function</span></span>


<span data-ttu-id="f6c74-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f6c74-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetinstanceinfo-function"></a><span data-ttu-id="f6c74-105">Jetgetinstancinput Info-Funktion</span><span class="sxs-lookup"><span data-stu-id="f6c74-105">JetGetInstanceInfo Function</span></span>

<span data-ttu-id="f6c74-106">Die **jetgetinstanceinfo** -Funktion Ruft Informationen zu den Instanzen ab, die ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f6c74-106">The **JetGetInstanceInfo** function retrieves information about the instances that are running.</span></span>

<span data-ttu-id="f6c74-107">**Windows XP: jetgetinstanceinfo** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f6c74-107">**Windows XP:  JetGetInstanceInfo** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a><span data-ttu-id="f6c74-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6c74-108">Parameters</span></span>

<span data-ttu-id="f6c74-109">*pcinstanceingefo*</span><span class="sxs-lookup"><span data-stu-id="f6c74-109">*pcInstanceInfo*</span></span>

<span data-ttu-id="f6c74-110">Ein Zeiger auf einen Puffer, der die Anzahl der in " *painstanceinfo*" gespeicherten Elemente empfängt.</span><span class="sxs-lookup"><span data-stu-id="f6c74-110">A pointer to a buffer which will receive the number of elements stored in *paInstanceInfo*.</span></span>

<span data-ttu-id="f6c74-111">*painstanceingefo*</span><span class="sxs-lookup"><span data-stu-id="f6c74-111">*paInstanceInfo*</span></span>

<span data-ttu-id="f6c74-112">Ein Zeiger auf einen Puffer, der die Adresse des ersten Elements eines Arrays von-Strukturen empfängt.</span><span class="sxs-lookup"><span data-stu-id="f6c74-112">A pointer to a buffer which will receive the address of the first element of an array of structures.</span></span>

### <a name="return-value"></a><span data-ttu-id="f6c74-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6c74-113">Return Value</span></span>

<span data-ttu-id="f6c74-114">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="f6c74-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f6c74-115">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f6c74-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f6c74-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f6c74-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="f6c74-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6c74-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6c74-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f6c74-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f6c74-119">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f6c74-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6c74-120">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f6c74-120">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f6c74-121">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="f6c74-121">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="f6c74-122">Dieser Fehler wird von <strong>jetgetinstanceingefo</strong> zurückgegeben, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="f6c74-122">This error will be returned by <strong>JetGetInstanceInfo</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="f6c74-123"><em>pcinstanceingefo</em> oder <em>painstanceingefo</em> ist NULL.</span><span class="sxs-lookup"><span data-stu-id="f6c74-123"><em>pcInstanceInfo</em> or <em>paInstanceInfo</em> are NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6c74-124">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="f6c74-124">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="f6c74-125">Es ist nicht genügend Arbeitsspeicher vorhanden, um die Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f6c74-125">There is insufficient memory to process the request.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="f6c74-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6c74-126">Remarks</span></span>

<span data-ttu-id="f6c74-127">Die Datenbank-Engine weist ein Array von [JET_INSTANCE_INFO](./jet-instance-info-structure.md) Strukturen zu.</span><span class="sxs-lookup"><span data-stu-id="f6c74-127">The database engine will allocate an array of [JET_INSTANCE_INFO](./jet-instance-info-structure.md) structures.</span></span> <span data-ttu-id="f6c74-128">Der Aufrufer ist dafür verantwortlich, diesen Arbeitsspeicher mit [jetfrebuffer](./jetfreebuffer-function.md)freizugeben.</span><span class="sxs-lookup"><span data-stu-id="f6c74-128">The caller is responsible for freeing this memory with [JetFreeBuffer](./jetfreebuffer-function.md).</span></span>

<span data-ttu-id="f6c74-129">Wenn keine aktiven Instanzen vorhanden sind, gibt **jetgetinstanceinfo** JET_errSuccess zurück, und *pcinstanceinfo* erhält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="f6c74-129">If there are no active instances, **JetGetInstanceInfo** will return JET_errSuccess, and *pcInstanceInfo* will receive a value of 0.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f6c74-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6c74-130">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6c74-131"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f6c74-131"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f6c74-132">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f6c74-132">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6c74-133"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f6c74-133"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f6c74-134">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f6c74-134">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6c74-135"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f6c74-135"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f6c74-136">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="f6c74-136">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6c74-137"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="f6c74-137"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f6c74-138">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f6c74-138">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6c74-139"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f6c74-139"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f6c74-140">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f6c74-140">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6c74-141"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f6c74-141"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f6c74-142">Implementiert als <strong>jetgetinstancin Fow</strong> (Unicode) und <strong>jetgetinstanceingefoa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f6c74-142">Implemented as <strong>JetGetInstanceInfoW</strong> (Unicode) and <strong>JetGetInstanceInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f6c74-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f6c74-143">See Also</span></span>

[<span data-ttu-id="f6c74-144">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f6c74-144">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f6c74-145">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f6c74-145">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="f6c74-146">JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="f6c74-146">JET_INSTANCE_INFO</span></span>](./jet-instance-info-structure.md)  
[<span data-ttu-id="f6c74-147">Jetfrebuffer</span><span class="sxs-lookup"><span data-stu-id="f6c74-147">JetFreeBuffer</span></span>](./jetfreebuffer-function.md)
