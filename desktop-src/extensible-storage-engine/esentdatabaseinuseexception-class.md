---
description: 'Weitere Informationen finden Sie unter: esentdatabaseingeuseexception-Klasse'
title: Esentdatabaseingeuseexception-Klasse
TOCTitle: EsentDatabaseInUseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseInUseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseinuseexception(v=EXCHG.10)
ms:contentKeyID: 55101372
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInUseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInUseException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8b97ce4cc0a02b322a0abfc882ee0fce398fb04b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862779"
---
# <a name="esentdatabaseinuseexception-class"></a><span data-ttu-id="02217-103">Esentdatabaseingeuseexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="02217-103">EsentDatabaseInUseException class</span></span>

<span data-ttu-id="02217-104">Basisklasse für JET_err. Databaseingeuse-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="02217-104">Base class for JET_err.DatabaseInUse exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="02217-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="02217-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="02217-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="02217-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="02217-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="02217-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="02217-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="02217-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="02217-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="02217-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="02217-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="02217-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="02217-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="02217-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="02217-112">Microsoft. ISAM. ESENT. Interop. esentdatabaseingeuseexception</span><span class="sxs-lookup"><span data-stu-id="02217-112">Microsoft.Isam.Esent.Interop.EsentDatabaseInUseException</span></span>  

<span data-ttu-id="02217-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="02217-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="02217-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="02217-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="02217-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="02217-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseInUseException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseInUseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseInUseException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="02217-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="02217-116">Thread safety</span></span>

<span data-ttu-id="02217-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="02217-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="02217-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="02217-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="02217-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02217-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="02217-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="02217-120">Reference</span></span>

[<span data-ttu-id="02217-121">Esentdatabaseingeuseexception-Member</span><span class="sxs-lookup"><span data-stu-id="02217-121">EsentDatabaseInUseException members</span></span>](./esentdatabaseinuseexception-members.md)

[<span data-ttu-id="02217-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="02217-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
