---
description: 'Weitere Informationen finden Sie unter: esentinvalidobjectexception-Klasse'
title: Esentinvalidobjectexception-Klasse
TOCTitle: EsentInvalidObjectException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidObjectException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidobjectexception(v=EXCHG.10)
ms:contentKeyID: 55107288
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidObjectException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidObjectException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86cf06f1f291ca6f2637e652a61b27319b4fa7c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366290"
---
# <a name="esentinvalidobjectexception-class"></a><span data-ttu-id="142c7-103">Esentinvalidobjectexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="142c7-103">EsentInvalidObjectException class</span></span>

<span data-ttu-id="142c7-104">Basisklasse für JET_err. Invalidobject-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="142c7-104">Base class for JET_err.InvalidObject exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="142c7-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="142c7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="142c7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="142c7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="142c7-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="142c7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="142c7-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="142c7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="142c7-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="142c7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="142c7-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="142c7-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="142c7-111">Microsoft. ISAM. ESENT. Interop. esentobsoleteexception</span><span class="sxs-lookup"><span data-stu-id="142c7-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="142c7-112">Microsoft. ISAM. ESENT. Interop. esentinvalidobjectexception</span><span class="sxs-lookup"><span data-stu-id="142c7-112">Microsoft.Isam.Esent.Interop.EsentInvalidObjectException</span></span>  

<span data-ttu-id="142c7-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="142c7-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="142c7-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="142c7-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="142c7-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="142c7-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidObjectException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentInvalidObjectException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidObjectException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="142c7-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="142c7-116">Thread safety</span></span>

<span data-ttu-id="142c7-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="142c7-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="142c7-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="142c7-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="142c7-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="142c7-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="142c7-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="142c7-120">Reference</span></span>

[<span data-ttu-id="142c7-121">Esentinvalidobjectexception-Member</span><span class="sxs-lookup"><span data-stu-id="142c7-121">EsentInvalidObjectException members</span></span>](./esentinvalidobjectexception-members.md)

[<span data-ttu-id="142c7-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="142c7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
