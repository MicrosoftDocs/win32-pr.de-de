---
description: 'Weitere Informationen finden Sie unter: esentmultivaluedduplicateexception-Klasse'
title: Esentmultivaluedduplicateexception-Klasse
TOCTitle: EsentMultiValuedDuplicateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmultivaluedduplicateexception(v=EXCHG.10)
ms:contentKeyID: 55102340
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fddfac316bb8ad13ff5c42abc8041e4a18c85321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349801"
---
# <a name="esentmultivaluedduplicateexception-class"></a><span data-ttu-id="faf57-103">Esentmultivaluedduplicateexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="faf57-103">EsentMultiValuedDuplicateException class</span></span>

<span data-ttu-id="faf57-104">Basisklasse für JET_err. Multivaluedduplicate-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="faf57-104">Base class for JET_err.MultiValuedDuplicate exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="faf57-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="faf57-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="faf57-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="faf57-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="faf57-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="faf57-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="faf57-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="faf57-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="faf57-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="faf57-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="faf57-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="faf57-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="faf57-111">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="faf57-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="faf57-112">Microsoft. ISAM. ESENT. Interop. esentmultivaluedduplicateexception</span><span class="sxs-lookup"><span data-stu-id="faf57-112">Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException</span></span>  

<span data-ttu-id="faf57-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="faf57-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="faf57-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="faf57-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="faf57-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="faf57-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMultiValuedDuplicateException _
    Inherits EsentStateException
'Usage
Dim instance As EsentMultiValuedDuplicateException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMultiValuedDuplicateException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="faf57-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="faf57-116">Thread safety</span></span>

<span data-ttu-id="faf57-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="faf57-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="faf57-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="faf57-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="faf57-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faf57-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="faf57-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="faf57-120">Reference</span></span>

[<span data-ttu-id="faf57-121">Esentmultivaluedduplicateexception-Member</span><span class="sxs-lookup"><span data-stu-id="faf57-121">EsentMultiValuedDuplicateException members</span></span>](./esentmultivaluedduplicateexception-members.md)

[<span data-ttu-id="faf57-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="faf57-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
