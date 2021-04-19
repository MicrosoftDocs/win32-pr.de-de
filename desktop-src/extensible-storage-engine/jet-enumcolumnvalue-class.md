---
description: 'Weitere Informationen finden Sie unter: JET_ENUMCOLUMNVALUE-Klasse'
title: JET_ENUMCOLUMNVALUE-Klasse
TOCTitle: JET_ENUMCOLUMNVALUE class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103622
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2066e6b4b3039ba150f17630afaef967c215823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346680"
---
# <a name="jet_enumcolumnvalue-class"></a><span data-ttu-id="0b68a-103">JET_ENUMCOLUMNVALUE-Klasse</span><span class="sxs-lookup"><span data-stu-id="0b68a-103">JET_ENUMCOLUMNVALUE class</span></span>

<span data-ttu-id="0b68a-104">Listet die Spaltenwerte eines Datensatzes mithilfe der jetenumeratecolumns-Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="0b68a-104">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="0b68a-105">[Jetenumeratecolumns (JET_SESID, JET_TABLEID, Int32, \[ \] , Int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, enumeratecolumnsgrbit)](./api.jetenumeratecolumns-method.md) gibt ein Array mit JET_ENUMCOLUMNVALUE Strukturen zurück.</span><span class="sxs-lookup"><span data-stu-id="0b68a-105">[JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="0b68a-106">Das Array wird im Arbeitsspeicher zurückgegeben, der mithilfe des Rückrufs zugewiesen wurde, der für diese Funktion angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="0b68a-106">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0b68a-107">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="0b68a-107">Inheritance hierarchy</span></span>

[<span data-ttu-id="0b68a-108">System.Object</span><span class="sxs-lookup"><span data-stu-id="0b68a-108">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="0b68a-109">Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="0b68a-109">Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE</span></span>  

<span data-ttu-id="0b68a-110">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0b68a-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0b68a-111">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0b68a-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0b68a-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b68a-112">Syntax</span></span>

``` vb
'Declaration
Public Class JET_ENUMCOLUMNVALUE
'Usage
Dim instance As JET_ENUMCOLUMNVALUE
```

``` csharp
public class JET_ENUMCOLUMNVALUE
```

## <a name="thread-safety"></a><span data-ttu-id="0b68a-113">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="0b68a-113">Thread safety</span></span>

<span data-ttu-id="0b68a-114">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="0b68a-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0b68a-115">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="0b68a-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b68a-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b68a-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0b68a-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="0b68a-117">Reference</span></span>

[<span data-ttu-id="0b68a-118">Mitglieder JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="0b68a-118">JET_ENUMCOLUMNVALUE members</span></span>](./jet-enumcolumnvalue-members.md)

[<span data-ttu-id="0b68a-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="0b68a-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
