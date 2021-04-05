---
description: 'Weitere Informationen finden Sie hier: lsgrbit-Enumeration'
title: Lsgrbit-Enumeration
TOCTitle: LsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.LsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.lsgrbit(v=EXCHG.10)
ms:contentKeyID: 39514518
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.LsGrbit
- Microsoft.Isam.Esent.Interop.LsGrbit.Cursor
- Microsoft.Isam.Esent.Interop.LsGrbit.None
- Microsoft.Isam.Esent.Interop.LsGrbit.Reset
- Microsoft.Isam.Esent.Interop.LsGrbit.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.LsGrbit
- Microsoft.Isam.Esent.Interop.LsGrbit.Reset
- Microsoft.Isam.Esent.Interop.LsGrbit.None
- Microsoft.Isam.Esent.Interop.LsGrbit.Table
- Microsoft.Isam.Esent.Interop.LsGrbit.Cursor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fc0a60d039d0eb1307558d42a3e7a3c7e99eb86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041797"
---
# <a name="lsgrbit-enumeration"></a><span data-ttu-id="f0d13-103">Lsgrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="f0d13-103">LsGrbit enumeration</span></span>

<span data-ttu-id="f0d13-104">Optionen für [jetsetls (JET_SESID, JET_TABLEID, JET_LS, lsgrbit)](./api.jetsetls-method.md) und [jetgetls (JET_SESID, JET_TABLEID, JET_LS, lsgrbit)](./api.jetgetls-method.md).</span><span class="sxs-lookup"><span data-stu-id="f0d13-104">Options for [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md) and [JetGetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md).</span></span>

<span data-ttu-id="f0d13-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="f0d13-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="f0d13-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f0d13-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f0d13-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f0d13-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f0d13-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0d13-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration LsGrbit
'Usage
Dim instance As LsGrbit
```

``` csharp
[FlagsAttribute]
public enum LsGrbit
```

## <a name="members"></a><span data-ttu-id="f0d13-109">Member</span><span class="sxs-lookup"><span data-stu-id="f0d13-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f0d13-110">Membername</span><span class="sxs-lookup"><span data-stu-id="f0d13-110">Member name</span></span></th>
<th><span data-ttu-id="f0d13-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0d13-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f0d13-112">Keine</span><span class="sxs-lookup"><span data-stu-id="f0d13-112">None</span></span></td>
<td><span data-ttu-id="f0d13-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="f0d13-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f0d13-114">Reset</span><span class="sxs-lookup"><span data-stu-id="f0d13-114">Reset</span></span></td>
<td><span data-ttu-id="f0d13-115">Das Kontext Handle für das ausgewählte Objekt sollte auf JET_LSNil zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="f0d13-115">The context handle for the chosen object should be reset to JET_LSNil.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f0d13-116">Cursor</span><span class="sxs-lookup"><span data-stu-id="f0d13-116">Cursor</span></span></td>
<td><span data-ttu-id="f0d13-117">Gibt an, dass das Kontext Handle dem angegebenen Cursor zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0d13-117">Specifies the context handle should be associated with the given cursor.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f0d13-118">Tabelle</span><span class="sxs-lookup"><span data-stu-id="f0d13-118">Table</span></span></td>
<td><span data-ttu-id="f0d13-119">Gibt an, dass das Kontext Handle der Tabelle zugeordnet werden soll, die dem angegebenen Cursor zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f0d13-119">Specifies that the context handle should be associated with the table associated with the given cursor.</span></span> <span data-ttu-id="f0d13-120">Die Verwendung dieser Option mit Cursor ist unzulässig.</span><span class="sxs-lookup"><span data-stu-id="f0d13-120">It is illegal to use this option with Cursor.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f0d13-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0d13-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f0d13-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="f0d13-122">Reference</span></span>

[<span data-ttu-id="f0d13-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f0d13-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
