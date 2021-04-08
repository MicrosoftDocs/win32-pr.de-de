---
description: 'Weitere Informationen finden Sie unter: termgrbit-Enumeration'
title: Termgrbit-Enumeration
TOCTitle: TermGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TermGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.termgrbit(v=EXCHG.10)
ms:contentKeyID: 39511147
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TermGrbit.None
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 49b466b298a78d7bfd6822904aed977e7117b927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759085"
---
# <a name="termgrbit-enumeration"></a><span data-ttu-id="60ea3-103">Termgrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="60ea3-103">TermGrbit enumeration</span></span>

<span data-ttu-id="60ea3-104">Optionen für [JetTerm2 (JET_INSTANCE, termgrbit)](./api.jetterm2-method.md).</span><span class="sxs-lookup"><span data-stu-id="60ea3-104">Options for [JetTerm2(JET_INSTANCE, TermGrbit)](./api.jetterm2-method.md).</span></span>

<span data-ttu-id="60ea3-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="60ea3-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="60ea3-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="60ea3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="60ea3-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="60ea3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="60ea3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="60ea3-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TermGrbit
'Usage
Dim instance As TermGrbit
```

``` csharp
[FlagsAttribute]
public enum TermGrbit
```

## <a name="members"></a><span data-ttu-id="60ea3-109">Member</span><span class="sxs-lookup"><span data-stu-id="60ea3-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="60ea3-110">Membername</span><span class="sxs-lookup"><span data-stu-id="60ea3-110">Member name</span></span></th>
<th><span data-ttu-id="60ea3-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60ea3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="60ea3-112">Keine</span><span class="sxs-lookup"><span data-stu-id="60ea3-112">None</span></span></td>
<td><span data-ttu-id="60ea3-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="60ea3-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="60ea3-114">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="60ea3-114">Complete</span></span></td>
<td><span data-ttu-id="60ea3-115">Fordert an, dass die Instanz ordnungsgemäß heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="60ea3-115">Requests that the instance be shut down cleanly.</span></span> <span data-ttu-id="60ea3-116">Alle optionalen Bereinigungs arbeiten, die normalerweise zur Laufzeit im Hintergrund durchgeführt werden, werden sofort abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="60ea3-116">Any optional cleanup work that would ordinarily be done in the background at run time is completed immediately.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="60ea3-117">Ter</span><span class="sxs-lookup"><span data-stu-id="60ea3-117">Abrupt</span></span></td>
<td><span data-ttu-id="60ea3-118">Fordert an, dass die Instanz so schnell wie möglich heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="60ea3-118">Requests that the instance be shut down as quickly as possible.</span></span> <span data-ttu-id="60ea3-119">Alle optionalen arbeiten, die normalerweise zur Laufzeit im Hintergrund durchgeführt werden, werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="60ea3-119">Any optional work that would ordinarily be done in the background at run time is abandoned.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="60ea3-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60ea3-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="60ea3-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="60ea3-121">Reference</span></span>

[<span data-ttu-id="60ea3-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="60ea3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="60ea3-123">TZI</span><span class="sxs-lookup"><span data-stu-id="60ea3-123">Dirty</span></span>](./windows7grbits.dirty-field.md)
