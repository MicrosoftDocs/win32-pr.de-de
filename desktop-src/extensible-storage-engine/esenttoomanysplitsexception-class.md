---
description: 'Weitere Informationen finden Sie unter: esentesomanysplitsexception-Klasse'
title: Esentesomanysplitsexception-Klasse
TOCTitle: EsentTooManySplitsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManySplitsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanysplitsexception(v=EXCHG.10)
ms:contentKeyID: 55103177
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManySplitsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManySplitsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fea122e5a5f40dd1a435a82f68d86766dc5518ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960769"
---
# <a name="esenttoomanysplitsexception-class"></a><span data-ttu-id="49c75-103">Esentesomanysplitsexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="49c75-103">EsentTooManySplitsException class</span></span>

<span data-ttu-id="49c75-104">Basisklasse für JET_err. "-Ausnahmen"-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="49c75-104">Base class for JET_err.TooManySplits exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="49c75-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="49c75-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="49c75-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="49c75-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="49c75-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="49c75-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="49c75-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="49c75-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="49c75-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="49c75-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="49c75-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="49c75-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="49c75-111">Microsoft. ISAM. ESENT. Interop. esentobsoleteexception</span><span class="sxs-lookup"><span data-stu-id="49c75-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="49c75-112">Microsoft. ISAM. ESENT. Interop. esentesomanysplitsexception</span><span class="sxs-lookup"><span data-stu-id="49c75-112">Microsoft.Isam.Esent.Interop.EsentTooManySplitsException</span></span>  

<span data-ttu-id="49c75-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="49c75-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="49c75-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="49c75-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="49c75-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="49c75-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManySplitsException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentTooManySplitsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManySplitsException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="49c75-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="49c75-116">Thread safety</span></span>

<span data-ttu-id="49c75-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="49c75-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="49c75-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="49c75-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="49c75-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49c75-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="49c75-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="49c75-120">Reference</span></span>

[<span data-ttu-id="49c75-121">Esentesomanysplitsexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="49c75-121">EsentTooManySplitsException members</span></span>](./esenttoomanysplitsexception-members.md)

[<span data-ttu-id="49c75-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="49c75-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
