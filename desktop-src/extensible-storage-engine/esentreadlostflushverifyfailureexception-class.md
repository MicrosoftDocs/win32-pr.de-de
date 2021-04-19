---
description: 'Weitere Informationen finden Sie unter: esentlelostflushverifyfailureexception-Klasse'
title: Esentlelostflushverifyfailureexception-Klasse
TOCTitle: EsentReadLostFlushVerifyFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentreadlostflushverifyfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102493
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: deddb54a6d22783270765e11a62070cd559ed2b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349111"
---
# <a name="esentreadlostflushverifyfailureexception-class"></a><span data-ttu-id="ccfa3-103">Esentlelostflushverifyfailureexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="ccfa3-103">EsentReadLostFlushVerifyFailureException class</span></span>

<span data-ttu-id="ccfa3-104">Basisklasse für JET_err. "Read lostflushverifyfailure"-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-104">Base class for JET_err.ReadLostFlushVerifyFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ccfa3-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="ccfa3-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ccfa3-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ccfa3-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ccfa3-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ccfa3-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ccfa3-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="ccfa3-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ccfa3-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="ccfa3-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ccfa3-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="ccfa3-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="ccfa3-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="ccfa3-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="ccfa3-112">Microsoft. ISAM. ESENT. Interop. esentlelostflushverifyfailureexception</span><span class="sxs-lookup"><span data-stu-id="ccfa3-112">Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException</span></span>  

<span data-ttu-id="ccfa3-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ccfa3-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ccfa3-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ccfa3-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ccfa3-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccfa3-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentReadLostFlushVerifyFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentReadLostFlushVerifyFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentReadLostFlushVerifyFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="ccfa3-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="ccfa3-116">Thread safety</span></span>

<span data-ttu-id="ccfa3-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ccfa3-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ccfa3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccfa3-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ccfa3-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="ccfa3-120">Reference</span></span>

[<span data-ttu-id="ccfa3-121">Esentleleslostflushverifyfailureexception-Member</span><span class="sxs-lookup"><span data-stu-id="ccfa3-121">EsentReadLostFlushVerifyFailureException members</span></span>](./esentreadlostflushverifyfailureexception-members.md)

[<span data-ttu-id="ccfa3-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ccfa3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
