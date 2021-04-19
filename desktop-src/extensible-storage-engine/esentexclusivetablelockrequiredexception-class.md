---
description: 'Weitere Informationen finden Sie unter: esentexclusivetablelockrequirements dexception-Klasse'
title: Esentexclusivetablelockrequirements dexception-Klasse
TOCTitle: EsentExclusiveTableLockRequiredException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentExclusiveTableLockRequiredException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentexclusivetablelockrequiredexception(v=EXCHG.10)
ms:contentKeyID: 55101593
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentExclusiveTableLockRequiredException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentExclusiveTableLockRequiredException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c167ab3910b3ba3ce69bc4f946ba7d315256b17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362313"
---
# <a name="esentexclusivetablelockrequiredexception-class"></a><span data-ttu-id="53ff6-103">Esentexclusivetablelockrequirements dexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="53ff6-103">EsentExclusiveTableLockRequiredException class</span></span>

<span data-ttu-id="53ff6-104">Basisklasse für JET_err. Exclusivetablelockrequired-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="53ff6-104">Base class for JET_err.ExclusiveTableLockRequired exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="53ff6-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="53ff6-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="53ff6-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="53ff6-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="53ff6-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="53ff6-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="53ff6-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="53ff6-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="53ff6-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="53ff6-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="53ff6-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="53ff6-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="53ff6-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="53ff6-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="53ff6-112">Microsoft. ISAM. ESENT. Interop. esentexclusivetablelockrequirements dexception</span><span class="sxs-lookup"><span data-stu-id="53ff6-112">Microsoft.Isam.Esent.Interop.EsentExclusiveTableLockRequiredException</span></span>  

<span data-ttu-id="53ff6-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="53ff6-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="53ff6-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="53ff6-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="53ff6-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="53ff6-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentExclusiveTableLockRequiredException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentExclusiveTableLockRequiredException
```

``` csharp
[SerializableAttribute]
public sealed class EsentExclusiveTableLockRequiredException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="53ff6-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="53ff6-116">Thread safety</span></span>

<span data-ttu-id="53ff6-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="53ff6-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="53ff6-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="53ff6-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="53ff6-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53ff6-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="53ff6-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="53ff6-120">Reference</span></span>

[<span data-ttu-id="53ff6-121">Esentexclusivetablelockrequirements dexception-Member</span><span class="sxs-lookup"><span data-stu-id="53ff6-121">EsentExclusiveTableLockRequiredException members</span></span>](./esentexclusivetablelockrequiredexception-members.md)

[<span data-ttu-id="53ff6-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="53ff6-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
