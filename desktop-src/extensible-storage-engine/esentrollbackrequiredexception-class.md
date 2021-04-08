---
description: 'Weitere Informationen finden Sie unter: esentrollbackrequirements dexception-Klasse'
title: Esentrollbackrequirements dexception-Klasse
TOCTitle: EsentRollbackRequiredException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrollbackrequiredexception(v=EXCHG.10)
ms:contentKeyID: 55107325
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 12baa9d69400cfd84c54184132c45aba4095b427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754521"
---
# <a name="esentrollbackrequiredexception-class"></a><span data-ttu-id="1277b-103">Esentrollbackrequirements dexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="1277b-103">EsentRollbackRequiredException class</span></span>

<span data-ttu-id="1277b-104">Basisklasse für JET_err. Rollbackrequired-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="1277b-104">Base class for JET_err.RollbackRequired exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1277b-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="1277b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1277b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1277b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1277b-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="1277b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1277b-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="1277b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1277b-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="1277b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1277b-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="1277b-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="1277b-111">Microsoft. ISAM. ESENT. Interop. esentobsoleteexception</span><span class="sxs-lookup"><span data-stu-id="1277b-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="1277b-112">Microsoft. ISAM. ESENT. Interop. esentrollbackrequirements dexception</span><span class="sxs-lookup"><span data-stu-id="1277b-112">Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException</span></span>  

<span data-ttu-id="1277b-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1277b-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1277b-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1277b-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1277b-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="1277b-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRollbackRequiredException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentRollbackRequiredException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRollbackRequiredException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="1277b-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="1277b-116">Thread safety</span></span>

<span data-ttu-id="1277b-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="1277b-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1277b-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="1277b-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1277b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1277b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1277b-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="1277b-120">Reference</span></span>

[<span data-ttu-id="1277b-121">Esentrollbackrequirements dexception-Member</span><span class="sxs-lookup"><span data-stu-id="1277b-121">EsentRollbackRequiredException members</span></span>](./esentrollbackrequiredexception-members.md)

[<span data-ttu-id="1277b-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="1277b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
