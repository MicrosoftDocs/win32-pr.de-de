---
description: 'Weitere Informationen finden Sie unter: esentfleiobeyondeofexception-Klasse'
title: Esentspleiobeyondeofexception-Klasse
TOCTitle: EsentFileIOBeyondEOFException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileIOBeyondEOFException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfileiobeyondeofexception(v=EXCHG.10)
ms:contentKeyID: 55101689
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileIOBeyondEOFException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileIOBeyondEOFException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67d7fa0730a265ddb0ed0f37cc6db250325b5a4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351091"
---
# <a name="esentfileiobeyondeofexception-class"></a><span data-ttu-id="dd4a1-103">Esentspleiobeyondeofexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="dd4a1-103">EsentFileIOBeyondEOFException class</span></span>

<span data-ttu-id="dd4a1-104">Basisklasse für JET_err. "Fleiobeyonde of"-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="dd4a1-104">Base class for JET_err.FileIOBeyondEOF exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="dd4a1-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="dd4a1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="dd4a1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="dd4a1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="dd4a1-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="dd4a1-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="dd4a1-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="dd4a1-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="dd4a1-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="dd4a1-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="dd4a1-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="dd4a1-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="dd4a1-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="dd4a1-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="dd4a1-112">Microsoft. ISAM. ESENT. Interop. esentfileiobeyonentofexception</span><span class="sxs-lookup"><span data-stu-id="dd4a1-112">Microsoft.Isam.Esent.Interop.EsentFileIOBeyondEOFException</span></span>  

<span data-ttu-id="dd4a1-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dd4a1-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dd4a1-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dd4a1-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dd4a1-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd4a1-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileIOBeyondEOFException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentFileIOBeyondEOFException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileIOBeyondEOFException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="dd4a1-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="dd4a1-116">Thread safety</span></span>

<span data-ttu-id="dd4a1-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="dd4a1-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="dd4a1-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="dd4a1-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd4a1-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd4a1-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dd4a1-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="dd4a1-120">Reference</span></span>

[<span data-ttu-id="dd4a1-121">Esentmeder Exception-Member</span><span class="sxs-lookup"><span data-stu-id="dd4a1-121">EsentFileIOBeyondEOFException members</span></span>](./esentfileiobeyondeofexception-members.md)

[<span data-ttu-id="dd4a1-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd4a1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
