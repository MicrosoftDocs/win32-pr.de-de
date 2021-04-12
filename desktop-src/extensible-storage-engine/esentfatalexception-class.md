---
description: 'Weitere Informationen finden Sie unter: esentfatalexception-Klasse'
title: EsentFatalException-Klasse
TOCTitle: EsentFatalException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFatalException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFatalException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c38df447f2eb816772713ba930204e75aa38a88c
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218938"
---
# <a name="esentfatalexception-class"></a><span data-ttu-id="a3968-103">EsentFatalException-Klasse</span><span class="sxs-lookup"><span data-stu-id="a3968-103">EsentFatalException class</span></span>

<span data-ttu-id="a3968-104">Basisklasse für schwerwiegende Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="a3968-104">Base class for Fatal exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a3968-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="a3968-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a3968-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a3968-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a3968-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="a3968-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a3968-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="a3968-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a3968-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="a3968-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a3968-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="a3968-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="a3968-111">Microsoft. ISAM. ESENT. Interop. esentfatalexception</span><span class="sxs-lookup"><span data-stu-id="a3968-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>  
            

<span data-ttu-id="a3968-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a3968-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a3968-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a3968-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a3968-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3968-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFatalException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentFatalException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFatalException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="a3968-115">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="a3968-115">Thread safety</span></span>

<span data-ttu-id="a3968-116">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="a3968-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a3968-117">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="a3968-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3968-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3968-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a3968-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="a3968-119">Reference</span></span>

[<span data-ttu-id="a3968-120">Esentfatalexception-Member</span><span class="sxs-lookup"><span data-stu-id="a3968-120">EsentFatalException members</span></span>](./esentfatalexception-members.md)

[<span data-ttu-id="a3968-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="a3968-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="a3968-122">Abgeleitete Typen</span><span class="sxs-lookup"><span data-stu-id="a3968-122">Derived types</span></span>

[<span data-ttu-id="a3968-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="a3968-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a3968-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="a3968-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a3968-125">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="a3968-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a3968-126">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="a3968-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a3968-127">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="a3968-127">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="a3968-128">Microsoft. ISAM. ESENT. Interop. esentfatalexception</span><span class="sxs-lookup"><span data-stu-id="a3968-128">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>  
            [<span data-ttu-id="a3968-129">Microsoft. ISAM. ESENT. Interop. esentinstanceunavailableduetofatemangdiskfullexception</span><span class="sxs-lookup"><span data-stu-id="a3968-129">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableDueToFatalLogDiskFullException</span></span>](./esentinstanceunavailableduetofatallogdiskfullexception-class.md)  
            [<span data-ttu-id="a3968-130">Microsoft. ISAM. ESENT. Interop. esentinstanceunavailableexception</span><span class="sxs-lookup"><span data-stu-id="a3968-130">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException</span></span>](./esentinstanceunavailableexception-class.md)  
            [<span data-ttu-id="a3968-131">Microsoft. ISAM. ESENT. Interop. esentlogdisabledduetorecoveryfailureexception</span><span class="sxs-lookup"><span data-stu-id="a3968-131">Microsoft.Isam.Esent.Interop.EsentLogDisabledDueToRecoveryFailureException</span></span>](./esentlogdisabledduetorecoveryfailureexception-class.md)  
            [<span data-ttu-id="a3968-132">Microsoft. ISAM. ESENT. Interop. esentrollbackerrorexception</span><span class="sxs-lookup"><span data-stu-id="a3968-132">Microsoft.Isam.Esent.Interop.EsentRollbackErrorException</span></span>](./esentrollbackerrorexception-class.md)  
            [<span data-ttu-id="a3968-133">Microsoft. ISAM. ESENT. Interop. esentsector sizenotsupportedexception</span><span class="sxs-lookup"><span data-stu-id="a3968-133">Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException</span></span>](./esentsectorsizenotsupportedexception-class.md)  
            [<span data-ttu-id="a3968-134">Microsoft. ISAM. ESENT. Interop. esentunloadableosfunctionalityexception</span><span class="sxs-lookup"><span data-stu-id="a3968-134">Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException</span></span>](./esentunloadableosfunctionalityexception-class.md)