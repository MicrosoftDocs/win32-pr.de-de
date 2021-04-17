---
description: Weitere Informationen finden Sie in der Eigenschaft instanceparameters. versionstoretaskqueuemax.
title: Instanceparameters. versionstoretaskqueuemax (Eigenschaft)
TOCTitle: 'VersionStoreTaskQueueMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.VersionStoreTaskQueueMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.versionstoretaskqueuemax(v=EXCHG.10)
ms:contentKeyID: 55103554
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.VersionStoreTaskQueueMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_VersionStoreTaskQueueMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.VersionStoreTaskQueueMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_VersionStoreTaskQueueMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd522fa46df40182b6dfe638e7663df8e9e56c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485867"
---
# <a name="instanceparametersversionstoretaskqueuemax-property"></a><span data-ttu-id="71945-103">Instanceparameters. versionstoretaskqueuemax (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="71945-103">InstanceParameters.VersionStoreTaskQueueMax property</span></span>

<span data-ttu-id="71945-104">Dient zum Abrufen oder Festlegen der Anzahl von Arbeitsaufgaben im Hintergrund Bereinigung, die zu einem beliebigen Zeitpunkt in die Warteschlange des Thread Pools der Datenbank-Engine eingereiht werden können.</span><span class="sxs-lookup"><span data-stu-id="71945-104">Gets or sets the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span>

<span data-ttu-id="71945-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="71945-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="71945-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="71945-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="71945-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="71945-107">Syntax</span></span>

``` vb
'Declaration
Public Property VersionStoreTaskQueueMax As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.VersionStoreTaskQueueMax

instance.VersionStoreTaskQueueMax = value
```

``` csharp
public int VersionStoreTaskQueueMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="71945-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="71945-108">Property value</span></span>

<span data-ttu-id="71945-109">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="71945-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="71945-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71945-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="71945-111">Referenz</span><span class="sxs-lookup"><span data-stu-id="71945-111">Reference</span></span>

[<span data-ttu-id="71945-112">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="71945-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="71945-113">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="71945-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="71945-114">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="71945-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
