---
description: Weitere Informationen finden Sie in der JET_ENUMCOLUMN. pvData-Eigenschaft.
title: JET_ENUMCOLUMN. pvData (Eigenschaft)
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103500
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_pvData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7d4c72a45d90fd8004af2011f9f6081a59cfabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484891"
---
# <a name="jet_enumcolumnpvdata-property"></a><span data-ttu-id="8dc3c-103">JET_ENUMCOLUMN. pvData (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8dc3c-103">JET_ENUMCOLUMN.pvData property</span></span>

<span data-ttu-id="8dc3c-104">Ruft den Wert ab, der für die Spalte aufgelistet wurde.</span><span class="sxs-lookup"><span data-stu-id="8dc3c-104">Gets the value that was enumerated for the column.</span></span> <span data-ttu-id="8dc3c-105">Dieser Member wird nur verwendet, wenn [Err](./jet-enumcolumn.err-property.md) gleich [columnsinglevalue](./jet-wrn-enumeration.md)ist.</span><span class="sxs-lookup"><span data-stu-id="8dc3c-105">This member is only used if [err](./jet-enumcolumn.err-property.md) is equal to [ColumnSingleValue](./jet-wrn-enumeration.md).</span></span> <span data-ttu-id="8dc3c-106">Dies verweist auf den Arbeitsspeicher, der mit dem an [jetenumeratecolumns (JET_SESID, JET_TABLEID, Int32, \[ \] , Int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, enumeratecolumnsgrbit)](./api.jetenumeratecolumns-method.md)weiter gegebenen [JET_PFNREALLOC](./jet-pfnrealloc-delegate.md) Zuordnungs Rückruf zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="8dc3c-106">This points to memory allocated with the [JET_PFNREALLOC](./jet-pfnrealloc-delegate.md) allocator callback passed to [JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md).</span></span> <span data-ttu-id="8dc3c-107">Vergessen Sie nicht, den Arbeitsspeicher zu veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="8dc3c-107">Remember to release the memory when finished.</span></span>

<span data-ttu-id="8dc3c-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8dc3c-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8dc3c-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8dc3c-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8dc3c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dc3c-110">Syntax</span></span>

``` vb
'Declaration
Public Property pvData As IntPtr
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As IntPtr

value = instance.pvData
```

``` csharp
public IntPtr pvData { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="8dc3c-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8dc3c-111">Property value</span></span>

<span data-ttu-id="8dc3c-112">Typ: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="8dc3c-112">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  

## <a name="see-also"></a><span data-ttu-id="8dc3c-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dc3c-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8dc3c-114">Referenz</span><span class="sxs-lookup"><span data-stu-id="8dc3c-114">Reference</span></span>

[<span data-ttu-id="8dc3c-115">JET_ENUMCOLUMN-Klasse</span><span class="sxs-lookup"><span data-stu-id="8dc3c-115">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="8dc3c-116">Mitglieder JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="8dc3c-116">JET_ENUMCOLUMN members</span></span>](./jet-enumcolumn-members.md)

[<span data-ttu-id="8dc3c-117">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8dc3c-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
