---
description: Weitere Informationen finden Sie in der attachdatabasegrbit-Enumeration.
title: Attachdatabasegrbit-Enumeration
TOCTitle: AttachDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.attachdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514410
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81525e97f1b6266ba15baab50168404566bd7bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366315"
---
# <a name="attachdatabasegrbit-enumeration"></a><span data-ttu-id="f216a-103">Attachdatabasegrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="f216a-103">AttachDatabaseGrbit enumeration</span></span>

<span data-ttu-id="f216a-104">Optionen für jetattachdatabase.</span><span class="sxs-lookup"><span data-stu-id="f216a-104">Options for JetAttachDatabase.</span></span>

<span data-ttu-id="f216a-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="f216a-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="f216a-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f216a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f216a-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f216a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f216a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f216a-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration AttachDatabaseGrbit
'Usage
Dim instance As AttachDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum AttachDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="f216a-109">Member</span><span class="sxs-lookup"><span data-stu-id="f216a-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f216a-110">Membername</span><span class="sxs-lookup"><span data-stu-id="f216a-110">Member name</span></span></th>
<th><span data-ttu-id="f216a-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f216a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f216a-112">Keine</span><span class="sxs-lookup"><span data-stu-id="f216a-112">None</span></span></td>
<td><span data-ttu-id="f216a-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="f216a-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f216a-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f216a-114">ReadOnly</span></span></td>
<td><span data-ttu-id="f216a-115">Verhindert Änderungen an der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f216a-115">Prevents modifications to the database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f216a-116">Deletekorruptindexes</span><span class="sxs-lookup"><span data-stu-id="f216a-116">DeleteCorruptIndexes</span></span></td>
<td><span data-ttu-id="f216a-117">Wenn JET_paramEnableIndexChecking festgelegt wurde, werden alle Indizes für Unicode-Daten gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f216a-117">If JET_paramEnableIndexChecking has been set, all indexes over Unicode data will be deleted.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f216a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f216a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f216a-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="f216a-119">Reference</span></span>

[<span data-ttu-id="f216a-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f216a-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
