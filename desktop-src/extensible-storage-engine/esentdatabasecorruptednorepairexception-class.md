---
description: 'Weitere Informationen finden Sie unter: esentdatabasecorruptednorepirexception-Klasse'
title: Esentdatabasecorruptednorepirexception-Klasse
TOCTitle: EsentDatabaseCorruptedNoRepairException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedNoRepairException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasecorruptednorepairexception(v=EXCHG.10)
ms:contentKeyID: 55101445
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedNoRepairException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedNoRepairException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1db5ebfb204e5b74a34e5fe52e7a5cc81260f194
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526657"
---
# <a name="esentdatabasecorruptednorepairexception-class"></a><span data-ttu-id="f4c1f-103">Esentdatabasecorruptednorepirexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="f4c1f-103">EsentDatabaseCorruptedNoRepairException class</span></span>

<span data-ttu-id="f4c1f-104">Basisklasse für JET_err. Databasecorruptednorepair-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="f4c1f-104">Base class for JET_err.DatabaseCorruptedNoRepair exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f4c1f-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="f4c1f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f4c1f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f4c1f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f4c1f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f4c1f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f4c1f-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="f4c1f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f4c1f-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="f4c1f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f4c1f-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="f4c1f-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f4c1f-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="f4c1f-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="f4c1f-112">Microsoft. ISAM. ESENT. Interop. esentdatabasecorruptednorepirexception</span><span class="sxs-lookup"><span data-stu-id="f4c1f-112">Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedNoRepairException</span></span>  

<span data-ttu-id="f4c1f-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f4c1f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f4c1f-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f4c1f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f4c1f-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4c1f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseCorruptedNoRepairException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseCorruptedNoRepairException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseCorruptedNoRepairException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="f4c1f-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="f4c1f-116">Thread safety</span></span>

<span data-ttu-id="f4c1f-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="f4c1f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f4c1f-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="f4c1f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4c1f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4c1f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f4c1f-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="f4c1f-120">Reference</span></span>

[<span data-ttu-id="f4c1f-121">Esentdatabasecorruptednorepirexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="f4c1f-121">EsentDatabaseCorruptedNoRepairException members</span></span>](./esentdatabasecorruptednorepairexception-members.md)

[<span data-ttu-id="f4c1f-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f4c1f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
