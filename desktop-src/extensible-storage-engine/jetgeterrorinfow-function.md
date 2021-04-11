---
description: 'Weitere Informationen zu: jetgeterrorinfow-Funktion'
title: Jetgeterrorinfow-Funktion
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bf4db5d8d34a741e57f72e8f237f1497de0bacf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104132436"
---
# <a name="jetgeterrorinfow-function"></a><span data-ttu-id="683c8-103">Jetgeterrorinfow-Funktion</span><span class="sxs-lookup"><span data-stu-id="683c8-103">JetGetErrorInfoW Function</span></span>


<span data-ttu-id="683c8-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="683c8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgeterrorinfow-function"></a><span data-ttu-id="683c8-105">Jetgeterrorinfow-Funktion</span><span class="sxs-lookup"><span data-stu-id="683c8-105">JetGetErrorInfoW Function</span></span>

<span data-ttu-id="683c8-106">Die **jetgeterrorinfow** -Funktion BAS_ der Datenbank-Engine.</span><span class="sxs-lookup"><span data-stu-id="683c8-106">The **JetGetErrorInfoW** function BAS_ of the database engine.</span></span>

<span data-ttu-id="683c8-107">Hinweis: Diese Dokumentation basiert auf einer vorläufigen Version der Extensible Storage-Engine.</span><span class="sxs-lookup"><span data-stu-id="683c8-107">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="683c8-108">Diese Informationen können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="683c8-108">This information is subject to change.</span></span>

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a><span data-ttu-id="683c8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="683c8-109">Parameters</span></span>

<span data-ttu-id="683c8-110">*pvcontext*</span><span class="sxs-lookup"><span data-stu-id="683c8-110">*pvContext*</span></span>

<span data-ttu-id="683c8-111">Der Kontext-oder Fehlerwert, für den die erweiterten Fehlerinformationen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="683c8-111">The context or error value for which the extended error information is needed.</span></span> <span data-ttu-id="683c8-112">Der übergebene Wert hängt vom *infolevel* -Parameterwert ab.</span><span class="sxs-lookup"><span data-stu-id="683c8-112">The value passed in depends on the *InfoLevel* parameter value.</span></span>

<span data-ttu-id="683c8-113">*pvresult*</span><span class="sxs-lookup"><span data-stu-id="683c8-113">*pvResult*</span></span>

<span data-ttu-id="683c8-114">Ein Zeiger auf einen Puffer, der die Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="683c8-114">A pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="683c8-115">Der Typ des Puffers hängt vom Wert des *infolevel* -Parameters ab.</span><span class="sxs-lookup"><span data-stu-id="683c8-115">The type of the buffer depends on the *InfoLevel* parameter value.</span></span> <span data-ttu-id="683c8-116">Der Aufrufer muss so konfiguriert werden, dass der Puffer entsprechend ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="683c8-116">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="683c8-117">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="683c8-117">*cbMax*</span></span>

<span data-ttu-id="683c8-118">Die maximale Größe der *pvresult* -Struktur, die übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="683c8-118">The maximum size of the *pvResult* structure that is passed in.</span></span>

<span data-ttu-id="683c8-119">*Infolevel*</span><span class="sxs-lookup"><span data-stu-id="683c8-119">*InfoLevel*</span></span>

<span data-ttu-id="683c8-120">Der Typ der Informationen, die für die Fehler Info/den Kontext abgerufen werden, wird durch den *pvcontext* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="683c8-120">The type of information that will be retrieved for the error info/context is specified by the *pvContext* parameter.</span></span> <span data-ttu-id="683c8-121">Das Format der Daten, die in *pvresult* gespeichert sind, ist von *infolevel* abhängig.</span><span class="sxs-lookup"><span data-stu-id="683c8-121">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="683c8-122">In der folgenden Tabelle sind die möglichen Werte für diesen Parameter aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="683c8-122">The following table lists the possible values for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="683c8-123">Wert</span><span class="sxs-lookup"><span data-stu-id="683c8-123">Value</span></span></p></th>
<th><p><span data-ttu-id="683c8-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="683c8-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="683c8-125">JET_ErrorInfoSpecificErr</span><span class="sxs-lookup"><span data-stu-id="683c8-125">JET_ErrorInfoSpecificErr</span></span></p></td>
<td><p><span data-ttu-id="683c8-126"><em>pvcontext</em> wird als <a href="gg269297(v=exchg.10).md">JET_ERR</a>/Error-Code interpretiert, <em>pvresult</em> wird als <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>interpretiert, und die Felder der <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> Struktur werden entsprechend ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="683c8-126"><em>pvContext</em> is interpreted as a <a href="gg269297(v=exchg.10).md">JET_ERR</a>/error code, <em>pvResult</em> is interpreted as a <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>, and the fields of the <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> structure are filled in appropriately.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="683c8-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="683c8-127">*grbit*</span></span>

<span data-ttu-id="683c8-128">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="683c8-128">Reserved.</span></span>

### <a name="return-value"></a><span data-ttu-id="683c8-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="683c8-129">Return Value</span></span>

<span data-ttu-id="683c8-130">Diese Funktion gibt den [JET_ERR](./extensible-storage-engine-error-codes.md) -Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="683c8-130">This function returns the [JET_ERR](./extensible-storage-engine-error-codes.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="683c8-131">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="683c8-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="683c8-132">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="683c8-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="683c8-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="683c8-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="683c8-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="683c8-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="683c8-135">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="683c8-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="683c8-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="683c8-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="683c8-137">Einer der angegebenen Parameter enthält einen unerwarteten Wert oder enthält einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="683c8-137">One of the parameters provided contains an unexpected value or contains a value that does not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="683c8-138">Dies kann bei <strong>jetgeterrorinfo</strong> vorkommen, wenn Folgendes zutrifft:</span><span class="sxs-lookup"><span data-stu-id="683c8-138">This can happen for <strong>JetGetErrorInfo</strong> when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="683c8-139">Der angegebene <em>infolevel</em> -Parameterwert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="683c8-139">The specified <em>InfoLevel</em> parameter value is invalid.</span></span></p></li>
<li><p><span data-ttu-id="683c8-140">Der angegebene <em>grbit</em> -Wert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="683c8-140">The specified <em>grbit</em> value is invalid.</span></span></p></li>
<li><p><span data-ttu-id="683c8-141">Der <em>cbmax</em> -Wert des angegebenen <em>pvresult</em> -Parameter Puffers ist kleiner als die erforderliche Größe für die Ausgabe dieses <em>infolevel</em> -Parameters.</span><span class="sxs-lookup"><span data-stu-id="683c8-141">The specified <em>pvResult</em> parameter buffer’s <em>cbMax</em> value is less than the required size for output of this <em>InfoLevel</em> parameter.</span></span></p></li>
<li><p><span data-ttu-id="683c8-142">Bei <em>infolevel</em> = JET_ErrorInfoSpecificErr ist der <a href="gg294092(v=exchg.10).md">JET_ERR</a> Wert, der in der-Engine nicht angezeigt wird, unbekannt.</span><span class="sxs-lookup"><span data-stu-id="683c8-142">For <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, the <a href="gg294092(v=exchg.10).md">JET_ERR</a> value passed in is unknown to the engine.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="683c8-143">JET_errDisabledFunctionality</span><span class="sxs-lookup"><span data-stu-id="683c8-143">JET_errDisabledFunctionality</span></span></p></td>
<td><p><span data-ttu-id="683c8-144">Wenn diese Funktion von dieser SKU von Windows nicht unterstützt wird, wird dieser Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="683c8-144">If this SKU of windows doesn’t support this function, this error will be returned.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="683c8-145">Bei Erfolg wird der Ausgabepuffer, der für den angeforderten Fehler Kontext/-Wert geeignet ist, auf die angeforderten erweiterten Fehlerinformationen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="683c8-145">On success, the output buffer that is appropriate for the requested error context/value will be set to the extended error info requested.</span></span>

<span data-ttu-id="683c8-146">Bei einem Fehler wird der Status der Ausgabepuffer nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="683c8-146">On failure, the state of the output buffers will be undefined.</span></span>

### <a name="remarks"></a><span data-ttu-id="683c8-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="683c8-147">Remarks</span></span>

<span data-ttu-id="683c8-148">Die [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) -Funktion und [JET_ERRCAT](./jet-errcat.md) Gruppe von Konstanten enthalten Dokumentation zu den erweiterten Fehlerinformationen, die für *infolevel* = JET_ErrorInfoSpecificErr zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="683c8-148">The [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) function and [JET_ERRCAT](./jet-errcat.md) group of constants contain documentation about the extended error information that is returned for *InfoLevel* = JET_ErrorInfoSpecificErr.</span></span>

### <a name="requirements"></a><span data-ttu-id="683c8-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="683c8-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="683c8-150"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="683c8-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="683c8-151">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="683c8-151">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="683c8-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="683c8-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="683c8-153">Erfordert Windows 8-Server.</span><span class="sxs-lookup"><span data-stu-id="683c8-153">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="683c8-154"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="683c8-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="683c8-155">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="683c8-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="683c8-156"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="683c8-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="683c8-157">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="683c8-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="683c8-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="683c8-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="683c8-159">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="683c8-159">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="683c8-160"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="683c8-160"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="683c8-161">Hinweis: nur <strong>jetgeterrorinfow</strong> (Unicode) ist implementiert.</span><span class="sxs-lookup"><span data-stu-id="683c8-161">Note: Only the <strong>JetGetErrorInfoW</strong> (Unicode) is implemented.</span></span> <span data-ttu-id="683c8-162">Diese API weist keine (ANSI)-Version auf.</span><span class="sxs-lookup"><span data-stu-id="683c8-162">This API does not have an A (ANSI) version.</span></span></p></td>
</tr>
</tbody>
</table>
