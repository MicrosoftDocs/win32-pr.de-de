---
description: 'Weitere Informationen finden Sie hier: System Parameters. startflushthreshold-Eigenschaft'
title: System Parameters. startflushthreshold (Eigenschaft)
TOCTitle: 'StartFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.startflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104050
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StartFlushThreshold
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0e520682253d7a586c36366d229be59e014c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347969"
---
# <a name="systemparametersstartflushthreshold-property"></a><span data-ttu-id="12b9b-103">System Parameters. startflushthreshold (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="12b9b-103">SystemParameters.StartFlushThreshold property</span></span>

<span data-ttu-id="12b9b-104">Ruft den Schwellenwert ab oder legt diesen fest, an dem der Datenbankseiten Cache mit der Überprüfung von Seiten aus dem Cache beginnt, um Platz für nicht zwischengespeicherte Seiten zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="12b9b-104">Gets or sets the threshold at which the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="12b9b-105">Wenn die Anzahl der Seiten Puffer im Cache unter diesen Schwellenwert fällt, wird ein Hintergrundprozess gestartet, um den Pool der verfügbaren Puffer aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="12b9b-105">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="12b9b-106">Dieser Schwellenwert ist immer relativ zur maximalen Cache Größe, die von JET_paramCacheSizeMax festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="12b9b-106">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="12b9b-107">Dieser Schwellenwert muss auch immer niedriger als der von JET_paramStopFlushThreshold festgelegte Schwellenwert sein.</span><span class="sxs-lookup"><span data-stu-id="12b9b-107">This threshold must also always be less than the stop threshold as set by JET_paramStopFlushThreshold.</span></span> <span data-ttu-id="12b9b-108">Die Entfernungs Höhe des Start Schwellenwerts bestimmt die Antwortzeit, die der Datenbankseiten Cache aufweisen muss, damit verfügbare Puffer erstellt werden, bevor die Anwendung Sie benötigt.</span><span class="sxs-lookup"><span data-stu-id="12b9b-108">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="12b9b-109">Ein Schwellenwert für hohe Starts gibt dem Hintergrundprozess mehr Zeit für die Reaktion.</span><span class="sxs-lookup"><span data-stu-id="12b9b-109">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="12b9b-110">Ein Schwellenwert für hohe Starts impliziert jedoch einen höheren Schwellenwert für die Beendigung, wodurch die effektive Größe des Datenbankseiten Caches verringert wird.</span><span class="sxs-lookup"><span data-stu-id="12b9b-110">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache.</span></span>

<span data-ttu-id="12b9b-111">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="12b9b-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="12b9b-112">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="12b9b-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="12b9b-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="12b9b-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property StartFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StartFlushThreshold

SystemParameters.StartFlushThreshold = value
```

``` csharp
public static int StartFlushThreshold { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="12b9b-114">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="12b9b-114">Property value</span></span>

<span data-ttu-id="12b9b-115">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="12b9b-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="12b9b-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12b9b-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="12b9b-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="12b9b-117">Reference</span></span>

[<span data-ttu-id="12b9b-118">SystemParameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="12b9b-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="12b9b-119">SystemParameters-Member</span><span class="sxs-lookup"><span data-stu-id="12b9b-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="12b9b-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="12b9b-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
