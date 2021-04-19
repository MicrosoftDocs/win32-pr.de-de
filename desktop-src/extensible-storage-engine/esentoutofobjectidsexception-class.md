---
description: 'Weitere Informationen finden Sie unter: esentouesfobjectidsexception-Klasse'
title: Esentouesfobjectidsexception-Klasse
TOCTitle: EsentOutOfObjectIDsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofobjectidsexception(v=EXCHG.10)
ms:contentKeyID: 55102436
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 18cf8d1b7c98db8f855cf970eed7be87185fc9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359459"
---
# <a name="esentoutofobjectidsexception-class"></a><span data-ttu-id="4063f-103">Esentouesfobjectidsexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="4063f-103">EsentOutOfObjectIDsException class</span></span>

<span data-ttu-id="4063f-104">Basisklasse für JET_err. Outoifobjectids-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="4063f-104">Base class for JET_err.OutOfObjectIDs exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4063f-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="4063f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4063f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4063f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4063f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="4063f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4063f-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="4063f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4063f-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="4063f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4063f-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="4063f-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="4063f-111">Microsoft. ISAM. ESENT. Interop. esentfragmentationexception</span><span class="sxs-lookup"><span data-stu-id="4063f-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="4063f-112">Microsoft. ISAM. ESENT. Interop. esentouesfobjectidsexception</span><span class="sxs-lookup"><span data-stu-id="4063f-112">Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException</span></span>  

<span data-ttu-id="4063f-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4063f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4063f-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4063f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4063f-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="4063f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfObjectIDsException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentOutOfObjectIDsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfObjectIDsException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="4063f-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="4063f-116">Thread safety</span></span>

<span data-ttu-id="4063f-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="4063f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4063f-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="4063f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4063f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4063f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4063f-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="4063f-120">Reference</span></span>

[<span data-ttu-id="4063f-121">Esentouesfobjectidsexception-Member</span><span class="sxs-lookup"><span data-stu-id="4063f-121">EsentOutOfObjectIDsException members</span></span>](./esentoutofobjectidsexception-members.md)

[<span data-ttu-id="4063f-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="4063f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
