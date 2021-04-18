---
description: 'Weitere Informationen finden Sie im folgenden Artikel: instanceparameters. waypointlatency-Eigenschaft'
title: Instanceparameters. waypointlatency (Eigenschaft)
TOCTitle: 'WaypointLatency property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.waypointlatency(v=EXCHG.10)
ms:contentKeyID: 55103325
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_WaypointLatency
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d7d837d7fff804926529ec67780e319d85031f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350965"
---
# <a name="instanceparameterswaypointlatency-property"></a><span data-ttu-id="3d35a-103">Instanceparameters. waypointlatency (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3d35a-103">InstanceParameters.WaypointLatency property</span></span>

<span data-ttu-id="3d35a-104">Ruft die Anzahl der Protokolle ab, für die ESENT Daten Bank Leerungen zurück stellt, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="3d35a-104">Gets or sets a the number of logs that esent will defer database flushes for.</span></span> <span data-ttu-id="3d35a-105">Dies kann verwendet werden, um die Wiederherstellbarkeit der Datenbank zu erhöhen, wenn Fehler beim Verlust von Protokolldateien auftreten.</span><span class="sxs-lookup"><span data-stu-id="3d35a-105">This can be used to increase database recoverability if failures cause logfiles to be lost.</span></span> <span data-ttu-id="3d35a-106">Unter Windows 7 und aufwärts unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3d35a-106">Supported on Windows 7 and up.</span></span> <span data-ttu-id="3d35a-107">Wird unter Windows XP, Windows Server 2003, Windows Vista und Windows Server 2008 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3d35a-107">Ignored on Windows XP, Windows Server 2003, Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="3d35a-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3d35a-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3d35a-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3d35a-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3d35a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d35a-110">Syntax</span></span>

``` vb
'Declaration
Public Property WaypointLatency As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.WaypointLatency

instance.WaypointLatency = value
```

``` csharp
public int WaypointLatency { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="3d35a-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3d35a-111">Property value</span></span>

<span data-ttu-id="3d35a-112">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3d35a-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="3d35a-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d35a-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3d35a-114">Referenz</span><span class="sxs-lookup"><span data-stu-id="3d35a-114">Reference</span></span>

[<span data-ttu-id="3d35a-115">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="3d35a-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="3d35a-116">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="3d35a-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="3d35a-117">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="3d35a-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
