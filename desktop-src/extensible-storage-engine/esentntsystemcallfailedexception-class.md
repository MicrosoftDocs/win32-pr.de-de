---
description: 'Weitere Informationen finden Sie unter: esentntsystemcallfailedexception-Klasse'
title: Esentntsystemcallfailedexception-Klasse
TOCTitle: EsentNTSystemCallFailedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentntsystemcallfailedexception(v=EXCHG.10)
ms:contentKeyID: 55102309
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 87ebb646a4746b86343772ff7fa509a2b99f0965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218764"
---
# <a name="esentntsystemcallfailedexception-class"></a><span data-ttu-id="34de7-103">Esentntsystemcallfailedexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="34de7-103">EsentNTSystemCallFailedException class</span></span>

<span data-ttu-id="34de7-104">Basisklasse für JET_err. Ntsystemcallfailed-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="34de7-104">Base class for JET_err.NTSystemCallFailed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="34de7-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="34de7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="34de7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="34de7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="34de7-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="34de7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="34de7-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="34de7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="34de7-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="34de7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="34de7-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="34de7-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="34de7-111">Microsoft. ISAM. ESENT. Interop. esentntsystemcallfailedexception</span><span class="sxs-lookup"><span data-stu-id="34de7-111">Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException</span></span>  

<span data-ttu-id="34de7-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="34de7-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="34de7-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="34de7-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="34de7-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="34de7-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNTSystemCallFailedException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentNTSystemCallFailedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNTSystemCallFailedException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="34de7-115">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="34de7-115">Thread safety</span></span>

<span data-ttu-id="34de7-116">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="34de7-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="34de7-117">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="34de7-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="34de7-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34de7-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="34de7-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="34de7-119">Reference</span></span>

[<span data-ttu-id="34de7-120">Esentntsystemcallfailedexception-Member</span><span class="sxs-lookup"><span data-stu-id="34de7-120">EsentNTSystemCallFailedException members</span></span>](./esentntsystemcallfailedexception-members.md)

[<span data-ttu-id="34de7-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="34de7-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
