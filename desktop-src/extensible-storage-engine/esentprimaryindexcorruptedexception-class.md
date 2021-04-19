---
description: 'Weitere Informationen finden Sie unter: esentprimaryindexverdertedexception-Klasse'
title: Esentprimaryindexverdertedexception-Klasse
TOCTitle: EsentPrimaryIndexCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentprimaryindexcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55102484
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a2d95d50e7cb8ba7bb962686e3c452c35c3b295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364207"
---
# <a name="esentprimaryindexcorruptedexception-class"></a><span data-ttu-id="aa6bd-103">Esentprimaryindexverdertedexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="aa6bd-103">EsentPrimaryIndexCorruptedException class</span></span>

<span data-ttu-id="aa6bd-104">Basisklasse für JET_err. Primaryindexbeschädigte-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="aa6bd-104">Base class for JET_err.PrimaryIndexCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="aa6bd-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="aa6bd-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="aa6bd-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="aa6bd-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="aa6bd-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="aa6bd-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="aa6bd-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="aa6bd-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="aa6bd-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="aa6bd-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="aa6bd-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="aa6bd-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="aa6bd-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="aa6bd-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="aa6bd-112">Microsoft. ISAM. ESENT. Interop. esentprimaryindexverdertedexception</span><span class="sxs-lookup"><span data-stu-id="aa6bd-112">Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException</span></span>  

<span data-ttu-id="aa6bd-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aa6bd-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aa6bd-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aa6bd-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aa6bd-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa6bd-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPrimaryIndexCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentPrimaryIndexCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPrimaryIndexCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="aa6bd-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="aa6bd-116">Thread safety</span></span>

<span data-ttu-id="aa6bd-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="aa6bd-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="aa6bd-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="aa6bd-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa6bd-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa6bd-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aa6bd-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="aa6bd-120">Reference</span></span>

[<span data-ttu-id="aa6bd-121">Esentprimaryindexverdertedexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="aa6bd-121">EsentPrimaryIndexCorruptedException members</span></span>](./esentprimaryindexcorruptedexception-members.md)

[<span data-ttu-id="aa6bd-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="aa6bd-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
