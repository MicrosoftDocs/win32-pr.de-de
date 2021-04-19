---
description: 'Weitere Informationen finden Sie unter: esentsecondaryindexverdertedexception-Klasse'
title: Esentsecondaryindexverdertedexception-Klasse
TOCTitle: EsentSecondaryIndexCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsecondaryindexcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55102677
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af6cc22e45db383dc3e5fd83b125263d055b95c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360863"
---
# <a name="esentsecondaryindexcorruptedexception-class"></a><span data-ttu-id="af0ac-103">Esentsecondaryindexverdertedexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="af0ac-103">EsentSecondaryIndexCorruptedException class</span></span>

<span data-ttu-id="af0ac-104">Basisklasse für JET_err. Secondaryindexbeschädigte-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="af0ac-104">Base class for JET_err.SecondaryIndexCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="af0ac-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="af0ac-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="af0ac-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="af0ac-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="af0ac-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="af0ac-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="af0ac-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="af0ac-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="af0ac-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="af0ac-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="af0ac-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="af0ac-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="af0ac-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="af0ac-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="af0ac-112">Microsoft. ISAM. ESENT. Interop. esentsecondaryindexverdertedexception</span><span class="sxs-lookup"><span data-stu-id="af0ac-112">Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException</span></span>  

<span data-ttu-id="af0ac-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="af0ac-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="af0ac-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="af0ac-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="af0ac-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="af0ac-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSecondaryIndexCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentSecondaryIndexCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSecondaryIndexCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="af0ac-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="af0ac-116">Thread safety</span></span>

<span data-ttu-id="af0ac-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="af0ac-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="af0ac-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="af0ac-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="af0ac-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af0ac-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="af0ac-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="af0ac-120">Reference</span></span>

[<span data-ttu-id="af0ac-121">Esentsecondaryindexverdertedexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="af0ac-121">EsentSecondaryIndexCorruptedException members</span></span>](./esentsecondaryindexcorruptedexception-members.md)

[<span data-ttu-id="af0ac-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="af0ac-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
