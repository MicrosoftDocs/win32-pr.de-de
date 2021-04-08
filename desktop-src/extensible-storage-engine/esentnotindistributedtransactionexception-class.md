---
description: 'Weitere Informationen finden Sie unter: esentnotindistributedtransaktionexception-Klasse'
title: Esentnotindistributedtransaktionexception-Klasse
TOCTitle: EsentNotInDistributedTransactionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnotindistributedtransactionexception(v=EXCHG.10)
ms:contentKeyID: 55102293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 983aa045b83a0382a3ec7676080f3cdada5e1517
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960885"
---
# <a name="esentnotindistributedtransactionexception-class"></a><span data-ttu-id="8c1f9-103">Esentnotindistributedtransaktionexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="8c1f9-103">EsentNotInDistributedTransactionException class</span></span>

<span data-ttu-id="8c1f9-104">Basisklasse für JET_err. Notindistributedtransaction-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="8c1f9-104">Base class for JET_err.NotInDistributedTransaction exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8c1f9-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="8c1f9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8c1f9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8c1f9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8c1f9-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="8c1f9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8c1f9-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="8c1f9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8c1f9-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="8c1f9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8c1f9-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="8c1f9-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="8c1f9-111">Microsoft. ISAM. ESENT. Interop. esentobsoleteexception</span><span class="sxs-lookup"><span data-stu-id="8c1f9-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="8c1f9-112">Microsoft. ISAM. ESENT. Interop. esentnotindistributedtransaktionexception</span><span class="sxs-lookup"><span data-stu-id="8c1f9-112">Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException</span></span>  

<span data-ttu-id="8c1f9-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8c1f9-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8c1f9-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8c1f9-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8c1f9-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c1f9-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNotInDistributedTransactionException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentNotInDistributedTransactionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNotInDistributedTransactionException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="8c1f9-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="8c1f9-116">Thread safety</span></span>

<span data-ttu-id="8c1f9-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="8c1f9-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8c1f9-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="8c1f9-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c1f9-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c1f9-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8c1f9-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="8c1f9-120">Reference</span></span>

[<span data-ttu-id="8c1f9-121">Esentnotindistributedtransaktionexception-Member</span><span class="sxs-lookup"><span data-stu-id="8c1f9-121">EsentNotInDistributedTransactionException members</span></span>](./esentnotindistributedtransactionexception-members.md)

[<span data-ttu-id="8c1f9-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8c1f9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
