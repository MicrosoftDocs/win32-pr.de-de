---
description: 'Weitere Informationen über: JET_CALLBACK Callback-Funktion'
title: JET_CALLBACK Callback-Funktion
TOCTitle: JET_CALLBACK Callback Function
ms:assetid: d15d4f84-8378-4b4b-9b8b-e89a56be5ead
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294098(v=EXCHG.10)
ms:contentKeyID: 32765713
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
ms.openlocfilehash: 5e6d26bd5e347757fce270d5f2c78ab471755c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348833"
---
# <a name="jet_callback-callback-function"></a><span data-ttu-id="c95f2-103">JET_CALLBACK Callback-Funktion</span><span class="sxs-lookup"><span data-stu-id="c95f2-103">JET_CALLBACK Callback Function</span></span>


<span data-ttu-id="c95f2-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c95f2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_callback-callback-function"></a><span data-ttu-id="c95f2-105">JET_CALLBACK Callback-Funktion</span><span class="sxs-lookup"><span data-stu-id="c95f2-105">JET_CALLBACK Callback Function</span></span>

<span data-ttu-id="c95f2-106">Die **JET_CALLBACK** -Funktion ist eine multizweck-Rückruffunktion, die von der Datenbank-Engine verwendet wird, um die Anwendung über ein Ereignis zu informieren, das Online Defragmentierung und Cursor Zustands Benachrichtigungen umfasst.</span><span class="sxs-lookup"><span data-stu-id="c95f2-106">The **JET_CALLBACK** function is a multi-purpose callback function used by the database engine to inform the application of an event involving online defragmentation and cursor state notifications.</span></span>

<span data-ttu-id="c95f2-107">Informationen zu bestimmten Einstellungen, die für die Parameter dieser Funktion verwendet werden können, finden Sie unter [JET_CBTYP](./jet-cbtyp.md) , da sich diese Einstellungen abhängig von der **JET_CBTYP** Option unterscheiden, die für die Verwendung im *cbyp* -Parameter ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="c95f2-107">See [JET_CBTYP](./jet-cbtyp.md) for specific settings to use for the parameters of this function, as these settings will differ depending upon the **JET_CBTYP** option that is selected for use in the *cbtyp* parameter.</span></span>

```cpp
    JET_ERR JET_API* JET_CALLBACK(
      [in]                 JET_SESID sesid,
      [in]                 JET_DBID dbid,
      [in]                 JET_TABLEID tableid,
      [in]                 JET_CBTYP cbtyp,
      [in, out]            void* pvArg1,
      [in, out]            void* pvArg2,
      [in]                 void* pvContext,
      [in]                 JET_API_PTR ulUnused
    );
```

### <a name="parameters"></a><span data-ttu-id="c95f2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c95f2-108">Parameters</span></span>

<span data-ttu-id="c95f2-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="c95f2-109">*sesid*</span></span>

<span data-ttu-id="c95f2-110">Die Sitzung, für die der Rückruf erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c95f2-110">The session for which the callback is being made.</span></span>

<span data-ttu-id="c95f2-111">*DBID*</span><span class="sxs-lookup"><span data-stu-id="c95f2-111">*dbid*</span></span>

<span data-ttu-id="c95f2-112">Die Datenbank, für die der Rückruf erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c95f2-112">The database for which the callback is being made.</span></span>

<span data-ttu-id="c95f2-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="c95f2-113">*tableid*</span></span>

<span data-ttu-id="c95f2-114">Der Cursor, für den der Rückruf erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c95f2-114">The cursor for which the callback is being made.</span></span>

<span data-ttu-id="c95f2-115">*cbyp*</span><span class="sxs-lookup"><span data-stu-id="c95f2-115">*cbtyp*</span></span>

<span data-ttu-id="c95f2-116">Der Punkt in dem Vorgang, an dem der Rückruf durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c95f2-116">The point in the operation at which the callback is being made.</span></span> <span data-ttu-id="c95f2-117">Unter [JET_CBTYP](./jet-cbtyp.md) finden Sie eine Liste der Werte und die Bedeutung der folgenden Parameter in jedem Fall.</span><span class="sxs-lookup"><span data-stu-id="c95f2-117">See [JET_CBTYP](./jet-cbtyp.md) for a list of values and the meaning of the following parameters in each case.</span></span>

<span data-ttu-id="c95f2-118">*pvArg1*</span><span class="sxs-lookup"><span data-stu-id="c95f2-118">*pvArg1*</span></span>

<span data-ttu-id="c95f2-119">Ein Parameter, der für die Kommunikation mit der Anwendung mithilfe des-Rückrufs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c95f2-119">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="c95f2-120">Weitere Informationen zur Verwendung dieses Parameters für jeden Rückruf, der von der Datenbank-Engine unterstützt wird, finden Sie unter [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="c95f2-120">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="c95f2-121">*pvArg2*</span><span class="sxs-lookup"><span data-stu-id="c95f2-121">*pvArg2*</span></span>

<span data-ttu-id="c95f2-122">Ein Parameter, der für die Kommunikation mit der Anwendung mithilfe des-Rückrufs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c95f2-122">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="c95f2-123">Weitere Informationen zur Verwendung dieses Parameters für jeden Rückruf, der von der Datenbank-Engine unterstützt wird, finden Sie unter [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="c95f2-123">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="c95f2-124">*pvcontext*</span><span class="sxs-lookup"><span data-stu-id="c95f2-124">*pvContext*</span></span>

<span data-ttu-id="c95f2-125">Ein Parameter, der für die Kommunikation mit der Anwendung mithilfe des-Rückrufs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c95f2-125">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="c95f2-126">Weitere Informationen zur Verwendung dieses Parameters für jeden Rückruf, der von der Datenbank-Engine unterstützt wird, finden Sie unter [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="c95f2-126">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="c95f2-127">*ulungenutzt*</span><span class="sxs-lookup"><span data-stu-id="c95f2-127">*ulUnused*</span></span>

<span data-ttu-id="c95f2-128">Ein Parameter, der für die Kommunikation mit der Anwendung mithilfe des-Rückrufs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c95f2-128">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="c95f2-129">Weitere Informationen zur Verwendung dieses Parameters für jeden Rückruf, der von der Datenbank-Engine unterstützt wird, finden Sie unter [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="c95f2-129">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c95f2-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c95f2-130">Return Value</span></span>

<span data-ttu-id="c95f2-131">Die-Funktion gibt einen der [Fehlercodes für die erweiterbare Speicher-Engine](./extensible-storage-engine-error-codes.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="c95f2-131">The function returns one of the [Extensible Storage Engine error codes](./extensible-storage-engine-error-codes.md).</span></span> <span data-ttu-id="c95f2-132">Informationen dazu, wie diese Codes als HRESULTs zurückgegeben werden, finden Sie unter [Fehler bei Extensible Storage Engine](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="c95f2-132">For information about how to return these codes as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span> <span data-ttu-id="c95f2-133">Bei Erfolg kann der Vorgang, der den Rückruf ausgegeben hat, normal fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="c95f2-133">On success, the operation that issued the callback can proceed normally.</span></span> <span data-ttu-id="c95f2-134">In einigen Fällen gibt der Rückruf möglicherweise eine Warnung zurück, die diesen Vorgang beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="c95f2-134">In some cases, the callback may return a warning that influences that operation.</span></span> <span data-ttu-id="c95f2-135">Unter [JET_CBTYP](./jet-cbtyp.md) finden Sie Informationen zur Verwendung dieser Warnungen durch den-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c95f2-135">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of these warnings by the operation.</span></span>

<span data-ttu-id="c95f2-136">Bei einem Fehler wird der Vorgang, der den Rückruf ausgegeben hat, normalerweise ordnungsgemäß fortgesetzt oder schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="c95f2-136">On failure, the operation that issued the callback may proceed normally or may fail.</span></span> <span data-ttu-id="c95f2-137">Unter [JET_CBTYP](./jet-cbtyp.md) finden Sie Informationen zur Verwendung des Fehlercodes durch den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c95f2-137">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of the error code by the operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c95f2-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c95f2-138">Remarks</span></span>

<span data-ttu-id="c95f2-139">Wenn der Rückruf einen Cursor an die Anwendung übergibt, ist es wichtig zu wissen, dass dieser Cursor absichtlich auf einen kleineren Satz von Funktionen beschränkt ist, um Rekursion und andere Hässlichkeit zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="c95f2-139">If the callback passes a cursor to the application then it is important to know that this cursor is intentionally limited to a smaller set of functionality to avoid recursion and other ugliness.</span></span> <span data-ttu-id="c95f2-140">Die folgenden Vorgänge sind zulässig:</span><span class="sxs-lookup"><span data-stu-id="c95f2-140">The following operations are allowed:</span></span>

  - [<span data-ttu-id="c95f2-141">Jetdupcursor</span><span class="sxs-lookup"><span data-stu-id="c95f2-141">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="c95f2-142">Jetenreeratecolumschlag</span><span class="sxs-lookup"><span data-stu-id="c95f2-142">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="c95f2-143">Jetgetbookmark</span><span class="sxs-lookup"><span data-stu-id="c95f2-143">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="c95f2-144">Jetgetcurrentindex</span><span class="sxs-lookup"><span data-stu-id="c95f2-144">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)

  - [<span data-ttu-id="c95f2-145">Jetgetcursor Info</span><span class="sxs-lookup"><span data-stu-id="c95f2-145">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="c95f2-146">Jetgetls</span><span class="sxs-lookup"><span data-stu-id="c95f2-146">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="c95f2-147">Jetgetrecordposition</span><span class="sxs-lookup"><span data-stu-id="c95f2-147">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)

  - [<span data-ttu-id="c95f2-148">Jetgetsecondaryindexbookmark</span><span class="sxs-lookup"><span data-stu-id="c95f2-148">JetGetSecondaryIndexBookmark</span></span>](./jetgetsecondaryindexbookmark-function.md)

  - [<span data-ttu-id="c95f2-149">Jetgettablecolumninfo</span><span class="sxs-lookup"><span data-stu-id="c95f2-149">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)

  - [<span data-ttu-id="c95f2-150">Jetgettableindexinfo</span><span class="sxs-lookup"><span data-stu-id="c95f2-150">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)

  - [<span data-ttu-id="c95f2-151">Jetgettableinfo</span><span class="sxs-lookup"><span data-stu-id="c95f2-151">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="c95f2-152">Jetregistercallback</span><span class="sxs-lookup"><span data-stu-id="c95f2-152">JetRegisterCallback</span></span>](./jetregistercallback-function.md)

  - [<span data-ttu-id="c95f2-153">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="c95f2-153">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="c95f2-154">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="c95f2-154">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="c95f2-155">Jetretrievekey</span><span class="sxs-lookup"><span data-stu-id="c95f2-155">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="c95f2-156">Jetsetcolumn</span><span class="sxs-lookup"><span data-stu-id="c95f2-156">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="c95f2-157">Jetsetcolumns</span><span class="sxs-lookup"><span data-stu-id="c95f2-157">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="c95f2-158">Jetsetls</span><span class="sxs-lookup"><span data-stu-id="c95f2-158">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="c95f2-159">Jetunregistercallback</span><span class="sxs-lookup"><span data-stu-id="c95f2-159">JetUnregisterCallback</span></span>](./jetunregistercallback-function.md)

<span data-ttu-id="c95f2-160">Berücksichtigen Sie beim Entwerfen Ihres Rückrufs, dass auch mit diesen Einschränkungen das Fehlschlagen des Rückrufs möglich ist.</span><span class="sxs-lookup"><span data-stu-id="c95f2-160">When you design your callback, take into account that even with these restrictions, it is still possible for the callback to fail.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c95f2-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c95f2-161">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c95f2-162"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c95f2-162"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c95f2-163">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c95f2-163">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c95f2-164"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c95f2-164"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c95f2-165">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c95f2-165">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c95f2-166"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c95f2-166"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c95f2-167">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="c95f2-167">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c95f2-168">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c95f2-168">See Also</span></span>

[<span data-ttu-id="c95f2-169">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="c95f2-169">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="c95f2-170">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="c95f2-170">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="c95f2-171">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c95f2-171">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c95f2-172">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c95f2-172">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c95f2-173">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="c95f2-173">JET_CBTYP</span></span>](./jet-cbtyp.md)
