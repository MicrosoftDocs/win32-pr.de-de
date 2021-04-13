---
description: 'Weitere Informationen finden Sie unter: esentlogdiskfullexception-Klasse'
title: Esentlogdiskfullexception-Klasse
TOCTitle: EsentLogDiskFullException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogDiskFullException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogdiskfullexception(v=EXCHG.10)
ms:contentKeyID: 55102101
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogDiskFullException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogDiskFullException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a237a8d21aab32114708a5cb59545ed827e05bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345989"
---
# <a name="esentlogdiskfullexception-class"></a><span data-ttu-id="e59ec-103">Esentlogdiskfullexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="e59ec-103">EsentLogDiskFullException class</span></span>

<span data-ttu-id="e59ec-104">Basisklasse für JET_err. Logdiskfull-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="e59ec-104">Base class for JET_err.LogDiskFull exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e59ec-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="e59ec-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e59ec-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e59ec-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e59ec-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="e59ec-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e59ec-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="e59ec-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e59ec-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="e59ec-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e59ec-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="e59ec-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="e59ec-111">Microsoft. ISAM. ESENT. Interop. esentresourceexception</span><span class="sxs-lookup"><span data-stu-id="e59ec-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="e59ec-112">Microsoft. ISAM. ESENT. Interop. esentdiskexception</span><span class="sxs-lookup"><span data-stu-id="e59ec-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>](./esentdiskexception-class.md)  
              <span data-ttu-id="e59ec-113">Microsoft. ISAM. ESENT. Interop. esentlogdiskfullexception</span><span class="sxs-lookup"><span data-stu-id="e59ec-113">Microsoft.Isam.Esent.Interop.EsentLogDiskFullException</span></span>  

<span data-ttu-id="e59ec-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e59ec-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e59ec-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e59ec-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e59ec-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="e59ec-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogDiskFullException _
    Inherits EsentDiskException
'Usage
Dim instance As EsentLogDiskFullException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogDiskFullException : EsentDiskException
```

## <a name="thread-safety"></a><span data-ttu-id="e59ec-117">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="e59ec-117">Thread safety</span></span>

<span data-ttu-id="e59ec-118">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="e59ec-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e59ec-119">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="e59ec-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e59ec-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e59ec-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e59ec-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="e59ec-121">Reference</span></span>

[<span data-ttu-id="e59ec-122">Esentlogdiskfullexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="e59ec-122">EsentLogDiskFullException members</span></span>](./esentlogdiskfullexception-members.md)

[<span data-ttu-id="e59ec-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e59ec-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
