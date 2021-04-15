---
description: 'Weitere Informationen finden Sie unter: esentdatabasein completeinkrementalreseedexception-Klasse'
title: Esentdatabaseingecompleteinkrementalreseedexception-Klasse
TOCTitle: EsentDatabaseIncompleteIncrementalReseedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseincompleteincrementalreseedexception(v=EXCHG.10)
ms:contentKeyID: 55101478
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 65d660c28f9b876e0cb2016631a4a8108a52b6dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526642"
---
# <a name="esentdatabaseincompleteincrementalreseedexception-class"></a><span data-ttu-id="ca4dd-103">Esentdatabaseingecompleteinkrementalreseedexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="ca4dd-103">EsentDatabaseIncompleteIncrementalReseedException class</span></span>

<span data-ttu-id="ca4dd-104">Basisklasse für JET_err. Databaseingecompleteinkrementalreseed-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-104">Base class for JET_err.DatabaseIncompleteIncrementalReseed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ca4dd-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="ca4dd-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ca4dd-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ca4dd-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ca4dd-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ca4dd-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ca4dd-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="ca4dd-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ca4dd-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="ca4dd-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ca4dd-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="ca4dd-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="ca4dd-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="ca4dd-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="ca4dd-112">Microsoft. ISAM. ESENT. Interop. esentdatabasincompleteinkrementalreseedexception</span><span class="sxs-lookup"><span data-stu-id="ca4dd-112">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException</span></span>  

<span data-ttu-id="ca4dd-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ca4dd-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ca4dd-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ca4dd-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ca4dd-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca4dd-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseIncompleteIncrementalReseedException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentDatabaseIncompleteIncrementalReseedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseIncompleteIncrementalReseedException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="ca4dd-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="ca4dd-116">Thread safety</span></span>

<span data-ttu-id="ca4dd-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ca4dd-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca4dd-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca4dd-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ca4dd-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="ca4dd-120">Reference</span></span>

[<span data-ttu-id="ca4dd-121">Esentdatabaseingecompleteinkrementalreseedexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="ca4dd-121">EsentDatabaseIncompleteIncrementalReseedException members</span></span>](./esentdatabaseincompleteincrementalreseedexception-members.md)

[<span data-ttu-id="ca4dd-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ca4dd-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
