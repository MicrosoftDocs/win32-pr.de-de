---
description: 'Weitere Informationen finden Sie unter: esentcheckpointfilename-FoundException-Klasse'
title: Esentcheckpointfile topics-Klasse
TOCTitle: EsentCheckpointFileNotFoundException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCheckpointFileNotFoundException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcheckpointfilenotfoundexception(v=EXCHG.10)
ms:contentKeyID: 55101224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCheckpointFileNotFoundException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCheckpointFileNotFoundException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52be1ce919119158e7f7f9aa40631767c2b9488d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132076"
---
# <a name="esentcheckpointfilenotfoundexception-class"></a><span data-ttu-id="16326-103">Esentcheckpointfile topics-Klasse</span><span class="sxs-lookup"><span data-stu-id="16326-103">EsentCheckpointFileNotFoundException class</span></span>

<span data-ttu-id="16326-104">Basisklasse für JET_err. Checkpointfile-found-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="16326-104">Base class for JET_err.CheckpointFileNotFound exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="16326-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="16326-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="16326-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="16326-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="16326-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="16326-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="16326-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="16326-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="16326-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="16326-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="16326-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="16326-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="16326-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="16326-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="16326-112">Microsoft. ISAM. ESENT. Interop. esentcheckpointfile topics-Quelle</span><span class="sxs-lookup"><span data-stu-id="16326-112">Microsoft.Isam.Esent.Interop.EsentCheckpointFileNotFoundException</span></span>  

<span data-ttu-id="16326-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="16326-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="16326-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="16326-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="16326-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="16326-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCheckpointFileNotFoundException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentCheckpointFileNotFoundException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCheckpointFileNotFoundException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="16326-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="16326-116">Thread safety</span></span>

<span data-ttu-id="16326-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="16326-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="16326-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="16326-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="16326-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16326-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="16326-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="16326-120">Reference</span></span>

[<span data-ttu-id="16326-121">Esentcheckpointfile topics-Elemente</span><span class="sxs-lookup"><span data-stu-id="16326-121">EsentCheckpointFileNotFoundException members</span></span>](./esentcheckpointfilenotfoundexception-members.md)

[<span data-ttu-id="16326-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="16326-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
