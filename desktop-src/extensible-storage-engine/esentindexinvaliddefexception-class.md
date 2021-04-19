---
description: 'Weitere Informationen finden Sie unter: esentindexinvaliddefexception-Klasse'
title: Esentindexinvaliddefexception-Klasse
TOCTitle: EsentIndexInvalidDefException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIndexInvalidDefException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentindexinvaliddefexception(v=EXCHG.10)
ms:contentKeyID: 55101833
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIndexInvalidDefException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIndexInvalidDefException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6246843f5f8284d8b39e42e1c4bcbef83f31962b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369878"
---
# <a name="esentindexinvaliddefexception-class"></a><span data-ttu-id="aac2d-103">Esentindexinvaliddefexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="aac2d-103">EsentIndexInvalidDefException class</span></span>

<span data-ttu-id="aac2d-104">Basisklasse für JET_err. Indexinvaliddef-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="aac2d-104">Base class for JET_err.IndexInvalidDef exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="aac2d-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="aac2d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="aac2d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="aac2d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="aac2d-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="aac2d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="aac2d-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="aac2d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="aac2d-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="aac2d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="aac2d-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="aac2d-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="aac2d-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="aac2d-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="aac2d-112">Microsoft. ISAM. ESENT. Interop. esentindexinvaliddefexception</span><span class="sxs-lookup"><span data-stu-id="aac2d-112">Microsoft.Isam.Esent.Interop.EsentIndexInvalidDefException</span></span>  

<span data-ttu-id="aac2d-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aac2d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aac2d-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aac2d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aac2d-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="aac2d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentIndexInvalidDefException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentIndexInvalidDefException
```

``` csharp
[SerializableAttribute]
public sealed class EsentIndexInvalidDefException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="aac2d-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="aac2d-116">Thread safety</span></span>

<span data-ttu-id="aac2d-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="aac2d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="aac2d-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="aac2d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="aac2d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aac2d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aac2d-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="aac2d-120">Reference</span></span>

[<span data-ttu-id="aac2d-121">Esentindexinvaliddefexception-Member</span><span class="sxs-lookup"><span data-stu-id="aac2d-121">EsentIndexInvalidDefException members</span></span>](./esentindexinvaliddefexception-members.md)

[<span data-ttu-id="aac2d-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="aac2d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
