---
description: 'Weitere Informationen finden Sie unter: esentinvalidloggedoperationexception-Klasse'
title: Esentinvalidloggedoperationexception-Klasse
TOCTitle: EsentInvalidLoggedOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidLoggedOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidloggedoperationexception(v=EXCHG.10)
ms:contentKeyID: 55101979
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidLoggedOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidLoggedOperationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d75ef32f471fcdae7e520844c4df8ef55260f682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485427"
---
# <a name="esentinvalidloggedoperationexception-class"></a><span data-ttu-id="d5544-103">Esentinvalidloggedoperationexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="d5544-103">EsentInvalidLoggedOperationException class</span></span>

<span data-ttu-id="d5544-104">Basisklasse für JET_err. Invalidloggedoperation-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="d5544-104">Base class for JET_err.InvalidLoggedOperation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d5544-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="d5544-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d5544-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d5544-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d5544-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d5544-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d5544-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="d5544-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d5544-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="d5544-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d5544-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="d5544-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="d5544-111">Microsoft. ISAM. ESENT. Interop. esentobsoleteexception</span><span class="sxs-lookup"><span data-stu-id="d5544-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="d5544-112">Microsoft. ISAM. ESENT. Interop. esentinvalidloggedoperationexception</span><span class="sxs-lookup"><span data-stu-id="d5544-112">Microsoft.Isam.Esent.Interop.EsentInvalidLoggedOperationException</span></span>  

<span data-ttu-id="d5544-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d5544-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d5544-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d5544-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d5544-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5544-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidLoggedOperationException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentInvalidLoggedOperationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidLoggedOperationException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="d5544-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="d5544-116">Thread safety</span></span>

<span data-ttu-id="d5544-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="d5544-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d5544-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="d5544-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5544-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5544-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d5544-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="d5544-120">Reference</span></span>

[<span data-ttu-id="d5544-121">Esentinvalidloggedoperationexception-Member</span><span class="sxs-lookup"><span data-stu-id="d5544-121">EsentInvalidLoggedOperationException members</span></span>](./esentinvalidloggedoperationexception-members.md)

[<span data-ttu-id="d5544-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="d5544-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
