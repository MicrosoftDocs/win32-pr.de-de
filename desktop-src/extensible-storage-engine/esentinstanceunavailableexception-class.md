---
description: 'Weitere Informationen finden Sie unter: esentinstanceunavailableexception-Klasse'
title: Esentinstanceunavailableexception-Klasse
TOCTitle: EsentInstanceUnavailableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinstanceunavailableexception(v=EXCHG.10)
ms:contentKeyID: 55101879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c3761965a836182480ec934be344322f5b5c6a1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347305"
---
# <a name="esentinstanceunavailableexception-class"></a><span data-ttu-id="71308-103">Esentinstanceunavailableexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="71308-103">EsentInstanceUnavailableException class</span></span>

<span data-ttu-id="71308-104">Basisklasse für JET_err. Instancenicht verfügbar-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="71308-104">Base class for JET_err.InstanceUnavailable exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="71308-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="71308-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="71308-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="71308-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="71308-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="71308-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="71308-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="71308-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="71308-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="71308-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="71308-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="71308-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="71308-111">Microsoft. ISAM. ESENT. Interop. esentfatalexception</span><span class="sxs-lookup"><span data-stu-id="71308-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
            <span data-ttu-id="71308-112">Microsoft. ISAM. ESENT. Interop. esentinstanceunavailableexception</span><span class="sxs-lookup"><span data-stu-id="71308-112">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException</span></span>  

<span data-ttu-id="71308-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="71308-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="71308-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="71308-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="71308-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="71308-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInstanceUnavailableException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentInstanceUnavailableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInstanceUnavailableException : EsentFatalException
```

## <a name="thread-safety"></a><span data-ttu-id="71308-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="71308-116">Thread safety</span></span>

<span data-ttu-id="71308-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="71308-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="71308-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="71308-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="71308-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71308-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="71308-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="71308-120">Reference</span></span>

[<span data-ttu-id="71308-121">Esentinstanceunavailableexception-Member</span><span class="sxs-lookup"><span data-stu-id="71308-121">EsentInstanceUnavailableException members</span></span>](./esentinstanceunavailableexception-members.md)

[<span data-ttu-id="71308-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="71308-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
