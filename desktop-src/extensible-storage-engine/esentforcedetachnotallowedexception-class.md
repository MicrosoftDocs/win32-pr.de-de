---
description: 'Weitere Informationen finden Sie unter: esentforcedetachnotallowedexception-Klasse'
title: Esentforcedetachnotallowedexception-Klasse
TOCTitle: EsentForceDetachNotAllowedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentForceDetachNotAllowedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentforcedetachnotallowedexception(v=EXCHG.10)
ms:contentKeyID: 55101772
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentForceDetachNotAllowedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentForceDetachNotAllowedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28a1987b82c4233302bbd3c2e8ffc928f4b55ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130904"
---
# <a name="esentforcedetachnotallowedexception-class"></a><span data-ttu-id="5e53d-103">Esentforcedetachnotallowedexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="5e53d-103">EsentForceDetachNotAllowedException class</span></span>

<span data-ttu-id="5e53d-104">Basisklasse für JET_err. Forcedetachnotallowed-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="5e53d-104">Base class for JET_err.ForceDetachNotAllowed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5e53d-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="5e53d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5e53d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5e53d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5e53d-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="5e53d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5e53d-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="5e53d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5e53d-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="5e53d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5e53d-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="5e53d-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="5e53d-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="5e53d-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="5e53d-112">Microsoft. ISAM. ESENT. Interop. esentforcedetachnotallowedexception</span><span class="sxs-lookup"><span data-stu-id="5e53d-112">Microsoft.Isam.Esent.Interop.EsentForceDetachNotAllowedException</span></span>  

<span data-ttu-id="5e53d-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5e53d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5e53d-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5e53d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5e53d-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e53d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentForceDetachNotAllowedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentForceDetachNotAllowedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentForceDetachNotAllowedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="5e53d-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="5e53d-116">Thread safety</span></span>

<span data-ttu-id="5e53d-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="5e53d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5e53d-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="5e53d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e53d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e53d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5e53d-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="5e53d-120">Reference</span></span>

[<span data-ttu-id="5e53d-121">Esentforcedetachnotallowedexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="5e53d-121">EsentForceDetachNotAllowedException members</span></span>](./esentforcedetachnotallowedexception-members.md)

[<span data-ttu-id="5e53d-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5e53d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
