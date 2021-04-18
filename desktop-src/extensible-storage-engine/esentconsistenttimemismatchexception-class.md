---
description: 'Weitere Informationen finden Sie unter: esentkonsistenttimemismatchexception-Klasse'
title: Esentkonsistenttimemismatchexception-Klasse
TOCTitle: EsentConsistentTimeMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentconsistenttimemismatchexception(v=EXCHG.10)
ms:contentKeyID: 55101416
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c356f32fa3c478ff376b651b9715cb5c89a337d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344033"
---
# <a name="esentconsistenttimemismatchexception-class"></a><span data-ttu-id="871fa-103">Esentkonsistenttimemismatchexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="871fa-103">EsentConsistentTimeMismatchException class</span></span>

<span data-ttu-id="871fa-104">Basisklasse für JET_err. "Konsistenttimemismatch"-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="871fa-104">Base class for JET_err.ConsistentTimeMismatch exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="871fa-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="871fa-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="871fa-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="871fa-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="871fa-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="871fa-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="871fa-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="871fa-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="871fa-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="871fa-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="871fa-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="871fa-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="871fa-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="871fa-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="871fa-112">Microsoft. ISAM. ESENT. Interop. esentkonsistenttimemismatchexception</span><span class="sxs-lookup"><span data-stu-id="871fa-112">Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException</span></span>  

<span data-ttu-id="871fa-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="871fa-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="871fa-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="871fa-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="871fa-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="871fa-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentConsistentTimeMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentConsistentTimeMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentConsistentTimeMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="871fa-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="871fa-116">Thread safety</span></span>

<span data-ttu-id="871fa-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="871fa-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="871fa-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="871fa-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="871fa-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="871fa-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="871fa-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="871fa-120">Reference</span></span>

[<span data-ttu-id="871fa-121">Esentkonsistenttimemismatchexception-Member</span><span class="sxs-lookup"><span data-stu-id="871fa-121">EsentConsistentTimeMismatchException members</span></span>](./esentconsistenttimemismatchexception-members.md)

[<span data-ttu-id="871fa-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="871fa-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
