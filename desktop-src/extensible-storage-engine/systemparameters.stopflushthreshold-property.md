---
description: 'Weitere Informationen finden Sie hier: System Parameters. stopflushthreshold-Eigenschaft'
title: System Parameters. stopflushthreshold (Eigenschaft)
TOCTitle: 'StopFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.stopflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104130
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b79a9e5894de6539e8ab7dc0db4218b5f6cb3bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347968"
---
# <a name="systemparametersstopflushthreshold-property"></a><span data-ttu-id="48ecd-103">System Parameters. stopflushthreshold (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="48ecd-103">SystemParameters.StopFlushThreshold property</span></span>

<span data-ttu-id="48ecd-104">Ruft den Schwellenwert ab, an dem der Datenbankseiten Cache die Überprüfung von Seiten aus dem Cache beendet, um Platz für nicht zwischengespeicherte Seiten zu schaffen, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="48ecd-104">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="48ecd-105">Wenn die Anzahl der Seiten Puffer im Cache über diesem Schwellenwert liegt, wird der Hintergrundprozess beendet, der zum Auffüllen dieses Pools verfügbarer Puffer gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="48ecd-105">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="48ecd-106">Dieser Schwellenwert ist immer relativ zur maximalen Cache Größe, die von JET_paramCacheSizeMax festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="48ecd-106">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="48ecd-107">Dieser Schwellenwert muss auch immer größer sein als der Start Schwellenwert, der durch JET_paramStartFlushThreshold festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="48ecd-107">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="48ecd-108">Der Abstand zwischen dem Start Schwellenwert und dem Schwellenwert für das Abbrechen wirkt sich auf die Effizienz aus, mit der Datenbankseiten durch den Hintergrundprozess geleert werden.</span><span class="sxs-lookup"><span data-stu-id="48ecd-108">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="48ecd-109">Eine größere Lücke macht es wahrscheinlicher, dass Schreibvorgänge auf benachbarte Seiten möglicherweise kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="48ecd-109">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="48ecd-110">Ein Schwellenwert für hohe Beendigung verringert jedoch die effektive Größe des Datenbankseiten Caches.</span><span class="sxs-lookup"><span data-stu-id="48ecd-110">However, a high stop threshold will reduce the effective size of the database page cache.</span></span>

<span data-ttu-id="48ecd-111">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="48ecd-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="48ecd-112">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="48ecd-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="48ecd-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="48ecd-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property StopFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StopFlushThreshold

SystemParameters.StopFlushThreshold = value
```

``` csharp
public static int StopFlushThreshold { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="48ecd-114">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="48ecd-114">Property value</span></span>

<span data-ttu-id="48ecd-115">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="48ecd-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="48ecd-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48ecd-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="48ecd-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="48ecd-117">Reference</span></span>

[<span data-ttu-id="48ecd-118">SystemParameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="48ecd-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="48ecd-119">SystemParameters-Member</span><span class="sxs-lookup"><span data-stu-id="48ecd-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="48ecd-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="48ecd-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
