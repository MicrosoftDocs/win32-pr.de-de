---
description: 'Weitere Informationen finden Sie unter: esentbadpatchpageexception-Klasse'
title: Esentbadpatchpageexception-Klasse
TOCTitle: EsentBadPatchPageException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadPatchPageException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadpatchpageexception(v=EXCHG.10)
ms:contentKeyID: 55101149
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadPatchPageException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadPatchPageException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b29602e327718dab63c402d075b3a7bf5695604a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759348"
---
# <a name="esentbadpatchpageexception-class"></a><span data-ttu-id="423dd-103">Esentbadpatchpageexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="423dd-103">EsentBadPatchPageException class</span></span>

<span data-ttu-id="423dd-104">Basisklasse für JET_err. Badpatchpage-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="423dd-104">Base class for JET_err.BadPatchPage exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="423dd-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="423dd-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="423dd-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="423dd-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="423dd-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="423dd-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="423dd-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="423dd-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="423dd-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="423dd-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="423dd-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="423dd-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="423dd-111">Microsoft. ISAM. ESENT. Interop. esentobsoleteexception</span><span class="sxs-lookup"><span data-stu-id="423dd-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="423dd-112">Microsoft. ISAM. ESENT. Interop. esentbadpatchpageexception</span><span class="sxs-lookup"><span data-stu-id="423dd-112">Microsoft.Isam.Esent.Interop.EsentBadPatchPageException</span></span>  

<span data-ttu-id="423dd-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="423dd-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="423dd-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="423dd-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="423dd-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="423dd-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadPatchPageException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentBadPatchPageException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadPatchPageException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="423dd-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="423dd-116">Thread safety</span></span>

<span data-ttu-id="423dd-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="423dd-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="423dd-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="423dd-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="423dd-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="423dd-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="423dd-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="423dd-120">Reference</span></span>

[<span data-ttu-id="423dd-121">Esentbadpatchpageexception-Member</span><span class="sxs-lookup"><span data-stu-id="423dd-121">EsentBadPatchPageException members</span></span>](./esentbadpatchpageexception-members.md)

[<span data-ttu-id="423dd-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="423dd-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
