---
description: 'Weitere Informationen finden Sie unter: esentapiexception-Klasse'
title: Esentapiexception-Klasse
TOCTitle: EsentApiException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentApiException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101032
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentApiException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b01747d2ecb197ce99617b8c9206d4fada8c2a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218269"
---
# <a name="esentapiexception-class"></a><span data-ttu-id="7bb6a-103">Esentapiexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="7bb6a-103">EsentApiException class</span></span>

<span data-ttu-id="7bb6a-104">Basisklasse für API-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="7bb6a-104">Base class for API exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7bb6a-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="7bb6a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7bb6a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7bb6a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7bb6a-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="7bb6a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7bb6a-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="7bb6a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7bb6a-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="7bb6a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="7bb6a-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="7bb6a-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>  
          [<span data-ttu-id="7bb6a-111">Microsoft. ISAM. ESENT. Interop. esentobsoleteexception</span><span class="sxs-lookup"><span data-stu-id="7bb6a-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
          [<span data-ttu-id="7bb6a-112">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="7bb6a-112">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
          [<span data-ttu-id="7bb6a-113">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="7bb6a-113">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  

<span data-ttu-id="7bb6a-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7bb6a-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7bb6a-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7bb6a-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7bb6a-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bb6a-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentApiException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentApiException
```

``` csharp
[SerializableAttribute]
public abstract class EsentApiException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="7bb6a-117">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="7bb6a-117">Thread safety</span></span>

<span data-ttu-id="7bb6a-118">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="7bb6a-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7bb6a-119">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="7bb6a-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7bb6a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bb6a-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7bb6a-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="7bb6a-121">Reference</span></span>

[<span data-ttu-id="7bb6a-122">Esentapiexception-Member</span><span class="sxs-lookup"><span data-stu-id="7bb6a-122">EsentApiException members</span></span>](./esentapiexception-members.md)

[<span data-ttu-id="7bb6a-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="7bb6a-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
