---
description: 'Weitere Informationen finden Sie hier: vistaapi. jetgetinstancefehlinfo-Methode'
title: Vistaapi. jetgetinstancefehlinfo-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetGetInstanceMiscInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE@,Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetinstancemiscinfo(v=EXCHG.10)
ms:contentKeyID: 55104187
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 204beee343a717d5b45d8003e123bbbe186437d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863692"
---
# <a name="vistaapijetgetinstancemiscinfo-method"></a><span data-ttu-id="d68a5-103">Vistaapi. jetgetinstancefehlinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="d68a5-103">VistaApi.JetGetInstanceMiscInfo method</span></span>

<span data-ttu-id="d68a5-104">Ruft Informationen zu einer-Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="d68a5-104">Retrieves information about an instance.</span></span>

<span data-ttu-id="d68a5-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d68a5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="d68a5-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d68a5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d68a5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d68a5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetInstanceMiscInfo ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef signature As JET_SIGNATURE, _
    infoLevel As JET_InstanceMiscInfo _
)
'Usage
Dim instance As JET_INSTANCE
Dim signature As JET_SIGNATURE
Dim infoLevel As JET_InstanceMiscInfoVistaApi.JetGetInstanceMiscInfo(instance, _
    signature, infoLevel)
```

``` csharp
public static void JetGetInstanceMiscInfo(
    JET_INSTANCE instance,
    out JET_SIGNATURE signature,
    JET_InstanceMiscInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="d68a5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d68a5-108">Parameters</span></span>

  - <span data-ttu-id="d68a5-109">instance</span><span class="sxs-lookup"><span data-stu-id="d68a5-109">instance</span></span>  
    <span data-ttu-id="d68a5-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d68a5-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="d68a5-111">Die-Instanz, über die Informationen erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="d68a5-111">The instance to get information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="d68a5-112">signature</span><span class="sxs-lookup"><span data-stu-id="d68a5-112">signature</span></span>  
    <span data-ttu-id="d68a5-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d68a5-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="d68a5-114">Informationen wurden abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d68a5-114">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="d68a5-115">infolevel</span><span class="sxs-lookup"><span data-stu-id="d68a5-115">infoLevel</span></span>  
    <span data-ttu-id="d68a5-116">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d68a5-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="d68a5-117">Der Typ der abzurufenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="d68a5-117">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="d68a5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d68a5-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d68a5-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="d68a5-119">Reference</span></span>

[<span data-ttu-id="d68a5-120">Vistaapi-Klasse</span><span class="sxs-lookup"><span data-stu-id="d68a5-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="d68a5-121">Vistaapi-Member</span><span class="sxs-lookup"><span data-stu-id="d68a5-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="d68a5-122">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="d68a5-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
