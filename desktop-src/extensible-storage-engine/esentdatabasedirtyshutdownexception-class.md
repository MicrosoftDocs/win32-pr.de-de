---
description: 'Weitere Informationen finden Sie unter: esentdatabasedirtyshutdownexception-Klasse'
title: Esentdatabasedirtyshutdownexception-Klasse
TOCTitle: EsentDatabaseDirtyShutdownException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasedirtyshutdownexception(v=EXCHG.10)
ms:contentKeyID: 55101339
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7fcb7a3dffd5626bcf8bfc926103951747ee07e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214720"
---
# <a name="esentdatabasedirtyshutdownexception-class"></a><span data-ttu-id="77635-103">Esentdatabasedirtyshutdownexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="77635-103">EsentDatabaseDirtyShutdownException class</span></span>

<span data-ttu-id="77635-104">Basisklasse für JET_err. Databasedirtyshutdown-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="77635-104">Base class for JET_err.DatabaseDirtyShutdown exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="77635-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="77635-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="77635-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="77635-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="77635-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="77635-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="77635-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="77635-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="77635-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="77635-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="77635-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="77635-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="77635-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="77635-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="77635-112">Microsoft. ISAM. ESENT. Interop. esentdatabasedirtyshutdownexception</span><span class="sxs-lookup"><span data-stu-id="77635-112">Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException</span></span>  

<span data-ttu-id="77635-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="77635-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="77635-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="77635-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="77635-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="77635-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseDirtyShutdownException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentDatabaseDirtyShutdownException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseDirtyShutdownException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="77635-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="77635-116">Thread safety</span></span>

<span data-ttu-id="77635-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="77635-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="77635-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="77635-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="77635-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77635-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="77635-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="77635-120">Reference</span></span>

[<span data-ttu-id="77635-121">Esentdatabasedirtyshutdownexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="77635-121">EsentDatabaseDirtyShutdownException members</span></span>](./esentdatabasedirtyshutdownexception-members.md)

[<span data-ttu-id="77635-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="77635-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
