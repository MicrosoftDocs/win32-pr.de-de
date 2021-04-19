---
description: 'Weitere Informationen finden Sie unter: esentlogverdertedexception-Klasse'
title: Esentlogverdertedexception-Klasse
TOCTitle: EsentLogCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55107292
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 962f27ee891434691531f44e400e39a19bfc98ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363353"
---
# <a name="esentlogcorruptedexception-class"></a><span data-ttu-id="65580-103">Esentlogverdertedexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="65580-103">EsentLogCorruptedException class</span></span>

<span data-ttu-id="65580-104">Basisklasse für JET_err. Logbeschädigte Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="65580-104">Base class for JET_err.LogCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="65580-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="65580-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="65580-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="65580-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="65580-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="65580-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="65580-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="65580-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="65580-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="65580-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="65580-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="65580-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="65580-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="65580-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="65580-112">Microsoft. ISAM. ESENT. Interop. esentlogkorruptedexception</span><span class="sxs-lookup"><span data-stu-id="65580-112">Microsoft.Isam.Esent.Interop.EsentLogCorruptedException</span></span>  

<span data-ttu-id="65580-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="65580-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="65580-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="65580-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="65580-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="65580-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="65580-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="65580-116">Thread safety</span></span>

<span data-ttu-id="65580-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="65580-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="65580-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="65580-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="65580-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65580-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="65580-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="65580-120">Reference</span></span>

[<span data-ttu-id="65580-121">Esentlogverdertedexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="65580-121">EsentLogCorruptedException members</span></span>](./esentlogcorruptedexception-members.md)

[<span data-ttu-id="65580-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="65580-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
