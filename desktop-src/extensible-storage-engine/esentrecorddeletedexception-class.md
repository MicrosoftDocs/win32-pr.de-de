---
description: 'Weitere Informationen finden Sie unter: esentrecorddeletedexception-Klasse'
title: Esentrecorddeletedexception-Klasse
TOCTitle: EsentRecordDeletedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordDeletedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecorddeletedexception(v=EXCHG.10)
ms:contentKeyID: 55107344
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordDeletedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordDeletedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61d09fca2e154f0a5c5e9e64b85b6a855c460593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959376"
---
# <a name="esentrecorddeletedexception-class"></a><span data-ttu-id="01545-103">Esentrecorddeletedexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="01545-103">EsentRecordDeletedException class</span></span>

<span data-ttu-id="01545-104">Basisklasse für JET_err. RecordDeleted-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="01545-104">Base class for JET_err.RecordDeleted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="01545-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="01545-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="01545-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="01545-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="01545-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="01545-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="01545-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="01545-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="01545-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="01545-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="01545-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="01545-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="01545-111">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="01545-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="01545-112">Microsoft. ISAM. ESENT. Interop. esentrecorddeletedexception</span><span class="sxs-lookup"><span data-stu-id="01545-112">Microsoft.Isam.Esent.Interop.EsentRecordDeletedException</span></span>  

<span data-ttu-id="01545-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="01545-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="01545-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="01545-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="01545-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="01545-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordDeletedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecordDeletedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordDeletedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="01545-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="01545-116">Thread safety</span></span>

<span data-ttu-id="01545-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="01545-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="01545-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="01545-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="01545-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01545-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="01545-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="01545-120">Reference</span></span>

[<span data-ttu-id="01545-121">Esentrecorddeletedexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="01545-121">EsentRecordDeletedException members</span></span>](./esentrecorddeletedexception-members.md)

[<span data-ttu-id="01545-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="01545-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
