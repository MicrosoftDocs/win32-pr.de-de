---
description: 'Weitere Informationen finden Sie unter: esentesomanysortsexception-Klasse'
title: Esentesomanysortsexception-Klasse
TOCTitle: EsentTooManySortsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManySortsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanysortsexception(v=EXCHG.10)
ms:contentKeyID: 55103099
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManySortsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManySortsException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9048d2c7c65906ba6f093f21c604f25adfcf16c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344439"
---
# <a name="esenttoomanysortsexception-class"></a><span data-ttu-id="ae145-103">Esentesomanysortsexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="ae145-103">EsentTooManySortsException class</span></span>

<span data-ttu-id="ae145-104">Basisklasse für JET_err. "-Ausnahmen sortieren".</span><span class="sxs-lookup"><span data-stu-id="ae145-104">Base class for JET_err.TooManySorts exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ae145-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="ae145-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ae145-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ae145-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ae145-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ae145-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ae145-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="ae145-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ae145-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="ae145-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ae145-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="ae145-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="ae145-111">Microsoft. ISAM. ESENT. Interop. esentresourceexception</span><span class="sxs-lookup"><span data-stu-id="ae145-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="ae145-112">Microsoft. ISAM. ESENT. Interop. esentmemoryexception</span><span class="sxs-lookup"><span data-stu-id="ae145-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="ae145-113">Microsoft. ISAM. ESENT. Interop. esentesomanysortsexception</span><span class="sxs-lookup"><span data-stu-id="ae145-113">Microsoft.Isam.Esent.Interop.EsentTooManySortsException</span></span>  

<span data-ttu-id="ae145-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ae145-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ae145-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ae145-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ae145-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae145-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManySortsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentTooManySortsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManySortsException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="ae145-117">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="ae145-117">Thread safety</span></span>

<span data-ttu-id="ae145-118">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="ae145-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ae145-119">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="ae145-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae145-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae145-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ae145-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="ae145-121">Reference</span></span>

[<span data-ttu-id="ae145-122">Esentesomanysortsexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="ae145-122">EsentTooManySortsException members</span></span>](./esenttoomanysortsexception-members.md)

[<span data-ttu-id="ae145-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ae145-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
