---
description: 'Weitere Informationen finden Sie unter: esentfixedinheritedddlexception-Klasse'
title: Esentfixedinheritedddlexception-Klasse
TOCTitle: EsentFixedInheritedDDLException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfixedinheritedddlexception(v=EXCHG.10)
ms:contentKeyID: 55101724
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43f8638b396848503819635860b7472a8af684c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354604"
---
# <a name="esentfixedinheritedddlexception-class"></a><span data-ttu-id="ad8da-103">Esentfixedinheritedddlexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="ad8da-103">EsentFixedInheritedDDLException class</span></span>

<span data-ttu-id="ad8da-104">Basisklasse für JET_err. Fixedinheritedddl-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="ad8da-104">Base class for JET_err.FixedInheritedDDL exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ad8da-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="ad8da-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ad8da-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ad8da-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ad8da-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ad8da-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ad8da-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="ad8da-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ad8da-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="ad8da-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ad8da-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="ad8da-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="ad8da-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="ad8da-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="ad8da-112">Microsoft. ISAM. ESENT. Interop. esentfixedinheritedddlexception</span><span class="sxs-lookup"><span data-stu-id="ad8da-112">Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException</span></span>  

<span data-ttu-id="ad8da-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ad8da-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ad8da-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ad8da-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ad8da-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad8da-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFixedInheritedDDLException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentFixedInheritedDDLException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFixedInheritedDDLException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="ad8da-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="ad8da-116">Thread safety</span></span>

<span data-ttu-id="ad8da-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="ad8da-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ad8da-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="ad8da-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad8da-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad8da-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ad8da-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="ad8da-120">Reference</span></span>

[<span data-ttu-id="ad8da-121">Esentfixedinheritedddlexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="ad8da-121">EsentFixedInheritedDDLException members</span></span>](./esentfixedinheritedddlexception-members.md)

[<span data-ttu-id="ad8da-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ad8da-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
