---
description: 'Weitere Informationen finden Sie unter: esentlogtornschreiteduringhardrecoveryexception-Klasse'
title: Esentlogtornwrite teduringhardrecoveryexception-Klasse
TOCTitle: EsentLogTornWriteDuringHardRecoveryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogtornwriteduringhardrecoveryexception(v=EXCHG.10)
ms:contentKeyID: 55102218
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 96a9f286008cc6d540ebbf6c44fb31b6b0f498d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360618"
---
# <a name="esentlogtornwriteduringhardrecoveryexception-class"></a><span data-ttu-id="43c44-103">Esentlogtornwrite teduringhardrecoveryexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="43c44-103">EsentLogTornWriteDuringHardRecoveryException class</span></span>

<span data-ttu-id="43c44-104">Basisklasse für JET_err. Logtornschreiteduringhardrecovery-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="43c44-104">Base class for JET_err.LogTornWriteDuringHardRecovery exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="43c44-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="43c44-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="43c44-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="43c44-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="43c44-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="43c44-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="43c44-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="43c44-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="43c44-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="43c44-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="43c44-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="43c44-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="43c44-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="43c44-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="43c44-112">Microsoft. ISAM. ESENT. Interop. esentlogtornschreiteduringhardrecoveryexception</span><span class="sxs-lookup"><span data-stu-id="43c44-112">Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException</span></span>  

<span data-ttu-id="43c44-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="43c44-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="43c44-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="43c44-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="43c44-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="43c44-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogTornWriteDuringHardRecoveryException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogTornWriteDuringHardRecoveryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogTornWriteDuringHardRecoveryException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="43c44-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="43c44-116">Thread safety</span></span>

<span data-ttu-id="43c44-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="43c44-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="43c44-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="43c44-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="43c44-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43c44-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="43c44-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="43c44-120">Reference</span></span>

[<span data-ttu-id="43c44-121">Esentlogtornschreiteduringhardrecoveryexception-Member</span><span class="sxs-lookup"><span data-stu-id="43c44-121">EsentLogTornWriteDuringHardRecoveryException members</span></span>](./esentlogtornwriteduringhardrecoveryexception-members.md)

[<span data-ttu-id="43c44-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="43c44-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
