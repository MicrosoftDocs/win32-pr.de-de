---
description: 'Weitere Informationen finden Sie unter: esentouesf buffersexception-Klasse'
title: Esentouesf buffersexception-Klasse
TOCTitle: EsentOutOfBuffersException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofbuffersexception(v=EXCHG.10)
ms:contentKeyID: 55102398
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fc8c5d22a6dc4d33d855d6d98a78e8ce7d33ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348936"
---
# <a name="esentoutofbuffersexception-class"></a><span data-ttu-id="0dd36-103">Esentouesf buffersexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="0dd36-103">EsentOutOfBuffersException class</span></span>

<span data-ttu-id="0dd36-104">Basisklasse für JET_err. Outo-Puffer-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="0dd36-104">Base class for JET_err.OutOfBuffers exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0dd36-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="0dd36-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0dd36-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0dd36-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0dd36-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="0dd36-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0dd36-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="0dd36-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0dd36-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="0dd36-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0dd36-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="0dd36-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="0dd36-111">Microsoft. ISAM. ESENT. Interop. esentresourceexception</span><span class="sxs-lookup"><span data-stu-id="0dd36-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="0dd36-112">Microsoft. ISAM. ESENT. Interop. esentmemoryexception</span><span class="sxs-lookup"><span data-stu-id="0dd36-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="0dd36-113">Microsoft. ISAM. ESENT. Interop. esentouesf buffersexception</span><span class="sxs-lookup"><span data-stu-id="0dd36-113">Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException</span></span>  

<span data-ttu-id="0dd36-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0dd36-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0dd36-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0dd36-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0dd36-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="0dd36-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfBuffersException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfBuffersException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfBuffersException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="0dd36-117">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="0dd36-117">Thread safety</span></span>

<span data-ttu-id="0dd36-118">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="0dd36-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0dd36-119">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="0dd36-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0dd36-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dd36-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0dd36-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="0dd36-121">Reference</span></span>

[<span data-ttu-id="0dd36-122">Esentouto fbuffersexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="0dd36-122">EsentOutOfBuffersException members</span></span>](./esentoutofbuffersexception-members.md)

[<span data-ttu-id="0dd36-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="0dd36-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
