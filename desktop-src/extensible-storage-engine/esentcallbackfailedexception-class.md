---
description: 'Weitere Informationen finden Sie unter: esentcallbackfailedexception-Klasse'
title: Esentcallbackfailedexception-Klasse
TOCTitle: EsentCallbackFailedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCallbackFailedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcallbackfailedexception(v=EXCHG.10)
ms:contentKeyID: 55101180
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCallbackFailedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCallbackFailedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: acf8ea822cb625d28ece0c80e69eb3947cec67c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218645"
---
# <a name="esentcallbackfailedexception-class"></a><span data-ttu-id="3f7db-103">Esentcallbackfailedexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="3f7db-103">EsentCallbackFailedException class</span></span>

<span data-ttu-id="3f7db-104">Basisklasse für JET_err. Callbackfailed-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="3f7db-104">Base class for JET_err.CallbackFailed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3f7db-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="3f7db-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3f7db-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3f7db-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3f7db-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="3f7db-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3f7db-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="3f7db-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3f7db-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="3f7db-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3f7db-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="3f7db-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="3f7db-111">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="3f7db-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="3f7db-112">Microsoft. ISAM. ESENT. Interop. esentcallbackfailedexception</span><span class="sxs-lookup"><span data-stu-id="3f7db-112">Microsoft.Isam.Esent.Interop.EsentCallbackFailedException</span></span>  

<span data-ttu-id="3f7db-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3f7db-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3f7db-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3f7db-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3f7db-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f7db-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCallbackFailedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentCallbackFailedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCallbackFailedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="3f7db-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="3f7db-116">Thread safety</span></span>

<span data-ttu-id="3f7db-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="3f7db-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3f7db-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="3f7db-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f7db-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f7db-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3f7db-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="3f7db-120">Reference</span></span>

[<span data-ttu-id="3f7db-121">Esentcallbackfailedexception-Member</span><span class="sxs-lookup"><span data-stu-id="3f7db-121">EsentCallbackFailedException members</span></span>](./esentcallbackfailedexception-members.md)

[<span data-ttu-id="3f7db-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="3f7db-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
