---
description: 'Weitere Informationen finden Sie unter: Instance.Init-Methode (JET_RSTINFO, initgrbit)'
title: Instance.Init-Methode (JET_RSTINFO, initgrbit)
TOCTitle: Init method (JET_RSTINFO, InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103274
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1945b0119053a2759b57b8781b86cf682b3a364c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354544"
---
# <a name="instanceinit-method-jet_rstinfo-initgrbit"></a><span data-ttu-id="bd36c-103">Instance.Init-Methode (JET_RSTINFO, initgrbit)</span><span class="sxs-lookup"><span data-stu-id="bd36c-103">Instance.Init method (JET_RSTINFO, InitGrbit)</span></span>

<span data-ttu-id="bd36c-104">Initialisieren Sie die JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="bd36c-104">Initialize the JET_INSTANCE.</span></span> <span data-ttu-id="bd36c-105">Diese API erfordert mindestens die Vista-Version von ESENT.</span><span class="sxs-lookup"><span data-stu-id="bd36c-105">This API requires at least the Vista version of ESENT.</span></span>

<span data-ttu-id="bd36c-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bd36c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bd36c-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bd36c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bd36c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd36c-108">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit

instance.Init(recoveryOptions, grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="bd36c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd36c-109">Parameters</span></span>

  - <span data-ttu-id="bd36c-110">Wiederherstellungsoptionen</span><span class="sxs-lookup"><span data-stu-id="bd36c-110">recoveryOptions</span></span>  
    <span data-ttu-id="bd36c-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="bd36c-111">Type: [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span></span>  
    
    <span data-ttu-id="bd36c-112">Zusätzliche Wiederherstellungs Parameter zum erneuten Zuordnen von Datenbanken während der Wiederherstellung, zur Position, an der die Wiederherstellung beendet werden soll, oder zur</span><span class="sxs-lookup"><span data-stu-id="bd36c-112">Additional recovery parameters for remapping databases during recovery, position where to stop recovery at, or recovery status.</span></span>

<!-- end list -->

  - <span data-ttu-id="bd36c-113">grbit</span><span class="sxs-lookup"><span data-stu-id="bd36c-113">grbit</span></span>  
    <span data-ttu-id="bd36c-114">Type: [Microsoft.Isam.Esent.Interop.Initgrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bd36c-114">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="bd36c-115">Initialisierungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="bd36c-115">Initialization options.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd36c-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd36c-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bd36c-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="bd36c-117">Reference</span></span>

[<span data-ttu-id="bd36c-118">Instanzklasse</span><span class="sxs-lookup"><span data-stu-id="bd36c-118">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="bd36c-119">Instanzmember</span><span class="sxs-lookup"><span data-stu-id="bd36c-119">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="bd36c-120">Init-Überladung</span><span class="sxs-lookup"><span data-stu-id="bd36c-120">Init overload</span></span>](./instance.init-method2.md)

[<span data-ttu-id="bd36c-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="bd36c-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
