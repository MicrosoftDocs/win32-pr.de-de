---
description: 'Weitere Informationen finden Sie unter: esentdatabasealleseryrunningmaintenanceexception-Klasse'
title: Esentdatabasealleseryrunningmaintenanceexception-Klasse
TOCTitle: EsentDatabaseAlreadyRunningMaintenanceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyRunningMaintenanceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasealreadyrunningmaintenanceexception(v=EXCHG.10)
ms:contentKeyID: 55101317
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyRunningMaintenanceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyRunningMaintenanceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c9f9f65df8db69762f6ec6bca72ad3903cd72ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128256"
---
# <a name="esentdatabasealreadyrunningmaintenanceexception-class"></a><span data-ttu-id="09c40-103">Esentdatabasealleseryrunningmaintenanceexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="09c40-103">EsentDatabaseAlreadyRunningMaintenanceException class</span></span>

<span data-ttu-id="09c40-104">Basisklasse für JET_err. Databaseallelerunningmaintenance-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="09c40-104">Base class for JET_err.DatabaseAlreadyRunningMaintenance exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="09c40-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="09c40-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="09c40-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="09c40-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="09c40-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="09c40-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="09c40-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="09c40-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="09c40-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="09c40-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="09c40-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="09c40-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="09c40-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="09c40-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="09c40-112">Microsoft. ISAM. ESENT. Interop. esentdatabasealleseryrunningmaintenanceexception</span><span class="sxs-lookup"><span data-stu-id="09c40-112">Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyRunningMaintenanceException</span></span>  

<span data-ttu-id="09c40-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="09c40-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="09c40-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="09c40-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="09c40-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="09c40-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseAlreadyRunningMaintenanceException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseAlreadyRunningMaintenanceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseAlreadyRunningMaintenanceException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="09c40-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="09c40-116">Thread safety</span></span>

<span data-ttu-id="09c40-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="09c40-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="09c40-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="09c40-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="09c40-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09c40-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="09c40-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="09c40-120">Reference</span></span>

[<span data-ttu-id="09c40-121">Esentdatabasealleseryrunningmaintenanceexception-Member</span><span class="sxs-lookup"><span data-stu-id="09c40-121">EsentDatabaseAlreadyRunningMaintenanceException members</span></span>](./esentdatabasealreadyrunningmaintenanceexception-members.md)

[<span data-ttu-id="09c40-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="09c40-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
