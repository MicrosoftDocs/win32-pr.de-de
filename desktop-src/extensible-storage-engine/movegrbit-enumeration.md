---
description: 'Weitere Informationen finden Sie in der folgenden Artikel-Enumeration:'
title: "\"Muvegrbit\"-Enumeration"
TOCTitle: MoveGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MoveGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.movegrbit(v=EXCHG.10)
ms:contentKeyID: 39513771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MoveGrbit
- Microsoft.Isam.Esent.Interop.MoveGrbit.MoveKeyNE
- Microsoft.Isam.Esent.Interop.MoveGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MoveGrbit
- Microsoft.Isam.Esent.Interop.MoveGrbit.None
- Microsoft.Isam.Esent.Interop.MoveGrbit.MoveKeyNE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81f047cd69bca668a5eae2b5147d8c0a137011e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042351"
---
# <a name="movegrbit-enumeration"></a><span data-ttu-id="3b22c-103">"Muvegrbit"-Enumeration</span><span class="sxs-lookup"><span data-stu-id="3b22c-103">MoveGrbit enumeration</span></span>

<span data-ttu-id="3b22c-104">Optionen für jetmove.</span><span class="sxs-lookup"><span data-stu-id="3b22c-104">Options for JetMove.</span></span>

<span data-ttu-id="3b22c-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="3b22c-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="3b22c-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3b22c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3b22c-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3b22c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3b22c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b22c-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MoveGrbit
'Usage
Dim instance As MoveGrbit
```

``` csharp
[FlagsAttribute]
public enum MoveGrbit
```

## <a name="members"></a><span data-ttu-id="3b22c-109">Member</span><span class="sxs-lookup"><span data-stu-id="3b22c-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="3b22c-110">Membername</span><span class="sxs-lookup"><span data-stu-id="3b22c-110">Member name</span></span></th>
<th><span data-ttu-id="3b22c-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b22c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3b22c-112">Keine</span><span class="sxs-lookup"><span data-stu-id="3b22c-112">None</span></span></td>
<td><span data-ttu-id="3b22c-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="3b22c-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3b22c-114">"Muvekeyne"</span><span class="sxs-lookup"><span data-stu-id="3b22c-114">MoveKeyNE</span></span></td>
<td><span data-ttu-id="3b22c-115">Verschiebt den Cursor um die Anzahl der Indexeinträge, die erforderlich sind, um die angeforderte Anzahl von Index Schlüsselwerten im Index zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="3b22c-115">Moves the cursor forward or backward by the number of index entries required to skip the requested number of index key values encountered in the index.</span></span> <span data-ttu-id="3b22c-116">Dies hat den Effekt, dass Indexeinträge mit doppelten Schlüsselwerten in einem einzelnen Index Eintrag reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="3b22c-116">This has the effect of collapsing index entries with duplicate key values into a single index entry.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="3b22c-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b22c-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3b22c-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="3b22c-118">Reference</span></span>

[<span data-ttu-id="3b22c-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="3b22c-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
