---
description: 'Weitere Informationen finden Sie unter: esentrestoreingeprogressexception-Klasse'
title: Esentrestoreingeprogressexception-Klasse
TOCTitle: EsentRestoreInProgressException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrestoreinprogressexception(v=EXCHG.10)
ms:contentKeyID: 55102631
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0906d1ee8c196260d36da8d385a0e48e12f31018
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364249"
---
# <a name="esentrestoreinprogressexception-class"></a><span data-ttu-id="94f78-103">Esentrestoreingeprogressexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="94f78-103">EsentRestoreInProgressException class</span></span>

<span data-ttu-id="94f78-104">Basisklasse für JET_err. Restoreingabe Progress-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="94f78-104">Base class for JET_err.RestoreInProgress exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="94f78-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="94f78-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="94f78-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="94f78-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="94f78-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="94f78-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="94f78-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="94f78-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="94f78-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="94f78-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="94f78-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="94f78-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="94f78-111">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="94f78-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="94f78-112">Microsoft. ISAM. ESENT. Interop. esentrestoreingeprogressexception</span><span class="sxs-lookup"><span data-stu-id="94f78-112">Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException</span></span>  

<span data-ttu-id="94f78-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="94f78-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="94f78-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="94f78-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="94f78-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="94f78-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRestoreInProgressException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRestoreInProgressException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRestoreInProgressException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="94f78-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="94f78-116">Thread safety</span></span>

<span data-ttu-id="94f78-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="94f78-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="94f78-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="94f78-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="94f78-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94f78-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="94f78-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="94f78-120">Reference</span></span>

[<span data-ttu-id="94f78-121">Esentrestoreingeprogressexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="94f78-121">EsentRestoreInProgressException members</span></span>](./esentrestoreinprogressexception-members.md)

[<span data-ttu-id="94f78-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="94f78-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
