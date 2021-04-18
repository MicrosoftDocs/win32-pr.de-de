---
description: Weitere Informationen finden Sie in der getrecordsizegrbit-Enumeration.
title: Getrecordsizegrbit-Enumeration
TOCTitle: GetRecordSizeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getrecordsizegrbit(v=EXCHG.10)
ms:contentKeyID: 39514742
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee95d29ed1913993aa37062137807bf8d635eecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368180"
---
# <a name="getrecordsizegrbit-enumeration"></a><span data-ttu-id="4ab66-103">Getrecordsizegrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="4ab66-103">GetRecordSizeGrbit enumeration</span></span>

<span data-ttu-id="4ab66-104">Optionen für [jetgetrecordsize (JET_SESID, JET_TABLEID, JET_RECSIZE, getrecordsizegrbit)](./vistaapi.jetgetrecordsize-method.md).</span><span class="sxs-lookup"><span data-stu-id="4ab66-104">Options for [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md).</span></span>

<span data-ttu-id="4ab66-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="4ab66-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="4ab66-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4ab66-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4ab66-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4ab66-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4ab66-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ab66-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetRecordSizeGrbit
'Usage
Dim instance As GetRecordSizeGrbit
```

``` csharp
[FlagsAttribute]
public enum GetRecordSizeGrbit
```

## <a name="members"></a><span data-ttu-id="4ab66-109">Member</span><span class="sxs-lookup"><span data-stu-id="4ab66-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="4ab66-110">Membername</span><span class="sxs-lookup"><span data-stu-id="4ab66-110">Member name</span></span></th>
<th><span data-ttu-id="4ab66-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ab66-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="4ab66-112">Keine</span><span class="sxs-lookup"><span data-stu-id="4ab66-112">None</span></span></td>
<td><span data-ttu-id="4ab66-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="4ab66-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="4ab66-114">Incopybuffer</span><span class="sxs-lookup"><span data-stu-id="4ab66-114">InCopyBuffer</span></span></td>
<td><span data-ttu-id="4ab66-115">Ruft die Größe des Datensatzes ab, der im Kopierpuffer vorbereitet oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="4ab66-115">Retrieve the size of the record that is in the copy buffer prepared or update.</span></span> <span data-ttu-id="4ab66-116">Andernfalls muss der TableID-Wert auf einem Datensatz positioniert werden, und dieser Datensatz wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ab66-116">Otherwise, the tableid must be positioned on a record, and that record will be used.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="4ab66-117">RunningTotal</span><span class="sxs-lookup"><span data-stu-id="4ab66-117">RunningTotal</span></span></td>
<td><span data-ttu-id="4ab66-118">Die JET_RECSIZE wird nicht vor dem Ausfüllen der Inhalte nullte und fungiert effektiv als Ansammlung der Statistiken für mehrere besuchte oder aktualisierte Datensätze.</span><span class="sxs-lookup"><span data-stu-id="4ab66-118">The JET_RECSIZE is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="4ab66-119">Lokal</span><span class="sxs-lookup"><span data-stu-id="4ab66-119">Local</span></span></td>
<td><span data-ttu-id="4ab66-120">Ignoriert nicht intrinsische Long-Werte.</span><span class="sxs-lookup"><span data-stu-id="4ab66-120">Ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="4ab66-121">Es wird nur der lokale Datensatz auf der Seite verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ab66-121">Only the local record on the page will be used.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="4ab66-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ab66-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4ab66-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="4ab66-123">Reference</span></span>

[<span data-ttu-id="4ab66-124">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="4ab66-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
