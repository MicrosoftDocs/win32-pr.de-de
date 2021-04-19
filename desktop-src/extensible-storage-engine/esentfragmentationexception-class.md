---
description: 'Weitere Informationen finden Sie unter: esentfragmentationexception-Klasse'
title: EsentFragmentationException-Klasse
TOCTitle: EsentFragmentationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFragmentationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 081198a696be9982e1fd8a7e4f1468e6d63d1c97
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106355091"
---
# <a name="esentfragmentationexception-class"></a><span data-ttu-id="47abc-103">EsentFragmentationException-Klasse</span><span class="sxs-lookup"><span data-stu-id="47abc-103">EsentFragmentationException class</span></span>

<span data-ttu-id="47abc-104">Basisklasse für Fragmentierungs Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="47abc-104">Base class for Fragmentation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="47abc-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="47abc-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="47abc-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="47abc-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="47abc-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="47abc-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="47abc-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="47abc-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="47abc-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="47abc-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="47abc-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="47abc-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="47abc-111">Microsoft. ISAM. ESENT. Interop. esentfragmentationexception</span><span class="sxs-lookup"><span data-stu-id="47abc-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>  
            

<span data-ttu-id="47abc-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="47abc-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="47abc-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="47abc-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="47abc-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="47abc-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFragmentationException _
    Inherits EsentDataException
'Usage
Dim instance As EsentFragmentationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFragmentationException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="47abc-115">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="47abc-115">Thread safety</span></span>

<span data-ttu-id="47abc-116">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="47abc-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="47abc-117">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="47abc-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="47abc-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47abc-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="47abc-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="47abc-119">Reference</span></span>

[<span data-ttu-id="47abc-120">Esentfragmentationexception-Member</span><span class="sxs-lookup"><span data-stu-id="47abc-120">EsentFragmentationException members</span></span>](./esentfragmentationexception-members.md)

[<span data-ttu-id="47abc-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="47abc-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="47abc-122">Abgeleitete Typen</span><span class="sxs-lookup"><span data-stu-id="47abc-122">Derived types</span></span>

[<span data-ttu-id="47abc-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="47abc-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="47abc-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="47abc-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="47abc-125">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="47abc-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="47abc-126">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="47abc-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="47abc-127">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="47abc-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="47abc-128">Microsoft. ISAM. ESENT. Interop. esentfragmentationexception</span><span class="sxs-lookup"><span data-stu-id="47abc-128">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>  
            [<span data-ttu-id="47abc-129">Microsoft. ISAM. ESENT. Interop. esentlogsector sizemismatchexception</span><span class="sxs-lookup"><span data-stu-id="47abc-129">Microsoft.Isam.Esent.Interop.EsentLogSectorSizeMismatchException</span></span>](./esentlogsectorsizemismatchexception-class.md)  
            [<span data-ttu-id="47abc-130">Microsoft. ISAM. ESENT. Interop. EsentLogSequenceEndDatabasesConsistentException</span><span class="sxs-lookup"><span data-stu-id="47abc-130">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndDatabasesConsistentException</span></span>](./esentlogsequenceenddatabasesconsistentexception-class.md)  
            [<span data-ttu-id="47abc-131">Microsoft. ISAM. ESENT. Interop. esentlogsequenceendexception</span><span class="sxs-lookup"><span data-stu-id="47abc-131">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException</span></span>](./esentlogsequenceendexception-class.md)  
            [<span data-ttu-id="47abc-132">Microsoft. ISAM. ESENT. Interop. esentouesf autoincrementvaluesexception</span><span class="sxs-lookup"><span data-stu-id="47abc-132">Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException</span></span>](./esentoutofautoincrementvaluesexception-class.md)  
            [<span data-ttu-id="47abc-133">Microsoft. ISAM. ESENT. Interop. esentouesf dbtimevaluesexception</span><span class="sxs-lookup"><span data-stu-id="47abc-133">Microsoft.Isam.Esent.Interop.EsentOutOfDbtimeValuesException</span></span>](./esentoutofdbtimevaluesexception-class.md)  
            [<span data-ttu-id="47abc-134">Microsoft. ISAM. ESENT. Interop. esentouesflongvalueidsexception</span><span class="sxs-lookup"><span data-stu-id="47abc-134">Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException</span></span>](./esentoutoflongvalueidsexception-class.md)  
            [<span data-ttu-id="47abc-135">Microsoft. ISAM. ESENT. Interop. esentouesfobjectidsexception</span><span class="sxs-lookup"><span data-stu-id="47abc-135">Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException</span></span>](./esentoutofobjectidsexception-class.md)  
            [<span data-ttu-id="47abc-136">Microsoft. ISAM. ESENT. Interop. esentouesf sequentialindexvaluesexception</span><span class="sxs-lookup"><span data-stu-id="47abc-136">Microsoft.Isam.Esent.Interop.EsentOutOfSequentialIndexValuesException</span></span>](./esentoutofsequentialindexvaluesexception-class.md)