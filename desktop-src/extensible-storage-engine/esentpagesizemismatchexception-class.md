---
description: 'Weitere Informationen finden Sie unter: esentpagesizemismatchexception-Klasse'
title: Esentpagesizemismatchexception-Klasse
TOCTitle: EsentPageSizeMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpagesizemismatchexception(v=EXCHG.10)
ms:contentKeyID: 55102466
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0573603fae445e1e5ae9d9768c3a0ffcf38f283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362558"
---
# <a name="esentpagesizemismatchexception-class"></a><span data-ttu-id="d88c6-103">Esentpagesizemismatchexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="d88c6-103">EsentPageSizeMismatchException class</span></span>

<span data-ttu-id="d88c6-104">Basisklasse für JET_err. Pagesizemismatch-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="d88c6-104">Base class for JET_err.PageSizeMismatch exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d88c6-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="d88c6-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d88c6-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d88c6-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d88c6-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d88c6-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d88c6-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="d88c6-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d88c6-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="d88c6-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d88c6-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="d88c6-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="d88c6-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="d88c6-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="d88c6-112">Microsoft. ISAM. ESENT. Interop. esentpagesizemismatchexception</span><span class="sxs-lookup"><span data-stu-id="d88c6-112">Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException</span></span>  

<span data-ttu-id="d88c6-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d88c6-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d88c6-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d88c6-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d88c6-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="d88c6-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPageSizeMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentPageSizeMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPageSizeMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="d88c6-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="d88c6-116">Thread safety</span></span>

<span data-ttu-id="d88c6-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="d88c6-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d88c6-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="d88c6-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d88c6-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d88c6-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d88c6-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="d88c6-120">Reference</span></span>

[<span data-ttu-id="d88c6-121">Esentpagesizemismatchexception-Member</span><span class="sxs-lookup"><span data-stu-id="d88c6-121">EsentPageSizeMismatchException members</span></span>](./esentpagesizemismatchexception-members.md)

[<span data-ttu-id="d88c6-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="d88c6-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
