---
description: 'Weitere Informationen finden Sie unter: esentschreiteconflictexception-Klasse'
title: Esentschreiteconflictexception-Klasse
TOCTitle: EsentWriteConflictException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentWriteConflictException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentwriteconflictexception(v=EXCHG.10)
ms:contentKeyID: 55103199
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentWriteConflictException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentWriteConflictException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fffcb0b2bb07e12dc4dd9f86de5c22b13aca66b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351603"
---
# <a name="esentwriteconflictexception-class"></a><span data-ttu-id="b17a4-103">Esentschreiteconflictexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="b17a4-103">EsentWriteConflictException class</span></span>

<span data-ttu-id="b17a4-104">Basisklasse für JET_err. "Write Conflict"-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="b17a4-104">Base class for JET_err.WriteConflict exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b17a4-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="b17a4-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b17a4-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b17a4-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b17a4-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b17a4-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b17a4-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="b17a4-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b17a4-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="b17a4-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b17a4-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="b17a4-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b17a4-111">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="b17a4-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="b17a4-112">Microsoft. ISAM. ESENT. Interop. esentschreiteconflictexception</span><span class="sxs-lookup"><span data-stu-id="b17a4-112">Microsoft.Isam.Esent.Interop.EsentWriteConflictException</span></span>  

<span data-ttu-id="b17a4-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b17a4-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b17a4-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b17a4-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b17a4-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="b17a4-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentWriteConflictException _
    Inherits EsentStateException
'Usage
Dim instance As EsentWriteConflictException
```

``` csharp
[SerializableAttribute]
public sealed class EsentWriteConflictException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="b17a4-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="b17a4-116">Thread safety</span></span>

<span data-ttu-id="b17a4-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="b17a4-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b17a4-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="b17a4-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b17a4-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b17a4-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b17a4-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="b17a4-120">Reference</span></span>

[<span data-ttu-id="b17a4-121">Esentschreiteconflictexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="b17a4-121">EsentWriteConflictException members</span></span>](./esentwriteconflictexception-members.md)

[<span data-ttu-id="b17a4-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="b17a4-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
