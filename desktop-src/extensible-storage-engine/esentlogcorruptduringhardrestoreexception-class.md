---
description: 'Weitere Informationen finden Sie unter: esentlogkorruptduringhardrestoreexception-Klasse'
title: Esentlogkorruptduringhardrestoreexception-Klasse
TOCTitle: EsentLogCorruptDuringHardRestoreException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogcorruptduringhardrestoreexception(v=EXCHG.10)
ms:contentKeyID: 55102073
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: daeabeae72916781e01640cd0de10c737b53e5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218408"
---
# <a name="esentlogcorruptduringhardrestoreexception-class"></a><span data-ttu-id="42dbc-103">Esentlogkorruptduringhardrestoreexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="42dbc-103">EsentLogCorruptDuringHardRestoreException class</span></span>

<span data-ttu-id="42dbc-104">Basisklasse für JET_err. Logkorruptduringhardrestore-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="42dbc-104">Base class for JET_err.LogCorruptDuringHardRestore exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="42dbc-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="42dbc-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="42dbc-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="42dbc-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="42dbc-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="42dbc-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="42dbc-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="42dbc-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="42dbc-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="42dbc-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="42dbc-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="42dbc-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="42dbc-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="42dbc-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="42dbc-112">Microsoft. ISAM. ESENT. Interop. esentlogkorruptduringhardrestoreexception</span><span class="sxs-lookup"><span data-stu-id="42dbc-112">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException</span></span>  

<span data-ttu-id="42dbc-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="42dbc-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="42dbc-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="42dbc-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="42dbc-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="42dbc-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogCorruptDuringHardRestoreException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogCorruptDuringHardRestoreException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogCorruptDuringHardRestoreException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="42dbc-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="42dbc-116">Thread safety</span></span>

<span data-ttu-id="42dbc-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="42dbc-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="42dbc-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="42dbc-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="42dbc-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42dbc-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="42dbc-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="42dbc-120">Reference</span></span>

[<span data-ttu-id="42dbc-121">Esentlogkorruptduringhardrestoreexception-Member</span><span class="sxs-lookup"><span data-stu-id="42dbc-121">EsentLogCorruptDuringHardRestoreException members</span></span>](./esentlogcorruptduringhardrestoreexception-members.md)

[<span data-ttu-id="42dbc-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="42dbc-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
