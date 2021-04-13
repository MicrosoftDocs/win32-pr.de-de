---
description: 'Weitere Informationen finden Sie unter: esentinvalidoperationexception-Klasse'
title: Esentinvalidoperationexception-Klasse
TOCTitle: EsentInvalidOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102007
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidOperationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ccf4c4fe3b980251c91d11387af02c56cc23772f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350489"
---
# <a name="esentinvalidoperationexception-class"></a><span data-ttu-id="a21c8-103">Esentinvalidoperationexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="a21c8-103">EsentInvalidOperationException class</span></span>

<span data-ttu-id="a21c8-104">Basisklasse für JET_err. InvalidOperation-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="a21c8-104">Base class for JET_err.InvalidOperation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a21c8-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="a21c8-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a21c8-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a21c8-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a21c8-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="a21c8-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a21c8-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="a21c8-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a21c8-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="a21c8-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a21c8-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="a21c8-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="a21c8-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="a21c8-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="a21c8-112">Microsoft. ISAM. ESENT. Interop. esentinvalidoperationexception</span><span class="sxs-lookup"><span data-stu-id="a21c8-112">Microsoft.Isam.Esent.Interop.EsentInvalidOperationException</span></span>  

<span data-ttu-id="a21c8-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a21c8-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a21c8-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a21c8-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a21c8-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="a21c8-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidOperationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidOperationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidOperationException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="a21c8-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="a21c8-116">Thread safety</span></span>

<span data-ttu-id="a21c8-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="a21c8-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a21c8-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="a21c8-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a21c8-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a21c8-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a21c8-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="a21c8-120">Reference</span></span>

[<span data-ttu-id="a21c8-121">Esentinvalidoperationexception-Member</span><span class="sxs-lookup"><span data-stu-id="a21c8-121">EsentInvalidOperationException members</span></span>](./esentinvalidoperationexception-members.md)

[<span data-ttu-id="a21c8-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="a21c8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
