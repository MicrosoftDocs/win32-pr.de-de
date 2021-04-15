---
description: 'Weitere Informationen finden Sie unter: esentdiskexception-Klasse'
title: Esentdiskexception-Klasse
TOCTitle: EsentDiskException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDiskException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskexception(v=EXCHG.10)
ms:contentKeyID: 55101517
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDiskException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22c2e2e2f829b6fcc6967e6e58692613243549c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393733"
---
# <a name="esentdiskexception-class"></a><span data-ttu-id="55072-103">Esentdiskexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="55072-103">EsentDiskException class</span></span>

<span data-ttu-id="55072-104">Basisklasse für Datenträger Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="55072-104">Base class for Disk exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="55072-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="55072-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="55072-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="55072-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="55072-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="55072-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="55072-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="55072-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="55072-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="55072-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="55072-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="55072-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="55072-111">Microsoft. ISAM. ESENT. Interop. esentresourceexception</span><span class="sxs-lookup"><span data-stu-id="55072-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="55072-112">Microsoft. ISAM. ESENT. Interop. esentdiskexception</span><span class="sxs-lookup"><span data-stu-id="55072-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>  
              [<span data-ttu-id="55072-113">Microsoft. ISAM. ESENT. Interop. esentdiskfullexception</span><span class="sxs-lookup"><span data-stu-id="55072-113">Microsoft.Isam.Esent.Interop.EsentDiskFullException</span></span>](./esentdiskfullexception-class.md)  
              [<span data-ttu-id="55072-114">Microsoft. ISAM. ESENT. Interop. esentlogdiskfullexception</span><span class="sxs-lookup"><span data-stu-id="55072-114">Microsoft.Isam.Esent.Interop.EsentLogDiskFullException</span></span>](./esentlogdiskfullexception-class.md)  

<span data-ttu-id="55072-115">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="55072-115">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="55072-116">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="55072-116">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="55072-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="55072-117">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentDiskException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentDiskException
```

``` csharp
[SerializableAttribute]
public abstract class EsentDiskException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="55072-118">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="55072-118">Thread safety</span></span>

<span data-ttu-id="55072-119">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="55072-119">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="55072-120">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="55072-120">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="55072-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55072-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55072-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="55072-122">Reference</span></span>

[<span data-ttu-id="55072-123">Esentdiskexception-Member</span><span class="sxs-lookup"><span data-stu-id="55072-123">EsentDiskException members</span></span>](./esentdiskexception-members.md)

[<span data-ttu-id="55072-124">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="55072-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
