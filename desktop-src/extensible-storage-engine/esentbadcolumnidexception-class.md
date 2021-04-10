---
description: 'Weitere Informationen finden Sie unter: esentbadcolumnidexception-Klasse'
title: Esentbadcolumnidexception-Klasse
TOCTitle: EsentBadColumnIdException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadColumnIdException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadcolumnidexception(v=EXCHG.10)
ms:contentKeyID: 55101061
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadColumnIdException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadColumnIdException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94b7e898b95130df4a1f7e3a88fa2e450d3b6776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042736"
---
# <a name="esentbadcolumnidexception-class"></a><span data-ttu-id="4c22f-103">Esentbadcolumnidexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="4c22f-103">EsentBadColumnIdException class</span></span>

<span data-ttu-id="4c22f-104">Basisklasse für JET_err. Badcolumnid-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="4c22f-104">Base class for JET_err.BadColumnId exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4c22f-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="4c22f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4c22f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4c22f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4c22f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="4c22f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4c22f-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="4c22f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4c22f-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="4c22f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4c22f-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="4c22f-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="4c22f-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="4c22f-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="4c22f-112">Microsoft. ISAM. ESENT. Interop. esentbadcolumnidexception</span><span class="sxs-lookup"><span data-stu-id="4c22f-112">Microsoft.Isam.Esent.Interop.EsentBadColumnIdException</span></span>  

<span data-ttu-id="4c22f-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4c22f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4c22f-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4c22f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4c22f-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c22f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadColumnIdException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentBadColumnIdException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadColumnIdException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="4c22f-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="4c22f-116">Thread safety</span></span>

<span data-ttu-id="4c22f-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="4c22f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4c22f-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="4c22f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c22f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c22f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4c22f-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="4c22f-120">Reference</span></span>

[<span data-ttu-id="4c22f-121">Esentbadcolumnidexception-Member</span><span class="sxs-lookup"><span data-stu-id="4c22f-121">EsentBadColumnIdException members</span></span>](./esentbadcolumnidexception-members.md)

[<span data-ttu-id="4c22f-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="4c22f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
