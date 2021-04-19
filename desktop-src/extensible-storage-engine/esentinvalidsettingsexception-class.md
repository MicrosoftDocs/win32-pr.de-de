---
description: 'Weitere Informationen finden Sie unter: esentinvalidsettingsexception-Klasse'
title: Esentinvalidsettingsexception-Klasse
TOCTitle: EsentInvalidSettingsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidSettingsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidsettingsexception(v=EXCHG.10)
ms:contentKeyID: 55102084
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidSettingsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidSettingsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb8f3983a906182baf394f2e35a9f7f9e288de01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348630"
---
# <a name="esentinvalidsettingsexception-class"></a><span data-ttu-id="ac8b0-103">Esentinvalidsettingsexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="ac8b0-103">EsentInvalidSettingsException class</span></span>

<span data-ttu-id="ac8b0-104">Basisklasse für JET_err. Invalidsettings-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="ac8b0-104">Base class for JET_err.InvalidSettings exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ac8b0-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="ac8b0-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ac8b0-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ac8b0-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ac8b0-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ac8b0-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ac8b0-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="ac8b0-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ac8b0-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="ac8b0-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ac8b0-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="ac8b0-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="ac8b0-111">Microsoft. ISAM. ESENT. Interop. esentusageexception</span><span class="sxs-lookup"><span data-stu-id="ac8b0-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="ac8b0-112">Microsoft. ISAM. ESENT. Interop. esentinvalidsettingsexception</span><span class="sxs-lookup"><span data-stu-id="ac8b0-112">Microsoft.Isam.Esent.Interop.EsentInvalidSettingsException</span></span>  

<span data-ttu-id="ac8b0-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ac8b0-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ac8b0-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ac8b0-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ac8b0-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac8b0-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidSettingsException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidSettingsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidSettingsException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="ac8b0-116">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="ac8b0-116">Thread safety</span></span>

<span data-ttu-id="ac8b0-117">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="ac8b0-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ac8b0-118">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="ac8b0-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac8b0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac8b0-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ac8b0-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="ac8b0-120">Reference</span></span>

[<span data-ttu-id="ac8b0-121">Esentinvalidsettingsexception-Member</span><span class="sxs-lookup"><span data-stu-id="ac8b0-121">EsentInvalidSettingsException members</span></span>](./esentinvalidsettingsexception-members.md)

[<span data-ttu-id="ac8b0-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ac8b0-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
