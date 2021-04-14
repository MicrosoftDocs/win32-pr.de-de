---
description: 'Weitere Informationen finden Sie unter: esentdatabaseleakinspaceexception-Klasse'
title: Esentdatabaseleakinspaceexception-Klasse
TOCTitle: EsentDatabaseLeakInSpaceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseleakinspaceexception(v=EXCHG.10)
ms:contentKeyID: 55101407
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51c011fb1cf3c1dc7ebcade5d88dc2cbce66351b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527095"
---
# <a name="esentdatabaseleakinspaceexception-class"></a><span data-ttu-id="d6045-103">Esentdatabaseleakinspaceexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="d6045-103">EsentDatabaseLeakInSpaceException class</span></span>

<span data-ttu-id="d6045-104">Basisklasse für JET_err. Databaseleakinspace-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="d6045-104">Base class for JET_err.DatabaseLeakInSpace exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d6045-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="d6045-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d6045-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d6045-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d6045-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d6045-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d6045-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="d6045-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d6045-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="d6045-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d6045-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="d6045-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="d6045-111">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="d6045-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="d6045-112">Microsoft. ISAM. ESENT. Interop. esentdatabaseleakinspaceexception</span><span class="sxs-lookup"><span data-stu-id="d6045-112">Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException</span></span>  

<span data-ttu-id="d6045-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d6045-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d6045-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d6045-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d6045-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6045-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseLeakInSpaceException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseLeakInSpaceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseLeakInSpaceException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="d6045-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="d6045-116">Thread safety</span></span>

<span data-ttu-id="d6045-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="d6045-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d6045-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="d6045-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6045-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6045-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d6045-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="d6045-120">Reference</span></span>

[<span data-ttu-id="d6045-121">Esentdatabaseleakinspaceexception-Member</span><span class="sxs-lookup"><span data-stu-id="d6045-121">EsentDatabaseLeakInSpaceException members</span></span>](./esentdatabaseleakinspaceexception-members.md)

[<span data-ttu-id="d6045-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="d6045-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
