---
description: 'Weitere Informationen finden Sie hier: Aufzählung von "kreatetablecolumnindexgrbit"'
title: Kreatetablecolumnindexgrbit-Enumeration
TOCTitle: CreateTableColumnIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createtablecolumnindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39516657
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72f91c5d41b8262e3b2804159914b0a9ccaaaa7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960785"
---
# <a name="createtablecolumnindexgrbit-enumeration"></a><span data-ttu-id="3760b-103">Kreatetablecolumnindexgrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="3760b-103">CreateTableColumnIndexGrbit enumeration</span></span>

<span data-ttu-id="3760b-104">Optionen für jetkreatetablecolumnindex.</span><span class="sxs-lookup"><span data-stu-id="3760b-104">Options for JetCreateTableColumnIndex.</span></span>

<span data-ttu-id="3760b-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="3760b-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="3760b-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3760b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3760b-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3760b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3760b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3760b-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateTableColumnIndexGrbit
'Usage
Dim instance As CreateTableColumnIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateTableColumnIndexGrbit
```

## <a name="members"></a><span data-ttu-id="3760b-109">Member</span><span class="sxs-lookup"><span data-stu-id="3760b-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="3760b-110">Membername</span><span class="sxs-lookup"><span data-stu-id="3760b-110">Member name</span></span></th>
<th><span data-ttu-id="3760b-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3760b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3760b-112">Keine</span><span class="sxs-lookup"><span data-stu-id="3760b-112">None</span></span></td>
<td><span data-ttu-id="3760b-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="3760b-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3760b-114">Fixedddl</span><span class="sxs-lookup"><span data-stu-id="3760b-114">FixedDDL</span></span></td>
<td><span data-ttu-id="3760b-115">Die DDL ist korrigiert.</span><span class="sxs-lookup"><span data-stu-id="3760b-115">The DDL is fixed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3760b-116">Templatetable</span><span class="sxs-lookup"><span data-stu-id="3760b-116">TemplateTable</span></span></td>
<td><span data-ttu-id="3760b-117">Die DDL ist vererbbar.</span><span class="sxs-lookup"><span data-stu-id="3760b-117">The DDL is inheritable.</span></span> <span data-ttu-id="3760b-118">Impliziert fixedddl.</span><span class="sxs-lookup"><span data-stu-id="3760b-118">Implies FixedDDL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3760b-119">Nofixedvarcolumnsinderivedtables</span><span class="sxs-lookup"><span data-stu-id="3760b-119">NoFixedVarColumnsInDerivedTables</span></span></td>
<td><span data-ttu-id="3760b-120">Wird in Verbindung mit "templatetable" verwendet.</span><span class="sxs-lookup"><span data-stu-id="3760b-120">Used in conjunction with TemplateTable.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="3760b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3760b-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3760b-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="3760b-122">Reference</span></span>

[<span data-ttu-id="3760b-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="3760b-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
