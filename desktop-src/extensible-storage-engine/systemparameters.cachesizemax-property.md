---
description: Weitere Informationen finden Sie in der System Parameters. cachesizemax-Eigenschaft.
title: System Parameters. cachesizemax (Eigenschaft)
TOCTitle: 'CacheSizeMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.cachesizemax(v=EXCHG.10)
ms:contentKeyID: 55104037
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.get_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7b03df288a0263cf6b79281f5ed79330dfd641d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218127"
---
# <a name="systemparameterscachesizemax-property"></a><span data-ttu-id="1aabd-103">System Parameters. cachesizemax (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1aabd-103">SystemParameters.CacheSizeMax property</span></span>

<span data-ttu-id="1aabd-104">Ruft die maximale Größe des Cache für die Datenbankseite ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="1aabd-104">Gets or sets the maximum size of the database page cache.</span></span> <span data-ttu-id="1aabd-105">Die Größe befindet sich auf Datenbankseiten.</span><span class="sxs-lookup"><span data-stu-id="1aabd-105">The size is in database pages.</span></span> <span data-ttu-id="1aabd-106">Wenn dieser Parameter auf seinen Standardwert zurückgesetzt wird, wird die maximale Cache Größe auf die Größe des physischen Arbeitsspeichers festgelegt, wenn jetinit aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1aabd-106">If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when JetInit is called.</span></span>

<span data-ttu-id="1aabd-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1aabd-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1aabd-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1aabd-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1aabd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1aabd-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Property CacheSizeMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.CacheSizeMax

SystemParameters.CacheSizeMax = value
```

``` csharp
public static int CacheSizeMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="1aabd-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1aabd-110">Property value</span></span>

<span data-ttu-id="1aabd-111">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1aabd-111">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="1aabd-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1aabd-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1aabd-113">Referenz</span><span class="sxs-lookup"><span data-stu-id="1aabd-113">Reference</span></span>

[<span data-ttu-id="1aabd-114">SystemParameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="1aabd-114">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="1aabd-115">SystemParameters-Member</span><span class="sxs-lookup"><span data-stu-id="1aabd-115">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="1aabd-116">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="1aabd-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
