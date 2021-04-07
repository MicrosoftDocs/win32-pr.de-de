---
description: Setzt den Integritäts Status aller Anwendungen auf einem virtuellen Computer zurück.
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: 'Ivmapplicationhealthmonitor:: resetallapplicationstate-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.ResetAllApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: b13781d26c256e41ea6685b19a3097236ebbdb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863567"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a><span data-ttu-id="da284-103">Ivmapplicationhealthmonitor:: resetallapplicationstate-Methode</span><span class="sxs-lookup"><span data-stu-id="da284-103">IVmApplicationHealthMonitor::ResetAllApplicationState method</span></span>

<span data-ttu-id="da284-104">Setzt den Integritäts Status aller Anwendungen auf einem virtuellen Computer zurück.</span><span class="sxs-lookup"><span data-stu-id="da284-104">Resets the health state for all applications in a virtual machine.</span></span> <span data-ttu-id="da284-105">Bei erfolgreicher Ausführung wird der Integritäts Status für alle überwachten Anwendungen auf **applicationstatehealthy** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da284-105">If successful, the health state for all monitored applications will be set to **ApplicationStateHealthy**.</span></span>

## <a name="syntax"></a><span data-ttu-id="da284-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="da284-106">Syntax</span></span>


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a><span data-ttu-id="da284-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="da284-107">Parameters</span></span>

<span data-ttu-id="da284-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="da284-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da284-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da284-109">Return value</span></span>

<span data-ttu-id="da284-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="da284-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="da284-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="da284-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="da284-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da284-112">Remarks</span></span>

<span data-ttu-id="da284-113">Um dieses Programmier Element zu verwenden, müssen die Windows 8-Integrations Komponenten auf dem virtuellen Computer installiert sein, auf dem die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da284-113">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="da284-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da284-114">Requirements</span></span>



| <span data-ttu-id="da284-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da284-115">Requirement</span></span> | <span data-ttu-id="da284-116">Wert</span><span class="sxs-lookup"><span data-stu-id="da284-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da284-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da284-117">Minimum supported client</span></span><br/> | <span data-ttu-id="da284-118">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da284-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="da284-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da284-119">Minimum supported server</span></span><br/> | <span data-ttu-id="da284-120">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da284-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="da284-121">Version</span><span class="sxs-lookup"><span data-stu-id="da284-121">Version</span></span><br/>                  | <span data-ttu-id="da284-122">Integrations Komponenten für Windows 8</span><span class="sxs-lookup"><span data-stu-id="da284-122">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="da284-123">IDL</span><span class="sxs-lookup"><span data-stu-id="da284-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="da284-124"><dt>Vmapplicationhealthmonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="da284-124"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da284-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da284-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da284-126">**Ivmapplicationhealthmonitor**</span><span class="sxs-lookup"><span data-stu-id="da284-126">**IVmApplicationHealthMonitor**</span></span>](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




