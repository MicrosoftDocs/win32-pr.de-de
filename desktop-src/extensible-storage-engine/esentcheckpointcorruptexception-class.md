---
description: 'Weitere Informationen finden Sie unter: esentcheckpointbeschädigen TException-Klasse'
title: Esentcheckpointverdertexception-Klasse
TOCTitle: EsentCheckpointCorruptException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcheckpointcorruptexception(v=EXCHG.10)
ms:contentKeyID: 55101237
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0654ff85fa74cca8435ca6366e301bc3c70fc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360160"
---
# <a name="esentcheckpointcorruptexception-class"></a><span data-ttu-id="b0142-103">Esentcheckpointverdertexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="b0142-103">EsentCheckpointCorruptException class</span></span>

<span data-ttu-id="b0142-104">Basisklasse für JET_err. Checkpointbeschädigte-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="b0142-104">Base class for JET_err.CheckpointCorrupt exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b0142-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="b0142-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b0142-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b0142-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b0142-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b0142-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b0142-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="b0142-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b0142-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="b0142-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b0142-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="b0142-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="b0142-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="b0142-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="b0142-112">Microsoft. ISAM. ESENT. Interop. esentcheckpointbeschädigen TException</span><span class="sxs-lookup"><span data-stu-id="b0142-112">Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException</span></span>  

<span data-ttu-id="b0142-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b0142-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b0142-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b0142-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b0142-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0142-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCheckpointCorruptException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentCheckpointCorruptException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCheckpointCorruptException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="b0142-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="b0142-116">Thread safety</span></span>

<span data-ttu-id="b0142-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="b0142-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b0142-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="b0142-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0142-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0142-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b0142-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="b0142-120">Reference</span></span>

[<span data-ttu-id="b0142-121">Esentcheckpointbeschädigte TException-Elemente</span><span class="sxs-lookup"><span data-stu-id="b0142-121">EsentCheckpointCorruptException members</span></span>](./esentcheckpointcorruptexception-members.md)

[<span data-ttu-id="b0142-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="b0142-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
