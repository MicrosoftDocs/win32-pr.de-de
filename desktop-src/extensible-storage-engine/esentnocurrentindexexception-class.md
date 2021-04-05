---
description: 'Weitere Informationen finden Sie unter: esentnocurrentindexexception-Klasse'
title: Esentnocurrentindexexception-Klasse
TOCTitle: EsentNoCurrentIndexException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNoCurrentIndexException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnocurrentindexexception(v=EXCHG.10)
ms:contentKeyID: 55102286
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNoCurrentIndexException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNoCurrentIndexException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a450f59ed2d90d9b352880ba1864daa621392516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757500"
---
# <a name="esentnocurrentindexexception-class"></a><span data-ttu-id="203a5-103">Esentnocurrentindexexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="203a5-103">EsentNoCurrentIndexException class</span></span>

<span data-ttu-id="203a5-104">Basisklasse für JET_err. Nocurrentindex-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="203a5-104">Base class for JET_err.NoCurrentIndex exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="203a5-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="203a5-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="203a5-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="203a5-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="203a5-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="203a5-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="203a5-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="203a5-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="203a5-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="203a5-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="203a5-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="203a5-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="203a5-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="203a5-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="203a5-112">Microsoft. ISAM. ESENT. Interop. esentnocurrentindexexception</span><span class="sxs-lookup"><span data-stu-id="203a5-112">Microsoft.Isam.Esent.Interop.EsentNoCurrentIndexException</span></span>  

<span data-ttu-id="203a5-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="203a5-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="203a5-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="203a5-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="203a5-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="203a5-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNoCurrentIndexException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentNoCurrentIndexException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNoCurrentIndexException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="203a5-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="203a5-116">Thread safety</span></span>

<span data-ttu-id="203a5-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="203a5-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="203a5-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="203a5-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="203a5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="203a5-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="203a5-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="203a5-120">Reference</span></span>

[<span data-ttu-id="203a5-121">Esentnocurrentindexexception-Member</span><span class="sxs-lookup"><span data-stu-id="203a5-121">EsentNoCurrentIndexException members</span></span>](./esentnocurrentindexexception-members.md)

[<span data-ttu-id="203a5-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="203a5-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
