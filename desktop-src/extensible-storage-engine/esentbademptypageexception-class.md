---
description: 'Weitere Informationen finden Sie unter: esentbademptypageexception-Klasse'
title: Esentbademptypageexception-Klasse
TOCTitle: EsentBadEmptyPageException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbademptypageexception(v=EXCHG.10)
ms:contentKeyID: 55101115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 144f42c42eaf3ccb804344214d396cd8ac2f8aa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217275"
---
# <a name="esentbademptypageexception-class"></a><span data-ttu-id="0c3c1-103">Esentbademptypageexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="0c3c1-103">EsentBadEmptyPageException class</span></span>

<span data-ttu-id="0c3c1-104">Basisklasse für JET_err. "Bademptypage"-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="0c3c1-104">Base class for JET_err.BadEmptyPage exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0c3c1-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="0c3c1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0c3c1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0c3c1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0c3c1-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="0c3c1-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0c3c1-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="0c3c1-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0c3c1-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="0c3c1-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0c3c1-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="0c3c1-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="0c3c1-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="0c3c1-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="0c3c1-112">Microsoft. ISAM. ESENT. Interop. esentbademptypageexception</span><span class="sxs-lookup"><span data-stu-id="0c3c1-112">Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException</span></span>  

<span data-ttu-id="0c3c1-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c3c1-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c3c1-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0c3c1-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c3c1-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c3c1-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadEmptyPageException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentBadEmptyPageException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadEmptyPageException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="0c3c1-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="0c3c1-116">Thread safety</span></span>

<span data-ttu-id="0c3c1-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="0c3c1-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0c3c1-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="0c3c1-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c3c1-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c3c1-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c3c1-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="0c3c1-120">Reference</span></span>

[<span data-ttu-id="0c3c1-121">Esentbademptypageexception-Member</span><span class="sxs-lookup"><span data-stu-id="0c3c1-121">EsentBadEmptyPageException members</span></span>](./esentbademptypageexception-members.md)

[<span data-ttu-id="0c3c1-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="0c3c1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
