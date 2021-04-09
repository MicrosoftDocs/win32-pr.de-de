---
description: 'Weitere Informationen finden Sie hier: objectinfoflags-Enumeration'
title: Objectinfoflags-Enumeration
TOCTitle: ObjectInfoFlags enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfoflags(v=EXCHG.10)
ms:contentKeyID: 39515824
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b3f301f1e786d126dbd57c071fe89356e0acc891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865623"
---
# <a name="objectinfoflags-enumeration"></a><span data-ttu-id="8ede7-103">Objectinfoflags-Enumeration</span><span class="sxs-lookup"><span data-stu-id="8ede7-103">ObjectInfoFlags enumeration</span></span>

<span data-ttu-id="8ede7-104">Flags für ESENT-Objekte (Tabellen).</span><span class="sxs-lookup"><span data-stu-id="8ede7-104">Flags for ESENT objects (tables).</span></span> <span data-ttu-id="8ede7-105">Wird in [JET_OBJECTINFO](./jet-objectinfo-class.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ede7-105">Used in [JET_OBJECTINFO](./jet-objectinfo-class.md).</span></span>

<span data-ttu-id="8ede7-106">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="8ede7-106">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="8ede7-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8ede7-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8ede7-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8ede7-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8ede7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ede7-109">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoFlags
'Usage
Dim instance As ObjectInfoFlags
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoFlags
```

## <a name="members"></a><span data-ttu-id="8ede7-110">Member</span><span class="sxs-lookup"><span data-stu-id="8ede7-110">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="8ede7-111">Membername</span><span class="sxs-lookup"><span data-stu-id="8ede7-111">Member name</span></span></th>
<th><span data-ttu-id="8ede7-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ede7-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8ede7-113">Keine</span><span class="sxs-lookup"><span data-stu-id="8ede7-113">None</span></span></td>
<td><span data-ttu-id="8ede7-114">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="8ede7-114">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8ede7-115">System</span><span class="sxs-lookup"><span data-stu-id="8ede7-115">System</span></span></td>
<td><span data-ttu-id="8ede7-116">Das Objekt ist nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="8ede7-116">Object is for internal use only.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8ede7-117">Tablefixedddl</span><span class="sxs-lookup"><span data-stu-id="8ede7-117">TableFixedDDL</span></span></td>
<td><span data-ttu-id="8ede7-118">Die DDL der Tabelle ist korrigiert.</span><span class="sxs-lookup"><span data-stu-id="8ede7-118">Table's DDL is fixed.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8ede7-119">TableTemplate</span><span class="sxs-lookup"><span data-stu-id="8ede7-119">TableTemplate</span></span></td>
<td><span data-ttu-id="8ede7-120">Die DDL der Tabelle ist vererbbar.</span><span class="sxs-lookup"><span data-stu-id="8ede7-120">Table's DDL is inheritable.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8ede7-121">Tableabgeleitet</span><span class="sxs-lookup"><span data-stu-id="8ede7-121">TableDerived</span></span></td>
<td><span data-ttu-id="8ede7-122">Die DDL der Tabelle wird von einer Vorlagen Tabelle geerbt.</span><span class="sxs-lookup"><span data-stu-id="8ede7-122">Table's DDL is inherited from a template table.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8ede7-123">Tablenofixedvarcolumnsinderivedtables</span><span class="sxs-lookup"><span data-stu-id="8ede7-123">TableNoFixedVarColumnsInDerivedTables</span></span></td>
<td><span data-ttu-id="8ede7-124">Korrigiert oder Variablen Spalten in abgeleiteten Tabellen (damit der Vorlage in Zukunft festgelegte oder Variable Spalten hinzugefügt werden können).</span><span class="sxs-lookup"><span data-stu-id="8ede7-124">Fixed or variable columns in derived tables (so that fixed or variable columns can be added to the template in the future).</span></span> <span data-ttu-id="8ede7-125">Wird in Verbindung mit TableTemplate verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ede7-125">Used in conjunction with TableTemplate.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8ede7-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ede7-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8ede7-127">Referenz</span><span class="sxs-lookup"><span data-stu-id="8ede7-127">Reference</span></span>

[<span data-ttu-id="8ede7-128">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8ede7-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
