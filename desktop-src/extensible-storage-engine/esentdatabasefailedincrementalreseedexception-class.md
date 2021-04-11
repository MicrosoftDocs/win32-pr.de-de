---
description: 'Weitere Informationen finden Sie unter: esentdatabasefailedinkrementalreseedexception-Klasse'
title: Esentdatabasefailedinkrementalreseedexception-Klasse
TOCTitle: EsentDatabaseFailedIncrementalReseedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasefailedincrementalreseedexception(v=EXCHG.10)
ms:contentKeyID: 55101465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfa0f4a82e3a8936ee3e7a262f8079396b95a54a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129596"
---
# <a name="esentdatabasefailedincrementalreseedexception-class"></a><span data-ttu-id="576a6-103">Esentdatabasefailedinkrementalreseedexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="576a6-103">EsentDatabaseFailedIncrementalReseedException class</span></span>

<span data-ttu-id="576a6-104">Basisklasse für JET_err. Databasefailedinkrementalreseed-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="576a6-104">Base class for JET_err.DatabaseFailedIncrementalReseed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="576a6-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="576a6-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="576a6-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="576a6-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="576a6-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="576a6-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="576a6-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="576a6-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="576a6-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="576a6-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="576a6-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="576a6-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="576a6-111">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="576a6-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="576a6-112">Microsoft. ISAM. ESENT. Interop. esentdatabasefailedinkrementalreseedexception</span><span class="sxs-lookup"><span data-stu-id="576a6-112">Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException</span></span>  

<span data-ttu-id="576a6-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="576a6-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="576a6-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="576a6-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="576a6-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="576a6-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseFailedIncrementalReseedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseFailedIncrementalReseedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseFailedIncrementalReseedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="576a6-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="576a6-116">Thread safety</span></span>

<span data-ttu-id="576a6-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="576a6-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="576a6-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="576a6-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="576a6-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="576a6-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="576a6-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="576a6-120">Reference</span></span>

[<span data-ttu-id="576a6-121">Esentdatabasefailedinkrementalreseedexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="576a6-121">EsentDatabaseFailedIncrementalReseedException members</span></span>](./esentdatabasefailedincrementalreseedexception-members.md)

[<span data-ttu-id="576a6-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="576a6-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
