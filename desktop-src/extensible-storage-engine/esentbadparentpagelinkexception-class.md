---
description: 'Weitere Informationen finden Sie unter: esentbadparser Exception-Klasse'
title: Esentbadparser Exception-Klasse
TOCTitle: EsentBadParentPageLinkException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadParentPageLinkException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadparentpagelinkexception(v=EXCHG.10)
ms:contentKeyID: 55101090
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadParentPageLinkException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadParentPageLinkException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffcfab55b6acda192252faeb43493dfba3978b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349644"
---
# <a name="esentbadparentpagelinkexception-class"></a><span data-ttu-id="67be4-103">Esentbadparser Exception-Klasse</span><span class="sxs-lookup"><span data-stu-id="67be4-103">EsentBadParentPageLinkException class</span></span>

<span data-ttu-id="67be4-104">Basisklasse für JET_err. Badparser-pagelink-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="67be4-104">Base class for JET_err.BadParentPageLink exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="67be4-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="67be4-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="67be4-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="67be4-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="67be4-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="67be4-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="67be4-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="67be4-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="67be4-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="67be4-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="67be4-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="67be4-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="67be4-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="67be4-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="67be4-112">Microsoft. ISAM. ESENT. Interop. esentbadparentpagelinkexception</span><span class="sxs-lookup"><span data-stu-id="67be4-112">Microsoft.Isam.Esent.Interop.EsentBadParentPageLinkException</span></span>  

<span data-ttu-id="67be4-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="67be4-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="67be4-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="67be4-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="67be4-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="67be4-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadParentPageLinkException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentBadParentPageLinkException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadParentPageLinkException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="67be4-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="67be4-116">Thread safety</span></span>

<span data-ttu-id="67be4-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="67be4-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="67be4-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="67be4-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="67be4-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67be4-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="67be4-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="67be4-120">Reference</span></span>

[<span data-ttu-id="67be4-121">Esentbadparser Exception-Member</span><span class="sxs-lookup"><span data-stu-id="67be4-121">EsentBadParentPageLinkException members</span></span>](./esentbadparentpagelinkexception-members.md)

[<span data-ttu-id="67be4-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="67be4-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
