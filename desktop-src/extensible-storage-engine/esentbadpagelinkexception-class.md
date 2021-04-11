---
description: 'Weitere Informationen finden Sie unter: esentbadpagelinkexception-Klasse'
title: Esentbadpagelinkexception-Klasse
TOCTitle: EsentBadPageLinkException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadPageLinkException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadpagelinkexception(v=EXCHG.10)
ms:contentKeyID: 55101138
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadPageLinkException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadPageLinkException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 308d0e220e2c39411d22622f907db6ce46013842
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217930"
---
# <a name="esentbadpagelinkexception-class"></a><span data-ttu-id="e2383-103">Esentbadpagelinkexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="e2383-103">EsentBadPageLinkException class</span></span>

<span data-ttu-id="e2383-104">Basisklasse für JET_err. Badpagelink-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="e2383-104">Base class for JET_err.BadPageLink exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e2383-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="e2383-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e2383-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e2383-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e2383-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="e2383-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e2383-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="e2383-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e2383-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="e2383-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e2383-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="e2383-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="e2383-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="e2383-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="e2383-112">Microsoft. ISAM. ESENT. Interop. esentbadpagelinkexception</span><span class="sxs-lookup"><span data-stu-id="e2383-112">Microsoft.Isam.Esent.Interop.EsentBadPageLinkException</span></span>  

<span data-ttu-id="e2383-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e2383-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e2383-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e2383-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e2383-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2383-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadPageLinkException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentBadPageLinkException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadPageLinkException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="e2383-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="e2383-116">Thread safety</span></span>

<span data-ttu-id="e2383-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="e2383-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e2383-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="e2383-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2383-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2383-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e2383-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="e2383-120">Reference</span></span>

[<span data-ttu-id="e2383-121">Esentbadpagelinkexception-Member</span><span class="sxs-lookup"><span data-stu-id="e2383-121">EsentBadPageLinkException members</span></span>](./esentbadpagelinkexception-members.md)

[<span data-ttu-id="e2383-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2383-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
