---
description: 'Weitere Informationen über: esenttransleseronlyexception-Klasse'
title: Esenttransleseronlyexception-Klasse
TOCTitle: EsentTransReadOnlyException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTransReadOnlyException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttransreadonlyexception(v=EXCHG.10)
ms:contentKeyID: 55107336
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTransReadOnlyException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTransReadOnlyException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eeb3576b2c33356c942e427d92bc40697c09921a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345649"
---
# <a name="esenttransreadonlyexception-class"></a><span data-ttu-id="f4c00-103">Esenttransleseronlyexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="f4c00-103">EsentTransReadOnlyException class</span></span>

<span data-ttu-id="f4c00-104">Basisklasse für JET_err. Transread only-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="f4c00-104">Base class for JET_err.TransReadOnly exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f4c00-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="f4c00-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f4c00-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f4c00-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f4c00-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f4c00-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f4c00-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="f4c00-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f4c00-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="f4c00-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f4c00-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="f4c00-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f4c00-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="f4c00-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="f4c00-112">Microsoft. ISAM. ESENT. Interop. esenttransread onlyexception</span><span class="sxs-lookup"><span data-stu-id="f4c00-112">Microsoft.Isam.Esent.Interop.EsentTransReadOnlyException</span></span>  

<span data-ttu-id="f4c00-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f4c00-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f4c00-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f4c00-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f4c00-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4c00-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTransReadOnlyException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTransReadOnlyException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTransReadOnlyException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="f4c00-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="f4c00-116">Thread safety</span></span>

<span data-ttu-id="f4c00-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="f4c00-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f4c00-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="f4c00-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4c00-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4c00-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f4c00-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="f4c00-120">Reference</span></span>

[<span data-ttu-id="f4c00-121">Esenttransread onlyexception-Member</span><span class="sxs-lookup"><span data-stu-id="f4c00-121">EsentTransReadOnlyException members</span></span>](./esenttransreadonlyexception-members.md)

[<span data-ttu-id="f4c00-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f4c00-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
