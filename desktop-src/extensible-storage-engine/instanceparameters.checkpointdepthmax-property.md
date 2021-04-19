---
description: Weitere Informationen finden Sie in der Eigenschaft instanceparameters. CheckpointDepthMax.
title: Instanceparameters. CheckpointDepthMax (Eigenschaft)
TOCTitle: 'CheckpointDepthMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.checkpointdepthmax(v=EXCHG.10)
ms:contentKeyID: 55103294
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CheckpointDepthMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CheckpointDepthMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3addab0356206577eda22119ddce81721e9c2bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355573"
---
# <a name="instanceparameterscheckpointdepthmax-property"></a><span data-ttu-id="20686-103">Instanceparameters. CheckpointDepthMax (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="20686-103">InstanceParameters.CheckpointDepthMax property</span></span>

<span data-ttu-id="20686-104">Ruft den Schwellenwert in Bytes für die Anzahl der Transaktionsprotokoll Dateien ab, die nach einem Absturz wiedergegeben werden müssen, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="20686-104">Gets or sets the threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span> <span data-ttu-id="20686-105">Wenn die zirkuläre Protokollierung mithilfe von circularlog aktiviert wird, steuert dieser Parameter auch die ungefähre Menge an Transaktionsprotokoll Dateien, die auf dem Datenträger aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="20686-105">If circular logging is enabled using CircularLog then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span>

<span data-ttu-id="20686-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="20686-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="20686-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="20686-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="20686-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="20686-108">Syntax</span></span>

``` vb
'Declaration
Public Property CheckpointDepthMax As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.CheckpointDepthMax

instance.CheckpointDepthMax = value
```

``` csharp
public int CheckpointDepthMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="20686-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="20686-109">Property value</span></span>

<span data-ttu-id="20686-110">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="20686-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="20686-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20686-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="20686-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="20686-112">Reference</span></span>

[<span data-ttu-id="20686-113">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="20686-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="20686-114">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="20686-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="20686-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="20686-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
