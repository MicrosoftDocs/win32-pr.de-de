---
description: 'Weitere Informationen finden Sie unter: esentquotaexception-Klasse'
title: EsentQuotaException-Klasse
TOCTitle: EsentQuotaException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentQuotaException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102495
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53b108a4d55553788a6c2d316f93f4f8efc76035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362910"
---
# <a name="esentquotaexception-class"></a><span data-ttu-id="7569f-103">EsentQuotaException-Klasse</span><span class="sxs-lookup"><span data-stu-id="7569f-103">EsentQuotaException class</span></span>

<span data-ttu-id="7569f-104">Basisklasse für Kontingent Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="7569f-104">Base class for Quota exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7569f-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="7569f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7569f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7569f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7569f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="7569f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7569f-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="7569f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7569f-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="7569f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7569f-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="7569f-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="7569f-111">Microsoft. ISAM. ESENT. Interop. esentresourceexception</span><span class="sxs-lookup"><span data-stu-id="7569f-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="7569f-112">Microsoft. ISAM. ESENT. Interop. esentquotaexception</span><span class="sxs-lookup"><span data-stu-id="7569f-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>  
              [<span data-ttu-id="7569f-113">Microsoft. ISAM. ESENT. Interop. esentouesfdatabasespaceexception</span><span class="sxs-lookup"><span data-stu-id="7569f-113">Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException</span></span>](./esentoutofdatabasespaceexception-class.md)  
              [<span data-ttu-id="7569f-114">Microsoft. ISAM. ESENT. Interop. esentesomanyinstancesexception</span><span class="sxs-lookup"><span data-stu-id="7569f-114">Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException</span></span>](./esenttoomanyinstancesexception-class.md)  
              [<span data-ttu-id="7569f-115">Microsoft. ISAM. ESENT. Interop. esentesomanyopentablesexception</span><span class="sxs-lookup"><span data-stu-id="7569f-115">Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException</span></span>](./esenttoomanyopentablesexception-class.md)  
              [<span data-ttu-id="7569f-116">Microsoft. ISAM. ESENT. Interop. esentversionstoreouesf memoryexception</span><span class="sxs-lookup"><span data-stu-id="7569f-116">Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException</span></span>](./esentversionstoreoutofmemoryexception-class.md)  

<span data-ttu-id="7569f-117">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7569f-117">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7569f-118">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7569f-118">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7569f-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="7569f-119">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentQuotaException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentQuotaException
```

``` csharp
[SerializableAttribute]
public abstract class EsentQuotaException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="7569f-120">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="7569f-120">Thread safety</span></span>

<span data-ttu-id="7569f-121">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="7569f-121">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7569f-122">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="7569f-122">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7569f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7569f-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7569f-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="7569f-124">Reference</span></span>

[<span data-ttu-id="7569f-125">Esentquotaexception-Member</span><span class="sxs-lookup"><span data-stu-id="7569f-125">EsentQuotaException members</span></span>](./esentquotaexception-members.md)

[<span data-ttu-id="7569f-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="7569f-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
