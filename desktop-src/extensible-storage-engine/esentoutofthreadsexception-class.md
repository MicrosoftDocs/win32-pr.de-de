---
description: 'Weitere Informationen finden Sie unter: esentouto fthreadsexception-Klasse'
title: Esentouto fthreadsexception-Klasse
TOCTitle: EsentOutOfThreadsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofthreadsexception(v=EXCHG.10)
ms:contentKeyID: 55102450
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 05a1427383a12c286ba37eee6f4ddfcd0b655350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960884"
---
# <a name="esentoutofthreadsexception-class"></a><span data-ttu-id="ff0d6-103">Esentouto fthreadsexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="ff0d6-103">EsentOutOfThreadsException class</span></span>

<span data-ttu-id="ff0d6-104">Basisklasse für JET_err. Outo-Threads-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="ff0d6-104">Base class for JET_err.OutOfThreads exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ff0d6-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="ff0d6-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ff0d6-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ff0d6-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ff0d6-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ff0d6-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ff0d6-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="ff0d6-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ff0d6-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="ff0d6-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ff0d6-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="ff0d6-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="ff0d6-111">Microsoft. ISAM. ESENT. Interop. esentresourceexception</span><span class="sxs-lookup"><span data-stu-id="ff0d6-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="ff0d6-112">Microsoft. ISAM. ESENT. Interop. esentmemoryexception</span><span class="sxs-lookup"><span data-stu-id="ff0d6-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="ff0d6-113">Microsoft. ISAM. ESENT. Interop. esentouesfthreadsexception</span><span class="sxs-lookup"><span data-stu-id="ff0d6-113">Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException</span></span>  

<span data-ttu-id="ff0d6-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ff0d6-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ff0d6-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ff0d6-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ff0d6-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff0d6-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfThreadsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfThreadsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfThreadsException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="ff0d6-117">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="ff0d6-117">Thread safety</span></span>

<span data-ttu-id="ff0d6-118">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="ff0d6-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ff0d6-119">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="ff0d6-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff0d6-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff0d6-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ff0d6-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="ff0d6-121">Reference</span></span>

[<span data-ttu-id="ff0d6-122">Esentouto fthreadsexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="ff0d6-122">EsentOutOfThreadsException members</span></span>](./esentoutofthreadsexception-members.md)

[<span data-ttu-id="ff0d6-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ff0d6-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
