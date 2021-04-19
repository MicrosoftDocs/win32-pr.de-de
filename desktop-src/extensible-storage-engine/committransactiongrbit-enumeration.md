---
description: Weitere Informationen finden Sie in der committransaktiongrbit-Enumeration.
title: Committransaktiongrbit-Enumeration
TOCTitle: CommitTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.committransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39510830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a93504d688d1eddfcde81ae23c87e62f70e0aab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366330"
---
# <a name="committransactiongrbit-enumeration"></a><span data-ttu-id="67b83-103">Committransaktiongrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="67b83-103">CommitTransactionGrbit enumeration</span></span>

<span data-ttu-id="67b83-104">Optionen für jetcommittransaction.</span><span class="sxs-lookup"><span data-stu-id="67b83-104">Options for JetCommitTransaction.</span></span>

<span data-ttu-id="67b83-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="67b83-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="67b83-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="67b83-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="67b83-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="67b83-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="67b83-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="67b83-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CommitTransactionGrbit
'Usage
Dim instance As CommitTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum CommitTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="67b83-109">Member</span><span class="sxs-lookup"><span data-stu-id="67b83-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="67b83-110">Membername</span><span class="sxs-lookup"><span data-stu-id="67b83-110">Member name</span></span></th>
<th><span data-ttu-id="67b83-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67b83-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="67b83-112">Keine</span><span class="sxs-lookup"><span data-stu-id="67b83-112">None</span></span></td>
<td><span data-ttu-id="67b83-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="67b83-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="67b83-114">Lazyflush</span><span class="sxs-lookup"><span data-stu-id="67b83-114">LazyFlush</span></span></td>
<td><span data-ttu-id="67b83-115">Die Transaktion wird normal ausgeführt, aber diese API wartet nicht, bis die Transaktion in die Transaktionsprotokoll Datei geleert wurde, bevor Sie an den Aufrufer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="67b83-115">The transaction is committed normally but this Api does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="67b83-116">Dadurch wird die Dauer eines Commitvorgangs drastisch reduziert und die Dauerhaftigkeit beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="67b83-116">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="67b83-117">Alle Transaktionen, die vor einem Absturz nicht in das Protokoll geschrieben werden, werden während des nächsten Aufrufens von jetinit automatisch abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="67b83-117">Any transaction that is not flushed to the log before a crash will be automatically aborted during crash recovery during the next call to JetInit.</span></span> <span data-ttu-id="67b83-118">Wenn WaitLastLevel0Commit oder WaitAllLevel0Commit angegeben wird, wird diese Option ignoriert.</span><span class="sxs-lookup"><span data-stu-id="67b83-118">If WaitLastLevel0Commit or WaitAllLevel0Commit are specified, this option is ignored.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="67b83-119">WaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="67b83-119">WaitLastLevel0Commit</span></span></td>
<td><span data-ttu-id="67b83-120">Wenn für die Sitzung bereits ein Commit für Transaktionen ausgeführt wurde und diese noch nicht in die Transaktionsprotokoll Datei geleert wurden, sollten Sie sofort geleert werden.</span><span class="sxs-lookup"><span data-stu-id="67b83-120">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="67b83-121">Diese API wartet, bis die Transaktionen geleert wurden, bevor Sie an den Aufrufer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="67b83-121">This Api will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="67b83-122">Dies ist nützlich, wenn die Anwendung zuvor mehrere Transaktionen mit JET_bitCommitLazyFlush committet hat und diese nun auf den Datenträger leeren möchte.</span><span class="sxs-lookup"><span data-stu-id="67b83-122">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span>
<p><span data-ttu-id="67b83-123">Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</span><span class="sxs-lookup"><span data-stu-id="67b83-123">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="67b83-124">Diese Option kann nicht in Kombination mit anderen Optionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67b83-124">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="67b83-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67b83-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="67b83-126">Referenz</span><span class="sxs-lookup"><span data-stu-id="67b83-126">Reference</span></span>

[<span data-ttu-id="67b83-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="67b83-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
