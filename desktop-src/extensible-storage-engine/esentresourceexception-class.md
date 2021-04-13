---
description: 'Weitere Informationen finden Sie unter: esentresourceexception-Klasse'
title: EsentResourceException-Klasse
TOCTitle: EsentResourceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentResourceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresourceexception(v=EXCHG.10)
ms:contentKeyID: 55102627
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentResourceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentResourceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7d4964bb4ed9c1305652d9425170bd934c9274e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216656"
---
# <a name="esentresourceexception-class"></a><span data-ttu-id="bdb75-103">EsentResourceException-Klasse</span><span class="sxs-lookup"><span data-stu-id="bdb75-103">EsentResourceException class</span></span>

<span data-ttu-id="bdb75-104">Basisklasse für Ressourcen Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="bdb75-104">Base class for Resource exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="bdb75-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="bdb75-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="bdb75-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="bdb75-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="bdb75-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="bdb75-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="bdb75-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="bdb75-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="bdb75-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="bdb75-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="bdb75-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="bdb75-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="bdb75-111">Microsoft. ISAM. ESENT. Interop. esentresourceexception</span><span class="sxs-lookup"><span data-stu-id="bdb75-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>  
            [<span data-ttu-id="bdb75-112">Microsoft. ISAM. ESENT. Interop. esentdiskexception</span><span class="sxs-lookup"><span data-stu-id="bdb75-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>](./esentdiskexception-class.md)  
            [<span data-ttu-id="bdb75-113">Microsoft. ISAM. ESENT. Interop. esentmemoryexception</span><span class="sxs-lookup"><span data-stu-id="bdb75-113">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
            [<span data-ttu-id="bdb75-114">Microsoft. ISAM. ESENT. Interop. esentquotaexception</span><span class="sxs-lookup"><span data-stu-id="bdb75-114">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
            [<span data-ttu-id="bdb75-115">Microsoft. ISAM. ESENT. Interop. esenttaskdroppedexception</span><span class="sxs-lookup"><span data-stu-id="bdb75-115">Microsoft.Isam.Esent.Interop.EsentTaskDroppedException</span></span>](./esenttaskdroppedexception-class.md)  
            [<span data-ttu-id="bdb75-116">Microsoft. ISAM. ESENT. Interop. esentesomanyioexception</span><span class="sxs-lookup"><span data-stu-id="bdb75-116">Microsoft.Isam.Esent.Interop.EsentTooManyIOException</span></span>](./esenttoomanyioexception-class.md)  

<span data-ttu-id="bdb75-117">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bdb75-117">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bdb75-118">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bdb75-118">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bdb75-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdb75-119">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentResourceException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentResourceException
```

``` csharp
[SerializableAttribute]
public abstract class EsentResourceException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="bdb75-120">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="bdb75-120">Thread safety</span></span>

<span data-ttu-id="bdb75-121">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="bdb75-121">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="bdb75-122">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="bdb75-122">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="bdb75-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdb75-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bdb75-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="bdb75-124">Reference</span></span>

[<span data-ttu-id="bdb75-125">Esentresourceexception-Member</span><span class="sxs-lookup"><span data-stu-id="bdb75-125">EsentResourceException members</span></span>](./esentresourceexception-members.md)

[<span data-ttu-id="bdb75-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="bdb75-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
