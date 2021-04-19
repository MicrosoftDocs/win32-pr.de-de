---
description: 'Weitere Informationen finden Sie unter: esentunicodetranslationfailexception-Klasse'
title: Esentunicodetranslationfailexception-Klasse
TOCTitle: EsentUnicodeTranslationFailException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationFailException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentunicodetranslationfailexception(v=EXCHG.10)
ms:contentKeyID: 55103154
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationFailException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationFailException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 65ee73df853a5dc64f3df4a05a192099ac943f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355442"
---
# <a name="esentunicodetranslationfailexception-class"></a><span data-ttu-id="be8c4-103">Esentunicodetranslationfailexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="be8c4-103">EsentUnicodeTranslationFailException class</span></span>

<span data-ttu-id="be8c4-104">Basisklasse für JET_err. Unicodetranslationfail-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="be8c4-104">Base class for JET_err.UnicodeTranslationFail exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="be8c4-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="be8c4-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="be8c4-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="be8c4-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="be8c4-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="be8c4-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="be8c4-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="be8c4-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="be8c4-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="be8c4-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="be8c4-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="be8c4-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="be8c4-111">Microsoft. ISAM. ESENT. Interop. esentunicodetranslationfailexception</span><span class="sxs-lookup"><span data-stu-id="be8c4-111">Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationFailException</span></span>  

<span data-ttu-id="be8c4-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="be8c4-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="be8c4-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="be8c4-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="be8c4-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="be8c4-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentUnicodeTranslationFailException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentUnicodeTranslationFailException
```

``` csharp
[SerializableAttribute]
public sealed class EsentUnicodeTranslationFailException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="be8c4-115">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="be8c4-115">Thread safety</span></span>

<span data-ttu-id="be8c4-116">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="be8c4-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="be8c4-117">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="be8c4-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="be8c4-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be8c4-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="be8c4-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="be8c4-119">Reference</span></span>

[<span data-ttu-id="be8c4-120">Esentunicodetranslationfailexception-Elemente</span><span class="sxs-lookup"><span data-stu-id="be8c4-120">EsentUnicodeTranslationFailException members</span></span>](./esentunicodetranslationfailexception-members.md)

[<span data-ttu-id="be8c4-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="be8c4-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
