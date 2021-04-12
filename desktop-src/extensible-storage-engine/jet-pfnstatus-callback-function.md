---
description: 'Weitere Informationen über: JET_PFNSTATUS Callback-Funktion'
title: JET_PFNSTATUS Callback-Funktion
TOCTitle: JET_PFNSTATUS Callback Function
ms:assetid: 8b0cf5bf-a4ee-4d8f-8dd7-556c35cd269d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269326(v=EXCHG.10)
ms:contentKeyID: 32765616
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c5f3eb374580dc6bed752900434706b66c6623b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217057"
---
# <a name="jet_pfnstatus-callback-function"></a><span data-ttu-id="cd80d-103">JET_PFNSTATUS Callback-Funktion</span><span class="sxs-lookup"><span data-stu-id="cd80d-103">JET_PFNSTATUS Callback Function</span></span>


<span data-ttu-id="cd80d-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cd80d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pfnstatus-callback-function"></a><span data-ttu-id="cd80d-105">JET_PFNSTATUS Callback-Funktion</span><span class="sxs-lookup"><span data-stu-id="cd80d-105">JET_PFNSTATUS Callback Function</span></span>

<span data-ttu-id="cd80d-106">Die **JET_PFNSTATUS** Callback-Funktion empfängt Informationen zum Fortschritt von Vorgängen mit langer Ausführungszeit, z. b. Defragmentierungs-, Sicherungs-oder Wiederherstellungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="cd80d-106">The **JET_PFNSTATUS** callback function receives information about the progress of long-running operations, such as defragmentation, backup, or restore operations.</span></span> <span data-ttu-id="cd80d-107">Bei solchen Vorgängen Ruft die Datenbank-Engine diese Rückruffunktion auf, um ein Update für den Fortschritt des Vorgangs zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cd80d-107">During such operations, the database engine calls this callback function to give an update on the progress of the operation.</span></span>

```cpp
    JET_ERR JET_API JET_PFNSTATUS(
                           JET_SESID  sesid,
                           JET_SNP snp,
                           JET_SNT snt,
                           void* pv
    );
```

### <a name="parameters"></a><span data-ttu-id="cd80d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd80d-108">Parameters</span></span>

<span data-ttu-id="cd80d-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="cd80d-109">*sesid*</span></span>

<span data-ttu-id="cd80d-110">Die Sitzung vom Typ [JET_SESID](./jet-sesid.md) , mit der die Funktion mit langer Ausführungszeit aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="cd80d-110">The session of type [JET_SESID](./jet-sesid.md) with which the long-running function was called.</span></span>

<span data-ttu-id="cd80d-111">*SNP*</span><span class="sxs-lookup"><span data-stu-id="cd80d-111">*snp*</span></span>

<span data-ttu-id="cd80d-112">Der Typ des Vorgangs, wie in [JET_SNP](./jet-snp.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="cd80d-112">The type of operation as specified in [JET_SNP](./jet-snp.md).</span></span> <span data-ttu-id="cd80d-113">Zu den Vorgangs Typen zählen Reparatur, Compact, Restore, Backup, Update, scrube und Update des Daten Satz Formats.</span><span class="sxs-lookup"><span data-stu-id="cd80d-113">Types of operations include repair, compact, restore, backup, update, scrub, and update the record format.</span></span>

<span data-ttu-id="cd80d-114">*SNT*</span><span class="sxs-lookup"><span data-stu-id="cd80d-114">*snt*</span></span>

<span data-ttu-id="cd80d-115">Der Status eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="cd80d-115">The status of an operation.</span></span> <span data-ttu-id="cd80d-116">Zu den Status Typen zählen Anfang, in Bearbeitung, Abschluss oder Fehler.</span><span class="sxs-lookup"><span data-stu-id="cd80d-116">Status types include beginning, in progress, completion, or failure.</span></span> <span data-ttu-id="cd80d-117">Der Status wird mit dem dritten Parameter des Typs [JET_SNT](./jet-snt.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="cd80d-117">The status will be specified with the third parameter of type [JET_SNT](./jet-snt.md).</span></span>

<span data-ttu-id="cd80d-118">*teuren*</span><span class="sxs-lookup"><span data-stu-id="cd80d-118">*pv*</span></span>

<span data-ttu-id="cd80d-119">Ein optionaler Zeiger auf eine Struktur vom Typ [JET_SNPROG](./jet-snprog-structure.md).</span><span class="sxs-lookup"><span data-stu-id="cd80d-119">An optional pointer to a structure of type [JET_SNPROG](./jet-snprog-structure.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="cd80d-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd80d-120">Return Value</span></span>

<span data-ttu-id="cd80d-121">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der [Fehlercodes für die erweiterbare Speicher-Engine](./extensible-storage-engine-error-codes.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="cd80d-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the [Extensible Storage Engine error codes](./extensible-storage-engine-error-codes.md).</span></span> <span data-ttu-id="cd80d-122">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cd80d-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<span data-ttu-id="cd80d-123">Bei Erfolg kann der Vorgang, der den Rückruf ausgegeben hat, normal fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="cd80d-123">On success, the operation that issued the callback can proceed normally.</span></span> <span data-ttu-id="cd80d-124">In einigen Fällen gibt der Rückruf möglicherweise eine Warnung zurück, die diesen Vorgang beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="cd80d-124">In some cases, the callback might return a warning that influences that operation.</span></span>

<span data-ttu-id="cd80d-125">Bei einem Fehler wird der Vorgang, der den Rückruf ausgegeben hat, normalerweise ordnungsgemäß fortgesetzt oder schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="cd80d-125">On failure, the operation that issued the callback might proceed normally or might fail.</span></span>

### <a name="remarks"></a><span data-ttu-id="cd80d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd80d-126">Remarks</span></span>

<span data-ttu-id="cd80d-127">Diese Rückruffunktion wird in einer Status Benachrichtigung verwendet, in der die Struktur den aktuellen Status des Fortschritts angibt.</span><span class="sxs-lookup"><span data-stu-id="cd80d-127">This callback function will be used in a progress notification in which the structure will indicate the current state of the progress.</span></span> <span data-ttu-id="cd80d-128">Beachten Sie, dass die Rückruffunktion möglicherweise mehrmals für den Fortschritt des Vorgangs aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cd80d-128">Note that the callback function might be called multiple times for the progress of the operation.</span></span>

### <a name="requirements"></a><span data-ttu-id="cd80d-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd80d-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd80d-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cd80d-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cd80d-131">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="cd80d-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd80d-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cd80d-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cd80d-133">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cd80d-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd80d-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="cd80d-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cd80d-135">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="cd80d-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="cd80d-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cd80d-136">See Also</span></span>

[<span data-ttu-id="cd80d-137">Fehlercodes für erweiterbare Speicher-Engine</span><span class="sxs-lookup"><span data-stu-id="cd80d-137">Extensible Storage Engine error codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="cd80d-138">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="cd80d-138">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="cd80d-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="cd80d-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="cd80d-140">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="cd80d-140">JET_SNP</span></span>](./jet-snp.md)  
[<span data-ttu-id="cd80d-141">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="cd80d-141">JET_SNPROG</span></span>](./jet-snprog-structure.md)  
[<span data-ttu-id="cd80d-142">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="cd80d-142">JET_SNT</span></span>](./jet-snt.md)
