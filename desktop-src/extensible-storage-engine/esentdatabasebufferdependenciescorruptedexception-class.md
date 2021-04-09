---
description: 'Weitere Informationen finden Sie unter: esentdatabasebufferdependenciescorruptedexception-Klasse'
title: Esentdatabasebufferdependenciescorruptedexception-Klasse
TOCTitle: EsentDatabaseBufferDependenciesCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasebufferdependenciescorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55101428
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ace9bfb553aaa04d853addd21e23df487fedd8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959707"
---
# <a name="esentdatabasebufferdependenciescorruptedexception-class"></a><span data-ttu-id="2fdf0-103">Esentdatabasebufferdependenciescorruptedexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="2fdf0-103">EsentDatabaseBufferDependenciesCorruptedException class</span></span>

<span data-ttu-id="2fdf0-104">Basisklasse für JET_err. DatabaseBufferDependenciesCorrupted-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="2fdf0-104">Base class for JET_err.DatabaseBufferDependenciesCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2fdf0-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="2fdf0-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2fdf0-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2fdf0-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2fdf0-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="2fdf0-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2fdf0-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="2fdf0-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2fdf0-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="2fdf0-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2fdf0-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="2fdf0-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="2fdf0-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="2fdf0-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="2fdf0-112">Microsoft. ISAM. ESENT. Interop. esentdatabasebufferdependenciescorruptedexception</span><span class="sxs-lookup"><span data-stu-id="2fdf0-112">Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException</span></span>  

<span data-ttu-id="2fdf0-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2fdf0-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2fdf0-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2fdf0-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2fdf0-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fdf0-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseBufferDependenciesCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentDatabaseBufferDependenciesCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseBufferDependenciesCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="2fdf0-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="2fdf0-116">Thread safety</span></span>

<span data-ttu-id="2fdf0-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="2fdf0-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2fdf0-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="2fdf0-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2fdf0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fdf0-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2fdf0-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="2fdf0-120">Reference</span></span>

[<span data-ttu-id="2fdf0-121">Esentdatabasebufferdependenciescorruptedexception-Member</span><span class="sxs-lookup"><span data-stu-id="2fdf0-121">EsentDatabaseBufferDependenciesCorruptedException members</span></span>](./esentdatabasebufferdependenciescorruptedexception-members.md)

[<span data-ttu-id="2fdf0-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="2fdf0-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
