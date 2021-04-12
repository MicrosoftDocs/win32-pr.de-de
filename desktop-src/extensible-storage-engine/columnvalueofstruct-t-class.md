---
description: 'Weitere Informationen finden Sie unter: columnvalueof struct- <T> Klasse'
title: ColumnValueOfStruct(T)-Klasse
TOCTitle: ColumnValueOfStruct(T) class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334171(v=EXCHG.10)
ms:contentKeyID: 55100962
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82083adcaaf0d9f5b4f2a720da83e95cd4b39401
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351089"
---
# <a name="columnvalueofstructt-class"></a><span data-ttu-id="7b023-103">Columnvalueosstruct- \<T\> Klasse</span><span class="sxs-lookup"><span data-stu-id="7b023-103">ColumnValueOfStruct\<T\> class</span></span>

<span data-ttu-id="7b023-104">Legen Sie eine Spalte eines Struktur Typs (z. b. Int32/GUID) fest.</span><span class="sxs-lookup"><span data-stu-id="7b023-104">Set a column of a struct type (e.g. Int32/Guid).</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7b023-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="7b023-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7b023-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7b023-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7b023-107">Microsoft. ISAM. ESENT. Interop. ColumnValue</span><span class="sxs-lookup"><span data-stu-id="7b023-107">Microsoft.Isam.Esent.Interop.ColumnValue</span></span>](./columnvalue-class.md)  
    <span data-ttu-id="7b023-108">Microsoft. ISAM. ESENT. Interop. columnvalueofistruct\<T\></span><span class="sxs-lookup"><span data-stu-id="7b023-108">Microsoft.Isam.Esent.Interop.ColumnValueOfStruct\<T\></span></span>  
      

<span data-ttu-id="7b023-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7b023-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7b023-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7b023-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7b023-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b023-111">Syntax</span></span>

``` vb
'Declaration
Public MustInherit Class ColumnValueOfStruct(Of T As {Structure, New, IEquatable(Of T)}) _
    Inherits ColumnValue
'Usage
Dim instance As ColumnValueOfStruct(Of T)
```

``` csharp
public abstract class ColumnValueOfStruct<T> : ColumnValue
where T : struct, new(), IEquatable<T>
```

#### <a name="type-parameters"></a><span data-ttu-id="7b023-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="7b023-112">Type parameters</span></span>

  - <span data-ttu-id="7b023-113">T</span><span class="sxs-lookup"><span data-stu-id="7b023-113">T</span></span>  
    <span data-ttu-id="7b023-114">Der festzulegende Typ.</span><span class="sxs-lookup"><span data-stu-id="7b023-114">Type to set.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="7b023-115">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="7b023-115">Thread safety</span></span>

<span data-ttu-id="7b023-116">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="7b023-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7b023-117">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="7b023-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b023-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b023-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7b023-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="7b023-119">Reference</span></span>

[<span data-ttu-id="7b023-120">Columnvalueofstruct \<T\> -Member</span><span class="sxs-lookup"><span data-stu-id="7b023-120">ColumnValueOfStruct\<T\> members</span></span>](./columnvalueofstruct-t-members.md)

[<span data-ttu-id="7b023-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="7b023-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="7b023-122">Abgeleitete Typen</span><span class="sxs-lookup"><span data-stu-id="7b023-122">Derived types</span></span>

[<span data-ttu-id="7b023-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="7b023-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7b023-124">Microsoft. ISAM. ESENT. Interop. ColumnValue</span><span class="sxs-lookup"><span data-stu-id="7b023-124">Microsoft.Isam.Esent.Interop.ColumnValue</span></span>](./columnvalue-class.md)  
    <span data-ttu-id="7b023-125">Microsoft. ISAM. ESENT. Interop. columnvalueofistruct\<T\></span><span class="sxs-lookup"><span data-stu-id="7b023-125">Microsoft.Isam.Esent.Interop.ColumnValueOfStruct\<T\></span></span>  
      [<span data-ttu-id="7b023-126">Microsoft. ISAM. ESENT. Interop. boolcolumnvalue</span><span class="sxs-lookup"><span data-stu-id="7b023-126">Microsoft.Isam.Esent.Interop.BoolColumnValue</span></span>](./boolcolumnvalue-class.md)  
      [<span data-ttu-id="7b023-127">Microsoft. ISAM. ESENT. Interop. bytecolumnvalue</span><span class="sxs-lookup"><span data-stu-id="7b023-127">Microsoft.Isam.Esent.Interop.ByteColumnValue</span></span>](./bytecolumnvalue-class.md)  
      [<span data-ttu-id="7b023-128">Microsoft. ISAM. ESENT. Interop. datetimecolumnvalue</span><span class="sxs-lookup"><span data-stu-id="7b023-128">Microsoft.Isam.Esent.Interop.DateTimeColumnValue</span></span>](./datetimecolumnvalue-class.md)  
      [<span data-ttu-id="7b023-129">Microsoft. ISAM. ESENT. Interop. doublecolumnvalue</span><span class="sxs-lookup"><span data-stu-id="7b023-129">Microsoft.Isam.Esent.Interop.DoubleColumnValue</span></span>](./doublecolumnvalue-class.md)  
      [<span data-ttu-id="7b023-130">Microsoft. ISAM. ESENT. Interop. floatcolumnvalue</span><span class="sxs-lookup"><span data-stu-id="7b023-130">Microsoft.Isam.Esent.Interop.FloatColumnValue</span></span>](./floatcolumnvalue-class.md)  
      [<span data-ttu-id="7b023-131">Microsoft. ISAM. ESENT. Interop. guidcolumnvalue</span><span class="sxs-lookup"><span data-stu-id="7b023-131">Microsoft.Isam.Esent.Interop.GuidColumnValue</span></span>](./guidcolumnvalue-class.md)  
      [<span data-ttu-id="7b023-132">Microsoft. ISAM. ESENT. Interop. Int16ColumnValue</span><span class="sxs-lookup"><span data-stu-id="7b023-132">Microsoft.Isam.Esent.Interop.Int16ColumnValue</span></span>](./int16columnvalue-class.md)  
      [<span data-ttu-id="7b023-133">Microsoft. ISAM. ESENT. Interop. Int32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="7b023-133">Microsoft.Isam.Esent.Interop.Int32ColumnValue</span></span>](./int32columnvalue-class.md)  
      [<span data-ttu-id="7b023-134">Microsoft. ISAM. ESENT. Interop. Int64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="7b023-134">Microsoft.Isam.Esent.Interop.Int64ColumnValue</span></span>](./int64columnvalue-class.md)  
      [<span data-ttu-id="7b023-135">Microsoft. ISAM. ESENT. Interop. UInt16ColumnValue</span><span class="sxs-lookup"><span data-stu-id="7b023-135">Microsoft.Isam.Esent.Interop.UInt16ColumnValue</span></span>](./uint16columnvalue-class.md)  
      [<span data-ttu-id="7b023-136">Microsoft. ISAM. ESENT. Interop. UInt32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="7b023-136">Microsoft.Isam.Esent.Interop.UInt32ColumnValue</span></span>](./uint32columnvalue-class.md)  
      [<span data-ttu-id="7b023-137">Microsoft. ISAM. ESENT. Interop. UInt64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="7b023-137">Microsoft.Isam.Esent.Interop.UInt64ColumnValue</span></span>](./uint64columnvalue-class.md)