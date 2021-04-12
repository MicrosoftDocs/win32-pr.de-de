---
description: 'Weitere Informationen finden Sie unter: EsentDecompressionFailedException-Klasse'
title: EsentDecompressionFailedException-Klasse
TOCTitle: EsentDecompressionFailedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDecompressionFailedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdecompressionfailedexception(v=EXCHG.10)
ms:contentKeyID: 55101587
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDecompressionFailedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDecompressionFailedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 185f224883e3e2850e4a94c53c49d19a165528ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130909"
---
# <a name="esentdecompressionfailedexception-class"></a><span data-ttu-id="f1930-103">EsentDecompressionFailedException-Klasse</span><span class="sxs-lookup"><span data-stu-id="f1930-103">EsentDecompressionFailedException class</span></span>

<span data-ttu-id="f1930-104">Basisklasse für JET_err. Fehler bei der Debug-Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="f1930-104">Base class for JET_err.DecompressionFailed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f1930-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="f1930-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f1930-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f1930-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f1930-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f1930-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f1930-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="f1930-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f1930-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="f1930-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f1930-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="f1930-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="f1930-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="f1930-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="f1930-112">Microsoft. ISAM. ESENT. Interop. EsentDecompressionFailedException</span><span class="sxs-lookup"><span data-stu-id="f1930-112">Microsoft.Isam.Esent.Interop.EsentDecompressionFailedException</span></span>  

<span data-ttu-id="f1930-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f1930-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f1930-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f1930-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f1930-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1930-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDecompressionFailedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentDecompressionFailedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDecompressionFailedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="f1930-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="f1930-116">Thread safety</span></span>

<span data-ttu-id="f1930-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="f1930-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f1930-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="f1930-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1930-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1930-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f1930-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="f1930-120">Reference</span></span>

[<span data-ttu-id="f1930-121">EsentDecompressionFailedException-Member</span><span class="sxs-lookup"><span data-stu-id="f1930-121">EsentDecompressionFailedException members</span></span>](./esentdecompressionfailedexception-members.md)

[<span data-ttu-id="f1930-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f1930-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
