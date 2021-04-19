---
description: 'Weitere Informationen finden Sie unter: esentdatabasein completeupgradeexception-Klasse'
title: Esentdatabaseingecompleteupgradeexception-Klasse
TOCTitle: EsentDatabaseIncompleteUpgradeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseincompleteupgradeexception(v=EXCHG.10)
ms:contentKeyID: 55101371
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ae6272559c537ae870794a9d5a7a76bb8672b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345131"
---
# <a name="esentdatabaseincompleteupgradeexception-class"></a><span data-ttu-id="44124-103">Esentdatabaseingecompleteupgradeexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="44124-103">EsentDatabaseIncompleteUpgradeException class</span></span>

<span data-ttu-id="44124-104">Basisklasse für JET_err. Databaseingecompleteupgrade-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="44124-104">Base class for JET_err.DatabaseIncompleteUpgrade exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="44124-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="44124-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="44124-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="44124-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="44124-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="44124-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="44124-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="44124-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="44124-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="44124-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="44124-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="44124-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="44124-111">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="44124-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="44124-112">Microsoft. ISAM. ESENT. Interop. esentdatabasincompleteupgrade Exception</span><span class="sxs-lookup"><span data-stu-id="44124-112">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException</span></span>  

<span data-ttu-id="44124-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="44124-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="44124-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="44124-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="44124-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="44124-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseIncompleteUpgradeException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseIncompleteUpgradeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseIncompleteUpgradeException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="44124-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="44124-116">Thread safety</span></span>

<span data-ttu-id="44124-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="44124-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="44124-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="44124-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="44124-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44124-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="44124-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="44124-120">Reference</span></span>

[<span data-ttu-id="44124-121">Esentdatabaseingecompleteupgrade Exception-Member</span><span class="sxs-lookup"><span data-stu-id="44124-121">EsentDatabaseIncompleteUpgradeException members</span></span>](./esentdatabaseincompleteupgradeexception-members.md)

[<span data-ttu-id="44124-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="44124-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
