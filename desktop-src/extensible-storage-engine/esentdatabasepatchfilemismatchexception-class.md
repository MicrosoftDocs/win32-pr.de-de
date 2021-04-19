---
description: 'Weitere Informationen finden Sie unter: esentdatabasepatchfilemismatchexception-Klasse'
title: Esentdatabasepatchfilemismatchexception-Klasse
TOCTitle: EsentDatabasePatchFileMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabasePatchFileMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasepatchfilemismatchexception(v=EXCHG.10)
ms:contentKeyID: 55101536
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabasePatchFileMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabasePatchFileMismatchException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b16d8d33dc6db26e88e5e0e5ccabb667a333e8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349114"
---
# <a name="esentdatabasepatchfilemismatchexception-class"></a><span data-ttu-id="ce008-103">Esentdatabasepatchfilemismatchexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="ce008-103">EsentDatabasePatchFileMismatchException class</span></span>

<span data-ttu-id="ce008-104">Basisklasse für JET_err. Databasepatchfilemismatch-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="ce008-104">Base class for JET_err.DatabasePatchFileMismatch exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ce008-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="ce008-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ce008-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ce008-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ce008-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ce008-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ce008-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="ce008-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ce008-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="ce008-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ce008-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="ce008-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="ce008-111">Microsoft. ISAM. ESENT. Interop. esentobsoleteexception</span><span class="sxs-lookup"><span data-stu-id="ce008-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="ce008-112">Microsoft. ISAM. ESENT. Interop. esentdatabasepatchfilemismatchexception</span><span class="sxs-lookup"><span data-stu-id="ce008-112">Microsoft.Isam.Esent.Interop.EsentDatabasePatchFileMismatchException</span></span>  

<span data-ttu-id="ce008-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ce008-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ce008-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ce008-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ce008-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce008-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabasePatchFileMismatchException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDatabasePatchFileMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabasePatchFileMismatchException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="ce008-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="ce008-116">Thread safety</span></span>

<span data-ttu-id="ce008-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="ce008-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ce008-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="ce008-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce008-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce008-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ce008-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="ce008-120">Reference</span></span>

[<span data-ttu-id="ce008-121">Esentdatabasepatchfilemismatchexception-Member</span><span class="sxs-lookup"><span data-stu-id="ce008-121">EsentDatabasePatchFileMismatchException members</span></span>](./esentdatabasepatchfilemismatchexception-members.md)

[<span data-ttu-id="ce008-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ce008-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
