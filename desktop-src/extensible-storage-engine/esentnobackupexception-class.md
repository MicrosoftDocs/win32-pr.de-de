---
description: 'Weitere Informationen finden Sie unter: esentnobackupexception-Klasse'
title: Esentnobackupexception-Klasse
TOCTitle: EsentNoBackupException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNoBackupException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnobackupexception(v=EXCHG.10)
ms:contentKeyID: 55102284
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNoBackupException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNoBackupException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 057e9e657c14e0ae0629618e7e7b138e053c5995
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750737"
---
# <a name="esentnobackupexception-class"></a><span data-ttu-id="6fd4e-103">Esentnobackupexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="6fd4e-103">EsentNoBackupException class</span></span>

<span data-ttu-id="6fd4e-104">Basisklasse für JET_err. Nobackup-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="6fd4e-104">Base class for JET_err.NoBackup exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="6fd4e-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="6fd4e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="6fd4e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="6fd4e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="6fd4e-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="6fd4e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="6fd4e-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="6fd4e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="6fd4e-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="6fd4e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="6fd4e-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="6fd4e-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="6fd4e-111">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="6fd4e-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="6fd4e-112">Microsoft. ISAM. ESENT. Interop. esentnobackupexception</span><span class="sxs-lookup"><span data-stu-id="6fd4e-112">Microsoft.Isam.Esent.Interop.EsentNoBackupException</span></span>  

<span data-ttu-id="6fd4e-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6fd4e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6fd4e-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6fd4e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6fd4e-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fd4e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNoBackupException _
    Inherits EsentStateException
'Usage
Dim instance As EsentNoBackupException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNoBackupException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="6fd4e-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="6fd4e-116">Thread safety</span></span>

<span data-ttu-id="6fd4e-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="6fd4e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="6fd4e-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="6fd4e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="6fd4e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fd4e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6fd4e-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="6fd4e-120">Reference</span></span>

[<span data-ttu-id="6fd4e-121">Esentnobackupexception-Member</span><span class="sxs-lookup"><span data-stu-id="6fd4e-121">EsentNoBackupException members</span></span>](./esentnobackupexception-members.md)

[<span data-ttu-id="6fd4e-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6fd4e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
