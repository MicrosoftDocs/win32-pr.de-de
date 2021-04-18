---
description: 'Weitere Informationen finden Sie hier: vistaapi. jetgetthreadstats-Methode'
title: Vistaapi. jetgetthreadstats-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetGetThreadStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetthreadstats(v=EXCHG.10)
ms:contentKeyID: 55104192
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 92572fd538f0c6c2643e7b40a07ac168ae6980d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347882"
---
# <a name="vistaapijetgetthreadstats-method"></a><span data-ttu-id="3d4e2-103">Vistaapi. jetgetthreadstats-Methode</span><span class="sxs-lookup"><span data-stu-id="3d4e2-103">VistaApi.JetGetThreadStats method</span></span>

<span data-ttu-id="3d4e2-104">Ruft Leistungsinformationen aus der Datenbank-Engine für den aktuellen Thread ab.</span><span class="sxs-lookup"><span data-stu-id="3d4e2-104">Retrieves performance information from the database engine for the current thread.</span></span> <span data-ttu-id="3d4e2-105">Mehrere Aufrufe können verwendet werden, um Statistiken zu sammeln, die die Aktivität der Datenbank-Engine in diesem Thread zwischen diesen Aufrufen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="3d4e2-105">Multiple calls can be used to collect statistics that reflect the activity of the database engine on this thread between those calls.</span></span>

<span data-ttu-id="3d4e2-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3d4e2-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="3d4e2-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3d4e2-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3d4e2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d4e2-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetThreadStats ( _
    <OutAttribute> ByRef threadstats As JET_THREADSTATS _
)
'Usage
Dim threadstats As JET_THREADSTATSVistaApi.JetGetThreadStats(threadstats)
```

``` csharp
public static void JetGetThreadStats(
    out JET_THREADSTATS threadstats
)
```

#### <a name="parameters"></a><span data-ttu-id="3d4e2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d4e2-109">Parameters</span></span>

  - <span data-ttu-id="3d4e2-110">threadstats</span><span class="sxs-lookup"><span data-stu-id="3d4e2-110">threadstats</span></span>  
    <span data-ttu-id="3d4e2-111">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="3d4e2-111">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="3d4e2-112">Gibt die Thread Statistikdaten zurück.</span><span class="sxs-lookup"><span data-stu-id="3d4e2-112">Returns the thread statistics data.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d4e2-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d4e2-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3d4e2-114">Referenz</span><span class="sxs-lookup"><span data-stu-id="3d4e2-114">Reference</span></span>

[<span data-ttu-id="3d4e2-115">Vistaapi-Klasse</span><span class="sxs-lookup"><span data-stu-id="3d4e2-115">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="3d4e2-116">Vistaapi-Member</span><span class="sxs-lookup"><span data-stu-id="3d4e2-116">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="3d4e2-117">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="3d4e2-117">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
