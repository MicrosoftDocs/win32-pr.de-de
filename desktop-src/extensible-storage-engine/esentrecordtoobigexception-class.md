---
description: 'Weitere Informationen finden Sie unter: esentrecorddeobigexception-Klasse'
title: Esentrecorddeobigexception-Klasse
TOCTitle: EsentRecordTooBigException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordTooBigException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordtoobigexception(v=EXCHG.10)
ms:contentKeyID: 55107350
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordTooBigException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordTooBigException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c252b8c3c5fdf8a78a0a971b24065d1cb8c92152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128684"
---
# <a name="esentrecordtoobigexception-class"></a><span data-ttu-id="ad066-103">Esentrecorddeobigexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="ad066-103">EsentRecordTooBigException class</span></span>

<span data-ttu-id="ad066-104">Basisklasse für JET_err. Recordteobig-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="ad066-104">Base class for JET_err.RecordTooBig exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ad066-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="ad066-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ad066-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ad066-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ad066-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ad066-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ad066-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="ad066-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ad066-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="ad066-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ad066-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="ad066-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="ad066-111">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="ad066-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="ad066-112">Microsoft. ISAM. ESENT. Interop. esentrecorddeobigexception</span><span class="sxs-lookup"><span data-stu-id="ad066-112">Microsoft.Isam.Esent.Interop.EsentRecordTooBigException</span></span>  

<span data-ttu-id="ad066-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ad066-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ad066-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ad066-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ad066-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad066-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordTooBigException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecordTooBigException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordTooBigException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="ad066-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="ad066-116">Thread safety</span></span>

<span data-ttu-id="ad066-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="ad066-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ad066-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="ad066-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad066-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad066-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ad066-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="ad066-120">Reference</span></span>

[<span data-ttu-id="ad066-121">Esentrecorddeobigexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="ad066-121">EsentRecordTooBigException members</span></span>](./esentrecordtoobigexception-members.md)

[<span data-ttu-id="ad066-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ad066-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
