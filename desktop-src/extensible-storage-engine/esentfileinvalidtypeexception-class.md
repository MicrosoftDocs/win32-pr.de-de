---
description: 'Weitere Informationen finden Sie unter: esentfileinvalidtypeexception-Klasse'
title: Esentfileinvalidtypeexception-Klasse
TOCTitle: EsentFileInvalidTypeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfileinvalidtypeexception(v=EXCHG.10)
ms:contentKeyID: 55107272
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2c2bf5cf30cb45734613fcabc446834085d5bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349159"
---
# <a name="esentfileinvalidtypeexception-class"></a><span data-ttu-id="a403f-103">Esentfileinvalidtypeexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="a403f-103">EsentFileInvalidTypeException class</span></span>

<span data-ttu-id="a403f-104">Basisklasse für JET_err. Fileinvalidtype-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="a403f-104">Base class for JET_err.FileInvalidType exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a403f-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="a403f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a403f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a403f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a403f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="a403f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a403f-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="a403f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a403f-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="a403f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a403f-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="a403f-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="a403f-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="a403f-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="a403f-112">Microsoft. ISAM. ESENT. Interop. esentfileinvalidtypeexception</span><span class="sxs-lookup"><span data-stu-id="a403f-112">Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException</span></span>  

<span data-ttu-id="a403f-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a403f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a403f-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a403f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a403f-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="a403f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileInvalidTypeException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentFileInvalidTypeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileInvalidTypeException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="a403f-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="a403f-116">Thread safety</span></span>

<span data-ttu-id="a403f-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="a403f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a403f-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="a403f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a403f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a403f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a403f-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="a403f-120">Reference</span></span>

[<span data-ttu-id="a403f-121">Esentfileinvalidtypeexception-Member</span><span class="sxs-lookup"><span data-stu-id="a403f-121">EsentFileInvalidTypeException members</span></span>](./esentfileinvalidtypeexception-members.md)

[<span data-ttu-id="a403f-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="a403f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
