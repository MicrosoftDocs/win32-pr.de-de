---
description: 'Weitere Informationen finden Sie unter: esentesomanyinstancesexception-Klasse'
title: Esentesomanyinstancesexception-Klasse
TOCTitle: EsentTooManyInstancesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyinstancesexception(v=EXCHG.10)
ms:contentKeyID: 55103084
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ecd20f6a05a17d4bd21623732a4e716e82c9b1cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359457"
---
# <a name="esenttoomanyinstancesexception-class"></a><span data-ttu-id="c960a-103">Esentesomanyinstancesexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="c960a-103">EsentTooManyInstancesException class</span></span>

<span data-ttu-id="c960a-104">Basisklasse für JET_err. Ausnahmen für "-Instanzen".</span><span class="sxs-lookup"><span data-stu-id="c960a-104">Base class for JET_err.TooManyInstances exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c960a-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="c960a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c960a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c960a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c960a-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c960a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c960a-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="c960a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c960a-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="c960a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c960a-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="c960a-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="c960a-111">Microsoft. ISAM. ESENT. Interop. esentresourceexception</span><span class="sxs-lookup"><span data-stu-id="c960a-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="c960a-112">Microsoft. ISAM. ESENT. Interop. esentquotaexception</span><span class="sxs-lookup"><span data-stu-id="c960a-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
              <span data-ttu-id="c960a-113">Microsoft. ISAM. ESENT. Interop. esentesomanyinstancesexception</span><span class="sxs-lookup"><span data-stu-id="c960a-113">Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException</span></span>  

<span data-ttu-id="c960a-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c960a-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c960a-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c960a-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c960a-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="c960a-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyInstancesException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentTooManyInstancesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyInstancesException : EsentQuotaException
```

## <a name="thread-safety"></a><span data-ttu-id="c960a-117">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="c960a-117">Thread safety</span></span>

<span data-ttu-id="c960a-118">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="c960a-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c960a-119">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="c960a-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c960a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c960a-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c960a-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="c960a-121">Reference</span></span>

[<span data-ttu-id="c960a-122">Esentesomanyinstancesexception-Member</span><span class="sxs-lookup"><span data-stu-id="c960a-122">EsentTooManyInstancesException members</span></span>](./esenttoomanyinstancesexception-members.md)

[<span data-ttu-id="c960a-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="c960a-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
