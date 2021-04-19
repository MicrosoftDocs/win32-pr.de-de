---
description: 'Weitere Informationen finden Sie unter: esentattacheddatabasemismatchexception-Klasse'
title: Esentattacheddatabasemismatchexception-Klasse
TOCTitle: EsentAttachedDatabaseMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentattacheddatabasemismatchexception(v=EXCHG.10)
ms:contentKeyID: 55101019
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fca9c0dcb7526df0373cbf26099a8ca810ab3eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346888"
---
# <a name="esentattacheddatabasemismatchexception-class"></a><span data-ttu-id="9c809-103">Esentattacheddatabasemismatchexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="9c809-103">EsentAttachedDatabaseMismatchException class</span></span>

<span data-ttu-id="9c809-104">Basisklasse für JET_err. "Attacheddatabasemismatch"-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="9c809-104">Base class for JET_err.AttachedDatabaseMismatch exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="9c809-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="9c809-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="9c809-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="9c809-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="9c809-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="9c809-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="9c809-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="9c809-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="9c809-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="9c809-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="9c809-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="9c809-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="9c809-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="9c809-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="9c809-112">Microsoft. ISAM. ESENT. Interop. esentattacheddatabasemismatchexception</span><span class="sxs-lookup"><span data-stu-id="9c809-112">Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException</span></span>  

<span data-ttu-id="9c809-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9c809-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9c809-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9c809-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9c809-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c809-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentAttachedDatabaseMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentAttachedDatabaseMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentAttachedDatabaseMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="9c809-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="9c809-116">Thread safety</span></span>

<span data-ttu-id="9c809-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="9c809-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="9c809-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="9c809-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c809-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c809-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9c809-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="9c809-120">Reference</span></span>

[<span data-ttu-id="9c809-121">Esentattacheddatabasemismatchexception-Member</span><span class="sxs-lookup"><span data-stu-id="9c809-121">EsentAttachedDatabaseMismatchException members</span></span>](./esentattacheddatabasemismatchexception-members.md)

[<span data-ttu-id="9c809-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9c809-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
