---
description: 'Weitere Informationen über: Windows8Api. JetStopServiceInstance2-Methode'
title: Windows8Api. JetStopServiceInstance2-Methode (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetStopServiceInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetstopserviceinstance2(v=EXCHG.10)
ms:contentKeyID: 55104460
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0821a00016eb9cd2c511ee37889e0ddaa0b76edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041881"
---
# <a name="windows8apijetstopserviceinstance2-method"></a><span data-ttu-id="cb217-103">Windows8Api. JetStopServiceInstance2-Methode</span><span class="sxs-lookup"><span data-stu-id="cb217-103">Windows8Api.JetStopServiceInstance2 method</span></span>

<span data-ttu-id="cb217-104">Bereitet eine Instanz für die Beendigung vor.</span><span class="sxs-lookup"><span data-stu-id="cb217-104">Prepares an instance for termination.</span></span> <span data-ttu-id="cb217-105">Kann auch verwendet werden, um ein vorheriges versetzen wieder aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="cb217-105">Can also be used to resume a previous quiescing.</span></span>

<span data-ttu-id="cb217-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cb217-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="cb217-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cb217-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cb217-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb217-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetStopServiceInstance2 ( _
    instance As JET_INSTANCE, _
    grbit As StopServiceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As StopServiceGrbitWindows8Api.JetStopServiceInstance2(instance, _
    grbit)
```

``` csharp
public static void JetStopServiceInstance2(
    JET_INSTANCE instance,
    StopServiceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="cb217-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb217-109">Parameters</span></span>

  - <span data-ttu-id="cb217-110">instance</span><span class="sxs-lookup"><span data-stu-id="cb217-110">instance</span></span>  
    <span data-ttu-id="cb217-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cb217-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="cb217-112">Die zu verwendende (laufende) Instanz.</span><span class="sxs-lookup"><span data-stu-id="cb217-112">The (running) instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cb217-113">grbit</span><span class="sxs-lookup"><span data-stu-id="cb217-113">grbit</span></span>  
    <span data-ttu-id="cb217-114">Typ: [Microsoft. ISAM. ESENT. Interop. Windows8. stopservicegrbit](./stopservicegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="cb217-114">Type: [Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit](./stopservicegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="cb217-115">Die Optionen, mit denen die Instanz beendet oder fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb217-115">The options to stop or resume the instance.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb217-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb217-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cb217-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="cb217-117">Reference</span></span>

[<span data-ttu-id="cb217-118">Windows8Api-Klasse</span><span class="sxs-lookup"><span data-stu-id="cb217-118">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="cb217-119">Windows8Api-Member</span><span class="sxs-lookup"><span data-stu-id="cb217-119">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="cb217-120">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="cb217-120">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
