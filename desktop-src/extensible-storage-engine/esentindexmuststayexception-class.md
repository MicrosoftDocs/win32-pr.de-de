---
description: 'Weitere Informationen finden Sie unter: esentindexmuststayexception-Klasse'
title: Esentindexmuststayexception-Klasse
TOCTitle: EsentIndexMustStayException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIndexMustStayException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentindexmuststayexception(v=EXCHG.10)
ms:contentKeyID: 55101835
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIndexMustStayException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIndexMustStayException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eeeb5949caa79d26894f5869ed31cc79ebba934d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357120"
---
# <a name="esentindexmuststayexception-class"></a><span data-ttu-id="20826-103">Esentindexmuststayexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="20826-103">EsentIndexMustStayException class</span></span>

<span data-ttu-id="20826-104">Basisklasse für JET_err. Indexmuststay-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="20826-104">Base class for JET_err.IndexMustStay exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="20826-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="20826-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="20826-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="20826-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="20826-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="20826-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="20826-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="20826-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="20826-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="20826-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="20826-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="20826-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="20826-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="20826-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="20826-112">Microsoft. ISAM. ESENT. Interop. esentindexmuststayexception</span><span class="sxs-lookup"><span data-stu-id="20826-112">Microsoft.Isam.Esent.Interop.EsentIndexMustStayException</span></span>  

<span data-ttu-id="20826-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="20826-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="20826-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="20826-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="20826-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="20826-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentIndexMustStayException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentIndexMustStayException
```

``` csharp
[SerializableAttribute]
public sealed class EsentIndexMustStayException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="20826-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="20826-116">Thread safety</span></span>

<span data-ttu-id="20826-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="20826-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="20826-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="20826-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="20826-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20826-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="20826-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="20826-120">Reference</span></span>

[<span data-ttu-id="20826-121">Esentindexmuststayexception-Member</span><span class="sxs-lookup"><span data-stu-id="20826-121">EsentIndexMustStayException members</span></span>](./esentindexmuststayexception-members.md)

[<span data-ttu-id="20826-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="20826-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
