---
description: 'Weitere Informationen finden Sie unter: esentpartiallyattacheddbexception-Klasse'
title: Esentpartiallyattacheddbexception-Klasse
TOCTitle: EsentPartiallyAttachedDBException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPartiallyAttachedDBException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpartiallyattacheddbexception(v=EXCHG.10)
ms:contentKeyID: 55107313
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPartiallyAttachedDBException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPartiallyAttachedDBException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 96ff15d9a2becb937c88f6e0bec689e68ddc39d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358478"
---
# <a name="esentpartiallyattacheddbexception-class"></a><span data-ttu-id="776c3-103">Esentpartiallyattacheddbexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="776c3-103">EsentPartiallyAttachedDBException class</span></span>

<span data-ttu-id="776c3-104">Basisklasse für JET_err. Partiallyattacheddb-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="776c3-104">Base class for JET_err.PartiallyAttachedDB exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="776c3-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="776c3-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="776c3-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="776c3-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="776c3-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="776c3-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="776c3-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="776c3-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="776c3-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="776c3-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="776c3-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="776c3-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="776c3-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="776c3-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="776c3-112">Microsoft. ISAM. ESENT. Interop. esentpartiallyattacheddbexception</span><span class="sxs-lookup"><span data-stu-id="776c3-112">Microsoft.Isam.Esent.Interop.EsentPartiallyAttachedDBException</span></span>  

<span data-ttu-id="776c3-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="776c3-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="776c3-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="776c3-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="776c3-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="776c3-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPartiallyAttachedDBException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentPartiallyAttachedDBException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPartiallyAttachedDBException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="776c3-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="776c3-116">Thread safety</span></span>

<span data-ttu-id="776c3-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="776c3-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="776c3-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="776c3-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="776c3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="776c3-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="776c3-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="776c3-120">Reference</span></span>

[<span data-ttu-id="776c3-121">Esentpartiallyattacheddbexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="776c3-121">EsentPartiallyAttachedDBException members</span></span>](./esentpartiallyattacheddbexception-members.md)

[<span data-ttu-id="776c3-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="776c3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
