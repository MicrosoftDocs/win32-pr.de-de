---
description: 'Weitere Informationen über: vistaapi. JetInit3-Methode'
title: Vistaapi. JetInit3-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetInit3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetinit3(v=EXCHG.10)
ms:contentKeyID: 55104198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c5fa7d1450240a8250e66e2bbe6d8ef0b97c136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372860"
---
# <a name="vistaapijetinit3-method"></a><span data-ttu-id="05210-103">Vistaapi. JetInit3-Methode</span><span class="sxs-lookup"><span data-stu-id="05210-103">VistaApi.JetInit3 method</span></span>

<span data-ttu-id="05210-104">Initialisieren Sie die ESENT-Datenbank-Engine.</span><span class="sxs-lookup"><span data-stu-id="05210-104">Initialize the ESENT database engine.</span></span>

<span data-ttu-id="05210-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="05210-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="05210-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="05210-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="05210-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="05210-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetInit3 ( _
    ByRef instance As JET_INSTANCE, _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit
Dim returnValue As JET_wrn

returnValue = VistaApi.JetInit3(instance, _
    recoveryOptions, grbit)
```

``` csharp
public static JET_wrn JetInit3(
    ref JET_INSTANCE instance,
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="05210-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="05210-108">Parameters</span></span>

  - <span data-ttu-id="05210-109">instance</span><span class="sxs-lookup"><span data-stu-id="05210-109">instance</span></span>  
    <span data-ttu-id="05210-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="05210-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="05210-111">Die-Instanz, die initialisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="05210-111">The instance to initialize.</span></span> <span data-ttu-id="05210-112">Wenn eine Instanz nicht zugeordnet wurde, wird ein neuer erstellt, und die Engine wird im einzelinstanzmodus betrieben.</span><span class="sxs-lookup"><span data-stu-id="05210-112">If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.</span></span>

<!-- end list -->

  - <span data-ttu-id="05210-113">Wiederherstellungsoptionen</span><span class="sxs-lookup"><span data-stu-id="05210-113">recoveryOptions</span></span>  
    <span data-ttu-id="05210-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="05210-114">Type: [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span></span>  
    
    <span data-ttu-id="05210-115">Zusätzliche Wiederherstellungs Parameter zum erneuten Zuordnen von Datenbanken während der Wiederherstellung, zur Position, an der die Wiederherstellung beendet werden soll, oder zur</span><span class="sxs-lookup"><span data-stu-id="05210-115">Additional recovery parameters for remapping databases during recovery, position where to stop recovery at, or recovery status.</span></span>

<!-- end list -->

  - <span data-ttu-id="05210-116">grbit</span><span class="sxs-lookup"><span data-stu-id="05210-116">grbit</span></span>  
    <span data-ttu-id="05210-117">Type: [Microsoft.Isam.Esent.Interop.Initgrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="05210-117">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="05210-118">Initialisierungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="05210-118">Initialization options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="05210-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05210-119">Return value</span></span>

<span data-ttu-id="05210-120">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="05210-120">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="05210-121">Ein Warnungs Code.</span><span class="sxs-lookup"><span data-stu-id="05210-121">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="05210-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05210-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="05210-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="05210-123">Reference</span></span>

[<span data-ttu-id="05210-124">Vistaapi-Klasse</span><span class="sxs-lookup"><span data-stu-id="05210-124">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="05210-125">Vistaapi-Member</span><span class="sxs-lookup"><span data-stu-id="05210-125">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="05210-126">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="05210-126">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
