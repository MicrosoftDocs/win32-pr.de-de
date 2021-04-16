---
description: 'Weitere Informationen finden Sie unter: esentdatabasealleseryupgradedexception-Klasse'
title: Esentdatabasealleseryupgradedexception-Klasse
TOCTitle: EsentDatabaseAlreadyUpgradedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasealreadyupgradedexception(v=EXCHG.10)
ms:contentKeyID: 55101322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27ad5a37676ef0b8e4a450619c19a45f3bdee1b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530362"
---
# <a name="esentdatabasealreadyupgradedexception-class"></a><span data-ttu-id="f05fb-103">Esentdatabasealleseryupgradedexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="f05fb-103">EsentDatabaseAlreadyUpgradedException class</span></span>

<span data-ttu-id="f05fb-104">Basisklasse für JET_err. Databasealleseryaktualisierte-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="f05fb-104">Base class for JET_err.DatabaseAlreadyUpgraded exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f05fb-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="f05fb-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f05fb-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f05fb-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f05fb-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f05fb-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f05fb-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="f05fb-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f05fb-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="f05fb-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f05fb-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="f05fb-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f05fb-111">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="f05fb-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="f05fb-112">Microsoft. ISAM. ESENT. Interop. esentdatabasealleseryupgradedexception</span><span class="sxs-lookup"><span data-stu-id="f05fb-112">Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException</span></span>  

<span data-ttu-id="f05fb-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f05fb-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f05fb-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f05fb-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f05fb-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="f05fb-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseAlreadyUpgradedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseAlreadyUpgradedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseAlreadyUpgradedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="f05fb-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="f05fb-116">Thread safety</span></span>

<span data-ttu-id="f05fb-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="f05fb-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f05fb-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="f05fb-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f05fb-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f05fb-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f05fb-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="f05fb-120">Reference</span></span>

[<span data-ttu-id="f05fb-121">Esentdatabasealleseryupgradedexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="f05fb-121">EsentDatabaseAlreadyUpgradedException members</span></span>](./esentdatabasealreadyupgradedexception-members.md)

[<span data-ttu-id="f05fb-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f05fb-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
