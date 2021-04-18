---
description: 'Weitere Informationen finden Sie unter: esentlogschreitefailexception-Klasse'
title: Esentlogschreitefailexception-Klasse
TOCTitle: EsentLogWriteFailException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogWriteFailException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogwritefailexception(v=EXCHG.10)
ms:contentKeyID: 55102169
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogWriteFailException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogWriteFailException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9cd3fe6b541a58b7498ca4117f7ba2af7662d5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347640"
---
# <a name="esentlogwritefailexception-class"></a><span data-ttu-id="55975-103">Esentlogschreitefailexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="55975-103">EsentLogWriteFailException class</span></span>

<span data-ttu-id="55975-104">Basisklasse für JET_err. Logwrite-Fail-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="55975-104">Base class for JET_err.LogWriteFail exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="55975-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="55975-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="55975-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="55975-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="55975-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="55975-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="55975-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="55975-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="55975-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="55975-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="55975-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="55975-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="55975-111">Microsoft. ISAM. ESENT. Interop. esentioexception</span><span class="sxs-lookup"><span data-stu-id="55975-111">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>](./esentioexception-class.md)  
            <span data-ttu-id="55975-112">Microsoft. ISAM. ESENT. Interop. esentlogschreitefailexception</span><span class="sxs-lookup"><span data-stu-id="55975-112">Microsoft.Isam.Esent.Interop.EsentLogWriteFailException</span></span>  

<span data-ttu-id="55975-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="55975-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="55975-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="55975-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="55975-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="55975-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogWriteFailException _
    Inherits EsentIOException
'Usage
Dim instance As EsentLogWriteFailException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogWriteFailException : EsentIOException
```

## <a name="thread-safety"></a><span data-ttu-id="55975-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="55975-116">Thread safety</span></span>

<span data-ttu-id="55975-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="55975-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="55975-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="55975-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="55975-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55975-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55975-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="55975-120">Reference</span></span>

[<span data-ttu-id="55975-121">Esentlogschreitefailexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="55975-121">EsentLogWriteFailException members</span></span>](./esentlogwritefailexception-members.md)

[<span data-ttu-id="55975-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="55975-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
