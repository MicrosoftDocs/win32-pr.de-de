---
description: 'Weitere Informationen finden Sie unter: esentbackupinprogressexception-Klasse'
title: Esentbackupinprogressexception-Klasse
TOCTitle: EsentBackupInProgressException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBackupInProgressException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbackupinprogressexception(v=EXCHG.10)
ms:contentKeyID: 55101081
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBackupInProgressException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBackupInProgressException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cae492abaaeac2b4f21b2afd109f8504fdc663f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349179"
---
# <a name="esentbackupinprogressexception-class"></a><span data-ttu-id="029b0-103">Esentbackupinprogressexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="029b0-103">EsentBackupInProgressException class</span></span>

<span data-ttu-id="029b0-104">Basisklasse für JET_err. BackupInProgress-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="029b0-104">Base class for JET_err.BackupInProgress exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="029b0-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="029b0-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="029b0-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="029b0-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="029b0-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="029b0-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="029b0-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="029b0-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="029b0-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="029b0-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="029b0-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="029b0-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="029b0-111">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="029b0-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="029b0-112">Microsoft. ISAM. ESENT. Interop. esentbackupinprogressexception</span><span class="sxs-lookup"><span data-stu-id="029b0-112">Microsoft.Isam.Esent.Interop.EsentBackupInProgressException</span></span>  

<span data-ttu-id="029b0-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="029b0-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="029b0-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="029b0-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="029b0-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="029b0-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBackupInProgressException _
    Inherits EsentStateException
'Usage
Dim instance As EsentBackupInProgressException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBackupInProgressException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="029b0-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="029b0-116">Thread safety</span></span>

<span data-ttu-id="029b0-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="029b0-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="029b0-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="029b0-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="029b0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="029b0-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="029b0-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="029b0-120">Reference</span></span>

[<span data-ttu-id="029b0-121">Esentbackupinprogressexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="029b0-121">EsentBackupInProgressException members</span></span>](./esentbackupinprogressexception-members.md)

[<span data-ttu-id="029b0-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="029b0-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
