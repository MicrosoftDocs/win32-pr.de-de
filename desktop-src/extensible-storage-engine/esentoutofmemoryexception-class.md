---
description: 'Weitere Informationen finden Sie unter: esentouesf memoryexception-Klasse'
title: Esentoudef memoryexception-Klasse
TOCTitle: EsentOutOfMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d766bdfa115db7e43cbee6242e41a5c7cdb281b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214798"
---
# <a name="esentoutofmemoryexception-class"></a><span data-ttu-id="72087-103">Esentoudef memoryexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="72087-103">EsentOutOfMemoryException class</span></span>

<span data-ttu-id="72087-104">Basisklasse für JET_err. Outo-Memory-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="72087-104">Base class for JET_err.OutOfMemory exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="72087-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="72087-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="72087-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="72087-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="72087-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="72087-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="72087-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="72087-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="72087-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="72087-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="72087-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="72087-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="72087-111">Microsoft. ISAM. ESENT. Interop. esentresourceexception</span><span class="sxs-lookup"><span data-stu-id="72087-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="72087-112">Microsoft. ISAM. ESENT. Interop. esentmemoryexception</span><span class="sxs-lookup"><span data-stu-id="72087-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="72087-113">Microsoft. ISAM. ESENT. Interop. esentouesf memoryexception</span><span class="sxs-lookup"><span data-stu-id="72087-113">Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException</span></span>  

<span data-ttu-id="72087-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="72087-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="72087-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="72087-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="72087-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="72087-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfMemoryException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfMemoryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfMemoryException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="72087-117">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="72087-117">Thread safety</span></span>

<span data-ttu-id="72087-118">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="72087-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="72087-119">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="72087-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="72087-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72087-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="72087-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="72087-121">Reference</span></span>

[<span data-ttu-id="72087-122">Esentouto fmemoryexception-Member</span><span class="sxs-lookup"><span data-stu-id="72087-122">EsentOutOfMemoryException members</span></span>](./esentoutofmemoryexception-members.md)

[<span data-ttu-id="72087-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="72087-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
