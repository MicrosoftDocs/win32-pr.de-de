---
description: 'Weitere Informationen zu: jetgetinstancefehlinfo-Funktion'
title: Jetgetinstancefehlinfo-Funktion
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed63c6a5c6d3b2488f7226da0a1f23e1adb39e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042652"
---
# <a name="jetgetinstancemiscinfo-function"></a><span data-ttu-id="d3f0d-103">Jetgetinstancefehlinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="d3f0d-103">JetGetInstanceMiscInfo Function</span></span>


<span data-ttu-id="d3f0d-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d3f0d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetinstancemiscinfo-function"></a><span data-ttu-id="d3f0d-105">Jetgetinstancefehlinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="d3f0d-105">JetGetInstanceMiscInfo Function</span></span>

<span data-ttu-id="d3f0d-106">Die **jetgetinstancefehlinfo** -Funktion Ruft Informationen über die Instanz ab, während die Instanz online ist.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-106">The **JetGetInstanceMiscInfo** function retrieves information about the instance, while the instance is online.</span></span>

<span data-ttu-id="d3f0d-107">**Windows Vista: jetgetinstancefehlinfo** wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-107">**Windows Vista:  JetGetInstanceMiscInfo** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="d3f0d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3f0d-108">Parameters</span></span>

<span data-ttu-id="d3f0d-109">*lichen*</span><span class="sxs-lookup"><span data-stu-id="d3f0d-109">*instance*</span></span>

<span data-ttu-id="d3f0d-110">Identifiziert die Daten Bank Instanz, die für den API-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-110">Identifies the database instance that will be used for the API call.</span></span>

<span data-ttu-id="d3f0d-111">*pvresult*</span><span class="sxs-lookup"><span data-stu-id="d3f0d-111">*pvResult*</span></span>

<span data-ttu-id="d3f0d-112">Zeiger auf einen Puffer, der die Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-112">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="d3f0d-113">Der Typ des Puffers ist von *infolevel* abhängig.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-113">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="d3f0d-114">Der Aufrufer ist dafür verantwortlich, den Puffer entsprechend anzupassen.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-114">The caller is responsible for aligning the buffer appropriately.</span></span>

<span data-ttu-id="d3f0d-115">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="d3f0d-115">*cbMax*</span></span>

<span data-ttu-id="d3f0d-116">Die Größe (in Bytes) des Puffers, der in *pvresult* übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-116">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="d3f0d-117">*Infolevel*</span><span class="sxs-lookup"><span data-stu-id="d3f0d-117">*InfoLevel*</span></span>

<span data-ttu-id="d3f0d-118">Bestimmt, welche Art von Informationen für die Instanz abgerufen werden, die von der- *Instanz* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-118">Determines what type of information will be retrieved for the instance specified by *instance*.</span></span> <span data-ttu-id="d3f0d-119">Das Format der in *pvresult* gespeicherten Daten hängt von *infolevel* ab.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-119">The format of the data stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="d3f0d-120">Die folgenden Optionen sind für die Verwendung mit diesem Parameter verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-120">The following options are available for use with this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d3f0d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d3f0d-121">Value</span></span></p></th>
<th><p><span data-ttu-id="d3f0d-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d3f0d-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3f0d-123">JET_InstanceMiscInfoLogSignature</span><span class="sxs-lookup"><span data-stu-id="d3f0d-123">JET_InstanceMiscInfoLogSignature</span></span></p></td>
<td><p><span data-ttu-id="d3f0d-124"><em>pvresult</em> wird als <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> Struktur der Transaktionsprotokoll Sequenz interpretiert, die dieser Instanz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-124"><em>pvResult</em> is interpreted as a <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> structure of the transaction log sequence associated with this instance.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d3f0d-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3f0d-125">Return Value</span></span>

<span data-ttu-id="d3f0d-126">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d3f0d-127">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d3f0d-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d3f0d-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d3f0d-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="d3f0d-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3f0d-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3f0d-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d3f0d-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d3f0d-131">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3f0d-132">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="d3f0d-132">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="d3f0d-133">Der Puffer war zu klein.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-133">The buffer was too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3f0d-134">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d3f0d-134">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d3f0d-135">Es wurde entweder ein ungültiger <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> oder eine ungültige <em>infolevel</em> angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-135">Either an invalid <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> or an invalid <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="d3f0d-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3f0d-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3f0d-137"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d3f0d-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d3f0d-138">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-138">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3f0d-139"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d3f0d-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d3f0d-140">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-140">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3f0d-141"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d3f0d-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d3f0d-142">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-142">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3f0d-143"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="d3f0d-143"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d3f0d-144">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-144">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3f0d-145"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d3f0d-145"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d3f0d-146">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d3f0d-146">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d3f0d-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d3f0d-147">See Also</span></span>

[<span data-ttu-id="d3f0d-148">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d3f0d-148">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d3f0d-149">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="d3f0d-149">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="d3f0d-150">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="d3f0d-150">JET_SIGNATURE</span></span>](./jet-signature-structure.md)
