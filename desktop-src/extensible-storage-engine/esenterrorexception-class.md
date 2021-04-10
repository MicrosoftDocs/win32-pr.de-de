---
description: 'Weitere Informationen finden Sie unter: esenterrorexception-Klasse'
title: EsentErrorException-Klasse
TOCTitle: EsentErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception(v=EXCHG.10)
ms:contentKeyID: 55101648
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb05197392c1d5c8798968254b24d2d0ae677bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042472"
---
# <a name="esenterrorexception-class"></a><span data-ttu-id="7e489-103">EsentErrorException-Klasse</span><span class="sxs-lookup"><span data-stu-id="7e489-103">EsentErrorException class</span></span>

<span data-ttu-id="7e489-104">Basisklasse für ESENT-Fehler Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="7e489-104">Base class for ESENT error exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7e489-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="7e489-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7e489-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7e489-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7e489-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="7e489-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7e489-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="7e489-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      <span data-ttu-id="7e489-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="7e489-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>  
        [<span data-ttu-id="7e489-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="7e489-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
        [<span data-ttu-id="7e489-111">Microsoft. ISAM. ESENT. Interop. esentcannotlogduringrecoveryredoexception</span><span class="sxs-lookup"><span data-stu-id="7e489-111">Microsoft.Isam.Esent.Interop.EsentCannotLogDuringRecoveryRedoException</span></span>](./esentcannotlogduringrecoveryredoexception-class.md)  
        [<span data-ttu-id="7e489-112">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="7e489-112">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
        [<span data-ttu-id="7e489-113">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="7e489-113">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
        [<span data-ttu-id="7e489-114">Microsoft. ISAM. ESENT. Interop. esentpreviousversionexception</span><span class="sxs-lookup"><span data-stu-id="7e489-114">Microsoft.Isam.Esent.Interop.EsentPreviousVersionException</span></span>](./esentpreviousversionexception-class.md)  
        [<span data-ttu-id="7e489-115">Microsoft. ISAM. ESENT. Interop. esentversionstoreentrydeobigexception</span><span class="sxs-lookup"><span data-stu-id="7e489-115">Microsoft.Isam.Esent.Interop.EsentVersionStoreEntryTooBigException</span></span>](./esentversionstoreentrytoobigexception-class.md)  

<span data-ttu-id="7e489-116">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7e489-116">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7e489-117">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7e489-117">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7e489-118">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e489-118">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Class EsentErrorException _
    Inherits EsentException
'Usage
Dim instance As EsentErrorException
```

``` csharp
[SerializableAttribute]
public class EsentErrorException : EsentException
```

## <a name="thread-safety"></a><span data-ttu-id="7e489-119">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="7e489-119">Thread safety</span></span>

<span data-ttu-id="7e489-120">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="7e489-120">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7e489-121">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="7e489-121">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e489-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e489-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7e489-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="7e489-123">Reference</span></span>

[<span data-ttu-id="7e489-124">Esenterrorexception-Member</span><span class="sxs-lookup"><span data-stu-id="7e489-124">EsentErrorException members</span></span>](./esenterrorexception-members.md)

[<span data-ttu-id="7e489-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="7e489-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
