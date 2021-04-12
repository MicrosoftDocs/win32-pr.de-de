---
description: 'Weitere Informationen zu: jetgetversion-Funktion'
title: Jetgetversion-Funktion
TOCTitle: JetGetVersion Function
ms:assetid: f25c3639-ae2b-4357-9947-563ef3df72c6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294133(v=EXCHG.10)
ms:contentKeyID: 32765747
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetVersion
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38128358d814ea85cf087c270a65a3fada976e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218133"
---
# <a name="jetgetversion-function"></a><span data-ttu-id="f22b8-103">Jetgetversion-Funktion</span><span class="sxs-lookup"><span data-stu-id="f22b8-103">JetGetVersion Function</span></span>


<span data-ttu-id="f22b8-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f22b8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetversion-function"></a><span data-ttu-id="f22b8-105">Jetgetversion-Funktion</span><span class="sxs-lookup"><span data-stu-id="f22b8-105">JetGetVersion Function</span></span>

<span data-ttu-id="f22b8-106">Die **jetgetversion** -Funktion Ruft die Version der Datenbank-Engine ab.</span><span class="sxs-lookup"><span data-stu-id="f22b8-106">The **JetGetVersion** function retrieves the version of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetGetVersion(
      __in          JET_SESID sesid,
      __out         unsigned long* pwVersion
    );
```

### <a name="parameters"></a><span data-ttu-id="f22b8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f22b8-107">Parameters</span></span>

<span data-ttu-id="f22b8-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="f22b8-108">*sesid*</span></span>

<span data-ttu-id="f22b8-109">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f22b8-109">The session to use for this call.</span></span>

<span data-ttu-id="f22b8-110">*pwversion*</span><span class="sxs-lookup"><span data-stu-id="f22b8-110">*pwVersion*</span></span>

<span data-ttu-id="f22b8-111">Ein Zeiger auf die Versionsnummer der Datenbank-Engine.</span><span class="sxs-lookup"><span data-stu-id="f22b8-111">A pointer to the version number of the database engine.</span></span>

### <a name="return-value"></a><span data-ttu-id="f22b8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f22b8-112">Return Value</span></span>

<span data-ttu-id="f22b8-113">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="f22b8-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f22b8-114">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f22b8-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f22b8-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f22b8-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="f22b8-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f22b8-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f22b8-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f22b8-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f22b8-118">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f22b8-118">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f22b8-119">Wenn diese Funktion erfolgreich ausgeführt wird, wird die Version der Datenbank-Engine abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f22b8-119">If this function succeeds, the version of the database engine is retrieved.</span></span>

<span data-ttu-id="f22b8-120">Es sind keine bekannten Fehlermodi vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f22b8-120">There are no known failure modes.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f22b8-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f22b8-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f22b8-122"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f22b8-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f22b8-123">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f22b8-123">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22b8-124"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f22b8-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f22b8-125">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f22b8-125">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22b8-126"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f22b8-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f22b8-127">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="f22b8-127">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f22b8-128"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="f22b8-128"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f22b8-129">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f22b8-129">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f22b8-130"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f22b8-130"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f22b8-131">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f22b8-131">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f22b8-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f22b8-132">See Also</span></span>

[<span data-ttu-id="f22b8-133">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="f22b8-133">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="f22b8-134">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="f22b8-134">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="f22b8-135">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f22b8-135">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f22b8-136">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f22b8-136">JET_SESID</span></span>](./jet-sesid.md)
