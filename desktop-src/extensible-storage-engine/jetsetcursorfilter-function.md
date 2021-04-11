---
description: Weitere Informationen finden Sie in der jetsetcurrsorfilter-Funktion.
title: Jetsetcurrsorfilter-Funktion
TOCTitle: JetSetCursorFilter Function
ms:assetid: 3cea5beb-2cf8-4053-8e7f-7b8645580ef0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835040(v=EXCHG.10)
ms:contentKeyID: 49894662
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetCursorFilter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad589fecb190ad0f0676325b78adc7c96028a3fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128633"
---
# <a name="jetsetcursorfilter-function"></a><span data-ttu-id="b5643-103">Jetsetcurrsorfilter-Funktion</span><span class="sxs-lookup"><span data-stu-id="b5643-103">JetSetCursorFilter Function</span></span>


<span data-ttu-id="b5643-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b5643-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="b5643-105">Die **jetsetcurrsorfilter** -Funktion legt ein Array einfacher Filter für die [jetmove](./jetmove-function.md) -Funktion fest.</span><span class="sxs-lookup"><span data-stu-id="b5643-105">The **JetSetCursorFilter** function sets an array of simple filters for the [JetMove](./jetmove-function.md) function.</span></span>

<span data-ttu-id="b5643-106">Die **jetsetcurrsorfilter** -Funktion wurde im Windows 8-Betriebssystem eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b5643-106">The **JetSetCursorFilter** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetSetCursorFilter(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in_ecount(cFilters)  JET_INDEX_COLUMN* rgFilters,
  __in          DWORD cFilters,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="b5643-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5643-107">Parameters</span></span>

<span data-ttu-id="b5643-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="b5643-108">*sesid*</span></span>

<span data-ttu-id="b5643-109">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="b5643-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="b5643-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="b5643-110">*tableid*</span></span>

<span data-ttu-id="b5643-111">Der Cursor, der positioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b5643-111">The cursor to position.</span></span>

<span data-ttu-id="b5643-112">*rgfilters*</span><span class="sxs-lookup"><span data-stu-id="b5643-112">*rgFilters*</span></span>

<span data-ttu-id="b5643-113">Die einfachen Daten Satz Filter.</span><span class="sxs-lookup"><span data-stu-id="b5643-113">The simple record filters.</span></span>

<span data-ttu-id="b5643-114">*cfilters*</span><span class="sxs-lookup"><span data-stu-id="b5643-114">*cFilters*</span></span>

<span data-ttu-id="b5643-115">Die Anzahl der Filter.</span><span class="sxs-lookup"><span data-stu-id="b5643-115">The number of filters.</span></span>

<span data-ttu-id="b5643-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b5643-116">*grbit*</span></span>

<span data-ttu-id="b5643-117">Eine Gruppe von Bits, die NULL oder mehr der in der folgenden Tabelle aufgeführten Verschiebungs Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="b5643-117">A group of bits that specifies zero or more of the move options listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5643-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b5643-118">Value</span></span></p></th>
<th><p><span data-ttu-id="b5643-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b5643-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5643-120">Keine</span><span class="sxs-lookup"><span data-stu-id="b5643-120">None</span></span></p></td>
<td><p><span data-ttu-id="b5643-121">Standardoption</span><span class="sxs-lookup"><span data-stu-id="b5643-121">Default option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="b5643-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5643-122">Return value</span></span>

<span data-ttu-id="b5643-123">Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="b5643-123">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="b5643-124">Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Fehler Behandlungsparameter](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b5643-124">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5643-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b5643-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="b5643-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5643-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5643-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b5643-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b5643-128">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b5643-128">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="b5643-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5643-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5643-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b5643-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b5643-131">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b5643-131">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5643-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b5643-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b5643-133">Erfordert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b5643-133">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5643-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b5643-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b5643-135">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="b5643-135">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5643-136"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="b5643-136"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b5643-137">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b5643-137">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5643-138"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b5643-138"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b5643-139">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b5643-139">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b5643-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5643-140">See also</span></span>

[<span data-ttu-id="b5643-141">Jetmove</span><span class="sxs-lookup"><span data-stu-id="b5643-141">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="b5643-142">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b5643-142">JET_ERR</span></span>](./jet-err.md)
