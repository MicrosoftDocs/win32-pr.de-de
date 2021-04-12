---
description: 'Weitere Informationen finden Sie unter: esentdatabasesharingviolationexception-Klasse'
title: Esentdatabasesharingviolationexception-Klasse
TOCTitle: EsentDatabaseSharingViolationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseSharingViolationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasesharingviolationexception(v=EXCHG.10)
ms:contentKeyID: 55101436
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseSharingViolationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseSharingViolationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 03d168a0235cdc31cd8e4420924f5f8b2dae90dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215290"
---
# <a name="esentdatabasesharingviolationexception-class"></a><span data-ttu-id="b7e48-103">Esentdatabasesharingviolationexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="b7e48-103">EsentDatabaseSharingViolationException class</span></span>

<span data-ttu-id="b7e48-104">Basisklasse für JET_err. Databasesharingverletzungs-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="b7e48-104">Base class for JET_err.DatabaseSharingViolation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b7e48-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="b7e48-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b7e48-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b7e48-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b7e48-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b7e48-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b7e48-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="b7e48-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b7e48-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="b7e48-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b7e48-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="b7e48-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b7e48-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="b7e48-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="b7e48-112">Microsoft. ISAM. ESENT. Interop. esentdatabasesharingviolationexception</span><span class="sxs-lookup"><span data-stu-id="b7e48-112">Microsoft.Isam.Esent.Interop.EsentDatabaseSharingViolationException</span></span>  

<span data-ttu-id="b7e48-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b7e48-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b7e48-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b7e48-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e48-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7e48-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseSharingViolationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseSharingViolationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseSharingViolationException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="b7e48-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="b7e48-116">Thread safety</span></span>

<span data-ttu-id="b7e48-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="b7e48-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b7e48-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="b7e48-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7e48-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7e48-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b7e48-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="b7e48-120">Reference</span></span>

[<span data-ttu-id="b7e48-121">Esentdatabasesharingviolationexception-Member</span><span class="sxs-lookup"><span data-stu-id="b7e48-121">EsentDatabaseSharingViolationException members</span></span>](./esentdatabasesharingviolationexception-members.md)

[<span data-ttu-id="b7e48-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="b7e48-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
