---
description: Weitere Informationen finden Sie in der getlockgrbit-Enumeration.
title: Getlockgrbit-Enumeration
TOCTitle: GetLockGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetLockGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getlockgrbit(v=EXCHG.10)
ms:contentKeyID: 39512424
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cfcad088fa93d73910a0333d3aca9a700e97996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959247"
---
# <a name="getlockgrbit-enumeration"></a><span data-ttu-id="04483-103">Getlockgrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="04483-103">GetLockGrbit enumeration</span></span>

<span data-ttu-id="04483-104">Optionen für jetgetlock.</span><span class="sxs-lookup"><span data-stu-id="04483-104">Options for JetGetLock.</span></span>

<span data-ttu-id="04483-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="04483-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="04483-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="04483-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="04483-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="04483-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="04483-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="04483-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetLockGrbit
'Usage
Dim instance As GetLockGrbit
```

``` csharp
[FlagsAttribute]
public enum GetLockGrbit
```

## <a name="members"></a><span data-ttu-id="04483-109">Member</span><span class="sxs-lookup"><span data-stu-id="04483-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="04483-110">Membername</span><span class="sxs-lookup"><span data-stu-id="04483-110">Member name</span></span></th>
<th><span data-ttu-id="04483-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04483-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="04483-112">Lesen</span><span class="sxs-lookup"><span data-stu-id="04483-112">Read</span></span></td>
<td><span data-ttu-id="04483-113">Erhält eine Lesesperre für den aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="04483-113">Acquire a read lock on the current record.</span></span> <span data-ttu-id="04483-114">Lese Sperren sind nicht kompatibel mit Schreib sperren, die bereits von anderen Sitzungen gehalten wurden, aber mit Lese Sperren von anderen Sitzungen kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="04483-114">Read locks are incompatible with write locks already held by other sessions but are compatible with read locks held by other sessions.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="04483-115">Schreiben</span><span class="sxs-lookup"><span data-stu-id="04483-115">Write</span></span></td>
<td><span data-ttu-id="04483-116">Rufen Sie eine Schreibsperre für den aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="04483-116">Acquire a write lock on the current record.</span></span> <span data-ttu-id="04483-117">Schreib Sperren sind nicht kompatibel mit Schreib-oder Lese sperren, die von anderen Sitzungen aufrechterhalten werden, aber mit Lese Sperren in derselben Sitzung kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="04483-117">Write locks are not compatible with write or read locks held by other sessions but are compatible with read locks held by the same session.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="04483-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04483-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="04483-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="04483-119">Reference</span></span>

[<span data-ttu-id="04483-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="04483-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
