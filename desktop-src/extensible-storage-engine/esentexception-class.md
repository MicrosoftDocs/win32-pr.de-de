---
description: 'Weitere Informationen finden Sie unter: esentexception-Klasse'
title: Esentexception-Klasse (Microsoft. ISAM. ESENT)
TOCTitle: EsentException class
ms:assetid: T:Microsoft.Isam.Esent.EsentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100645
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.EsentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.EsentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 775d63c6b1d234696790b1187538a6d1ee734a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353968"
---
# <a name="esentexception-class"></a><span data-ttu-id="439d3-103">Esentexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="439d3-103">EsentException class</span></span>

<span data-ttu-id="439d3-104">Basisklasse für ESENT-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="439d3-104">Base class for ESENT exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="439d3-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="439d3-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="439d3-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="439d3-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="439d3-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="439d3-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    <span data-ttu-id="439d3-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="439d3-108">Microsoft.Isam.Esent.EsentException</span></span>  
      [<span data-ttu-id="439d3-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="439d3-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
      [<span data-ttu-id="439d3-110">Microsoft. ISAM. ESENT. Interop. esentinvalidcolumnexception</span><span class="sxs-lookup"><span data-stu-id="439d3-110">Microsoft.Isam.Esent.Interop.EsentInvalidColumnException</span></span>](./esentinvalidcolumnexception-class.md)  

<span data-ttu-id="439d3-111">**Namespace:**  [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="439d3-111">**Namespace:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)</span></span>  
<span data-ttu-id="439d3-112">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="439d3-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="439d3-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="439d3-113">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentException _
    Inherits Exception
'Usage
Dim instance As EsentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentException : Exception
```

## <a name="thread-safety"></a><span data-ttu-id="439d3-114">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="439d3-114">Thread safety</span></span>

<span data-ttu-id="439d3-115">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="439d3-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="439d3-116">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="439d3-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="439d3-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="439d3-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="439d3-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="439d3-118">Reference</span></span>

[<span data-ttu-id="439d3-119">Esentexception-Member</span><span class="sxs-lookup"><span data-stu-id="439d3-119">EsentException members</span></span>](./esentexception-members.md)

[<span data-ttu-id="439d3-120">Microsoft. ISAM. ESENT-Namespace</span><span class="sxs-lookup"><span data-stu-id="439d3-120">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)
