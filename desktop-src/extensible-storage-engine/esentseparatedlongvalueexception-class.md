---
description: 'Weitere Informationen finden Sie unter: esentseparatedlongvalueexception-Klasse'
title: Esentseparatedlongvalueexception-Klasse
TOCTitle: EsentSeparatedLongValueException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSeparatedLongValueException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentseparatedlongvalueexception(v=EXCHG.10)
ms:contentKeyID: 55107331
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSeparatedLongValueException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSeparatedLongValueException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d35977f8b27914799097188030f6b91afd055d08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042513"
---
# <a name="esentseparatedlongvalueexception-class"></a><span data-ttu-id="4d3c2-103">Esentseparatedlongvalueexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="4d3c2-103">EsentSeparatedLongValueException class</span></span>

<span data-ttu-id="4d3c2-104">Basisklasse für JET_err. Separatedlongvalue-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="4d3c2-104">Base class for JET_err.SeparatedLongValue exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4d3c2-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="4d3c2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4d3c2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4d3c2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4d3c2-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="4d3c2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4d3c2-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="4d3c2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4d3c2-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="4d3c2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4d3c2-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="4d3c2-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="4d3c2-111">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="4d3c2-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="4d3c2-112">Microsoft. ISAM. ESENT. Interop. esentseparatedlongvalueexception</span><span class="sxs-lookup"><span data-stu-id="4d3c2-112">Microsoft.Isam.Esent.Interop.EsentSeparatedLongValueException</span></span>  

<span data-ttu-id="4d3c2-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4d3c2-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4d3c2-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4d3c2-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4d3c2-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d3c2-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSeparatedLongValueException _
    Inherits EsentStateException
'Usage
Dim instance As EsentSeparatedLongValueException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSeparatedLongValueException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="4d3c2-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="4d3c2-116">Thread safety</span></span>

<span data-ttu-id="4d3c2-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="4d3c2-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4d3c2-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="4d3c2-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d3c2-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d3c2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4d3c2-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="4d3c2-120">Reference</span></span>

[<span data-ttu-id="4d3c2-121">Esentseparatedlongvalueexception-Member</span><span class="sxs-lookup"><span data-stu-id="4d3c2-121">EsentSeparatedLongValueException members</span></span>](./esentseparatedlongvalueexception-members.md)

[<span data-ttu-id="4d3c2-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="4d3c2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
