---
description: 'Weitere Informationen finden Sie unter: esentbadlogversionexception-Klasse'
title: Esentbadlogversionexception-Klasse
TOCTitle: EsentBadLogVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadLogVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadlogversionexception(v=EXCHG.10)
ms:contentKeyID: 55101079
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadLogVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadLogVersionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e1bdf96dd46fdd16a566c2a6cc5047f4a74fef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485723"
---
# <a name="esentbadlogversionexception-class"></a><span data-ttu-id="5e254-103">Esentbadlogversionexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="5e254-103">EsentBadLogVersionException class</span></span>

<span data-ttu-id="5e254-104">Basisklasse für JET_err. Badlogversion-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="5e254-104">Base class for JET_err.BadLogVersion exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5e254-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="5e254-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5e254-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5e254-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5e254-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="5e254-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5e254-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="5e254-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5e254-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="5e254-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5e254-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="5e254-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="5e254-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="5e254-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="5e254-112">Microsoft. ISAM. ESENT. Interop. esentbadlogversionexception</span><span class="sxs-lookup"><span data-stu-id="5e254-112">Microsoft.Isam.Esent.Interop.EsentBadLogVersionException</span></span>  

<span data-ttu-id="5e254-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5e254-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5e254-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5e254-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5e254-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e254-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadLogVersionException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentBadLogVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadLogVersionException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="5e254-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="5e254-116">Thread safety</span></span>

<span data-ttu-id="5e254-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="5e254-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5e254-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="5e254-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e254-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e254-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5e254-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="5e254-120">Reference</span></span>

[<span data-ttu-id="5e254-121">Esentbadlogversionexception-Member</span><span class="sxs-lookup"><span data-stu-id="5e254-121">EsentBadLogVersionException members</span></span>](./esentbadlogversionexception-members.md)

[<span data-ttu-id="5e254-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5e254-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
