---
description: 'Weitere Informationen finden Sie unter: esentlogsequenceendexception-Klasse'
title: Esentlogsequenceendexception-Klasse
TOCTitle: EsentLogSequenceEndException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogsequenceendexception(v=EXCHG.10)
ms:contentKeyID: 55102213
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 78de803d31d8e97f9493d605d688916501edba6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215255"
---
# <a name="esentlogsequenceendexception-class"></a><span data-ttu-id="8c2ce-103">Esentlogsequenceendexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="8c2ce-103">EsentLogSequenceEndException class</span></span>

<span data-ttu-id="8c2ce-104">Basisklasse für JET_err. Logsequenceend-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="8c2ce-104">Base class for JET_err.LogSequenceEnd exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8c2ce-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="8c2ce-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8c2ce-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8c2ce-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8c2ce-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="8c2ce-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8c2ce-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="8c2ce-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8c2ce-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="8c2ce-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8c2ce-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="8c2ce-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="8c2ce-111">Microsoft. ISAM. ESENT. Interop. esentfragmentationexception</span><span class="sxs-lookup"><span data-stu-id="8c2ce-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="8c2ce-112">Microsoft. ISAM. ESENT. Interop. esentlogsequenceendexception</span><span class="sxs-lookup"><span data-stu-id="8c2ce-112">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException</span></span>  

<span data-ttu-id="8c2ce-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8c2ce-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8c2ce-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8c2ce-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8c2ce-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c2ce-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogSequenceEndException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentLogSequenceEndException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogSequenceEndException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="8c2ce-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="8c2ce-116">Thread safety</span></span>

<span data-ttu-id="8c2ce-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="8c2ce-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8c2ce-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="8c2ce-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c2ce-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c2ce-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8c2ce-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="8c2ce-120">Reference</span></span>

[<span data-ttu-id="8c2ce-121">Esentlogsequenceendexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="8c2ce-121">EsentLogSequenceEndException members</span></span>](./esentlogsequenceendexception-members.md)

[<span data-ttu-id="8c2ce-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8c2ce-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
