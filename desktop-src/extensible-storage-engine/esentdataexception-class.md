---
description: 'Weitere Informationen finden Sie unter: esentdataexception-Klasse'
title: Esentdataexception-Klasse
TOCTitle: EsentDataException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDataException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdataexception(v=EXCHG.10)
ms:contentKeyID: 55101456
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDataException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 996839740d1b008ffae12cf823b9664bf8ca4273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347059"
---
# <a name="esentdataexception-class"></a><span data-ttu-id="c629c-103">Esentdataexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="c629c-103">EsentDataException class</span></span>

<span data-ttu-id="c629c-104">Basisklasse für Daten Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="c629c-104">Base class for Data exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c629c-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="c629c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c629c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c629c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c629c-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c629c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c629c-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="c629c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c629c-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="c629c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="c629c-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="c629c-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>  
          [<span data-ttu-id="c629c-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="c629c-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
          [<span data-ttu-id="c629c-112">Microsoft. ISAM. ESENT. Interop. esentfragmentationexception</span><span class="sxs-lookup"><span data-stu-id="c629c-112">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
          [<span data-ttu-id="c629c-113">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="c629c-113">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  

<span data-ttu-id="c629c-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c629c-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c629c-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c629c-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c629c-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="c629c-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentDataException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentDataException
```

``` csharp
[SerializableAttribute]
public abstract class EsentDataException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="c629c-117">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="c629c-117">Thread safety</span></span>

<span data-ttu-id="c629c-118">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="c629c-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c629c-119">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="c629c-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c629c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c629c-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c629c-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="c629c-121">Reference</span></span>

[<span data-ttu-id="c629c-122">Esentdataexception-Member</span><span class="sxs-lookup"><span data-stu-id="c629c-122">EsentDataException members</span></span>](./esentdataexception-members.md)

[<span data-ttu-id="c629c-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="c629c-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
