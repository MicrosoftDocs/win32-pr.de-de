---
description: 'Weitere Informationen finden Sie hier: JET_SESID'
title: JET_SESID
TOCTitle: JET_SESID
ms:assetid: 56b53532-e0a8-4255-8442-bb90184d91da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269253(v=EXCHG.10)
ms:contentKeyID: 32765555
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
ms.openlocfilehash: 542802c806bbea55aafb4fc1a0241a92b2842878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862208"
---
# <a name="jet_sesid"></a><span data-ttu-id="4d4ce-103">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4d4ce-103">JET_SESID</span></span>


<span data-ttu-id="4d4ce-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4d4ce-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_sesid"></a><span data-ttu-id="4d4ce-105">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4d4ce-105">JET_SESID</span></span>

<span data-ttu-id="4d4ce-106">Der **JET_SESID** -Datentyp enthält ein Handle für die Sitzung, die für einen aufzurufenden Jet-API-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d4ce-106">The **JET_SESID** data type contains a handle to the session to use for a call to the JET API.</span></span>

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a><span data-ttu-id="4d4ce-107">Datentypen</span><span class="sxs-lookup"><span data-stu-id="4d4ce-107">Data Types</span></span>

<span data-ttu-id="4d4ce-108">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4d4ce-108">JET_SESID</span></span>

<span data-ttu-id="4d4ce-109">Entweder **null** oder [JET_sesidNil](./invalid-handle-constants.md) kann verwendet werden, um ein ungültiges Sitzungs handle anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4d4ce-109">Either **NULL** or [JET_sesidNil](./invalid-handle-constants.md) can be used to indicate an invalid session handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="4d4ce-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d4ce-110">Remarks</span></span>

<span data-ttu-id="4d4ce-111">Eine Sitzung ist der Transaktionskontext der Datenbank-Engine.</span><span class="sxs-lookup"><span data-stu-id="4d4ce-111">A session is the transaction context of the database engine.</span></span> <span data-ttu-id="4d4ce-112">Sie kann verwendet werden, um Transaktionen zu starten, zu übertragen oder abzubrechen, die die Sichtbarkeit und Dauerhaftigkeit von Änderungen, die von dieser oder anderen Sitzungen vorgenommen werden, beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="4d4ce-112">It can be used to begin, commit, or abort transactions that affect the visibility and durability of changes that are made by this or other sessions.</span></span>

<span data-ttu-id="4d4ce-113">Eine Transaktion kann mithilfe von [jetbegintransaction](./jetbegintransaction-function.md)gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="4d4ce-113">A transaction can be started using [JetBeginTransaction](./jetbegintransaction-function.md).</span></span> <span data-ttu-id="4d4ce-114">Eine Sitzung kann mithilfe von [jetbeginsession](./jetbeginsession-function.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4d4ce-114">A session may be created using [JetBeginSession](./jetbeginsession-function.md).</span></span> <span data-ttu-id="4d4ce-115">Die maximale Anzahl von Sitzungen, die zu einem beliebigen Zeitpunkt erstellt werden können, wird durch [JET_paramMaxSessions](./resource-parameters.md)gesteuert, der mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md)konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4d4ce-115">The maximum number of sessions that can be created at any one time is controlled by [JET_paramMaxSessions](./resource-parameters.md), which can be configured by means of [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="4d4ce-116">Eine Sitzung wird explizit durch einen " [jetendsession](./jetendsession-function.md) "-Rückruf beendet oder durch einen " [jetterm](./jetterm-function.md)"-Befehl implizit beendet.</span><span class="sxs-lookup"><span data-stu-id="4d4ce-116">A session is explicitly ended by a call to [JetEndSession](./jetendsession-function.md) or implicitly ended by a call to [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="4d4ce-117">Jede Sitzung kann nur von einem Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d4ce-117">Each session can only be used by one thread at a time.</span></span> <span data-ttu-id="4d4ce-118">Außerdem besteht das Standardverhalten der-Engine darin, die Verwendung einer Sitzung auf denselben Thread ab dem Zeitpunkt zu beschränken, zu dem der erste Aufruf von [jetbegintransaction](./jetbegintransaction-function.md) bis zu dem Zeitpunkt erfolgt, zu dem der Aufruf von [jetcommittransaction](./jetcommittransaction-function.md) oder [jetrollback](./jetrollback-function.md) durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d4ce-118">In addition, the default behavior of the engine is to restrict the use of a session to the same thread from the time the first call to [JetBeginTransaction](./jetbegintransaction-function.md) is made until the time when the matching call to [JetCommitTransaction](./jetcommittransaction-function.md) or [JetRollback](./jetrollback-function.md) is made.</span></span> <span data-ttu-id="4d4ce-119">Dieses Verhalten kann geändert werden, um diese zweite Einschränkung zu entfernen, indem ein benutzerdefinierter Sitzungs Kontext mithilfe von [jetsetessioncontext](./jetsetsessioncontext-function.md) und [jetresetessioncontext](./jetresetsessioncontext-function.md)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4d4ce-119">This behavior can be changed to remove this second restriction by setting a custom session context using [JetSetSessionContext](./jetsetsessioncontext-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="4d4ce-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d4ce-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d4ce-121"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="4d4ce-121"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4d4ce-122">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4d4ce-122">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d4ce-123"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4d4ce-123"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4d4ce-124">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4d4ce-124">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d4ce-125"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4d4ce-125"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4d4ce-126">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="4d4ce-126">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="4d4ce-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4d4ce-127">See Also</span></span>

[<span data-ttu-id="4d4ce-128">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="4d4ce-128">JET_paramMaxSessions</span></span>](./resource-parameters.md)  
[<span data-ttu-id="4d4ce-129">Jetbeginsession</span><span class="sxs-lookup"><span data-stu-id="4d4ce-129">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="4d4ce-130">Jetbegintransaction</span><span class="sxs-lookup"><span data-stu-id="4d4ce-130">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="4d4ce-131">Jetcommittransaction</span><span class="sxs-lookup"><span data-stu-id="4d4ce-131">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="4d4ce-132">Jetendsession</span><span class="sxs-lookup"><span data-stu-id="4d4ce-132">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="4d4ce-133">Jetresessioncontext</span><span class="sxs-lookup"><span data-stu-id="4d4ce-133">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="4d4ce-134">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="4d4ce-134">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="4d4ce-135">Jetabessioncontext</span><span class="sxs-lookup"><span data-stu-id="4d4ce-135">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="4d4ce-136">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="4d4ce-136">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="4d4ce-137">Jetterm</span><span class="sxs-lookup"><span data-stu-id="4d4ce-137">JetTerm</span></span>](./jetterm-function.md)
