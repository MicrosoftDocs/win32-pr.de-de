---
description: 'Weitere Informationen finden Sie unter: esentnotintransaktionexception-Klasse'
title: Esentnotintransaktionexception-Klasse
TOCTitle: EsentNotInTransactionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNotInTransactionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnotintransactionexception(v=EXCHG.10)
ms:contentKeyID: 55107294
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNotInTransactionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNotInTransactionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1630ecc3cea33af09c0c81be69beb9a852609f32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348038"
---
# <a name="esentnotintransactionexception-class"></a><span data-ttu-id="eac7c-103">Esentnotintransaktionexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="eac7c-103">EsentNotInTransactionException class</span></span>

<span data-ttu-id="eac7c-104">Basisklasse für JET_err. Notintransaction-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="eac7c-104">Base class for JET_err.NotInTransaction exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="eac7c-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="eac7c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="eac7c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="eac7c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="eac7c-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="eac7c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="eac7c-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="eac7c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="eac7c-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="eac7c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="eac7c-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="eac7c-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="eac7c-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="eac7c-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="eac7c-112">Microsoft. ISAM. ESENT. Interop. esentnotintransaktionexception</span><span class="sxs-lookup"><span data-stu-id="eac7c-112">Microsoft.Isam.Esent.Interop.EsentNotInTransactionException</span></span>  

<span data-ttu-id="eac7c-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eac7c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eac7c-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eac7c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eac7c-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="eac7c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNotInTransactionException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentNotInTransactionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNotInTransactionException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="eac7c-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="eac7c-116">Thread safety</span></span>

<span data-ttu-id="eac7c-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="eac7c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="eac7c-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="eac7c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="eac7c-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eac7c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eac7c-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="eac7c-120">Reference</span></span>

[<span data-ttu-id="eac7c-121">Esentnotintransaktionexception-Member</span><span class="sxs-lookup"><span data-stu-id="eac7c-121">EsentNotInTransactionException members</span></span>](./esentnotintransactionexception-members.md)

[<span data-ttu-id="eac7c-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="eac7c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
