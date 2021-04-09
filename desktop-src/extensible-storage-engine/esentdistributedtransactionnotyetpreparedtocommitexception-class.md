---
description: 'Weitere Informationen finden Sie unter: esentdistributedtransaktionnotyetprepareddecommitexception-Klasse'
title: Esentdistributedtransaktionnotyetpreparedycommitexception-Klasse
TOCTitle: EsentDistributedTransactionNotYetPreparedToCommitException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdistributedtransactionnotyetpreparedtocommitexception(v=EXCHG.10)
ms:contentKeyID: 55101626
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bc118aa601559677c4b93025b9f39275b12bd89d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865331"
---
# <a name="esentdistributedtransactionnotyetpreparedtocommitexception-class"></a><span data-ttu-id="a90af-103">Esentdistributedtransaktionnotyetpreparedycommitexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="a90af-103">EsentDistributedTransactionNotYetPreparedToCommitException class</span></span>

<span data-ttu-id="a90af-104">Basisklasse für JET_err. Distributedtransaktionnotyetpreparedtcommit-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="a90af-104">Base class for JET_err.DistributedTransactionNotYetPreparedToCommit exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a90af-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="a90af-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a90af-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a90af-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a90af-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="a90af-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a90af-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="a90af-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a90af-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="a90af-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a90af-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="a90af-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="a90af-111">Microsoft. ISAM. ESENT. Interop. esentobsoleteexception</span><span class="sxs-lookup"><span data-stu-id="a90af-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="a90af-112">Microsoft. ISAM. ESENT. Interop. esentdistributedtransaktionnotyetprepareddecommitexception</span><span class="sxs-lookup"><span data-stu-id="a90af-112">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException</span></span>  

<span data-ttu-id="a90af-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a90af-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a90af-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a90af-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a90af-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="a90af-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDistributedTransactionNotYetPreparedToCommitException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDistributedTransactionNotYetPreparedToCommitException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDistributedTransactionNotYetPreparedToCommitException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="a90af-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="a90af-116">Thread safety</span></span>

<span data-ttu-id="a90af-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="a90af-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a90af-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="a90af-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a90af-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a90af-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a90af-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="a90af-120">Reference</span></span>

[<span data-ttu-id="a90af-121">Esentdistributedtransaktionnotyetpreparedtrecommitexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="a90af-121">EsentDistributedTransactionNotYetPreparedToCommitException members</span></span>](./esentdistributedtransactionnotyetpreparedtocommitexception-members.md)

[<span data-ttu-id="a90af-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="a90af-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
