---
description: 'Weitere Informationen finden Sie unter: esentcannotdisableversioningexception-Klasse'
title: Esentcannotdisableversioningexception-Klasse
TOCTitle: EsentCannotDisableVersioningException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotDisableVersioningException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotdisableversioningexception(v=EXCHG.10)
ms:contentKeyID: 55101260
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotDisableVersioningException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotDisableVersioningException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df332b292d3bee2c4e25d9fc331d53f67bf9a0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749401"
---
# <a name="esentcannotdisableversioningexception-class"></a><span data-ttu-id="c88cb-103">Esentcannotdisableversioningexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="c88cb-103">EsentCannotDisableVersioningException class</span></span>

<span data-ttu-id="c88cb-104">Basisklasse für JET_err. Cannotdisableversioning-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="c88cb-104">Base class for JET_err.CannotDisableVersioning exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c88cb-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="c88cb-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c88cb-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c88cb-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c88cb-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c88cb-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c88cb-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="c88cb-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c88cb-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="c88cb-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c88cb-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="c88cb-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="c88cb-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="c88cb-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="c88cb-112">Microsoft. ISAM. ESENT. Interop. esentcannotdisableversioningexception</span><span class="sxs-lookup"><span data-stu-id="c88cb-112">Microsoft.Isam.Esent.Interop.EsentCannotDisableVersioningException</span></span>  

<span data-ttu-id="c88cb-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c88cb-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c88cb-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c88cb-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c88cb-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="c88cb-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotDisableVersioningException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentCannotDisableVersioningException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotDisableVersioningException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="c88cb-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="c88cb-116">Thread safety</span></span>

<span data-ttu-id="c88cb-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="c88cb-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c88cb-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="c88cb-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c88cb-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c88cb-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c88cb-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="c88cb-120">Reference</span></span>

[<span data-ttu-id="c88cb-121">Esentcannotdisableversioningexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="c88cb-121">EsentCannotDisableVersioningException members</span></span>](./esentcannotdisableversioningexception-members.md)

[<span data-ttu-id="c88cb-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="c88cb-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
