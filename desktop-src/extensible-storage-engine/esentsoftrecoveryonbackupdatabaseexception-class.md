---
description: 'Weitere Informationen finden Sie unter: esentsoftrecoveryonbackupdatabaseexception-Klasse'
title: Esentsoftrecoveryonbackupdatabaseexception-Klasse
TOCTitle: EsentSoftRecoveryOnBackupDatabaseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnBackupDatabaseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsoftrecoveryonbackupdatabaseexception(v=EXCHG.10)
ms:contentKeyID: 55102863
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnBackupDatabaseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnBackupDatabaseException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e68aba29c7dccfdc715c3db94eddfd35e3ef66d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362537"
---
# <a name="esentsoftrecoveryonbackupdatabaseexception-class"></a><span data-ttu-id="9fb52-103">Esentsoftrecoveryonbackupdatabaseexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="9fb52-103">EsentSoftRecoveryOnBackupDatabaseException class</span></span>

<span data-ttu-id="9fb52-104">Basisklasse für JET_err. Softrecoveryonbackupdatabase-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="9fb52-104">Base class for JET_err.SoftRecoveryOnBackupDatabase exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="9fb52-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="9fb52-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="9fb52-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="9fb52-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="9fb52-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="9fb52-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="9fb52-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="9fb52-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="9fb52-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="9fb52-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="9fb52-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="9fb52-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="9fb52-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="9fb52-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="9fb52-112">Microsoft. ISAM. ESENT. Interop. esentsoftrecoveryonbackupdatabaseexception</span><span class="sxs-lookup"><span data-stu-id="9fb52-112">Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnBackupDatabaseException</span></span>  

<span data-ttu-id="9fb52-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9fb52-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9fb52-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9fb52-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb52-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fb52-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSoftRecoveryOnBackupDatabaseException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSoftRecoveryOnBackupDatabaseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSoftRecoveryOnBackupDatabaseException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="9fb52-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="9fb52-116">Thread safety</span></span>

<span data-ttu-id="9fb52-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="9fb52-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="9fb52-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="9fb52-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="9fb52-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fb52-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9fb52-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="9fb52-120">Reference</span></span>

[<span data-ttu-id="9fb52-121">Esentsoftrecoveryonbackupdatabaseexception-Member</span><span class="sxs-lookup"><span data-stu-id="9fb52-121">EsentSoftRecoveryOnBackupDatabaseException members</span></span>](./esentsoftrecoveryonbackupdatabaseexception-members.md)

[<span data-ttu-id="9fb52-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9fb52-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
