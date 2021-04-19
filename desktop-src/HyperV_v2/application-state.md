---
description: Gibt den Integritäts Status einer Anwendung an.
ms.assetid: CA06AA34-A549-4CFC-9B52-D2E0B200C3E9
title: APPLICATION_STATE-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPLICATION_STATE
api_type:
- IDLDef
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 4b7e288f41c863dc3f0365db3c6aae867605e5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348617"
---
# <a name="application_state-enumeration"></a><span data-ttu-id="3661d-103">\_Enumeration des Anwendungs Zustands</span><span class="sxs-lookup"><span data-stu-id="3661d-103">APPLICATION\_STATE enumeration</span></span>

<span data-ttu-id="3661d-104">Gibt den Integritäts Status einer Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="3661d-104">Specifies the health state of an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="3661d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3661d-105">Syntax</span></span>


```C++
typedef enum _APPLICATION_STATE { 
  ApplicationStateHealthy   = 0,
  ApplicationStateCritical
} APPLICATION_STATE, *PAPPLICATION_STATE;
```



## <a name="constants"></a><span data-ttu-id="3661d-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="3661d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3661d-107"><span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**Applicationstatuehealthy**</span><span class="sxs-lookup"><span data-stu-id="3661d-107"><span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**</span></span>
</dt> <dd>

<span data-ttu-id="3661d-108">Der Anwendungs Status ist fehlerfrei.</span><span class="sxs-lookup"><span data-stu-id="3661d-108">The application state is healthy.</span></span>

</dd> <dt>

<span data-ttu-id="3661d-109"><span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**Applicationstatuecritical**</span><span class="sxs-lookup"><span data-stu-id="3661d-109"><span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**</span></span>
</dt> <dd>

<span data-ttu-id="3661d-110">Der Anwendungs Status ist kritisch.</span><span class="sxs-lookup"><span data-stu-id="3661d-110">The application state is critical.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3661d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3661d-111">Remarks</span></span>

<span data-ttu-id="3661d-112">Um dieses Programmier Element zu verwenden, müssen die Windows 8-Integrations Komponenten auf dem virtuellen Computer installiert sein, auf dem die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3661d-112">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="3661d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3661d-113">Requirements</span></span>



| <span data-ttu-id="3661d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3661d-114">Requirement</span></span> | <span data-ttu-id="3661d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3661d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3661d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3661d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3661d-117">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3661d-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="3661d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3661d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3661d-119">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3661d-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3661d-120">Version</span><span class="sxs-lookup"><span data-stu-id="3661d-120">Version</span></span><br/>                  | <span data-ttu-id="3661d-121">Integrations Komponenten für Windows 8</span><span class="sxs-lookup"><span data-stu-id="3661d-121">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="3661d-122">IDL</span><span class="sxs-lookup"><span data-stu-id="3661d-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3661d-123"><dt>Vmapplicationhealthmonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3661d-123"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3661d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3661d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3661d-125">**"Standort Status"**</span><span class="sxs-lookup"><span data-stu-id="3661d-125">**SetApplicationState**</span></span>](ivmapplicationhealthmonitor-setapplicationstate.md)
</dt> </dl>

 

 




