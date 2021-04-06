---
description: 'Weitere Informationen finden Sie hier: begintransaktiongrbit-Enumeration'
title: Begintransaktiongrbit-Enumeration
TOCTitle: BeginTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.begintransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39515115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5f407c54b7b6e76ab63dcfb97d1307458ba15277
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758970"
---
# <a name="begintransactiongrbit-enumeration"></a><span data-ttu-id="1e8d0-103">Begintransaktiongrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="1e8d0-103">BeginTransactionGrbit enumeration</span></span>

<span data-ttu-id="1e8d0-104">Optionen für [JetBeginTransaction2 (JET_SESID, begintransaktiongrbit)](./api.jetbegintransaction2-method.md).</span><span class="sxs-lookup"><span data-stu-id="1e8d0-104">Options for [JetBeginTransaction2(JET_SESID, BeginTransactionGrbit)](./api.jetbegintransaction2-method.md).</span></span>

<span data-ttu-id="1e8d0-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="1e8d0-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="1e8d0-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1e8d0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1e8d0-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1e8d0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1e8d0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e8d0-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginTransactionGrbit
'Usage
Dim instance As BeginTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="1e8d0-109">Member</span><span class="sxs-lookup"><span data-stu-id="1e8d0-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="1e8d0-110">Membername</span><span class="sxs-lookup"><span data-stu-id="1e8d0-110">Member name</span></span></th>
<th><span data-ttu-id="1e8d0-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e8d0-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1e8d0-112">Keine</span><span class="sxs-lookup"><span data-stu-id="1e8d0-112">None</span></span></td>
<td><span data-ttu-id="1e8d0-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="1e8d0-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1e8d0-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1e8d0-114">ReadOnly</span></span></td>
<td><span data-ttu-id="1e8d0-115">Die Datenbank wird von der Transaktion nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="1e8d0-115">The transaction will not modify the database.</span></span> <span data-ttu-id="1e8d0-116">Wenn versucht wird, ein Update auszuführen, schlägt dieser Vorgang mit <a href="hh564840(v=exchg.10).md">transread only</a>fehl.</span><span class="sxs-lookup"><span data-stu-id="1e8d0-116">If an update is attempted, that operation will fail with <a href="hh564840(v=exchg.10).md">TransReadOnly</a>.</span></span> <span data-ttu-id="1e8d0-117">Diese Option wird ignoriert, es sei denn, Sie wird angefordert, wenn die angegebene Sitzung nicht bereits in einer Transaktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1e8d0-117">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="1e8d0-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e8d0-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1e8d0-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="1e8d0-119">Reference</span></span>

[<span data-ttu-id="1e8d0-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="1e8d0-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
