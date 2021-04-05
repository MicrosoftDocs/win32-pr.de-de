---
description: 'Weitere Informationen finden Sie unter: esentdatahasangedexception-Klasse'
title: Esentdatahasangedexception-Klasse
TOCTitle: EsentDataHasChangedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDataHasChangedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatahaschangedexception(v=EXCHG.10)
ms:contentKeyID: 55101459
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDataHasChangedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataHasChangedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 003045a1aec3cf299fc24f45491424e167a18e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754840"
---
# <a name="esentdatahaschangedexception-class"></a><span data-ttu-id="4753b-103">Esentdatahasangedexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="4753b-103">EsentDataHasChangedException class</span></span>

<span data-ttu-id="4753b-104">Basisklasse für JET_err. Ausnahmen für datahasge.</span><span class="sxs-lookup"><span data-stu-id="4753b-104">Base class for JET_err.DataHasChanged exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4753b-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="4753b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4753b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4753b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4753b-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="4753b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4753b-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="4753b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4753b-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="4753b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4753b-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="4753b-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="4753b-111">Microsoft. ISAM. ESENT. Interop. esentobsoleteexception</span><span class="sxs-lookup"><span data-stu-id="4753b-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="4753b-112">Microsoft. ISAM. ESENT. Interop. esentdatahaschangedexception</span><span class="sxs-lookup"><span data-stu-id="4753b-112">Microsoft.Isam.Esent.Interop.EsentDataHasChangedException</span></span>  

<span data-ttu-id="4753b-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4753b-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4753b-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4753b-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4753b-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="4753b-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDataHasChangedException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDataHasChangedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDataHasChangedException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="4753b-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="4753b-116">Thread safety</span></span>

<span data-ttu-id="4753b-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="4753b-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4753b-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="4753b-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4753b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4753b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4753b-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="4753b-120">Reference</span></span>

[<span data-ttu-id="4753b-121">Esentdatahaschangedexception-Member</span><span class="sxs-lookup"><span data-stu-id="4753b-121">EsentDataHasChangedException members</span></span>](./esentdatahaschangedexception-members.md)

[<span data-ttu-id="4753b-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="4753b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
