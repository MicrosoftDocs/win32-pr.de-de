---
description: 'Weitere Informationen finden Sie unter: esentfilecloseexception-Klasse'
title: Esentfilecloseexception-Klasse
TOCTitle: EsentFileCloseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileCloseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfilecloseexception(v=EXCHG.10)
ms:contentKeyID: 55101667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileCloseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileCloseException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 357237cd6ed2210f298eccb3e76d7684ec52c0f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348675"
---
# <a name="esentfilecloseexception-class"></a><span data-ttu-id="3b809-103">Esentfilecloseexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="3b809-103">EsentFileCloseException class</span></span>

<span data-ttu-id="3b809-104">Basisklasse für JET_err. FileClose-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="3b809-104">Base class for JET_err.FileClose exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3b809-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="3b809-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3b809-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3b809-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3b809-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="3b809-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3b809-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="3b809-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3b809-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="3b809-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3b809-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="3b809-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="3b809-111">Microsoft. ISAM. ESENT. Interop. esentobsoleteexception</span><span class="sxs-lookup"><span data-stu-id="3b809-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="3b809-112">Microsoft. ISAM. ESENT. Interop. esentfilecloseexception</span><span class="sxs-lookup"><span data-stu-id="3b809-112">Microsoft.Isam.Esent.Interop.EsentFileCloseException</span></span>  

<span data-ttu-id="3b809-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3b809-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3b809-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3b809-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3b809-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b809-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileCloseException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentFileCloseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileCloseException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="3b809-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="3b809-116">Thread safety</span></span>

<span data-ttu-id="3b809-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="3b809-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3b809-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="3b809-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b809-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b809-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3b809-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="3b809-120">Reference</span></span>

[<span data-ttu-id="3b809-121">Esentfilecloseexception-Member</span><span class="sxs-lookup"><span data-stu-id="3b809-121">EsentFileCloseException members</span></span>](./esentfilecloseexception-members.md)

[<span data-ttu-id="3b809-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="3b809-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
