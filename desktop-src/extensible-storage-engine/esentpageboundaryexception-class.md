---
description: 'Weitere Informationen finden Sie unter: esentpageboundaryexception-Klasse'
title: Esentpageboundaryexception-Klasse
TOCTitle: EsentPageBoundaryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPageBoundaryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpageboundaryexception(v=EXCHG.10)
ms:contentKeyID: 55102457
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPageBoundaryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPageBoundaryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6521c820d23577f8b86d416856a644b2fe24f2c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352375"
---
# <a name="esentpageboundaryexception-class"></a><span data-ttu-id="dfdaf-103">Esentpageboundaryexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="dfdaf-103">EsentPageBoundaryException class</span></span>

<span data-ttu-id="dfdaf-104">Basisklasse für JET_err. Pageborder-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="dfdaf-104">Base class for JET_err.PageBoundary exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="dfdaf-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="dfdaf-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="dfdaf-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="dfdaf-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="dfdaf-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="dfdaf-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="dfdaf-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="dfdaf-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="dfdaf-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="dfdaf-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="dfdaf-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="dfdaf-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="dfdaf-111">Microsoft. ISAM. ESENT. Interop. esentobsoleteexception</span><span class="sxs-lookup"><span data-stu-id="dfdaf-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="dfdaf-112">Microsoft. ISAM. ESENT. Interop. esentpageboundaryexception</span><span class="sxs-lookup"><span data-stu-id="dfdaf-112">Microsoft.Isam.Esent.Interop.EsentPageBoundaryException</span></span>  

<span data-ttu-id="dfdaf-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dfdaf-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dfdaf-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dfdaf-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dfdaf-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfdaf-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPageBoundaryException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentPageBoundaryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPageBoundaryException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="dfdaf-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="dfdaf-116">Thread safety</span></span>

<span data-ttu-id="dfdaf-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="dfdaf-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="dfdaf-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="dfdaf-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="dfdaf-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfdaf-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dfdaf-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="dfdaf-120">Reference</span></span>

[<span data-ttu-id="dfdaf-121">Esentpageboundaryexception-Member</span><span class="sxs-lookup"><span data-stu-id="dfdaf-121">EsentPageBoundaryException members</span></span>](./esentpageboundaryexception-members.md)

[<span data-ttu-id="dfdaf-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="dfdaf-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
