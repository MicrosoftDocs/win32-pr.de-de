---
description: 'Weitere Informationen finden Sie unter: esentesomanycolumnsexception-Klasse'
title: Esentyomanycolumnsexception-Klasse
TOCTitle: EsentTooManyColumnsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanycolumnsexception(v=EXCHG.10)
ms:contentKeyID: 55103051
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2191abd07aea85dac6275f3c42f34acd13376035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352687"
---
# <a name="esenttoomanycolumnsexception-class"></a><span data-ttu-id="9c4e3-103">Esentyomanycolumnsexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="9c4e3-103">EsentTooManyColumnsException class</span></span>

<span data-ttu-id="9c4e3-104">Basisklasse für JET_err. "-Ausnahmen"-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="9c4e3-104">Base class for JET_err.TooManyColumns exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="9c4e3-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="9c4e3-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="9c4e3-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="9c4e3-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="9c4e3-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="9c4e3-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="9c4e3-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="9c4e3-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="9c4e3-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="9c4e3-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="9c4e3-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="9c4e3-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="9c4e3-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="9c4e3-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="9c4e3-112">Microsoft. ISAM. ESENT. Interop. esentesomanycolumnsexception</span><span class="sxs-lookup"><span data-stu-id="9c4e3-112">Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException</span></span>  

<span data-ttu-id="9c4e3-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9c4e3-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9c4e3-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9c4e3-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9c4e3-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c4e3-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyColumnsException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyColumnsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyColumnsException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="9c4e3-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="9c4e3-116">Thread safety</span></span>

<span data-ttu-id="9c4e3-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="9c4e3-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="9c4e3-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="9c4e3-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c4e3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c4e3-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9c4e3-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="9c4e3-120">Reference</span></span>

[<span data-ttu-id="9c4e3-121">Esentesomanycolumnsexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="9c4e3-121">EsentTooManyColumnsException members</span></span>](./esenttoomanycolumnsexception-members.md)

[<span data-ttu-id="9c4e3-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9c4e3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
