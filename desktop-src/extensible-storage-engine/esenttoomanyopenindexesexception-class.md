---
description: 'Weitere Informationen finden Sie unter: esentesomanyopenindexesexception-Klasse'
title: Esentesomanyopenindexesexception-Klasse
TOCTitle: EsentTooManyOpenIndexesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopenindexesexception(v=EXCHG.10)
ms:contentKeyID: 55103106
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 681f9a8ec67b9b9c82babcc3814833a1a3dbb0d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217879"
---
# <a name="esenttoomanyopenindexesexception-class"></a><span data-ttu-id="ac7de-103">Esentesomanyopenindexesexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="ac7de-103">EsentTooManyOpenIndexesException class</span></span>

<span data-ttu-id="ac7de-104">Basisklasse für JET_err. Ausnahmen für "-openindexes".</span><span class="sxs-lookup"><span data-stu-id="ac7de-104">Base class for JET_err.TooManyOpenIndexes exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ac7de-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="ac7de-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ac7de-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ac7de-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ac7de-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ac7de-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ac7de-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="ac7de-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ac7de-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="ac7de-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ac7de-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="ac7de-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="ac7de-111">Microsoft. ISAM. ESENT. Interop. esentresourceexception</span><span class="sxs-lookup"><span data-stu-id="ac7de-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="ac7de-112">Microsoft. ISAM. ESENT. Interop. esentmemoryexception</span><span class="sxs-lookup"><span data-stu-id="ac7de-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="ac7de-113">Microsoft. ISAM. ESENT. Interop. esentesomanyopenindexesexception</span><span class="sxs-lookup"><span data-stu-id="ac7de-113">Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException</span></span>  

<span data-ttu-id="ac7de-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ac7de-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ac7de-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ac7de-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ac7de-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac7de-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenIndexesException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentTooManyOpenIndexesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenIndexesException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="ac7de-117">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="ac7de-117">Thread safety</span></span>

<span data-ttu-id="ac7de-118">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="ac7de-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ac7de-119">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="ac7de-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac7de-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac7de-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ac7de-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="ac7de-121">Reference</span></span>

[<span data-ttu-id="ac7de-122">Esentesomanyopenindexesexception-Member</span><span class="sxs-lookup"><span data-stu-id="ac7de-122">EsentTooManyOpenIndexesException members</span></span>](./esenttoomanyopenindexesexception-members.md)

[<span data-ttu-id="ac7de-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ac7de-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
