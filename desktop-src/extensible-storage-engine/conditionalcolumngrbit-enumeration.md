---
description: 'Weitere Informationen finden Sie hier: conditionalcolumngrbit-Enumeration'
title: Conditionalcolumngrbit-Enumeration
TOCTitle: ConditionalColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conditionalcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39513009
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNonNull
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNull
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNonNull
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82828df5d5a25dac08a2a8ab560225456f075a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959153"
---
# <a name="conditionalcolumngrbit-enumeration"></a><span data-ttu-id="c7893-103">Conditionalcolumngrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="c7893-103">ConditionalColumnGrbit enumeration</span></span>

<span data-ttu-id="c7893-104">Optionen für die JET_CONDITIONALCOLUMN Struktur.</span><span class="sxs-lookup"><span data-stu-id="c7893-104">Options for the JET_CONDITIONALCOLUMN structure.</span></span>

<span data-ttu-id="c7893-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="c7893-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="c7893-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c7893-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c7893-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c7893-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c7893-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7893-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ConditionalColumnGrbit
'Usage
Dim instance As ConditionalColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum ConditionalColumnGrbit
```

## <a name="members"></a><span data-ttu-id="c7893-109">Member</span><span class="sxs-lookup"><span data-stu-id="c7893-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c7893-110">Membername</span><span class="sxs-lookup"><span data-stu-id="c7893-110">Member name</span></span></th>
<th><span data-ttu-id="c7893-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7893-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c7893-112">Columnmustbenull</span><span class="sxs-lookup"><span data-stu-id="c7893-112">ColumnMustBeNull</span></span></td>
<td><span data-ttu-id="c7893-113">Die Spalte muss NULL sein, damit ein Index Eintrag im Index angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c7893-113">The column must be null for an index entry to appear in the index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c7893-114">Columnmustbenonnull</span><span class="sxs-lookup"><span data-stu-id="c7893-114">ColumnMustBeNonNull</span></span></td>
<td><span data-ttu-id="c7893-115">Die Spalte darf nicht NULL sein, damit ein Index Eintrag im Index angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c7893-115">The column must be non-null for an index entry to appear in the index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="c7893-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7893-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c7893-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="c7893-117">Reference</span></span>

[<span data-ttu-id="c7893-118">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="c7893-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
