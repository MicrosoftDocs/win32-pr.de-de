---
description: Legt den Integritäts Status einer Anwendung fest, die auf einem virtuellen Computer ausgeführt wird.
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: 'Ivmapplicationhealthmonitor:: stapplicationstate-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.SetApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 8e6c64ecec827f6f75f382fbca7aadf8fc0c7dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348511"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a><span data-ttu-id="fe6b6-103">Ivmapplicationhealthmonitor:: stapplicationstate-Methode</span><span class="sxs-lookup"><span data-stu-id="fe6b6-103">IVmApplicationHealthMonitor::SetApplicationState method</span></span>

<span data-ttu-id="fe6b6-104">Legt den Integritäts Status einer Anwendung fest, die auf einem virtuellen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-104">Sets the health state of an application that is running in a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe6b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe6b6-105">Syntax</span></span>


```C++
HRESULT SetApplicationState(
  [in] BSTR              Id,
  [in] BSTR              Name,
  [in] APPLICATION_STATE State
);
```



## <a name="parameters"></a><span data-ttu-id="fe6b6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe6b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe6b6-107">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe6b6-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6b6-108">Eine **BSTR** -Darstellung der **GUID** , die die Anwendung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-108">A **BSTR** representation of the **GUID** that identifies the application.</span></span> <span data-ttu-id="fe6b6-109">Es liegt in der Verantwortung der aufrufenden Anwendung, die Bezeichner zu erstellen und zu verwalten, die für die überwachten Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-109">It is the calling application's responsibility to create and maintain the identifiers it uses for the applications being monitored.</span></span>

</dd> <dt>

<span data-ttu-id="fe6b6-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe6b6-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6b6-111">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-111">The display name of the application.</span></span> <span data-ttu-id="fe6b6-112">Dieser Name wird in einem Informations Ereignis-Protokolleintrag für die Zustandsänderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-112">This name is used in an informational event log entry for the state change.</span></span>

</dd> <dt>

<span data-ttu-id="fe6b6-113">*Status* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe6b6-113">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6b6-114">Ein Wert der Enumeration des [**Anwendungs \_ Zustands**](application-state.md) , der den neuen Integritäts Status der Anwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-114">A value of the [**APPLICATION\_STATE**](application-state.md) enumeration that specifies the new health state of the application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe6b6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe6b6-115">Return value</span></span>

<span data-ttu-id="fe6b6-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fe6b6-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe6b6-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe6b6-118">Remarks</span></span>

<span data-ttu-id="fe6b6-119">Der Status der Anwendungen, die auf dem virtuellen Computer ausgeführt werden, wird im Eigenschafts Wert **OperationalStatus** \[ 1 \] der [**MSVM-Klasse \_ heartbeatcomponent**](msvm-heartbeatcomponent.md) widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-119">The state of the applications running in the virtual machine are reflected in the **OperationalStatus**\[1\] property value of the [**Msvm\_HeartbeatComponent**](msvm-heartbeatcomponent.md) class.</span></span>

<span data-ttu-id="fe6b6-120">Um dieses Programmier Element zu verwenden, müssen die Windows 8-Integrations Komponenten auf dem virtuellen Computer installiert sein, auf dem die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-120">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe6b6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe6b6-121">Requirements</span></span>



| <span data-ttu-id="fe6b6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe6b6-122">Requirement</span></span> | <span data-ttu-id="fe6b6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="fe6b6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe6b6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe6b6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fe6b6-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe6b6-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="fe6b6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe6b6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fe6b6-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe6b6-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fe6b6-128">Version</span><span class="sxs-lookup"><span data-stu-id="fe6b6-128">Version</span></span><br/>                  | <span data-ttu-id="fe6b6-129">Integrations Komponenten für Windows 8</span><span class="sxs-lookup"><span data-stu-id="fe6b6-129">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="fe6b6-130">IDL</span><span class="sxs-lookup"><span data-stu-id="fe6b6-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fe6b6-131"><dt>Vmapplicationhealthmonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fe6b6-131"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe6b6-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe6b6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe6b6-133">**Ivmapplicationhealthmonitor**</span><span class="sxs-lookup"><span data-stu-id="fe6b6-133">**IVmApplicationHealthMonitor**</span></span>](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




