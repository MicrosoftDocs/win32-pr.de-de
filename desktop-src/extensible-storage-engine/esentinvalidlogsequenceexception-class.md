---
description: 'Weitere Informationen finden Sie unter: esentinvalidlogsequenceexception-Klasse'
title: Esentinvalidlogsequenceexception-Klasse
TOCTitle: EsentInvalidLogSequenceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidlogsequenceexception(v=EXCHG.10)
ms:contentKeyID: 55107285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8803298a3202ea151bcb42e5490931c0aba2705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960601"
---
# <a name="esentinvalidlogsequenceexception-class"></a><span data-ttu-id="99550-103">Esentinvalidlogsequenceexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="99550-103">EsentInvalidLogSequenceException class</span></span>

<span data-ttu-id="99550-104">Basisklasse für JET_err. Invalidlogsequence-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="99550-104">Base class for JET_err.InvalidLogSequence exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="99550-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="99550-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="99550-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="99550-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="99550-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="99550-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="99550-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="99550-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="99550-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="99550-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="99550-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="99550-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="99550-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="99550-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="99550-112">Microsoft. ISAM. ESENT. Interop. esentinvalidlogsequenceexception</span><span class="sxs-lookup"><span data-stu-id="99550-112">Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException</span></span>  

<span data-ttu-id="99550-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="99550-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="99550-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="99550-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="99550-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="99550-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidLogSequenceException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentInvalidLogSequenceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidLogSequenceException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="99550-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="99550-116">Thread safety</span></span>

<span data-ttu-id="99550-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="99550-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="99550-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="99550-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="99550-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99550-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="99550-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="99550-120">Reference</span></span>

[<span data-ttu-id="99550-121">Esentinvalidlogsequenceexception-Member</span><span class="sxs-lookup"><span data-stu-id="99550-121">EsentInvalidLogSequenceException members</span></span>](./esentinvalidlogsequenceexception-members.md)

[<span data-ttu-id="99550-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="99550-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
