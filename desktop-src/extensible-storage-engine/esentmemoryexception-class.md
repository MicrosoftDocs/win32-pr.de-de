---
description: 'Weitere Informationen finden Sie unter: esentmemoryexception-Klasse'
title: EsentMemoryException-Klasse
TOCTitle: EsentMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a7090fdedee2969e5dd3658b7068fd8739e9365
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103869375"
---
# <a name="esentmemoryexception-class"></a><span data-ttu-id="68581-103">EsentMemoryException-Klasse</span><span class="sxs-lookup"><span data-stu-id="68581-103">EsentMemoryException class</span></span>

<span data-ttu-id="68581-104">Basisklasse für Speicher Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="68581-104">Base class for Memory exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="68581-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="68581-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="68581-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="68581-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="68581-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="68581-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="68581-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="68581-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="68581-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="68581-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="68581-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="68581-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="68581-111">Microsoft. ISAM. ESENT. Interop. esentresourceexception</span><span class="sxs-lookup"><span data-stu-id="68581-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="68581-112">Microsoft. ISAM. ESENT. Interop. esentmemoryexception</span><span class="sxs-lookup"><span data-stu-id="68581-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>  
              

<span data-ttu-id="68581-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="68581-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="68581-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="68581-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="68581-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="68581-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentMemoryException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentMemoryException
```

``` csharp
[SerializableAttribute]
public abstract class EsentMemoryException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="68581-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="68581-116">Thread safety</span></span>

<span data-ttu-id="68581-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="68581-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="68581-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="68581-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="68581-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68581-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="68581-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="68581-120">Reference</span></span>

[<span data-ttu-id="68581-121">Esentmemoryexception-Member</span><span class="sxs-lookup"><span data-stu-id="68581-121">EsentMemoryException members</span></span>](./esentmemoryexception-members.md)

[<span data-ttu-id="68581-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="68581-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="68581-123">Abgeleitete Typen</span><span class="sxs-lookup"><span data-stu-id="68581-123">Derived types</span></span>

[<span data-ttu-id="68581-124">System.Object</span><span class="sxs-lookup"><span data-stu-id="68581-124">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="68581-125">System.Exception</span><span class="sxs-lookup"><span data-stu-id="68581-125">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="68581-126">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="68581-126">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="68581-127">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="68581-127">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="68581-128">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="68581-128">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="68581-129">Microsoft. ISAM. ESENT. Interop. esentresourceexception</span><span class="sxs-lookup"><span data-stu-id="68581-129">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="68581-130">Microsoft. ISAM. ESENT. Interop. esentmemoryexception</span><span class="sxs-lookup"><span data-stu-id="68581-130">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>  
              [<span data-ttu-id="68581-131">Microsoft. ISAM. ESENT. Interop. esentouesf buffersexception</span><span class="sxs-lookup"><span data-stu-id="68581-131">Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException</span></span>](./esentoutofbuffersexception-class.md)  
              [<span data-ttu-id="68581-132">Microsoft. ISAM. ESENT. Interop. esentouyscurrsorsexception</span><span class="sxs-lookup"><span data-stu-id="68581-132">Microsoft.Isam.Esent.Interop.EsentOutOfCursorsException</span></span>](./esentoutofcursorsexception-class.md)  
              [<span data-ttu-id="68581-133">Microsoft. ISAM. ESENT. Interop. esentouesffilelenker sexception</span><span class="sxs-lookup"><span data-stu-id="68581-133">Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException</span></span>](./esentoutoffilehandlesexception-class.md)  
              [<span data-ttu-id="68581-134">Microsoft. ISAM. ESENT. Interop. esentouesf memoryexception</span><span class="sxs-lookup"><span data-stu-id="68581-134">Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException</span></span>](./esentoutofmemoryexception-class.md)  
              [<span data-ttu-id="68581-135">Microsoft. ISAM. ESENT. Interop. esentouyfsessionsexception</span><span class="sxs-lookup"><span data-stu-id="68581-135">Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException</span></span>](./esentoutofsessionsexception-class.md)  
              [<span data-ttu-id="68581-136">Microsoft. ISAM. ESENT. Interop. esentouesfthreadsexception</span><span class="sxs-lookup"><span data-stu-id="68581-136">Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException</span></span>](./esentoutofthreadsexception-class.md)  
              [<span data-ttu-id="68581-137">Microsoft. ISAM. ESENT. Interop. esentesomanymempoolentriesexception</span><span class="sxs-lookup"><span data-stu-id="68581-137">Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException</span></span>](./esenttoomanymempoolentriesexception-class.md)  
              [<span data-ttu-id="68581-138">Microsoft. ISAM. ESENT. Interop. esentesomanyopenindexesexception</span><span class="sxs-lookup"><span data-stu-id="68581-138">Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException</span></span>](./esenttoomanyopenindexesexception-class.md)  
              [<span data-ttu-id="68581-139">Microsoft. ISAM. ESENT. Interop. esentesomanysortsexception</span><span class="sxs-lookup"><span data-stu-id="68581-139">Microsoft.Isam.Esent.Interop.EsentTooManySortsException</span></span>](./esenttoomanysortsexception-class.md)