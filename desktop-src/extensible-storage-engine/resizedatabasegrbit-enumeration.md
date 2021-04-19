---
description: 'Weitere Informationen finden Sie hier: resizedatabasegrbit-Enumeration'
title: Resizedatabasegrbit-Enumeration (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: ResizeDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.resizedatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 55104329
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.OnlyGrow
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.OnlyGrow
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51d703f96882136e2b88f1a2df37609573c725e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362518"
---
# <a name="resizedatabasegrbit-enumeration"></a><span data-ttu-id="324f2-103">Resizedatabasegrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="324f2-103">ResizeDatabaseGrbit enumeration</span></span>

<span data-ttu-id="324f2-104">Optionen für [jetresizedatabase (JET_SESID, JET_DBID, Int32, Int32, resizedatabasegrbit)](./windows8api.jetresizedatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="324f2-104">Options for [JetResizeDatabase(JET_SESID, JET_DBID, Int32, Int32, ResizeDatabaseGrbit)](./windows8api.jetresizedatabase-method.md).</span></span>

<span data-ttu-id="324f2-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="324f2-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="324f2-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="324f2-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="324f2-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="324f2-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="324f2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="324f2-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ResizeDatabaseGrbit
'Usage
Dim instance As ResizeDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum ResizeDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="324f2-109">Member</span><span class="sxs-lookup"><span data-stu-id="324f2-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="324f2-110">Membername</span><span class="sxs-lookup"><span data-stu-id="324f2-110">Member name</span></span></th>
<th><span data-ttu-id="324f2-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="324f2-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="324f2-112">Keine</span><span class="sxs-lookup"><span data-stu-id="324f2-112">None</span></span></td>
<td><span data-ttu-id="324f2-113">Keine Option.</span><span class="sxs-lookup"><span data-stu-id="324f2-113">No option.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="324f2-114">Onlygrow</span><span class="sxs-lookup"><span data-stu-id="324f2-114">OnlyGrow</span></span></td>
<td><span data-ttu-id="324f2-115">Vergrößern Sie nur die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="324f2-115">Only grow the database.</span></span> <span data-ttu-id="324f2-116">Wenn der Größenänderung die Datenbank verkleinern würde, führen Sie keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="324f2-116">If the resize call would shrink the database, do nothing.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="324f2-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="324f2-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="324f2-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="324f2-118">Reference</span></span>

[<span data-ttu-id="324f2-119">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="324f2-119">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
