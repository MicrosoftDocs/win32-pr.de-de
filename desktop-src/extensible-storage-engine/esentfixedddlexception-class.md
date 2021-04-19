---
description: 'Weitere Informationen finden Sie unter: esentfixedddlexception-Klasse'
title: Esentfixedddlexception-Klasse
TOCTitle: EsentFixedDDLException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFixedDDLException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfixedddlexception(v=EXCHG.10)
ms:contentKeyID: 55101723
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFixedDDLException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFixedDDLException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 181c8ba1786202290d9efa32f811f7ad92b6ad2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360081"
---
# <a name="esentfixedddlexception-class"></a><span data-ttu-id="6c0c4-103">Esentfixedddlexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="6c0c4-103">EsentFixedDDLException class</span></span>

<span data-ttu-id="6c0c4-104">Basisklasse für JET_err. Fixedddl-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-104">Base class for JET_err.FixedDDL exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="6c0c4-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="6c0c4-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="6c0c4-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="6c0c4-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="6c0c4-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="6c0c4-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="6c0c4-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="6c0c4-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="6c0c4-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="6c0c4-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="6c0c4-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="6c0c4-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="6c0c4-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="6c0c4-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="6c0c4-112">Microsoft. ISAM. ESENT. Interop. esentfixedddlexception</span><span class="sxs-lookup"><span data-stu-id="6c0c4-112">Microsoft.Isam.Esent.Interop.EsentFixedDDLException</span></span>  

<span data-ttu-id="6c0c4-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6c0c4-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6c0c4-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6c0c4-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6c0c4-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c0c4-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFixedDDLException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentFixedDDLException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFixedDDLException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="6c0c4-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="6c0c4-116">Thread safety</span></span>

<span data-ttu-id="6c0c4-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="6c0c4-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c0c4-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c0c4-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6c0c4-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="6c0c4-120">Reference</span></span>

[<span data-ttu-id="6c0c4-121">Esentfixedddlexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="6c0c4-121">EsentFixedDDLException members</span></span>](./esentfixedddlexception-members.md)

[<span data-ttu-id="6c0c4-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6c0c4-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
