---
description: 'Weitere Informationen finden Sie unter: API. jetgetinstanceingefo-Methode'
title: API. jetgetinstancinput Info-Methode
TOCTitle: 'JetGetInstanceInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetInstanceInfo(System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetinstanceinfo(v=EXCHG.10)
ms:contentKeyID: 55100729
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetInstanceInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetInstanceInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b618c0eb7bf6e861337ebb40a95cb75d4434038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214498"
---
# <a name="apijetgetinstanceinfo-method"></a><span data-ttu-id="c56c8-103">API. jetgetinstancinput Info-Methode</span><span class="sxs-lookup"><span data-stu-id="c56c8-103">Api.JetGetInstanceInfo method</span></span>

<span data-ttu-id="c56c8-104">Ruft Informationen zu den Instanzen ab, die ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c56c8-104">Retrieves information about the instances that are running.</span></span>

<span data-ttu-id="c56c8-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c56c8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c56c8-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c56c8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c56c8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c56c8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetInstanceInfo ( _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO() _
)
'Usage
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()

Api.JetGetInstanceInfo(numInstances, _
    instances)
```

``` csharp
public static void JetGetInstanceInfo(
    out int numInstances,
    out JET_INSTANCE_INFO[] instances
)
```

#### <a name="parameters"></a><span data-ttu-id="c56c8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c56c8-108">Parameters</span></span>

  - <span data-ttu-id="c56c8-109">numinstance</span><span class="sxs-lookup"><span data-stu-id="c56c8-109">numInstances</span></span>  
    <span data-ttu-id="c56c8-110">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c56c8-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c56c8-111">Gibt die Anzahl von-Instanzen zurück.</span><span class="sxs-lookup"><span data-stu-id="c56c8-111">Returns the number of instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="c56c8-112">instances</span><span class="sxs-lookup"><span data-stu-id="c56c8-112">instances</span></span>  
    <span data-ttu-id="c56c8-113">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="c56c8-113">Type: \[\]</span></span>  
    
    <span data-ttu-id="c56c8-114">Gibt ein Array von instanzinformationsobjekten zurück, eines für jede laufende Instanz.</span><span class="sxs-lookup"><span data-stu-id="c56c8-114">Returns an array of instance info objects, one for each running instance.</span></span>

## <a name="see-also"></a><span data-ttu-id="c56c8-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c56c8-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c56c8-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="c56c8-116">Reference</span></span>

[<span data-ttu-id="c56c8-117">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="c56c8-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c56c8-118">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="c56c8-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c56c8-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="c56c8-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
