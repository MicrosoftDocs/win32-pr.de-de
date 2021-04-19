---
description: 'Weitere Informationen finden Sie hier: Server2003Grbits. enumerateignoreuserdefineddefault-Feld'
title: Server2003Grbits. enumerateignoreuserdefineddefault-Feld (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: EnumerateIgnoreUserDefinedDefault field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.enumerateignoreuserdefineddefault(v=EXCHG.10)
ms:contentKeyID: 55104099
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 508565c518b67d31b0299014817b669f9484f743
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349887"
---
# <a name="server2003grbitsenumerateignoreuserdefineddefault-field"></a><span data-ttu-id="64f46-103">Server2003Grbits. enumerateignoreuserdefineddefault-Feld</span><span class="sxs-lookup"><span data-stu-id="64f46-103">Server2003Grbits.EnumerateIgnoreUserDefinedDefault field</span></span>

<span data-ttu-id="64f46-104">Wenn eine bestimmte Spalte nicht im Datensatz vorhanden ist und über einen benutzerdefinierten Standardwert verfügt, wird kein Spaltenwert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="64f46-104">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="64f46-105">Mit dieser Option wird verhindert, dass der Rückruf, der den benutzerdefinierten Standardwert für die Spalte berechnet, beim Auflisten der Werte für diese Spalte aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="64f46-105">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span>

<span data-ttu-id="64f46-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="64f46-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="64f46-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="64f46-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="64f46-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="64f46-108">Syntax</span></span>

``` vb
'Declaration
Public Const EnumerateIgnoreUserDefinedDefault As EnumerateColumnsGrbit
'Usage
Dim value As EnumerateColumnsGrbit

value = Server2003Grbits.EnumerateIgnoreUserDefinedDefault
```

``` csharp
public const EnumerateColumnsGrbit EnumerateIgnoreUserDefinedDefault
```

## <a name="remarks"></a><span data-ttu-id="64f46-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64f46-109">Remarks</span></span>

<span data-ttu-id="64f46-110">Diese Option ist nur für Windows Server 2003 SP1 und spätere Betriebssysteme verfügbar.</span><span class="sxs-lookup"><span data-stu-id="64f46-110">This option is only available for Windows Server 2003 SP1 and later operating systems.</span></span>

## <a name="see-also"></a><span data-ttu-id="64f46-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64f46-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="64f46-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="64f46-112">Reference</span></span>

[<span data-ttu-id="64f46-113">Server2003Grbits-Klasse</span><span class="sxs-lookup"><span data-stu-id="64f46-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="64f46-114">Server2003Grbits-Member</span><span class="sxs-lookup"><span data-stu-id="64f46-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="64f46-115">Microsoft. ISAM. ESENT. Interop. Server2003-Namespace</span><span class="sxs-lookup"><span data-stu-id="64f46-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
