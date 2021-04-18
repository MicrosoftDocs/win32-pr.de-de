---
description: 'Weitere Informationen finden Sie unter: esentsessioninuseexception-Klasse'
title: Esentsessioninuseexception-Klasse
TOCTitle: EsentSessionInUseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionInUseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessioninuseexception(v=EXCHG.10)
ms:contentKeyID: 55102709
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionInUseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionInUseException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b956d88e1a8c59f23bedc25fadcacd234841572b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348037"
---
# <a name="esentsessioninuseexception-class"></a><span data-ttu-id="3b0f8-103">Esentsessioninuseexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="3b0f8-103">EsentSessionInUseException class</span></span>

<span data-ttu-id="3b0f8-104">Basisklasse für JET_err. Sessioninuse-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="3b0f8-104">Base class for JET_err.SessionInUse exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3b0f8-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="3b0f8-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3b0f8-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3b0f8-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3b0f8-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="3b0f8-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3b0f8-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="3b0f8-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3b0f8-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="3b0f8-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3b0f8-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="3b0f8-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="3b0f8-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="3b0f8-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="3b0f8-112">Microsoft. ISAM. ESENT. Interop. esentsessioninuseexception</span><span class="sxs-lookup"><span data-stu-id="3b0f8-112">Microsoft.Isam.Esent.Interop.EsentSessionInUseException</span></span>  

<span data-ttu-id="3b0f8-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3b0f8-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3b0f8-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3b0f8-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3b0f8-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b0f8-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionInUseException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionInUseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionInUseException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="3b0f8-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="3b0f8-116">Thread safety</span></span>

<span data-ttu-id="3b0f8-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="3b0f8-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3b0f8-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="3b0f8-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b0f8-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b0f8-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3b0f8-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="3b0f8-120">Reference</span></span>

[<span data-ttu-id="3b0f8-121">Esentsessioninuseexception-Member</span><span class="sxs-lookup"><span data-stu-id="3b0f8-121">EsentSessionInUseException members</span></span>](./esentsessioninuseexception-members.md)

[<span data-ttu-id="3b0f8-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="3b0f8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
