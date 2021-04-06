---
description: 'Weitere Informationen finden Sie unter: esentlogdisabledduetorecoveryfailureexception-Klasse'
title: Esentlogdisabledduetorecoveryfailureexception-Klasse
TOCTitle: EsentLogDisabledDueToRecoveryFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogDisabledDueToRecoveryFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogdisabledduetorecoveryfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102151
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogDisabledDueToRecoveryFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogDisabledDueToRecoveryFailureException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b1a631dc6e0495a958555547f8e7c540263dfc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960981"
---
# <a name="esentlogdisabledduetorecoveryfailureexception-class"></a><span data-ttu-id="4f28e-103">Esentlogdisabledduetorecoveryfailureexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="4f28e-103">EsentLogDisabledDueToRecoveryFailureException class</span></span>

<span data-ttu-id="4f28e-104">Basisklasse für JET_err. Logdisabledduetorecoveryfailure-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="4f28e-104">Base class for JET_err.LogDisabledDueToRecoveryFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4f28e-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="4f28e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4f28e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4f28e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4f28e-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="4f28e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4f28e-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="4f28e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4f28e-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="4f28e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4f28e-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="4f28e-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="4f28e-111">Microsoft. ISAM. ESENT. Interop. esentfatalexception</span><span class="sxs-lookup"><span data-stu-id="4f28e-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
            <span data-ttu-id="4f28e-112">Microsoft. ISAM. ESENT. Interop. esentlogdisabledduetorecoveryfailureexception</span><span class="sxs-lookup"><span data-stu-id="4f28e-112">Microsoft.Isam.Esent.Interop.EsentLogDisabledDueToRecoveryFailureException</span></span>  

<span data-ttu-id="4f28e-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4f28e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4f28e-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4f28e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4f28e-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f28e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogDisabledDueToRecoveryFailureException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentLogDisabledDueToRecoveryFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogDisabledDueToRecoveryFailureException : EsentFatalException
```

## <a name="thread-safety"></a><span data-ttu-id="4f28e-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="4f28e-116">Thread safety</span></span>

<span data-ttu-id="4f28e-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="4f28e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4f28e-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="4f28e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f28e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f28e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4f28e-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="4f28e-120">Reference</span></span>

[<span data-ttu-id="4f28e-121">Esentlogdisabledduetorecoveryfailureexception-Member</span><span class="sxs-lookup"><span data-stu-id="4f28e-121">EsentLogDisabledDueToRecoveryFailureException members</span></span>](./esentlogdisabledduetorecoveryfailureexception-members.md)

[<span data-ttu-id="4f28e-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="4f28e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
